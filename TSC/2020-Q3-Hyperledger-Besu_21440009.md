1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q3 Hyperledger Besu

Created by Grace Hartley, last modified by Gari Singh on Sep 17, 2020

# Project

Hyperledger Besu

Project Health

Hyperledger Besu remains a strong project with a growing community network of contributors. This quarter the team has focused on fostering its community as well as many performance improvements, included in the Hyperledger Besu 1.5 Release, which was launched on July 15th. The team is currently building towards its 1.6 Release.

# Questions/Issues for the TSC

There are no issues at this point. The Hyperledger Besu team does have a question for the TSC:

- **Release Versioning:** Our Hyperledger Besu team is currently proposing switching from Semantic Versioning for Releases to CalVer. Instead of using Major.Minor.Patch, Besu would use Year.Quarter.PatchNumber or Year.Month.PatchNumber. For example, instead of 1.5.2 and 1.6.0 we would have something like 20.3.2 and 20.4.0 or 20.8.2 and 20.10.0. We would like to gain the TSC’s feedback on this change.

# Releases

Hyperledger Besu has completed eight bi-weekly patch releases (1.4.6 on 10 Jun, 1.5RC1 on 17 Jun, 1.5-RC2 on 30 Jun, 1.5 on July 15, 1.5.1 RC on 22 Jul, 1.5.1 on 29 Jul, 1.5.2 on 13 Aug, and 1.5.3 on 27 Aug)

Some functional improvements include:

**Production-Ready Features:**

- **Privacy:** The most recent set of privacy enhancements include:
  
  - Ability to add and remove members from privacy groups.
  - Filters and subscriptions for private contracts.
  - Web3j and web3js support for private transactions and filters.
- **Performance**
  
  - Added native encryption libraries to provide optimization optionality
  - EVM execution improvements
  - Improved logs querying performance
  - Improved transactions per second (TPS) performance by 33%
- **Parity Tracing APIs**: Performed additional testing

**Early Access Features:**

- **EIP-1559 Support:** Hyperledger Besu has been one of the clients leading the implementation of EIP-1559, a major upgrade to Ethereum’s transaction fee market.
- **Ephemeral Testnet YOLO:** In preparation for the next network upgrade, Berlin, an ephemeral testnet called YOLO was launched with two new EIPs enabled: [EIP-2315](https://eips.ethereum.org/EIPS/eip-2315), which adds subroutines to the EVM, and [EIP-2537](https://eips.ethereum.org/EIPS/eip-2537), which introduces a new precompile for the BLS12-381 curve.
- **DNS Support**
- **State back-up and restore option**

Go to the [Changelog](https://github.com/hyperledger/besu/releases) for more details.

# Overall Activity in the Past Quarter

A few high-level activities include:

- The Hyperledger Besu 1.5 Release Overview blog was published [here](https://www.hyperledger.org/blog/2020/07/16/announcing-hyperledger-besu-1-5-available-now).
- Hyperledger Besu 1.5. Performance Blog was published [here](https://www.hyperledger.org/blog/2020/08/06/hyperledger-besu-1-5-performance-enhancements). This gives a detailed look at the performance upgrades and metrics to Besu in the past quarter.
- Continue to run our bi-weekly contributor calls and grow the attendance.
- We have been using the Hyperledger tools consistently and with continued success.

As a part of participating in the Hyperledger community, the Besu team has participated in the community by:

- Continuing to work on Besu’s support of Caliper.
- Presented Hyperledger webinar on Hyperledger Besu on August 4th.
- Mark Wagner led the Hyperledger mentorship project to have Besu run on OpenShift with Josh Fernandes' help. The mentorship proejct was completed last week with the work completed.

# Current Plans

1. The project team remains currently working towards its 1.6 Release, scheduled for mid-October. The 1.6 Release is expected to include the following features:
2. 1. Berlin network upgrade preparation
   2. P2P improvements
   3. Performance improvements and testing for privacy groups
   4. Bonsai Tries
3. Similar to last quarter, Besu is also continuing to engage with its community and grow the diversity of its maintainer and contributor base. The team is also looking forward to participating at the Hyperledger Member Summit.

# Maintainer Diversity

Our maintainer diversity remained fairly consistent from the prior quarter.  We continue to have maintainers from four different organizations. 

The four organizations include:

- ConsenSys (PegaSys)
- Web3Labs
- Chainsafe
- Splunk (maintainer was formerly at Machine Consultancy)

The new maintainers this quarter include:

- Stefan Pingel (ConsenSys)
- David Mechler (ConsenSys)

We had a one maintainer transition to Emeritus in the last quarter.

The maintainers breakdown is currently:

- 16% non-ConsenSys - This is a slight decrase from 21% in the prior quarter

# Contributor Diversity

Commits from 2020-06-08 to 2020-08-28 : 216

Committers from 2020-06-08 to 2020-08-28 : 26 (9 non-PegaSys)

Identified Orgs  2020-06-08 to 2020-08-28 : 5 + 4 independent

# Additional Information

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
