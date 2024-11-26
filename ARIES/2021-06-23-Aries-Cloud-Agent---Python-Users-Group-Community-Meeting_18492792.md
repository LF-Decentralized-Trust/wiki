1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2021](ACA-Pug-Meetings-Archive-2021_18514526.html)

# Hyperledger Aries : 2021-06-23 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Jun 23, 2021

## Summary:

Planned Topics:

- Status Check: ACA-Py Release 0.7.0
- Performance Issue Update – Public DID Handling
- DIF Presentation Exchange in ACA-Py
- Multi-Tenant Experience: OrgBook Issuer Agency
- AMA (as time permits)

## Recording from the call:

- Full recording: [dummyfile.txt](#)
- DIF Presentation Exchange Section: [dummyfile.txt](#)
- Multi-Tenant Experience Section: [dummyfile.txt](#)

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
  - Vaccination/Test Result Verifiable Credential Issuer Service
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: https://aries-interop.info
    
    - DID Exchange Test Cases; deprecating 0160 Connections usage
    - Backchannel for Aries Framework Go
  - BBS+ support to achieve W3C Standard VCs with ZKP and Selective Disclosure
    
    - Including Presentation Exchange
  - BPA - Business Partner Agent for B2B use of VCs
  - did:indy, AIP 2.0

## Agenda

- Status Update – ACA-Py 0.7.0 Release – [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)
  
  - 0.7.0RC1 tag Real Soon Now
    
    - PE Merged, lots of testing and tweaking going on.
    - Shared components to be merged
    - Alice/Faber Demo
- Performance issue addressed – redundant Public DID Queries – [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)
- DIF Presentation Exchange in ACA-Py – [Shaanjot Gill](https://lf-hyperledger.atlassian.net/wiki/people/712020:ef425cae-d196-44a6-b7e8-c21e4470d0d3?ref=confluence)
- Multi-Tenancy Example: OrgBook Issuer Agency – Akiff Manji
- Questions – AMA:

## Next Meeting

- Queues – [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)
  
  - Actions:
    
    - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)to do a hackmd doc design to meet mediator-centric requirements, ideally with a narrative on push notification handling
    - [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)to do a hackmd doc design to meet scalabilty requirements - [https://hackmd.io/OF5o0idQTwi\_T\_3eWkDvmw](https://hackmd.io/OF5o0idQTwi_T_3eWkDvmw)
    - Ideally, incorporated into the above, but if not, a third design doc, covering the use of the event bus with the outbound queuing

## Future Topics

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492792/18515304.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492792/18515305.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492792/18515306.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
