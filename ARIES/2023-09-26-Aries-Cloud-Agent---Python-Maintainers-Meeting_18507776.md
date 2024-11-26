1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Py Maintainers Meetings](ACA-Py-Maintainers-Meetings_18506202.html)

# Hyperledger Aries : 2023-09-26 Aries Cloud Agent - Python Maintainers Meeting

Created by Stephen Curran, last modified by Sean Bohan on Sep 27, 2023

## Summary:

Topics:

- 0.10.3? #2486
- Timing/Content for the next release
- Offer to implement OpenID4VCs – guidance?
- AnonCreds RS in ACA-Py progress/next steps
- Open PR / High Priority Issues
- Open Discussion

**Zoom Link**: [https://zoom.us/j/91279968714?pwd=Yk9GVVNLOFE1cklkSk51UEZQTklOQT09](https://zoom.us/j/91279968714?pwd=Yk9GVVNLOFE1cklkSk51UEZQTklOQT09)

**Call Time**: 9:00 Pacific / 18:00 Central Europe

## Recordings From the Call:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Jason Sherman](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b5eb4a5-0d5d-4a7f-b2cc-b2d7597a7e8c?ref=confluence) (BC Gov/Quartech) &lt;jason@usingtechnolo.gy&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence)  (BC Gov / Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- 0.10.3 - [#2486](https://github.com/hyperledger/aries-cloudagent-python/pull/2486)
- Timing/Content for the next release
  
  - [Unreleased PRs in main]()
  - Consider ACA-Py 1.0.0
    
    - What is left? [List from ACA-Py](https://github.com/hyperledger/aries-cloudagent-python/blob/main/SupportedRFCs.md#aip-20)
      
      - DID Exchange – done?
      - Use DID Key?
      - Encryption Envelope?
      - Static Peer DIDs?
      - Route Coordination?
- Offer to implement OpenID4VCs – guidance?
  
  - Indicio PoC in place as a separate service – uses ACA-Py Issuer/Verifier for the signing/verifying of the SD-JWT, DIDs, etc.
    
    - Separate controller service
  - Andrew has a proof of concept as well, not using ACA-Py - pre-auth flow
- Open [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) / High Priority [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
  
  - [PR Review Required](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20review%3Arequired%20draft%3Afalse)
  - Issues: [2514](https://github.com/hyperledger/aries-cloudagent-python/issues/2514), [2506](https://github.com/hyperledger/aries-cloudagent-python/issues/2506) (AnonCreds branch), [2505](https://github.com/hyperledger/aries-cloudagent-python/issues/2505) (other Shared Components), [2501](https://github.com/hyperledger/aries-cloudagent-python/issues/2501), [2424](https://github.com/hyperledger/aries-cloudagent-python/issues/2424)
- AnonCreds RS in ACA-Py progress/next steps
  
  - Revocation done
  - Next:
    
    - Rotation is next
    - PyTests have been commented out – let's get as many as we can activated again
  - Jason is away Oct. 10-13 – good time to get things lined up with main without Jason. Except its IIW week...
  - Endorser is the next big one after that, then migration.
- Plugins – repository – 0.1.0
  
  - Moving some use case specific protocols into repositories – mediation and connections are ideal examples.
- Open Discussion
  
  - Other Topics:
    
    - Sonar Cloud - is this actually working? Add issue to take a look – perhaps Wade or Jason Syrotuck.
    - OpenAPI - Indicio is doing post processing on the OpenAPI file, because what is in the repo is not especially useful.
      
      - too many values being marked as optional – especially on receipt of results from the Admin API.
      - multiple use of the schema – technically they are optional in other places, but not in the OpenAPI
      - Response schemas aren't enforced allowing for returned values to differ
    - Code coverage reports on ACA-Py
    - Resolved, new indy-tails-server released.
      
      - We can't open PRs to the bcgov/indy-tails-server repo; we've got the necessary changes to support uploading tails files by hash in our fork but don't have anywhere for these changes to go
    - Done:
      
      - When do we stop running tests with Indy wallets? AKA When should we move BDD tests to using images without Indy SDK cause it will make our tests a lot faster
    - Quick thoughts on OpenID4VCI/VP
  - did:peer work

## Upcoming Meeting Topics:

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
