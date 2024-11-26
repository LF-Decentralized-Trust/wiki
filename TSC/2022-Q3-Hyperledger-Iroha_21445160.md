1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q3 Hyperledger Iroha

Created by Victor Gridnevsky, last modified on Oct 13, 2022

## Project Health

Iroha 1 is no longer actively maintained, and no major releases are planned at this time. However, Iroha 1 still receives regular contributions from outside the core development team, [Grzegorz Bazior](https://github.com/baziorek) contributing himself, and organizing contributions from his students. The Iroha 2 team is doing bug triage for both projects and implements security fixes for Iroha 1.

Iroha 2 is ramping up production. All developers are now fully onboarded and at maximum productivity. We have implemented a crude delineation of responsibilities, and implemented all processes for long-term development. We are following a timed release cadence, with a Long-term supported release planned at critical stability milestones. Iroha 2 repository is well organised, with branch protection rules enforced for all main branches ( **`iroha2-stable`** ,  **`iroha2-dev`** ,  **`iroha2-lts`** ,  **`iroha2-staging`** ) as well as a common [CI/CD](https://en.wikipedia.org/wiki/CI/CD) pipeline with thorough testing/linting and API verification systems.

Work is underway to bring the supporting libraries up to feature parity with the Rust library. Particular efforts are made to improve the Iroha Python library to be available for testing and automation. Additionally, a Hyperledger Cactus plugin is developed based on the Iroha typescript library. Additional tooling is made for improving the UX, and the Blockchain explorer is nearing the minimum viable product state. Finally, Iroha Kotlin is going to be used as a basis for a public test network, where we will analyse real-world usage statistics and use the data-driven optimisation approaches to further improve Iroha 2.

## Questions/Issues for the TSC

We have a few issues in relation to Hyperledger Ursa. For example, due to its release cadence and relative lull in development activity, we had had to hold back a few dependencies in order to remain binary compatible with the  **`Errors`**  returned from Ursa methods. Our automated auditing tools have identified several deprecations as well as unmaintained libraries which cannot be simply “version bumped” into Ursa.

[Ry Jones](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=22446085) suggested that we take over some of the maintenance burden, particularly ensuring that the code quality of Ursa is up to the same high standards that we ensure for Iroha 2 (linting, reviews, release timing, auditing, fresh dependencies, dependency pruning, automated feature flag coherence testing, property-based testing, fuzzing, functional testing, coverage, modularity).

We would also like to involve more people in the development of Iroha v2, particularly interns and community members. We would like to plan and discuss a few key issues with [David Boswell](https://wiki.hyperledger.org/spaces/viewspace.action?key=~davidwboswell) and design a new internship programme that would involve Iroha 2.

## Releases

Last release reported [here](https://lf-hyperledger.atlassian.net/wiki/display/TSC/2022+Q2+Hyperledger+Iroha) at May 26, 2022.

Timed releases:

- `v2.0.0-pre-rc.4` (internal)
- `v2.0.0-pre-rc.5` (internal)
- [`v2.0.0-pre-rc.6 (LTS)`](https://github.com/hyperledger/iroha/releases/tag/v2.0.0-pre.rc.6)
- `v2.0.0-pre-rc.7` (internal, TBR)

## Overall Activity in the Past Quarter

### Iroha v1

Merged [Grzegorz Bazior](https://github.com/baziorek)’s PRs:

- [#2494](https://github.com/hyperledger/iroha/pull/2494): Update documentation: AddPeer with  **`syncing_node`**  option
- [#2475](https://github.com/hyperledger/iroha/pull/2475): Many documentation changes, corrections, etc.

### Iroha v2

#### Performance enhancements

We have made several changes to both how we measure performance and how we improve it.

We now use profiling as a mandatory step: if something causes a performance regression of more than 10% in throughput and/or latency, we don’t allow it to be merged.

Based off of that we triggered a series of simplifications and optimisations which led to increased performance in the  **`iroha2-staging`**  branch. It is our best bet to increase throughput.

#### WASM dynamic linkage

Dynamic linkage of WASM binaries allows us to

- Save space on-chain, since smartcontracts are stored in binary
- Disallow direct allocations and direct memory manipulations enhancing security
- Allow manipulation of opaque objects only, enforcing invariants, netting even more security
- Increase the number of available methods and functions

#### New functionality

- Additional tooling (genesis block builder GUI)
- Sorting / filtering / pagination of queries, as well as several additional query types (block headers)

#### Improvements

- Better permission validation system
- Trigger improvements (scope, performance, strong typing)
- Better deployment scheme (fully static linkage, much smaller [Docker](https://www.docker.com/) container)
- Kura API improvements
- [Iroha-Python](https://github.com/hyperledger/iroha-python) currently works correctly with Iroha 2
- Run-time modular permission validation
- Simplified Expression subsystem
- Stability, performance improvements, bug fixes, actor system improvements
- Technical debt reduction
- Testing coverage improvements
- Introduction of other testing methods (property-based testing, fuzzing, failure point testing)
- Better UX (more readable error messages, tutorial, on-peer documentation)

## Current Plans

- Resolve Ursa issues by possibly hiring a new developer, who will address the security issues in it.
- Improve the contributing process for community members by tracking PRs with a bot.
- Involve more community members by producing more content related to Iroha v2 (blog posts, video demo, tutorial content).
- Record a detailed demonstration video on Hyperledger Iroha use with CLI.
- Integrate examples into the documentation, so the users have fresh examples easily available and tested. Integrate language-specific guides into articles with a custom code component.

## Maintainer Diversity

As of writing the Iroha 2 core development team consists of:

- 8 Rust developers + 1 tech lead
- 1 front-end developer
- 2 full-time QA engineers (functional and load testing/benchmarking)
- 1 full-time technical writer
- 1 full-time DevOps
- 1 community manager, who also handles front-end, back-end, DevOps and writing tasks as needed

Currently, the maintainer team consists of the Soramitsu employees. [Gregorz Bazior](https://github.com/baziorek) (Yonix Digital Systems, AGH University of Science and Technology) is interested in Iroha 2 and maintains Iroha 1.

## Contributor Diversity

A new intern working on reimplementing iroha-swarm as a plugin to Kagami (Iroha 2’s example generation program).

We have had several contributions ([#2264](https://github.com/hyperledger/iroha/pull/2264), [#2285](https://github.com/hyperledger/iroha/pull/2285), [#2326](https://github.com/hyperledger/iroha/pull/2326)) from [Omkar Mohanty](https://github.com/omkar-mohanty) (intern), Tejas (intern), who has shown interest, but has not contributed code directly and [Ritik Bhandari](https://github.com/ritikBhandari) who contributed the code that was part of [PR#2125](https://github.com/hyperledger/iroha/pull/2214) (add query for  **`FindAssetDefinitionById`** ).

On the Python side of Iroha, we’ve had valuable input about ergonomics of the Iroha 2 Python [library](https://github.com/hyperledger/iroha-python/tree/iroha2) from [Gregorz Bazior](https://github.com/baziorek) (Yonix Digital Systems, AGH University of Science and Technology).

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [artem](https://lf-hyperledger.atlassian.net/wiki/people/557058:5196a62e-7a77-4c97-8180-ae5a5992fb63?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [kamlesh nagware](https://lf-hyperledger.atlassian.net/wiki/people/557058:8e1fc425-f938-4b39-ad13-9cd8b0ddde52?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

# Submission date

18-Aug-2022, added the review section at 1-Sep-2022

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
