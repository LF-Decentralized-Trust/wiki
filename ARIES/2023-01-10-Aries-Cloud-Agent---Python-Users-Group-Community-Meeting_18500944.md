1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-01-10 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Jan 20, 2023

## Summary:

Topics:

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio
- Progress/discussion on Ledger-Agnostic AnonCreds
- ACA-Py 1.0 Discussion/Priorities, including an ACA-Py Documentation site
- Open Discussion

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 16:00 CET

## Recordings From the Call: [dummyfile.txt](#)

- Full Meeting:
- Topics:

```

```

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;,Announcements
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;

## Agenda

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio
  
  - Started from Andrew's script, SQLite only though
  - Adding Postgres support
  - Upgraded the per database wallet and adding tests
  - Repo is: [https://github.com/Indicio-tech/acapy-wallet-upgrade](https://github.com/Indicio-tech/acapy-wallet-upgrade); open question as to where it will live in the end – ACA-Py or external?  Leaning to leaving it outside.
  - Current branch: [https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support](https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support)
  - From [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) – AFJ issue: [https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support](https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support)
- Ledger-Agnostic AnonCreds Interface is ACA-Py: progress
  
  - Issue: [#2044 in ACA-Py](https://github.com/hyperledger/aries-cloudagent-python/issues/2044) is about the ledger-agnostic AnonCreds interface
  - Hack MD Document: [https://hackmd.io/Ailjb-WDTeC48EjF0gjrGA](https://hackmd.io/Ailjb-WDTeC48EjF0gjrGA)
    
    - DID Registration interface from DIF: [https://identity.foundation/did-registration/](https://identity.foundation/did-registration/) – basis of the API
    - Bottom line – a new endpoint /anoncreds will be added to the Admin API for handling AnonCreds
      
      - Will handle the differences in the ledgers
      - Tricky will be handling endorsing within Indy – and possibly other ledgers that need similar (but not the same) support
  - RootsID working on Cardano AnonCreds implementation
    
    - [https://github.com/roots-id/cardano-anoncreds](https://github.com/roots-id/cardano-anoncreds)
    - AnonCreds Method Registry entry: [https://hyperledger.github.io/anoncreds-methods-registry/#cardano-anoncreds-method](https://hyperledger.github.io/anoncreds-methods-registry/#cardano-anoncreds-method)
  - Question from Alex in chat:  What would be the process to add cheqd and cardano anoncreds in acapy 1.0? Is the driver to write to the ledger enough?
    
    - From Timo Glastra : Alex, there's some work that needs to be done on the did registrar module, as you need to have the key in the wallet to publish to the ledgers
- BC Gov ACA-Py 1.0 Priorities – [Project](https://github.com/orgs/hyperledger/projects/10/views/1)
  
  - Adding a [Documentation site](https://github.com/hyperledger/aries-cloudagent-python/issues/1951) for ACA-Py - as nice as the AFJ one - [https://aries.js.org/](https://aries.js.org/)
  - [AIP 2.0 Support](https://github.com/hyperledger/aries-cloudagent-python/blob/main/SupportedRFCs.md#aip-20)
    
    - Legacy Peer DIDs / Peer DIDs / DID Key / Encryption Envelope
    - Please Ack
  - Other activities:
    
    - Cluster Support - PQs and Shared Cache - Documentation and Testing
    - OCA for Aries – Issuer support, plus holder for testing
    - Ledger Agnostic DIDs
    - Ledger Agnostic AnonCreds
      
      - Drop indy-sdk support in 1.0?
        
        - OK if we have the upgrade script and do some patch releases if really needed.
        - Agents with different underlying features can interop – indy-sdk and shared-components
  - Need a release roadmap, as that is a long list for 1.0.0.
- Open Discussion
  
  - Encryption Envelope for DIDComm V2, issues to discuss: 
    
    - Encryption envelope in Askar - how do we proceed to get that created?
    - Other libraries are available (Python, Rust, others) - e.g., SICPA – should we use one of those are keep working on Askar's implementation?
      
      - Askar – somethings are still missing
      - SICPA Python library is more complete - suggestion is to use that - donated to the OWF - contact SICPA to find out development status
        
        - Indicio also looking at it.
        - Use authlib – private keys are being called to a library – makes it harder to use an HSM for handling secrets
      - 2 or 3 others available - Rust, Go
      - Decision: Go with SICPA library for now.
  - Python upgrade
    
    - Completing the upgrade away from 3.6.  What is needed?
      
      - Creating images for 3.9 as the target - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) has started, but if others want to pick it up, he'll review.
    - Why are 3.7 and 3.10 failing?  Could be a dependency issue away from 3.6.
    - First important step is 3.9 images.

## Next Meeting

- Does anyone use/see a use case for Web Sockets and Return Route beyond ACA-Py as a mobile agent mediator?
- Issue [2029](https://github.com/hyperledger/aries-cloudagent-python/issues/2029): Additional security controls for webhooks for multi-tenancy

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18500944/18517413.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
