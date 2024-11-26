1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q1 Hyperledger Fabric

Created by Christopher Ferris, last modified by Gari Singh on Feb 07, 2020

# Project

## Hyperledger Fabric

Project Health

Fabric continues to grow and mature. Our v1.4.4 release was delivered mid-November and v2.0-beta mid-December. We have experienced a slight decrease in the diversity of contributors with IBM comprising 41.7% of the contributors over the past quarter (-1.3%). All of the main project repositories have been transitioned to GitHub from Gerrit, and the CI/CD has also been transitioned to Azure Pipelines. Hopefully the new GitHub contributions will make it easier to attract and retain new contributors. We also discussed changes to the documentation review process to allow for greater diversity of maintainers who are focused primarily on the documentation, given that much of that work has been done in the Fabric Documentation WG, but not visible to the commit review process.

# Questions/Issues for the TSC

Diversity of maintainers and contributors improved slightly this past quarter. New documentation maintainers team created that should enable those focused exclusively on documentation to become more involved in the review process for documentation.

# Releases

As noted, we released v1.4.4 mid-November with some minor enhancements to address administrative issues. We also bumped the versions of Go and Node. We released v2.0-beta mid December that incorporates the new chaincode lifecycle, a new chaincode launching mechanism, some performance improvements, and improvements to private data that enable new decentralized application patterns. There was also some considerable refactoring of the validation pipeline which necessitated removing the FabToken feature that was previewed in v2.0-alpha. We do plan to revisit the token design in the coming releases post 2.0. Additionally, there was a large amount of tech debt addressed in the areas of automated test, CI, and code cleanup. We plan to formally release v2.0 next week given that the testing of v2.0-beta has gone well.

# Overall Activity in the Past Quarter

There were 790 commits from 90 engineers representing 20 entities in the past quarter. Mailing list activity for the quarter remained fairly robust at ~225 emails. RocketChat also remained quite active. [StackOverflow](https://stackoverflow.com/questions/tagged/hyperledger-fabric) also added another 300 questions, remaining a very popular means of engagement.

# Current Plans

The maintainers have adopted an RFC process to manage new feature discussion and agreement.The new [fabric-rfcs](https://github.com/hyperledger/fabric-rfcs/) repo holds the specifics, and there's a [splash page](https://hyperledger.github.io/fabric-rfcs/) that makes navigating the substance easier.

The maintainers plan to continue the quarterly release strategy post v2.0, and there will likely be a v1.4.5 in February continuing the LTS support.

The maintainers are also in the process of revising the LTS strategy for Fabric. It was felt that we need to continue LTS support for the 1.4 release stream until we feel comfortable that the feature set for a new LTS release is worth making a new (and overlapping) LTS commitment. Current thinking is that we hope to have v2.2 at end of Q2 become the next LTS release, and that there will be an overlapping of LTS support for the 1.4 release stream. Expect an RFC outlining the new LTS strategy once v2.0 has been released.

# Maintainer Diversity

As noted, we have modified the documentation review process to enable those who are focused on docs to contribute. As such we have added additional maintainers for the docs tree including one non-IBMer. Again, we continue to encourage others to engage in reviewing PRs with the hopes that we can add more.

# Contributor Diversity

We have experienced a slight increase in the diversity of contributors with IBM comprising 41.7% of the contributors over the past quarter (-1.7%). We are still actively interested in growing contributions and expect the transition from Gerrit to GitHub will lower the barrier for contributions.

# Additional Information

# Reviewed by

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Christopher Ferris](https://lf-hyperledger.atlassian.net/wiki/people/5abb903a8724022aa9070581?ref=confluence)
- [Dan Middleton](https://lf-hyperledger.atlassian.net/wiki/people/712020:2979764a-3998-4ef1-8810-60b799067924?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Swetha Repakula](https://lf-hyperledger.atlassian.net/wiki/people/712020:503b5691-8e92-4d2d-83d3-e9e74d296436?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
