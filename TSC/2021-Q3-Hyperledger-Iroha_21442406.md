1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q3 Hyperledger Iroha

Created by Sara Garifullina, last modified by Arun .S.M. on Nov 01, 2021

Project Health

We are doing pretty well - both Iroha versions are being developed, there is a status update on every community meeting. Community is happy to welcome the contributions from the interns. New features are being implemented and general community communication seems to be going well. 

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Last 2 library repos left. We do not have permissions to rename anything there or change default branches. We will ask the LF support team to do that instead.
2. [Have you implemented the Common Repository Structure in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)?

# Questions/Issues for the TSC

We believe CRS was somehow implemented by the HL team, but maybe we are wrong?  

# Releases

Last release ([https://github.com/hyperledger/iroha/releases/tag/1.2.1](https://github.com/hyperledger/iroha/releases/tag/1.2.1)) was on March 19, currently we are already testing the new release that will include new features such as new DB. 

# Overall Activity in the Past Quarter

Chats are relatively active. With the internship projects and new features being developed we are pretty active. Questions are being answered. We are also working on a process of how questions about client libraries will be replied as libraries require some more qualifications but as of now everything is going smoothly. Community meetings keep happening every 2 weeks. 

1. RocksDB was integrated to store Iroha's state
2. WSVChecker tool was implemented to check consistency of Iroha state after migration from PosgresDB to RocksDB
3. Tool that migrates database from Postgres backend to RocksDB backend is being implemented
4. Other minor improvements: further replacement of RXCPP with custom Subscription engine, consensus optimizations, stability improvements

For Iroha2 overall we have been working hard on client libraries and network stability:

1. Multiple consensus fixes
2. Actor framework integration
3. Java client lib finished
4. JS client lib finished
5. iOS client lib nearly finished

# Current Plans

For Iroha 1 the plan is to release the version with a new DB option. We are very close to it. We have every reason to plan finishing internships successfully and have new Cactus integration and some other features. 

After that we will work on new features that will be part of the 1.3.1 release:

1. Syncing node – back up node that does not participate in consensus, but may process queries and propagate transactions
2. Optimize storage – integrated key-value storage already speeds up transaction processing, but we may further improve performance by introducing in-memory caches for the most frequently accessible data

For Iroha 2 - development is going forward, new features are being implemented. Pre-release scope is defined and its date is in discussion. Internship is progressing successfully.

The features currently in development and planned for near future:

1. Python Client Library
2. Triggers
3. WASM Integration Prototyping
4. Migration to custom p2p networking lib

# Maintainer Diversity

[https://github.com/orgs/hyperledger/teams/iroha-maintainers/members](https://github.com/orgs/hyperledger/teams/iroha-maintainers/members) - for both Iroha 1 and Iroha 2 development teams. 

# Contributor Diversity

Contributors are represented by Soramitsu employees and also individual contributors helping both with code and helping out in chats. 

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
