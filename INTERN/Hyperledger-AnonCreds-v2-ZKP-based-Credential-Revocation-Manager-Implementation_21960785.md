1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2024 Projects](2024-Projects_21954934.html)

# Hyperledger Mentorship Program : Hyperledger AnonCreds v2 ZKP-based Credential Revocation Manager Implementation

Created by Stephen Curran, last modified by Min Yu on Jun 07, 2024

el

**Project Title**Hyperledger AnonCreds v2 ZKP-based Credential Revocation Manager Implementation**Status**

IN PROGRESS

**Primary Focus**

CODING    

# Description

Hyperledger AnonCreds v2 takes the privacy-preserving features of AnonCreds v1 Verifiable Credentials to a new level. AnonCreds v2 adds support for newer, mature cryptosuites (including BBS+ Signatures), and for a number of important Zero Knowledge Proofs (ZKP) that enable an even better balance between verifiability and privacy. AnonCreds v2 also adds a crucial new, highly-scaled approach to ZKP-based credential revocation – a crucial element of almost all verifiable credential ecosystems. Called ALLOSAUR, this new scheme allows a single revocation registry to be created by an verifiable credential issuer that scales to support millions of credentials in a fast, low-data manner. Instead of sharing millions of credential revocation statuses (revoked or not), the scheme relies on the transfer of just a handful of integers between participants, enabling secure revocation without a verifiable credential holder from having to share a correlatable identifer for themself to the verifier. ALLOSAUR requires the creation of a new component in the verifiable credential ecosystem, the revocation manager, which is the goal of this Hyperledger Mentorship – to implement a scalable ALLOSAUR revocation manager.  The revocation manager is a (relatively) simple service that implements two HTTP interfaces – an authorized interface to one or more AnonCreds issuers, and an open interface for receiving "update my data" requests from verifiable credential holders. The cryptography implemented by the revocation manager is interesting – employing both data sharding (processing a data split into segments such that the output can later be combined) and cryptographic accumulator processing. The implementation will at least be partially in Rust, with flexibility on the choice of languages/frameworks for the web service. The following shows the various the participants in a verifiable credential ecosystem, including the Revocation Manager to be added through this project.

![](https://www.plantuml.com/plantuml/img/RL7DJiCm3BxtAQnnMQNs1Gf20eG6qa1J4N399JHk6z4v8qdBw-CstHe6DylvVXqo2k7HkHujI0VQkOJ6rOFfL5YrqnIsgn87Kqcl3GbwaYGRjAiHP760YwrkMh-nY3IZtz3gMi-GuIIoHNNa3Sec2Pj2VZqR5I6De7LWouyEuSwYGl9QTfaWM4B0VOTxVaWdZQkSLJX9CUAbPmr6bjW86YVVMtA5e9kgwlTz9xsnPwnHzpCsSvnYTd1ff7BvLoNl3op3TGfuFQZ9F8PmUJRgiFPv06tG_uU8ph2pwDWuz2pngqV7b6_jMuXulxl1iw4yEi_E6bCBkfKE5Ipdok1TUqB-ws0MtI24Fxul_U6bbLQjNPh5xkcP_KmxWPCV)

# Learning Objectives

- Develop a sophisticated (yet straight-forward), high-performance web service for privacy-preserving verifiable credential ecosystems.
- Learn about and use state of the art zero knowledge proof (ZKP) cryptography.
- Use and evolve Rust software that implements the cryptographic core of the Revocation Manager component.
- Develop a performant web service with an embedded cryptographic component.
- Work with cryptographers and experts in verifiable credentials and the broader field of digital trust.
- Understand the processes around delivering an open source web component for broad deployment.

# Expected Outcome and Deliverables

- The creation of the AnonCreds v2 Revocation Manager component.
- A release pipeline for the publication of the Revocation Manager artifacts.
- The creation of automated unit and integration tests for the component.
- Documentation about how to run, test and deploy the Revocation Service service.
- Opportunities to collaborate with project maintainers, and to present progress and results to the Hyperledger AnonCreds community.

# Relation to Hyperledger and Impact on the community

This project focuses mainly on Hyperledger AnonCreds, and to a lesser extent on Hyperledger Aries, which uses AnonCreds, and Hyperledger Indy, a ledger on which AnonCreds objects may be stored. Enabling a highly-scalable, ZKP-based revocation scheme will have a significant impact on the ability to deploy privacy-preserving verifiable credentials in "jurisdication-level" use cases, such as in national identity systems, education credential ecosystems, and the other million/billion credential ecosystems.

# Recommended Skills

The mentee should be comfortable with, and interested in, cryptography, particularly zero knowledge proofs, and in their application in web technologies. As well, the mentee should be comfortable in using GitHub for development, at least one web framework, and in implementing unit and integration tests using containers and GitHub actions. An interest in learning about cryptography, zero-knowledge proofs, and Rust is desirable.

# Mentor(s) Names and Contact Info

Stephen Curran, [swcurran@cloudcompass.ca](mailto:swcurran@cloudcompass.ca), Cloud Compass Computing Inc. (Hyperledger AnonCreds Maintainer)

Mike Lodder, [redmike7@gmail.com](mailto:redmike7@gmail.com) (Hyperledger AnonCreds Maintainer)

# Additional Information

The following are links to the related topics:

- The [Hyperledger AnonCreds](https://www.hyperledger.org/use/anoncreds) project
- The [AnonCreds Specification, Version 1.0](https://hyperledger.github.io/anoncreds-spec/), [source](https://github.com/hyperledger/anoncreds-spec).
- The [AnonCreds 1.0 implementation in Rust](https://github.com/hyperledger/anoncreds-rs).
- The [AnonCreds 2.0 implementation in Rust](https://github.com/hyperledger/anoncreds-v2-rs).
- The [ALLOSAUR](https://eprint.iacr.org/2022/1362) paper – very long and complicated!
- A presentation about [ALLOSAUR revocation in AnonCreds](https://docs.google.com/presentation/d/1b6h6ZNgat3-4TZomA2h09QUnqU3jOWkLIf1zu6MkoiM/edit?usp=sharing)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
