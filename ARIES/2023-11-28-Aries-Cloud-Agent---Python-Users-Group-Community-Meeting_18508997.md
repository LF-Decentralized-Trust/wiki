1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-11-28 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Nov 29, 2023

## Summary:

Topics:

- The 0.10.5 and 0.11.0 Releases
- Status: AnonCreds RS Branch into Main
- Update on did:peer and AFJ Interop – where we are
- Status: Load Generator
- Status: AnonCreds in W3C Format
- Indy VDR Pool Management – what we have learned
- PRs and Issues - status update
- Open Discussion

**Zoom Link**: [https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09](https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:  [https://youtu.be/BvbeDCcYCL4](https://youtu.be/BvbeDCcYCL4)

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
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio PBC) &lt;colton@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Tim Bloomfield](https://lf-hyperledger.atlassian.net/wiki/people/5a70c8faa02421507dce29c3?ref=confluence) (OPS) &lt;tim.bloomfield@ontario.ca&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Jamie Popkin](https://lf-hyperledger.atlassian.net/wiki/people/557058:73d5013c-2347-45e0-b243-75082e5f30be?ref=confluence) (Little Earth) &lt;popkinj@littleearth.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov / Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio PBC) &lt;kim@indicio.tech&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Release 0.10.5 – flaw in the JSON-LD Presentation verification code.
- Release 0.11.0 – available now!
- Status: Moving AnonCreds RS Branch into Main
  
  - New endpoints are merged - /anoncreds
  - Issue and present proof being merged in – no revocation, that will be added.
- Update on did:peer and AFJ Interop – where we are
  
  - Two PRs (might end up combined?):
    
    [https://github.com/hyperledger/aries-cloudagent-python/pull/2611](https://github.com/hyperledger/aries-cloudagent-python/pull/2611)
    
    [https://github.com/hyperledger/aries-cloudagent-python/pull/2578](https://github.com/hyperledger/aries-cloudagent-python/pull/2578)
  - [Issue](https://github.com/hyperledger/aries-cloudagent-python/issues/2610) resolved by [PR 2611](https://github.com/hyperledger/aries-cloudagent-python/pull/2611): did:peer:1 not accepted in ACA-Py DID Exchange
  - Next issue: AFJ doesn't accept unqualified DIDs in DID Exchange but should accept a did:peer:2 ([PR 2578](https://github.com/hyperledger/aries-cloudagent-python/pull/2578))
  - Anticipated issue: did\_rotate~attach support in AFJ
  - Hacky test environment: [https://github.com/dbluhm/acapy-afj-interop](https://github.com/dbluhm/acapy-afj-interop)
- Status: Load Generator – moving along – migrating to Askar for the load agent
  
  - Askar work on hold - issues with it.  Receiving different events.
  - Working in on modules for issuer and verifier – add it to list of modules.
- Status: AnonCreds in W3C VC Format
- If time permits: Indy VDR Pool Management – what we have learned
- If time permits: Using the Timing Decorator for Investigating Multi-Party Issues
- Other [PRs Ready for Review](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20draft%3Afalse%20) and [Issues to Discuss](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3ADiscuss)

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
