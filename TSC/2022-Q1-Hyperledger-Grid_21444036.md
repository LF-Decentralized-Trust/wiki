1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q1 Hyperledger Grid

Created by Shannyn Telander, last modified by Jim Zhang on Mar 24, 2022

Hyperledger Grid: [https://www.hyperledger.org/projects/grid](https://www.hyperledger.org/projects/grid) 

Project Health

Health is good. Grid v0.3 was released and roadmap items for release 0.4 are beginning development.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? Yes
3. Has your project implemented these inclusive language changes listed below to your repo? You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo.
   
   1. master → main: Yes
   2. slave → replicas: N/A
   3. blacklist → denylist: N/A
   4. whitelist → allowlist: Yes
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages?: No

# Questions/Issues for the TSC

- Grid's documentation/website ([https://grid.hyperledger.org/](https://grid.hyperledger.org/)) is difficult to find starting from [https://www.hyperledger.org/](https://www.hyperledger.org/).

# Releases

- Grid 0.2.3 - 12/20/2021
- Grid 0.3.1 - 1/28/2022
- Grid 0.3.2 - 2/3/2022

# Overall Activity in the Past Quarter

Features enter Grid as experimental, then go through a formal review process to stabilize them. Several features were stabilized:

- Xsd-downloader
- Purchase-order
- Client-reqwest
- Data-validation
- Workflow

Work towards stabilizing additional Grid features continues.

Completed work on version 1 of Grid Purchase Order, including smart contract, state-delta export, REST API endpoints, database schema, store implementation, etc. This provides functionality for managing a purchase order throughout its lifecycle for agents involved in the purchasing and selling process.

Continued work on the design of components for the 0.4 release. This includes a batch submitter, which submits batches to the DLT, and a queuer for this component that decides which batches the submitter will claim. A DLT monitor component will track the status of a submitted batch. Also, the REST API is undergoing redesign to support submitting batches as JSON. The batch store has also been designed to be updated to support all of these components. 

The main source of asynchronous engagement has been moved to Discord, while RFC PRs remain.

# Current Plans

Current work is focused on design and development for batch tracking within Grid. The main goal of this work is to make interaction with the DLT simpler and more familiar for the user, as they would now be able to submit transactions to the REST API using simple JSON. Overall, batch tracking includes several components that will oversee the submission of batches as well as monitoring the batch through its lifecycle, from submitting the changes to the changes being committed to state. This functionality is planned for the 0.4 release.

# Maintainer Diversity

We have added one maintainer, Lee Bradley, since the previous update. There are 20 maintainers across the different repos. 

# Contributor Diversity

Contributor diversity remains steady with previous quarters, with some share of the project's overall diversity coming from non-developer participation in their areas of expertise. 

Sponsoring organizations that are actively contributing to Grid include Cargill, Target, GS1, and Bitwise IO. Additional contributions come from individual contributors. 

We have had one new contributor since the last update.

# Additional Information

Insights from November 25th 2021 to February 25th 2022

 [https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fgrid/dashboard;subTab=technical?time=%7B%22from%22:%222021-11-25T06:00:00.000Z%22,%22type%22:%22absolute%22,%22to%22:%222022-02-25T06:00:00.000Z%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fgrid/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-11-25T06%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-02-25T06%3A00%3A00.000Z%22%7D)

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
