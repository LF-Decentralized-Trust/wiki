1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : An object-key-value mapper for Hyperledger Fabric

Created by Imre Kocsis, last modified by Min Yu on Dec 18, 2023

**Project Title**

**An object-key-value mapper for Hyperledger Fabric**

**Status**

COMPLETED

**Primary Focus**

CODING   

# Description

In Hyperledger Fabric, there can be a significant mismatch between the simple key-value ledger storage abstraction and the data representation style used for developing chaincode – i.e., Java has classes and objects, not keys and values. Currently, there aren’t really good tools for facilitating the “object-key-value mapping” (at least anything approaching classic Object-Relational Mapping – ORM). This not only complicates chaincode development, but a less than systematic approach with the mapping can lead to performance problems (through logically unnecessary MVCC conflict transaction invalidations). Additionally, an explicit object-oriented ledger data model would enable imposing data-centric constraints on the ledger content, either for runtime checking or development time verification and validation.

The goal of the mentorship is to design and implement an object-key-value mapper with the following functionality:

- Generating key-value storage models from UML ledger data models
- Application of storage strategies during the mapping (as we explored in the report referenced below)
- Generating a chaincode-internal Java data access/persistence layer, “parameterized” by the storage model
- Demonstration on a representative example (e.g., our earlier work on faithfully implementing TPC-C to Fabric)
- (If we have time): declaring OCL (Object Constraint Language) constraints on the models and enforcing them in the data access layer

# Additional Information

A report exploring key related problems on the storage model side: [https://tdk.bme.hu/VIK/DownloadPaper/Alkalmazasi-szintu-ateresztokepesseg](https://tdk.bme.hu/VIK/DownloadPaper/Alkalmazasi-szintu-ateresztokepesseg)

As a motivating example, our ACM SAC DAPP 2022 paper on TPC-C over Fabric: [https://arxiv.org/pdf/2112.11277.pdf](https://arxiv.org/pdf/2112.11277.pdf)

The Wikipedia article on ORM: [https://en.wikipedia.org/wiki/Object%E2%80%93relational\_mapping](https://en.wikipedia.org/wiki/Object%E2%80%93relational_mapping)

# Learning Objectives

- Mastering the open-source workflow
  
  - Managing issues, pull requests, development branches, and repository content
- Being part of an open community, navigating and utilizing different forums
- Working in a team
- Covering a broad spectrum of software development skills
  
  - Conducting unsupervised research for state-of-the-art solutions
  - Designing/implementing functionally rich, testable, maintainable software components
  - Introduction to model-driven software engineering approaches
  - Documentation and presentation skills
    
    - Developer documentation
    - User documentation
    - To-the-point, coherent presentation

# Expected Outcome

1. Survey existing (including DLT-independent) ORM solutions
2. Define a methodology for translating data models to a key-value store-compatible scheme
3. Explore/identify various possible strategies for storing entities on the ledger
4. Implement the workflow for generating data access layer for Java chaincodes based on the input models

# Relation to Hyperledger

The project aims to enhance the chaincode development experience for the Hyperledger Fabric platform.

# Mentee Skills

## Education Level

At least an ongoing M.Sc. study in software engineering is recommended.

## Technical Skills

Required skills:

- Basic understanding of version control and git
- Some experience with Java
- Intermediate verbal and writing skills in English
- High-level understanding of Hyperledger Fabric consensus and chaincode development

Nice-to-have skills (the mentee can learn these during the internship):

- Advanced git usage (upstream repositories, branching, rebasing, etc)
- Familiarity with Visual Studio Code or similar IDE
- Experience in software modeling approaches
- Writing documentation in markdown
- Capability for unsupervised learning

# Mentee Open Source Contribution Experience

Show us a code base (preferably on GitHub) you created/had a major role in creating and which you are proud of. If that's not applicable, our plan is to assign some programming tasks during the selection interview for such candidates.

# Future plans

- The project results can significantly lower the entry barrier for chaincode development, independently of the use case. Thus it would be highly beneficial for the community, for example, in the form of a hl-lab project after the mentorship.
- Moreover, the project targets the Java language, but it can be extended later to support the other chaincode development languages.
- Also, such functionality could be integrated into IDEs (such as VS Code) to support rapid chaincode prototyping.

# Mentor(s) Names and Contact Info

[Attila Klenik](https://lf-hyperledger.atlassian.net/wiki/people/712020:4b6a8d7d-e65a-471e-a60d-e945d09147e2?ref=confluence), research fellow, [attila.klenik@vik.bme.hu](mailto:attila.klenik@vik.bme.hu), Budapest University of Technology and Economics, Dept. of Measurement and Inf. Systems, Critical Systems Research Group (ftsrg)

[Imre Kocsis](https://lf-hyperledger.atlassian.net/wiki/people/5ab966218835f42a650a01ba?ref=confluence), assistant professor, [kocsis.imre@vik.bme.hu](mailto:kocsis.imre@vik.bme.hu), Budapest University of Technology and Economics, Dept. of Measurement and Inf. Systems, Critical Systems Research Group (ftsrg)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
