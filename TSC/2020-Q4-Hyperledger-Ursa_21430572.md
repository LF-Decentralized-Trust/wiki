1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q4 Hyperledger Ursa

Created by Hart Montgomery, last modified by Gari Singh on Feb 05, 2021

# Project

This report covers Hyperledger Ursa.  We apologize for the fact that it is late.  This can be blamed on @hartm for those looking for a reason.

Project Health

Ursa is reasonably healthy right now.  The bad news:  we have lost some contributors and interest from the Indy ecosystem.  This is mostly because these contributors are happy with the current features that Ursa provides and don't feel the need to improve them, so this isn't a wholly negative thing.  We expect these kinds of contributions to wax and wane, so it's not a truly negative thing, but it does show up in our project metrics.  The good news:  Philip and Mikaela from Scoir, who are relatively new contributors, have done great work on a Go interface from Ursa.  We encourage the projects that heavily use Go to check out ursa-wrapper-go and see for themselves.

In sum, we could always use more contributors, but it's hard to find cryptographers and cryptographic engineers, so we expect our core group to not be too huge.

# Questions/Issues for the TSC

We say something like this in pretty much every report, but we want to reiterate that we are always interested in getting in touch with others who want to use cryptography, and particularly so for people that want to use non-standardized crypto like threshold signatures or zero knowledge proofs.  If this describes you, please feel free to get in touch with us.

Yes, that was a cut and paste, and yes, we will continue to post it.  Please talk to us!

# Releases

We have had three releases from ursa-wrapper-go since our last report.  In particular, v0.1, v0.2, and v0.3 have been released (with v0.3 just recently released two days ago).  In particular, v0.3 does a full round trip of Indy credentials.  Thank you Philip and Mikaela for all your hard work on this!

We didn't have a core Ursa crate this quarter, but expect to release in the not too distant future.  We have a lot of new features that we want to include (see below).

# Overall Activity in the Past Quarter

We had two major foci of activity in the past quarter:

1. We have a Go interface!  Thanks go to Philip and Mikaela.  It's right now focused on Indy credentials, but is certainly extensible.
2. We added code to our core Rust library that handles a variety of secret sharing cases.  Thanks Mike!  While secret sharing itself is not widely used by itself, it is used as a tool for many different kinds of threshold cryptography, which is where we expect to use it.

# Current Plans

We have a number of things on our docket.  In addition to continuing existing work, we are doing the following:

1. Perhaps most notably, we are doing a large reorganization.  All of our "fancy" crypto was structured in the form of a library we called zmix, which was originally designed to be an extensible zero knowledge proof system.  However, the people that designed that, while excellent, moved on from Ursa a while ago.  In the meantime, people have used Ursa in different ways than the zmix design originally anticipated.  As such, we are rearchitecting Ursa to better reflect how people are actually using Ursa today.  Mike and Brent, in particular, have done a great job getting this going.
2. We anticipate including new schemes for revocable credentials in Ursa next quarter.  This contains some of the most complicated crypto we've included in Ursa to this point.  Thanks again to Mike!
3. We plan on streamlining our signature interface for more modular signatures.
4. Threshold signatures.  We've been meaning to do this for a long time, and hopefully now that we have secret sharing implementations that can be used for the initial key distribution, we can make good progress.

# Maintainer Diversity

New Maintainers:

- Mikaela Tarkocheva (Scoir)
- Philip Feairheller (Scoir)

Current (Old) Maintainers:

- Mike Lodder (Independent)
- Brent Zundel (Evernym Inc.)
- Dave Huseby (Linux Foundation)
- Hart Montgomery (Fujitsu)
- Dan Middleton (Intel)
- Cam Parra (Kiva)
- Dan Anderson (Intel)
- Jon Geater (Jitsuin)

Some of these maintainers are obviously more active than others.

# Contributor Diversity

Here is the relevant link from LF Analytics:  [https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22:%22now-90d%22,%22type%22:%22datemath%22,%22to%22:%22now%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22%3A%22now-90d%22%2C%22type%22%3A%22datemath%22%2C%22to%22%3A%22now%22%7D)

The TL;DR is that overall contributions are about static, core contributions are down a little bit, and wrapper contributions are up (thanks Philip and Mikeala!).

While the project continues to move along, we do not have enough diversity to apply for active status at this point in time.  Cryptographers and good cryptographic engineers are hard to find.

# Additional Information

Since Mic Bowman is less involved in Hyperledger these days, we need to offer up another human sacrifice to the dunking booth in order to appease the gods of open source software.  We would like to propose Dan Middleton, although of course we would be happy to consider TSC feedback.

In all seriousness, thanks for reading if you've made it this far and feel free to ask us questions.  Sorry again for the late report!

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

## Attachments:

![](images/icons/bullet_blue.gif) [image2020-12-27\_17-24-57.png](attachments/21430572/21452535.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
