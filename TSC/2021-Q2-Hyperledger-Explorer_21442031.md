1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q2 Hyperledger Explorer

Created by jeeva sang, last modified by Gari Singh on Oct 16, 2021

[Hyperledger Explorer](https://github.com/hyperledger/blockchain-explorer)

Project Health

Project health is green. We use all of the following to help keep project health green. Questions asked via rocket chat are being answered on time. For greater efficiency in this regard, the FAQ page is updated with every release.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? yes
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? yes

# Questions/Issues for the TSC

Still, we are in incubation status only. we would like to move from incubation to active projects. What is the procedure for promoting this project? 

# Releases

Releases this quarter:

- v1.1.5 - April 21, 2021
- v1.1.6 - June 06, 2021

v1.1.5 added features and bug fixes:

New Features

- [BE-694](https://jira.hyperledger.org/browse/BE-694) Add UI link to trans ([#227](https://github.com/hyperledger/blockchain-explorer/pull/227))
- [BE-858](https://jira.hyperledger.org/browse/BE-858) Upgrade base image of Explorer container image ([#220](https://github.com/hyperledger/blockchain-explorer/pull/220))
- [BE-801](https://jira.hyperledger.org/browse/BE-801) Add the steps to configure a subdomain ([#219](https://github.com/hyperledger/blockchain-explorer/pull/219))
- Upgrade fabric version supported by Explorer ([#227](https://github.com/hyperledger/blockchain-explorer/pull/227))

Bug Fixes and Updates

- [BE-862](https://jira.hyperledger.org/browse/BE-862) Fix sync error ([#228](https://github.com/hyperledger/blockchain-explorer/pull/228))
- Fix layout of icons on the navigation bar ([#218](https://github.com/hyperledger/blockchain-explorer/pull/218))

v1.1.6 added features and bug fixes:

New Features

- [BE-871](https://jira.hyperledger.org/browse/BE-871) Introduce dropdown to put together icons ([#247](https://github.com/hyperledger/blockchain-explorer/pull/247))
- [BE-870](https://jira.hyperledger.org/browse/BE-870) display direct trans link ([#237](https://github.com/hyperledger/blockchain-explorer/pull/237))
- Add typescript compilation on main. sh install ([#234](https://github.com/hyperledger/blockchain-explorer/pull/234))
- [BE-865](https://jira.hyperledger.org/browse/BE-865) Fix Repolinter Report Issues ([#231](https://github.com/hyperledger/blockchain-explorer/pull/231))

Bug Fixes and Updates

- [BE-855](https://jira.hyperledger.org/browse/BE-855) Stop unnecessary sync process triggered by FabricEvent ([#240](https://github.com/hyperledger/blockchain-explorer/pull/240))
- [BE-855](https://jira.hyperledger.org/browse/BE-855) Add try-catch block to handle block in-process exception ([#239](https://github.com/hyperledger/blockchain-explorer/pull/239))

# Overall Activity in the Past Quarter

The project has released few features

- Upgraded fabric version.
- Upgraded the base image of the Explorer container image.
- In UI we have added a transaction view and icon changes

# Current Plans

- Add more information on the Hyperledger Fabric network to get more insight from data
  
  - Endorsement Policy
  - Metrics exposed by each peer via Prometheus
- Raise Explorer to the powerful next level Ledger Data Query Platform
- - Track historical operations for any specific state
  - Automatically analyzing schema of the ledger state
- Continue on bug fixes, help community in configuring HLExplorer and troubleshooting
- Integrate the additional features mentioned in the "Contributor Diversity" section into Explorer

# Maintainer Diversity

We've had a few spot contributors added. No new maintainers were added. We really need the community to come forward and contribute.

Please find here the maintainers list. [https://github.com/hyperledger/blockchain-explorer/blob/master/MAINTAINERS.md](https://github.com/hyperledger/blockchain-explorer/blob/master/MAINTAINERS.md)

# Contributor Diversity

The current main contributors are from DTCC and Fujitsu. We have 4 unique contributors on [Github](https://github.com/hyperledger/blockchain-explorer/graphs/contributors?from=2021-01-01&to=2021-06-30&type=c)in this quarter.

And we had some proposals for Hyperledger Explorer as below:

- **New contributions**
  
  - EasyDoser
    
    - This is the outcome of one of the Hyperledger Internship programs. The integration of this feature into Explorer will offer more visibility of the network to users.
    - [Ease endorsement operations for Hyperledger based products (EasyDoser)](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=21954688)
  - LedgerDataRefiner
    
    - Fujitsu Lab. has proposed integrating their open-sourced ledger data analytics tool into Explorer. We have started the discussion on how to proceed with this contribution.
    - [https://github.com/FujitsuLaboratories/Ledger-Data-Refiner](https://github.com/FujitsuLaboratories/Ledger-Data-Refiner)
- WIP contributions
  
  - [minifab](https://github.com/litong01/minifabric)
    
    - This project is offering Hyperledger Explorer support as one of their features and we think it will be a good mutual reference.
  - [hyperledger-explorer-made-easy](https://github.com/saanvijay/hyperledger-explorer-made-easy)
    
    - This is a kind of utility tool for the easy setup of Hyperledger Explorer. After evaluating this tool and having a consensus for merging it into the Explorer repo within the team, we might get it included in Explorer as one of the official features.

# Additional Information

The insight chart can be found at [Explorer stats for the last quarter](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fexplorer/dashboard)[.](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fcello/dashboard;subTab=technical?time=%7B%22from%22%3A%222020-08-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222020-11-01T07%3A00%3A00.000Z%22%7D)

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
