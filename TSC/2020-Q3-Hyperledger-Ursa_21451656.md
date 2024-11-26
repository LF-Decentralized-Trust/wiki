1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2020 Project Updates](2020-Project-Updates_21450093.html)

# Technical Oversight Committee : 2020 Q3 Hyperledger Ursa

Created by Hart Montgomery, last modified by Troy Ronda on Oct 01, 2020

# Project

This report covers Hyperledger Ursa.

Project Health

Ursa has been in a relatively stable state recently.  Contributions have been down a little bit, some of which we attribute to the "summer of COVID" and others due to the fact that some users of Ursa are happy with the existing primitives and want to work on things that are more immediate to their business needs.  We have recently seen a surge in Ursa usage by groups outside of Hyperledger, although unfortunately we have not been able to use this to increase our contributor base.

# Questions/Issues for the TSC

We say something like this in pretty much every report, but we want to reiterate that we are always interested in getting in touch with others who want to use cryptography, and particularly so for people that want to use non-standardized crypto like threshold signatures or zero knowledge proofs.  If this describes you, please feel free to get in touch with us.

# Releases

We released 0.3.4 on Jul 7, 2020 0.3.5 Aug 19, 2020 this quarter, and bbs 0.4.0 on Jul 7, 2020.  Internally, we are on v0.3.6.

The new releases include

- BBS+ work with wasm
- Shamir secret sharing
- BLS signature integration with Signer interface

# Overall Activity in the Past Quarter

We implemented a number of exciting new features in the past quarter, although these are not reflected yet in our current releases&gt;

- We added WASM support for BBS+ signatures as we indicated in our plans in the last report.  The BBS+ signature code is probably our most popular feature, as a number of people outside Hyperledger seem to be using this.
- Upgraded all of our external dependencies on crypto primitives to the latest versions and ensured compatibility.
- Implemented our own version of Shamir secret sharing.  Existing versions don't have the flexibility that we need in Ursa.  For those unaware, Shamir secret sharing (and some other tricks) are widely used across group-based threshold cryptography.  We have demand for threshold crypto implementations, so this is something that we are currently working towards.
- Perhaps most importantly, we agreed to an RFC that details the project structure for the zero knowledge proofs.  This will guide Ursa going forward.
- We did not make much progress on trusted hardware this quarter, unfortunately.

# Current Plans

We have a number of things that we want to build and/or design:

- Threshold cryptography:  we would like to have threshold signatures and other threshold crypto primitives.  We are planning on working towards building these.
  
  - tBLS
  - Feldman VSS
  - Pedersen VSS
- Accumulator work
  
  - RSA
  - ECC
- Post-quantum cryptography:  now that the NIST competition is in the final round, we feel like it is time to start providing options for post-quantum crypto primitives in Ursa.  Luckily, many of the teams behind these new key exchange protocols and signature schemes have written their code in Rust, so hopefully integration should be straightforward.  This will probably necessitate some work on our configuration options for the "base" Ursa primitives.
- Hyperledger Cactus is potentially interested in using Ursa.  This will require effort from both sides, but we may aim to work on our node.js wrappers to help them.

# Maintainer Diversity

Current Active Maintainers:

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

Current Contributor Affiliations:

- Independent (thanks Mike!)
- Evernym, Inc
- Intel
- BCGov
- Iqlusion
- Fujitsu
- Innopolis University (thanks Iroha team!)
- MediConCen Limited

This list is inexact and may be missing some people, but should be representative (lots of people don't have company information listed, and some are mostly working as contractors).  If you should be represented here and are not, please add yourself!  We would also like to thank Ry and others that made collecting all of this information easy with Community Bridge!

# Additional Information

We have received more academic interest in Ursa recently, which has been a very positive development.  In particular, we had a meeting with Prof. Anna Lysyanskaya, an IACR fellow and famous cryptographer, to discuss our CL signatures and open problems regarding anonymous credentials.  We can hopefully get more academic interest in Ursa and use this to stay on the cutting edge of safe cryptography. 

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
