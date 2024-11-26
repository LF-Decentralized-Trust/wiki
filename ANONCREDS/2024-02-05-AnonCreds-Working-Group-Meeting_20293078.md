1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)

# Hyperledger AnonCreds : 2024-02-05 AnonCreds Working Group Meeting

Created by Stephen Curran, last modified on Feb 05, 2024

## Summary

- AnonCreds in W3C Format - Status Update / Issues - Demo
- AnonCreds v2 Objects – Review, suggestions – especially ALLOSAUR revocation, verifiable encryption, and (perhaps) other advanced ZKP capabilities
- Open Discussion

## Time: 7:00 Pacific / 16:00 Central Europe Call Link: [https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09](https://zoom.us/j/97954159540?pwd=WWk3WmQ3MVh1SXBYZGVreGl0QllGdz09)

## Recording:

## Extracted from the recording – Credo demo of AnonCreds in W3C VCDM format:

A demo of the Credo Framework ([https://github.com/openwallet-foundation/credo-ts](https://github.com/openwallet-foundation/credo-ts)) issuing, holding, presenting and verifying AnonCreds Verifiable Credentials that are exchanged in the W3C Verifiable Credential Data Model using Data Integrity proofs. Presented at the AnonCreds Working Group Meeting by Animo Solutions ([https://animo.tech/](https://animo.tech/)).

## Notices:

This specification creating group operates under the Linux Foundation [Community Specification License v1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md).

cifi![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Meeting Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

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

- AnonCreds in W3C Format - Status/Updates
  
  - Demo (recording here) from Martin Auer of Animo Solutions
  - Proposal to use new format for issuing: [https://github.com/hyperledger/aries-rfcs/pull/809](https://github.com/hyperledger/aries-rfcs/pull/809) (based on [https://hackmd.io/JEIOxf\_ETnaX33kTIu7YJw?view](https://hackmd.io/JEIOxf_ETnaX33kTIu7YJw?view))
  - Test Vectors Repo: [https://github.com/TimoGlastra/anoncreds-w3c-test-vectors](https://github.com/TimoGlastra/anoncreds-w3c-test-vectors)
  - Attachment Format to use for Present Proof will be DIF Presentation Exchange - [Aries RFC 0510](https://github.com/hyperledger/aries-rfcs/tree/main/features/0510-dif-pres-exch-attach)
  - ACA-Py work [design document in repo](https://github.com/hyperledger/aries-cloudagent-python/blob/main/docs/design/AnoncredsW3CCompatibility.md)
  - AnonCreds RS [PRs](https://github.com/hyperledger/anoncreds-rs/pulls)
- AnonCreds V2 Objects - [Presentation](https://docs.google.com/presentation/d/1tQsTdNAAgOvug5Nbkt3x3I_nxPBPJjE10LpoVJKXWqE/edit?usp=sharing) from last meeting, evolved
  
  - How does ALLOSAUR Revocation work? High level – not at the crypto. More about what data gets generated (inputs, size) and shared between participants.
    
    - Data:
      
      - Accumulator – fixed sized digest regardless of the number of credentials - public
      - Elements of the set – one per credential – could be whatever you want (e.g. Hashed UUIDs) – what the holder gets associated with their credential.
        
        - Must be tracked by the issuer and associated with the holder – this is what gets revoked – this element is removed from the accumulator.
      - The "witness" (aka revocation handle, revocation signature) – known only to the holder, created by the issuer. Needed, with the element, to produce the holder's NRP (Non-Revocation Proof).
      - The key pair used for managing the revocation registry. Verifiers must have the accumulator (that the holder used) and the public key.
    - Issuer and Revocation Manager relationship
      
      - Could be one and the same, but could be separate.
      - Separated out "thresholdizing the private key of the revocation set" – if different than the issuer, the private key can be split across revocation manager (called MPC – multi-party computation).
      - Accumulator must change when elements are removed.
      - Issuer notifies the revocation managers of elements that are removed.
        
        - Requires some part of the private key to do the removals.
    - Issuer setup
      
      - Decides on the element construction – e.g. a hashed UUID
      - Requests a new revocation manager create a new registry – new key is created.
        
        - Revocation managers use a distributed key generation (DKG) – where it may be just one.
      - Publishes the public key
      - Publishes the accumulator
    - Issuer credential issuance
      
      - Issuer generates an element
      - Element sends element to revocation manager
        
        - Issuer requests from the revocation manager the witness for a given element, forwards this to the holder.
      - Data to holder
        
        - Signed credential, element, witness, accumulator
    - Issuer revocation
      
      - Authorization, element(s) being revoked.
      - Revocation manager returns the new accumulator
      - Issuer publishes the new accumulator
    - Verifier presentation request
      
      - Verifier gets accumulator from a public location (could get multiple), and public key
        
        - Allows the verifier to define how fresh of a revocation they want
      - Sends those to the holder.
    - Holder and revocation manager for presentation – request data, response data 
      
      - Holder checks if they already have the data for that accumulator – generates the NRP using the element and witness
      - If not, holder contacts (somehow) revocation manager to get a new witness
        
        - Sends Schmir's Secret split of their element to the revocation managers and requests their witness – could send multiple splits to the same revocation manager – assembles resulting shares
          
          - Could do this with a single revocation manager — split element
    - Holder to verifier non-revocation proof data
      
      - NRP that is generated using the element and witness, accumulator
    - Verifier and revocation manager – request data, response data
      
      - Verifier has already retrieved the accumulator or the verifier confirms the accumulator that the holder gave them.
  - How does Verifiable Encryption work?
    
    - Issuer setup
    - Issue process
    - Holder/Verifier presentation request / presentation
    - Decryption process
- Open Discussion
  
  - Workshop This Thurs Feb 8: [Decentralized Identity + Interoperability: Connecting Credo (Agent Framework Javascript) with Hyperledger Besu, Cardano, Cheqd, Hyperledger AnonCreds, and OIDC4VCFuture Calls](https://zoom.us/meeting/register/tJUuf-6srToiGdQZCHMxaJZoON1RCuwiDRcY)
  - Workshop Weds April 24th: [Zero Knowledge Proofs and ZK Programming in Blockchain Application Development](https://zoom.us/meeting/register/tJYkfuyhpjsqGd1FCs-ZeFzD90EyqFy18IMt)

## To Dos:

## Action items

- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

## W3C AnonCreds + AFJ Demo

- Aries Framework JavaScript repo: [https://github.com/DSRCorporation/aries-framework-javascript/tree/w3c-demo-poc](https://github.com/DSRCorporation/aries-framework-javascript/tree/w3c-demo-poc)
- Anoncreds-RS library, Anoncreds-NodeJs, and Anoncreds-Shared are built from the branch: [https://github.com/DSRCorporation/anoncreds-rs/tree/anoncreds-wc3-wrappers](https://github.com/DSRCorporation/anoncreds-rs/tree/anoncreds-wc3-wrappers)
  
  - Use main implementation (not included, dropping of `mapping`  and `encoding`  changes)
- Update AFJ `@hyperledger/anoncreds-nodejs`  and \`@hyperledger/anoncreds-shared\` dependencies to use locally built packages

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
