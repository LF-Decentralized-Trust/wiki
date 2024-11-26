1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-12-12 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Dec 15, 2023

## Summary:

Topics:

- Status: AnonCreds RS Branch into Main
- New Plugin: OpenID4VCs
- Update on did:peer and AFJ Interop – where we are
- Indy VDR Pool Management – progress and next steps
- Status: Load Generator
- Status: AnonCreds in W3C Format
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

- BC Gov Code With Us – AnonCreds in W3C Format – Application Period open until October 20, 2023.
  
  - [AnonCreds Rust Updates](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/d81f1bb4-4abb-4a4c-8b19-92904e0bd6a6) – Awarded to [DSR Corporation](https://en.dsr-corporation.com/) – [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  - [AnonCreds Rust Changes Deployed in ACA-Py](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/7afcbd7c-2bbc-41ed-bf27-b6ba6e2903c5) – Awarded to What's Cookin' Inc.
  - [AnonCreds Rust Changes Deployed in Aries Framework JavaScript and Aries Bifold](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/6f08d6d5-7e3d-489a-a98f-d7c607309dc9) – [Animo Solutions](https://animo.id/)
- Adding DIDComm to the [VC Playground](https://vcplayground.org/) issuer exchange services - considering using ACA-Py
- Enabling CHAPI initiated credential exchange to be stored in an Aries agent (considering aca-py, afj or vcx)

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence) (IDLab/Open Security and Identity inc.) &lt;patrick.st-louis@idlab.org&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio PBC) &lt;alex.walker@indicio.tech&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Status: Moving AnonCreds RS Branch into Main [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
  
  - All the code from the RS branch is in Main – new wallet type to trigger – "askar-anoncreds"  – adds/moves endpoints
  - Currently working on adding unit and (mostly completed) updating and adding integration tests
  - AATH issues added
  - Next up - endorser, upgrade script
- A new plugin for ACA-Py: [OpenID4VCI](https://github.com/hyperledger/aries-acapy-plugins/tree/main/oid4vci) - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)
  
  - PR with UI Updates: [https://github.com/hyperledger/aries-acapy-plugins/pull/56](https://github.com/hyperledger/aries-acapy-plugins/pull/56)
- Update on eliminating unqualified DIDs, did:peer, and AFJ Interop – where we are [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) 
  
  - did:peer:1 PR merged
  - did:peer:2 PR is in work – having to learn integration testing slow things down a bit
  - did:peer:4 next
  - Issues added to AATH, work ongoing with AFJ
- Status: Indy VDR Pool Management – updates
  
  - Pool Caching in Indy VDR added – caller needs to provide a path for the cache
- Status: Load Generator – ready!? - [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) 
  
  - New docker-compose guide for getting started
  - Ability for running Load Generator against external issuers, verifiers
- Status: AnonCreds in W3C VC Format
- Other [PRs Ready for Review](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20draft%3Afalse%20) and [Issues to Discuss](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3ADiscuss)
  
  - Using did:web (and other DID Methods) for signing non-AnonCreds credentials – [https://github.com/hyperledger/aries-cloudagent-python/issues/2667](https://github.com/hyperledger/aries-cloudagent-python/issues/2667)

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
