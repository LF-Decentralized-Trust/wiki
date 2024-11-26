1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q4 Hyperledger Sawtooth

Created by Andi Gunderson, last modified by Bobbi Muscara on Nov 04, 2021

Project Health

Hyperledger Sawtooth [https://sawtooth.hyperledger.org/](https://sawtooth.hyperledger.org/)

In the last quarter work was done to simplify some aspects of Sawtooth Sabre in preparation for it being moved to Transact. SQLite, PostgreSQL and LMDB support for ReceiptStore in sawtooth-lib has been stabilized. The design can be found [here](https://www.splinter.dev/community/planning/libsawtooth_receipt_store.html).

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)?
   
   1. LICENSE - yes
   2. CODE\_OF\_CONDUCT.md - no
   3. SECURITY.md - yes
   4. README.md - yes
   5. MAINTAINERS.md - yes
   6. CONTRIBUTING.md - yes
   7. CHANGELOG - yes, but called [RELEASE\_NOTES.md](http://RELEASE_NOTES.md)

# Questions/Issues for the TSC

No new issues.

# Releases

- Sawtooth Library v0.6.6 - 8/31/2021
- Sawtooth Library v0.6.7 - 10/07/2021

# Overall Activity in the Past Quarter

The community continues to discuss Sawtooth-related issues on Rocketchat. Live working sessions have also been used on a monthly basis to discuss the future of Sawtooth, with participation from the community.

Sawtooth Updates:

- Stabilized SQLite and PostgresSQL support for the ReceiptStore in sawtooth-lib
- Removed smart permission and Pike from Sabre. Pike has been moved to Grid and had a major update, and Smart Permissions are currently not used anywhere but did rely heavily on Pike.
- Community bug fixes

# Current Plans

The following work is currently in progress:

- Move portions of Sawtooth Sabre to Hyperledger Transact
- Migrate to Github Issues, away from JIRA.
- Rewriting the Sawtooth CLI in Rust
- Refreshing the Sawtooth website and documentation

The following work is currently planned:

- Create a new consensus library that will be used by the Sawtooth validator
- Initialize a Sawtooth service for Splinter
- Improve Sabre performance

Plans will continue to be developed as part of the working sessions.

# Maintainer Diversity

Maintainers are distributed across [Bitwise](http://bitwise.io/) IO, Cargill, Intel, and Walmart Labs.

# Contributor Diversity

Commits from 2021-07-20 to 2021-10-26 :  102

Committers from 2021-07-20 to 2021-10-26 :  6

Domains from 2021-07-20 to 2021-10-26 :  2

# Additional Information

Insights: [https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fsawtooth/dashboard;subTab=technical?time=%7B%22from%22:%222021-07-20T05:00:00.000Z%22,%22type%22:%22absolute%22,%22to%22:%222021-10-26T05:00:00.000Z%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fsawtooth/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-07-20T05%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-10-26T05%3A00%3A00.000Z%22%7D) 

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

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
