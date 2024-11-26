1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-11-14 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Dec 15, 2023

## Summary:

Topics:

- Status: 0.11.0 Release
- Status: AnonCreds RS Branch into Main
- Status: Load Generator
- Status: AnonCreds in W3C Format
- Demo: The Traction Sandbox – a new utility for playing with ACA-Py, AnonCreds
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
- [Alexander Sherbakov](https://lf-hyperledger.atlassian.net/wiki/people/557058:a955b109-9f8c-405c-9f96-0903d4de8c46?ref=confluence) (DSR Corporation) &lt;alexander.sherbakov@dsr-corporation.com&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio) &lt;colton@indicio.tech&gt;
- [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence) (IDLab) &lt;patrick.st-louis@idlab.org&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov / Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio PBC) &lt;kim@indicio.tech&gt;
- [Jamie Popkin](https://lf-hyperledger.atlassian.net/wiki/people/557058:73d5013c-2347-45e0-b243-75082e5f30be?ref=confluence) (BC Gov / Little Earth Spatial Programming Inc.) &lt;popkinj@littleearth.ca&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Release 0.11.0 status
- Status: Moving AnonCreds RS Branch into Main
  
  - Created branch, manually pulling across code net new and integration – all unit tests passing
  - Endpoints hooked up – new /anoncreds endpoints – not the existing endpoints
  - New wallet type "--wallet-type askar-anoncreds"
- Status: Load Generator – moving along – migrating to Askar for the load agent
- Status: AnonCreds in W3C VC Format
- Demo: Traction Sandbox – a new utility for the ACA-Py community
  
  - [AnonCreds Traction Workshop](https://bit.ly/AnonCredsTraction)
    
    - Create Tenant
    - Make Issuer
    - Create Schema
    - Create CredDef
    - Generate Invitation
    - Establish Connection
    - Issue Credential
    - Present Proof
    - Use the API – the important part!!
  - [Traction Issuer Example](https://github.com/hyperledger/aries-acapy-controllers/tree/main/TractionIssuanceDemo)
- Update on Please Ack "~please\_ack":
  
  - One party can request an `Ack`  on any message – either to be returned on receipt, or on outcome of the message.
  - Other party MAY send an extra `Ack`  message.
  - Tricky to implement:
    
    - Generic ACA-Py `on receipt`  is not as easy as it could be.  Possible, but requires some rework.
      
      - Is the message a generic Ack or an adopted Ack
    - `on outcome`  definitely requires per protocol updates at least, plus logic for determining when the outcome of a message is known.
    - Isn't required on many messages, as once the message outcome is determined, a message is immediately generated and sent. What help is sending another message in parallel?
    - Where it is most likely to be useful – at the end of a protocol when there is no other message – making it useful may mean altering the protocol.
      
      - Issue Credential – should it be sent when the protocol "completes" or after the controller/business process decides to keep the credential.
      - Present Proof – should it be sent when the credential is cryptographically verified, or when the controller/business process decides the credential satisfies the business need?
        
        - If ACA-Py deletes the protocol state object automatically when the controller is sent the verification result, how can the protocol be kept for an optional "Ack"?
      - Basic Message – could (in theory) be used to enable "received" and "read" notifications of basic messages, but the "read" notification would extend the protocol lifetime from when the controller received the message, to when an event happened inside the controller. Tricky!
    - Requesting `~please_ack` :
      
      - The configuration or the admin API would have to be updated to add the ability for the controller to say, "Hey, I want a `~please_ack` added in these places..."
      - How do applications (wallets, etc.) want to use the `~please_ack` feature?
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
