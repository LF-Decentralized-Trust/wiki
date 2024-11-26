1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-10-17 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Oct 31, 2023

## Summary:

Topics:

- Next Release
- PRs and Issues - status update
- Presentation: Please Ack Protocol in ACA-Py
- Presentation: Load Testing ACA-Py-based Issuers, Verifiers and Mediators
- IIW Follow Up
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

- BC Gov Code With Us – AnonCreds in W3C Format – Application Period open until October 20, 2023.
  
  - [AnonCreds Rust Updates](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/d81f1bb4-4abb-4a4c-8b19-92904e0bd6a6) – $CDN35k
  - [AnonCreds Rust Changes Deployed in ACA-Py](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/7afcbd7c-2bbc-41ed-bf27-b6ba6e2903c5) – $CDN35k
  - [AnonCreds Rust Changes Deployed in Aries Framework JavaScript and Aries Bifold](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/6f08d6d5-7e3d-489a-a98f-d7c607309dc9) – $CDN35k
- [Hyperledger Member Summit](https://www.hyperledger.org/events/hyperledger-member-summit-2023) October 23 in San Francisco and Tokyo

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio PBC) &lt;kim@indicio.tech&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio PBC) &lt;alex.walker@indicio.tech&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov/Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Tim Bloomfield](https://lf-hyperledger.atlassian.net/wiki/people/5a70c8faa02421507dce29c3?ref=confluence) (OPS) &lt;tim.bloomfield@ontario.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence) (IDLab) &lt;patrick.st-louis@idlab.org&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio) &lt;colton@indicio.tech&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Release 0.10.4 Released
- Release ACA-Py Next – lots to include in a (likely 0.11.0)
- [PRs Ready for Review](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20draft%3Afalse%20) and [Issues to Discuss](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3ADiscuss)
- Presentation from DSR Research on the PleaseAck protocol – [design](https://github.com/hyperledger/aries-cloudagent-python/pull/2540) and [PoC implementation](https://github.com/hyperledger/aries-cloudagent-python/pull/2546)
- Presentation/Discussion from Indicio on the progress made on the [Load Test Generator](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/51d7c289-51a8-4307-939c-5a4271c7b2b6) – Code With Us from BC Gov
- IIW Happenings:
  
  - AnonCreds V2
  - [did:webs](https://trustoverip.github.io/tswg-did-method-webs-specification/index.html) – a compatible DID Method to did:web but that includes security and verifiability
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
- The DSR team has started looking into supporting the "please-ack" protocol. A draft PoA will likely be ready for review on the next call, 17 Oct 2023

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
