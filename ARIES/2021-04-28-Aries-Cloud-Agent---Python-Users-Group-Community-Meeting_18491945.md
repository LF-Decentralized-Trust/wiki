1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2021](ACA-Pug-Meetings-Archive-2021_18514526.html)

# Hyperledger Aries : 2021-04-28 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Apr 28, 2021

## Summary:

Planned Topics:

- Developer AMA
- Discussion: New things in ACA-Py

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
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;

## Announcements

- ACA-Py Updates since  0.6.0:
  
  - CWU is "merge-ready"
  - Endorser Signing
  - Continued evolution of the Shared Components branch

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

- AMA with the Developers
  
  - PR: [Loosen restrictions](https://github.com/hyperledger/aries-cloudagent-python/pull/1096)
  - PR: [ECDH-1PU](https://github.com/hyperledger/aries-cloudagent-python/pull/1085) – what next?
  - PR: [Small AIP-2 updates](https://github.com/hyperledger/aries-cloudagent-python/pull/1056) - what next?
  - What up with canonicalized schema attributes – seems wrong.
  - Endorser Protocol – what do we do next?  Demo? Are we using it in the OrgBook Issuer Service?
    
    - How to handle auto-endorse?
  - Describe [Feature/Event Bus](https://github.com/hyperledger/aries-cloudagent-python/pull/1063)
    
    - Goal - webhooks to other parts of ACA-Py, Plugins to ACA-Py (vs. multiple external listeners)
      
      - A layer between event creation and subscribers to allow internal subscribers
      - Use case – plugin subscriber to push events to a Kafka queue.
      - Need to update the persistent queue work – make it a plugin?
      - How to convey how/when to use this to other developers
      - Integration test or walk-through of how to use.
- Issues: 
  
  - Too many!  Need to have a culling. 94
  - Hot ones?
    
    - Problem Reports
      
      - Key Case: Receiving PR within the Credential Exchange to do clean-up, etc.
        
        - Change the message family
      - Also important - sending Credential Exchange specific PR.
      - PR schema with the RFC.
    - JSON-LD Performance - contexts are not cached.
      
      - Once BBS PR is merged, does some replacements with re-route.
    - Aries Go Interop – base64url, recipientKeys/routingKeys, DIDDoc
      
      - Addressed in "small AIP 2" PR.  Or at least should be...
- Progressing on initiatives; priorities
  
  - Adding a JSON-LD, BBS+, PE Demo
    
    - What keys, what ledger?
    - What does the PD look like?
  - AF-Go Interop – how?
  - Persistent Queues – Need On/Off queue implementation

## Next Meeting

- Requests?

## Future Topics

- Double Signature with eIDAS?
  
  - Background: [https://www.slideshare.net/FIDOAlliance/introduction-to-fido-and-eidas-services](https://www.slideshare.net/FIDOAlliance/introduction-to-fido-and-eidas-services)
  - SICPA - For the eSSIF program, with json-ld credential we are adding double signature, the normal + eIDAS
    
    - [Mateo](https://lf-hyperledger.atlassian.net/wiki/people/557058:46dd489d-ef95-4225-b625-9e0bf11b4704?ref=confluence)
  - Double signature in ACA-Py with pluggable mechanism, and implementation for eIDAS

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18491945/18515124.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
