1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)
5. [2023 Meetings: AnonCreds Working Group](20295076.html)

# Hyperledger AnonCreds : 2023-08-21 AnonCreds v2.0 Working Group Meeting

Created by Stephen Curran, last modified on Aug 21, 2023

## Summary

- AnonCreds v1.0 Spec PRs – Cryptographic Elements
- Open Discussion

## Recording of Call:

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
- Updates to the Agenda?
  
  - Patrik: Revocation lists in Anoncreds spec
    
    - revocation lists in relation to indy "from, to" intervals
    - Anoncreds registry specification for indy
    - Anoncreds 2.0 revocation

## Agenda

- PRs from AnonCreds v1.0 Spec.
  
  - Clarification about nonces used in the issue credential process:
    
    - Nonces are used to prevent replay attacks, requiring the other party to use the nonce in proofs, thus requiring that they be calculated in real time – and preventing the reuse of a previously calculated proof.
    - Issuer generates nonce n0 and sends it to the holder in OfferCredential data structure.
    - Holder:
      
      - Uses nonce n0 in creating the blinded\_link\_secret\_correctness\_proof that proves the holder knows the link secret that was used to create the blinded link secret.
      - Generates nonce n1.
      - Sends both the  blinded\_link\_secret\_correctness\_proof and n1 to the issuer in the RequestCredential data structure.
    - Issuer:
      
      - Uses nonce n0 and the blinded\_link\_secret\_correctness\_proof to verify the proof.
      - Uses the nonce n1 when creating the signature\_correctness\_proof that proves the issuer knows the private keys used to generate the signature over the credential (didn't just send a previously signed credential).
      - Sends the data, signature, and signature\_correctness\_proof to the holder.
    - Holder
      
      - Uses nonce n1 to verify the signature\_correctness\_proof
      - Accepts the credential from the issuer as valid.
- Open Discussion

## Future Calls

- Collect some use case specific examples and continue the discussions:
  
  - Applying the data structures to a real use case or two
    
    - Take an existing AnonCreds Schema (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/13)) and Credential Definition (maybe [this](https://candyscan.idlab.org/tx/CANDY_PROD/domain/14)) and define what it would be using Mike's proposed data models.
      
      - Where would the data models exist, such as on ledger, in the AnonCreds specification?
  - What concrete uses other than link-secret is there for blinded data in a credential?

## To Dos:

Schema Claim Type:

- Would it make sense defining encodings for date related schema claim types that are especially useful to use in ZKP predicates?
  
  - "iso860\_date" – encodes to dateint e.g., 2023.06.26 is 20230626
  - "iso860\_datetime" - encodes to Unix Time e.g., seconds since Jan 1, 1970
- Yes – these would be "numbers" by type, but with special encoding handling.

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
