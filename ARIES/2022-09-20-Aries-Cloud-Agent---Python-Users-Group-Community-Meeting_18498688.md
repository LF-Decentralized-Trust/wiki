1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-09-20 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Sep 20, 2022

## Summary:

Topics:

- Aries Mediator Service
- Patch Release needed?  See PR 1936
- Update on "VDR-agnostic AnonCreds"
- Roadmap – follow up from last meeting
- Discussion on [recently merged PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-08-18), [open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
- Q&amp;A

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 CET

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Relevant Chat Bits:

```

```

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io) &lt;warren@affinitiquest.io&gt;

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

- Aries Endorser Service
  
  - Patch Release needed?  See [PR 1936](https://github.com/hyperledger/aries-cloudagent-python/issues/1936)
  - Yes – [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)to do a review of the PRs merged since 0.7.4 to see if any need to be added.
- Update on "VDR-agnostic AnonCreds", including PR 
  
  - Multiple independent implementations of AnonCreds without Indy found – cheqd, database, file, Fabric and two others.
  - Plan is to have an abstract API for AnonCreds for writing/reading objects and then methods to handle the writes/reads for specific ledgers
  - Discussed at Hyperledger Global Forum – AnonCreds as a separate project at Hyperledger, including the implementation, specification, some VDR methods, documentation
- Roadmap – follow up from last meeting
  
  - Milestone created for [Version 1.0.0](https://github.com/hyperledger/aries-cloudagent-python/milestone/5)
  - Not a proper long roadmap – looking for more ideas on how to do that.
- Discussion on [recently merged PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-08-18), [open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
- Q&amp;A

## Next Meeting

## Future Topics

- Proposal for topic (Indicio): Pickup Protocol Plugin + Persistence of mediated messages
  
  - [https://github.com/indicio-tech/acapy-plugin-pickup](https://github.com/indicio-tech/acapy-plugin-pickup)
  - Persistence Feature Branch: [https://github.com/indicio-tech/acapy-plugin-pickup/tree/feature/persistence](https://github.com/indicio-tech/acapy-plugin-pickup/tree/feature/persistence)

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498688/18516751.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
