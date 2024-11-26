1. [Hyperledger AnonCreds](index.html)

# ![Home Page](images/icons/contenttypes/home_page_16.png) Hyperledger AnonCreds : Hyperledger AnonCreds

Created by Ry Jones, last modified on Apr 23, 2024

**Project**

**Status**

[INCUBATION](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Project+Lifecycle#ProjectLifecycle-incubation) [ACTIVE](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Project+Lifecycle#ProjectLifecycle-active)

**CII Badge**

[![](https://img.shields.io/badge/cii%20best%20practices-not%20started-red.svg)](https://bestpractices.coreinfrastructure.org/projects/new)

**Description**AnonCreds (anonymous credentials) are a type of verifiable credential that supports important privacy-preserving capabilities through the use of zero-knowledge proof (ZKP) cryptography. Within the Hyperledger AnonCreds project is a specification for AnonCreds, documentation, implementations and tests.

# Key Characteristics

AnonCreds ZKP verifiable credentials provide capabilities that many see as important for digital identity use cases in particular, and verifiable data in general. These features include:

- A full implementation of the Layer 3 verifiable credential “Trust Triangle” of the [Trust over IP Model](https://trustoverip.org/wp-content/toip-model/).
- Complete flows for issuing verifiable credentials (Issuer to Holder), and requesting, generating and verifying presentations of verifiable claims (Holder to Verifier).
- Fully defined data models for all of the objects in the flows, including verifiable credentials, presentation requests and presentations sourced from multiple credentials.
- Fully defined applications of cryptographic primitives.
- The use of Zero Knowledge Proofs (ZKPs) in the verifiable presentation process to enhance the privacy protections available to the holder in presenting data to verifiers, including:
  
  - Blinding issuer signatures to prevent correlation based on those signatures.
  - The use of unrevealed identifiers for holder binding to prevent correlation based on such identifiers.
  - The use of predicate proofs to reduce the sharing of PII and potentially correlating data, especially dates (birth, credential issuance/expiry, etc.).
  - A revocation scheme that proves a presentation is based on credentials that have not been revoked by the issuers without revealing correlatable revocation identifiers.

AnonCreds was initially part of the [Hyperledger Indy](https://lf-hyperledger.atlassian.net/wiki/display/indy/) project, but has always been largely agnostic to the ledger/data store where AnonCreds objects are stored. The shift of AnonCreds from Indy to being an independent project reflects that reality – that AnonCreds can use any number of platform for the storage of materials needed for issuing, holding, proving and verifying AnonCreds verifiable credentials.

# Specification

The current version working draft AnonCreds specification can be found [here](https://hyperledger.github.io/anoncreds-spec/), along with the related [AnonCreds Methods Registry](https://hyperledger.github.io/anoncreds-methods-registry/). The AnonCreds Specification Working Group manages the specification and registry in these GitHub repositories: [AnonCreds Specification](https://github.com/hyperledger/anoncreds-spec), [AnonCreds Methods Registry](https://github.com/hyperledger/anoncreds-methods-registry).

# Implementations

There is a currently one [Rust implementation of AnonCreds](https://github.com/hyperledger/anoncreds-rs) in the project, with wrappers for use in other languages.

# Communication

## Mailing List

Information about the mailing list for Hyperledger AnonCreds is available here: [https://lists.hyperledger.org/g/anoncreds](https://lists.hyperledger.org/g/anoncreds), including guidance on subscribing to the list and access to the mailing list archives.

## Discord Chat (for questions and ephemeral discussions)

We encourage anyone interested in Hyperledger AnonCreds to join the Hyperledger Discord (here's an [invitation to join](https://discord.gg/hyperledger)), and go to the [main AnonCreds channel](https://discord.com/channels/905194001349627914/1035263835449331793). You'll find a friendly community and lots of people happy to answer your questions!

# Meetings

- AnonCreds Specification Working Group – [Meetings](20291486.html) – Weekly on Mondays 7:00 Pacific / 16:00 Central Europe.
- AnonCreds Rust Working Group – [Meetings](/wiki/pages/createpage.action?spaceKey=ANONCREDS&title=Meetings%3A%20AnonCreds%20Rust%20Working%20Group&linkCreation=true&fromPageId=20283406) – Called when needed by Developers usually within or after the AnonCreds Specification Working Group meeting.

# History

Hyperledger AnonCreds was accepted as project at the Hyperledger Foundation in October, 2022. However, AnonCreds within Hyperledger dates back to the the start of the Hyperledger Indy project in 2017. The motivation in taking AnonCreds out of the Indy project was to simplify the technology for use beyond Indy, enabling its use with any public data storage mechanism—making AnonCreds “ledger-agnostic.” Any Verifiable Data Registry (VDR) that allows an issuer to publish the necessary objects such that holders and verifiers can access (resolve) those objects, supports AnonCreds. That definitely includes Indy (of course!), but that also allows others to take advantage of the extremely important privacy-protecting capabilities of AnonCreds independent of an Indy ledger implementation.

The history leading to AnonCreds goes back much further than Indy, tracing back (at least) to pioneering “[blind signatures](https://en.wikipedia.org/wiki/Blind_signature)” work published by famed “[ecash](https://en.wikipedia.org/wiki/Ecash)” cryptographer [David Chaum](https://en.wikipedia.org/wiki/David_Chaum) in 1983. Jan Camenisch and Anna Lysyanskaya (the “CL” of “[CL-Signatures](https://en.wikipedia.org/wiki/Signatures_with_efficient_protocols)” in AnonCreds) published their academic papers on the underlying algorithms in AnonCreds starting in 2001, taking ZKP capabilities from ideas to reality. Between then and the 2016 creation of Indy, there was at least one other full implementation of the CL-Signatures cryptography in an IBM product called [IDMixer](https://www.zurich.ibm.com/pdf/csc/Identity_Mixer_Nov_2015.pdf). And in 2022, after 5+ years as a key component of Indy, AnonCreds was accepted as standalone project at Hyperledger, available for use in conjunction with Indy and with many other types of ledgers, blockchains and even centralized databases or file systems.

## Recent space activity

- [![](null/aa-avatar/557058:d676f135-ecd6-465b-b7eb-f87976bf4569 "557058:d676f135-ecd6-465b-b7eb-f87976bf4569")](null/display/~557058%3Ad676f135-ecd6-465b-b7eb-f87976bf4569)
  
  - [Stephen Curran](null/display/~557058%3Ad676f135-ecd6-465b-b7eb-f87976bf4569)
  - [2024-11-11 AnonCreds Working Group Meeting](2024-11-11-AnonCreds-Working-Group-Meeting_50331649.html "data-linked-resource-id=") contributed Nov 11, 2024
  - [2024-10-28 AnonCreds Working Group Meeting -- CANCELLED for IIW](2024-10-28-AnonCreds-Working-Group-Meeting----CANCELLED-for-IIW_39321601.html "data-linked-resource-id=") contributed Oct 24, 2024
  - [2024-10-14 AnonCreds Working Group Meeting](2024-10-14-AnonCreds-Working-Group-Meeting_29458433.html "data-linked-resource-id=") contributed Oct 14, 2024
  - [2024-09-23 AnonCreds Working Group Meeting](2024-09-23-AnonCreds-Working-Group-Meeting_20293431.html "data-linked-resource-id=") contributed Sep 23, 2024
  - [2024-09-09 AnonCreds Working Group Meeting](2024-09-09-AnonCreds-Working-Group-Meeting_20293443.html "data-linked-resource-id=") contributed Sep 09, 2024

[Show More](/wiki/plugins/recently-updated/changes.action?theme=social&pageSize=5&startIndex=5&searchToken=1&spaceKeys=ANONCREDS&contentType=page%2C%20comment%2C%20blogpost&cursor=_f_NQ%3D%3D_sa_WzE3MjU4OTUzOTAwMDAsIlx0MjAyOTM0NDMgb1o1UF1BUD5nJ1peYFxcV21nb3RXIGNwIl0%3D) ![Please wait](images/icons/wait.gif)

## Space contributors

- [Stephen Curran](/wiki/display/~557058%3Ad676f135-ecd6-465b-b7eb-f87976bf4569) (14 days ago)

## Attachments:

![](images/icons/bullet_blue.gif) [hl\_anoncreds\_colour.png](attachments/20283406/20295040.png) (image/png)  
![](images/icons/bullet_blue.gif) [hl\_anoncreds\_colour\_small.png](attachments/20283406/20295042.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Anon\_Creds.png](attachments/20283406/20295296.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Anon\_Creds.svg](attachments/20283406/20295298.svg) (image/svg+xml)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
