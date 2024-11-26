1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q3 Hyperledger Transact

Created by Andi Gunderson, last modified by David Enyeart on Sep 22, 2022

Hyperledger Transact - [https://github.com/hyperledger/transact](https://github.com/hyperledger/transact)

Project Health

Health is good. In the last quarter there was one release. This release includes a number of fixes to the stability of the SQL-backed merkle state implementation, including stable behavior of the merkle tree after state pruning has been applied.  It also includes changes to support using the SQL-backed merkle state in the context of a wider transaction.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
   
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes
   
3. Has your project implemented these inclusive language changes listed below to your repo? You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo.
   
   1. master → main Yes
   2. slave → replicas N/A
   3. blacklist → denylist N/A
   4. whitelist → allowlist Yes
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? The statement has not been added.
   

# Questions/Issues for the TSC

No issues currently.

# Releases

Since project creation, the project has had 33 releases. The current release is 0.4.6. The releases are available on [crates.io](http://crates.io): [https://crates.io/crates/transact/versions](https://crates.io/crates/transact/versions)

# Overall Activity in the Past Quarter

Continued incremental improvements to the initial code base. Additional activity shown below. The primary method of discussion has been moved to Discord.

Additional work:

- Fix state pruning when using SqlMerkleState
- Allow the use of SqlMerkleState with-in existing transactions
- Stabilize the "state-merkle-sql-in-transaction" feature by removing it
- Make updates necessary for the eventual stabilization of the "playlist-smallbank" feature

# Current Plans

The Transact team is investigating merging libtransact into sawtooth-lib in order to simplify the overall dependency tree. sawtooth-lib did not exist when the Transact project was created, but might now be a good fit.

Future:

- Re-evaluate threading model for batch scheduling and execution
- Setup a documentation site to help explain/advocate the project
- Add a next-generation smart contract API / simplified smart contracts (cross-project with Sawtooth, in progress)
- Further develop the Transact SDK for JavaScript

# Maintainer Diversity

Maintainers are the same as the previous quarter. Maintainers are currently:

**Name**

**GitHub**

Andi Gunderson

agunde406

Isabel Tomb

isabeltomb

James Mitchell

jsmitchell

Logan Seeley

ltseeley

Peter Schwarz

peterschwarz

Richard Berg

rberg2

Ryan Beck-Buysse

rbuysse

Ryan Banks

ryanlassigbanks

Shannyn Telander

shannynalayna

Shawn Amundson

vaporos

# Contributor Diversity

There were a total of 5 contributors in the last quarter.

# Additional Information

Insights from May 23rd 2022 to August 25th 2022

[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ftransact/dashboard;subTab=technical?time=%7B%22from%22:%222022-05-23T05:00:00.000Z%22,%22type%22:%22absolute%22,%22to%22:%222022-08-25T05:00:00.000Z%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ftransact/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-05-23T05%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-08-25T05%3A00%3A00.000Z%22%7D)

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
