1. [Hyperledger AnonCreds](index.html)
2. [Hyperledger AnonCreds](Hyperledger-AnonCreds_20283406.html)
3. [AnonCreds Working Group](AnonCreds-Working-Group_20291468.html)
4. [Meetings: AnonCreds Working Group](20291486.html)

# Hyperledger AnonCreds : 2024-02-19 AnonCreds Working Group Meeting -- Cancelled

Created by Stephen Curran, last modified on Mar 04, 2024

## Summary

- Meeting Cancelled – Holidays in the US and Canada

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

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

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
  
  - AnonCreds annual review at the Hyplerledger TOC – this Thursday, February 15th – [Meeting Notice](https://lists.hyperledger.org/g/toc/viewevent?repeatid=52670&eventid=2208914&calstart=2024-02-15)
  - Workshop Weds April 24th: [Zero Knowledge Proofs and ZK Programming in Blockchain Application Development](https://zoom.us/meeting/register/tJYkfuyhpjsqGd1FCs-ZeFzD90EyqFy18IMt)
  - IIW – April 16-18, 2024
- Any updates to the Agenda?

## Agenda

- AnonCreds in W3C Format - Status/Updates
  
  - Test Vectors Repo: [https://github.com/TimoGlastra/anoncreds-w3c-test-vectors](https://github.com/TimoGlastra/anoncreds-w3c-test-vectors)
  - Attachment Format to use for Present Proof will be DIF Presentation Exchange - [Aries RFC 0510](https://github.com/hyperledger/aries-rfcs/tree/main/features/0510-dif-pres-exch-attach)
  - ACA-Py work [design document in repo](https://github.com/hyperledger/aries-cloudagent-python/blob/main/docs/design/AnoncredsW3CCompatibility.md)
  - AnonCreds RS [PRs](https://github.com/hyperledger/anoncreds-rs/pulls)
- Recent updates to AnonCreds RS – [0.2.0 release](https://github.com/hyperledger/anoncreds-rs/pulls?q=is%3Apr%20is%3Amerged%20closed%3A%3E2023-06-02)
  
  - When AnonCreds v1.0 1.0.0?
- AnonCreds V2 ZKP Capabilities
  
  - Adding BBS+ to the library?
    
    - Extraction layer – abstracting other signatures, once done, adding BBS+ available.
  - Missing Object – revocation registry
    
    - Verifying key (96) and accumulator (48) – VK could be the identifier.
    - Definition - not needed
    - State - published on every accumulator update
  - How does Verifiable Encryption work?
    
    - Can be done by any party – need a BLS key pair - issuer, auditor, etc.
    - Issuer setup – anything? Encoding types?
      
      - Public key has to be published somewhere – most likely the CredDef,
      - A "message\_generator" - point on the curve, like the public key – could use this to tie it down to a specific field.
    - Issue process
      
      - Nothing is done with VE at issuance time
      - Can be used with any claim
        
        - Could be used for specific values, e.g., Credit Card Number
        - But not defined apriori
        - Could use for a unique value – e.g. the revocation key
    - Verifier presentation request
      
      - Please give me a VE about a certain claim – reference to the two public data items (generator, pubkey), reference to attribute
    - Holder
      
      - Generates the encrypted value (verifiable cyphertext). Will be unique because of the nonce from the verifier.
    - Decryption process
      
      - Pass cyphertext (nonce, generator is embedded in cyphertext) to someone that knows the private key – decrypt to get the claim
  - Equality proofs – claims across two source verifiable credentials
    
    - Could be in the same credential
    - Statement ID, List/Map of statement ID, claim ID.
    - Holder:
      
      - Creates a proof statement based on input of the claims
    - Verifier:
      
      - Verification of the proof and data
    - AnonCreds v1 aggregate – called "challenge" right now.
      
      - All of the proofs were generated by one holder
      - A signature over all of the proofs knew the raw data.
      - Not associated with the link secret in v1
        
        - In v1, there was an equality proof
      - Proofs that the data was fresh – e.g. used the same nonce in all of the proofs
        
        - In example – proof request ID is the nonce – everything is included in the aggregate proof signature.
  - Domain proofs (called a Commitment in V2) – consistent identifiers for a verifier – different across different verifiers
    
    - Issuer setup?
      
      - None
    - Issue process?
      
      - None
    - Verifier presentation request?
      
      - Creates two values – message and blinder generators - passed in the presentation request applied to a specific claim
      - Always use the same generators
    - Holder presentation process
      
      - Same as verifiable encryption – no decryption key
    - Verifier gets a consistent value from the holder
- Question – call home for revocation
  
  - Does the issuer know who is calling home? No... ![(smile)](images/icons/emoticons/smile.png)
  - Trade-off – massive list, holder tells verifier which entry they are
  - Mitigate:
    
    - Get the latest state somehow.
    - Anonymous Revocation Handle Update - Call home – get me an update so I can proof a proof.
      
      - I have a credential.
      - Verifier to holder: Prove revoked as of this accumulator.
      - Holder to issuer: Give me an up to date witness for the accumulator – issuer does not know who is asking.
        
        - Holder – passes signature proof (I have a valid credential) – optional, accumulator, N shares of their element.
          
          - Issuer returns shares of the result.
        - If revoked – not useful.
        - If never issued a credential – not useful.
- Claim Schema format
  
  - Default encoding if no other information?  E.g. if just the name is given.
    
    - Dynamic encoding using AnonCreds v1 rules?  Notably: "If integer or integerString, then integer, else stringified and hashed"
  - link\_secret automatically added as in AnonCreds v1?
  - Externalized set for list of set members
  - Date as ISO Date and encoded as Integer Date
  - DateTime as ISO Date and encoded as Unix Time
  - Research – what can be derived from JSON-LD information?
- Open Discussion

## To Dos:

## Action items

- Links to be referenced in the spec and used where needed:
  
  - From Will Abramson : [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&amp;rep=rep1&amp;type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.186.5994&rep=rep1&type=pdf)
  - From Will Abramson : [https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md](https://github.com/hyperledger/indy-hipe/blob/c761c583b1e01c1e9d3ceda2b03b35336fdc8cc1/text/anoncreds-protocol/README.md)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
