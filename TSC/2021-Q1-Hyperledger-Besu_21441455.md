1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q1 Hyperledger Besu

Created by Grace Hartley (Deactivated), last modified by Arun .S.M. on Apr 29, 2021

# Hyperledger Besu

Project Health

Hyperledger Besu remains a strong project with a growing community network of contributors. This quarter the team has focused on Ethereum protocol improvements as well as many performance improvements, included in the Hyperledger Besu 21.1.0 Release, which was launched on February 24th. The team is currently building towards its Q2 2021 release.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? No, awaiting final Berlin Mainnet activation then will switch
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? Yes, via github actions.

# Questions/Issues for the TSC

We continue to have issues with contributors giving up committing when encountered with the DCO sign off, especially with  documentation requests. Any suggestions on how to make the process easier and with less friction would be appreciated.

One possibility is to relax the DCO check *within* the PR for repositories who only do squash-merges and if the contributor makes a clear and unambiguous statement in the PR comments that their contribution conforms to the DCO standards. The commits to any main or non pull-request branch, however, would still require a DCO `Signed-off-by` line.

# Releases

Hyperledger Besu has completed seven  releases, including the quarterly major release cycle of 21.1.0. The releases included 20.10.2 on Dec. 16th, 20.10.4 on Jan 13, 21.1.0-RC1 on Jan 27th, 21.1.0-RC2 on Feb 10th, 21.1.0 (full release) on Feb. 24th, 21.1.1 on March 8th, 21.1.2 on March 15th. We had an extra release in addition to our regular bi-weekly schedule because we identified a bug related to the Berlin Hard Fork that we needed to fix.

Some functional improvements include:

**Berlin Network Upgrade** 

The team has been preparing Hyperledger Besu to be compatible with the next Ethereum hard fork, Berlin. The [Berlin Network upgrade](https://blog.ethereum.org/2021/03/08/ethereum-berlin-upgrade-announcement/) will include several improvements to the Ethereum mainnet, such as the addition of subroutines to the EVM, the introduction of “transaction envelopes”; which make it easier for Ethereum to support several different kinds of transactions, and changes in gas costs to increase the security of the network.

**Mainnet Launcher**

Mainnet Launcher makes it easy to create a config file for an Ethereum client at startup

**Node Hibernate:**

This is a proxy that monitors a node’s API traffic and hibernates the node when inactive. This reduces infrastructure costs by ensuring only nodes receiving API requests, or nodes required to establish consensus are running.

**Bonsai Tries – Early Access**  
Bonsai Tries is a new database format which reduces storage requirements and improves performance for access to recent state. While this feature is being developed as a way to deal with mainnet’s large state size, any network with a comparable state could benefit from it. With Bonsai Tries instead of a multi-trie key value store, there is one trie, one set of indexed leafs, and a series of diffs that can be used to move the trie forward or backwards. This will reduce chain head count and state read and write amplification from its current 10x-20x levels to 1x-2x for non-committed access. This feature is early access and may break between each release, and is hence not production recommended yet.

Go to the [Changelog](https://github.com/hyperledger/besu/releases) for more details.

# Overall Activity in the Past Quarter

There have been some significant maintainer contributions from decentralized maintainers

- Bonsai Tries by Danno Ferrin in an individual capacity.
- OpenTracing support langed provided by Antoine Tolume from Splunk.

The remainder of the maintainers have been focusing on continuing mainnet compatibility work and adding cross-client support for GoQuorum within the Besu codebase.

# Current Plans

1. The project team remains currently working towards its 21.4.0 Release, scheduled forJuly of 2021. The 21.4 Release is expected to include the following features:
2. 1. London network upgrade
   2. EIP-1559
   3. QiBFT a cross-client BFT algorithm specified by the EEA.
3. Similar to last quarter, Besu is also continuing to engage with its community and grow the diversity and decentralization of its maintainer and contributor base.

# Maintainer Decentralization

Our maintainer decentralization had a small increase from the prior quarter. Danno Ferrin has moved from ConsenSys to Reddit, but will continue to contribute in a personal capacity. David Mechler has moved to earn.com.

The four organizations include:

- ConsenSys Quorum (FKA PegaSys)
- Web3Labs
- Chainsafe
- Splunk

We are in the process of voting on making 3 maintainers emeritus status and adding 1 new maintainer. There were no other changes to the maintainer roster.

Prior to the pending actions 5 of 23 (21%) maintainers were non-ConsenSys. The maintainers breakdown if all the pending actions pass is:

- 19% non-ConsenSys (4 of 21) - an increase of 3% from last quarter.

# Contributor Diversity

[LF Analytics for Besu from 8 Dec 2020 to 22 Mar 2021](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fbesu/dashboard?time=%7B%22from%22%3A%222020-12-08T05%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-03-22T04%3A00%3A00.000Z%22%7D)

Commits from 2020-12-08 to 2021-03-22: 262

Committers from 2020-12-08 to 2021-03-22: 26 (13 non-PegaSys)

Identified Orgs   2020-12-08 to 2021-03-22: 5

# Additional Information

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
