[invalid_url] err=parse "http://Hyperledger Iroha": invalid character " " in host name url="http://Hyperledger Iroha" 
1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Archived](Archived_21447696.html)
4. [TSC Decision Log](TSC-Decision-Log_21437418.html)

# Technical Oversight Committee : Move Hyperledger Explorer from incubation to active status

Created by Nick Frunza, last modified by Nathan George on May 06, 2021

**Status**

WITHDRAWN 

**Outcome****Minutes Link**

# Overview of Proposal

The Hyperledger Explorer community would like to apply for the project to be moved from incubation to active status. Below outlines an assessment of the requirements of graduating from incubation status to active status and how Hyperledger Explorer meets minimum requirement. We believe we believe the project is ready for active status because:

1. Diversity of Community and Contributors: Hyperledger Explorer (aka Blockchain Explorer) since the proposal back in 2016 has been extensively used, and improved by feedbacks, and raised issues [feedbacks, and raised issues](https://jira.hyperledger.org/secure/RapidBoard.jspa?rapidView=155) from the community.
   
   1. The project has been maintained by various [contributors](https://github.com/hyperledger/blockchain-explorer/graphs/contributors) durring this period, and continue to be. On average there are more than 250 [unique GitHub cloners](https://github.com/hyperledger/blockchain-explorer/graphs/traffic) weekly, and more than 100K pulls from the docker hub [Docker Hub](https://hub.docker.com/r/hyperledger/explorer/).
   2. There are many companies already using Hyperledger Explorer in production worldwide industries like: financial, banking institutions, educational, government, science, etc,  but due to their non-disclosure policy we cannot collect that information.
2. Release 1.0-rc1 Occurred recently in November 2019.
3. Hyperledger Explorer is a valuable tool for exploring a Hyperledger Fabric permissioned blockchain. 
   
   1. Easily configurable to connect to any Hyperledger Fabric network.
   2. Designed to implementation, and support other blockchain platforms.
   3. Integrated with PostgreSQL to search, and filter historical data.
4. The Hyperledger Explorer has been participated in multiple hackfests, meetups, and others.
   
   1. Hyperledger Hackfests/Meetups
      
      1. [Hyperledger Chennai Meetup - December 2018](https://www.meetup.com/Hyperledger-Colombo/events/256376595/)
      2. [Montreal- October 2018](https://drive.google.com/open?id=1pYhoy5CxgSyXclIsQs-W8yaIcndjfD-qPWvJmpAehP0)
      3. [Los Angeles - February 2018](https://docs.google.com/document/d/14yNuJsFEWnVsAclKb1QjPluRKgz3rIpaApRSppJj6to/edit)
      4. [San Francisco - February 2017](https://drive.google.com/open?id=12GHlJlX0NntEtiVYwl1w0V6JRibD66LuAmKBGGRxxfo)
      5. [NYC - December 2016](https://docs.google.com/document/d/1iokahBpG7U8TuYn-HmAUCfzLsbq-5L1zW6oWe1ymuv4/edit)
5. Hyperledger Explorer links:
   
   01. [Wiki page](https://lf-hyperledger.atlassian.net/wiki/display/explorer/)
   02. [Hyperledger Explorer](https://www.hyperledger.org/projects/explorer)
   03. [CII Best Practices Badge](https://bestpractices.coreinfrastructure.org/en/projects/2710)
   04. [Read the docs](https://blockchain-explorer.readthedocs.io/en/master/index.html)
   05. [GitHub](https://github.com/hyperledger/blockchain-explorer)
   06. [Docker Hub](https://hub.docker.com/r/hyperledger/explorer)
   07. [Jira](https://jira.hyperledger.org/projects/BE/issues)
   08. [Rocket Chat](https://chat.hyperledger.org/channel/hyperledger-explorer)
   09. [Azure Pipeline](https://dev.azure.com/Hyperledger/blockchain-explorer/_build)
   10. Retired 
       
       1. [Gerrit](https://gerrit.hyperledger.org/)
       2. [Jenkins](https://jenkins.hyperledger.org/view/blockchain-explorer/)

The assessment against the requirements can be found below, and the [CII Best Practices](https://bestpractices.coreinfrastructure.org/en/projects/2710).

**Category**

**Requirement**

**Hyperledger Explorer Community Response**

**Legal**

All code has been made available under the Apache License and is free of incompatible dependencies

done

Project name has been checked for trademark issues

DCO check

done

License check

Jira assigned [BE-723](https://jira.hyperledger.org/browse/BE-723 "BE-723")

**Community Support**

The project must have an active and diverse set of contributing members representing various constituencies

Hyperledger Explorer has an active community,  

The project is not highly dependent on any single contributor (there are at least 3 legally independent committers and there is no single company or entity that is vital to the success of the project)

DTCC is the main organization that is contributing to Hyperledger Explorer, and actively contributors from Fujitsu. Past contributing organizations: Altoros, American Express, Blockchain Tecnalia, and [other contributors](https://github.com/hyperledger/blockchain-explorer/graphs/contributors).

Release plans are developed and executed in public by the community.

The releases of Hyperledger Explorer have been in a public forum available on the GitHub, Docker Hub, and RocketChat. We do communicate using Rocket Chat, and Zoom meeting, as needed.

Sprints are managed via Jira. Epics, and stories are maintained in Jira, and tracked against versions.

**Test**

Sufficient test coverage

See below.

The project must include a comprehensive unit and integration test suite and document its coverage. Additional performance and scale test capability is desirable.

Currently there are comprehensive unit, integration and acceptance tests with Hyperledger Explorer that are triggered by  [Azure Pipeline](https://dev.azure.com/Hyperledger/blockchain-explorer/_build) on pull requests by contributors.  Merges to master are reviewed by approvers, and prevented if there are failing tests.

**Documentation**

Sufficient user documentation

Hyperledger Explorer team maintains a [blockchain-explorer.readthedocs.io](https://blockchain-explorer.readthedocs.io/en/master/index.html), and [README.md](https://github.com/hyperledger/blockchain-explorer/blob/master/README.md) documentation.

The project must include enough documentation for anyone to test or deploy any of the modules.

Done. See above.

**Alignment**

Requirements fulfillment

Hyperledger Explorer team maintains a [Jira](https://jira.hyperledger.org/projects/BE/issues) that provides details on requirements, use cases, and other expectations for the project created from the community feedback and reported issues.

The project must document what [requirements and use cases](https://wiki-archive.hyperledger.org/groups/requirements/requirements-wg) it addresses.

Hyperledger Explorer team maintains a robust [Documentation site](http://besu.hyperledger.org/en/latest/) that provides details on requirements, use cases, and other expectations for the project.

The project must document how it fits within the [Hyperledger Architecture](https://lf-hyperledger.atlassian.net/wiki/display/AWG/)

Hyperledger Explorer was designed based on initial proposal [initial proposal](https://docs.google.com/document/d/1GuVNHZ5Jqq-gTVKflnZ1YiJfEoozvugqenC6QEQFQj4/edit), and enhanced since the beginning of the project  by the community feedback and reported issues in [Jira](https://jira.hyperledger.org/projects/BE/issues).

Compatibility with other Hyperledger projects

Hyperledger Explorer is a tool that can be connected to any Hyperledger Fabric blockchain network, also it is designed to implement any other blockchain platform. The are are some potential projects that can be added as part of the Explorer, like  [Hyperledger Iroha](http://Hyperledger%20Iroha).

Where applicable, the project should be compatible with other active projects.

This is a work in progress that we are excited to continue to engage with the community on.

**Alignment**

Release numbering: the project should use the [Hyperledger standard release taxonomy](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Release+Taxonomy), once that is agreed upon.

Hyperledger Explorer uses the appropriate naming taxonomy.

Project must make a release, even a “developer preview”, before graduation.

The past releases and the respective documentation for Hyperledger Explorer can be found [here](https://github.com/hyperledger/blockchain-explorer/releases).

**Infrastructure**

Github repo has been created

[GitHub](https://github.com/hyperledger/blockchain-explorer/releases)

Mailing lists have been created and are archived

[Mailing lists](https://lists.hyperledger.org/g/explorer)

Other communication means used, such as slack channels, are set up

[Rocket chat hyperledger-explorer channel](https://chat.hyperledger.org/channel/hyperledger-explorer)

[Rocket chat hyperledger-developers channel](https://chat.hyperledger.org/channel/hlexplorer-developers)

Project is set up with Continuous Integration

 [Azure Pipeline](https://dev.azure.com/Hyperledger/blockchain-explorer/_build)

All information necessary for someone to join the community and be able to start contributing is duly documented (location of repo, list of maintainers, mailing lists addresses, slack channels if used, etc) following the Hyperledger Project standard practice ([CONTRIBUTING.md](http://contributing.md/), MAINTAINERS.txt, [SECURITY.md](https://github.com/hyperledger/ursa/blob/master/SECURITY.md), etc)

We currently have documentation in the current Docs and Wiki site referenced above.

**CII Badge**

A team seeking to graduate from incubation shall have started the CII Badge application and be nearly complete with incomplete badge requirements referenced in their graduation proposal. 100% of the applicable criteria for the CII Badge is a requirement for releasing a 1.0 of the project. That does not mean the project must have 100% of all criteria, just 100% of the applicable criteria. This is to allow for projects such as test harnesses, that have “N/A” answers for questions that don't offer that as an option.

[CII Best Practices](https://bestpractices.coreinfrastructure.org/en/projects/2710).

**Other Considerations**

Sufficient real world use

The project should be used in real applications and not just in demos. Because not all real applications may be discussed publicly, in such cases statements providing as much detail as possible should be made.

Sufficient scalability

The project must demonstrate sufficient scalability and document its scalability over various dimensions such as:

- Maximum number of transactions per second
- Maximum number of transactions per chain
- Maximum size of a block

Minimum test code coverage expected, such as, for example:

- Minimum coverage for Security &amp; cryptography
- Minimum coverage for other functionality
- Minimum coverage for Business logic/smart contract

There are many companies already using Hyperledger Explorer in production worldwide industries like: financial, banking institutions, educational, government, science, etc,  but due to their non-disclosure policy we cannot collect that information. 

Scalability - Hyperledger Explorer has performed several monitoring and benchmarking assessments of explorer. We have tested and created  ["How to configure with Prometheus, and Grafana" instructions.](https://github.com/hyperledger/blockchain-explorer/blob/master/CONFIG-OPERATIONS-SERVICE-HLEXPLORER.md)

The main dashboard page of the Hyperledger Explorer had a [detailed metrics panel](https://blockchain-explorer.readthedocs.io/en/master/presentation/index.html#metrics) on the blocks, and transactions per hour, and minutes.

Formal Proposal(s)

Move Hyperledger Explorer from incubation to active status

# Action Items

- Type your task here, using "@" to assign to a user and "//" to select a due date

# Reviewed By

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

## Attachments:

![](images/icons/bullet_blue.gif) [github\_hlexplorer\_stats.png](attachments/21430602/21449666.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:23

[Atlassian](http://www.atlassian.com/)
