1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q1 Hyperledger Besu

Created by Danno Ferrin, last modified by Bobbi Muscara on Apr 06, 2022

Project Health

Hyperledger Besu remains a strong project with a growing community network of contributors. This quarter the team has passed a major milestone for the Ethereum Mainnet "merge" update as well as supporting the Ethereum Classic Mystique Hard Fork.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? - Yes
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? - Yes
3. Has your project implemented these inclusive language changes listed below to your repo? - Yes
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? - Yes ([Point 5](https://lf-hyperledger.atlassian.net/wiki/spaces/BESU/pages/22154271/Documentation+style+guide))
   

# Questions/Issues for the TSC

None at this time

# Releases

- 21.10.5 - 19 Dec 2021
- 21.10.6 -  4 Jan 2022
- 22.1.0-RC2 - 6 Jan 2022
- 21.0.7 - 13 Jan 2022
- 21.0.8 - 16 Jan 2022
- 21.0.9 - 19 Jan 2022
- 22.1.0-RC3 - 25 Jan 2022
- 22.1.0-RC4 - 30 Jan 2022
- 22.1.0 - 16 Feb 2022
- 22.1.1 - 24 Feb 2022
- 22.1.2 - 15 Mar 2022

More releases occurred than typical for the 22.10.x cycle because an ETC hard fork occurred during the 22.1.x release cycle, some fixes related to merge testing, and one regression.

# Overall Activity in the Past Quarter

- **Mainnet Paris Upgrade**
  
  Previously known as "the merge" a critical test event known as "kiln testnet" successfully occurred, with Besu fully participating.
  
  Key areas include synchronization and consensus layer communication APIs.
- **QBFT**
  
  Marked as production ready
- **EVM Library**
  
  Investigated removing the "Gas" object to reduce short lived object garbage collection.
- **Tracing**
  
  Exposed new tracing methods and added revert reason to traces.

# Current Plans

- **Migration to Java 17**
  
  In the 22.7.x cycle Besu will move to Java 17 as the required JVM.
- **Paris Upgrade**
  
  Paris will ship when it's ready, but final preparations are at hand.
- **Shanghai Fork**
  
  The first fork after The Merge is expected to add some long overdue EVM improvements, such as the Ethereum Object Format.
- **Developer experience**
  
  Planning to add a work stream to specifically focus on developer experience, allowing prioritization of issues alongside feature work.

# Maintainer Diversity

One maintainer was moved to Emeritus status this quarter (Vijay Michalik), reducing the non-consensys maintainer share to 17.8% (5 of 28).

Corporate distribution is unchanged from the last quarters report (ConsenSys, Splunk, Hedera, ETC Co-operative)

# Contributor Diversity

[LFX Insights Report](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fbesu/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-12-16T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-03-24T06%3A00%3A00.000Z%22%7D)  

# Additional Information

Hyperledger, the Ethereum Foundation, and ConsenSys are still working through the final agreements and documentation for the Client Incentive Program. But, in this quarter, the community agreed on following Proposal #4 for setting up the program.

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
