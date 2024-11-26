1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q3 Hyperledger Avalon

Created by Yevgeniy Y Yarmosh, last modified by Nathan George on Nov 11, 2021

[Hyperledger Avalon](https://lf-hyperledger.atlassian.net/wiki/display/avalon/Hyperledger+Avalon)

Prepared by Eugene (Yevgeniy) Yarmosh

Project Health

The team was focused on identifying an appropriate path that would split Avalon main into two independent parts – blockchain connectors and confidential computing (Intel SGX based) core. As result there were no commits to the main repository. We continued to work on the Python SDK sub-project and Kata/K8S prototype.  The team continued to support General Department of Vietnam Customs project.

Analytics: [link](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Favalon/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-07-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-09-30T07%3A00%3A00.000Z%22%7D)

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes.
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? No

# Questions/Issues for the TSC

There are no issues for the TSC currently.

# Releases

There was no release in this quarter.

A release schedule will be updated Avalon split plan is finalized.

# Overall Activity in the Past Quarter

The primary focus has been on splitting Avalon main into two independent parts – blockchain connectors and confidential computing (Intel SGX based) core. The SGX core may be potentially hosted at Confidential Computing Consortium while Avalon itself will focus on the blockchain integration. This work is in progress and will continue in Q4.  

Other activities during Q3/2021

- Avalon SDK for direct mode is merged and the package is published at [https://pypi.org/project/avalon-sdk-py/](https://pypi.org/project/avalon-sdk-py/)
- Presentation on Avalon at the Webinar organized by STPI India for the upcoming startups/entrepreneurs with panelists from Amazon, IBM, MathWorks and other companies. [https://apiary.stpi.in/](https://apiary.stpi.in/)
- Continued support for the POC for General Department of Vietnam Customs projects and a corresponding white paper is published by Intel and SAP  at [white-paper-link](https://www.intel.com/content/www/us/en/partner/showcase/sap/protect-confidential-customs-data-brief.html).
- Started prototyping running SGX enabled microservices in Kata runtime under K8S
- Started discussions with LF Edge Alvarium team on utilizing Avalon for improved data provenance trust and confidentiality in decentralized use cases

# Current Plans

The team is working on

- Finalizing Avalon code base spilt into independent parts – blockchain specific and confidential compute core with a possibility of hosting the core at Confidential Computing Consortium
- Engaging with LF Edge Alvarium project on the data provenance solution
- Defining smart contracts focused on the data provenance use cases
- Integrating Python SDK in the main repository
- Improving deployment and ease-of-use in cloud native (K8S) environment

# Maintainer Diversity

No changes to the maintainer list in this quarter.

# Contributor Diversity

No changes to the contributors list in this quarter.

# Additional Information

None at this time.

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

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
