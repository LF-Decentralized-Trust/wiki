1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q4 Hyperledger Iroha

Created by Victor Gridnevsky, last modified by Jim Zhang on Dec 01, 2022

## Project Health

While the active maintainance of Iroha 1 stopped and no major releases are planned at this time, it still receives regular contributions from outside the core development team. [Grzegorz Bazior](https://github.com/baziorek) is actively contributing himself, both with code and support, and organizing contributions from his students. The Iroha 2 team is doing bug triage for both projects and implements security fixes for Iroha 1.

All Iroha 2 developers are now fully onboarded and at maximum productivity. We have implemented a crude delineation of responsibilities, and implemented all processes for long-term development. We are following a timed release cadence, with a Long-term supported release planned at critical stability milestones. Iroha 2 repository is well organised, with branch protection rules enforced for all main branches ( **`iroha2-stable`** ,  **`iroha2-dev`** ,  **`iroha2-lts`** ,  **`iroha2-staging`** ) as well as a common [CI/CD](https://en.wikipedia.org/wiki/CI/CD) pipeline with thorough testing/linting and API verification systems. Iroha 1 and Iroha 2 branches may soon switch places due to the limited maintainance of Iroha 1.

An interaction between Iroha and Ursa teams was established and updates are being implemented.

## Questions/Issues for the TSC

None.

## Releases

Releases past quarter:

- `v2.0.0-pre-rc.4` (internal)
- `v2.0.0-pre-rc.5` (internal)
- [`v2.0.0-pre-rc.6 (LTS)`](https://github.com/hyperledger/iroha/releases/tag/v2.0.0-pre.rc.6)
- `v2.0.0-pre-rc.7` (internal)

Timed:

- v2.0.0-pre-rc.9

## Overall Activity in the Past Quarter

### Iroha v1

- Sample config update: max\_rounds\_delay was replaced with proposal\_creation\_timeout in [#1662](https://github.com/hyperledger/iroha/pull/1662)
- Compile errors with G++11 in Iroha 1 were fixed in [#1765](https://github.com/hyperledger/iroha/pull/1765)
- Documentation was improved in [#2475](https://github.com/hyperledger/iroha/pull/2475) and [#2494](https://github.com/hyperledger/iroha/pull/2494)
- Building was fixed in [#2902](https://github.com/hyperledger/iroha/pull/2902) and [#2906](https://github.com/hyperledger/iroha/pull/2906)

### Iroha v2

- Outstanding PR count: 9, all of which are new. PRs are approximately closed in a week.
- A new QA process is implemented. It focuses on the defect reproduction and MWE generation. 100% of the tickets are filed as bugs and are re-tested.
- New Sumeragi consensus was implemented, tested and merged into the lts branch; it focuses on ironing out the previous p2p actor problem and it improves the performance.
- P2P module restructuring leads to the stability improvements.
- Ursa preliminary cleanup is in progress.
- Kura inspector CLI is stable and working.
- Docker and docker-compose configuration was improved
- WASM: there’s an ongoing work regarding the compilation time, file size, security, introspection and documentation.
- Iroha configuration parser handles the default values better, covering more edge-cases.
- The documentation was updated to RC10
- An initial implementation of `iroha_swarm` by our intern, Michael
- A Blockchain explorer demo was implemented
- A new JSON logging mode improves the diagnostic process.
- A new feature for Kagami: synthetic genesis blocks
- A syntax block generation tool was added
- Load test generation tool was added (both statistic and representative)
- Kagami UX:
  
  - Better help messages,
  - More subcommands,
  - Easier generation of keys given passphrase
- CVE in `SignatureCheckCondition` fixed
- Permission validators can be registered at run-time and user-generated with run-time upgradeability.
- What changed regarding the Kagami UX?
- Run-time permission validators implementation (?)
- Sumeragi optimisation (what was changed?)
- WASM dynamic linkage: FFI interface 95% finished.
- Fully functional events:
  
  - Scoped
  - Global
  - Event-based
  - Time-based
  - By-call
  - With event processing
- QA testing roadmap (De-containerised tests, CI Tests for SDK compatibility)
- The Websocket connections are closed cleanly
- Error states are reported with more information and with better feedback to the user

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

A practice of working with interns was established and will continue.

Since the last time, Jonathan Plasse contributed a fix ([#2670](https://github.com/hyperledger/iroha/pull/2670)) for issue [#2667](https://github.com/hyperledger/iroha/issues/2667), "Refactor &amp;Option&lt;T&gt; to Option&lt;&amp;T&gt;".

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

11-Nov-2022

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
