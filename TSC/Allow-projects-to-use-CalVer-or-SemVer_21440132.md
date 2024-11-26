1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Archived](Archived_21447696.html)
4. [TSC Decision Log](TSC-Decision-Log_21437418.html)

# Technical Oversight Committee : Allow projects to use CalVer or SemVer

Created by Danno Ferrin, last modified on Oct 20, 2020

  **Status**

RESOLVED 

**Blocking****Outcome**Approved**Minutes Link**[2020 09 17 TSC Minutes](2020-09-17-TSC-Minutes_21440209.html)

# Overview of Proposal

Allow projects to switch from [SemVer](http://semver.org) (Semantic Versioning) for their versioning to [CalVer](http://calver.org) (Calender Versioning) for their versioning.

Besu is different from a lot of the Hyperledger project in that it is beholden to a standard (Ethereum Mainnet compatibility) that it does not control. While it participates in co-ordination of that standard Besu does not have simple control over it like the other DLT projects do.

When working with public networks such as Mainnet there is a critical need to use the most current version of Besu, no matter what the semantic compatibility is.  Not dealing with a breaking change is the same as dropping the service.  Mainnet is fairly good about maintaining backwards compatibility, but there are other smaller changes such as P2P network protocol upgrades and RPC APIs that update at an infrequent cadence.

Besu feels  that a CalVer versioning for the main DLT release itself would better signal how aligned we are to the continually moving target of mainnet compatibility. We think it will also more clearly communicate multiple release streams should not be expected.

# Formal Proposal(s)

Update the [Release Taxonomy](Release-Taxonomy_21430846.html) to allow project to opt into using Calendar Versioning ([CalVer](http://calver.org)) instead of Semantic Versioning MAJOR.MINOR.PATCH versioning.

Projects that opt in must meet these criteria:

- The project has a regular or semi-regular release schedule that is oriented around release dates
- If there are different points in time where different release processes are used, those need to be documented.
- The project has an established policy for introducing breaking changes
  
  - This policy must allow users sufficient time to adapt to the changes
  - This policy must include the channels used to communicate this (such as prominent placement in CHANGELOG files)
  - Some period of backward compatibility should exist.

For example, Besu's policy would be:

- Besu has triannual to quarterly major releases. These are numbered YY.M.0, such as 20.9.0.
  
  - These releases undergo a two week beta and two week RC cycle,
  - All supported public networks are synchronized and validated to stay in sync
- Besu has fortnightly patch releases. These are numbered YY.M.PATCH, such as 20.9.1
  
  - These releases come off of continuous integration releases
  - A smaller number of select networks are re-synchronized, and previously nodes are upgraded and observed for 24 hours prior to release.
- Breaking changes are only introduced in quarterly changes
  
  - These should have an entire quarter of notice, for example if notice of a breaking change is given in 20.2.4 then 20.5.0 should not implement the change but instead warn that 20.8.0 will implement the change
  - These must be placed prominently at the top of the CHANGELOG for the quarterly release and each patch release for the notice period should reference it.
- If Besu exposes external libraries (such as JNI libraries for cryptography), those should continue to use SemVer.
- Internal versioning of build modules will use CalVer, providing a clear delineation as to what is an API and what isn't.

# Action Items

- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence) to submit a corresponding PR to update the Release Taxonomy

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

Document generated by Confluence on Nov 26, 2024 11:23

[Atlassian](http://www.atlassian.com/)
