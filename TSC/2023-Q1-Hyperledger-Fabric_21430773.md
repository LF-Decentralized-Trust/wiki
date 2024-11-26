1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2023 Project Updates](2023-Project-Updates_21445803.html)

# Technical Oversight Committee : 2023 Q1 Hyperledger Fabric

Created by David Enyeart, last modified by Bobbi Muscara on Jan 25, 2023

  

Project Health

Hyperledger Fabric is fairly mature and stable with a Long-term support (LTS) release and incremental new features being added in minor releases. There is less churn and fewer commits than in years past, with continued focus on quality and support. New features get proposed, approved, and implemented based on a community RFC process. Mailing list activity is down a bit compared to prior years. PRs and mailing list questions are generally turned around quickly.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes
3. Has your project implemented these inclusive language changes listed below to your repo? You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo. Yes
   
   1. master → main
   2. slave → replicas
   3. blacklist → denylist
   4. whitelist → allowlist
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? Yes
   

# Questions/Issues for the TSC

None.

# Releases

v2.2 is the current LTS releases with patch releases approximately quarterly.

Releases past quarter:

- Fabric v2.2.9 - October 25, 2022
- Fabric v2.4.7 - October 25, 2022
- Fabric v2.5.0-alpha3 - December 21, 2022

Fabric CA

- Fabric CA v1.5.6-beta3 - January 3, 2023

Fabric v2.5.0-alpha3 and Fabric CA v1.5.6-beta3 pre-releases were created so that the community can try the new ARM support in the binaries and images. This is more important these days given the rising prevalence of Mac M1 ARM architecture in the developer community.

Upcoming releases:

- Fabric v2.5.0 - Expected to be next LTS release

# Overall Activity in the Past Quarter

The project delivered fixes to the Fabric v2.2 (current LTS) and v2.4 (latest) releases.

The Purge Private Data History feature has been implemented with plan to release in Fabric v2.5 in Q1.

ARM support was added for Fabric binaries and images and made available in pre-releases v2.5.0-alpha3 and Fabric v1.5.6-beta3.

SmartBFT consensus algorithm is being integrated into the Fabric ordering service for an eventual Fabric v3.0 release.

An RFC was merged, and development started, to create a [fabric-admin-sdk](https://github.com/hyperledger/fabric-admin-sdk) seeded from Technical Working Group China that will help with programatic channel and chaincode management. Targeting a Go SDK first.

The Fabric workshop created for Global Forum has been merged into [fabric-samples](https://github.com/hyperledger/fabric-samples/tree/main/full-stack-asset-transfer-guide).

New lab created - [microfab](https://github.com/hyperledger-labs/microfab) - a single container Fabric environment intended to accelerate application and chaincode development, and used in the workshop mentioned above.

Additional Fabric repositories have shifted CI from Azure Pipelines to Github Actions.

# Current Plans

The project is working on a v2.5.0 release in the release-2.5 branch, with a feature to Purge the history of private data. The feature may help organizations meet GDPR requirements with the ability to delete private data while preserving a hash of the data on the blockchain. The v2.5 release is expected early 2023 and is expected to become the next long-term support (LTS) release. 

Fabric v3.0 release development has started, primarily around refactoring the ordering service for the upcoming BFT consensus integration. In the v3.0 release we are considering deprecation and removal of some features that have historically made deployment difficult, such as docker-in-docker chaincode building.

# Maintainer Diversity

6 of 8 maintainers from IBM.

# Contributor Diversity

Year to year comparison, by commit:

- Q4 2021 - 361 commits. 80% from IBM.
- Q4 2022 - 382 commits. 80% from IBM.

Year to year comparison, by contributor:

- Q4 2021 - 45 contributors. 42% from IBM.
- Q4 2022 - 40 contributors. 38% from IBM.

# Additional Information

[Insights dashboard link](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffabric/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-10-01T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222023-01-01T05%3A00%3A00.000Z%22%7D)

# Reviewed By

- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [Marcus Brandenburger](https://lf-hyperledger.atlassian.net/wiki/people/5d6cd4bb3803ee0db6cedaaf?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Venkatraman Ramakrishna](https://lf-hyperledger.atlassian.net/wiki/people/6124c28b45f75300691e9f16?ref=confluence)

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
