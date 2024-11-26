1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q2 Hyperledger Besu

Created by Grace Hartley (Deactivated), last modified by Gari Singh on Oct 16, 2021

## Project Health

Hyperledger Besu remains a strong project with a growing community network of contributors. This quarter the team has focused on Ethereum protocol improvements as well as many performance improvements, included in the Hyperledger Besu 21.7.0 Release, which will be launched on July 6th. 

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? No, this was not completed with final Berlin mainnet activation as originally planned. It is was deprioritized to be completed after the London Hard fork (scheduled for mid-July) because of unknown downstream impacts. [Issue is here](https://github.com/hyperledger/besu/issues/2035).
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? Yes, via GitHub actions.

Questions/Issues for the TSC

None, at this time. DCO sign off remains a challenge, but we are aware that this request is being considered by Linux Foundation's Legal team.

# Releases

Hyperledger Besu has completed six releases. We are currently preparing for the 21.7.0 Quarterly Release.

- 21.1.3 - 2021 Mar 23
- 21.1.4 - 2021 Apr 8
- 21.1.5 - 2021 Apr 21
- 21.1.6 - 2021 May 19
- 21.1.7 - 2021 Jun 1
- 21.7.0-RC1 - 2021 Jun 15

Functional improvements in these releases include:

**Berlin Network Upgrade - Released**

The team completed work to ensure Hyperledger Besu was compatible with the Ethereum hard fork, Berlin, which occurred on April 15th. The [Berlin Network upgrade](https://blog.ethereum.org/2021/03/08/ethereum-berlin-upgrade-announcement/) included several improvements to the Ethereum mainnet, such as the addition of subroutines to the EVM, the introduction of “transaction envelopes”; which make it easier for Ethereum to support several different kinds of transactions, and changes in gas costs to increase the security of the network.

**London Hard Fork - Scheduled for July 14th**

The team has been preparing Hyperledger Besu to be compatible with the next Ethereum hard fork, London. The London Hard Fork includes: 

- [EIP-1559: Fee market change for ETH 1.0 chain](https://eips.ethereum.org/EIPS/eip-1559)
- [EIP-3198: BASEFEE opcode](https://eips.ethereum.org/EIPS/eip-3198)
- [EIP-3529: Reduction in refunds](https://eips.ethereum.org/EIPS/eip-3529)
- [EIP-3541: Reject new contracts starting with the 0xEF byte](https://eips.ethereum.org/EIPS/eip-3541)
- [EIP-3554: Difficulty Bomb Delay to December 1st 2021](https://eips.ethereum.org/EIPS/eip-3554)

**Besu on Tessera**

Besu is now compatible with and can be run with Tessera, the Apache 2.0 licensed private transaction manager written in Java. If you have previously used Orion as a privacy transaction manager of choice, it will be deprecated in November 2021. Tessera is a drop in replacement for Orion.

Overall Activity in the Past Quarter

Many of the maintainers have been focusing on continuing mainnet compatibility work and adding cross-client support for GoQuorum within the Besu codebase.

# Current Plans

1. The project team remains currently working towards its 21.7.0 Release, scheduled for July of 2021. The 21.7 Release is expected to include the following features:
2. 1. London network upgrade
   2. EIP-1559
   3. Besu working with Tessera
3. Similar to last quarter, Besu is also continuing to engage with its community and grow the diversity and decentralization of its maintainer and contributor base.

# Maintainer Diversity

Our maintainer decentralization had a small decrease from the prior quarter. 

The three organizations include:

- ConsenSys Quorum (FKA PegaSys)
- Chainsafe
- Splunk

We completed moving 3 maintainers to emeritus status and we added 4 (Vijay Michalik, Sajida Zouarhi, Gary Schulte, and Alexandra Tran) new maintainers from ConsenSys. We also updated our [maintainer definition](https://github.com/hyperledger/besu/blob/master/MAINTAINERS.md) to allow for non-code contributors. Because we expanded the definition of maintainers, which we think is valuable for our community, we have seen a slight decrease in the maintainer diversity of the organizations.

The maintainers breakdown is:

- 13% non-ConsenSys (3 of 23) - a decrease of 6% from last quarter.

# Contributor Diversity

[LF Analytics from March 23 to June 21st](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fbesu/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-03-23T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-06-21T04%3A00%3A00.000Z%22%7D)

Commits from 2021-03-23 to 2021-06-21: 253

Committers from 2021-03-23 to 2021-06-21: 33 (13 non-ConsenSys)

Identified Orgs  2021-03-23 to 2021-06-21: 5

# Badging

Hyperledger Besu is testing out the badging process. [Here is a link](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Project+Badge+Status) of its current statuses for each of the badges.

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
