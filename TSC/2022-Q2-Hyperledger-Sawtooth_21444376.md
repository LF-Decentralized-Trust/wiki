1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q2 Hyperledger Sawtooth

Created by Andi Gunderson, last modified by Sandor Miskey on Aug 24, 2022

Hyperledger Sawtooth [https://sawtooth.hyperledger.org/](https://sawtooth.hyperledger.org/)

Project Health

In the last quarter focus has been on design work for consensus-related components with contributions to Sawtooth's underlying dependencies. Design continues on block publishing, block management, and pending batch queue.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
   
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes
   
3. Has your project implemented these inclusive language changes listed below to your repo? You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo.
   
   1. master → main: Yes
   2. slave → replicas: Yes
   3. blacklist → denylist
      
      1. Some old PoET documentation needs to be updated.
   4. whitelist → allowlist
      
      1. Sawtooth back pressure handler needs to be updated.
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages?
   
   1. We have not added the statement to the documentation but besides the instance noted above we believe the documentation is inclusive.

# Questions/Issues for the TSC

No new issues.

# Releases

- Sawtooth Library v0.7.3 - 1/28/22

# Overall Activity in the Past Quarter

Design and implementation of consensus algorithms continued in Augrim, with an initial implementation of the 2PC algorithm. Current planned algorithms include 3PC, E3PC, and PBFT, and the designs are intended to cover those as well as algorithms with forking. Design work continued for the higher-level layer which uses consensus for the blockchain / distributed ledger, which will inform components in sawtooth-lib.

Sawtooth's website ([https://sawtooth.hyperledger.org/](https://sawtooth.hyperledger.org/))  has been updated to use Jekyll markdown files for the most recent release. The documentation for older releases is still a work in progress.

A performance improving change was made to the transaction receipt store: an index was added to the frequently queried "idx" and "service\_id" columns in the "transaction\_receipt" table.

The community now discusses Sawtooth-related issues on Discord. The monthly live working sessions continue and now primarily focus on design documents for Sawtooth 2-related work.

# Current Plans

The following work is currently in progress:

- Create a new consensus library that will be used by the Sawtooth validator
- Improve Sabre performance by implementing state caching in Transact for large pieces of state, such as smart contracts.
- Sawtooth 2 component designs
- Migrate to Github Issues, away from JIRA.
- Rewriting the Sawtooth CLI in Rust (paused)

The following work is currently planned:

- Initialize a Sawtooth service for Splinter

Plans will continue to be developed as part of the working sessions.

# Maintainer Diversity

Maintainers are distributed across [Bitwise](http://bitwise.io/) IO, Cargill, Intel, and Walmart Labs.

# Contributor Diversity

Commits from 2022-01-26 to 2022-04-26 :  325

Committers from 2022-01-26 to 2022-04-26 :  9

Domains from 2022-01-26 to 2022-04-26 :  4

# Additional Information

Insights 

[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fsawtooth/dashboard;subTab=technical?time=%7B%22from%22:%222022-01-26T06:00:00.000Z%22,%22type%22:%22absolute%22,%22to%22:%222022-04-26T05:00:00.000Z%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fsawtooth/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-01-26T06%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-04-26T05%3A00%3A00.000Z%22%7D)

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
