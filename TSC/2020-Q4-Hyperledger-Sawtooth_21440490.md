1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q4 Hyperledger Sawtooth

Created by Andi Gunderson, last modified by David Enyeart on Oct 22, 2020

# Project

Hyperledger Sawtooth [https://sawtooth.hyperledger.org/](https://sawtooth.hyperledger.org/)

Project Health

The primary focus of the last quarter was integrating Hyperledger Transact's transaction execution platform into the Sawtooth Validator.

The Sawtooth community is actively engaging in live, public working sessions to decide Sawtooth's future. Some community members have expressed interest in contributing to new Sawtooth features, and others have promised to contribute enhancements and features already developed.

# Questions/Issues for the TSC

No new issues.

# Releases

- Sawtooth Library v0.4.0 -  8/4/2020
- Sawtooth Library v0.5.0 -  8/13/2020
- Sawtooth Library v0.6.0 -  9/17/2020
- Sawtooth Library v0.6.1 -  9/24/2020
- Sawtooth Library v0.6.2 -  9/29/2020
- Sawtooth Library v0.6.3 -  10/05/2020
- Sawtooth Rust SDK v0.4.5 - 8/4/2020
- Sawtooth Rust SDK v0.5.0 - 9/3/2020
- Sawtooth Sabre v0.6.0 - 9/8/2020
- Sawtooth PBFT v1.03 - 8/5/2020
- Sawtooth Devmode v1.2.4 - 8/4/2020

# Overall Activity in the Past Quarter

The community continues to discuss Sawtooth-related issues on Rocketchat. Live working sessions have also been used on a monthly basis to discuss the future of Sawtooth, with strong participation from the community.

The following key work has been completed in the Sawtooth codebase:

- Sawtooth-core now uses Hyperledger Transact for transaction execution. The Python transaction execution platform has been removed from sawtooth-core. This replaces a large chuck of the validator that was still written in Python and updates it to Rust. Transact does not currently support external smart contract engines, so the required smart contracts are now compiled in, including Sawtooth Sabre to support uploading custom smart contracts.
- The transact-compat feature was removed from the Rust SDK. This feature provided a trait implementation for the Transact signer trait for the sawtooth signer. The signer trait was removed in the 0.3 release of Transact.
- More code has been re-written in Rust and moved to the Sawtooth library from the Sawtooth validator. This is a continuation of the efforts to rewrite the Sawtooth validator entirely in Rust and to provide a library of Sawtooth components that can be used in a variety of ledger implementations.
- The infrastructure and theme for the Sawtooth website refresh have been completed in a new branch.

# Current Plans

The following work is currently in progress:

- Long running (LR) network testing of the Sawtooth validator with Hyperledger Transact
- Rewriting the Sawtooth CLI in Rust
- Refreshing the Sawtooth website and documentation

The following work is currently planned:

- Create a new consensus library that will be used by the Sawtooth validator
- Initialize a Sawtooth service for Splinter
- Move portions of Sawtooth Sabre to Hyperledger Transact

Plans will continue to be developed as part of the working sessions.

# Maintainer Diversity

Maintainers are distributed across [Bitwise](http://bitwise.io/) IO, Cargill, Intel, and Walmart Labs.

# Contributor Diversity

Commits from 2020-07-01 to 2020-09-31 :  257

Committers from 2020-07-01 to 2020-09-31 :  8

Domains from 2020-07-01 to 2020-09-31 :  3

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
