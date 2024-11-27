1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)
5. [Extend existing Iroha - Cactus integration](Extend-existing-Iroha---Cactus-integration_21954791.html)

# Hyperledger Mentorship Program : Project Plan - Extend existing Iroha - Cactus integration

Created by Yashraj Desai, last modified by baziorek on Nov 19, 2022

# Overview

The project's primary goal is to extend the integration of Iroha and Cactus (Iroha version at least 1.4) and make the connector plugin configurable. It also includes end-to-end testing and documentation of the Cactus-Iroha connector plugin.

## Mentor and Mentee

Mentor

Mentor

Mentee

Peter Somogyvari

PDT (UTC-7)

[peter.somogyvari@accenture.com](mailto:peter.somogyvari@accenture.com)

Grzegorz Baz

CEST (UTC+2)

[g.bazior@yodiss.pl](mailto:g.bazior@yodiss.pl)

Yashraj Desai

IST (UTC+05:30)

[yashrajdesai30@gmail.com](mailto:yashrajdesai30@gmail.com)

Communication channel: RocketChat/ Public Channels/ Emails/ Microsoft Teams

**Project repository:** 

[https://github.com/yashrajdesai/iroha-javascript/tree/main](https://github.com/yashrajdesai/iroha-javascript/tree/main)

[https://github.com/yashrajdesai/cactus](https://github.com/yashrajdesai/cactus)

**Project pull requests:** 

[https://github.com/hyperledger/iroha-javascript/pull/110](https://github.com/hyperledger/iroha-javascript/pull/110)

[https://github.com/hyperledger/cactus/pull/2148](https://github.com/hyperledger/cactus/pull/2148)

[https://github.com/hyperledger/iroha-javascript/pull/125](https://github.com/hyperledger/iroha-javascript/pull/125)

[https://github.com/hyperledger/cactus/pull/2166](https://github.com/hyperledger/cactus/pull/2166)

[https://github.com/hyperledger/cactus/pull/2202](https://github.com/hyperledger/cactus/pull/2202)

# Project Plan

**Schedule**

**Task/Plan**

Week 1 - Week 2

Jun 1 - Jun 18

- Mentee intro with the mentor.
- Introduction to the concepts of Hyperledger Iroha.
- Attend on-board meeting
- Build and run Hyperledger Iroha node (Irohad) and Catus.
- Send sample commands and queries via Iroha-CLI and Iroha-javascript.
- Understand the architecture and test the Cactus-Iroha plugin.

Week 3 - Week 6

Jun 19 - July 9

- Implement missing features of the Cactus-Iroha plugin.
- Test and document missing features of the Cactus-Iroha plugin.

Week 6 - Week 10

July 10 - July 30

- Implement missing features of the Cactus-Iroha plugin.
- Make the plugin configurable.
- Testing and documentation of the plugin.

Week 10

July 31 - Aug 10

**Aug 20-31: Midterm Evaluation**

- Add dynamic request parameters for the cactus-iroha plugin.
- Discuss and create priority list of future objectives with mentors.

Week 11 - Week 15

Aug 9 - 10 Sept

- Generate ts files from the latest iroha proto files.
- Test all iroha commands and queries in the iroha-javascript client.

Week 16 - Week 20

11 Sept - 9 Oct

- Update the iroha-javascript library in the iroha-cactus plugin.
- Implement TLS encryption in cactus-iroha plugin.

Week 21 - Week 25

10 Oct - 18 Nov

**Nov 18: Final Evaluation**

- Documentation of how to integrate multiple (two and more) Iroha's networks with Cactus
- Prepare final project report.
- Present changes to Iroha and Cactus communities ([link](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=21013325))

# Timeline

Week

Task

**1 (Jun 1 - Jun 6)**

- Mentee intro with the mentor.
- Introduction to the concepts of Hyperledger Iroha.
- Built Cactus

**2 (Jun 7 - Jun 13)**

- Attend on-board meeting
- Build and run Hyperledger Iroha node (Irohad).
- Send sample commands and queries via Iroha-CLI and Iroha-javascript.

**3 (Jun 14 - Jun 20)**

- Report issues in the Cactus-Iroha-connector plugin
- Discuss issues with mentors.
- Fix issues in the Cactus-Iroha-connector plugin.

**4 (Jun 21- Jun 27)**

- Discussed TLS encryption objective with mentors.
- Enabled TLS encryption in the Iroha server.
- Researched client-side encryption for the Iroha-javascript library.

**5 (Jun 28- July 4)**

- Completed and tested client-side TLS encryption for the Iroha-javascript library.
- Implemented and tested fetchCommits in the Iroha-javascript library.
- Tested commands and queries using smart contracts from the Iroha-python library.

**6 (July 5 - July 11)**

- Implemented queries and commands using smart contracts in the Iroha-javascript library.
- Tested smart contracts in the Iroha-javascript library.
- Discussed future objectives with mentors.
- Created [PR #110](https://github.com/hyperledger/iroha-javascript/pull/110) to add a sample for smart contracts to the iroha-javascript library.

**7 (July 12 - July 18)**

- Updated [PR #110](https://github.com/hyperledger/iroha-javascript/pull/110) according to mentors' suggestions.
- Tested compareAndSetAccount detail query.
- Tested gRPC health check.

**8 (July 19 - July 25)**

- Researched and studied proto files and compilation of proto files to generate TS files.
- Started TLS integration with the Iroha-Cactus integration plugin.
- Started compilation of latest proto files to update the Iroha-javascript library.
- Researched various LFX docker training.

**9 (July 26 - Aug 1)**

- Added TLS encryption in the cactus-iroha plugin.
- Started writing tests for TLS encryption.
- Made final changes in [PR #110](https://github.com/hyperledger/iroha-javascript/pull/110) and got it merged.

**10 (Aug 2 - Aug 8)**

- Discussed future internship objectives with mentors.
- Discussed and partially completed implementation of [# 1253](https://github.com/hyperledger/cactus/issues/1253)
- Completed initial chapters of docker training.

**11 (Aug 9 - Aug 15)**

- Completed implementation of [# 1253](https://github.com/hyperledger/cactus/issues/1253) and created [PR #2148](https://github.com/hyperledger/cactus/pull/2148)
- Generated ts files from the latest proto files.

**12 - 13 (Aug 16 - Aug 28)**

- Planned future objectives with mentors.
- Updated [PR #2148](https://github.com/hyperledger/cactus/pull/2148) according to mentors' suggestions.

**14 - 15 (Aug 29 - 10 Sept)**

- Tested the latest proto files from the Iroha-javascript library.

**16 - 17 (Sept 11 - Sept 24)**

- Created [PR #125](https://github.com/hyperledger/iroha-javascript/pull/125) to update the iroha-javascript library with the latest Iroha (1.5.0) proto files.

**18 - 19 (Sept 25 - Oct 9)**

- Tested latest iroha-javascript library in the iroha-cactus plugin.
- Created [PR #2166](https://github.com/hyperledger/cactus/pull/2166) to update the iroha-javascript library in the iroha-cactus plugin.

**20 - 21 (Oct 10 - Oct 23)**

- Discussed improvements in [PR #125](https://github.com/hyperledger/iroha-javascript/pull/125) with mentors.
- Made final changes in [PR #2148](https://github.com/hyperledger/cactus/pull/2148) and got it merged.

**22 - 25 (Oct 24 - Nov 18)**

- Updated [PR #2166](https://github.com/hyperledger/cactus/pull/2166) according to mentors' suggestions.
- Discussed TLS Encryption integration in cactus-iroha plugin [# 1251](https://github.com/hyperledger/cactus/issues/1251) with mentors.
- Created draft [PR #2202](https://github.com/hyperledger/cactus/pull/2202) to add TLS encryption in cactus-iroha plugin.
- Created final report and presentation ([link](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=21013325))

# Process

- Communication and updates:
- - RocketChat/ Public Channels/ Emails/ Microsoft Teams are used as tools.
  - Weekly check-in meetings between mentors and the mentee.

# Recommendations for future work:

CategoryIndexCurrent implementation and issueExpected improvementsDifficulty level \*Priority \*Github IssueIroha connector plugin

1

gRPC TLS option is not implemented.

Currently, only able to generate and pass in TLS parameters( TLS Cert/ TLS Key/ TLS Port) to iroha test ledger, but those parameters are immediately discarded.

Implement gRPC TLS support for Iroha test ledger.

(Refer to [Cactus PR #1190](https://github.com/hyperledger/cactus/pull/1190) and [Cactus PR #2202](https://github.com/hyperledger/cactus/pull/2202))

3/51[Link](https://github.com/hyperledger/cactus/issues/1251)2

**fetchCommits** is not implemented. 

It is inside the plugin-ledger-connector-iroha.ts, but unable to test it due to its unique characteristic of streaming responses.

**fetchCommits** could be implemented as something similar to Besu connector's [WatchBlockV1](https://github.com/hyperledger/cactus/blob/main/packages/cactus-plugin-ledger-connector-besu/src/main/typescript/web-services/watch-blocks-v1-endpoint.ts).3/52[Link](https://github.com/hyperledger/cactus/issues/1254)

3

Test smart contracts by using Call Engine command for the Iroha-Cactus connector.

Implement InvokeContractV1 for Iroha connector once Iroha fully support smart contract. (Refer: [Iroha-javascript PR #110](https://github.com/hyperledger/iroha-javascript/pull/110))

3/5

3

[Link](https://github.com/hyperledger/cactus/issues/1255)

[Link](https://github.com/hyperledger/cactus/issues/1256)

4

**setSettingValue** is not implemented because this command can only be called inside genesis.block file.

(Current connector implementation returns HTTP 405 Error in plugin-ledger-connector-iroha.ts)

When Iroha is able to run **SetSettingValue** outside of genesis.block, implement and test it.

(It is being said that the Iroha team plans to support running **SetSettingValue** outside of genesis.block.)

2/55[Link](https://github.com/hyperledger/cactus/issues/1257)5

**removePeer** is not fully tested. 

A valid Iroha testnet needs to be constructed to test **removePeer**.

Able to manipulate Iroha testnet ( An Iroha testnet usually composes of &gt;= 3 Iroha nodes).

Then, construct Iroha test within the test case to test **removePeer**.

4/54[Link](https://github.com/hyperledger/cactus/issues/1258)

6

**getPendingTransaction** is not fully tested.

There is an issue with producing a pending transaction: the code will get stuck and fail the test suite. It seems like Iroha ledger itself is struggling to generate the pending transaction. ([https://jira.hyperledger.org/browse/IR-1010](https://jira.hyperledger.org/browse/IR-1010)) In other words, it seems to be an issue with Iroha ledger itself instead of the Iroha Javascript library.

Able to produce a pending transaction in the test case.

Able to validate the pending transaction via **getPendingTrasaction** query.

4/54[Link](https://github.com/hyperledger/cactus/issues/1259)7

Prometheus exporter metrics integration is not implemented.

Add prometheus exporter to the Iroha connector plugin.

2/54[Link](https://github.com/hyperledger/cactus/issues/1260)Iroha docker container1

An Iroha Python SDK is embedded inside the Iroha AIO docker image for docker healthcheck. Although this healthcheck mechanism works fine, it makes the docker image ~100MB larger. 

Once the Iroha team introduces the gRPC healthcheck/ Iroha metrics page in a stable release (e.g., v1.2.2), implement healthcheck mechanism through gRPC healthcheck or curl the metric page.   
\`curl [http://127.0.0.1:8080/metrics](http://127.0.0.1:8080/metrics)\`2/54[Link](https://github.com/hyperledger/cactus/issues/1263)2Each Iroha docker container relies on a corresponding Postgres database container to store information. Replace the Postgres database docker container with RocksDB, which needs just one folder ( a docker volume) to keep data between different runs of image.3/54[Link](https://github.com/hyperledger/cactus/issues/1264)

\*For the difficulty level, 1 means the easiest, 5 means the most challenging.

\*For the priority listing, 1 means the most important, 5 means the least important. Important ones have been marked as red.

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
