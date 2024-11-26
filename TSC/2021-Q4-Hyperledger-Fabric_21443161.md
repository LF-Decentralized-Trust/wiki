1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q4 Hyperledger Fabric

Created by David Enyeart, last modified by Bobbi Muscara on Nov 04, 2021

Hyperledger Fabric [https://github.com/hyperledger/fabric](https://github.com/hyperledger/fabric)

# Project Health

Hyperledger Fabric has stabilized with an LTS release process and incremental new features being added in minor releases. There is less churn and fewer commits than in years past, with continued focus on quality and support. New features get proposed, approved, and implemented based on a community RFC process. Mailing list activity is down compared to prior years. PRs and mailing list questions are generally turned around quickly.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
   
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes.
   

# Questions/Issues for the TSC

None

# Releases

v2.2 is the current LTS releases with patch releases quarterly.

Releases past quarter:

- v2.2.4 - September 8, 2021
- v2.3.3 - September 8, 2021
- v2.4.0-beta - August 12, 2021

Upcoming releases planned this quarter:

- v2.4.0

# Overall Activity in the Past Quarter

The project delivered v2.4.0-beta with two significant new features:

- **Fabric Gateway** - The Fabric Gateway will remove much of the transaction submission and query logic from the client application and shift it to a common gateway running within the Fabric peer, enabling each of the various client SDKs to be slimmer, more consistent, and require less maintenance. Applications will interact with a trusted peer (e.g. at their organization) and the peer will coordinate endorsements from other peers and submission to the ordering service. It will also simplify the administrative overhead of running a Fabric network because client applications will be able to connect and submit transactions via a single network port at their organization rather than the current situation where ports have to be opened from a client application to multiple peers across potentially multiple organizations. The Fabric Gateway is delivered along with slim SDKs in the [https://github.com/hyperledger/fabric-gateway](https://github.com/hyperledger/fabric-gateway) repository. Check out the [client application samples](https://github.com/hyperledger/fabric-gateway/tree/main/samples).
- **Peer unjoin** - The new command "peer node unjoin" enables an administrator to remove (unjoin) a channel from a peer.
  
  The peer must be stopped when the command is executed so that channel artifacts can be cleaned up.
  
  The channel's blockchain, state database, and associated entries will be removed from the peer.
  
  When the peer is restarted it will no longer receive blocks for the channel.

Additionally the project has been planning future work through the RFC process.

[RFCs merged](https://github.com/hyperledger/fabric-rfcs/tree/master/text) this quarter:

- OpenTelemetry (implementation has started across Fabric, SDKs, and chaincodes to enable tracing across the components).

New [RFCs in review](https://github.com/hyperledger/fabric-rfcs/pulls) this quarter:

- Private Data Purge

A survey was completed to gauge interest in future enhancements. The top candidates were identified as 1) BFT support 2) Pruning of old blocks 3) Performance improvements. Each of these items are on the Fabric roadmap. Specifically in the area of BFT options, the [SmartBFT RFC](https://github.com/hyperledger/fabric-rfcs/pull/33) has been revived and progress is being made on the [MirBFT Hyperledger lab](https://github.com/hyperledger-labs/mirbft).

There has also been a significant amount of Fabric activity in Hyperledger Labs, a few highlights:

- [https://github.com/hyperledger-labs/fabric-smart-client](https://github.com/hyperledger-labs/fabric-smart-client)
- [https://github.com/hyperledger-labs/fabric-token-sdk](https://github.com/hyperledger-labs/fabric-token-sdk)
- [https://github.com/hyperledger-labs/fabric-operations-console](https://github.com/hyperledger-labs/fabric-operations-console)
- [https://github.com/hyperledger-labs/minifabric](https://github.com/hyperledger-labs/minifabric)
- [https://github.com/hyperledger-labs/fabric-opssc](https://github.com/hyperledger-labs/fabric-opssc)
- [https://github.com/hyperledger-labs/mirbft](https://github.com/hyperledger-labs/mirbft)

# Current Plans

The project is working towards a final v2.4.0 release in Q4 with the Fabric Gateway as the primary new feature.

Other work items in plan or in progress:

- A feature to purge private data stores, which will help solutions meet GDPR requirements. [RFC available for review](https://github.com/hyperledger/fabric-rfcs/pull/46).
  
- A more realistic Node.js SDK sample application demonstrating good practices (connection management, error handling, timeouts, retries, etc)
- Guidance for kubernetes deployments and announcement of a Fabric Kubernetes working group. For more information see the contributor meeting from [October 13th](https://lf-hyperledger.atlassian.net/wiki/download/attachments/22842558/20211013_contributors_meeting.mp4?api=v2).
  

# Maintainer Diversity

One new maintainer was added this quarter. 6 of 11 maintainers are from IBM.

# Contributor Diversity

Year to year comparison, by commit:

- Q3 2020 - 990 commits. 69% from IBM.
- Q3 2021 - 411 commits. 59% from IBM

Year to year comparison, by contributor:

- Q3 2020 - 130 contributors. 27% from IBM.
- Q3 2021 - 87 contributors. 28% from IBM.

# Additional Information

Link to the Fabric dashboard: [Q3 2021](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffabric/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-07-01T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-10-01T04%3A00%3A00.000Z%22%7D)

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [artem](https://lf-hyperledger.atlassian.net/wiki/people/557058:5196a62e-7a77-4c97-8180-ae5a5992fb63?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [kamlesh nagware](https://lf-hyperledger.atlassian.net/wiki/people/557058:8e1fc425-f938-4b39-ad13-9cd8b0ddde52?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:54be3a11-ffe8-43a5-b37d-c854a0aa21c3?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
