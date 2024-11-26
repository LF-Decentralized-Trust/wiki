1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)

# Hyperledger AnonCreds : 2024-05-20 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on May 20, 2024

## Summary

- Survey of Communities Working on Privacy Preserving Credentials
- Reminder: New Meeting Times

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
  
  - Identiverse - next week
  - EuroCrypt
  - EIC
  - Identity Week
  - DICE – IIW Europe
- Any updates to the Agenda?

## Agenda

- Survey about the various privacy preserving verifiable credential efforts taking place.
  
  - [Dock response](https://docs.google.com/document/d/1ZcYHEbbQ468zjiKULp8mgccuuJpMnw7yxBS0mGJs6Kw/edit?usp=sharing)
  - [Other responses](https://docs.google.com/presentation/d/1ANjeNyzDDnL1pshF12jirLmapSKRdMw75d60S29vCHg/edit?usp=sharing)
    
    - Digital Bazaar - W3C VC-DI-BBS
    - Academic/Research
      
      - Internet Initiative Japan Inc.
    - Portage (Canada)
    - Oracle Labs
    - Hyperledger AnonCreds v2
- VC-DI-BBS Specification and AnonCreds V2 – getting to collaboration?
  
  - BBS Signatures specification is moving through IETF – [https://datatracker.ietf.org/doc/draft-irtf-cfrg-bbs-signatures/](https://datatracker.ietf.org/doc/draft-irtf-cfrg-bbs-signatures/)
    
    - Incubation happening at DIF
  - DHS has announced support for using BBS Signatures for selective disclosure and unlinkability
    
    - Intended approach is to use Parallel Signatures, and to sign VCs with a NIST approved signature and BBS Signatures
  - W3C Working Group has a release candidate spec – [vc-di-bbs](https://w3c.github.io/vc-di-bbs/)
    
    - Selective disclosure, unlinkability, holder binding, pseudonyms (issuer and holder defined) (directed identifiers)
    - Left off – revocation (!!), blinded secret, claim equality, set membership, range proof, signed integer
    - [RDF Canonicalization](https://www.w3.org/TR/rdf-canon/) is used – JSON-LD-based, and same as other VC-DI cryprosuites
- Getting BBS Support into AnonCreds v2
  
  - Started, but not complete
- Audit: 
  
  - blsful - audit complete and published in Agora
  - Focus: Key Share Proofs
  - Audit complete: Genaro to be contributed
  - Verifiable secret sharing – under audit
- Reminder of new meeting times
  
  - Second Monday of each month – 7:00 Pacific / 16:00 Central Europe
  - Fourth Monday of each month – 15:00 Pacific / 16:00 Mountain / Super Late Central Europe (Midnight...) / 10:00 Auckland 
    
    - **Except this month – May**, because of the US Memorial Day Holiday – replacement meeting May 20, 2024 (this meeting).
- Open Discussion
  
  - Using an accumulator or a bloom filter as a space-efficient way to enable set membership of hashes? For example:
    
    - Up to a million high-entropy hashes
    - Only needed query: "is hash XYZ in the set (Y/N)?" – e.g., given hash XYZ and the database (accumulator, bloom filter), can I answer that question?
    - XOR filter

## To Dos:

## Action items

- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
