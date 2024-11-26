1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q3 Hyperledger Ursa

Created by Hart Montgomery, last modified by Gari Singh on Oct 16, 2021

Project Health

The health of Ursa has stabilized, although it continues to be mixed.  Our contributions were especially low this quarter:  pretty much only some basic upkeep stuff was done.  However, some of this is due to the fact that we have been working on some pretty huge feature improvements coming soon, and these will be contributed in the near future.  We will explain more on this later.

We have not done as much as we would have liked this quarter to better optimize community outreach efforts.  Ry and David B have committed to helping us, and we will work with them  this fall to get moving on outreach.  Unfortunately, we are heavily dependent on a small handful of core contributors, and if they get busy (which happened this summer), then large-scale progress tends to slow down.

However, despite contributions being down, Ursa meetings are still well-attended and communication channels are still active.  It seems like many people in Hyperledger (and outside communities) are still interested in using and learning about cryptography, but just not interested in building novel cryptosystems.  We have also garnered more interest from the Aries community, mostly through discussing a BBS+ LD-proof vulnerability (essentially, a proof construction leaks more information than is desirable).  This is an interesting case where a higher-layer use pattern causes undesirable security properties.  More communication between the Aries and Ursa contributors is a step in the right direction towards Ursa health, and, in our opinion, the health of Hyperledger as a whole.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes.
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? No, sorry.

# Questions/Issues for the TSC

We don't have any current issues or questions for the TSC.

We say something like this in pretty much every report, but we want to reiterate that we are always interested in getting in touch with others who want to use cryptography, and particularly so for people that want to use non-standardized crypto like threshold signatures or zero knowledge proofs. If this describes you, please feel free to get in touch with us.

Yes, that was a cut and paste, and yes, we will continue to post it. Please talk to us!

# Releases

We did not have a release since the last report (our last release was in May).  However, we should have a new release very soon (perhaps by the time you read this), so we will maintain at least a not unreasonable release cadence.

# Overall Activity in the Past Quarter

Our communication channels continue to be relatively active (they're obviously not Fabric-levels of active, but for us, things move). We have noticed a recent uptick in traffic, which has been nice and maybe correlated with the HGF. The email list doesn't see a lot of traffic but we get a number of questions on rocketchat that are usually answered quickly.

We didn't have a lot of big code contributions show up:  there was basically just maintenance work.

On the other hand, there has been a lot of work done recently (with the intention of contributing it to Ursa) that has not made it in to Ursa yet.  In particular, we expect to add to Ursa some exciting new zero knowledge proof functionality in the form of a "compiler" that takes R1CS representations of statements and can "compile" them into ZK proofs using a number of different backend systems.  This will enable us to keep high-level, application layer crypto code the same while switching ZK backends as the ZK proof systems themselves improve and change.  Although this has not been contributed yet, we have talked extensively about it, and certain members of the Ursa community (Avradip, and especially Mike) have spent a lot of time on it.  So we think this qualifies as overall activity even if it hasn't made its way to Ursa yet.

# Current Plans

Our immediate plans involve getting our new ZK code merged into Ursa.  This should allow people to use ZK proofs more easily, and we know that some companies that use Hyperledger are planning on putting this library to work in practice (Fujitsu, for one).  

At some point this year, we'll work on adding post-quantum implementations. The timeline for this depends a bit on NIST though.  We also need to see when people start demanding post-quantum crypto, as this hasn't happened to a large degree in the blockchain space yet (possibly because some post-quantum protocols, like zero-knowledge proofs, are extremely expensive computationally).

In terms of community management, we our discussing with Ry and David B about how to better do community outreach so that we can find more contributors and users. We recognize that it is hard to find talented cryptographers and cryptographic engineers with time to contribute, but we need to expand our contributor base and so are going to make a concerted effort to do so.

# Maintainer Diversity

Mike Lodder (Independent)

Brent Zundel (Evernym Inc.)

Dave Huseby (Independent)

Hart Montgomery (Fujitsu)

Dan Middleton (Intel)

We have more maintainers, but this is the group that generally participates actively.  

# Contributor Diversity

Here is the link from LF analytics:  [https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22:%22now-90d%22,%22type%22:%22datemath%22,%22to%22:%22now%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22%3A%22now-90d%22%2C%22type%22%3A%22datemath%22%2C%22to%22%3A%22now%22%7D).  

Our contribution levels are low this quarter, but we expect to see a number of substantial contributions hit soon (e.g. the ZK proof framework we have mentioned earlier).

# Additional Information

We don't have a whole lot else to say!  

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
