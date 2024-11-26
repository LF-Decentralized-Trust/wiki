1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q4 Hyperledger Avalon Project Update

Created by Yevgeniy Y Yarmosh, last modified by Nathan George on Mar 31, 2020

Prepared by Eugene (Yevgeniy) Yarmosh

# Project

Hyperledger Avalon

Project Health

The Avalon project has grown well in its first quarter.  We are establishing community processes that include regular (every other week) meetings, JIRA, etc. We have completed direct model (JRPC), developed hello-world tutorial, improved project documentation, and added more use cases. Initial integration with Ethereum blockchain was completed. The focus is on integrating Hyperledger Fabric and porting Ethereum JAVA connector to PYTHON to improve code consistency. The team is evaluating options for separating key management from work order processing and on scalable worker orchestration. 

# Questions/Issues for the TSC

There are no issues for the TSC at this time.

# Releases

October 2019 - Release 0.4. This release was focused on baseline end-to-end functionality for direct model.

The plan for minor releases (0.5, 0.6, 0.7, ...) to be done roughly quarterly in 2020.

The team doesn't yet plan patch releases (e.g. 0.4.1, 0.4.2), but it may change in the near future to better capture intermediate progress.    

# Overall Activity in the Past Quarter

Hyperledger Avalon transitioned from Hyperledger Lab - Trusted Compute Framework (TCF).

- Completed core implementation for the direct model (via JSON RPC) that also fully reusable for integration with blockchain
- Added initial Ethereum support (Solidity smart contracts and JAVA connector)
- Started integration of Hyperledger Fabric
- Implemented hello-world tutorial and several end-to-end examples
- Updated project documentation
- Implemented baseline inside-out API
- Started evaluation of Kubernetes as a foundation for scalable worker execution orchestration
- Evaluated Graphene as a candidate for integration with Avalon
- Established CI/CD build infrastructure
- Established a bi-weekly contributor call

Avalon team participated in the following activities:

- Presented the Hyperledger meet-up at Ethereum Devcon V in Japan
- Presented Avalon at Architecture WG
- Presented at Hyperledger meet-up in Bangalore, India
- Submitted a workshop proposal that was approved to present at the Hyperledger Global Forum

# Current Plans

The Avalon project has several upcoming priorities:

- 0.5 Release, scheduled for March 2020. The focus of this release is on:
  
  - Integrate Avalon with Hyperledger Fabric
  - Port Ethereum connector from JAVA to python
  - Add a security layer to inside-out API
  - Implementation policy based worker encryption key
  - Define of architecture for separation of key management from workload processing
  - Define architecture for the scalable orchestration layer
- The Avalon team is also focusing on improving project documentation that is relatively thin at this time. Immediate goals are to build up content in the project WiKi, document Avalon architecture (current and upcoming plans), and simplify/streamline overall project structure and build process
- Another important area is continuing engagement with its community to grow the diversity of its maintainer and contributor base. Primary mechanisms are to grow attendance for its regular contributor calls and present Avalon to developers through Hyperledger (Global Forum, meet-ups) and other industry venues.

# Maintainer Diversity

Since Avalon is a new Hyperledger project, its maintainers is the same as it was when the project was hosted as TCF Hyperledger Lab. Based on the activity going within the Avalon community and our current plans we anticipate that the maintainers list will be extended by release 0.5 after more community members make substantial contributions to the project. 

# Contributor Diversity

Avalon includes active contributors from five organizations. The Avalon Developer Forum calls we established every other week during last quarter have been well attended by members from different organizations. We are reaching out to all original Avalon project sponsors and we also see members joining the community from organizations that have not been on the original project sponsor list.

We will present Avalon workshop at the Hyperledger Global Forum in the spring of 2020 to attract additional contributors to the project. We also plan to utilize EEA,  Hyperledger meet-ups, and other industry venues to bring more contributes to the project. 

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
