1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q1 Hyperledger Avalon Project Update

Created by Yevgeniy Y Yarmosh, last modified by Gari Singh on Apr 27, 2020

Prepared by Eugene (Yevgeniy) Yarmosh

# Project

Hyperledger Avalon

Project Health

The Avalon team successfully accomplished its plans for this quarter and is on track to release 0.5 version in March. This release supports proxy model and integrates with Ethereum (Hyperledger Besu) and Hyperledger Fabric blockchains. It also includes improved Inside-Out API implementation, encryption key update logic, improved documentation and tutorials. The team also completed several prototypes focused on integration with K8S and made a progress refining Avalon architecture. The Avalon team actively participated in Hyperledger Global Forum. Upcoming release 0.6 will focus on adding enclave pools, key management isolation from the transaction execution, and an initial K8S integration. The team continues to improve its processes and building up community.

# Questions/Issues for the TSC

There are no issues for the TSC at this time.

# Releases

March 2020 - Release 0.5. This release was focused on proxy model implementation and integration of Hyperledger Besu and Hyperledger Fabric blockchains.

April 2020 – a minor release 0.5.1 is planned to address few bugs and missing corner cases.

The plan for releases (0.6, 0.7, ...) to be done roughly quarterly in 2020.

# Overall Activity in the Past Quarter

Avalon team was focused on building proxy model functionality and exploratory activities related to future releases focused on scalability and key management isolation.

During work on 0.5 version released in March the Avalon team

- Integrated Hyperledger Fabric in the Avalon proxy model
- Integrated Hyperledger Besu in the Avalon proxy model
- Added a security layer to the inside-out API
- Implemented policy-based worker encryption key
- Prototyped K8S as a foundation for scalable worker execution orchestration
- Evaluated Occlum as a candidate for integration with Avalon
- Added new use cases, e.g. Cold Chain presented at HGF (by WiPro)
- Updated tutorial to include the proxy model with Fabric and Besu
- Updated tutorial to include the inside-out API
- Defined of architecture for separation of key management from workload processing
- Defined architecture for the scalable orchestration layer
- Improved project documentation and Wiki based on the feedback from the last quarter

Avalon team participated in the following activities:

- Avalon Workshop at Hyperledger Global Forum
- Avalon project kiosk and Confidential Compute presentations at Hyperledger Global Forum
- Trusted Compute precompiled smart contract proposal is accepted by EEA to become a part of Ethereum Enterprise Client spec
- Avalon presentation at Hyperledger Bootcamp in Moscow
- Avalon tech talk in Hyperledger India chapter National e-Meetup

# Current Plans

The Avalon plans include following releases

- 6 – worker pools with key management isolation
- 7 – elastic scalability and broader runtime support
- 8 – performance optimization and Avalon SDK

Next release 0.6 will focus on

- Initial implementation of scalable worker pools
- Key management isolation from the workorder execution
- Baseline work order scheduler with pluggable orchestration adaptors
- Baseline Kubernetes engine integration (without elastic compute)
- Extending SGX attestation model to support 3rd party attestation (aka DCAP)
- Prototypes for integration of high-level (e.g. LibOS based) runtimes
- Adding attested oracles end-to-end use case (to be contributed by Chainlink)
- Updating and refactoring CI
- Refining Avalon Architecture with focus on scalability and multi-tenancy

The team plans to start a more efficient use of JIRA for the project management and will continue to build up WiKi content. In addition to Avalon Developer Forum calls (every other weeks) the plan includes starting a new series of Avalon Architecture Forum calls.

Grow Avalon community and increasing the diversity of its maintainer and contributor base continues to be a priority. Since face-to-face meetups and other venues are limited due to coronavirus, emphasis will be made on publishing technical blogs, user case studies, and video tutorials at Hyperledger, EEA, and other suitable on-line venues.

# Maintainer Diversity

Avalon maintainers has not changed during this quarter, but we see great code contributions by several team members that constitute Avalon maintainers candidate list. Based on the recent activity and our current plans we anticipate that the Avalon maintainers list will be extended within couple release cycles.

# Contributor Diversity

Avalon code contributions come from multiple companies – Intel, IBM, iExec, WiPro, Consensys/Kaleido, Santander, Espeo, and (planned for 0.6) Chainlink. Several more companies are considering their contributions for upcoming Avalon releases.  
Avalon Developer Forum calls happens every other week attended by members from different organizations. Additionally, an Architecture Forum is planned to start also every other week.  
Avalon was presented at the Hyperledger Global Forum during Avalon Workshop and other presentations. They generated a significant interest from the broader Hyperledger community that is expected to result in additional Avalon contributors. We plan to continue drive a broader Avalon awareness via EEA, Hyperledger, and other industry venues, this time focusing on on-line options.

# Additional Information

None at this time.

# Reviewed by

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Christopher Ferris](https://lf-hyperledger.atlassian.net/wiki/people/5abb903a8724022aa9070581?ref=confluence)
- [Dan Middleton](https://lf-hyperledger.atlassian.net/wiki/people/712020:2979764a-3998-4ef1-8810-60b799067924?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Swetha Repakula](https://lf-hyperledger.atlassian.net/wiki/people/712020:503b5691-8e92-4d2d-83d3-e9e74d296436?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
