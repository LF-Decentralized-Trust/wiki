1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q1 Hyperledger Fabric

Created by David Enyeart, last modified by Jim Zhang on Mar 09, 2022

Hyperledger Fabric [https://github.com/hyperledger/fabric](https://github.com/hyperledger/fabric)

Project Health

Hyperledger Fabric is fairly mature and stable with a Long-term support (LTS) release and incremental new features being added in minor releases. There is less churn and fewer commits than in years past, with continued focus on quality and support. New features get proposed, approved, and implemented based on a community RFC process. Mailing list activity is down compared to prior years. PRs and mailing list questions are generally turned around quickly.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
   
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes
   

# Questions/Issues for the TSC

None.

# Releases

v2.2 is the current LTS releases with patch releases approximately quarterly.

Releases past quarter:

- v2.2.4 - September 8, 2021
- v2.3.3 - September 8, 2021
- v2.4.0 - November 29, 2021
- v2.4.1 - December 17, 2021

Additionally, SDKs are regularly patched, most notably Java SDK v2.2.11 to update log4j and address the log4j December vulnerability.

Upcoming releases:

- v2.2.5 - Update to Go 1.17
- v2.4.2 - Update to Go 1.17
- v2.5.0 - Expected to be next LTS release

# Overall Activity in the Past Quarter

The project delivered v2.4.0 with two significant new features:

- **Fabric Gateway** - The Fabric Gateway will remove much of the transaction submission and query logic from the client application and shift it to a common gateway running within the Fabric peer, enabling each of the various client SDKs to be slimmer, more consistent, and require less maintenance. Applications will interact with a trusted peer (e.g. at their organization) and the peer will coordinate endorsements from other peers and submission to the ordering service. It will also simplify the administrative overhead of running a Fabric network because client applications will be able to connect and submit transactions via a single network port at their organization rather than the current situation where ports have to be opened from a client application to multiple peers across potentially multiple organizations. The Fabric Gateway is delivered along with slim SDKs in the [https://github.com/hyperledger/fabric-gateway](https://github.com/hyperledger/fabric-gateway) repository.
- **Peer unjoin** - The new command "peer node unjoin" enables an administrator to remove (unjoin) a channel from a peer.
  
  The peer must be stopped when the command is executed so that channel artifacts can be cleaned up.
  
  The channel's blockchain, state database, and associated entries will be removed from the peer.
  
  When the peer is restarted it will no longer receive blocks for the channel.

v2.4.1 also added an external builder for 'chaincode as a service' to the fabric-peer docker image that makes deployment to Kubernetes environments simpler.

For more details on v2.4 see the [What's New documentation](https://hyperledger-fabric.readthedocs.io/en/latest/whatsnew.html#what-s-new-in-hyperledger-fabric-v2-4).

Additionally the project has been planning future work through the RFC process.

[RFCs merged](https://github.com/hyperledger/fabric-rfcs/tree/master/text) this quarter:

- Purge Private Data

Other [RFCs are in review](https://github.com/hyperledger/fabric-rfcs/pulls) with recent discussions surrounding SmartBFT, OpenTelemetry tracing, and module crypto service.

Finally, new project samples have been added to help users get up to speed and deploy Fabric:

- Asset transfer samples with new Gateway SDK - [https](https://hyperledger-fabric.readthedocs.io/en/latest/write_first_app.html)[://hyperledger-fabric.readthedocs.io/en/latest/write\_first\_app.](https://hyperledger-fabric.readthedocs.io/en/latest/write_first_app.html)[html](https://hyperledger-fabric.readthedocs.io/en/latest/write_first_app.html)
- Advanced REST sample demonstrating good practices for interacting with a Fabric network - [https](https://github.com/hyperledger/fabric-samples/tree/main/asset-transfer-basic/rest-api-typescript)[://github.com/hyperledger/fabric-samples/tree/main/asset-transfer-basic/](https://github.com/hyperledger/fabric-samples/tree/main/asset-transfer-basic/rest-api-typescript)[rest-api-typescript](https://github.com/hyperledger/fabric-samples/tree/main/asset-transfer-basic/rest-api-typescript)
- Kubernetes Test Network - [https://github.com/hyperledger/fabric-samples/tree/main/test-network-k8s](https://github.com/hyperledger/fabric-samples/tree/main/test-network-k8s)

# Current Plans

**Releases**

The project is working on a v2.5.0 release with a feature to Purge the history of private data. The feature may help organizations meet GDPR requirements with the ability to delete private data while preserving a hash of the data on the blockchain.

Discussion about a future Fabric v3.0 release was kicked off at the January 5th contributor meeting. The proposal is to refactor some Fabric components so that new features can be more easily added on top, most notably a proposed BFT ordering service. For more details see the recording at [Contributor Meetings 2022](https://lf-hyperledger.atlassian.net/wiki/spaces/fabric/pages/22839810/Contributor+Meetings+2022).

**Documentation**

We plan to resume the Fabric community documentation meetings and update Fabric documentation in the following areas:

- Developing Applications with new Gateway SDKs
- Certificate management (expirations, renewals)

**Performance**

Update Caliper client for Fabric.

# Maintainer Diversity

No changes. 6 of 11 maintainers of core Fabric from IBM.

# Contributor Diversity

Year to year comparison, by commit:

- Q4 2020 - 674 commits. 71% from IBM.
- Q4 2021 - 361 commits. 80% from IBM

Year to year comparison, by contributor:

- Q4 2020 - 94 contributors. 38% from IBM.
- Q4 2021 - 45 contributors. 42% from IBM.

# Additional Information

Link to the Fabric dashboard: [Q4 2021](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffabric/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-10-01T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-01-01T04%3A00%3A00.000Z%22%7D)

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
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
