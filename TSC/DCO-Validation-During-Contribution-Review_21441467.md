1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Archived](Archived_21447696.html)
4. [TSC Decision Log](TSC-Decision-Log_21437418.html)

# Technical Oversight Committee : DCO Validation During Contribution Review

Created by Danno Ferrin, last modified by David Enyeart on Apr 15, 2021

  **Status**

PROPOSED 

**Blocking**None blocking, but Besu docs and Fabric docs are regularly impacted**Outcome**  
**Minutes Link**

# Overview of Proposal

Multiple projects have faced issues with new contributors not correctly adding DCO sign off lines in their contributions, and when maintainers attempt to help the new contributors fix the issue the contributor withdraws from the process either implicitly (by ghosting) or explicitly (by saying this is too complex and then withdrawing).  This is most pronounced in the documentation repositories.

The proposed solution would allow for an author to make a DCO declaration outside of the git commits for workflows that support it. A comment in a Github PR would be an example.  Rather than asking the contributor to re-submit their git commits they can assert the DCO in the comments and the maintainers would squash merge the commit.

This is what [Chef](https://blog.chef.io/introducing-developer-certificate-of-origin) does with their DCO statements (see the next to last Q&amp;A question).

# Formal Proposal(s)

If a contributor does not make a DCO statement in each of their commits in a proposed change (via GitHub PR or other similar workflow) they can make a declaration in the comments of the review stream.  Ideally adding the "Signed-off-by: John Doe &lt;john.doe@example.com&gt;" line in the comment stream or another statement such as "this is my work and it complies with the DCO."  It is good form for the maintainers to directly link [https://developercertificate.org/](https://developercertificate.org/) when requesting the contributor provide an in-review stream sign-off. One such claim in a PR will be sufficient for each commit in the PR up to the point of attestation.

When merging such a commit the maintainer will either need to rebase the commit so that all commit entries have a DCO or perform a "squash" commit and enter the DCO. The "signed off by tag" in one of two forms:

- If the contributor provided a "signed off by" tag in the comment stream that tag alone may be used.  The maintainer may optionally add their own tag in addition.
- Otherwise the maintainer will need to provide their own signed off by tag (pursuant to clause c) in one of two forms:
  
  - `Signed-off-by: Jane Maintainer <jmaintainer@example.org>`
  - `Signed-off-by: Jane Maintainer <jmaintainer@example.org> on behalf of John Doe <john.doe@example.com>`

This proposal only applies to commits submitted for review.  All commits in branches that releases of any caliber are built off of (main/master, release branches, patch branches, alpha/beta/nightly) must still contain a signed off by tag in each commit.

Linear merges or linear rebases should not be done for commits covered by this policy.  Squash merges are recommended instead.

## Tooling Impact

The current configuration of the DCO bot will need to be adjusted.  The quickest change is to make the DCO bot check not block merging, although that introduces risk that invalid merges may occur.  A more involved change would be for the DCO bot to check merge comments for a DCO tag.  If the maintainer accepts a non-tag statement they should reply with an "on behalf of" tag in the stream which the DCO bot can pick up.

Projects should be encouraged to add DCO checks into their CI build process.  Such a check would cause the CI to fail to produce a usable output if the DCO validation of the commits fails. These checks are not as universal as the DCO bot. If a project can demonstrate that the DCO checks are caught by their CI system then they would be allowed to drop DCO but errors to advisory errors in the Github PR flow.

# Action Items

- Type your task here, using "@" to assign to a user and "//" to select a due date

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

Document generated by Confluence on Nov 26, 2024 11:23

[Atlassian](http://www.atlassian.com/)
