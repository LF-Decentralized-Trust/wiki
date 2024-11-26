1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q4 Hyperledger Ursa

Created by Hart Montgomery, last modified by Danno Ferrin on Jan 20, 2022

Project Health

This was a difficult quarter for Ursa–probably the worst quarter for it ever.  Not a lot got done due to a combination of factors, which included core contributors being too busy to contribute (or, in some cases, people leaving contributing organizations) and the holiday period slowing everything to a crawl.

However, not all is gloom and doom:  there is renewed interest from end users of Ursa (particularly through Aries) and we will do a security audit soon.  As such, we are planning on soliciting contributions from companies related to these end users (i.e. people using Aries) and some of these folks have already agreed to help (thanks Cam and others!).  This transition will not be immediate but hopefully Ursa will come out of it stronger than ever.

We are also still planning on incorporating some rather large contributions soon (hopefully by the time you will be reading this), including a nice new zero knowledge framework.  These have just been bogged down due to the holidays and lack of contributor availability.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)?  Yes.
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)?  No, we are undergoing a (very slow) migration to a different repo structure and things aren't totally done yet, so we haven't modified the old repos to support the CRS.  Sorry about this.  The new repo structure will have the CRS implemented though.

# Questions/Issues for the TSC

We don't have any current issues or questions for the TSC.

We say something like this in pretty much every report, but we want to reiterate that we are always interested in getting in touch with others who want to use cryptography, and particularly so for people that want to use non-standardized crypto like threshold signatures or zero knowledge proofs. If this describes you, please feel free to get in touch with us.

Yes, that was a cut and paste, and yes, we will continue to post it. Please talk to us!

# Releases

We were planning on releasing this quarter, but did not get around to it due to the aforementioned issues.  We are planning on rectifying this in the next quarter.

# Overall Activity in the Past Quarter

Our communication channels continue to be relatively active (they're obviously not Fabric-levels of active, but for us, things move). The email list doesn't see a lot of traffic but we get a number of questions on rocketchat that are usually answered quickly.

Our big code contributions got stalled.  We plan on getting these in soon.  In particular, we expect to add to Ursa some exciting new zero knowledge proof functionality in the form of a "compiler" that takes R1CS representations of statements and can "compile" them into ZK proofs using a number of different backend systems.  This will enable us to keep high-level, application layer crypto code the same while switching ZK backends as the ZK proof systems themselves improve and change.  Although this has not been contributed yet, we have talked extensively about it, and certain members of the Ursa community (Avradip, and especially Mike) have spent a lot of time on it.  

# Current Plans

Our immediate plans involve getting our new ZK code merged into Ursa.  This should allow people to use ZK proofs more easily, and we know that some companies that use Hyperledger are planning on putting this library to work in practice (Fujitsu, for one).   We also have a backlog of some relatively routine maintenance work.  As we mentioned before, we also are planning on working on a security audit soon.

Assuming we have bandwidth, at some point this year, we'll work on adding post-quantum implementations. The timeline for this depends a bit on NIST though.  We also need to see when people start demanding post-quantum crypto, as this hasn't happened to a large degree in the blockchain space yet (possibly because some post-quantum protocols, like zero-knowledge proofs, are extremely expensive computationally).

In terms of community management, we our discussing with Ry and David B about how to better do community outreach so that we can find more contributors and users. We recognize that it is hard to find talented cryptographers and cryptographic engineers with time to contribute, but we need to expand our contributor base and so are going to make a concerted effort to do so.

# Maintainer Diversity

Mike Lodder (Independent)

Brent Zundel (Evernym Inc.)

Dan Anderson (Intel)

Cam Parra (Kiva)

Hart Montgomery (Fujitsu)

Dan Middleton (Intel)

We have more maintainers, but this is the group that generally participates actively.  

# Contributor Diversity

Here is the link from LF analytics:  [https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22:%22now-90d%22,%22type%22:%22datemath%22,%22to%22:%22now%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22%3A%22now-90d%22%2C%22type%22%3A%22datemath%22%2C%22to%22%3A%22now%22%7D).  

It's not pretty, but hopefully will be better next quarter.

# Additional Information

We don't really have much to add.  This quarter has been a struggle but we aim to turn things around soon.

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
