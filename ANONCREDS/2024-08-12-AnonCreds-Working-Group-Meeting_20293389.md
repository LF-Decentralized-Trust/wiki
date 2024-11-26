1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)

# Hyperledger AnonCreds : 2024-08-12 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on Aug 12, 2024

## Summary

- Further Update: Proposed scheme for unlinkability with ZKPs using hardware based holder key
- Project status updates – Revocation Manager for ALLOSAUR, BBS, auditing
- AnonCreds Project Charter
- Merging BBS Efforts
- Open Discussion

## Time: 7:00 Pacific / 16:00 Central Europe Call Link: [https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09](https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09)

## Recording:

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

cifi![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Meeting Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Specifications and Repositories:

- AnonCreds v1.0:
  
  - The v1.0 specification is published here: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
  - The Working Group uses this GitHub repository to manage the specification: [https://github.com/hyperledger/anoncreds-spec](https://github.com/hyperledger/anoncreds-spec)
  - The AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
  - The v1.0 implementation in Rust is here: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
  - The v1.0 implementation is dependent on this Rust CL Signatures implementation: [https://github.com/hyperledger/anoncreds-clsignatures-rs](https://github.com/hyperledger/anoncreds-spec-v2)
- AnonCreds v2.0
  
  - The initial framework for the v2.0 specification repository is here: [https://github.com/hyperledger/anoncreds-spec-v2](https://github.com/hyperledger/anoncreds-spec-v2)
  - The v2.0 implementation in Rust is here: [https://github.com/hyperledger/anoncreds-v2-rs](https://github.com/hyperledger/anoncreds-v2-rs)
  - Underlying AnonCreds v2.0 are cryptographic libraries in Hyperledger Labs Agora

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
- Any updates to the Agenda?

## Agenda

- Proposal from Dfinity / Google / Jan Camenisch for using ZKPs with Hardware Keys
  
  - Follows:
    
    - Feedback from Cryptographers on the European ARF
      
      - GitHub Issue: [https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/issues/66](https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/issues/66)
      - Paper: [https://github.com/user-attachments/files/15904122/cryptographers-feedback.pdf](https://github.com/user-attachments/files/15904122/cryptographers-feedback.pdf)
      - Proposal: [EUDI\_Follow\_up-2.pdf](#)
    - ECDSA proposal – early days. Start of an academic paper. – [EUDI\_\_\_Generic\_ZK\_\_\_ECDSA\_Proposal.pdf](attachments/20293389/20295323.pdf). The work is based on [Ligaro (Ames, Ishai, Hazay, Venkitasubramaniam)](https://dl.acm.org/doi/pdf/10.1145/3133956.3134104).
      
      - Must go through all the rigour, and then through standardization.
      - Digital Bazaar objects because it lacks a pseudonymous identifier for the credential – same complaint it had about AnonCreds back in the day.
      - Push for BBS to be reviewed by Cryptographers.
- Status updates from current work:
  
  - Revocation Manager for ALLOSAUR Project – Hyperledger Mentorship project being executed by [VictorH2208](https://lf-hyperledger.atlassian.net/wiki/people/712020:a4e736ac-f0a4-4270-ae8b-ef76cebf844d?ref=confluence)[Project plan](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Project+Plan+-+AnonCreds+v2+Credential+Revocation+Manager+Implementation)
  - BBS Signatures
  - Audit Updates from Mike Lodder: 
    
    - blsful - audit complete and published in Agora
    - Audit complete: Genaro to be contributed
    - Audit Complete: verifiable-secret-sharing – some changes, and some ripple affects, such as to Genaro.
- AnonCreds Project Charter:
  
  - Stems from the recent "intent to form" [announcement](https://www.linuxfoundation.org/press/linux-foundation-announces-intent-to-form-lf-decentralized-trust) from the Linux Foundation and Hyperledger Foundation about LF Decentralized Trust.
  - Proposed Charter: [https://docs.google.com/document/d/1UiUv2H\_xOHxV\_rXfTSlsPu2TdQjgxNlVhU67RtqbMlM/edit?usp=sharing](https://docs.google.com/document/d/1UiUv2H_xOHxV_rXfTSlsPu2TdQjgxNlVhU67RtqbMlM/edit?usp=sharing)
  - Plan:
    
    - Create an "anoncreds" repo, similar to this [Aries repo](https://github.com/hyperledger/aries).
    - Put into it a "TSC.md" file that lists the TSC members and processes – same as this [TSC.md in Aries](https://github.com/hyperledger/aries/pull/22/files?short_path=a30a225#diff-a30a2252bbf738b901d35399ea54d5f4dffbbf6bf9e2619de7c3fe53b14c7262).
    - Put into it a "MAINTAINERS.md" that points to the Hyperledger "[access-control.yaml](https://github.com/hyperledger/governance/blob/main/access-control.yaml)" file and processes of Maintainers – same as this [MAINTAINERS.md in Aries](https://github.com/hyperledger/aries/pull/23/files?short_path=39da3bd#diff-39da3bd6270d44ea37b6ed50bd42eeb9d93ac5e1639645871a69cbe08cbe29de).
    - Put a "MAINTAINERS.md" ([like this one](https://github.com/hyperledger/aries-mediator-service/pull/167/files?short_path=39da3bd#diff-39da3bd6270d44ea37b6ed50bd42eeb9d93ac5e1639645871a69cbe08cbe29de)) file in all repos that points to the "[access-control.yaml](https://github.com/hyperledger/governance/blob/main/access-control.yaml)" file and to the AnonCreds repo MAINTAINERS.md ^^^^^^
    - Update the charter to match roughly what is in the [Aries Charter](https://docs.google.com/document/d/1F6RbR7xDaBt5CDJhqLJzR4c1pDJtyPGshp9fy6eVtSM/edit?usp=drive_link)
- PQ Efforts for Revocation
  
  - PQ equivalent to ALLOSAUR – fast, scalable, unlimited.
  - Research – very fast set membership for both lattice and elliptic curves (need not be pairing friendly).
    
    - Tweak to bullet proofs.
    - As high as: 2^38 memberships – pre-allocated – but can be a smaller set.
    - Less than 1 sec. to make proof, less than 1 sec. to verify.
- Open Discussion

## To Dos:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [EUDI\_\_\_Generic\_ZK\_\_\_ECDSA\_Proposal.pdf](attachments/20293389/20295323.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
