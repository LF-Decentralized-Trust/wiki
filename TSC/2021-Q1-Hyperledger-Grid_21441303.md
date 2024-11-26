1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q1 Hyperledger Grid

Created by Andi Gunderson, last modified by Gari Singh on Mar 17, 2021

# Project

Hyperledger Grid: [https://www.hyperledger.org/projects/grid](https://www.hyperledger.org/projects/grid)

Project Health

Health is good. Multiple releases, including Grid's first official release, have gone out which allow stable Grid deployments. Design and implementation of new features for workflows, integration, and purchase orders are underway. A new version of the Pike smart contract, and a new feature for Product are being developed.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? In progress
   
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? No
   

# Questions/Issues for the TSC

There are no specific issues at the moment.

# Releases

- 0.1.1
- 0.1.2

# Overall Activity in the Past Quarter

Started work on an integration component for Grid. This component is meant to provide a more traditional API interface for third party components and partners.

Grid daemon REST API endpoints that return multiple records are now paged.

Versioning the grid daemon REST API and moving the bulk of its functionality into the SDK crate.

Started work on a workflow module in the Grid SDK. This will allow smart contract authors to create custom workflows.

A new version of the Pike smart contract is in development which includes functionality such as role delegation, and an index of alternate organization identifiers.

A lot of planning/design of new features in the form of RFC content.

The main source of asynchronous engagement is still the Hyperledger Chat [#grid channel](https://chat.hyperledger.org/channel/grid) and RFC PRs. Grid community meetings continue, with a schedule of one every 4 weeks.

# Current Plans

Working through RFCs for Grid Workflow, Grid Purchase Order, Grid Integration Component, and enhancements to Grid Product and Grid Pike. Implementations of the same.

# Maintainer Diversity

Maintainers remain the same as the previous quarter. There are 19 maintainers across the different repos.

# Contributor Diversity

Contributor diversity remains steady with previous quarters, with some share of the project's overall diversity coming from non-developer participation in their areas of expertise.

Sponsoring organizations that are actively contributing to Grid include Cargill, Target, GS1, and Bitwise IO. Additional contributions come from individual contributors.

# Additional Information

Insights from December 3rd 2020 to February 24th 2021

[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fgrid/dashboard?time=%7B%22from%22:%222020-12-03T06:00:00.000Z%22,%22type%22:%22absolute%22,%22to%22:%222021-02-24T06:00:00.000Z%22%7D&amp;filter=%23%2Fdashboard%2FGit%3Fembed%3Dtrue%26\_g%3D(refreshInterval:(pause:!t,value:0),time:(from:%272020-12-03T06:00:00.000Z%27,to:%272021-02-24T06:00:00.000Z%27))](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fgrid/dashboard?time=%7B%22from%22%3A%222020-12-03T06%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-02-24T06%3A00%3A00.000Z%22%7D&filter=%23%2Fdashboard%2FGit%3Fembed%3Dtrue%26_g%3D%28refreshInterval%3A%28pause%3A%21t%2Cvalue%3A0%29%2Ctime%3A%28from%3A%272020-12-03T06%3A00%3A00.000Z%27%2Cto%3A%272021-02-24T06%3A00%3A00.000Z%27%29%29)

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
