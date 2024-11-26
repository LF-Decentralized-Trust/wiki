1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q4 Hyperledger Avalon

Created by Yevgeniy Y Yarmosh, last modified by Gari Singh on Feb 05, 2021

Prepared by Eugene (Yevgeniy) Yarmosh

# Project

[Hyperledger Avalon](https://lf-hyperledger.atlassian.net/wiki/display/avalon/Hyperledger+Avalon)

Project Health

The project health is good. The team focused on improving integration with K8S, worker pool scalability, multitenancy support and Graphene runtime integration.

Divya Taori became a new project maintainer.

[LF Analytics for Q4](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Favalon/dashboard?time=%7B%22from%22%3A%222020-10-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222020-12-31T08%3A00%3A00.000Z%22%7D)

# Questions/Issues for the TSC

There are no issues for the TSC currently.

# Releases

Last release was done in July 2020. No new releases have been done during Q4.

Due to the nature and complexity of the currently built capabilities the team decided to postpone the release to Q1/2021 in order to get to an appropriate completeness point function-wise. 

# Overall Activity in the Past Quarter

The project development was focused on the following areas

- Work-order Processing Enclave (WPE) implementation
- Kubernetes integration with elastic compute support
- Extending SGX attestation model to support 3rd party attestation (aka DCAP)
- Worker attestation support for SGX KSS (Key Sharing and Separation) as a steppingstone for supporting multi-tenancy (aka dedicated worker instances for tenants without any code changes)
- Integration of high-level LibOS runtimes Graphene as worker processing enclave
- CentOS Support (in addition to Ubuntu)
- Improving test automation and CI
- CII Best Practices Badge Complete

Avalon team participated in the following activities:

- Continued regular Avalon Technical Forum calls every other week with a good community participation
- Presented Hyperledger Avalon at EEA Financial Services SIG
- Continuously utilized email and rocket chat for community support

There were lower number of Avalon presentations at the industry forums, partially, due to some event cancellations. This is an area needs to focus in 2021. 

# Current Plans

The team is working towards release 0.7 that includes

- Completion of the worker pool implementation
- Finalize DCAP attestation support
- Key management enclave replication (final part of the worker pool scalability design)
- Secure cross-worker (Graphene) communication channel
- Multi-threading support for the key management enclave
- Multi-tenancy (dedicated worker instances per requester)
- Improved Python SDK as a separate subproject
- Improving test coverage and CI

The team also evaluation plans to increase number Avalon presentations at various industry events. 

# Maintainer Diversity

Divya Taori from Wipro became a Hyperledger Avalon maintainer.     

# Contributor Diversity

Contributor diversity is gradually improving. ASUS joint the project and contributed during the previous quarter. We have an interest in contributing starting from Q1/2021 from China Unicom.

# Additional Information

None at this time.

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
