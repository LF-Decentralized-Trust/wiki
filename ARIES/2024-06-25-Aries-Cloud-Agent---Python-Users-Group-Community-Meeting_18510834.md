1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2024](ACA-Pug-Meetings-2024_18519005.html)

# Hyperledger Aries : 2024-06-25 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Jun 27, 2024

## Summary:

Topics:

- PRs and Issues
- LTS Handling - Issue #, PR
- Questions from Anonyome Labs
- 1.0.0 Progress
- Open Discussion

## **Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Documentation:

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Open [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)
- Open [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues):
- Anything hot that should be addressed before 1.0.0rc0?
  
  - - Perhaps: [3055](https://github.com/hyperledger/aries-cloudagent-python/issues/3055), [3020](https://github.com/hyperledger/aries-cloudagent-python/issues/3020), [3018](https://github.com/hyperledger/aries-cloudagent-python/issues/3018), [2999](https://github.com/hyperledger/aries-cloudagent-python/issues/2999), [2895](https://github.com/hyperledger/aries-cloudagent-python/issues/2895)
- LTS Handling - Issue [#2993](https://github.com/hyperledger/aries-cloudagent-python/issues/2993), PR [#3051](https://github.com/hyperledger/aries-cloudagent-python/pull/3051)
  
  - Outlines the strategy
  - Commits to LTS for 0.11.1 and 0.12.0
  - Initial Questions:
    
    - Policy for setting end dates for LTS.
    - Release number for an LTS – seems we need both a minor number to be the LTS (e.g., 0.11.1), but we also need to have additional releases on the branch for identified vulnerabilities – how does that work?
    - How are we notified of only the dependabot vulnerabilities that need fixing in an LTS?
- Questions from [John Court (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5e78520461dfd90c309d7d99?ref=confluence) of Anonyome Labs about Universal DID Support:
  
  - Universal DID Resolver support is there using the --universal-resolver switch to set server location (we actually have deployed this to support cheqd DIDs locally).
    
    - Supported – directly in ACA-Py.
  - The AnonCreds abstraction for native registrar and resolver implementation of AnonCred VC objects exists, being defined in aries\_cloudagent/anaoncreds/base.py. Currently the only concrete implemenations I see is for legacy\_indy in aries\_cloudagent/anoncreds/default/legacy\_indy/. The other default implementations seem to mostly have "NotImplemented" for most methods. This means someone could write a native AnonCreds registrar/resolver for other VDRs (e.g. cheqd). There is however no Universal AnonCreds equivalent community project to the Universal Resolver/Registrar that I can find.
    
    - This is correct. Immediate goal is to get did:indy and did:tdw as the next concrete use cases.
  - The real missing piece for me seems to be there is still no abstraction of the DID Registrar concept with that functionality still being tied to the aries\_cloudagent/ledger code which is indy specific. This seems to be the point of [https://github.com/hyperledger/aries-cloudagent-python/issues/1876](https://github.com/hyperledger/aries-cloudagent-python/issues/1876 "https://github.com/hyperledger/aries-cloudagent-python/issues/1876") to resolve but has stagnated since 2022 ?
    
    - Attempted twice, and the conclusion seems to be that a Universal Registrar is a false optimization for ACA-Py – DIDs are too variable, and as such, the plugin approach is more appropriate, allowing a deployment to pick their own.
    - did:web would be a good example, as will did:tdw.
    - Infrastructure is there for adding an admin interface and secrets access via a plugin.
    - [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence) has been trying out GoDIDdy to see the range of types, and agrees that the plugin approach is more appropriate – deployments could add whatever plugins needed for an instance.
      
      - Plugins should be documented in ACA-Py for how to do that – plugins in general, DID Registrar plugins specifically.  aries-acapy-plugins is the place for them.
  - The tails-server is currently indy specific and has no abstraction layer to deal with reading revocation registry data from non-indy VDRs.
    
    - This should probably be changed to "anoncreds-tails-server".
    - When ledger-agnostic AnonCreds was implemented, extra endpoints were added (with some verification), and the older Indy endpoints are still there with verifications tied to Indy.
    - Should we extend out the functionality of what amounts to a file server to support other kinds of things – e.g. BitStringStatusList VCs, etc.?  Generally yes, but the verification/authorization checks need to be appropriately applied.
    - Question: What authorization is implemented in a Tails Server deployment?
      
      - Endpoints are locked behind a reverse proxy so that only the issuers can write to the ledger.
      - The tails files are hash checked, so you could not override an existing file.
- Question: Possible issue with the `--preserve-exchange-records`  flag in acapy
  
  - If you don't have that flag enabled, there is no way to complete a proof request if you are the verifier.
  - Should only be deleted AFTER the web-hook has fired to notify the controller.
    
    - The web-hook is coming back as a "terse web-hook", that does not have sufficient information, and then it is a race condition between the controller and the deleter.
    - Likely the fix needs to be making sure the webhook has sufficient info.
- Getting to a default Arm friendly release.
  
  - Any progress?  Nothing yet.
  - Issue posted to Mattr with a request. [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) to follow up with the them and failing that – we look for an alternative.
- Other hot issues.
- Open Discussion

## Upcoming Meeting Topics:

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
