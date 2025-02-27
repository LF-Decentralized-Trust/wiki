1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q1 Hyperledger Quilt

Created by David Fuelling, last modified by Gari Singh on Apr 27, 2020

# Project

[Hyperledger Quilt](https://github.com/hyperledger/quilt)

Project Health

Project health over Q1 has been good. We had a new dot-release of version 1 of the library, and a few patch releases. Additionally, we have engaged an independent third party to perform a security audit of the library. No new contributors or maintainers joined the project during this quarter.

# Questions/Issues for the TSC

There are no issues at this time.

# Releases

Quilt had three releases in Q1:

- Quilt [v1.1.0](https://github.com/hyperledger/quilt/releases/tag/v1.1.0): Adjusted the API for network communication settings; misc bug fixes.
  
  - Quilt [v1.1.](https://github.com/hyperledger/quilt/releases/tag/v1.1.0)1: Fix packet-expiry computation in STREAM Sender (See [#432](https://github.com/hyperledger/quilt/issues/432)).
- Quilt [v1.0.3](https://github.com/hyperledger/quilt/releases/tag/v1.0.3): A maintenance release fixing a few outstanding bugs; deprecating unused features and general library cleanup.

# Overall Activity in the Past Quarter

This past quarter was mainly focused on bug-fixes and API improvements as we deploy the Quilt library into actual systems such as the [Java Connector](https://connector.interledger4j.dev/). We had three releases to fix bugs and make minor improvements in response to this feedback. In addition, we are kicking off a third-party independent security review of Quilt and hope to publish findings in Q2.

# Current Plans

The team is currently working to productionalize the [Java Connector](https://connector.interledger4j.dev/) and enhance it with Wallet functionality to be able to store and track Interledger transactions. A dev implementation can be found at [https://wallet.ilpv4.dev](https://wallet.ilpv4.dev) and a test/mainnet implementation of this wallet will be hosted and supported at [https://xpring.io](https://xpring.io). Using feedback from this process, we will potentially introduce new functionality into the Quilt library as it makes sense. To this end, we plan on having a 1.2 release during Q2, but no exact date has been determined.

One goal of the Xpring wallet is to demonstrate the cross-asset exchange capabilities of Interledger. To this end we hope to setup and start experimenting with a fabric testnet to demonstrate cross-chain fungible asset transfers between two fabric networks. More details to come on this POC.

Finally, a third-party independent security review of both the Quilt libraries and Java Connector projects is underway. Results of these audits will be published to the Quilt wiki once they the reports are completed and any critical security vulnerabilities, if any, are patched.

# Maintainer Diversity

Maintainer diversity is unchanged with four full-time people maintaining the project. While our technical diversity is strong, we are all funded by the same company, so from this perspective maintainer diversity is low.

# Contributor Diversity

Contributor diversity is unchanged.

# Additional Information

Not at this time.

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
