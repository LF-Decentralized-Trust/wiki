1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q4 Hyperledger FireFly

Created by Nicko Guyer, last modified by kamlesh nagware on Jan 27, 2022

Hyperledger FireFly [https://github.com/hyperledger/firefly](https://github.com/hyperledger/firefly)

# Project Health

Hyperledger FireFly continues to make progress toward v1.0

DimensionLink to InsightsCommit Activities[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical;v=source-control%2Fcommits%2Foverview](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical;v=source-control%2Fcommits%2Foverview)PR Activities[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical;v=pull-request-management%2Fgithub-pr%2Foverview](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical;v=pull-request-management%2Fgithub-pr%2Foverview)Contributor Strength[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;quicktime=time\_filter\_3M](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;quicktime=time_filter_3M)

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776) ? Yes
   
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure) ? Yes
   

# Questions/Issues for the TSC

- None

# Releases

- Our release process and versioning schemes were established this quarter (documented in the [Maintainer Docs](https://hyperledger.github.io/firefly/maintainers/maintainers.html)), and all firefly-* repos are following semantic versioning now.
- Recent releases can be found on the Release page: [https://github.com/hyperledger/firefly/releases](https://github.com/hyperledger/firefly/releases)
  
  - Each FireFly microservice may have an independent release schedule/version, and releases for each service can be found in their respective repos
- While we are striving to keep breaking changes to a minimum, there is a possibility that some releases will include breaking changes before the project reaches v1.0

Overall Activity in the Past Quarter

The team continues to make good progress toward [v1.0](https://github.com/hyperledger/firefly/issues/117), including adding several major new pieces of work:

- Tokens (fungible and non-fungible)
- Custom smart contract support (in progress)
- Performance testing and tuning

The [FireFly Improvement Request (FIR)](https://github.com/hyperledger/firefly-fir) process was established earlier this quarter and the first FIR is currently in progress for Custom Smart Contracts.

# Current Plans

[https://github.com/hyperledger/firefly/issues/117](https://github.com/hyperledger/firefly/issues/117)

The v1.0 release remains the primary focus of the team

# Maintainer Diversity

[https://github.com/orgs/hyperledger/teams/firefly-committers/members](https://github.com/orgs/hyperledger/teams/firefly-committers/members)

8 of 8 maintainers are from Kaleido.

# Contributor Diversity

[https://github.com/hyperledger/firefly/graphs/contributors](https://github.com/hyperledger/firefly/graphs/contributors)

[https://github.com/hyperledger/firefly-ethconnect/graphs/contributors](https://github.com/hyperledger/firefly-ethconnect/graphs/contributors)

[https://github.com/hyperledger/firefly-fabconnect/graphs/contributors](https://github.com/hyperledger/firefly-fabconnect/graphs/contributors)

[https://github.com/hyperledger/firefly-tokens-erc1155/graphs/contributors](https://github.com/hyperledger/firefly-tokens-erc1155/graphs/contributors)

[https://github.com/hyperledger/firefly-dataexchange-https/graphs/contributors](https://github.com/hyperledger/firefly-dataexchange-https/graphs/contributors)

[https://github.com/hyperledger/firefly-cli/graphs/contributors](https://github.com/hyperledger/firefly-cli/graphs/contributors)

[https://github.com/hyperledger/firefly-ui/graphs/contributors](https://github.com/hyperledger/firefly-ui/graphs/contributors)

20 committers - 55% from Kaleido

# Additional Information

Technical metrics from 9/16/2021 to 12/16/2021

[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical?time=%7B%22from%22:%222021-09-16T04:00:00.000Z%22,%22type%22:%22absolute%22,%22to%22:%222021-12-16T05:00:00.000Z%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffirefly/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-09-16T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-12-16T05%3A00%3A00.000Z%22%7D)

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
