1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)

# Hyperledger AnonCreds : 2024-06-24 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on Jun 24, 2024

## Summary

- Feedback from Cryptographers on the European ARF
- Recap of DICE (Decentralized Identity unConference Europe) and other Conferences
- Suggestion from Jan Camenisch – ZKP to prove bound Hardware Key to a ZKP Proof
- Revocation Manager for ALLOSAUR
- Help Me Understand
  
  - How do we BBS Support into AnonCreds v2?
  - What BBS Library should we use?
  - Are all of the AnonCreds v2 features supported in all Libraries?

## Time: 15:00 Pacific / 16:00 Mountain / Super Late Central Europe (Midnight...) / 10:00 Auckland Call Link: [https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09](https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09)

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
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com

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
  
  - Identiverse - next week
  - EuroCrypt
  - EIC
  - Identity Week - this week
  - DICE – IIW Europe
- Any updates to the Agenda?

## Agenda

- Feedback from Cryptographers on the European ARF
  
  - GitHub Issue: [https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/issues/66](https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/issues/66)
  - Paper: [https://github.com/user-attachments/files/15904122/cryptographers-feedback.pdf](https://github.com/user-attachments/files/15904122/cryptographers-feedback.pdf)
- Recap of DICE (Decentralized Identity unConference Europe) and other Conferences
- Suggestion from Jan Camenisch – ZKP to prove bound Hardware Key to a ZKP Proof
- Revocation Manager for ALLOSAUR
- Help Me Understand:
  
  - Comparing Dock Networks Library and AnonCreds v2: Apples to Apples or Apples to Oranges?
  - How do we BBS Support into AnonCreds v2?
    
    - Hyperledger Labs Agora will have a BBS Library
      
      - [https://github.com/hyperledger-labs/](https://github.com/hyperledger-labs/) search for "agora" to see the (currently) 5 libraries.
    - MTTR has an old version
    - W3C VC-DI-BBS working group – it BBS, blinded secret, pseudonymous identifiers (holder-, issuer-based)
  - What BBS Library should we use?
    
    - Coming Real Soon – will be in Agora
  - Are all of the AnonCreds v2 features supported in all Libraries?
- Audit Updates from Mike Lodder: 
  
  - blsful - audit complete and published in Agora
    
    - Now compatible with Dock Networks
  - Focus: Key Share Proofs
  - Audit complete: Genaro to be contributed
  - Audits coming: verifiable-secret-sharing, threshold-mpc libraries
- Next Meeting
- Open Discussion

## To Dos:

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
