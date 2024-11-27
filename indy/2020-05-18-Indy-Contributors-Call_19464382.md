1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-05-18 Indy Contributors Call

Created by Stephen Curran, last modified on May 18, 2020

## Summary

Planned:

- Work updates:
  
  - Indy VDR
  - Indy Credx
  - Aries Credx
  - Aries Storage
- Update on Revocation 2.0 - progress and discussion on desired properties

## The call was recorded is available here: [20200518 Indy Contributors Call](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Calls and Announcements

- Identity Implementer Working Group call ([Wiki Page](https://lf-hyperledger.atlassian.net/wiki/display/IWG/Identity+WG+Implementers+Call)) - every 2nd Thursday

## Release Status and Work Updates

- Move from Sovrin Foundation infrastructure - **Help Wanted**
  
  - Move from Jenkins to GitHub actions
    
    - Sovrin Foundation Jenkins machines are going away
    - [Sovrin resource migration](https://lf-hyperledger.atlassian.net/wiki/spaces/CICD/pages/19011213/Sovrin+resource+migration)
    - #cicd discussion "Indy CI / CD Migration" (in #cicd use menu item "Discussions" to see/get to the discussion)
  - Move repo.sovrin.org → Hyperledger Artifactory for all except Sovrin Foundation specific artifacts
- Indy Node
  
  - June:
    
    - Replacing Indy Crypto with Ursa (Kiva)
    - More "rich schema" objects
    - Ubuntu 20.04 (Kiva)
      
      - Need to check additional dependencies: 
        
        Error rendering macro 'jira' : null
- Indy SDK
  
  - June:
    
    - Indy VDR into LibIndy
    - Indy Credx into LibIndy
- Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
      
      - Nearing release 0.6(?) - most work complete that was needed: Design doc, FFI, testing, CI / CD
        
        - CI - GitHub actions runs unit tests and basic integration tests
        - CD not there
        - No design doc, but crate docs
        - Rich Schema merged and behind a feature flag
        - Refactoring PR not merged - cleanup, internal simplification, crate docs
    - indy-credx - [https://github.com/bcgov/indy-credx](https://github.com/bcgov/indy-credx)
      
      - Experimental ACA-Py branch created that can do credential exchange with indy-credx
    - indy-shared-rs - [https://github.com/bcgov/indy-shared-rs](https://github.com/bcgov/indy-shared-rs)
      
      - Shared features across indy-vdr and indy-credx
      - pack/unpack on Ursa (not libsodium)
    - aries-credx
      
      - [https://github.com/sovrin-foundation/aries-credx-framework-rs](https://github.com/sovrin-foundation/aries-credx-framework-rs)
        
        - 6 most common attribute encodings (but not anoncreds 1 attribute encoding)
      - Can make a non-revocable credential and create proofs.
    - Aries Secure Storage initiatives:
      
      - Mike working on documentation and architecture as an Aries RFC (KMS architecture) and Ursa RFC (API)
        
        - PR is submitted: [https://github.com/hyperledger/aries-rfcs/pull/440](https://github.com/hyperledger/aries-rfcs/pull/440)
      - Mike and Cam's work aries-kms-mayaguez - Postgres backend for credential storage
        
        [https://github.com/sovrin-foundation/aries-kms-rs](https://github.com/sovrin-foundation/aries-kms-rs)
        
        - Persistence work allows plugging in any database engine.
        - Focus is using an external enclave.
      - aries-kms-vostok
        
        - Andrew also working on that
  - Ursa
    
    - BBS+ added
    - 0.3.5 pending, plus new additions

## Meeting Topics

- Indy Performance Testing
- Revocation 2.0 
  
  - Tech Spike on Merkle Trees in process ([Daniel Hardman](https://lf-hyperledger.atlassian.net/wiki/people/557058:d8f2338c-759d-4e0c-bb47-14386507f414?ref=confluence))
    
    - Tech Spike Implementation: [https://github.com/dhh1128/merklespike](https://github.com/dhh1128/merklespike)
    - Notes on Issues: [size of compressed leaves](https://github.com/hyperledger/indy-node/issues/1596), [resources to calculate internal nodes](https://github.com/hyperledger/indy-node/issues/1597)
    - Good progress on time to a size of about 256k but the memory usage is high (1GB).
      
      - Optimizations likely for performance and size as possible next steps.
  - Tech Spike on using ranges in the bitstream ([Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)) which is looking very promising
    
    - 1M revocation registry seems viable, 16M may be possible
    - Question as to whether this approach will yield a range proof (user exposes range) or a ZKP
    - Next step: [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence) [Mike Lodder](https://lf-hyperledger.atlassian.net/wiki/people/557058:23b28066-a30e-4a6b-9b86-34dae49fd7f0?ref=confluence) [Brent Zundel](https://lf-hyperledger.atlassian.net/wiki/people/557058:bf590372-a52e-4c12-b1da-0c07b8b0a512?ref=confluence)to discuss and define if work on this approach should continue.
  - **Discussion**: How big should a revocation registry should be?
    
    - What constraints should be applied?
      
      - Issuer: revocation profile (% revoked, frequency), total credential pool size, number of rev. registries
      - Holder (especially mobile holder) resources: bandwidth, memory, compute resources, revocation frequency
      - Verifier: Rev Registries/Entries
      - Ledger: Rev Entry size, frequency, reads
      - Herd size
    - Should it be as large as possible within the tightest constraints, or should we aim for just a specific size?
    - **Answer**: Go for the largest that we can achieve within the constraints, with a likely minimum acceptable size being 1M credentials/registry
      
      - Issuers can choose smaller based on the use case, but we should aim for the largest feasible.

## Future Calls

Next call:

Future:

- Requirements questions:
  
  - IS-1099: anoncreds.prover\_get\_credentials\_for\_proof\_req should return per-credential timestamp
    
    - Should we allow duplicate credentials from the same issuer?

## Action items

- PR to RFC #0019 to compare pack/upack to msgpack (Sergey)
- Review the 61 cases of "unsafe" libindy calls and figure out if they are justified.

## Call Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464382/19465417.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
