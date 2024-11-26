1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Developing and Conventions](Developing-and-Conventions_22153909.html)
4. [Releasing](Releasing_22154097.html)
5. [Obsolete Proposals and Policies](Obsolete-Proposals-and-Policies_22154144.html)

# Besu : Proposal for Off-Cycle, Delayed, and Scuttled Releases

Created by Matt Nelson (Deactivated), last modified by Danno Ferrin on Dec 14, 2022

# Principals

The principals of this release process should reflect the networks it is supporting: censorship resistance, freedom to transact, and byzantine fault tolerance.

There are also four principal use cases that the Besu code supports, and should continue to support:

- Ethereum Mainnet Client
- Ethereum Classic Client
- Enterprise Ethereum Client
- EVM Library

Release decisions and processes should be beneficial to all, and should not advance one use case at the expense of other use cases.  If a conflict is identified effort should be expended to ensure that the advancement of one use case is at least neutral to all use cases.

# Release Committee

A release committee will be established (much like existing ad-hoc and de-facto security and github administration committees). Voting procedures and committee composition will be set up to ensure that a *change* in releases cannot be done by a single use case or a single company, and that such changes require co-operation among the committee (where such co-operation shall not be unreasonably denied).

## Possible formulations:

- Release Committee is all maintainers.  For a change to pass a "diverse majority" is required, including a majority of committers and committers from two or more employers. The downside is a majority of one interest/company can block any change, even though they cannot force a change.
- Smaller 5-seat committee, one seat for each use case and one at large seat.  Release Committee members need not be maintainers.  The downside is a small committee can force a change over the majority of committers.  This is, however, closer to the battle tested Apache PMC model.

## Votes are to change

All votes represent a change from the published schedule.  If a diverse majority cannot agree on a change then the prior action stands and is acted upon.

## "Without Objection" actions.

Scheduled releases proceed on a "without objection" basis, where it is presumed that there is consensus to proceed. 

- Any maintainer or release committee member may, within a reasonable timeframe, raise an objection to an action.  This pauses an action until a vote of the release committee concludes.
- Release committee members then vote within a reasonable time frame.
- Votes do not close until there is a "diverse opinion," i.e. multiple companies and multiple interests, but they may close because a resonable time has passed or the outcome is clear.
- If a diverse opinion cannot be gathered then the action remains paused until such an opinion is registered.
- A reasonable timeframe scales with the urgency of the concern.  A regular release would have at least a business day, whereas a security risk under active exploit may only have until the PR has cleared CI.

# Scheduled Releases

- The release committee can set and change a release schedule.
- The current schedule is a two-week release cadence with a 6 week quarterly release where large breaking changes unrelated to hard forks are introduced.
- The release cadence includes a [burn in period as described on another page](22155972.html).
  
  - The release committee may waive the burn in period and change the checkpoints of a particular scheduled release.  This is a change and requires a Release Committee vote.
- The release consists of the current head of the "main" branch, selected in a timeframe appropriate for the burn-in testing schedule.
  
  - The release committee may change a scheduled release to be a "cherry-picked" release, such an action is considered a change and requires a Release Committee vote.
- Progression of the release proceeds on a "without objection" basis, where expected objections may be significant performance regressions, failures in testing outside the scope of CI, or discovery of security issues that may warrant scuttling the release.
- A vote of the Release Committee is required to scuttle a scheduled release. The change is to scuttle the release.
  
  - If an objection is raised the release is paused until the Release Committee vote concludes.

## Patch releases during Quarterly Releases

- If there is a quarterly release underway the release may be accompanied by a patch release of the prior generation.
- Any release committee member may propose a patch release, at least 24 hours prior to any burn-in process cutoff
- Release committee members propose PRs to be cherry picked into a release.
- All proposed cherry picks are accepted on a "without objection" basis.
  
  - The default action is no patch release and a patch release with specific contents is the change the release committee is voting on.
- A separate release manager may run the patch release.

# Off-Cycle Releases

- Maintainers and Release Committee members may propose a release that is not on the release schedule.
- The contents and timeframe of the release are part of the proposal.
- Release committee members should consider the following issues in their vote
  
  - How close the next release is scheduled
  - How widespread the issue is the off-cycle release would address
  - Issues addressing consensus failures and scheduled hard forks
  - Scope and impact of security issues in the proposed release.
- Release Committee members are expected to be prompt in reviewing requests for off-cycle releases, as these are typically time sensitive.
- The default action is not to do an off cycle release.  The Release Committee vote is to change to do an Off-Cycle Release.

# Context

\[The following is context from the discord chat, but is not considered part of the process itself]

The following proposal is intended to address issues in the current process for Besu Maintainers to propose off-cycle, delayed, or scuttled releases. This proposal does not conflict with the [burn-in process outlined here](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Process+change+proposal%3A+burn-in?src=contextnavpagetreemode), and intends to build upon it. Both processes should be maintained, if accepted. 

Off-cycle, Delayed, and Scuttled releases are defined as any release altered from its date on the [release schedule](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Release+Rotations+2022) by more than 24 hours (to accommodate contributor time-zones), either pulled forward to address a critical bug or patch, delayed to accommodate bugs or issues exposed during the release (n-5) burn-in period, or something extenuating to require scuttling the entire release. 

A release committee would be established to make go/no-go decisions on moving releases. This committee is comprised of Maintainers to begin with, but can be expanded to include non-maintainers as the contributor base grows. Only committee members can raise votes. Scheduled releases are to be done "without objection" and if one party formally objects then a formal vote is required of the committee. At least 24 hours is required for a vote to close, and a scheduled release can be delayed for the vote. #besu-release in Discord is the intended venue for this vote and discussion. If RC members cannot be reached within the 24 hour period, their vote must be delegated. If that Maintainer is unreliable for multiple votes, they may be removed from the committee. 

With the combination of the Friday "commit pick" for the burn in process, Maintainers and RC members will have 3-4 days (2 business days) to find a reason to object to a regularly scheduled release and 24 hours to vote. A release can be delayed with [majority rule](https://www.apache.org/legal/release-policy.html#release-approval) from RC members. 

Document generated by Confluence on Nov 26, 2024 12:58

[Atlassian](http://www.atlassian.com/)
