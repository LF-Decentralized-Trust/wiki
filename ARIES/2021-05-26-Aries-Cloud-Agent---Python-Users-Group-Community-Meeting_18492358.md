1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2021](ACA-Pug-Meetings-Archive-2021_18514526.html)

# Hyperledger Aries : 2021-05-26 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on May 26, 2021

## Summary:

Planned Topics:

- Status Check: ACA-Py Release 0.7.0
- Update: Queue Handling In ACA-Py
- If we have time: What's in AIP 2.0 that we need to add to ACA-Py

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

- ACA-Py Updates since  0.6.0:
  
  - DIF Presentation Exchange is ready to be merged
  - Aries/Indy Shared Components
- New work item: Multi-ledger support without did:indy

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

- Status Update – ACA-Py 0.7.0 Release
  
  - Pending: [PR 1125](https://github.com/hyperledger/aries-cloudagent-python/pull/1125) – DIF Presentation Exchange – being reviewed – needed.
  - Demo Updates
  - Merging Shared Components
  - Last two weeks:
    
    - Performance issue resolved (issuing)
    - OOB Updates
    - Endorser updates
    - Problem Report handling in Credential Exchange protocols
- Queues – [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)
  
  - Actions:
    
    - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)to do a hackmd doc design to meet mediator-centric requirements, ideally with a narrative on push notification handling
    - [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)to do a hackmd doc design to meet scalabilty requirements - [https://hackmd.io/OF5o0idQTwi\_T\_3eWkDvmw](https://hackmd.io/OF5o0idQTwi_T_3eWkDvmw)
    - Ideally, incorporated into the above, but if not, a third design doc, covering the use of the event bus with the outbound queuing
- Questions – AMA:
  
  - Issuer backend – 100/second issuances – EU Vaccination Credentials into SSI Credentials.
    
    - Limit – seem to have 2 issues/second/ACA-Py instance.  BC has scaled to 21 ACA-Py instances and beyond that the returns are limited.
    - BC Gov has "OrgBook Configurations" to show the settings of the instances. These were developed via tests and analysis of the performance.
      
      - Load balancing has been done through k8s.
- AIP 2.0 – what's got to be added to ACA-Py?
  
  - `--version 2.0` flag to enable "breaking changes" features/completed community updates
  - RFC 0557 Discover Features V2 – Added AIP 2.0 features / potentially dynamic based on loaded modules
  - RFC 0519 Goal Codes in specific protocols (RFC 0453/0454 - Credential Exchange V2), OOB, DID Exchange
    
    - Generalized support?
  - RFC 0627 Static Peer DID Support
  - RFC 0183 Revocation Notification – flag on API to notify user (+ connection\_id?)
  - RFC 0587 Encryption Envelope V2
  - Review and update as needed all AIP 1.0 RFCs – to be added: a diff link for each "updated" RFC

## Next Meeting

- TBD

## Future Topics

- Double Signature with eIDAS?
  
  - Background: [https://www.slideshare.net/FIDOAlliance/introduction-to-fido-and-eidas-services](https://www.slideshare.net/FIDOAlliance/introduction-to-fido-and-eidas-services)
  - SICPA - For the eSSIF program, with json-ld credential we are adding double signature, the normal + eIDAS
    
    - [Mateo](https://lf-hyperledger.atlassian.net/wiki/people/557058:46dd489d-ef95-4225-b625-9e0bf11b4704?ref=confluence)
  - Double signature in ACA-Py with pluggable mechanism, and implementation for eIDAS

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492358/18515219.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
