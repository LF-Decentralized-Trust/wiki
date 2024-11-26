1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)

# Hyperledger AnonCreds : 2024-03-18 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on Mar 18, 2024

## Summary

- Status Updates on AnonCreds in W3C VCDM Format projects
- Revocation Manager for ALLOSAUR and AnonCreds – Design
- Schema Object for Complex JSON Objects – Discussion
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
  
  - IIW – April 16-18, 2024
  - Workshop Wed. April 24th: [Zero Knowledge Proofs and ZK Programming in Blockchain Application Development](https://zoom.us/meeting/register/tJYkfuyhpjsqGd1FCs-ZeFzD90EyqFy18IMt)
- Any updates to the Agenda?

## Agenda

- AnonCreds in W3C VCDM Format - Status/Updates
  
  - Test Vectors Repo: [https://github.com/TimoGlastra/anoncreds-w3c-test-vectors](https://github.com/TimoGlastra/anoncreds-w3c-test-vectors)
  - Credo / Bifold Progress
  - ACA-Py Progress
- ALLOSAUR/AnonCreds Revocation Manager Component – what is it, design?  ALLOSAUR/AnonCreds Credential Status Manager (reflects 
  
  - [Presentation](https://docs.google.com/presentation/d/1t9E0djp8zC8QE2GCZvmF6ZuIwMdvM3-uw_iRt9i6TOA/edit?usp=sharing)
  - [Hyperledger Mentorship Program](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Hyperledger+Mentorship+Program)
  - Proposed Hyperledger Mentorship project: [AnonCreds Revocation Manager Component Implementation](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Hyperledger+AnonCreds+v2+ZKP-based+Credential+Revocation+Manager+Implementation)
  - On the Ledger:
    
    - RevRegDef: ID, Public Key, Accumulator, RM URLs
    - RevRegEntry: Accumulator (no list of changed status)
  - Is this NIST-compliant?
    
    - NIST has no approved pairing cryptography libraries, and this is based on pairing cryptography
    - Uses BLS12381 – which is used by many of the blockchains, BBS+, etc. – stronger curve – zCash and others
- Update on the Hyperledger Labs Agora Libraries
  
  - Contributions this week – audits are completed
    
    - Audit Complete: BLSFUL – [https://github.com/mikelodder7/blsful](https://github.com/mikelodder7/blsful) - powers the ALLOSAUR library, replaces what is currently in AnonCreds v2
    - Audit Complete: Gennaro – [https://github.com/mikelodder7/gennaro-dkg](https://github.com/mikelodder7/gennaro-dkg) – distributed key generator
    - Being audited: Verifiable Secret Sharing – [https://github.com/mikelodder7/vsss-rs](https://github.com/mikelodder7/vsss-rs)
    - Plan is to ALLOSAUR into Agora as well
- PS vs. BBS+ Attributes
  
  - Aside: Rumour has it that a PS key size changes based on number of attributes to sign. If so, does that impact support for arrays in complex JSON?
    
    - PS must know the maximum number of claims you are going to sign at credential definition time.  Tradeoff of key size vs. number of claims.
    - PS vs. BBS+ relates to threshold signing.
    - PS has stronger security proofs.
    - PS – smaller and faster to generate
  - Nice point – could choose based on use case.
- Complex JSON in AnonCreds – ideas for the Schema Object
  
  - Thinking about AnonCreds V2 with complex JSON, and what the Schema would look like.
  - In V2, there are is metadata per VC attribute that provides input into the encoding for the element -- e.g., it's a string, an integer, an integer range, a date, an enumerated set, scalar (e.g. link secret).
  - Example of a simple schema to show the metadata: [https://github.com/swcurran/anoncreds-v2-rs/blob/samples/examples/schema-with-linked-secret.json](https://github.com/swcurran/anoncreds-v2-rs/blob/samples/examples/schema-with-linked-secret.json "https://github.com/swcurran/anoncreds-v2-rs/blob/samples/examples/schema-with-linked-secret.json")
  - Question – how do we manage the schema when we need to support complex JSON (structures, arrays). 
    
    - Idea 1: Use JSON.Path so we are back to a list of attributes
      
      - Schema is a flat list like we have in AnonCreds v1, but attribute names are in JSON Path format.
      - Metadata is attached to each attribute in the (flat) list.
    - Idea 2: Use JSON-LD 
      
      - How much would JSON-LD help with this?
        
        - Probably not much
      - Is there already enough data to tell us much of those things?
        
        - I would guess not. It could have a lot of it, but not all that we need.
        - Completely dependent on the use case – definitely not guaranteed. Must be able to supplement it.
      - What tools are there to see for a given JSON-LD document what attributes we know about each attribute?
        
        - Tools are available.
      - Would it make sense to use JSON-LD and supplement attributes as needed?
        
        - Question for the JSON-LD crowd.
    - Idea 3: Combine the two
      
      - Use JSON-LD for much of the data
      - Use JSON.PATH to add additional metadata when needed to specific items.
    - Idea 4: Pure JSON-LD, adding new "features" to get support for what we need
      
      - Don't really know what this entails...
- Open Discussion

## To Dos:

## Action items

- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
