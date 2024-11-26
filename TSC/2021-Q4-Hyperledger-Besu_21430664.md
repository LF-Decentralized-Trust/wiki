1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q4 Hyperledger Besu

Created by Danno Ferrin, last modified by Angelo de Caro on Jan 20, 2022

# Project Health

Hyperledger Besu remains a strong project with a growing community network of contributors. This quarter the team has focused on the Ethereum Mainnet "merge" update, library refactoring, and Quorum and QBFT compatibility.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? - Yes
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? - Yes

# Questions/Issues for the TSC

None

# Releases

- 21.10.0-RC1 - 4 Oct 2021
- 21.10.0-RC2 - 12 Oct 2021
- 21.10.0-RC3 - 15 Oct 2021
- 21.10.0-RC4 - 28 Oct 2021
- 21.10.0 - 1 Nov 2021
- 21.10.1 - 8 Nov 2021
- 21.10.2 - 15 Nov 2021
- 21.10.3 - 10 Dec 2021
- 21.10.4 - 16 Dec 2021
- 21.10.5 - 20 Dec 2021
- 22.1.0-RC1 - 16 Dec 2021

There were more releases this quarter than typical due to 4 separate CVEs (one Besu related, three Log4J related).  The 21.10.x line will remain "open" for security updates until 22.1.0 releases.

# Overall Activity in the Past Quarter

- **EVM Library**
  
  Work by Hedera Hashgraph has resulted into the separation of the EVM code into a stand-alone library, used by both Hedera and Hyperledger Besu.
- **QBFT**
  
  Interoperable with GoQuorum.
  
  Validators can be managed via smart contracts - allowing operators to quickly change validators if there is a problem (HA).
- **Mainnet Merge Offsite**
  
  Multiple Besu maintainers attended an offsite in Q4 with all the major Ethereum Mainnet consensus and execution layer clients, resulting in an initial proof of concept for the merge.
- **Privacy code hardening**
  
  Addressing tech debt in privacy code. Consolidation of naming ("onchain" privacy deprecated in favour of "flexible" privacy).
- **EVM Performance**
  
  Hedera has worked to roughly triple the throughput of the EVM.
- **JWT Authentication**
  
  Added support for additional (and stronger) authentication algorithms (default was RSA).
- **Logging and Developer experience improvements**
  
  Improvements in response to community feedback. More work to do here.

# Current Plans

- **"The Merge"**
  
  Ethereum Mainnet expects to merge the current mainnet chain into the Beacon chain in an event called "Docking" or "The Merge."  This is expected to occur in the first half of 2022. Principal work is mostly done and is expected to finish in Q1.
- **Shanghai Fork**
  
  The first fork after The Merge is expected to add some long overdue EVM improvements, such as the Ethereum Object Format.
- **Developer experience**
  
  Planning to add a workstream to specifically focus on developer experience, allowing prioritization of issues alongside feature work.
- **Tracing APIs**
  
  Parity-style Tracing APIs, requested by Infura

# Maintainer Diversity

Three maintainers were moved to emeritus status due to inactivity (David Mechler, Edward Mack, and Trent Mohay).  Seven new maintainers were added (Daniel Lehrner, Diego López León, Fabio Di Fabio, Frank Li, Jiri Peinlich, Simon Dudley, Taccat Isid)

Maintainers are employed by the following organizations:

- ConsenSys Quorum (FKA PegaSys)
- ETC Cooperative
- Hedera Hashgraph
- Splunk

The maintainers breakdown is:

- 20% not currently employed by ConsenSys (6 of 29) - This is a slight improvement from prior quarters, however this includes two who have not made contributions since leaving ConsenSys. This will drop to 14% if we do not retain their participation.

# Contributor Diversity

[LFX Analytics from 22  Sep to 22 Dec, 2021](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fbesu/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-09-22T06%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-12-22T07%3A00%3A00.000Z%22%7D)

(report generated prior to close of 3 month window)

Commits from 2021-09-22 to 2021-12-22: 309+

Committers from 2021-12-22 to 2021-12-22: 33 (9 non-ConsenSys)

Identified Orgs  2021-12-23 to 2021-12-21: 6

# Additional Information

None as of the due date for this report.

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

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
