1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Governance](Governance_22153937.html)

# Besu : Hyperledger Besu Active Status Proposal

Created by Grace Hartley, last modified on Mar 26, 2020

The Hyperledger Besu community would like to request graduation for the project to be moved from incubation to active status. Below outlines an assessment of the requirements of graduating from incubation status to active status and how Hyperledger Besu meets each requirement. From a high-level, we believe we believe the project is ready for active status because:

1. *Diversity of Community and Contributors*: Besu has built an extensive and active community around its project. Some data points around the community include:
2. 1. Since Besu was approved and joined Hyperledger, there have been 29 contributors from the PegaSys team and 20 contributors from outside of the PegaSys team. Since Besu was initially launched in November 2018 (as Pantheon), there have been 42 external contributors to PegaSys while there have been 37 PegaSys contributors.
   2. There have been over 120 community-raised issues on the project since November 2018, when the project was launched. This demonstrates the engagement and excitement around the project.
   3. The project has a diverse maintainer group with 4 organizations being represented. They include, PegaSys (ConsenSys), Chainsafe, Web3Labs, and Machine Consultancy. These teams are major contributors using Besu and providing feedback on the codebase. Additionally, 50+ companies (that we know of) are building blockchain applications have tested out Besu, provided feedback, and demonstrated its usability for their application. Additionally, there are four organizations as maintainers of the project currently.
3. *Besu has demonstrated success using Hyperledger tools and processes:*
4. 1. Public / Community Driven Releases: Each release planning is done during bi-weekly contributor call. Additionally, all releases are announced in our contributors’ RocketChat channel.
   2. Bi-Weekly Contributor Calls: We have had bi-weekly contributor calls to discuss different bodies of work. We are focused on teh
   3. Public Issue Board: We have all issues published on Jira board (Hyperledger’s), but we have recently switched to GItHub issues (under Hyperledger’s account)
   4. RocketChat: While we have struggled with adoption of Ethereum community members on RocketChat, we have been operating successfully on RocketChat with public q&amp;a, feedback, release annoucements, and general community engagement.
5. *Besu is Meant for Production*: Several enterprises are building permissioned networks to use Besu in production. It is also a fully compatible client that runs in production in mainnet Ethereum with its 1.0 Release occurring in April 2020.
6. *The Besu Team Is Heavily Involved in the Hyperledger Community*: Since being accepted as a project in August 2019, the Besu team has been participating in the following activities:
   
   1. [Announcing Hyperledger Besu 1.4](https://www.hyperledger.org/blog/2020/02/27/announcing-hyperledger-besu-v1-4-available-now) (Feb.27)
   2. [How Hyperledger Besu will Help Solve the Pharmaceutical Waste Problem in the U.S.](https://www.hyperledger.org/blog/2020/01/28/how-hyperledger-besu-will-help-solve-the-pharmaceutical-waste-problem-in-the-u-s) (Jan. 28)
   
   <!--THE END-->
7. 01. Added support for Besu in Caliper (Oct. 20)
   02. Participated in the CI/CD working group conversations and sharing our project’s research and best practices (Sep .- Oct.)
   03. Attended the Maintainer summit in Minneapolis (Oct. 8-9)
   04. Presented a talk at the Hyperledger booth at Sibos (Sep.23-25)
   05. Submitted several talks for consideration for the Hyperledger Global Forum and participated in planning of agenda (Sep. - Oct.)
   06. Attended the Hyperledger meet-up at Devcon in Japan (Oct. 9)
   07. Presented privacy solution at Architecture WG - Privacy Confidentiality track (Sep. 20)
   08. Continuing to work on Besu’s support of Caliper (ongoing Oct. - March)
   09. Presented on supply chain SIG (Jan. 23)
   10. Attended the Hyperledger Global Forum and presented several talks (March 9-12)
   11. Attended Hyperledger meet-up in Phoenix (March 9)
   12. Presented at Hyperledger Korea meet-up (Jan. 16)
   13. Provided proposal on DCO process for Hyperledger
   14. Approved to be Co-mentor with Mark Wagner on Hyperledger mentorship project to implement OpenShift on Besu (Mar. 19th)
   15. Published a couple of blogs on Hyperledger’s site:

The assessment against the requirements can be found here:

**Category**

**Requirement**

**Besu Community Response**

**Legal**

All code has been made available under the Apache License and is free of incompatible dependencies

Complete.

Project name has been checked for trademark issues

Complete.

DCO check

Besu Repo:

(lftools) user@dev &gt; ~/Projects/besu &gt; (master) $ git id  
7fbdcbcaa9632351b65323331385864e45e714a7  
(lftools) user@dev &gt; ~/Projects/besu &gt; (master) $ lftools dco check  
Checking commits in branch origin/master for commits missing DCO...  
(lftools) ✘ user@dev &gt; ~/Projects/besu &gt; (master) $

Besu Docs Repo:  
(lftools) user@dev &gt; ~/Projects/besu-docs &gt; (master) $ git id  
34c4aa7931f0632b5bcd62c73b75c84841000b60  
(lftools) user@dev &gt; ~/Projects/besu-docs &gt; (master) $ lftools dco check  
Checking commits in branch origin/master for commits missing DCO...  
(lftools) ✘ user@dev &gt; ~/Projects/besu-docs &gt; (master) $

Run by [David Huseby](https://lf-hyperledger.atlassian.net/wiki/people/5c81ef6e187e8e0b95b0b1e9?ref=confluence)

License check

Notes for besu scan 2019-10-24:

1. The Gradle check-licenses file at /gradle/check-licenses.gradle in lines 139-152 appears to list license choices for a few third party dependencies (to be separately provided and not checked into the source code repo). Two of those listed are for licenses other than Apache-2.0: * javax.ws.rs - CDDL-1.1 * org.checkerframework - MIT Is besu using these dependencies? If so, then under the Hyperledger IP Policy these should likely be included in a license exception request to the Governing Board. I expect it is likely that the GB would grant exceptions to use these as build-time dependencies.
2. Hyperledger's documentation license is Creative Commons Attribution 4.0, CC-BY-4.0. None of the files in besu contained CC-BY-4.0 notices. Consider adding notices to any Hyperledger documentation files, such as: SPDX-License-Identifier: CC-BY-4.0 Most of these documentation files should be listed in the "No license found" tab of the license scan report spreadsheet.
3. Although virtually all besu source code files contain Apache-2.0 license notices, there are a small number of files with no license information. In the "No license found" tab of the spreadsheet, the files with "No license found" do not contain license notices that were detected from our scanning. Where possible, for those that contain Hyperledger code, Apache-2.0 comments should likely be added. This can be done by adding a comment with an SPDX short-form identifier, such as: SPDX-License-Identifier: Apache-2.0 Note that any files in this tab labelled as "third party directory", "excluded file extension" or "empty file" likely do not need to have these notices added. More information for #2 and #3 can be found on the Hyperledger wiki, at [https://lf-hyperledger.atlassian.net/wiki/display/HYP/Copyright+and+License+Policy](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Copyright+and+License+Policy)

Scan report:

[besu-2019-10-24.xlsx](attachments/22153936/22154050.xlsx)

**Community Support**

The project must have an active and diverse set of contributing members representing various constituencies

Hyperledger Besu has active community. We have 217 users on RocketChat. There have been 38 non-PegaSys contributors since the projects’ acceptance into Hyperledger in September 2019 with 191 non-PegaSys contributions total.

Prior to entering Hyperledger the project had [55 contributors](https://github.com/PegaSysEng/pantheon/graphs/contributors) (31 from PegaSys, 24 external) with over 100 external commits and over [200 members of our public Gitter channel](https://gitter.im/PegaSysEng/pantheon).

The project is not highly dependent on any single contributor (there are at least 3 legally independent committers and there is no single company or entity that is vital to the success of the project)

While PegaSys is the main organization that is contributing to Besu, there are several organizations and contributors contributing to Besu, including web3labs, Chainsafe Labs, and Machine Consultancy. We have maintainers from 4 organizations: PegaSys, Web3Labs, Chainsafe labs, and Machine Consultancy.  The ETC Cooperative has also been funding major feature additions, namely Ethereum Classic Support and Keccak256 PoW support.

Release plans are developed and executed in public by the community.

The releases of Pantheon and now Besu have been in a public forum available on the GitHub and the Gitter channel, and RocketChat. We also have set up a bi-weekly contributor call in which release activities are discussed. Meeting minutes and agendas are posted publicly on the [Besu Wiki](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Agendas).

Finer grained details are managed via Jira. Epics, and stories are maintained in Jira, and tracked against versions.

**Test**

Sufficient test coverage

See below.

The project must include a comprehensive unit and integration test suite and document its coverage. Additional performance and scale test capability is desirable.

Currently there are comprehensive unit, integration and acceptance tests with Besu. Merges to master are prevented if there are failing tests.

Performance and scale testing is under development through a partnership with WhiteBlock.

**Documentation**

Sufficient user documentation

Hyperledger Besu team maintains a robust documentation site [here](http://besu.hyperledger.org/en/latest/). 

The project must include enough documentation for anyone to test or deploy any of the modules.

Done. See above.

**Alignment**

Requirements fulfillment

Hyperledger Besu team maintains a robust [Documentation site](http://besu.hyperledger.org/en/latest/) that provides details on requirements, use cases, and other expectations for the project.

The project must document what [requirements and use cases](https://wiki-archive.hyperledger.org/groups/requirements/requirements-wg) it addresses.

Hyperledger Besu team maintains a robust [Documentation site](http://besu.hyperledger.org/en/latest/) that provides details on requirements, use cases, and other expectations for the project.

The project must document how it fits within the [Hyperledger Architecture](https://lf-hyperledger.atlassian.net/wiki/display/AWG/)

Besu’s architecture can be seen in [this blog post.](https://www.hyperledger.org/blog/2019/08/29/announcing-hyperledger-besu) Because it's a mainnet Ethereum client, Besu represents some new considerations and opportunities for the Architecture Working group which require further discussion.

Compatibility with other Hyperledger projects

This is a work in progress that we are excited to continue to engage with the community on. Our team attended the maintainer summit Oct. 8-9 to begin exploring these options.

Where applicable, the project should be compatible with other active projects.

This is a work in progress that we are excited to continue to engage with the community on.

**Alignment**

Release numbering: the project should use the [Hyperledger standard release taxonomy](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Release+Taxonomy), once that is agreed upon.

Besu uses the appropriate naming taxonomy.

Project must make a release, even a “developer preview”, before graduation.

The past releases and the respective documentation for Hyperledger Besu can be found [here](https://github.com/hyperledger/besu/releases).

**Infrastructure**

Gerrit or Github repo has been created

Done and code has been moved. [https://github.com/hyperledger/besu](https://github.com/hyperledger/besu)

[https://github.com/hyperledger/besu-docs](https://github.com/hyperledger/besu-docs)

Mailing lists have been created and are archived

Done: [https://lists.hyperledger.org/g/besu](https://lists.hyperledger.org/g/besu)

Other communication means used, such as slack channels, are set up

Done:

[https://chat.hyperledger.org/channel/besu](https://chat.hyperledger.org/channel/besu)

[https://chat.hyperledger.org/channel/besu-contributors](https://chat.hyperledger.org/channel/besu-contributors)

Project is set up with Continuous Integration

Done

All information necessary for someone to join the community and be able to start contributing is duly documented (location of repo, list of maintainers, mailing lists addresses, slack channels if used, etc) following the Hyperledger Project standard practice ([CONTRIBUTING.md](http://CONTRIBUTING.md), MAINTAINERS.txt, [SECURITY.md](https://github.com/hyperledger/ursa/blob/master/SECURITY.md), etc)

We currently have documentation in the current Docs and Wiki site referenced above.

**CII Badge**

A team seeking to graduate from incubation shall have started the CII Badge application and be nearly complete with incomplete badge requirements referenced in their graduation proposal. 100% of the applicable criteria for the CII Badge is a requirement for releasing a 1.0 of the project. That does not mean the project must have 100% of all criteria, just 100% of the applicable criteria. This is to allow for projects such as test harnesses, that have “N/A” answers for questions that don't offer that as an option.

CII Badge was completed. [Seen here.](https://bestpractices.coreinfrastructure.org/en/projects/3174)

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

Besu has several real world use cases. There are several that are not public. Here are links to a couple of public real world applications being developed using Hyperledger Besu:

1. [LiquidShare](https://pegasys.tech/pegasys-protocol-engineering-liquidshare-partnership/)
2. [IoBuilders](https://pegasys.tech/these-are-the-startups-building-on-pantheon-iobuilders/)
3. [ZarX](https://www.iol.co.za/business-report/companies/watch-zar-x-to-launch-first-blockchain-system-in-sa-for-unit-trusts-33120386)

There is also notable downstream use of Besu code:

1. 41North has created a plugin to export to data to enterprise systems.
2. Web3J uses the EVM to provide CLI Debugging.
3. Rootstock is porting their Unitrie to Besu code.

Scalability - PegaSys has performed several monitoring and benchmarking assessments of Besu.

PegaSys also has a research &amp; development team fully dedicated to the long-term scalability of Ethereum and Hyperledger Besu.

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

## Attachments:

![](images/icons/bullet_blue.gif) [besu-2019-10-24.xlsx](attachments/22153936/22154050.xlsx) (application/vnd.openxmlformats-officedocument.spreadsheetml.sheet)

Document generated by Confluence on Nov 26, 2024 12:59

[Atlassian](http://www.atlassian.com/)
