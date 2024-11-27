1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [HL Iroha and HL Cactus Integration](HL-Iroha-and-HL-Cactus-Integration_21954723.html)

# Hyperledger Mentorship Program : Project Plan - HL Iroha and HL Cactus Integration

Created by Han Xu, last modified by baziorek on Aug 30, 2021

# Overview

The main goal of the project is to create a documented Iroha (1.x) package for the Cactus project, which demonstrates the interoperability between Iroha and Cactus. The project also includes 1 documented examples of integration between Iroha and Cactus. The documentation will benefit the community so that people can understand this project.

## Mentor and Mentee

MentorMentorMentee

Peter Somogyvari

PDT (UTC-7)

[peter.somogyvari@accenture.com](mailto:peter.somogyvari@accenture.com)

Grzegorz Baz

CEST (UTC+2)

[g.bazior@yodiss.pl](mailto:g.bazior@yodiss.pl)

Han Xu

EST (UTC-5)

[hongkexuhan@gmail.com](mailto:hongkexuhan@gmail.com)

Communication channel: Telegram/ RocketChat/ Public Channels/ Emails/ Microsoft Teams

**Project repository:** 

[https://github.com/hyperledger/cactus](https://github.com/hyperledger/cactus) (main)

[https://github.com/hyperledger/iroha](https://github.com/hyperledger/iroha)

**Project pull requests:**

[https://github.com/hyperledger/cactus/pull/1183](https://github.com/hyperledger/cactus/pull/1183)

[https://github.com/hyperledger/cactus/pull/1169](https://github.com/hyperledger/cactus/pull/1169) 

**Practical presentation of completed project (not the same presentation as [on project site](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/HL+Iroha+and+HL+Cactus+Integration)) - how to use result of the internship:**

[![](attachments/thumbnails/21954749/21965620)](attachments/21954749/21965620.pdf)

# Project Plan

**Schedule**

**Task**

**Deliverable**

Week 1 - Week 3

Jun 1 - Jun 18

**Jun 18: 1st Quarter Evaluation**

- Install Ubuntu 20.04 LTS and set up environment.
- Build Cactus.
- Build Iroha.
- Understand existing source code.
- Start the Iroha and Cactus integration.

<!--THE END-->

- Project Plan.
- Skeleton for Iroha and Cactus integration.

Week 3 - Week 6

Jun 19 - July 9

**July 9: Midterm Quarter Evaluation**

- Implement the Iroha and Cactus integration.
- Write tests for the Iroha and Cactus integration.
- Write documentation.

<!--THE END-->

- ~50% of the Iroha and Cactus integration package.
- Technical documentation for the package.

Week 6 - Week 10

July 10 - July 30

**July 30: 3rd Quarter Evaluation**

- Write tests for Iroha and Cactus integration.
- Write documentation.

<!--THE END-->

- Completed package for Iroha and Cactus integration.

Week 10

July 31 - Aug 10

**Aug 20-31: Final Evaluation**

- Wrap up documentation.
- Final report of the project.
- Final presentation of the project

<!--THE END-->

- Code for unit tests and integration tests. *
- Technical documentation for the entire project.
- Final report.
- Final presentation.
- 1 example of Iroha and Cactus integration. (Nice-to-have)
- 2 examples of Iroha and Cactus integration. (Optional)
- 2 examples of Iroha and Fabric integration. (Optional)

\* Will wrap up all codes-relevant stuff by Aug 5.

# Timeline

Week

Task

Weekly Slide

**1 (Jun 1 - Jun 6)**

- Attend onboard meeting
- Attend 6/4 Iroha community meeting
- Read the project wiki page

[W1 Slide.pdf](attachments/21954749/21964794.pdf)

**2 (Jun 7 - Jun 13)**

- Install Ubuntu 20.04 LTS
- Set up environment
- Build Cactus
- Build Iroha
- Project Plan

[W2 Slide.pdf](attachments/21954749/21964841.pdf)

**3 (Jun 14 - Jun 20)**

- Skeleton code for Iroha and Cactus Integration
- Learn Typescript via Udemy course

[W3 Slide.pdf](attachments/21954749/21964840.pdf)

**4 (Jun 21- Jun 27)**

- Finished the Typescript Udemy course
- Stripped out files and functions for Iroha plugin
- Worked on current Tx test
- Tried to compile the package

[W4 Slide.pdf](attachments/21954749/21965006.pdf)

**5 (Jun 28- July 4)**

- Made sure the project compiles
- Used dockerode to run Iroha+Postgres docker image properly
- Modified based on v1.2.0 Iroha Docker image; posted on DockerHub
- Tried to run Iroha’s JS library

[W5 Slide.pdf](attachments/21954749/21965010.pdf)

**6 (July 5 - July 11)**

- Inquired Iroha community about Iroha docker health check + Iroha JS library response
- Switched to Iroha’s TS library, got output from all commands/queries
- Rewrote Cactus’s connector to manipulate Iroha’s TS library (able to pass commands and queries and get back response)
- Tried almost all Iroha’s commands+queries. (a shared Google Sheet is used to track the progress)
- Redesigned test cases, pushed to Github.

[W6 Slide.pdf](attachments/21954749/21965054.pdf)

**7 (July 12 - July 18)**

- Switched from connector to apiClient to run transactions for everything
- Progress: Commands -&gt; 14/20; Queries -&gt; 12/15; in total: 26/35 (~74%)
- Made code cleaner (used enum for Iroha commands/queries)

[W7 Slide.pdf](attachments/21954749/21965192.pdf)

**8 (July 19 - July 25)**

- Implementation progress: Iroha commands -&gt; 19/20; Iroha queries -&gt; 14/15; in total: 33/35 (~94%)
- Working on rebasing
- Took a look at the Iroha Testnet

[W8 Slide.pdf](http://lf-hyperledger.atlassian.net)**9 (July 26 - Aug 1)**

- Finished rebasing
- Drafted pull request with Peter; fixed most feedback from Peter (11/12)
- Finished my own Dockerfile; shrinked the size to 120MB; 85% improvement (thanks to help from Iroha community and Greg)
- Delivered presentation to the Iroha community this morning
- Explored the issue behind grpc error “GOAWAY unavailable” (get pending transaction)

[W9 Slide.pdf](attachments/21954749/21965507.pdf)

**10 (Aug 2 - Aug 8)**

- Responded to all feedback from Peter for my [2nd PR](https://github.com/hyperledger/cactus/pull/1183)
- Look into the pending transaction issue

[W10 Slide.pdf](attachments/21954749/21965509.pdf)

**11 (Aug 9 - Aug 15)**

- Finished Iroha-Iroha transfer example (including passing randomly generated admin/node key pairs)
- Finished the irohaBaseConfig interface for the request
- Tweaked Iroha docker healthcheck via Python SDK
- Tried best to remove magical strings (e.g., changing the strings to enum; randomly generate admin/node key pairs; uuidv4())
- Responded to most of the feedback

[W11 Slide.pdf](attachments/21954749/21965510.pdf)

**12 (Aug 16 - Aug 20)**

- Fixed the crash issue with Iroha-Iroha transfer example (will not crash if pass in no
  
  parameter)
- Updated comments and documentation (e.g., [readme.md](http://readme.md))
- Removed magical strings for all files; responded to all PR feedback
- Completed the “Recommendations for future work” list
- Added tls:boolean option inside the baseConfig interface (tls is not implemented)

[W12 Slide.pdf](attachments/21954749/21965511.pdf)

# Process

- Communication and updates:
- - Telegram/ RocketChat/ Public Channels/ Emails/ Microsoft Teams are used as tools.
  - Weekly check-in meetings between mentors and the mentee.

<!--THE END-->

- Quarterly evaluations on Jun 18/ July 9/ July 30/ Aug 20.

# Recommendations for future work:

CategoryIndexCurrent implementation and issueExpected improvementsDifficulty level \*Priority \*Github IssueIroha connector plugin

1

gRPC TLS option is not implemented.

Currently, only able to pass in TLS parameters( TLS Cert/ TLS Key/ TLS Port) to iroha test ledger, but those parameters are immediately discarded.

Implement gRPC TLS support for Iroha test ledger.

(Refer to [Cactus PR #1190](https://github.com/hyperledger/cactus/pull/1190) as an example. )

3/51[Link](https://github.com/hyperledger/cactus/issues/1251)

2

Currently the parameters are hardcoded ( i.e., we can only support new parameters if we recompile the code of the connector and then publish a brand new release of it.) Parameters should be more generic in the future so that parameter changes can be done dynamically.3/52[Link](https://github.com/hyperledger/cactus/issues/1253)3

**fetchCommits** is not implemented. 

It is inside the plugin-ledger-connector-iroha.ts, but unable to test it due to its unique characteristic of streaming responses.

**fetchCommits** could be implemented as something similar to Besu connector's [WatchBlockV1](https://github.com/hyperledger/cactus/blob/main/packages/cactus-plugin-ledger-connector-besu/src/main/typescript/web-services/watch-blocks-v1-endpoint.ts).3/54[Link](https://github.com/hyperledger/cactus/issues/1254)

4

4a. There is no implementation for smart contract.

4b. InvokeContractV1 is not implemented due to the lack of smart contract.

4c. **Call Engine** is not implemented. (because Call Engine calls smart contract)

For Call Engine, we intentionally reject the transaction within the ledger, and then validate the rejection in the test case. 

4a. Implement smart contract once Iroha fully supports smart contract.

4b. Implement InvokeContractV1 for Iroha connector once Iroha fully support smart contract.

4c. Given smart contract is supported by Iroha, implement **Call Engine** and test it.

3/5

5 ( will be important once Iroha fully supports smart contract)

[Link](https://github.com/hyperledger/cactus/issues/1255)

[Link](https://github.com/hyperledger/cactus/issues/1256)

5

**setSettingValue** is not implemented because this command can only be called inside genesis.block file.

(Current connector implementation returns HTTP 405 Error in plugin-ledger-connector-iroha.ts)

When Iroha is able to run **SetSettingValue** outside of genesis.block, implement and test it.

(It is being said that the Iroha team plans to support running **SetSettingValue** outside of genesis.block.)

2/57[Link](https://github.com/hyperledger/cactus/issues/1257)6

**removePeer** is not fully tested. 

A valid Iroha testnet needs to be constructed to test **removePeer**.

Able to manipulate Iroha testnet ( An Iroha testnet usually composes of &gt;= 3 Iroha nodes).

Then, construct Iroha test within the test case to test **removePeer**.

4/56[Link](https://github.com/hyperledger/cactus/issues/1258)

7

**getPendingTransaction** is not fully tested.

There is an issue with producing a pending transaction: the code will get stuck and fail the test suite. It seems like Iroha ledger itself is struggling to generate the pending transaction. ([https://jira.hyperledger.org/browse/IR-1010](https://jira.hyperledger.org/browse/IR-1010)) In other words, it seems to be an issue with Iroha ledger itself instead of the Iroha Javascript library.

Able to produce a pending transaction in the test case.

Able to validate the pending transaction via **getPendingTrasaction** query.

4/56[Link](https://github.com/hyperledger/cactus/issues/1259)8

Prometheus exporter metrics integration is not implemented.

Add prometheus exporter to the Iroha connector plugin.

2/56[Link](https://github.com/hyperledger/cactus/issues/1260)Iroha-Javascript library1

1a. Utilized [iroha-helpers-ts](https://www.npmjs.com/package/iroha-helpers-ts) since the original [Iroha Javascript library](https://github.com/hyperledger/iroha-javascript) gives “undefined” as output. 

However, [iroha-helper-ts](https://www.npmjs.com/package/iroha-helpers-ts) is based on an old Iroha Javascript library (12/23/2020 release), which does not support some new features.

1b. Due to this, currently, [one argument for compareAndSetAccountDetail, check\_empty](https://iroha.readthedocs.io/en/main/develop/api/commands.html#compare-and-set-account-detail), is not dealt with inside the plugin-ledger-connector-iroha.ts file. The run-transaction test case also fail to use this argument.

1a. Build our own iroha-helper-ts library (outputs tx status and tx hash) based on the Iroha Javascript library, so that it could be upgraded to match the most recent Javascript library version. Moreover, our own iroha-helper-ts's output could be further optimized to suit test cases better. 

1b. After developing our own iroha-helper-ts library, correct compareAndSetAccountDetail's arguments. Also, correct the test case accordingly.

3/53

[Link](https://github.com/hyperledger/cactus/issues/1261)

[Link](https://github.com/hyperledger/cactus/issues/1265)

Iroha docker container

1

The test cases rely on [a modified Iroha v1.2.0 all-in-one (AIO) docker image](https://github.com/hyperledger/cactus/pkgs/container/cactus-iroha-all-in-one).

However, Iroha version 1.2.0 is outdated.

Upgrade Iroha to the latest version to improve its functionality and performance.2/56[Link](https://github.com/hyperledger/cactus/issues/1262)2

An Iroha Python SDK is embedded inside the Iroha AIO docker image for docker healthcheck. Although this healthcheck mechanism works fine, it makes the docker image ~100MB larger. 

Once the Iroha team introduces the gRPC healthcheck/ Iroha metrics page in a stable release (e.g., v1.2.2), implement healthcheck mechanism through gRPC healthcheck or curl the metric page.   
\`curl [http://127.0.0.1:8080/metrics](http://127.0.0.1:8080/metrics)\`2/56[Link](https://github.com/hyperledger/cactus/issues/1263)3Each Iroha docker container relies on a corresponding Postgres database container to store information. Replace the Postgres database docker container with RocksDB, which needs just one folder ( a docker volume) to keep data between different runs of image.3/56[Link](https://github.com/hyperledger/cactus/issues/1264)Documentation1

For docs/source/support/iroha.md, the link to the transaction test is not guaranteed to be valid.

Once the current [Iroha connector plugin PR](https://github.com/hyperledger/cactus/pull/1169) gets merged/released, update the test link to be a valid link. 1/56[Link](https://github.com/hyperledger/cactus/issues/1246)

\*For the difficulty level, 1 means the easiest, 5 means the most challenging.

\*For the priority listing, 1 means the most important, 7 means the least important. Important ones have been marked as red.

## Attachments:

![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W1 Slide.pdf](attachments/21954749/21964794.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W3 Slide.pdf](attachments/21954749/21964840.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W2 Slide.pdf](attachments/21954749/21964841.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W4 Slide.pdf](attachments/21954749/21965006.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W5 Slide.pdf](attachments/21954749/21965010.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W6 Slide.pdf](attachments/21954749/21965054.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W7 Slide.pdf](attachments/21954749/21965192.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W8 Slide.pdf](attachments/21954749/21965505.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W9 Slide.pdf](attachments/21954749/21965507.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W10 Slide.pdf](attachments/21954749/21965509.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W11 Slide.pdf](attachments/21954749/21965510.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha and Cactus integration W12 Slide.pdf](attachments/21954749/21965511.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha Meeting Presentation HanXu - 2021\_v2.pdf](attachments/21954749/21965620.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 14:56

[Atlassian](http://www.atlassian.com/)
