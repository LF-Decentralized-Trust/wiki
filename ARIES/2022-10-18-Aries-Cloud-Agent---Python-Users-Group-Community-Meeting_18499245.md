1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-10-18 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Oct 31, 2022

## Summary:

Topics:

- 0.7.5 Patch Release.
- PR Activity Update
- Ideas on OIDC4VC and ACA-Py: Holder and Verifier
- PR Summary – combining credentials with Present Proof V2 (#1956)
- DIDComm V2 in ACA-Py (and other Aries Frameworks) efforts
- Open Discussion

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 CET

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#) - Design/Overview Document: [https://hackmd.io/@romanr/H1WXfAcQj](https://hackmd.io/@romanr/H1WXfAcQj)
- ACA-Py Processing an OIDC Request from a Relying Party: [dummyfile.txt](#)
- ACA-Py Processing Combined AnonCreds and W3C Presentations (PR #[1956](https://github.com/hyperledger/aries-cloudagent-python/pull/1956)): [dummyfile.txt](#)

```

```

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Victor Martinez](https://lf-hyperledger.atlassian.net/wiki/people/557058:73fff461-39df-4cc9-85d1-7b8a65773bee?ref=confluence) (SICPA) &lt;victor.martinez@sicpa.com&gt;

## Announcements

- IIW coming up: November 15-17, joining?  Almost sold out...
- Presentation to Hyperledger TOC (formerly TSC) on Hyperledger AnonCreds as a project
  
  - Proposal as [Google Document](https://docs.google.com/document/d/1_hlZZNkY1gmdi3Basz4LRh_U9xK0NTkQ4vTowyWeYeY/edit?usp=sharing) and [Hyperledger-HIP Pull Request](https://github.com/hyperledger/hyperledger-hip/pull/7)
  - TOC Meeting is this Thursday at 7:00 Pacific / 16:00 Central Europe using this [Zoom Link](https://zoom.us/j/91447530149?pwd=NWRNQ1BhRjhQd29GNTdUcmVSTWNKQT09)

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

- Release of version 0.7.5 – ready to go?
  
  - Huge thanks to [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence)on the cherry-picking!
- Discussion on [recently merged PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-08-18), [open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
- Ideas on OIDC4VC and ACA-Py: Holder and Verifier (IDUnion – Roman Reinert and Ingo Wolf) – Design Document: [https://hackmd.io/@romanr/H1WXfAcQj](https://hackmd.io/@romanr/H1WXfAcQj)
- Overview of PR [#1956](https://github.com/hyperledger/aries-cloudagent-python/pull/1956) - using DIF Presentation Exchange (Present Proof V2) with AnonCreds, and improvements in JSON-LD Presentation Exchange Handling
- Discussion of DIDComm v2 in ACA-Py
  
  - From Victor Martinez : [https://github.com/sicpa-dlab/didcomm-python](https://github.com/sicpa-dlab/didcomm-python)
  - From Yildiz, Hakan : [https://identity.foundation/didcomm-messaging/spec/#defined-profiles](https://identity.foundation/didcomm-messaging/spec/#defined-profiles)
- Q&amp;A

## Next Meeting

## Future Topics

- Proposal for topic (Indicio): Pickup Protocol Plugin + Persistence of mediated messages
  
  - [https://github.com/indicio-tech/acapy-plugin-pickup](https://github.com/indicio-tech/acapy-plugin-pickup)
  - Persistence Feature Branch: [https://github.com/indicio-tech/acapy-plugin-pickup/tree/feature/persistence](https://github.com/indicio-tech/acapy-plugin-pickup/tree/feature/persistence)

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18499245/18516852.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18499245/18516851.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18499245/18516850.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
