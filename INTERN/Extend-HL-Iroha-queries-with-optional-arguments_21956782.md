1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)

# Hyperledger Mentorship Program : Extend HL Iroha queries with optional arguments

Created by baziorek, last modified by Min Yu on Nov 29, 2021

**Project Title**Extend HL Iroha (version 1.x) queries with optional arguments to add possibility of fetching data in time range**Status**

COMPLETED

**Difficulty**

MEDIUM  

# Description

[Hyperledger Iroha](https://www.hyperledger.org/use/iroha) has implemented set of [commands](https://iroha.readthedocs.io/en/master/develop/api/commands.html) and [queries](https://iroha.readthedocs.io/en/master/develop/api/queries.html). In the internship's project for few Iroha's queries ([GetAccountTransactions](https://iroha.readthedocs.io/en/master/develop/api/queries.html#get-account-transactions) and [GetAccountAssetTransactions](https://iroha.readthedocs.io/en/master/develop/api/queries.html#get-account-asset-transactions) and optionally [GetPendingTransactions](https://iroha.readthedocs.io/en/master/develop/api/queries.html#get-pending-transactions)) should be added optional arguments e.g.: `from` and `to` to return transactions in the provided time range or in provided blocks range.

**Problem description**

Fetching transactions in Iroha can be from first account's transaction or from provided transaction hash. On the other bound transactions are limited by max number of transactions to fetch. So when it is necessarily to fetch transactions for a month: hash of first transaction needs to be stored in blockchain and number of transactions should be "guessed" -if too big it would take longer, if too small another query would be necessarily). It also requires few queries instead of one.

# Additional Information

- [Hyperledger Iroha](https://www.hyperledger.org/use/iroha) ([documentation](https://iroha.readthedocs.io/en/master/), [chat,](https://chat.hyperledger.org/channel/iroha) [wiki](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Hyperledger+Iroha), [source code](https://github.com/hyperledger/iroha))
- [Helper notes where queries are in Iroha code](https://lf-hyperledger.atlassian.net/wiki/display/RU/Advanced+Iroha)
- Completed Internship project which was adding extra command and queries in 2020: [Making HL Iroha Data Model Modular for Interoperability with Other Projects](Making-HL-Iroha-Data-Model-Modular-for-Interoperability-with-Other-Projects_21956175.html)
- [Iroha-python library](https://github.com/hyperledger/iroha-python)

# Learning Objectives

The mentee will be able to learn:

- architecture of Iroha (1.x),
- work in true spirit of open-source, communicating with Iroha community, joining calls,
- writing documentation,
- following [rules of open-source code](https://iroha.readthedocs.io/en/master/community/index.html#c-style-guide) of Hyperledger Iroha,
- creating automatic tests of code,

# Expected Outcome

Implementation according to description and plan of documentation and tests. Added possibility of running modified queries from iroha-python library.

# Relation to Hyperledger

[Hyperledger Iroha](https://www.hyperledger.org/use/iroha) ([documentation](https://iroha.readthedocs.io/en/master/), [chat,](https://chat.hyperledger.org/channel/iroha) [wiki](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Hyperledger+Iroha))

Internship project which was adding extra command and queries in 2020: [Making HL Iroha Data Model Modular for Interoperability with Other Projects](Making-HL-Iroha-Data-Model-Modular-for-Interoperability-with-Other-Projects_21956175.html)

# Education Level

Preferred undergraduate.

# Skills

- Reading English documentation
- C++ advanced
- depending on database software when the internship starts: ability to use SQL and PostgreSQL or ability to use [RocketDB](https://rocksdb.org/)
- basic knowledge of Protobuf
- Python (optionally)

# Future plans

After project completion more commands and queries to Iroha will be added.

# Preferred Hours and Length of Internship

No preference (just do your job good before 15th August according to project plan and report to mentors every week progress and report progress during [bi-weekly Iroha Community meeting](https://lists.hyperledger.org/g/iroha/calendar)).

# Mentor Name and Contact Info

**Grzegorz Bazior** (Yonix Digital Systems, AGH University of Science and Technology)  
email: g.bazior\[you know what]yodiss.pl  
gitter and Telegram and RocketChat: @baziorek

# Mentee

[**Piotr Pawłowski**](https://lf-hyperledger.atlassian.net/wiki/people/62266827b7e7c7007159523d?ref=confluence) 

# Results

- [GetAccountTransactions and GetAccountAssetTransactions for main iroha code](https://github.com/hyperledger/iroha/pull/1092)
- [Changes in Iroha-Python library](https://github.com/hyperledger/iroha-python/pull/77)
- [Changes in Iroha-JavaScript library](https://github.com/hyperledger/iroha-javascript/pull/63)
- [GetPendingTransactions for main iroha code](https://github.com/hyperledger/iroha/pull/1300)
- [Changes in Iroha-Java library](https://github.com/hyperledger/iroha-java/pull/83)

# Final Report

[![](attachments/thumbnails/21956782/21966108)](attachments/21956782/21966108.pptx)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation Template - Nov2021.pptx](attachments/21956782/21966108.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)

Document generated by Confluence on Nov 26, 2024 14:56

[Atlassian](http://www.atlassian.com/)
