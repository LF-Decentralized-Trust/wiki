1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-10-04 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Oct 05, 2022

## Summary:

Topics:

- 0.7.5 Patch Release status  See 0.7.5 Milestone
- AnonCreds updates – likely path forward
- PR Summary – combining credentials with Present Proof V2 (#1956)
- Discussion on [recently merged PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-08-18), [open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
- Open Discussion – bring your topics

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 CET

## Recordings from the call: [dummyfile.txt](#)

- Full Meeting:
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
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io) &lt;warren@affinitiquest.io&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence)(Indicio PBC) &lt;colton@indicio.tech&gt;

## Announcements

- IIW coming up in November
- DIF Interop WG
  
  - Survey on Verifiable Credential formats and exchange mechanisms everyone is using to inform what discussions we should be pursuing in the Interop WG: [https://forms.gle/4YqrjFcB5Fnbcrgz8](https://forms.gle/4YqrjFcB5Fnbcrgz8)
  - October 5, 11 AM ET - Alex Tweeddale from Cheqd will be presenting on their work "Decoupling AnonCreds from Hyperledger Indy and creating extensible resources on-ledger with DID URLs"
- Last AATH Meeting – worth reviewing the recording posted on the [meeting page](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2022-09-29+AATH-AMTH+Users+Group+Meeting) – cool stuff from IdLab on using AATH!

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

- Milestone 0.7.5 – progress and anything more to add to it?
  
  - Wrapping up – should be today. [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)and team to try to create 0.7.5 Branch in ACA-Py repo.
- AnonCreds discussions from Hyperledger Global Forum and Rebooting Web of Trust
  
  - AnonCreds as a top level project – [presentation](https://docs.google.com/presentation/d/1pgWZSnFMJZZ82d72XRt-stlWvB00nkIpofoWpCp7ty8/edit?usp=sharing) and [draft proposal](https://docs.google.com/document/d/1_hlZZNkY1gmdi3Basz4LRh_U9xK0NTkQ4vTowyWeYeY/edit) – please consider being a sponsor (name, optional organization, email address)
  - AnonCreds ledger agnostic
    
    - Up to 6 non-Indy AnonCreds implementations found
    - Progress on AnonCreds Spec – more contributors
    - Working right now on AnonCreds API with AnonCreds Methods
      
      - AnonCreds spec defines the format produced on creation and/or expected for use of: Schema, CredDef, RevRegDef, RevRegEntry
      - AnonCreds Methods must provide the objects in the expected format.
      - Mostly straight-forward, but interesting for RevRegEntry, where AnonCreds Methods may store the data as deltas or as full state.
  - AnonCreds in W3C Verifiable Credential Data Model Format
    
    - It seems to be really easy...
  - Likely path forward:
    
    - Code: Extract AnonCreds from indy-shared-rs
    - Code: Define AnonCreds – AnonCreds Method API
    - Code: Implement AnonCreds Methods – indy legacy, did:indy, perhaps HTTP, cheqd
    - Code: AnonCreds in W3C Format – transformations
    - Top Level AnonCreds Project
    - New AnonCreds Revocation
    - Next Gen AnonCreds with (at least) the same features, but better, faster
- Discussion on [recently merged PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-08-18), [open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
  
  - GitHub Actions and publishing artifacts - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)
- Using the W3C's CCG effort on VC-API and ACA-Py – an experiment by Patrick from IdLabs
  
  - VC-API is a standard API, much like what we call a controller for the limited purpose generating and verifying Verifiable Credentials.  Does not include delivery, or any protocols related to VCs.
  - [https://coordinator.acapy.idlab.app/docs](https://coordinator.acapy.idlab.app/docs)
  - [https://w3c-ccg.github.io/vc-api/#architecture-overview](https://w3c-ccg.github.io/vc-api/#architecture-overview)
- Paul Wen has been working on an SSI Verifier – [https://github.com/PaulWen/ssi-verifier](https://github.com/PaulWen/ssi-verifier)
  
  - Define a Presentation Request
  - Generate a QR code
  - Display if a Presentation received meets the Presentation Request
- Open Discussion
- Q&amp;A

## Next Meeting

## Future Topics

- Discussion of PR [1956](https://github.com/hyperledger/aries-cloudagent-python/pull/1956) - Combining credentials in Present Proof v2
- Proposal for topic (Indicio): Pickup Protocol Plugin + Persistence of mediated messages
  
  - [https://github.com/indicio-tech/acapy-plugin-pickup](https://github.com/indicio-tech/acapy-plugin-pickup)
  - Persistence Feature Branch: [https://github.com/indicio-tech/acapy-plugin-pickup/tree/feature/persistence](https://github.com/indicio-tech/acapy-plugin-pickup/tree/feature/persistence)

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498977/18516807.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
