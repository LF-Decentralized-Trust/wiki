1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q2 Hyperledger Ursa

Created by Hart Montgomery, last modified by Gari Singh on Oct 16, 2021

# Project Health

The health of Ursa has continued to be mixed.  Contributions have not picked up dramatically.  Our core maintainers and contributors have continued to be quite busy, and a lot of progress on things we want to accomplish has been slow.  To combat this, we are working with Ry and David B to better optimize community outreach efforts (well, really put them together in the first place).  We haven't done a good job on a lot of things in this area, and think that we can improve with their help.  We also saw a lot of interest in Ursa due to the global forum (no contributions yet, but people joining our channels) so we hope that we can build on this momentum. 

However, despite contributions being down, Ursa meetings are still well-attended and communication channels are still active.  It seems like many people in Hyperledger (and outside communities) are still interested in using and learning about cryptography, but just not interested in building novel cryptosystems.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes!
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? No.

# Questions/Issues for the TSC

We don't have any current issues or questions for the TSC.

We say something like this in pretty much every report, but we want to reiterate that we are always interested in getting in touch with others who want to use cryptography, and particularly so for people that want to use non-standardized crypto like threshold signatures or zero knowledge proofs.  If this describes you, please feel free to get in touch with us.

Yes, that was a cut and paste, and yes, we will continue to post it.  Please talk to us!

# Releases

We had a minor release (v0.3.6) in May.  We are still working towards our refactoring, and will have a major release when that happens, but have just been slow.  Our core contributors and code reviewers have been very, very busy.

# Overall Activity in the Past Quarter

Our communication channels continue to be relatively active (they're obviously not Fabric-levels of active, but for us, things move).  We have noticed a recent uptick in traffic, which has been nice and maybe correlated with the HGF.  The email list doesn't see a lot of traffic but we get a number of questions on rocketchat that are usually answered quickly.  

Some accomplishments (code-wise) for the past quarter:

1. We released v0.3.6.  Thanks Mike!
2. We added some optimizations to the BBS+ signature suite (these are not cryptographic in nature).  Thanks to Andrew Whitehead for handling this!
3. We cleaned up some of our test cases.  Thanks Nathan!

# Current Plans

We have a lot of stuff in the pipeline.  We'll list some things here:

1. Perhaps most notably, we are *still* doing a large reorganization.  It's been slow.  All of our "fancy" crypto was structured in the form of a library we called zmix, which was originally designed to be an extensible zero knowledge proof system.  However, the people that designed that, while excellent, moved on from Ursa a while ago.  In the meantime, people have used Ursa in different ways than the zmix design originally anticipated.  As such, we are rearchitecting Ursa to better reflect how people are actually using Ursa today.  Mike and Brent, in particular, have done a great job getting this going.
2. At some point, we should have a zero knowledge library contribution.  The goal would be to enable flexible use of ZK proofs in a way that the underlying proof cryptography can be switched out in a modular manner.

At some point this year, we'll work on adding post-quantum implementations.  The timeline for this depends a bit on NIST though.

In terms of community management, we our discussing with Ry and David B about how to better do community outreach so that we can find more contributors and users.  We recognize that it is hard to find talented cryptographers and cryptographic engineers with time to contribute, but we need to expand our contributor base and so are going to make a concerted effort to do so.

# Maintainer Diversity

Active Maintainers:

Mike Lodder (Independent)  
Brent Zundel (Evernym Inc.)  
Dave Huseby (Independent)  
Hart Montgomery (Fujitsu)  
Dan Middleton (Intel)

We have more maintainers, but this is the group that generally participates actively.  

# Contributor Diversity

Here is the link from LF analytics:  [https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22:%22now-90d%22,%22type%22:%22datemath%22,%22to%22:%22now%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22%3A%22now-90d%22%2C%22type%22%3A%22datemath%22%2C%22to%22%3A%22now%22%7D).

We are hoping to see a bump from the HGF and outreach efforts so that we can increase this.

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
