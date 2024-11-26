1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q2 Hyperledger Cactus

Created by Hart Montgomery, last modified by Nathan George on Aug 20, 2020

# Hyperledger Cactus Quarterly Report

Project Health

As a brand new project, Hyperledger Cactus seems to be building momentum.  We have had a number of new people (outside of the core Accenture/Fujitsu group that founded Cactus) participate in our meetings and, in some cases, even contribute.  We have presented in the architecture and identity working groups, where we have also garnered a good amount of project interest.  Mostly, however, we are just thrilled to be done with the initial bureaucracy around getting a project approved and set up, and are very happy that we can finally spend most of our time on the architecture and code.

# Questions/Issues for the TSC

We don't have any issues or questions for the TSC at this time.  As we roll out interfaces for different Hyperledger blockchains, though, we would appreciate reviews and comments from people affiliated with said blockchains.  So please expect contact from us in the future!

# Releases

We have not had any notable releases of the combined Cactus codebase, although there are previous releases of the BIF and ConnectionChain.  We hope to have a full Cactus release in the not too distant future.

The releases will be pushed to npm and in a monorepo format but under the npm scope of ***@hyperledger*** meaning that the project name will not be the npm scope but rather just a prefix prior to the package name. This makes it much wordier for the package names, but the upside is that we are consistent with the global Hyperledger npm scope. So the package names will be like this for exmaple:

- @hyperledger/cactus-cmd-api-sever,
- @hpyerledger/cactus-common
- @hyperledger/cactus-sdk,
- etc..

It is not too late to change the package naming theme if the TSC would rather have us our own npm scope such as:

- @cactus/cmd-api-server
- @cactus/common
- @cactus/sdk

Which is easier to read (less verbose), but may be confusing to users who expect all legit Hyperledger projects to publish under the same @hyperledger npm scope.

# Overall Activity in the Past Quarter

The focus of the project at this point has mostly been getting all of the infrastructure set up and working on a modular, combined architecture.  There has been quite a bit of coding going into this as well, but the priorities have been focused on infrastructure.

# Current Plans

Our plans are essentially the following:

1. Finalize our plugin architecture, down to minute specifications needed for implementation.
2. Merge all of the functionality from the Fujitsu and Accenture solutions into our plugin architecture.
3. Add functionality for immediately needed use cases.
4. Design future architectures for things that are needed to scale Cactus to bigger use cases, such as identity management.

# Maintainer Diversity

We currently have four maintainers.  They are:

Shingo Fujimoto – Fujitsu

Jonathan Hamilton – Accenture

Peter Somogyvari – Accenture

Takuma Takeuchi – Fujitsu

We are more than open to adding additional maintainers outside of the core Accenture/Fujitsu group, and hopefully in the not too distant future.

# Contributor Diversity

We recommend the following for detailed contributor information:  [https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard](https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard).  Thanks Ry!

That being said, our contributors are (in lexicographical order) as follows:

Rafael Belchior – Technico Lisboa

Patrick Erichsen – Target

Shingo Fujimoto – Fujitsu

Jonathan Hamilton – Accenture

Tracy Kuhrt – Accenture

Hart Montgomery – Fujitsu

Sownak Roy – Accenture

Peter Somogyvari – Accenture

Takuma Takeuchi – Fujitsu

程阳 – Aliyun

# Additional Information

Thanks for reading this!  

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
