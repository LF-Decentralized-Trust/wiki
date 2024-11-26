1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q1 Hyperledger Iroha

Created by Nikolay Yushkevich, last modified on Jan 23, 2019

Project

Hyperledger Iroha [https://github.com/hyperledger/iroha](https://github.com/hyperledger/iroha)

Project Health

We released a couple of Release Candidate releases since the last report. New features and improvements:

- New component for YAC: BFT Ordering Service
- Resistance to replay attacks
- Stability improvements and error handling

In addition, several client libraries were updated: Javascript, Java, Swift/Objective-C, Python. There was a contribution to Kubernetes-based deployment and Ansible scripts. Also, iroha-testcontainers library was contributed to Hyperledger for fast deployment of local peer network in Java code for experimenting and testing purposes. 

Our chats are integrated now with the help of Nakayoshi bot [https://github.com/soramitsu/nakayoshi](https://github.com/soramitsu/nakayoshi) and soon we are going to contribute to Hyperledger a bot capable of forwarding GitHub issues to JIRA bugs/issues, written in Rust: [https://github.com/soramitsu/yozhik](https://github.com/soramitsu/yozhik).

In general, we would like to start a formal process of requesting TSC for the release approval after we resolve some of the pending issues: 

# Issues

1. Code contributions are not diverse enough. As the part of our release plan, we are composing a contributors diversity plan in order to present TSC a set of actions in order to strengthen the involvement of outside contributors.
2. Also, we need to ensure that all of our code is licensed under the Apache-2.0 license.
3. Prior to requesting TSC or releasing the version of Hyperledger Iroha 1.0 final, we will need to modify the history of commits and fix DCO non-conformances.

# Releases

- 10 Jan 2019 [Hyperledger Iroha v1.0 Release Candidate 2](https://github.com/hyperledger/iroha/releases/tag/1.0.0_rc2)
- 12 Dec 2018 [Hyperledger Iroha v1.0 Release Candidate 1](https://github.com/hyperledger/iroha/releases/tag/1.0.0_rc1)

# Overall Activity in the Past Quarter

- Met David Huseby in Innopolis, Russia for the purpose of process and security audit
- Improved involvement of maintainers in Rocket.Chat and mailing list
- Transferred issue management to [jira.hyperledger.org](http://jira.hyperledger.org) and initiated process of project design/process documentation transfer to [wiki2.hyperledger.org](http://wiki2.hyperledger.org)
- Started design discussions over mailing lists and community meeting
- Reached sufficient test coverage (**78.1%** 2018-12-05 17:11:35 [https://out-8410xxpdz.now.sh](https://out-8410xxpdz.now.sh))
- We have updated the CII certification, which can be viewed here [https://bestpractices.coreinfrastructure.org/ru/projects/960](https://bestpractices.coreinfrastructure.org/ru/projects/960)

# Current Plans

1. Continue the development of contributors' diversity plan.
2. Ship remaining technical improvements.
3. Finish the activities, required in the quality gate for 1.0 final release: [https://soramitsucoltd.aha.io/published/e9bce93777c2c4b2448e4e6e78e90b4f](https://soramitsucoltd.aha.io/published/e9bce93777c2c4b2448e4e6e78e90b4f?page=1)
4. Request TSC to move to v1.0.
5. Execute the diversity plan and provide support for v1.0 with the help of maintainers and contributors.
6. Release next version of Iroha with a customizable API.

# Maintainer Diversity

Number of active code maintainers: 12 (all currently represented by Soramitsu)

# Contributor Diversity

Coming closer to production version we see more and more activity in chats. People come interested in Iroha's simplicity and client libraries — we receive lots of feedback and feature requests that help us make a plan for Iroha development. Based on that we can tell that Iroha has many ways of development. Still, lack of production-ready version might be an obstacle for some projects and we hope to gain more users after we release v1.0. 

We receive around 10 messages a day from people using Iroha in their projects and it is exciting to discuss the experience with them to see a greater picture. At the moment there are several users/ use case contributors that provided us with evaluation of Iroha for future release and we continue to receive feedback. 

Currently, many issues in Jira are based on issue reports from outside contributors. 

### Documentation and translation

New languages added: Dutch, Chinese (simplified), Spanish, French: [https://poeditor.com/join/project/SFpZw7o33o](https://poeditor.com/join/project/SFpZw7o33o)

41 contributors in total for 2018, 7 contributors were most active since the last report:

NicknameEmailLanguageFrederik De Breuckfrederik.debreuck@[ts.fujitsu.com](http://ts.fujitsu.com)Dutchmichaeltianya0yingzi@[gmail.com](http://gmail.com)Chinese (simplified)Aleksander Fielekaleksander.fielek@[outlook.com](http://outlook.com)FrenchYehua Chenemail@[krischen.ca](http://krischen.ca)Chinese (simplified)熊超xchtl@[qq.com](http://qq.com)Chinese (simplified)Mikhailboldrev@[soramitsu.co.jp](http://soramitsu.co.jp)SpanishYang Gaokingjiyang@[gmail.com](http://gmail.com)Chinese (simplified)

### Code contributions

#### Iroha

Number of active current code contributors since the last report: 7

Total number of code contributors since the last report: 19

Unique domains for the contributors since the last report: 12 (including Soramitsu domain)

#### Client libraries

Number of active code contributors: 8

New: since the last report [https://github.com/hyperledger/iroha-java](https://github.com/hyperledger/iroha-java) has been released to Hyperledger (from [https://github.com/Warchant/iroha-pure-java](https://github.com/Warchant/iroha-pure-java)) and [https://github.com/hyperledger/iroha-testcontainers](https://github.com/hyperledger/iroha-testcontainers) (from [https://github.com/Warchant/testcontainers-iroha](https://github.com/Warchant/testcontainers-iroha))

# Additional Information

It was a pleasure to meet the vast majority of TSC members in Hyperledger Global Forum and discuss current issues. The topmost setback was the diversity of community, which we are going to address in our plan, along with TSC request for the release.

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
