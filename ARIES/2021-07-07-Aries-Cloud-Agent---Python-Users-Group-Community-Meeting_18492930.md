1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2021](ACA-Pug-Meetings-Archive-2021_18514526.html)

# Hyperledger Aries : 2021-07-07 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Jul 07, 2021

## Summary:

Planned Topics:

- Status Check: ACA-Py Release 0.7.0
- Performance Issue Update – Public DID Handling
- Discussion: What's next/getting to Release 1.0.0
- AMA (as time permits)

## Recording from the call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- Name (Organization) &lt;email&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Announcements

## Deployments and Work Updates

- BC Gov Team
  
  - Aries-VCR/OrgBook BC Deployment
    
    - In progress: a multi-tenant OrgBook Issuer
  - Issuer Kit - VCs for OIDC Issuer Service - [Safe Entry BC PoC](https://vonx.io/safeentry) - VCs for Physical Access Points
  - Verification Tutorial – multi-purpose verifier aimed at the general population receiving their first verifiable credential
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: https://aries-interop.info
  - BPA - Business Partner Agent for B2B use of VCs
  - AIP 2.0
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)

## Agenda

- Status Update – ACA-Py 0.7.0 Release – [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)
  
  - ACA-Py 0.7.0RC0 has been tagged
  - List of major updates and additions:
    
    - Support for W3C Standard Verifiable Credentials based on JSON-LD using LD-Signatures and BBS+ Signatures
    - Support for DIF Presentation Exchange
    - Present Proof V2 Support
    - Pluggable DID Resolver (with a did:web resolver) with fallback to an optional/configurable external DID universal resolver
    - Endorser Signing Transactions Protocol
    - Upgrades to Demos to add support for Credential Exchange 2.0 and W3C Verifiable Credentials
    - Alpha support for the Indy/Aries Shared Components (indy-vdr, indy-shared-rs and aries-askar), enabling running ACA-Py without using the Indy-SDK, while still supporting the use of Indy as a ledger, and Indy AnonCreds verifiable credential format
    - Feature/Event bus for ACA-Py generated events for controllers
    - Initial support for AIP 2.0 DIDComm envelopes (e.g. ECDH-1PU support)
    - Enable operation without Indy ledger support if not needed
    - Performance fix for deployments with large numbers of DIDs/connections
    - Simplify the creation/handling of plugin protocols
    - DID Exchange implicit invitation handling
    - Add support for Indy 1.16 predicates (restrictions on predicates based on attribute name and value)
    - BDD Tests run via GitHub Actions
  - Breaking changes?
    
    - DID Exchange Create Request returned the request, and now returns the connection object
    - When endorsement is enabled, the revocation capabilities are not working. For now, don't use the features in combination.
    - Possible – did related methods for handling unqualified did:sov keys
  - What's left?
- Performance issue addressed – redundant Public DID Queries – [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)
  
  - Issue - public DID checked multiple times per request; old approach was check each DID until public one found; blows up with many DIDs (public or peer) – fixed!
  - Could be improved further with caching, as it is still doing the multiple checks per request, but minor issue
  - Discovered along the way that DIDs from wallet cannot be deleted (e.g. when deleting a connection) – a leftover indy-sdk issue (never implemented). Likely to be addressed in Askar.
- Discussion: What's next in ACA-Py/Getting to 1.0.0
  
  - Support for did:orb
    
    - Where do we do this?
    - How are we using external universal resolvers?
  - Support for multiple Indy ledgers
  - Support for revised did:sov
  - Persistent Queues – getting more done on that.
    
    - Loading and unloading the queues
    - Transports through the event bus, making the mechanism pluggable - inbound and outbound
      
      - Will require changes in the forward message handling for notifications to mobile devices – generalize this and enable notification handlers to see the message off the bus
      - These are changes to externalize the handling are a step to persistent queues, but not complete answer.
  - AIP 2.0 Features
    
    - `--version 2.0` flag to enable "breaking changes" features/completed community updates
    - RFC 0557 Discover Features V2 – Added AIP 2.0 features / potentially dynamic based on loaded modules
    - RFC 0519 Goal Codes in specific protocols (RFC 0453/0454 - Credential Exchange V2), OOB, DID Exchange
      
      - Generalized support?
    - RFC 0627 Static Peer DID Support
    - RFC 0183 Revocation Notification – flag on API to notify user (+ connection\_id?)
    - RFC 0587 Encryption Envelope V2
    - Review and update as needed all AIP 1.0 RFCs – to be added: a diff link for each "updated" RF
- Questions – AMA:

## Next Meeting

## Future Topics

- Queues – [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)
  
  - Actions:
    
    - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)to do a hackmd doc design to meet mediator-centric requirements, ideally with a narrative on push notification handling
    - [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)to do a hackmd doc design to meet scalability requirements - [https://hackmd.io/OF5o0idQTwi\_T\_3eWkDvmw](https://hackmd.io/OF5o0idQTwi_T_3eWkDvmw)
    - Ideally, incorporated into the above, but if not, a third design doc, covering the use of the event bus with the outbound queuing
- Double Signature with eIDAS?
  
  - Background: [https://www.slideshare.net/FIDOAlliance/introduction-to-fido-and-eidas-services](https://www.slideshare.net/FIDOAlliance/introduction-to-fido-and-eidas-services)
  - SICPA - For the eSSIF program, with json-ld credential we are adding double signature, the normal + eIDAS
    
    - [Mateo](https://lf-hyperledger.atlassian.net/wiki/people/557058:46dd489d-ef95-4225-b625-9e0bf11b4704?ref=confluence)
  - Double signature in ACA-Py with pluggable mechanism, and implementation for eIDAS
- Performance with Shared Components enabled (Aries Askar et al.)
- AIP 2.0 Features:
  
  - `--version 2.0` flag to enable "breaking changes" features/completed community updates
  - RFC 0557 Discover Features V2 – Added AIP 2.0 features / potentially dynamic based on loaded modules
  - RFC 0519 Goal Codes in specific protocols (RFC 0453/0454 - Credential Exchange V2), OOB, DID Exchange
    
    - Generalized support?
  - RFC 0627 Static Peer DID Support
  - RFC 0183 Revocation Notification – flag on API to notify user (+ connection\_id?)
  - RFC 0587 Encryption Envelope V2
  - Review and update as needed all AIP 1.0 RFCs – to be added: a diff link for each "updated" RF

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492930/18515342.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492930/18515333.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492930/18515334.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492930/18515335.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
