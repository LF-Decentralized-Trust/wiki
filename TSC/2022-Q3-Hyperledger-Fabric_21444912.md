1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q3 Hyperledger Fabric

Created by David Enyeart, last modified on Jul 21, 2022

Project Health

Hyperledger Fabric is fairly mature and stable with a Long-term support (LTS) release and incremental new features being added in minor releases. There is less churn and fewer commits than in years past, with continued focus on quality and support. New features get proposed, approved, and implemented based on a community RFC process. Mailing list activity is down compared to prior years. PRs and mailing list questions are generally turned around quickly.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? YES
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? YES
3. Has your project implemented these inclusive language changes listed below to your repo? YES You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo.
   
   1. master → main
   2. slave → replicas
   3. blacklist → denylist
   4. whitelist → allowlist
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? YES
   

# Questions/Issues for the TSC

None.

# Releases

v2.2 is the current LTS releases with patch releases approximately quarterly.

Releases past quarter:

- Fabric v2.2.6 - June 17, 2022
- Fabric v2.2.7 - July 1, 2022
- Fabric v2.4.4 - June 17, 2022
- Fabric v2.4.5 - July 1, 2022

Fabric CA

- v1.5.4 - June 17, 2022

Fabric Gateway SDKs

- v1.1 - June 30, 2022 - Brings functional parity relative to the legacy (deprecated) SDKs.

Additionally, legacy SDKs are regularly patched.

Upcoming releases:

- Fabric v2.5.0 - Expected to be next LTS release

# Overall Activity in the Past Quarter

The project delivered fixes to the Fabric v2.2 and v2.4 releases, as well as Fabric CA v1.5 release. The latest Fabric and Fabric CA releases were updated to utilize Go 1.18.

Work is underway to implement the Purge Private Data History feature, targeted for v2.5 later this year. Additionally for v2.5 many project dependencies were updated including a somewhat invasive update in the ordering service for etcd and protobuf.

The new Gateway SDKs were updated to support checkpointing for chaincode events, block events, and off-line signing so that they will have parity with the legacy (deprecated) SDKs, enabling existing users to move up to the new Gateway SDKs that simplify application logic.

[RFCs merged](https://github.com/hyperledger/fabric-rfcs/tree/master/text) this quarter:

- [Ordering service refactor for BFT support](https://github.com/hyperledger/fabric-rfcs/blob/main/text/orderer-v3.md)

**Related Projects**

- **Caliper** project was updated to utilize the Fabric Gateway SDK along with general updates, released as Caliper v0.5.
- **Fabric-operator** - IBM contributed the kubernetes operator that powers IBM Blockchain Platform as a Hyperledger lab - [https://github.com/hyperledger-labs/fabric-operator](https://github.com/hyperledger-labs/fabric-operator). The intent is to socialize with the community this quarter and determine if this lab can help to coalesce the various Fabric deployment solutions that have been made available over the last couple years.

# Current Plans

The project is working on a v2.5.0 release with a feature to Purge the history of private data. The feature may help organizations meet GDPR requirements with the ability to delete private data while preserving a hash of the data on the blockchain. The v2.5 release is expected to become the next long-term support release. 

Fabric v3.0 release was kicked off with the merge of the ordering service refactor RFC. The refactor is underway and will enable the addition of BFT consensus algorithms with intent to integrate SmartBFT initially.

The project is working on a workshop that will help users with Fabric deployment and application development, with initial workshop delivery at Hyperledger Global Forum.

# Maintainer Diversity

6 of 8 maintainers from IBM.

# Contributor Diversity

Year to year comparison, by commit:

- Q2 2021 - 403 commits. 61% from IBM.
- Q2 2022 - 319 commits. 59% from IBM

Year to year comparison, by contributor:

- Q2 2021 - 74 contributors. 32% from IBM.
- Q2 2022 - 54 contributors. 31% from IBM.

# Additional Information

[Insights dashboard for Q2](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffabric/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-04-01T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-07-01T03%3A00%3A00.000Z%22%7D).

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
