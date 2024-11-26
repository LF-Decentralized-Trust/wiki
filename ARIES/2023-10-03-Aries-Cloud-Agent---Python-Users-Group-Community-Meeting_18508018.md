1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-10-03 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Emiliano Suñé on Oct 03, 2023

## Summary:

Topics:

- Next Release
- OpenID4VCs Discussion
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
- BC Gov Code With Us for [Load Test Generator](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/51d7c289-51a8-4307-939c-5a4271c7b2b6) - awarded to Indicio PBC
- [Hyperledger Member Summit](https://www.hyperledger.org/events/hyperledger-member-summit-2023) October 23 in San Francisco and Tokyo

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Sergey Minaev](https://lf-hyperledger.atlassian.net/wiki/people/557058:f3eb01c9-c402-4ddf-8eb0-18eff9f16aa2?ref=confluence) (DSR) &lt;sergey.minaev@dsr-corporation.com&gt;
- Alexander Sukhachev (DSR) &lt;alexander.sukhachev@dsr-corporation.com&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio PBC) &lt;alex.walker@indicio.tech&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio PBC) &lt;colton@indicio.tech&gt;
- [Jason Sherman](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b5eb4a5-0d5d-4a7f-b2cc-b2d7597a7e8c?ref=confluence) (BC Gov/Quartech) &lt;jason@usingtechnolo.gy&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov/Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov/Quartech) &lt;emiliano.sune@quartech.com&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Release 0.10.3 Status
- Release ACA-Py Next – contents, desired.
  
  - did:peer:2/3 and did:peer:4
- OpenID4VCs with ACA-Py – use cases, requirements, approaches, collaborations
- Update: Hyperledger AnonCreds Rust in ACA-Py
- [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
- Community Happenings:
  
  - Draft AnonCredsv2 library being contributed to Hyperledger as we speak... Builds on the Hyperledger Labs Agora cryptographic primitives.
- AATH Test [Failing](https://allure.vonx.io/allure-docker-service-ui/projects/acapy) – **FIXED** – last passed [2023.08.29](https://allure.vonx.io/allure-docker-service-ui/projects/acapy/reports/824), first failed [2023.09.01](https://allure.vonx.io/allure-docker-service-ui/projects/acapy/reports/825)
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
