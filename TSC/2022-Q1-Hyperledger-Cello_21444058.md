1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q1 Hyperledger Cello

Created by Baohua Yang, last modified by Angelo de Caro on Mar 23, 2022

# Project Health

Overall health is OK with working on the coming v1.0 release.  v1.0.0-alpha is released on Jan 19, 2022. v1.0.0-alpha2 is coming this quarter.

The 1.0 release is with new architecture.

1. Continue with the new dashboard;
2. Finish new agent design and docker agent implementation;
3. Continue the API Engine;
4. Finish two demos: creating nodes, new cliSDK;

On the other hand, the internship project is done well with [Yuanmao Zhu](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a1ab58c-74d8-45f1-ad1c-4fc227eb20cf?ref=confluence) , who will continue to work on the project as an open-source contributor.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? yes
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)?
   
   1. [LICENSE](https://github.com/hyperledger/cello/blob/main/LICENSE) - yes
   2. [CODE\_OF\_CONDUCT.md](https://github.com/hyperledger/cello/blob/main/CODE_OF_CONDUCT.md) - yes
   3. [SECURITY.md](https://github.com/hyperledger/cello/blob/main/SECURITY.md) - yes
   4. [README.md](https://github.com/hyperledger/cello/blob/main/README.md) - yes
   5. [MAINTAINERS.md](https://github.com/hyperledger/cello/blob/main/MAINTAINERS.md) - yes
   6. [CONTRIBUTING.md](https://github.com/hyperledger/cello/blob/main/CONTRIBUTING.md) - yes
   7. [CHANGELOG](https://github.com/hyperledger/cello/blob/main/CHANGELOG.md) - yes

# Issues

No.

# Releases

Jan 19, 2022: v1.0.0-alpha is released

# Overall Activity in the Past Quarter

This quarter, we mainly have been focusing on the implementation of API engine and front end.

- Completed the front end basic work on the deployment operations;
- Finish the new backend agent (based on Docker);
- Finish the cli SDK for dashboard usage.
- Continued development of API engine.
  
  - node APIs are done;
  - channel APIs are almost done;
  - chaincode APIs are on-going.

# Current Plans

Next steps include:

- Finish the v1.0.0-alpha2 release this quarter;
- Finish the v1.0.0-beta release in the 2nd quarter of 2022.

Maintainer Diversity

Current there are 3 maintainers, and those active developers who contribute to cello continuously (3 month) may be nominated as new maintainers. 

1 maintainer (Haitao Yue ) is retired this quarter and a new one is nominated (Yang Feng).

- Baohua Yang (Oracle)
- Qiang Xu (JiLi Technology)
- Yang Feng (H3C)

# Contributor Diversity

This quarter, we have a total of 26 commits from 6 contributors.

# Additional Information

Insights from Dec 7, 2021  to  Feb 26 2022 ,can be found at [Cello stats for last quarter.](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fcello/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-12-07T08%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-02-26T08%3A00%3A00.000Z%22%7D)

# Reviewed by

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
- [feng yang](https://lf-hyperledger.atlassian.net/wiki/people/712020:23894469-5964-413e-bde8-8baa9f37d28d?ref=confluence)
- [Peng Du](https://lf-hyperledger.atlassian.net/wiki/people/712020:40cfa3db-3ae0-4442-b843-16a107ce7b9f?ref=confluence)

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
