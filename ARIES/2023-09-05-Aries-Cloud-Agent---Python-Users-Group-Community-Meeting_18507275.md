1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-09-05 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Sergey Minaev on Sep 06, 2023

## Summary:

Topics:

- Release 0.10.1 Published
- AATH Issue – ACA-Py Tests Failing since 2023.09.01
- DID Peer discussion – Across Aries and ACA-Py-specific
- PRs and Issues - status update
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
- [Aries Working Group](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Aries+Working+Group) call – Wednesday (7:00 Pacific / 16:00 Central Europe) with a NEW Zoom link!!!

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Jason Sherman](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b5eb4a5-0d5d-4a7f-b2cc-b2d7597a7e8c?ref=confluence) (BC Gov / Quartech) &lt;jason@usingtechnolo.gy&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Sergey Minaev](https://lf-hyperledger.atlassian.net/wiki/people/557058:f3eb01c9-c402-4ddf-8eb0-18eff9f16aa2?ref=confluence) (DSR) &lt;sergey.minaev@dsr-corporation.com&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Release 0.10.1 Published
- AATH Test [Failing](https://allure.vonx.io/allure-docker-service-ui/projects/acapy) – last passed [2023.08.29](https://allure.vonx.io/allure-docker-service-ui/projects/acapy/reports/824), first failed [2023.09.01](https://allure.vonx.io/allure-docker-service-ui/projects/acapy/reports/825)
  
  - Poetry PR - [commit](https://github.com/hyperledger/aries-cloudagent-python/commit/981a3f09008964b5ba5d4d99492bd9d336fec16a)
  - Flake8 to Ruff PR - [commit](https://github.com/hyperledger/aries-cloudagent-python/commit/fa28560ed7db55f925ae5ff0d043abc55e136574)
- DID Peer Progress and Discussion
  
  - Aries: Introduction of did:peer:4 – a new numalgo
    
    - Relevant issue: [https://github.com/decentralized-identity/peer-did-method-spec/issues/58](https://github.com/decentralized-identity/peer-did-method-spec/issues/58)
    - Outline: [https://hackmd.io/@dbluhm/did-peer-4](https://hackmd.io/@dbluhm/did-peer-4)
    - Reference implementation: [https://github.com/dbluhm/did-peer-4](https://github.com/dbluhm/did-peer-4)
  - Aries: Introduction of new RFC "rotate-did" for DIDComm Messaging DIDs
    
    - [https://github.com/hyperledger/aries-rfcs/pull/794](https://github.com/hyperledger/aries-rfcs/pull/794)
  - Wrapping up the work to move from unqualified to qualified DIDs
- Update: Hyperledger AnonCreds Rust in ACA-Py
  
  - Status of AnonCreds RS – has merged in the latest CL Signatures.
    
    - No release has been done. Need to get that done ASAP - Andrew or Timo?
    - Following that, Daniel will get main merged into the AnonCreds RS branch in ACA-Py.
- [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
  
  - Old ones (suggested for discussion by [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)): 
    
    - [https://github.com/hyperledger/aries-cloudagent-python/issues/1042](https://github.com/hyperledger/aries-cloudagent-python/issues/1042) - https message type prefix
    - [https://github.com/hyperledger/aries-cloudagent-python/issues/1044](https://github.com/hyperledger/aries-cloudagent-python/issues/1044) - updated media types
    - Yes!  Need to decide exactly the behaviour to change.
      
      - Document what is there today.
      - Decide what will be the new behaviour – simply drop the old style or add a flag that defaults but allows the old style?  Hopefully no new flag...
      - The existing flag should continue to be accepted, I think, although we could drop it as well.
  - What would LTS (Long Term Support) support mean for ACA-Py?
    
    - Commitment from an organization to provide the support
      
      - Keep the infrastructure to keep running – e.g. GHA for now – but monitor changes in that.
    - Time frame for the LTS – 3 years, 5 years?
      
      - Plan for the "next LTS"
    - Get to a 1.0 version?  E.g. AIP 2.0?  Getting close... 
      
      - Please ACK – needs to be implemented.
    - Pick an LTS OS to run on
      
      - Target the version of Python associated with the OS and other dependencies
        
        - All python releases get 5 years of security updates (starting from release date)
        - Python 3.9 ends October 5, 2025
    - Monitor OS and dependencies and update them on a branch
    - Cherry pick ACA-Py PRs suitable for LTS
      
      - CI/CD Infrastructure changes – maintain them for the LTS
      - Security fixes - Yes
      - New features – No
    - Marketing/Guidance – the positioning of LTS versions and the ongoing evolution of the codebase
    - Interoperability – maintenance of the test harness – e.g. adding a Test Agent for the LTS branch ongoing execution
      
      - AATH – need feature to NOT run tests when the Test Agent has not changed
    - Migration – migration to the next LTS – managing that, perhaps beyond what we do in ACA-Py today
    - Impacts on Community Coordinate Updates
      
      - Should we, for example, support step 1 of CCUs by adding handling receipt of old and new?
- Open Discussion

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
