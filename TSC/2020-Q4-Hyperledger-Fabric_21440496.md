1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q4 Hyperledger Fabric

Created by David Enyeart, last modified by Gari Singh on Oct 22, 2020

Project Health

Hyperledger Fabric continues to mature, as evidenced by the following observations throughout this report:

- Two LTS releases available
- Project developers are spending a larger percentage of time on maintenance and support than in the past, given the increasing number of production deployments and two LTS releases.
- Lower commit velocity on new features.
- Healthy RFC process with reviews in contributor meetings to drive consensus on new features.
- Increased contributor diversity, driven in part by documentation translation initiative.

The commit rate and mailing list activity are down slightly compared to the same period last year.

The project would benefit from increased maintainer diversity.

# Questions/Issues for the TSC

None.

# Releases

v1.4 and v2.2 are the current LTS releases. Each has patch releases at least quarterly.

- v1.4.8 - July 22, 2020
- v1.4.9 - September 30, 2020
- v2.2.0 - July 9, 2020
- v2.2.1 - September 30, 2020
- v2.3 is planned for November.

# Overall Activity in the Past Quarter

The project was busy maintaining the two LTS releases, given an increasing number of production deployments.

[RFCs merged](https://github.com/hyperledger/fabric-rfcs/tree/master/text):

- Ledger checkpointing
- Channel participation API

[RFCs in review](https://github.com/hyperledger/fabric-rfcs/pulls):

- Fabric website
- Fabric gateway
- WASM for smart contracts
- Fabric private chaincode
- BFT ordering service
- Modular crypto service

In active development:

- Ledger checkpointing
- Channel participation API
- WASM for smart contracts (tech preview released)
- Samples and tutorials revamp
- Production deployment guides
- Documentation translation

Mailing list activity:

**557 messages in Q3 2019** versus **480 messages in Q3 2020**, down 14%. While Chat and Stackoverflow numbers are not available, they are likely slightly down as well.

# Current Plans

The project is working towards a v2.3 release in November. Major features include ledger checkpoint and channel participation management without a system channel.

Ledger checkpoint will allow new peers to join a channel from a checkpointed snapshot of the state database. This reduces the time to join a channel, and reduces the storage size required to maintain a ledger. In the future it will also be possible to prune/archive old blocks to bring the same benefit to existing peers.

The channel participation management feature improves the privacy and scalability of the ordering service since a global 'system channel' will no longer be needed for the creation and management of channels.

The project is shifting from a release cadence of every 3 months to every 4 months. The change is driven by the overall project maturity/stability/velocity, as well as the difficulty for consumers to keep up with a quarterly release cadence.

The other active development items mentioned above for Q2 continue into Q3 as well.

# Maintainer Diversity

No maintainer changes for core fabric project this quarter. 12 of 13 from IBM.

# Contributor Diversity

Year to year comparison, by commit:

- Q3 2019 - 1293 commits. 85% from IBM.
- Q3 2020 - 893 commits. 68% from IBM

Year to year comparison, by contributor:

- Q3 2019 - 85 contributors. 52% from IBM.
- Q3 2020 - 106 contributors. 28% from IBM.

Documentation translation was a driver in the increased contributor diversity.

# Additional Information

Link to the Fabric dashboard [https://lfanalytics.io/projects/hyperledger%2Ffabric/dashboard](https://lfanalytics.io/projects/hyperledger%2Ffabric/dashboard)

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Baohua Yang](https://lf-hyperledger.atlassian.net/wiki/people/557058:17d87dbf-05fe-4c1b-84cf-fd69f7fcbb20?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [María Teresa nieto](https://lf-hyperledger.atlassian.net/wiki/people/5d36fa46af1d920bc99755b6?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
