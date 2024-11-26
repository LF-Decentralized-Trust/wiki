1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q3 Hyperledger Quilt

Created by David Fuelling, last modified by Mark Wagner (Deactivated) on Sep 26, 2019

# Project

[Hyperledger Quilt](https://github.com/hyperledger/quilt)

Project Health

Project health over Q1/Q2 of 2019 has been poor, although I (David Fuelling) would like this to improve in Q3 2019 and beyond. Some things that have changed over the past month that are important to note:

1\) The TSC decided that the Quilt project should be limited to Interledger (ILP) Java, which is its current charter (i.e., the "reboot" [will not proceed](https://lists.hyperledger.org/g/quilt/topic/32846626)). While I supported the reboot and at the time was unable to assume leadership of the Quilt project, I am now in a position to actively maintain the project, especially since it will be limited to an Interledger Java focus.

2.) There has been renewed interest in Interledger Java, even over the past month. First, organizational support is expanding around ILP Java, so I expect there to be at least 3 full-time engineers (myself included) with bandwidth to focus on Quilt and Java software built around Quilt by the end of Q3 2019. Additionally, the project has recently had a new unaffiliated contributor who has [begun submitting PRs](https://github.com/hyperledger/quilt/pulls?utf8=%E2%9C%93&q=%20is%3Apr%20author%3Asudheesh001%20), so by the end of Q3, I expect project health to be improved as compared to H1 2019.

# Issues

Given the various potential changes discussed in Q1/Q2 2019 in the Quilt project, there is confusion around the focus of the project, who will lead it and maintain it, and what its future will be. I am interested in revitalizing the Quilt project and begin shipping ILP code around it. However, if the TSC feels that this effort is too late, or the charter of the project doesn't align with the broader focus of Hyperledger, then this is potentially something to clarify.

To this end, I sometimes find it difficult to know what is expected by the TSC in terms of tasks or reports that project maintainers should be delivering. This is likely just because I have never filled this role before (prior to the reboot these tasks were performed by a maintainer who is no longer able to contribute), but I was unaware of [this page](https://lf-hyperledger.atlassian.net/wiki/display/HYP/TSC+Project+Updates), as an example. Are there other TSC reporting requirements of the project lead other than these reports?

# Releases

Quilt has had only [SNAPSHOT releases](https://oss.sonatype.org/content/repositories/snapshots/org/interledger/) thus far. However, we are targeting a 1.0 release of Quilt Core (see [remaining tasks here](https://github.com/hyperledger/quilt/issues?q=is%3Aopen%20is%3Aissue%20label%3Av1.0)) by the end of Q3. Follow-on deliverables will be identified after this release. 

# Overall Activity in the Past Quarter

Activity over the past quarter started off light. However, in late August/early-september, activity picked-up ([5 PRs](https://github.com/hyperledger/quilt/pulls?utf8=%E2%9C%93&q=%20is%3Apr%20author%3Asudheesh001%20) were merged). From mid Sept to the end of the month, participation and activity [has been very robust](https://github.com/hyperledger/quilt/projects/2), with many tasks completed towards providing Interledger [STREAM](https://github.com/interledger/rfcs/blob/master/0029-stream/0029-stream.md) support in the Quilt library (this will allow Quilt clients to interact with Interledger Connectors for the first time!).

# Current Plans

We are currently planning to release [v1.0 of Quilt](https://github.com/hyperledger/quilt/issues?q=is%3Aopen%20is%3Aissue%20label%3Av1.0) by Sept 30th, 2019. This will include core libraries to support ILP sender &amp; receiver functionality, including support for the [STREAM](https://github.com/interledger/rfcs/blob/master/0029-stream/0029-stream.md) protocol, which will be a large enabler for applications built on top of Quilt libraries. That said, today's Quilt is currently limited to core-libraries underpinning ILP (IL-DCP, BTP, Core packets, OER serialization, etc). Over the coming month we will be discussing potential additional contributions to the project, including an ILP Sender, ILP Receiver, and possibly an ILP Connector/Router as well.

# Maintainer Diversity

Two new maintainers have been added in Q3: ([https://github.com/nhartner](https://github.com/nhartner)) and ([https://github.com/theotherian](https://github.com/theotherian)). Including myself, there are now three maintainers. While our technical diversity is strong, we are all funded by the same company, so from this perspective diversity is low.

# Contributor Diversity

Currently contributions are coming from developers at [Ripple/Xpring](https://xpring.io/) and the University of Washington (e.g., [https://github.com/sudheesh001](https://github.com/sudheesh001)), with some less regular contributions coming from developers at [Coil](https://coil.com/).

# Additional Information

Not at this time.

# Reviewed by

- Arnaud Le Hors
- Baohua Yang
- Binh Nguyen
- Christopher Ferris
- Dan Middleton
- Hart Montgomery
- Kelly Olson
- Mark Wagner
- Mic Bowman
- Nathan George
- Silas Davis

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
