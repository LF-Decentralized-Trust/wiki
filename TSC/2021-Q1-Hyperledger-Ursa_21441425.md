1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q1 Hyperledger Ursa

Created by Hart Montgomery, last modified by Arun .S.M. on Apr 29, 2021

# Project

This report covers the Hyperledger Ursa project.

Project Health

The health of Ursa has been mixed recently.  Contributions have slowed down.  There are two core reasons for this.  First, our most prolific contributor, Mike Lodder, has spent less time on Ursa recently.  This has had an outsized effect on our project since Mike has done so much for us (thanks Mike!).  Second, a lot of our core contributors came from the Indy/Aries groups.  It seems like that these projects are happy with the cryptography tools currently in Ursa and thus are not spending time working on Ursa.

However, despite contributions being down, Ursa meetings are still well-attended and communication channels are still active.  It seems like many people in Hyperledger (and outside communities) are still interested in using and learning about cryptography, but just not interested in building novel cryptosystems.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes!
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? No.

# Questions/Issues for the TSC

We don't have any current issues or questions for the TSC.

We say something like this in pretty much every report, but we want to reiterate that we are always interested in getting in touch with others who want to use cryptography, and particularly so for people that want to use non-standardized crypto like threshold signatures or zero knowledge proofs.  If this describes you, please feel free to get in touch with us.

Yes, that was a cut and paste, and yes, we will continue to post it.  Please talk to us!

# Releases

We haven't had any releases since our last quarterly report.  Our last release was Dec. 20th.

We anticipate another release once we finish our refactoring.

# Overall Activity in the Past Quarter

Our communication channels continue to be relatively active (they're obviously not Fabric-levels of active, but for us, things move).  The email list doesn't see a lot of traffic but we get a number of questions on rocketchat that are usually answered quickly.

Some accomplishments (code-wise) for the past quarter:

1. Implementation of a go interface for BBS+ signatures.  This will allow arguably our most popular primitive to be used in go projects.  Thanks to Mikaela for leading this!
2. Replacing some older rust base-crypto dependencies with the new k256 crate.  This substantially increased the efficiency of a number of our primitives.  Thanks to a face familiar to the TSC–Dan Middleton–for handling this!

# Current Plans

We have a lot of stuff in the pipeline.  We'll list some things here:

1. Perhaps most notably, we are doing a large reorganization.  All of our "fancy" crypto was structured in the form of a library we called zmix, which was originally designed to be an extensible zero knowledge proof system.  However, the people that designed that, while excellent, moved on from Ursa a while ago.  In the meantime, people have used Ursa in different ways than the zmix design originally anticipated.  As such, we are rearchitecting Ursa to better reflect how people are actually using Ursa today.  Mike and Brent, in particular, have done a great job getting this going.  Mikaela is planning on working on this some as well.
2. At some point, we should have a zero knowledge library contribution.  The goal would be to enable flexible use of ZK proofs in a way that the underlying proof cryptography can be switched out in a modular manner.

At some point this year, we'll work on adding post-quantum implementations.  The timeline for this depends a bit on NIST though.

# Maintainer Diversity

Active Maintainers:

Mikaela Tarkocheva (Scoir)  
Philip Feairheller (Scoir)  
Mike Lodder (Independent)  
Brent Zundel (Evernym Inc.)  
Dave Huseby (Independent)  
Hart Montgomery (Fujitsu)  
Dan Middleton (Intel)

We have more maintainers, but this is the group that generally participates actively.  We note that we are super excited to have Dave Huseby in a non-LF capacity.

# Contributor Diversity

Here is the link from LF analytics:  [https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22:%22now-90d%22,%22type%22:%22datemath%22,%22to%22:%22now%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22%3A%22now-90d%22%2C%22type%22%3A%22datemath%22%2C%22to%22%3A%22now%22%7D).

As we discussed before, contributions are down, which the link shows.  Use of Ursa has probably gone up, but we don't have effective ways of tracking or verifying this.

# Additional Information

Dan Middleton is back in the dunking booth!

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
