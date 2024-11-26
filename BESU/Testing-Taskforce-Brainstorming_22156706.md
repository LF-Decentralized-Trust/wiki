1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Performance &amp; Stability](22155524.html)

# Besu : Testing Taskforce Brainstorming

Created by Matt Nelson (Deactivated), last modified by Sally MacFarlane on Mar 22, 2024

# Context

Its dawned on us that Besu now represents upward of ~***$5B on Mainnet in stake*** !! Great job for everyone [https://supermajority.info/](https://supermajority.info/ "https://supermajority.info/")

This is a big responsibility, not just on Mainnet, but other chains that use Besu too. We are representing more and more value and reputation for a ton of organizations. The Consensys team is thinking on how we may be more careful in the release process (specifically regressions). As we approach the Cancun fork, is it OK to delay less-tested PRs on Main to avoid releasing any issues (especially in 24.1.2)? The problem is, users may not be able to safely downgrade after the fork without a manual intervention / new release. Is anything going into this next release that may be less tested? or a default that should be hidden behind a feature flag? Additionally - **I wanted to crowd source ideation about regressions**. We have had a handful of interventions on releases recently. Instead of just entirely slowing down releases, any ideas from maintainers? The Consensys team is scheduling a sprint to look at testing gaps and improvements that can be made in the codebase. If anyone would like to help in this, let me know! Thanks all!

# Ideation

- integrate Hive testing into CI/CD pipeline.
- We should measure code coverage and make it a condition for merging a PR
- benchmark metrics - sync time, block import time etc and test PRs for regression
  
  - some of these metrics (sync time, peering) may require long-running tests so may not be practical to run on individual PRs - could be on a nightly cadence
- Ensure test coverage for key features eg bonsai
- tests that run on mainnet config aren't testing upcoming hard fork features - to avoid finding bugs at the last minute, change this to holesky/sepolia (or make it configurable?)
- burn-in on existing (synced) nodes vs syncing from scratch
  
  - backward sync is triggered when you upgrade
  - it would be awesome to make the (Consensys internal) burn-in process less manual.
- don't want to make the release process more painful

# What will be the outcomes of this epic?

## Phase 1 (Analysis)

Aiming to complete this by end of March.

List of recommendations / Prioritized list of gaps to be addressed

- An Epic/workstream is created with actionable item based on the findings from the brainstorm
- Would be nice to have an idea of the relative amount of work involved so we can compare cost to benefit.

## Phase 2 (Solutions)

Start solving the problems identified. May need different resources at this point.

# What is the problem we’re trying to solve?

## Why has this come up now?

More money is at stake

Besu profile is rising

Besu gaining market share

Greater reputational risk

## What would be catastrophic?

- Consensus issue
- Sync issue
- Peering issue (eg Besu nodes lose 100% of peers and drop off the network)
- Chain fork
- Node database corruption or significant downtime (quite impactful at scale)
- Missing or empty block production
- Anything with customer funds or keys (includes Web3signer)

Need to verify that our bug prioritization matrix aligns with this.

## Bad (but not catastrophic)

Anything here could escalate to catastrophic if the scale was big enough.

- Missed attestations
- Regression in block processing time
- Regression in sync times or performance
- Bad UX (nodes are a pain to manage)
- Substantial drop in performance
- Block export/import broken

# Goals

- No P1 bugs released
- No P2 bugs released
- - One P2 bug per quarter is tolerable (but our goal should be zero)
  - We have P2 bugs identified, in the backlog - how do we make sure we don’t release them
  - Ditto bugs that haven’t been prioritized (unknown - maybe they are P2 or even P1)
- Robust processes
- - we know that PRs have sufficient automated tests and/or require evidence of manual tests where this makes sense
- Don't want to make the release process more painful
- - But could make the release process more robust/comprehensive if doing so doesn’t add hassle/pain to the process?
- Ensure we’re spending effort where it makes sense

# Opportunities in our (current) process

- Bug prioritization 
  
  - Triage matrix - review
- PRs
  
  - Feature toggles - new code paths are disabled by default? 
    
    - Note this requires some extra effort to leverage DI (Dagger)
- Merge to main
- Nightly
  
  - Nightly build could publish to a "nightly" or "develop" version so we can point nightly canaries to it instead of relying on remembering to update them. [https://github.com/hyperledger/besu/issues/6426](https://github.com/hyperledger/besu/issues/6426)
  
  <!--THE END-->
  
  - Confirm that automation around deployment actually deploys a new build each night, should be confirmed by self-reporting the git sha at startup. [https://github.com/hyperledger/besu/issues/6637](https://github.com/hyperledger/besu/issues/6637)
  - Canaries updated with nightly build
- Pre-release
  
  - Enterprise-oriented testing - Incorporating Matt Whitehead's suggestions
  - [https://lf-hyperledger.atlassian.net/wiki/display/BESU/Testing](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Testing)
  - And ensuring enterprise PRs don't leak bugs into main
  - Maybe use PEEPS [https://github.com/Consensys/PEEPS](https://github.com/Consensys/PEEPS) as a reference but probably makes sense to start with a new repo - might be easier to start from Besu AT framework than the PEEPS one. The PEEPS framework runs everything in Docker so could be slow and the DSL is quite cumbersome to use as everything is very generic so it works with both Quorum, Besu and EthSigner.
    
    - Bring this on board later? Part of burn-in or a separate ad-hoc process?
  - A big part of the release process is regression testing - but it’s very manual
    
    - burn-in on existing (synced) nodes vs syncing from scratch
    - it would be awesome to make the (Consensys internal) burn-in process less manual.
- Post-release
  
  - Retrospective to fold new learnings back into our processes and automation.

# Gaps

## Tickets in the epic

See Testing Gaps [Epic](https://app.zenhub.com/workspaces/besu-team-65de4730380c1800c30a9f3a/board?epics=Z2lkOi8vcmFwdG9yL0VwaWMvMTEyNTQzNw) for the stack ranked issues. (For those without zenhub licences, the epic is [here](https://github.com/hyperledger/besu/issues/6538) in Github but it won't show all the detail.)

- Hive testing - can we integrate Hive testing into CI/CD pipeline? Or at least an intermediate step (less effort) that will enable us to easily view new failures
- Smoke test: test besu starts up (with default options?)
  
  - Context: our tests didn’t pick up that the data directory wasn’t being created automatically
  - [https://github.com/hyperledger/besu/issues/6610](https://github.com/hyperledger/besu/issues/6610)
- Simon: Downgrade test - would be good to have a regression test for each release to check we can downgrade to previous version(s).
- Automate burn-in
- Not much in the way of “initial sync” tests at the IT/AT level. Should review what hive provides for this. [https://github.com/hyperledger/besu/issues/6652](https://github.com/hyperledger/besu/issues/6652)
- Decouple ATs from mainnet.json
  
  - most acceptance tests use mainnet.json, so bugs on adding a new fork (eg cancun) may not get covered until much later in the SDLC.
  - to avoid finding bugs at the last minute, change this to holesky/sepolia (or make it configurable?)
  - [https://github.com/hyperledger/besu/issues/6653](https://github.com/hyperledger/besu/issues/6653)
- Fuzz testing [https://github.com/hyperledger/besu/issues/6655](https://github.com/hyperledger/besu/issues/6655) 
  
  - Fuzz testing on critical areas e.g. Bonsai trielogs - something like tx-fuzz
- Code coverage Aggregation [https://github.com/hyperledger/besu/issues/6650](https://github.com/hyperledger/besu/issues/6650) 
  
  - We should measure code coverage
  - and consider make it a condition for merging a PR?
- Snap gaps! 
  
  - Besu serving besu [https://github.com/hyperledger/besu/issues/6656](https://github.com/hyperledger/besu/issues/6656)
- Current ATs test (previous default) forest storage format - need to update to bonsai
  
  - [https://github.com/hyperledger/besu/issues/6583](https://github.com/hyperledger/besu/issues/6583)
  - reference tests have been updated already
- Can we fail faster with local and CI builds - improve devx and reduce context switching
  
  - [https://github.com/hyperledger/besu/issues/6740](https://github.com/hyperledger/besu/issues/6740)
  - Flaky tests are a major barrier here. People will run more tests locally when they are more reliable, and don’t require multiple runs for confidence.
  - Does GHA have metrics for flaky tests / see it manually
- Integration tests - are very out of date
  
  - Update or remove - [https://github.com/hyperledger/besu/issues/6739](https://github.com/hyperledger/besu/issues/6739)

## Covered elsewhere

- Is there any coverage of different solidity versions?
- - No there isn’t.
  - This would be a very narrow gap - besu EVM is thoroughly tested by reference tests. Anything falling into this gap would likely be a bug in solidity, and caught elsewhere.
- Something like [Pact contract tests](https://docs.pact.io/) for engine API for various CLs?? Again, might be covered by Hive.
- - Think this is covered by Hive tests
- Devwatch / operational oversight / dogfooding
- - See [DWIP](https://docs.google.com/document/d/1F2gnh71RleBHej_coyd7Vr9Og_vZCE7a4E117eL0_Vw/edit#heading=h.o1e4ume8ubm1) separate effort for improving devwatch itself
  - Is observability a quality issue?
  - QA / devops / holesky/sepolia validators

Document generated by Confluence on Nov 26, 2024 13:01

[Atlassian](http://www.atlassian.com/)
