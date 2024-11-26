1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q4 Hyperledger Grid

Created by Andi Gunderson, last modified by Gari Singh on Feb 05, 2021

# Project

Hyperledger Grid: [https://www.hyperledger.org/projects/grid](https://www.hyperledger.org/projects/grid)

Project Health

Health is good. Focus and discussion is currently around preparing Grid for its initial release, an integration component meant to interface with external systems, and designing a default schema for GS1 products.

# Questions/Issues for the TSC

- There are no specific issues at the moment.

# Releases

- No prior releases.

# Overall Activity in the Past Quarter

The Location smart contract was completed and its functionality can be accessed via the CLI and REST API, and the Location RFC was approved. Initial work has started on an integration component meant to interface with external ERP systems. 

The Grid SDK was refactored to adopt more modular patterns. Database functionality was split into modules for each individual Grid feature, each supporting PostgreSQL and SQLite database backends. Error handling in the SDK was also revamped to be more consistent between modules. Finally, various bug fixes and enhancements for the CLI and REST API were completed to prepare Grid for it’s initial release.

Documentation was added to the Grid website that adds content regarding running Grid on Sawtooth. This includes documentation on setting up an environment and using Grid features. Additionally, database schema reference information is now available on the website.

The main source of asynchronous engagement is still the Hyperledger Chat [#grid channel](https://chat.hyperledger.org/channel/grid) and RFC PRs. Grid community meetings continue, with a schedule of one every 4 weeks.

# Current Plans

Preparing for the initial 0.1 release

Designing and implementing an integration component for external systems

Purchase order RFC

# Maintainer Diversity

Davey Newhall was added as a maintainer of the Grid and Grid Website repositories. There are 19 maintainers across the different repos.

We anticipate adding additional maintainers as contributions increase for areas currently in development.

# Contributor Diversity

Contributor diversity remains steady with previous quarters, with some share of the project's overall diversity coming from non-developer participation in their areas of expertise.

Sponsoring organizations that are actively contributing to Grid include Cargill, Target, GS1, and Bitwise IO. Additional contributions come from individual contributors.

# Additional Information

Insights from September 3rd to December 3rd 2020

[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fgrid/dashboard?time=%7B%22from%22:%222020-09-03T05:00:00.000Z%22,%22type%22:%22absolute%22,%22to%22:%222020-12-03T06:00:00.000Z%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fgrid/dashboard?time=%7B%22from%22%3A%222020-09-03T05%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222020-12-03T06%3A00%3A00.000Z%22%7D)

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
