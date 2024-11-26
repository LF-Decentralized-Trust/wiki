1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q3 Hyperledger Cello

Created by Yuanmao Zhu, last modified by artem on Sep 24, 2022

2022 Q3 Hyperledger Cello 2022

Project Health

Project health is OK with working on the coming v1.0 release.  v1.0.0-alpha2 is released on May 30, 2022. v1.0.0-beta is planned this quarter. v1.0.0 hopefully could be released by the end of year. 

The 1.0 release is with new architecture.

1. The new dashboard is almost done;
2. New agent design and docker agent implementation are done;
3. Continue the API Engine;

[Xichen Pan](https://lf-hyperledger.atlassian.net/wiki/people/712020:1085087f-f6a8-47ad-b5ae-b985d6152460?ref=confluence) joins us as an intern for Linux mentorship program this Q3, and has started to contribute the Cello project, and actively participates weekly meetings.

# Required Information

- [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)?
- [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)?
- Has your project implemented these inclusive language changes listed below to your repo? You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo.
  
  1. master → main
  2. slave → replicas
  3. blacklist → denylist
  4. whitelist → allowlist
- Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages?
  

# Questions/Issues for the TSC

There are no issues.

# Releases

1. v1.0.0-alpha2 is done in May, 2022.
2. v1.0.0-beta is planed this quarter
3. v1.0.0 is planed this year.

# Overall Activity in the Past Quarter

In Q3, we continue to focus on the implementation of API engine and front-end clients.

- Completed the front end basic work on the deployment operations;
- Finish the new backend agent (based on Docker);
- Finish the cli SDK for dashboard usage.
- Continued development of API engine.
  
  - node APIs are done;
  - channel APIs are almost done;
  - chaincode APIs are on-going.
  - support mutiple organizations.
- Kick off documentation "fix"

# Current Plans

Next steps include:

- Finish the v1.0.0-beta release in the Q3 quarter of 2022.
- Release the v1.0.0 in the Q4

# Maintainer Diversity

Current there are 3 maintainers, and those active developers who contribute to cello continuously (3 month) may be nominated as new maintainers. 

- [Baohua Yang](https://lf-hyperledger.atlassian.net/wiki/people/557058:17d87dbf-05fe-4c1b-84cf-fd69f7fcbb20?ref=confluence) (Oracle)
- [feng yang](https://lf-hyperledger.atlassian.net/wiki/people/712020:23894469-5964-413e-bde8-8baa9f37d28d?ref=confluence)  (H3C)
- [Yuanmao Zhu](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a1ab58c-74d8-45f1-ad1c-4fc227eb20cf?ref=confluence) (Coinbase)

# Contributor Diversity

In Q3, we have a total of 21 commits from 4 contributors.

# Additional Information

[Contribution Metrics](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fcello/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-07-01T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-08-30T04%3A00%3A00.000Z%22%7D)

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
