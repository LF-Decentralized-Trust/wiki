1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q3 Hyperledger Besu

Created by Grace Hartley (Deactivated), last modified by Arnaud J LE HORS on Nov 11, 2021

Project Health

Hyperledger Besu remains a strong project with a growing community network of contributors. This quarter the team has focused on Ethereum protocol improvements, including EIP-1559, which went live on August 5th, as well as many performance improvements, included in the Hyperledger Besu 21.10.0 Release, which will be launched on October 26th. 

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes, this is complete.
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes, via GitHub actions

# Questions/Issues for the TSC

None, at this time. DCO sign off remains a challenge, but we are aware that this request is being considered by Linux Foundation's Legal team.

# Releases

Hyperledger Besu has completed five releases. We are currently preparing for the 21.10.0 Quarterly Release.

- 21.7.0 RC 1 - 2021 Jun 15
- 21.7.0 RC 2 - 2021 June 22
- 21.7.0 (full release) - 2021 Jul 6
- 21.7.1 - 2021 Jul 14
- 21.7.2 - 2021 Aug 4
- 21.7.3 - 2021 Sep 2
- 21.7.4 - 2021 Sep 16

Functional improvements included in these releases:

**London Hard Fork - Launched on August 5th**

The team has been preparing Hyperledger Besu to be compatible with the next Ethereum hard fork, London. The London Hard Fork included: 

- [EIP-1559: Fee market change for ETH 1.0 chain](https://eips.ethereum.org/EIPS/eip-1559)
- [EIP-3198: BASEFEE opcode](https://eips.ethereum.org/EIPS/eip-3198)
- [EIP-3529: Reduction in refunds](https://eips.ethereum.org/EIPS/eip-3529)
- [EIP-3541: Reject new contracts starting with the 0xEF byte](https://eips.ethereum.org/EIPS/eip-3541)
- [EIP-3554: Difficulty Bomb Delay to December 1st 2021](https://eips.ethereum.org/EIPS/eip-3554)

**EthStats Support**

Previously, we launched EthStats support as an experimental feature. We are pleased to share that it is now a stable feature generally available for use within Hyperledger Besu. EthStats provides insight into network health by displaying real time and historical statistics about the network and nodes on public mainnets, testnets and permissioned networks.

**QBFT: The New Byzantine Fault Tolerant Consensus Algorithm**

The team has released QBFT, a Byzantine Fault Tolerant consensus algorithm, building on the capabilities of IBFT and IBFT 2.0. In addition to the benefits of earlier BFT consensus mechanisms, such as stability and reliability, QBFT aims to provide performance improvements in cases of excess round change. QBFT is interoperable between the GoQuorum Ethereum client and Hyperledger Besu and supports networks with both GoQuorum and Hyperledger Besu nodes.

# Overall Activity in the Past Quarter

Many of the maintainers have been focusing on continuing mainnet compatibility work and adding cross-client support for GoQuorum within the Besu codebase. Specifically, the team was dedicated towards the London Hard Fork. Significant contributions have come from Hedera Hashgraph, who are working on integrating the Besu EVM into future releases of Hedera's network. Hedera's focus is on performance and utility.

# Current Plans

1. **21.10.0 Release:** The project team remains currently working towards its 21.10.0 Release, scheduled for October 2021. The 21.10.0 Release is expected to include the following features:
   
   1. Performance improvements to prepare for the Merge
   2. Optimistic Besu: The team will be exploring different options for supporting use of the Besu EVM for Optimistic Rollups
   3. Permissioning features will be extended to include more granular account permissioning for different transaction and interaction types.
   4. EVM Library: the core EVM component will be separated as a stand alone library, suitable for use outside of an integrated mainnet client.
2. **Eth 1 to Eth 2 Merge:** Some of the Besu team is participating in a Eth1 and Eth2 contributor meet-up the week of October 2nd to discuss in detail the plans for the Eth 1 to Eth2 Merge, which moves Ethereum from Proof of Work to Proof of Stake. We anticipate this body of work to take up a significant amount of the team's time in the coming months.
3. **Grace Hopper Open Source Day:** The Besu project is participating in the Grace Hopper Open Source Day and we are excited to share our project with new joiners there.
4. **Community Engagement:** Similar previous quarters, Besu is also continuing to engage with its community and grow the diversity and decentralization of its maintainer and contributor base. We have added about 15 new good first issues so we encourage the community to give them a try.

# Maintainer Diversity

There four organizations who are maintainers include:

- ConsenSys Quorum (FKA PegaSys)
- Chainsafe
- Hedera Hashgraph
- Splunk

The maintainers breakdown is:

- 16% non-ConsenSys (4 of 25) - This is a slight improvement from prior quarters.

# Contributor Diversity

[LF Analytics from June 22nd to September 22nd](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fbesu/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-06-21T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-09-22T04%3A00%3A00.000Z%22%7D)

Commits from 2021-06-22 to 2021-09-22: 215

Committers from 2021-06-22 to 2021-09-22: 28 (9 non-ConsenSys)

Identified Orgs  2021-03-23 to 2021-06-21: 4

# Badging

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

## Attachments:

![](images/icons/bullet_blue.gif) [QBFT Presentation for the EEA (1).pdf](attachments/21443069/21454771.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
