1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q2 Hyperledger Iroha

Created by Sara Garifullina, last modified by Jim Zhang on Aug 25, 2022

Project Health

Generally, the situation is the following: Iroha 1 is being maintained and improved in terms of performance – the new transport system is being developed. Iroha 2 is rapidly growing – the team welcomed several new developers and numerous features; releases are presented every month. [baziorek](https://lf-hyperledger.atlassian.net/wiki/people/70121:fcfd1447-e409-47ac-bf14-f78e6031899d?ref=confluence) is leading this year's Mentorship effort. Community is not very active but the team is open and answers the questions when those occur.

Iroha 2 team has acquired 4 more Rust developers to speed up the planned workload and cover more "functional ground". Also, as part of a wider organisational change, Iroha 2 team will fall within HL Iroha 2.0 Tribe which consists of multiple related projects. As a result, to improve the internal communication, we are planning to start running monthly technical demonstration sessions on new delivered features. In the near future, we are aiming to open the demo session to a wider audience and make it publicly available to the wider Hyperledger community. In addition, Iroha 2 has started with a new front-and initiative (blockchain Explored). Currently, UI/designs are ready and the development is well underway. 

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes
3. Has your project implemented these inclusive language changes listed below to your repo? You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo.
   
   1. master → main
   2. slave → replicas
   3. blacklist → denylist
   4. whitelist → allowlist
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? Not yet
   

# Questions/Issues for the TSC

# Releases (Iroha 1x)

[https://github.com/hyperledger/iroha/releases/tag/1.4.0](https://github.com/hyperledger/iroha/releases/tag/1.4.0)

[https://github.com/hyperledger/iroha/releases/tag/1.5.0](https://github.com/hyperledger/iroha/releases/tag/1.5.0)

# Releases (Iroha 2x)

[https://github.com/hyperledger/iroha/releases/tag/v2.0.0-pre-rc.2](https://github.com/hyperledger/iroha/releases/tag/v2.0.0-pre-rc.2)

[https://github.com/hyperledger/iroha/releases/tag/v2.0.0-pre-rc.3](https://github.com/hyperledger/iroha/releases/tag/v2.0.0-pre-rc.3)

# Overall Activity in the Past Quarter

We moved to Discord with the whole Hyperledger Community and adapted the chat bot – now it connects Discord, Telegram and Gitter and runs more easily maintainable code, so everyone should be able to stay in contact just the way it is convenient to them.

# Iroha v1

Some of the most important technical results for Iroha 1 team in the last quarter were:

- the module for MST was rebuilt for more efficiency
- [baziorek](https://lf-hyperledger.atlassian.net/wiki/people/70121:fcfd1447-e409-47ac-bf14-f78e6031899d?ref=confluence) and his team helped greatly with updating Python library that is now working perfectly with Iroha 1 newest versions
- Work is on the way on rework of the transport
- Burrow now works with RocksDB
- Other optimisations

# Iroha v2 (main completed features for the last quarter):

- Introduced better and improved non-mintable assets
- Introduced new standard for TPS benchmarks
- Account restructuring
- Roles are no longer optional. More features to be axed
- SDK - Trigger support
- RawGenesisBlock builder
- Real-world performance testing (stable ~40TPS)

# Current Plans

It is important to keep in touch with the community using all the channels possible: Iroha 2 is being very actively developed with many new team members.

Iroha 1 is also not only maintained – the next release should include changes that will drastically improve the performance via rework of the transport – it should be completed for Iroha v1.6.

**Iroha v2 (in the progress):**

- Improved common filtering API
- Debug 3 high severity actor-related bugs:

<!--THE END-->

1. 1. Slow processing (~50TPS)
   2. Kura init (versioning)
   3. Register/unregister peer

<!--THE END-->

- Distributed testing in CI
- Ongoing work on WASM dynamic linkage
- Docker friendly CLI

**Long term deliverables for Iroha 2**

1. Hijiri (local reputation system)
2. Offline transactions (Hardware is ready and waiting to be programmed)
3. Parachain compatibility
4. Iroha Python Library should be improved
5. Transaction fees are to be introduced.

# Maintainer Diversity

Iroha 2 has considerably grown in size and diversity of resources. Currently, Iroha 2 team consist of 1 front-end developer (mainly engaged in the blockchain explorer initiative), a technical writer, fully committed QA and currently, the core team consists of 8 Rust developers. 

# Contributor Diversity

[baziorek](https://lf-hyperledger.atlassian.net/wiki/people/70121:fcfd1447-e409-47ac-bf14-f78e6031899d?ref=confluence)'s team still greatly contributes to the project, Soramitsu's team is growing as well. We hope to find more contributors interested in features that Iroha 2 can provide. 

# Additional Information

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [artem](https://lf-hyperledger.atlassian.net/wiki/people/557058:5196a62e-7a77-4c97-8180-ae5a5992fb63?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [kamlesh nagware](https://lf-hyperledger.atlassian.net/wiki/people/557058:8e1fc425-f938-4b39-ad13-9cd8b0ddde52?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
