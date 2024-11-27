1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : Document, Review, and Implement Hyperledger AnonCreds ZKP Cryptographic Primitives

Created by Stephen Curran, last modified by Min Yu on Dec 18, 2023

**Project Title**Document, Review, and Implement Hyperledger AnonCreds ZKP Cryptographic Primitives**Status**

COMPLETED

**Primary Focus**

DOCUMENTATIONCODING    

# Description

Hyperledger AnonCreds includes specifications and implementations of AnonCreds (Anonymous Credentials) Zero-Knowledge Proof (ZKP)-based verifiable credentials. AnonCreds extends the capabilities of “typical” verifiable credentials by including important privacy-preserving features including selective disclosure, ZKP predicates (e.g., ***proving*** I’m older than 21 based on my date of birth without sharing my date of birth), and not revealing any correlatable identifiers in presenting credentials. The version 1.0 specification (based on CL-Signatures as initially implemented in Hyperledger Indy) is near completion, and work has begun on the version 2.0 specification that will retain and extend the privacy-preserving features of AnonCreds v1.0, while improving capabilities, performance, extensibility, and security. An implementation based on the Version 2.0 specification will occur in parallel with the development of the specification.

In this project, the mentee will participate directly in the specification development process.

- For the Version 1.0 specification, the primary task will be to extract the cryptographic primitives from identified sources, confirm alignment with the Rust implementation of AnonCreds, and include the cryptographic primitives in the specification. This is the last step of the specification to make it ready for submission to a standards development organization (SDO).
- The Version 2.0 specification, the task will be similar, but the work will extend the focus as appropriate to implementation of the cryptographic primitives.

# Additional Information

The following are links to the related topics:

- The [Hyperledger AnonCreds](https://www.hyperledger.org/use/anoncreds) project
- The [CL Signatures](https://github.com/hyperledger/anoncreds-clsignatures-rs) implementation project (cryptographic library used in AnonCreds).
- The [AnonCreds Specification, Version 1.0](https://hyperledger.github.io/anoncreds-spec/), [source](https://github.com/hyperledger/anoncreds-spec).
- The [AnonCreds 1.0 implementation in Rust](https://github.com/hyperledger/anoncreds-rs).
- An [AnonCreds Implementation Paper](https://github.com/hyperledger/anoncreds-spec/blob/main/spec/ursaAnonCreds.pdf), with cryptographic primitives documented.
- The [original CL Signatures](https://eprint.iacr.org/2001/019.pdf) paper.
- [Community Specification License 1.0](https://github.com/hyperledger/anoncreds-spec/blob/main/1._Community_Specification_License-v1.md) – the specification equivalent to an Open Source license.
- An example of a [pull request to the v1.0 specification](https://github.com/hyperledger/anoncreds-spec/pull/144) to add a cryptographic primitive.

# Learning Objectives

The objectives for this mentorship include the following:

- Gain experience in applied cryptography – taking academic cryptographic work and making it useful in the “real world."
- Become an expert in a very hot topic in cryptography – zero-knowledge proofs.
- Understand the AnonCreds cryptographic primitives sufficiently to document and review implementations, and as time and interest permits, develop code for select primitives.
- Collaborate on the development of an open specification using the tools and processes of a mature open source community.
- Gain experience in GitHub, Rust, Markdown, Latex and working in an open source community.

# Expected Outcome

The expected outcomes for this mentorship include the following:

- The completed AnonCreds v1.0 specification, with key contributions from the mentee documenting the cryptographic primitives used in the current AnonCreds implementation.
- Confirmation that the AnonCreds implementation aligns with the AnonCreds specification, and issued raised when differences are found.
- Contributions to the development of the AnonCreds v2.0 specification, including documenting and, where appropriate, implementing cryptographic primitives in Rust.

Relation to Hyperledger 

This project will focus mainly on Hyperledger AnonCreds, and to a lesser extent on Hyperledger Aries, which uses AnonCreds, and Hyperledger Indy, a ledger on which AnonCreds objects are stored. All are Hyperledger projects.

# Mentee Skills

The mentee should be comfortable with, and interested in, the mathematics used in cryptography. As well, the mentee should be comfortable in using GitHub for development, markdown, and able to at least read code. An interest in learning about cryptography, zero-knowledge proofs, and Rust is desirable.

# Future plans

By putting Hyperledger AnonCreds Version 1.0 into a specification and ideally, putting it onto a standards track, the path is open for this mature yet novel technology to be used in many applications and frameworks within Hyperledger and beyond. With Version 2.0, we are looking to make the privacy-preserving features of AnonCreds even more powerful – and useful – for a wide variety of applications. The long term goal: a better, safer Internet with trusted, privacy-preserving verifiable data. Important stuff!

# Mentor(s) Names and Contact Info

Stephen Curran, [swcurran@cloudcompass.ca](mailto:swcurran@cloudcompass.ca), Cloud Compass Computing Inc. (Hyperledger AnonCreds Maintainer)

Mike Lodder, [redmike7@gmail.com](mailto:redmike7@gmail.com)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
