1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-09-19 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Sean Bohan on Oct 03, 2023

## Summary:

Topics:

- Release 0.10.2 Status
- SD-JWTs in ACA-Py
- Status of AnonCreds RS in ACA-Py update
- PRs and Issues - status update
- Community Happenings
- AATH Issue – ACA-Py Tests Failing since 2023.09.01
- Open Discussion

**Zoom Link**: [https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09](https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

- [Internet Identity Workshop](https://internetidentityworkshop.com/) coming up October 10-12
- [Hyperledger Member Summit](https://www.hyperledger.org/events/hyperledger-member-summit-2023) October 23 in San Francisco and Tokyo

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov/Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio PBC) &lt;alex.walker@indicio.tech&gt;
- [Jason Sherman](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b5eb4a5-0d5d-4a7f-b2cc-b2d7597a7e8c?ref=confluence) (BC Gov/Quartech) &lt;jason@usingtechnolo.gy&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio PBC) &lt;char@indicio.tech&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Release 0.10.2 Status
- SD-JWTs in ACA-Py – [PR 2487](https://github.com/hyperledger/aries-cloudagent-python/pull/2487) from [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) 
  
  - [Documentation](https://github.com/Indicio-tech/aries-cloudagent-python/blob/feat/sd-jwt-implementation/docs/GettingStartedAriesDev/SelectiveDisclosureJWTs.md)
  - SD-JWT Spec: [https://datatracker.ietf.org/doc/html/draft-ietf-oauth-selective-disclosure-jwt-05](https://datatracker.ietf.org/doc/html/draft-ietf-oauth-selective-disclosure-jwt-05)
- Update: Hyperledger AnonCreds Rust in ACA-Py
  
  - Status of AnonCreds RS – has merged in the latest CL Signatures.
    
    - AnonCreds Version 0.2.0-dev1 has been made available - pending tag and release.
    - Plan is that once available, Daniel to get main merged into the AnonCreds RS branch in ACA-Py.
      
      - Primarily: Tails file handling on issuing and revoking credentials
- [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
  
  - Still to be done: 
    
    - [https://github.com/hyperledger/aries-cloudagent-python/issues/1042](https://github.com/hyperledger/aries-cloudagent-python/issues/1042) - https message type prefix, [https://github.com/hyperledger/aries-cloudagent-python/issues/1044](https://github.com/hyperledger/aries-cloudagent-python/issues/1044) - updated media types
      
      - Proposed behaviour:
        
        - Document what is there today: default to old, flags to emit new.
        - Change the default behaviour to emit new (as if the flags were ALWAYS set)
        - Leave the existing flag, but it does nothing.
        - Do **NOT** add a new flag to allow the old behaviour.
          
          - Are we sure?
- Community Happenings:
  
  - Relevant Hyperledger Labs proposal from Mike Lodder – Agora – [https://github.com/hyperledger-labs/hyperledger-labs.github.io/pull/249](https://github.com/hyperledger-labs/hyperledger-labs.github.io/pull/249)
  - DID Peer Progress and Discussion
    
    - Aries: Introduction of did:peer:4 – a new numalgo
      
      - Relevant issue: [https://github.com/decentralized-identity/peer-did-method-spec/issues/58](https://github.com/decentralized-identity/peer-did-method-spec/issues/58)
      - PR: [https://github.com/decentralized-identity/peer-did-method-spec/pull/61](https://github.com/decentralized-identity/peer-did-method-spec/pull/61)
      - Reference implementation: [https://github.com/dbluhm/did-peer-4](https://github.com/dbluhm/did-peer-4)
    - Aries: Introduction of new RFC "rotate-did" for DIDComm Messaging DIDs
      
      - [https://github.com/hyperledger/aries-rfcs/pull/794](https://github.com/hyperledger/aries-rfcs/pull/794)
- AATH Test [Failing](https://allure.vonx.io/allure-docker-service-ui/projects/acapy) – last passed [2023.08.29](https://allure.vonx.io/allure-docker-service-ui/projects/acapy/reports/824), first failed [2023.09.01](https://allure.vonx.io/allure-docker-service-ui/projects/acapy/reports/825)
  
  - Poetry PR - [commit](https://github.com/hyperledger/aries-cloudagent-python/commit/981a3f09008964b5ba5d4d99492bd9d336fec16a)
- Open Discussion
  
  - Mediation Routing Keys:
    
    [https://github.com/hyperledger/aries-cloudagent-python/issues/2357](https://github.com/hyperledger/aries-cloudagent-python/issues/2357)
    
    [https://github.com/hyperledger/aries-cloudagent-python/issues/2492](https://github.com/hyperledger/aries-cloudagent-python/issues/2492)
    
    [https://github.com/Indicio-tech/aries-cloudagent-python/pull/153](https://github.com/Indicio-tech/aries-cloudagent-python/pull/153)

## Upcoming Meeting Topics:

- Discussion Topics:
  
  - Update on ACA-Py Container Scanning
  - Multi-architecture containers
    
    - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
    - Solution: A third container published that includes BBS+ package, but is single architecture
    - Others are Askar

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
