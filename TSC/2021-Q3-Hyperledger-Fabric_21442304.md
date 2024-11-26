1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q3 Hyperledger Fabric

Created by David Enyeart, last modified by Gari Singh on Oct 16, 2021

Hyperledger Fabric [https://github.com/hyperledger/fabric](https://github.com/hyperledger/fabric)

# Project Health

Hyperledger Fabric continues to mature, as evidenced by the following observations throughout this report:

- LTS release available
- Project developers have been spending a larger percentage of time on maintenance and support than in the past, given the increasing number of production deployments and LTS releases.
- Lower commit velocity on new features in core Fabric, more activity around extensions in Hyperledger labs
- Healthy RFC process with reviews in contributor meetings to drive consensus on new features.

The commit rate and mailing list activity were down compared to the same period last year. PRs and mailing list questions are generally turned around quickly.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
   
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? Not yet
   

# Questions/Issues for the TSC

None

# Releases

v2.2 is the current LTS releases with patch releases quarterly. v1.4 LTS went end of support in April 2021. Production users are encouraged to use v2.2, users who want to try new features are encouraged to use v2.3 and v2.4.0-alpha and provide feedback.

Releases past quarter:

- v1.4.12 - April 23, 2021
- v2.2.3 - April 23, 2021
- v2.3.2 - April 23, 2021
- v2.4.0-alpha - April 15, 2021

Upcoming releases planned this quarter:

- v2.2.4
- v2.3.3
- v2.4.0-beta

v2.3 added two major features which are seeing encouraging adoption in the community:

- Ledger snapshot enables a peer to take a snapshot of its state. This allows new peers to join a channel from an agreed upon snapshot, reducing the time to join a channel and the storage size required to maintain a ledger. In the future it will also be possible to prune/archive old blocks to bring the same benefit to existing peers.
- The channel participation management feature improves the privacy and scalability of the ordering service since a global 'system channel' will no longer be needed for the creation and management of channels.

# Overall Activity in the Past Quarter

The project was busy maintaining the releases and preparing for a v2.4.0-beta release with the new Fabric Gateway (details below).

Additionally the project has been planning future work through the RFC process.

[RFCs merged](https://github.com/hyperledger/fabric-rfcs/tree/master/text) this quarter:

- Orderer ledger snapshots

[RFCs in review](https://github.com/hyperledger/fabric-rfcs/pulls) this quarter:

- WASM for smart contracts
- BFT ordering service
- Modular crypto service
- OpenTelemetry

There has also been a significant amount of Fabric activity in Hyperledger Labs, a few highlights:

- [https://github.com/hyperledger-labs/fabric-smart-client](https://github.com/hyperledger-labs/fabric-smart-client)
- [https://github.com/hyperledger-labs/fabric-token-sdk](https://github.com/hyperledger-labs/fabric-token-sdk)
- [https://github.com/hyperledger-labs/fabric-operations-console](https://github.com/hyperledger-labs/fabric-operations-console)
- [https://github.com/hyperledger-labs/minifabric](https://github.com/hyperledger-labs/minifabric)
- [https://github.com/hyperledger-labs/fabric-opssc](https://github.com/hyperledger-labs/fabric-opssc)
- [https://github.com/hyperledger-labs/mirbft](https://github.com/hyperledger-labs/mirbft)

# Current Plans

The largest item being worked in 2021 is the Fabric Gateway, a new component that will implement much of the high-level 'gateway' programming model. This will remove much of the transaction submission and query logic from the client application and shift it to a common gateway running within the Fabric peer, enabling each of the various client SDKs to be slimmer, more consistent, and require less maintenance. It will also simplify the administrative overhead of running a Fabric network because client applications will be able to connect and submit transactions via a single network port rather than the current situation where ports have to be opened from a client application to multiple peers across potentially multiple organizations. The Fabric Gateway is expected to be function complete for a Q3 v2.4.0-beta release.

Other work items in plan or in progress:

- A feature to purge private data stores, which will help solutions meet GDPR requirements. An RFC is expected so that we can gather additional feedback from the community.
- A feature to unjoin a peer from a channel.
- A more realistic Node.js SDK sample application demonstrating good practices (connection management, error handling, timeouts, retries, etc)
- Guidance for kubernetes deployments

Additional discussion of Fabric roadmap can be found in [this contributor meeting recording](https://lf-hyperledger.atlassian.net/wiki/download/attachments/22842558/20210623_contributors_meeting.mp4?api=v2).

# Maintainer Diversity

Two maintainers retired this quarter. 5 of 10 maintainers are from IBM.

# Contributor Diversity

Year to year comparison, by commit:

- Q2 2020 - 1140 commits. 67% from IBM.
- Q2 2021 - 396 commits. 54% from IBM

Year to year comparison, by contributor:

- Q2 2020 - 96 contributors. 38% from IBM.
- Q2 2021 - 77 contributors. 22% from IBM.

# Additional Information

Link to the Fabric dashboard: [Q2 2021](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffabric/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-04-01T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-07-01T04%3A00%3A00.000Z%22%7D)

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
