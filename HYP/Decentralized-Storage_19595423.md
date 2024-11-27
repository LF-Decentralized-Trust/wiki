1. [Hyperledger](index.html)
2. [Working Groups](Working-Groups_19595403.html)
3. [Working Group Proposals](Working-Group-Proposals_19595279.html)

# Hyperledger : Decentralized Storage

Created by Saswata Basu, last modified on Aug 15, 2019

# Introduction

A decentralized storage provides a single source of truth for data, with unparalleled privacy, security, and transparency.

There are three relevant data trends. One, data is expected to grow from 33 ZB (zettabytes) today to 175 ZB in 5 years. Two, data breaches are a growing problem with $150M+ liability issues. Three, the cloud needs to move to the edge data centers for performance and availability, driven by IoT applications, multi-player gaming, autonomous vehicles, and content streaming. Decentralization accelerates this change and adoption, as it lowers deployment, management, and scale-out cost while providing better security, performance, and availability. 

# Scope

The scope is to define concepts regarding decentralized storage and to produce material to describe the various aspects and meanings, trying to come up to standards or good practices. The audience for decentralized storage is large and spans from researchers, developers, cloud providers, and storage system vendors in several industry verticals such as supply chain, healthcare, government, financial institutions, real estate, insurance providers,  etc

Some research topics and separation of interest are:

- Models of and mechanism for providing single source of truth for smart contract execution
- Storage protocol specifics such as:

  - Generating unbiased random challenges to verify storage of data

  - Verification of data

  - Execution determinism, and sources of non-determinism in existing languages

  - Mechanism to transact with USD or fiat currency to storage providers and clients

  - Cost models for metering challenges and verification

  - Paradigms for storage provider selection - e.g. based on region, challenge response time, price, public reputation via oracle 

  - Parallelism of execution, state independence 

- Formal guarantees on outputs of storage smart contracts
- Storage smart contract packaging, code reuse, and dependency auditing
- Storage smart contracts as representatives of obligations and fulfillment (i.e. 'SLA - service level agreement')

  - What properties should storage smart contracts with 'SLA' have?

  - At what scale to smart contracts best contribute to certainty and execution of agreement?

  - What relationship do legal storage smart contracts have to models of computation?

- Models of and mechanism for providing single source of truth for decentralized storage document
- Data structures and state

  - Verifiable and authenticated data structures - e.g. Merkle paths, log-backed maps,

  - How best to expose through storage smart contract languages/libraries

  - Sharing state back-ends across execution engines

  - Conflict-free and additive data structures

- Privacy

  - Multi-party secure share of data

  - Proxy re-encryption

  - Zero knowledge

# Work Products

The anticipated initial work products will include (but is not limited to):

- White Paper about storage smart contracts and the respected aspects concerning their development, deployment and usage
- Taxonomy of storage smart contracts
- Find practical ways to connect stuff 'out there' with things we could use within implementations
- Performance of storage smart contracts across the different HL DLT frameworks
- Identifying use cases, case studies
- Survey and continuously keep a record for the state of the art and academic content
- Produce 'Requests To Build' that could feed into feature planning on the different Hyperledger frameworks
- Exploring security, privacy, legal boundaries
- Proposing solutions to the problems identified
- Identifying conferences or other opportunities to connect face to face

# Collaborators (other groups)

This working group will collaborate with other Hyperledger working groups, the TSC, Linux Foundation staff, and the project maintainers. Especially the following Working Groups and their subgroups will be of great importance in achieving the anticipated results.

### Workgroups

- [Architecture Working Group](https://lf-hyperledger.atlassian.net/wiki/display/AWG/)
- [Identity Working Group](https://lf-hyperledger.atlassian.net/wiki/display/IWG/)
  
- [Performance and Scale Working Group](https://wiki.hyperledger.org/display/PWG)

### SIGs

- [Healthcare SIG](https://lf-hyperledger.atlassian.net/wiki/display/HCSIG/)
- [Public Sector SIG](https://lf-hyperledger.atlassian.net/wiki/display/PSSIG/)
- [Social Impact SIG](https://lf-hyperledger.atlassian.net/wiki/display/SISIG/)
- [Trade Finance SIG](https://lf-hyperledger.atlassian.net/wiki/display/TFSIG/)
- [Supply Chain SIG](https://lf-hyperledger.atlassian.net/wiki/display/SCSIG/)
- [Capital Markets SIG](https://lf-hyperledger.atlassian.net/wiki/display/CMSIG/)

# Interested Parties

The following individuals have already expressed an interest in joining this working group, and we hope they will become contributors over the first year:

NameCompanyEmail Address

# Proposed Chair

The following individual has volunteered to serve as the initial chair for the working group:

I, Saswata Basu, am volunteering to run this group initially, unless somebody else with interest in the group would like to volunteer.

# Reviewed by

- Arnaud Le Hors
- Baohua Yang
- Binh Nguyen
- Christopher Ferris
- Dan Middleton
- Hart Montgomery
- Kelly Olson
- Mark Wagner
- Mic Bowman
- Nathan George
- Silas Davis

Document generated by Confluence on Nov 26, 2024 16:46

[Atlassian](http://www.atlassian.com/)
