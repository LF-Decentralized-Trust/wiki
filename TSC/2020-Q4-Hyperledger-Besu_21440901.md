1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q4 Hyperledger Besu

Created by Danno Ferrin, last modified by Arun .S.M. on Apr 29, 2021

# Project

Hyperledger Besu

Project Health

Hyperledger Besu remains a strong project with a growing community network of contributors. This quarter the team has focused on Ethereum protocol improvements as well as many performance improvements, included in the Hyperledger Besu 20.10.0 Release, which was launched on November 3rd. The team is currently building towards its Q1 2021 release.

# Questions/Issues for the TSC

There are no issues or questions for this reporting period.

# Releases

Hyperledger Besu has completed six bi-weekly releases, including the quarterly major release cycle for 20.10.0 (1.5.5 on 23 Jun, 20.10.0-RC1 on 8 Oct, 20.10.0-RC2 on 21 Oct, 20.10.0 on 3 Nov, 20.10.1 on 17 Nov, 20.10.2 on 2 Dec).

Also, Hyperledger Besu transitioned to the CalVer release versioning taxonomy for our Q4 release.

Some functional improvements include:

**Production-Ready Features:**

- **Privacy:** The most recent set of privacy enhancements include:
- - [Multi Tenancy of Privacy Groups](https://besu.hyperledger.org/en/stable/Concepts/Privacy/Multi-Tenancy/)
- **Performance**
- - Support for OpenTelemetry as a metrics backend (in addition to existing Prometheus support)
  - New library updates for secpk256k1 and altBN precompiles, resulting in 3% to 15% overall performance improvements depending on the chosen network.
  - EVM tool added to the standard set of distribution binaries.
- **Standard Tracing APIs**:
- - Added debug\_standardTraceBlockToFile, debug\_standardTraceBadBlockToFile, and debug\_getBadBlocks to support Ethereum Foundation mainnet chain security efforts.

**Early Access Features:**

- **EIP-1559 Support:** Hyperledger Besu has been one of the clients leading the implementation of EIP-1559, a major upgrade to Ethereum’s transaction fee market. This work accelerated this quarter.
- **Ephemeral Testnet YOLO:** In preparation for the next network upgrade, Berlin, an ephemeral testnet called YOLO was launched.  This network has evolved into YOLOv3 with additional EIPs.

Go to the [Changelog](https://github.com/hyperledger/besu/releases) for more details.

# Overall Activity in the Past Quarter

There have been some significant maintainer contributions from decentralized maintainers

- Ethereum Classic’s Thanos Hard Fork support was contributed by Ed Mack from Chainsafe Systems
- OpenTelementry metrics support was contributed by Antoine Tolume from Splunk.
- DNS Auto-discovery for Ethereum Mainnet and Testnets, by Antoine Tolume from Splunk.
- Next Quarter OpenTracing support is expected to land, also provided by Antoine Tolume from Splunk.

The remainder of the maintainers have been focusing on continuing mainnet compatibility work and adding cross-client support for GoQuorum within the Besu codebase.

# Current Plans

1. The project team remains currently working towards its 21.2.0 Release, scheduled for February or March of 2021. The 21.2 Release is expected to include the following features:
2. 1. Berlin network upgrade (pending Ethereum All Core Devs scheduling)
   2. Bonsai Tries (slipped from 20.10)
   3. QiBFT a cross-client BFT algorithm specified by the EEA.
3. Similar to last quarter, Besu is also continuing to engage with its community and grow the diversity of its maintainer and contributor base.

# Maintainer Diversity

Our maintainer diversity remained fairly consistent from the prior quarter.  We continue to have maintainers from four different organizations. 

The four organizations include:

- ConsenSys Quorum (FKA PegaSys)
- Web3Labs
- Chainsafe
- Splunk

There were no new maintainers added or removed this quarter.

The maintainers breakdown is currently:

- 16% non-ConsenSys (unchanged from last quarter)

# Contributor Diversity

[LF Analytics for Besu from 28 Sep 2020 to 7 Dec 2020](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fbesu/dashboard?time=%7B%22from%22%3A%222020-09-28T06%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222020-12-08T01%3A50%3A27.952Z%22%7D)

Commits from 2020-08-28 to 2020-12-07 : 169

Committers from 2020-08-28 to 2020-12-07 : 20 (5 non-PegaSys)

Identified Orgs  2020-08-28 to 2020-12-07 : 4 + 1 independent

# Additional Information

N/A

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
