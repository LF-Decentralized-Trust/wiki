1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q2 Hyperledger Iroha

Created by Sara Garifullina, last modified by Gari Singh on May 26, 2021

Project Health

Everything is going ok: there are 2 lines of development - of Iroha v1 (on C++, production ready) and Iroha v2 (in Rust, in development). There are internship projects for both of them.  Work is being done, updates are provided to the community every 2 weeks on the community meetings from both lines of development.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Switched in the main repository, others (library repositories) are not yet
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? We believe that [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) added it to the repos.

# Questions/Issues for the TSC

While moving to main branch we've realised that we have DCO issues that were not reported by the DCO tool before. Also, from where does the DCO tool gets what it expects in the sign-off?

# Releases

[https://github.com/hyperledger/iroha/releases/tag/1.2.1](https://github.com/hyperledger/iroha/releases/tag/1.2.1)

# Overall Activity in the Past Quarter

In general, communication is going smoothly, we try to answer questions that come to the chat and also hold our bi-weekly meetings synchronously. 

Regarding some more technical developments:

Iroha v1:

- Performance degradation fix
- Stability fixes that handle cases when other nodes are not accessible or have slow connection
- Performance metrics endpoint using prometheus (currently in support/1.2.x branch)
- Replacement RxCPP dependency with custom subscription engine for more predictable thread management (currently in test and review)
- Key-Value storage (currently under review)

Iroha v2: 

- Introduced lockfree data structures
- Introduced Grantable permissions
- Added Roles
- Deployed longevity stand
- Increased significantly linting strictness
- Covered several DOS attack vectors
- Improved error reporting
- Introduced transaction, block and message versioning support
- Added pagination for queries

# Current Plans

Iroha 1:

- Introduce UDP-based peer-to-peer gossiping to boost networking
- Improve ordering service and consensus to improve performance

Iroha 2:

- Record telemetry and display it as a web app
- Prometheus endpoint
- Researching possibility of migrating async runtime to Tokio
- Researching Triggers for our smart contract language
- Implement autogeneration of client libs data model

# Maintainer Diversity

Our contributor [baziorek](https://lf-hyperledger.atlassian.net/wiki/people/70121:fcfd1447-e409-47ac-bf14-f78e6031899d?ref=confluence) (Grzegorz) is now a maintainer and already helped us a lot by helping others in the chat, adding new functionality to Python library and by mentoring one of the internship projects. 

Another addition to the team is Ivan Kuvaldin who developed the metrics feature. 

# Contributor Diversity

Core team still consists of Soramitsu team as well as contributors from other companies, such as Grzegorz and Sonoko Mizuki.

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
