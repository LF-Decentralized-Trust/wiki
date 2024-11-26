1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-06-14 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Jun 14, 2022

## Summary:

Topics:

- Getting to release 0.7.4
- Dealing with duplicate Admin API endpoint calls / Problem Reports
- Q&amp;A

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Extracted segments:
- Relevant Chat Bits:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)(Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Bruno Hivert](https://lf-hyperledger.atlassian.net/wiki/people/712020:0ef3e380-8e1e-45be-82e1-708b65f236da?ref=confluence)([https://idlab.org)](https://idlab.org%29) &lt;bruno.hivert@idlab.org&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence)(Indicio) &lt;colton@indicio.tech&gt;

## Announcements

## Deployments and Work Updates

- BC Gov Team
  
  - [Aries Cloud Agent Python](https://github.com/hyperledger/aries-cloudagent-python)
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)
  - [Aries-VCR](https://github.com/bcgov/aries-vcr)/OrgBook BC Deployment
  - [Issuer Kit](https://github.com/bcgov/issuer-kit) - VCs for OIDC Issuer Service
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: [https://aries-interop.info](https://aries-interop.info)
  - [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness)
  - BC Wallet – based on [Aries Framework JavaScript](https://github.com/hyperledger/aries-framework-javascript) and [Aries Bifold](https://github.com/hyperledger/aries-mobile-agent-react-native)
  - [Aries Endorser Service](https://github.com/bcgov/aries-endorser-service)
  - [Traction](https://github.com/bcgov/traction)

## Agenda

- Getting to release 0.7.4 – what is needed after RC2
  
  - [PRs since Release 0.7.4-RC2](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-05-11)
  - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)
- Dealing with duplicate Admin API calls – e.g. [Issue 1798 - store credential](https://github.com/hyperledger/aries-cloudagent-python/issues/1798); [Issue 1782](https://github.com/hyperledger/aries-cloudagent-python/issues/1782); even [issue 1730 - problem report for a non-protocol](https://github.com/hyperledger/aries-cloudagent-python/issues/1730)
  
  - How aggressively should we address these issues?
    
    - One pass through the protocols, states and endpoints?
    - As they come up?
  - From discussion:
    
    - Where possible, report back to the Controller that their call was unexpected – by the response to the request where possible, perhaps via the follow up event.
    - Separate out where the action breaks the protocol (interaction with other Agent) and where it impacts only the operation if this agent (e.g. the store credential example – doesn't impact the execution of the protocol).
    - Definitely prevent problem reports being sent out BEFORE the protocol exists (the [issue 1730 - problem report for a non-protocol](https://github.com/hyperledger/aries-cloudagent-python/issues/1730) example).
    - For now, handle as they occur and learn from those implementations.
    - Look for the patterns and see if there is something that can be done at the framework level.  What do other frameworks do?

## Next Meeting

- An update from [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence) and his team from the discussion on [2022-04-19](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2022-04-19+Aries+Cloud+Agent+-+Python+Users+Group+Community+Meeting) about adding DIDComm V2 to ACA-Py

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18497011/18516371.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
