1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)
5. [Document, Review, and Implement Hyperledger AnonCreds ZKP Cryptographic Primitives](Document%2C-Review%2C-and-Implement-Hyperledger-AnonCreds-ZKP-Cryptographic-Primitives_21954891.html)

# Hyperledger Mentorship Program : Project plan - AnonCreds ZKP Cryptographic Primitives

Created by Stephen Curran, last modified on Jun 30, 2023

## **Abstract**

> Taken from the [Mentorship Description](Document%2C-Review%2C-and-Implement-Hyperledger-AnonCreds-ZKP-Cryptographic-Primitives_21954891.html)

Hyperledger AnonCreds includes specifications and implementations of AnonCreds (Anonymous Credentials) Zero-Knowledge Proof (ZKP)-based verifiable credentials. AnonCreds extends the capabilities of “typical” verifiable credentials by including important privacy-preserving features including selective disclosure, ZKP predicates (e.g., ***proving*** I’m older than 21 based on my date of birth without sharing my date of birth), and not revealing any correlatable identifiers in presenting credentials. The version 1.0 specification (based on CL-Signatures as initially implemented in Hyperledger Indy) is near completion, and work has begun on the version 2.0 specification that will retain and extend the privacy-preserving features of AnonCreds v1.0, while improving capabilities, performance, extensibility, and security. An implementation based on the Version 2.0 specification will occur in parallel with the development of the specification.

In this project, the mentee will participate directly in the specification development process.

- For the Version 1.0 specification, the primary task will be to extract the cryptographic primitives from identified sources, confirm alignment with the Rust implementation of AnonCreds, and include the cryptographic primitives in the specification. This is the last step of the specification to make it ready for submission to a standards development organization (SDO).
- The Version 2.0 specification, the task will be similar, but the work will extend the focus as appropriate to implementation of the cryptographic primitives.

## **Mentor and Mentee**

Mentor: Stephen Curran, Mike Lodder

Time zones: Pacific Time, North America, Mountain Time, North America

Discord: swcurran, mikelodder

Mentee: Aritra Bhaduri

Time zone: India Time

Official repository for this project:

- Specification: [https://github.com/hyperledger/anoncreds-spec](https://github.com/hyperledger/anoncreds-spec)
- Implementation: [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
- Published Specification: [https://hyperledger.github.io/anoncreds-spec](https://hyperledger.github.io/anoncreds-spec/)

## **Deliverables**

The primary deliverable is the population of the AnonCreds specification with the cryptographic algorithms used in the four AnonCreds operations (setup, issuance, presentation, and verification), including the impact of revocation on those operations. Based on the time available after that work we may look to have the project also include the AnonCreds V2.0 cryptographic primitives. The Milestones are each of the operations, plus revocation. The approach is defined in the methodology section.

The cryptography primitives should be put inline into the specification. The [BBS+ Signatures IETF Specification](https://www.ietf.org/archive/id/draft-looker-cfrg-bbs-signatures-01.html) uses an approach that should be followed, albeit with Latex where it is helpful.

## **Milestones**

### **Setup:**

- As is done in the BBS+ Signatures IETF Specification, add a "Notations" section to the specification, and populate it as appropriate based on the cryptographic algorithms in the specification.
- Credential Definition generation process (noting the public and private portions) – no revocation.

### **Issuance:**

**NOTE**: In this section there is a lot of back and forth of data elements (e.g. two nonces, three correctness proofs). As the details are added, feel free to adjust the text to make it as easy as possible for the reader to understand the process.

- Terminology:
  
  - Blinding Factor
  - Signature Correctness Proof, Blinded Secret Correctness Proof
- Credential Offer:
  
  - Verify the specification of the Credential Offer key correctness proof and verification of the key correctness proof.
- Credential Request:
  
  - Description of the nonce in the credential request data model.
  - Document how the nonce from the Credential Offer is used.
  - Verify how the blinding link secret is generated.
  - Document the items in the blinded link secret data model and how they are generated.
  - Document the items in the blinded link secret correctness proof data model and how they are generated.
- Issue Credential:
  
  - Document how the nonce from the credential offer is verified in the credential generation.
  - Document how the blinded kink secret correctness proof is verified.
  - Document how the nonce from the credential request is used.
  - Document how the Credential Signature is generated.
  - Document how the Credential Signature Correctness Proof is generated.
- Receiving a Credential
  
  - Document how the nonce from the Credential Request is verified.
  - Document how the Credential Signature Correctness Proof is verified.

### **Presentation:**

**NOTE:** This section needs to be reworked to be more in the style of the rest of the specification, with a description of the process, cryptographic processes invoked, and the data models that result are described. [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) to do that step.

**NOTE**: AFAIK, the AnonCreds library does not include the credential searching, nor does it deal with the wallet, and as part of the rewrite, those items will be removed. The current "Step 5" will update to cover the data passed in to the presentation generation process, how the proofs from a source credential is produced (credential and predicate), how the aggregate proof is generated, and how the data is mapped back into the response to the proof request (e.g. requested\_attr groups, unrevealed\_attrs, self\_attested\_attrs and predicates).

- Document the items in the and generation process for a credential proof.
- Document the items and generation process for a predicate proof.
- Document the Aggregate proof
- Document how the full presentation data model is populated.

### **Verification:**

**NOTE:** This section needs to be reworked to be more in the style of the rest of the specification, with a description of the process, cryptographic processes invoked, and the data models that result are described. [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) to do that step.

- Document how a credential proof is verified.
- Document how a predicate proof is verified
- Document how the aggregate proof is verified.

### **Revocation:**

**NOTE:** Section 10.3 will be re-written to be less opinionated on the format of the RevRegEntry, allowing it to be either a list of deltas or the full state of the RevReg, e.g. a True/False bit for each credential in the registry.

- Setup:
  
  - Document the additional data in the credential definition data models (public and private) with revocation support, including where needed how the data is generated ([Section 7.2.3](https://hyperledger.github.io/anoncreds-spec/#generating-a-credential-definition-with-revocation-support)).
  - Document the data in the Revocation Registry Definition data models (public and private) and how it is generated.
  - Document the Tails File generation process and file format. DONE!
  - Document the data in a Revocation Registry Entry data model, and the generation process of those elements.
- Issuance:
  
  - Describe the revocation part of the Credential data model and how the elements are generated.
- Presentation:
  
  - Describe how the witness is created for the non-revocation proof, given the tails file, accumulator (if needed), and a revocation registry state object.
  - Document the values in the non-revocation proof data model for a source credential and how the values are generated.
- Verification:
  
  - Document how the non-revocation proof is verified.

## **Timeline**

It is extremely difficult to define a timeline for the work to be done on this project, as it will depend on far too many factors that we don't know right now. Instead, we will begin with the assumption that the work will be done in sequence as listed in the Milestones section. We will communicate continuously on Discord and meet every 2nd week to discuss progress and adjust the Milestones. For example, we might change the ordering of the work, add new milestones (such as adding work on AnonCreds v2.0), or drop milestones.

Every second of those meetings will include an "evaluation" of the work completed that is sufficient to meet the needs of the Hyperledger Mentorship Program (to be determined).

## **Methodology**

For each item to be documented, the following approach is suggested.

- Review the source documents and AnonCreds implementation.
- Document a minimum draft of the process as the basis for questions about the process.
- Ask questions about the process in Discord.
  
  - If ever the online back and forth is ineffective, call a meeting. No need to spend time writing back and forth messages about an issue that needs a face-to-face discussion.
- Refine the document and confirm the implementation.
- Identify any information that should be updated in the Terminology and Notations section of the document from the newly documented item.
- Submit a PR to the specification for review.

As we gain experience, feel free to adjust this approach to what works best/most efficient.

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
