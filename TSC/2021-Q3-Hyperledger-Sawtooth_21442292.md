1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q3 Hyperledger Sawtooth

Created by Andi Gunderson, last modified by Gari Singh on Oct 16, 2021

Project Health

In the last quarter work was done to find and improve a memory leak in Sawtooth Sabre. Work is currently underway to add SQLite and PostgreSQL support for the ReceiptStore in sawtooth-lib. The design can be found [here](https://www.splinter.dev/community/planning/libsawtooth_receipt_store.html).

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
   
2. [Have you implemented the Common Repository Structure in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? No
   

# Questions/Issues for the TSC

No new issues

# Releases

Sawtooth Sabre v0.7.2 - 06/24/2021

# Overall Activity in the Past Quarter

The community continues to discuss Sawtooth-related issues on Rocketchat. Live working sessions have also been used on a monthly basis to discuss the future of Sawtooth, with participation from the community.

Sawtooth Updates:

- A memory leak was discovered in Sawtooth Sabre caused by the version of wasmi pulled in. The leak was improved by updating wasmi from 0.4 to 0.9. This update also provided a small performance increase.

# Current Plans

The following work is currently in progress:

- Rewriting the Sawtooth CLI in Rust
- Refreshing the Sawtooth website and documentation
- Move portions of Sawtooth Sabre to Hyperledger Transact
- Migrate to Github Issues, away from JIRA.
- Add a receipt store trait that will be implemented with LMDB, SQLite and PostgreSQL backends.

The following work is currently planned:

- Create a new consensus library that will be used by the Sawtooth validator
- Initialize a Sawtooth service for Splinter
- Improve Sabre performance

Plans will continue to be developed as part of the working sessions.

# Maintainer Diversity

Maintainers are distributed across [Bitwise](http://bitwise.io/) IO, Cargill, Intel, and Walmart Labs.

# Contributor Diversity

Commits from 2021-04-21 to 2021-07-20 :  21

Committers from 2021-04-21 to 2021-07-20 :  7

Domains from 2021-04-21 to 2021-07-20 :  3

# Additional Information

Insights [https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fsawtooth/dashboard;subTab=technical?time=%7B%22from%22:%222021-04-21T05:00:00.000Z%22,%22type%22:%22absolute%22,%22to%22:%222021-07-20T13:42:12.561Z%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fsawtooth/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-04-21T05%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-07-20T13%3A42%3A12.561Z%22%7D)

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Baohua Yang](https://lf-hyperledger.atlassian.net/wiki/people/557058:17d87dbf-05fe-4c1b-84cf-fd69f7fcbb20?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [María Teresa nieto](https://lf-hyperledger.atlassian.net/wiki/people/5d36fa46af1d920bc99755b6?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
