1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q3 Hyperledger Explorer

Created by jeeva sang, last modified by Troy Ronda on Nov 04, 2021

Project Health

Project health is green. We use all of the following to help keep project health green. Questions asked via rocket chat are being answered on time. For greater efficiency in this regard, the FAQ page is updated with every release.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yet to verify

# Questions/Issues for the TSC

None

# Releases

Releases this quarter:

- v1.1.7 - July 05, 2021
- v1.1.8 - August 16, 2021

v1.1.7 added bug fixes:

Bug Fixes and Updates

- [BE-876](https://jira.hyperledger.org/browse/BE-876) Stop unnecessary discovery request ([#255](https://github.com/hyperledger/blockchain-explorer/pull/255))
- Bugfix: tailing ampersand sign prevents container from restarting ([#254](https://github.com/hyperledger/blockchain-explorer/pull/254))
- [BE-857](https://jira.hyperledger.org/browse/BE-857) Change invoking function of lifecycle scc to allow non-admin client access ([#252](https://github.com/hyperledger/blockchain-explorer/pull/252))
- Bugfix: timeout error crashing explorer ([#253](https://github.com/hyperledger/blockchain-explorer/pull/253))
- Bugfix: disable enableAuthentication auth auto login using wrong network key issue ([#250](https://github.com/hyperledger/blockchain-explorer/pull/250))

v1.1.8 added bug fixes:

Bug Fixes and Updates

- BE-880 Fix incorrect multi-process logging ([#260](https://github.com/hyperledger/blockchain-explorer/pull/260))
- docs: add code snippet for admin cert modification ([#257](https://github.com/hyperledger/blockchain-explorer/pull/257)) ([#258](https://github.com/hyperledger/blockchain-explorer/pull/258))

# Overall Activity in the Past Quarter

The project has released for bug fixes

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

No new maintainers were added. We really need the community to come forward and contribute.

Please find here the maintainers list. [https://github.com/hyperledger/blockchain-explorer/blob/master/MAINTAINERS.md](https://github.com/hyperledger/blockchain-explorer/blob/master/MAINTAINERS.md)

# Contributor Diversity

The current main contributors are from DTCC and Fujitsu. We have 3 unique contributors on [Github](https://github.com/hyperledger/blockchain-explorer/graphs/contributors?from=2021-06-01&to=2021-10-30&type=c)in this quarter.

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
