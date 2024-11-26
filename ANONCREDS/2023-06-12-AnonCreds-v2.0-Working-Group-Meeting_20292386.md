1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-06-12 AnonCreds v2.0 Working Group Meeting

Created by Stephen Curran, last modified on Jun 23, 2023

## Summary

- Update on AnonCreds Happenings
- Discussion: Modularity in the Underlying Signature Schemes - Mike Lodder
- Understandable names for schema types
- Presentation Data Models
- Open Discussion

## Recording of Call:  [https://youtu.be/qAkODMA3dgc](https://youtu.be/qAkODMA3dgc)

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Meeting Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Repositories:

- Mike Lodder's proposed Data Models: [https://hackmd.io/ZlsnLoclSveePJOZljgMfA](https://hackmd.io/ZlsnLoclSveePJOZljgMfA)
- AnonCreds v2.0 Specification Repository: [https://github.com/hyperledger/anoncreds-spec-v2/](https://github.com/hyperledger/anoncreds-spec-v2/)
- AnonCreds v1.0 Specification: [https://hyperledger.github.io/anoncreds-spec/](https://hyperledger.github.io/anoncreds-spec/)
- AnonCreds Methods Registry: [https://hyperledger.github.io/anoncreds-methods-registry](https://hyperledger.github.io/anoncreds-methods-registry)
- AnonCreds Rust Open Source Code: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)

## Goals of the Working Group:

The goal of AnonCreds v2.0 is to retain and extend the privacy-preserving features of AnonCreds v1.0, while improving capabilities, performance, extensibility, and security.

## Meeting Preliminaries:

- Welcome and Introductions
- Announcements:
  
  - 2023.05.15 (this Thursday): Presentation: [ZKPs – the High School Math Edition](https://lf-hyperledger.atlassian.net/wiki/display/IWG/2023-06-15%3A+Identity+Special+Interest+Group) - [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) at the Identity SIG Meeting
- Updates to the Agenda?

## Agenda

- Update on AnonCreds Happenings
- Discussion: Modularity in the Underlying Signature Schemes - Mike Lodder
  
  - AnonCreds v2.0 could use one of four (CL, BLS, BBS, and PS) signatures schemes at the moment. How does that work?
  - As with CL Signatures, data is encoded as numbers
  - The additional Schema Claim data allows for "improved" encoding – e.g. zero centring integer data
  - The signature type and the Schema Claim data determine exactly what is needed per claim to enable comparable presentation ZKP capabilities.
    
    - These will have to be defined in the specification – e.g.
      
      - the requirements of the cryptography for the features, and,
      - for specific signatures to be supported (perhaps BBS+ and PS), the details of using those signatures
- Purposes/use cases for the Schema Types proposed for AnonCreds v2.0, with a goal of leading to some useful names for the different types:
  
  - Enumeration
    
    - Hashed
    - Numeric
    - Scalar
  - String
  - Unsigned Byte/Binary
    
    - **Hashed**: claim data is hashed before signing
    - **Numeric**: claim data is zero centered before signing
    - **Scalar**: claim data is already a cryptographic value. Equivalent to a null hash
- Predicates:
  
  - Hide signature – proof of signature (unlinkable)
  - Hide attribute - reveal or hide - Schnorr Proof
  - Set memberships, such as
    
    - Zip/postal Code
    - State
    - City
    - Accumulator
  - Commitment - same value
  - Range Proof
  - Verifiable Encryption
  - Commitment
  - Not discussed: Claim equality across credentials (e.g. proof that the claims in two credentials are the same without sharing the value).

## Future Calls

- Collect some use case specific examples and continue the discussions:
  
  - Applying the data structures to a real use case or two
    
    - Take an existing AnonCreds Schema (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/13)) and Credential Definition (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/14)) and define what it would be using Mike's proposed data models.
      
      - Where would the data models exist, such as on ledger, in the AnonCreds specification?
  - What concrete uses other than link-secret is there for blinded data in a credential?

## To Dos:

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
