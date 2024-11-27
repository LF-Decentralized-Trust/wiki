1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Evernym Contributions](Evernym-Contributions_19464930.html)

# Hyperledger Indy : Evernym Sprint Demos 2018-2019

Created by Richard Esplin, last modified on Aug 17, 2020

The demos are recorded every 2 weeks and posted to this YouTube playlist in the Evernym channel:  
[https://www.youtube.com/playlist?list=PLRp0viTDxBWGLdZk0aamtahB9cpJGV7ZF](https://www.youtube.com/playlist?list=PLRp0viTDxBWGLdZk0aamtahB9cpJGV7ZF)

Sprint Demos starting in 2020 are [listed on a separate page](Evernym-Sprint-Demos_19464929.html).

# Demo for Sprint EV 20.01 (2020-01-30)

- Welcome, project update, and plans, Richard Esplin, 8 min
  
  - Team changes, Aries-Framework-Go (Discussion in Aries WG A call)
  - Rich Schemas
- Indy Node: Release, Vladimir Shishkin, 3 min
  
  - INDY-2325
- Indy Node: Testing promotion and demotion: system and load testing, Vladimir Shishkin, 4 min
  
  - INDY-2326. INDY-2323
- Indy Node: Testing promotion and demotion: unit, integration and simulation testing, Andrew Nikitin, 4 min
  
  - INDY-2326, INDY-2324
- Indy SDK: Release 1.14.2: Rotation of Pairwise Keys, Anoncreds API improvements, CLI Updates, Artem 3 min
  
  - IS-1468, IS-1166, IS-1447, IS-1415

# Demo for Sprint EV 19.26 (2020-01-16)

- Welcome and goals, Richard Esplin, 3 min
- Indy SDK: Release 1.14.0 and 1.14.1 with extended Aries support in libvcx, updated TAA and improved input validation in Anoncreds, Sergey Minaev, 3 min
  
  - IS-1427, IS-1462
- Aries: Support VC-Authn-OIDC in LibVCX, Artem Ivanov 5 min
  
  - IS-1453
- Indy Node: Release 1.12.1, Alexander Shcherbakov, 2 min
  
  - INDY-2310
- Indy Node: Improvements and fixes in primary selection and quorum values calculation in case of new nodes added/demoted, Alexander Shcherbakov, 6 min
  
  - INDY-2322, INDY-2320
  - [Slides](https://docs.google.com/presentation/d/1l7_D3iActhLBMwzoFAH3xWUEGmlH-2PRaLKrNH2_KKg/edit?usp=sharing)
- Indy-Node: Fix infinite view change for a lagging node, Andrew Nikitin, 4 min,
  
  - INDY-2308
- Plans for next sprint, Richard Esplin, 3 min

# Demo for Sprint EV 19.25 (2019-12-19)

- Welcome and goals, Richard Esplin, 3 min
- Indy Node: Document PBFT view change protocol, Renata Toktar, 3 min
  
  - INDY-2138
- Indy Node: Fix rejecting of GET\_CRED\_DEF Reply for a Schema with a lot of attributes, Alexander Shcherbakov, 3 min
  
  - INDY-2306
  - [Slides](https://docs.google.com/presentation/d/1i3UxeTlYEfrhKmISd4fnJlmvCt4zIgI6VIS9U7rxUi0/edit#slide=id.p)
- Indy SDK: Support for empty attributes in credentials, Nikita Khateev, 3 min
  
  - IS-1421
- Indy Node / SDK: Allow multiple active TAAs, Sergey Khoroshavin, 8 min,
  
  - INDY-2302
  - IS-1427
- Plans for next sprint, Richard Esplin, 3 min

# Demo for Sprint EV 19.24 (2019-12-05)

- Welcome and goals, Alex Shcherbakov, 3 min
- Indy Node: Simulation tests and corresponding architecture improvement to include processing of InstanceChanges, Sergey Khoroshavin, 5 min,
  
  - INDY-2263
  - [Presentation](http://Presentation)
- Indy Node: Enable zeroMQ auto-reconnection, Nemanja Patrnogic, 5 min
  
  - INDY-2289
- Indy SDK: Allow using two attrs from the same credential, Nikita Khateev, 5 min
  
  - IS-1381
- Indy Node and SDK: New Stable Releases (indy-node 1.12.0 and indy-sdk 1.13.0), Vladimir Shishkin, 5 min
  
  - INDY-2265
  - IS-1399
- Plans for next sprint, Alex Shcherbakov, 3 min

# Demo for Sprint EV 19.23 (2019-11-21)

- Welcome and goals, Richard Esplin, 2 min
- Indy Node: New logic of Primary Selection to have the same primary selected when View Change starts, Alexander Shcherbakov , 5-7 mins
  
  - INDY-2262
  - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/presentation/d/1CoAXpVdoIfYDeGUmO7_6gLReEvGrriE30mXuT3IVzSI/edit#slide=id.p)
- Indy Node: Versioning ReqHandlers and fixing of problems with state on Sovrin Nets, Renata Toktar, 5-7 mins
  
  - INDY-2292
  - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/presentation/d/18Ek_r0oHtCf63OdgeqEaRR6i9sGhBFXz6yF04tO9twc/edit?usp=sharing)
- Indy SDK: libVCX compatibility with Aries Test Suite, Artem Ivanov, 5-7 mins
  
  - IS-1412, IS-1192
- Plans for next sprint, 3 min

# Demo for Sprint EV 19.22 (2019-11-07)

- Welcome and goals, Alexander Shcherbakov, 2 min
  
  - New release of Indy Node with PBFT view change (see previous videos)
  - No release of Indy SDK in October
- Indy SDK / Aries: Aries support in LibVCX, Sergey Minaev, 10 mins
  
  - Epic: IS-1377
- Indy Node: Performance tests of Indy Node, Sergey Khoroshavin, 7 mins
  
  - Increase batch size =&gt; increased write latency
  - Benefits of moving from RBFT to Aardvark
- Plans for next sprint, 3 min

# Demo for Sprint EV 19.21 (2019-10-24)

- Welcome and goals, Richard, 5 min
- Hyperledger Bootcamp Moscow Update, 5 min
  
  - Presentation slides in the wiki as part of the agenda pages: [Sessions GRID](https://lf-hyperledger.atlassian.net/wiki/spaces/RU/pages/22315050/Sessions+GRID)
- Aries: Repositories for shared libraries, 5 min
  
  - ARIES-3
- SDK: Aries support in libVCX, Sergey Minaev, 5 min
  
  - IS-1377, IS-1378
  - [https://github.com/hyperledger/indy-sdk/tree/vcx-aries-support](https://github.com/hyperledger/indy-sdk/tree/vcx-aries-support)
- Node: PBFT View Change update, Alexander Shcherbakov, 5 min
  
  - INDY-2244
  - INDY-2268
- Plans for next sprint, Richard, 3 min

# Demo for Sprint EV 19.20 (2019-10-10)

- Welcome and goals, Richard, 5 min
- Stable Releases of Node and SDK, Vladimir Shishkin, 5 min
- Node: PBFT View Change update, Renata Toktar, 5 min
  
  - INDY-2140
  - Presentation slides: [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/presentation/d/1X2P4j27s4NkIDndnraKdT15MO1ZJgnB_BtGnB--xlXA)
- Roadmap and architectural explorations for Indy SDK,  5 min
- Plans for next sprint, Richard, 3 min

# Demo for Sprint EV 19.19 (2019-09-26)

- Welcome and goals, Richard, 5 min
- SDK: Release Indy 1.12.0, Artem Ivanov, 7 min
  
  - IS-1361
- Node: bump pyzmq to the latest stable version, Nemanja Patrnogic, 5 min
  
  - INDY-2213
- Node: PBFT View Change update, Sergey Khoroshavin, 15 min
  
  - INDY-2223

# Demo for Sprint EV 19.18 (2019-09-12)

- Welcome and goals, Alex, 5 min
- Sovrin Token: Fixing BLS multisig for FEEs transactions, Nikita Khateev, 5 min
  
  - ST-623
- SDK: Fully qualified DID support update, Artem Ivanov, 10 min
  
  - IS-1358
  - IS-1359
- SDK / Aries: Proposal for async-await, Sergey Minaev, 7 min
  
  - IS-1371
  - [https://www.diffchecker.com/0WkrvEnt](https://www.diffchecker.com/0WkrvEnt)
  - Uses Rust nightly
- Plans for next sprint, Alex, 3 min

# Demo for Sprint EV 19.17 (2019-08-29)

- Welcome and goals, Richard, 5 min
- SDK: Documentation improvements, Sergey Minaev, 10 min
  
  - IS-1353
- Node+SDK: GET\_TXN improvements, Nikita Khateev, 5 min
  
  - INDY-1954
- Node+SDK: Upcoming releases, Vladimir Shishkin, 7 min
  
  - SDK: CentOS support replacing Amazon Linux
  - Node: Issue on Builder Net (INDY-2211)
- Plans for next sprint, Richard, 3 min

# Demo for Sprint EV 19.16 (2019-08-15)

- Welcome and goals, Richard (5 min)
- \[Indy-Node] PBFT View Change fixes, Alexander Shcherbakov, 7 min
  
  - INDY-2147
  - INDY-2136, INDY-2139, INDY-2137, INDY-2179, INDY-2169
  - INDY-1335
  - INDY-2200
  - Alex's presentation: [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/presentation/d/1uoavaxUkUa5yfjgdzWiVYi7fxHyiuDXKv-lN6iX4qXA/edit#slide=id.p)
- \[Indy SDK / Sovrin] Prove possession of a payment address with the Indy CLI, Nikita Khateev, 5 min
  
  - IS-1336
- \[Indy-Node] Changes to permissions for endorsing 3rd party transactions, Vladimir Shishkin, 2 min
  
  - INDY-2199
  - INDY-2198
- \[Indy-SDK] Endorsing 3rd party transactions with the Indy CLI, Artem Ivanov, 5 min
  
  - IS-1346
  - IS-1337
- \[Indy-SDK] Images for Ubuntu 18.04, Artem Ivanov, 2 min
  
  - IS-905
  - IS-906
- Plans for next sprint, Richard (5 min)

# Demo for Sprint EV 19.15 (2019-08-01)

- Welcome and goals, Richard (5 min)
- \[Indy-SDK / Indy-Node] Transaction Endorser support, Artem Ivanov, 5 min
  
  - INDY-2173
  - IS-1325
- \[Indy-Node / Indy-SDK] New DIDs can be created without endorsers, Alexander Shcherbakov, 5 min
  
  - INDY-2171
  - IS-1329
- \[Indy-Node / Indy-SDK / Sovrin] New stable releases, Vladimir Shishkin, 5 min
  
  - INDY-2162
  - IS-1324
  - ST-611
  - ST-609
- Plans for next sprint, Richard (5 min)

# Demo for Sprint EV 19.14 (2019-07-18)

- Welcome and goals, Richard (3 min)
- \[Sovrin plugins / libsovtoken]: Pagination for GET\_UTXO request, Nikita Khateev, 5 min
  
  - ST-600
  - ST-601
  - ST-602
  - ST-604
- \[Indy-SDK / Indy-Node]: TAA acceptance uses date instead of time, Sergey Minaev, 3 min
  
  - INDY-2157
  - IS-1298
- \[Indy-SDK]: CLI improvements, Vladimir Shishkin, 3 min
  
  - IS-1292
- \[Indy-Node]: Issue with notifying clients about Invalid requests, Renata Toktar, 5 min
  
  - INDY-2164
- Plans for next sprint, Richard (3 min)

# Demo for Sprint EV 19.13 (2019-07-03)

- Welcome and goals, Richard (3 min)
- Update on release and Sovrin network updates, Richard Esplin (3 min)
- Indy-SDK: Aries / Indy split, Sergey Minaev (5 min) 
  
  - IS-1285
- Indy-Node: Improved testing of view change, Sergey Khoroshavin (5 min)
  
  - Property based testing (INDY-2135)
  - The view change protocol that we are implementing is described on pages 43-48 of this thesis [https://www.microsoft.com/en-us/research/wp-content/uploads/2017/01/thesis-mcastro.pdf](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/01/thesis-mcastro.pdf)
- Indy-Node: Bug fix for node crashes with invalid requests, Artem Obruchnikov (5 min)
  
  - INDY-2144 ([https://github.com/hyperledger/indy-plenum/pull/1243/](https://github.com/hyperledger/indy-plenum/pull/1243/))
- Plans for next sprint, Richard (3 min)

# Demo for Sprint EV 19.12 (2019-06-20)

- Welcome and goals, Richard (3 min)
- Indy-Node: PBFT View Change Design, Alexander Shch. (6 min)
  
  - INDY-2134
- Indy-Node: Plenum 2.0 Architecture (needed to implement PBFT View Change), Alexander Shch. (6 min)
  
  - INDY-1338
- Indy-Node: Renamed Trust Anchor to Endorser, Artem O. (2 min)
  
  - INDY-1950
- Indy-Node: Removed ANYONE\_CAN\_WRITE flag, Artem O. (2 min)
  
  - INDY-1956
- Indy-SDK: Offline signatures for payment transactions, Vladimir Sh. (3 min)
  
  - ST-576
- Plans for next sprint, Richard (3 min)

# Demo for Sprint EV 19.11 (2019-06-06)

- Welcome and goals, Richard (3 min)
- Indy-Node: Hot fix for Builder Net, Sergey K. (5 min)
  
  - INDY-2128, INDY-2129
- Indy-Node + Indy SDK: AUTH\_RULES improvements, Sergey M. (5 min)
  
  - command to set multiple auth rules (INDY-2087, IS-1265)
  - Auth Rule constraint to forbid an action (INDY-2077)
  - Renaming TRUST\_ANCHOR to ENDORSER in libindy (IS-1262)
- Indy-Node + Sovrin Plugins: Pluggable Request Handlers in Token Plugins, Nikita Kh. (5 min)
  
  - ST-510
  - Video 18.25 (2018-12-20)
- Plans for next sprint, Richard (3)

# Demo for Sprint EV 19.10 (2019-05-23)

- Welcome and Goals, Alex S. (3 min)
- End-to-end Demo: Network administration, Sergey M. (10 min)
  
  - End-to-end Demo on how to setup a Pool. It includes setting Auth Rules and Fees, setting Transaction Author Agreement, and do minting of tokens
- End-to-end Demo: Token usage, Sergey M. (10 min)
  
  - End-to-end Demo of using tokens. It includes payment transfer transactions, and domain transactions with Fees.
- Plans for next sprint, Alex S. (4 min)

# Demo for Sprint EV 19.09 (2019-05-08)

- Welcome and Goals, Richard (3 min)
- Indy Node: Transaction Author Agreement Design, Alex S. (4 min)
- Indy SDK: Transaction Author Agreement API in LibIndy, Sergey M. (4 min)
- Sovrin Token Plugins: Auth rule support for XFER, SET\_FEES, and MINT, Renata (2 min)
- Plans for next sprint, Richard (4)

# Demo for Sprint EV 19.08 (2019-04-26)

- Welcome and Goals, Richard (4 min)
- Indy Node: Auth rules examples and tests, Andrew N. (4 min)
- Indy Node: 1.7.0 release process, Andrey K. (4 min)
- Indy Node: Catch-up improvements, Sergey K. (4 min)
  
  - INDY-2053
- Plans for next sprint, Richard (4 min)

# Demo for Sprint EV 19.07 (2019-04-11)

- Welcome and Goals, Richard (4 min)
- Indy SDK: Minting tool, Artem I (4 min)
  
  - ST-276
- Indy Node: Plan of integration tests for token plugins, Nikita Kh. (4 min)
  
  - ST-524
- Indy Node and Sovrin Token: Replacing SET\_FEES by AUTH\_RULE, Andrew N. (4 min)
  
  - ST-529
- Plans for next sprint, Richard (4 min)

# Demo for Sprint EV 19.06 (2019-03-28)

- Welcome and Goals, Richard (4 min)
  
  - Our sprints now also include the Sovrin Token backlog.
- Indy SDK: Updates to Credential Exchange and SDK architecture proposal, Nikita K. (4 min)
  
  - IS-1182
- Indy SDK: Updates to SDK architecture proposal, Artem I. (2 min)
  
  - IS-1196
- Indy SDK: Release of Indy SDK 1.8.2, Artem I. (2 min)
  
  - IS-1199
- Indy Node: Restore 3PC state after restart from the Audit Ledger, Artem O. (4 min)
  
  - INDY-1946
- HIPEs and SIPs: Anoncreds 2.0, and future HIPEs on Payments, Brent (4 min)
  
  - ST-519
- Plans for next sprint, Richard (3 min)

# Demo for Sprint EV 19.05 (2019-03-14)

- Welcome and Goals, Richard (2 min)
- Indy SDK: Announce IndySDK 2.0 architecture, Sergey M. (4 min)
  
  - IS-1196
- Indy SDK: Auth Rule integration into Libindy and Indy-CLI, Artem I. (4 min)
  
  - IS-1201
  - IS-1202
- Indy Node: Consistent catch-up using Audit Ledger, Sergey Kh. (4 min)
  
  - INDY-1945
- Indy Node: Release workflow and versioning improvements, Andrey K. (4 min)
  
  - INDY-1992
- Plans for next sprint, Richard (3 min)

# Demo for Sprint EV 19.04 (2019-02-28)

- Welcome and goals, Richard (4 min)
- Indy SDK: VCX Error handling enhancement, Artem I. (4 min)
  
  - IS-1121
- Indy Node: Audit Ledger, Alex S. (4 min)
  
  - INDY-1944
- Indy Node: Auth rules integrated into config ledger, Andrey N. (4 min)
  
  - INDY-2001, INDY-2002, INDY-2006
- Indy Node: Persisting Instance Change messages, Renata (4 min)
  
  - INDY-1984
- Plans for next sprint, Richard (3 min)

# Demo for Sprint EV 19.03 (2019-02-14)

- Welcome and Goals, Richard (2 min)
- Indy SDK / Indy Node: Releases of IndyNode and IndySDK, Vladimir. (4 min)
- Indy Node: Freshness-based View Change, Sergey Kh. (4 min)
  
  - INDY-1911
- Indy Node: Fixing detection of backup performance degradation, Renata T. (4 min)
  
  - INDY-1933
- Indy SDK: Credential Exchange message family HIPE, Nikita Kh. (4 min)
  
  - IS-1125
- Plans for next sprint, Richard (3 min)

# Demo for Sprint EV 19.02 (2019-01-31)

- Welcome and Goals, Richard (2 min)
- Indy Node: Freshness, Alex (4 min)
  
  - INDY-933
- Indy Node: Freshness support in validator info and Network Monitor role, Vladimir Sh. (4 min)
  
  - INDY-1928
- Indy SDK: Freshness support, Nikita Kh. (4 min)
  
  - IS-954
- Indy SDK: New stable release 1.8.0, Artem I. (4 min)
  
  - IS-1150
- Plans for next sprint, Richard (3 min)

# Demo for Sprint EV 19.01 (2019-01-17)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: Indy SDK Error handling enhancement, Artem I. (4 min)
- Indy Node: Stashing during catch-up, Renata. (4 min)
  
  - INDY-1876
- Indy Node: Audit ledger design, Sergey K. (4 min)
  
  - INDY-1924
- Plans for next sprint, Richard (3 min)

# Demo for Sprint EV 18.25 (2018-12-20)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: VCX: Credential Values format is outdated, Matt. (4 min)
  
  - IS-1101
- Indy SDK: PostgreSQL wallet storage, Vyacheslav G. (4 min)
  
  - IS-1063
- Indy Node: New request handlers architecture, Artem O. (4 min)
  
  - INDY-1728
  - INDY-1730
- Indy Node: Hotfix releases 1.6.80 and 1.6.82; issues with POOL\_RESTART and triggering of VIEW\_CHANGE, Sergey Kh. (4 min)
  
  - INDY-1896
  - INDY-1909
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.24 (2018-12-06)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: Preparation VCX for release, Artem I. (4 min)
  
  - IS-874 IS-936
  - IS-950 IS-951 IS-952
  - IS-1090
  - IS-1059
  - IS-1061
  - IS-1071
- Indy SDK: Revocation serialization and AMCL migration, Nikita Kh. (4 min)
  
  - IS-1093
- Indy Node: New Stable Release 1.6.79; Improvements in Validator Info tool, Vladimir. (4 min)
  
  - INDY-1726
  - INDY-1814
  - INDY-1854
  - INDY-1841
  - INDY-967
- Indy Node: Fixes related to BLS signature, Renata. (4 min)
  
  - INDY-1846
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.23 (2018-11-22)

- Welcome and Goals, Alex and Sergey M. (2 min)
- Indy SDK: Rust wrapper integration, Nikita Kh. (4 min)
  
  - IS-1066
- Indy SDK: 1.6.8 Release, Sergey M. (4 min)
  
  - IS-1030, IS-1031, IS-1032
- Indy Node: Found out why max node prod time increases during long load test, Sergey Kh. (4 min)
  
  - INDY-1747
- Indy Node: Sequence diagram for Plenum Consensus Protocol, Alex. (4 min)
  
  - INDY-1851
- Plans for next sprint, Alex/Sergey M. (3 min)

# Demo for Sprint EV 18.22 (2018-11-08)

- Welcome and Goals, Richard. (5 min)
  
  - Upgrade of Sovrin Main Net
- Indy SDK: Dummy Agents, Artem I. (4 min)
  
  - IS-1042
- Indy SDK: IndyCLI resuming key rotation, Darko. (4 min)
  
  - IS-1036
- Indy Node: Recent load test results, Vladimir Sh. (2 min)
  
  - INDY-1774, 1775, 1776, 1821
- Indy Node: Test Pool Automation scripts, Sergey Kh. (2 min)
  
  - INDY-1641 Epic
- Plans for next sprint, Richard. (8 min)
  
  - Changes to team organization

# Demo for Sprint EV 18.21 (2018-10-24)

- Welcome and Goals, Alex. (2 min)
- Indy SDK: Reduce common build times, Sergey. (4 min)
  
  - IS-1020
- Indy SDK: Avoid VCX compile time linking with payments plugins, Nem. (4 min)
  
  - IS-934
- Indy Node: Fixes for Backup Instances degradation (leading to OOM), Renata. (4 min)
  
  - INDY-1682
- Indy Node: ZMQ memory Consumption, Sergey Sh. (4 min)
  
  - INDY-1686
- Plans for next sprint, Alex. (3 min)

# Demo for Sprint EV 18.20 (2018-10-11)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: Artem I. (4 min)
  
  - Support DID seeds in hex format, IS-1023
  - 1.6.7 release, IS-1024
- Indy SDK: Sergey M. (4 min)
  
  - Rust Wrapper, IS-1013
    
    Rust Wrapper CI/CD pipeline, IS-1014
- Indy Node: Ledger 2.0: alternatives to RBFT, Sergey Kh. (4 min)
  
  - INDY-1615
  - INDY-1613
- Indy Node: Fixing catch-up issues, Nikita S. (4 min)
  
  - INDY-1711
  - INDY-1739
  - INDY-1740
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.19 (2018-09-27)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: Getting Started Tutorial for libvcx, Darko. (4 min)
  
  - IS-935
- Indy SDK: Indy CLI allows to work with wallets created outside of CLI, Artem I. (4 min)
  
  - IS-988
- Indy Node: Do not re-verify signature for Propagates, Andrey N. (4 min)
  
  - INDY-1649
- Indy Node: Support all FEEs txns in the load script, Dmitry. (4 min)
  
  - INDY-1665
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.18 (2018-09-13)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: Ledger queries without an active DID, Vladimir. (4 min)
  
  - IS-863
- Indy SDK: Better logging, Slava. (4 min)
- Indy Node: Historical data in validator-info, Sergey S. (4 min)
  
  - INDY-1637
- Indy Node: Switch off backup replicas with lost primary, Renata. (4 min)
  
  - INDY-1680
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.17 (2018-08-30)

- Welcome and Goals, Alex / Slava
- Indy Node: Load testing with non-smooth load, Natalia Dracheva. (4 min)
- Indy Node: False positive View Change issue and fixes, Sergey Shilov. (4 min)
- Indy SDK: Support of RAW wallet keys, Artem. (4 min)
- Indy SDK: Wallet benchmarking, Sergey. (4 min)
- Plans for next sprint, Alex / Slava. (3 min)

# Demo for Sprint EV 18.16 (2018-08-16)

- Welcome and Goals, Richard. (2 min)
- Indy Node: Trust anchor permission not needed for ledger writes, Artem Obruchnikov. (4 min)
- Indy Node: Load test results, Vladimir. (4 min)
- Indy SDK: Advanced support of pool actions, Sergey. (4 min)
- Indy SDK: Support simplified pwhash key derivation algorithm in Wallet API, Artem Ivanov. (4 min)
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.15 (2018-08-02)

- Welcome and Goals, Richard
- Indy Node: Explore timing and execution time, Sergey Khoroshavin. (4 min)
  
  - INDY-1475
- Indy Node: A possibility to upgrade Sovrin instead of Indy-Node, Dmitry Surnin. (4 min)
  
  - INDY-1491
- Indy SDK: 1.6.1 stable release, Sergey M. (4 min)
- Indy SDK: CD for mobile platforms, Artem. (4 min)
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.14 (2018-07-19)

- Welcome and Goals, Richard (2 min)
- Indy Node: Load and stress testing results, Nikita Zh. (4 min)
  
  - [https://docs.google.com/spreadsheets/d/1DTjDsLSysFBiKU-9z4-IzunJk4wEy44hE\_PGZYxnN\_8/edit#gid=1813415708](https://docs.google.com/spreadsheets/d/1DTjDsLSysFBiKU-9z4-IzunJk4wEy44hE_PGZYxnN_8/edit#gid=1813415708)
- Indy Node: Fix for open connection issue, Sergey Sh. (4 min)
- Indy SDK: Fix for open connection, Sergey M. (4 min)
  
  - [https://github.com/hyperledger/indy-sdk/tree/master/doc/design/009-efficient-connections](https://github.com/hyperledger/indy-sdk/tree/master/doc/design/009-efficient-connections)
- Indy SDK: Integrate tags-based search to Anoncreds workflow, Artem. (4 min)
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.13 (2018-07-05)

- Welcome and Goals, Alex. (2 min)
- Indy SDK: Indy SDK Release 1.5, Nikita Zh. (4 min)
- Indy SDK: Wallet access from cluster nodes, Slava. (4 min)
- Indy Node: Indy Node Release 1.4, Alex. (4 min)
- Indy Node: Decreasing amount of INFO log level, Dmitry S. (4 min)
- Plans for next sprint, Alex/Slava (3 min)

# Demo for Sprint EV 18.12 (2018-06-21)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: Wallet Import/Export, Nikita Zhigunenko. (4 min)
- Indy SDK: Support of Indy Node protocol version 2, Vyacheslav Gudkov. (4 min)
- Indy Node: Fixing catchup cancellation during ViewChange, Alex. (4 min)
- Indy Node: Extending load script to support all write and read requests, Olga. (4 min)
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.11 (2018-06-06)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: Support of state proofs for custom transactions, Sergey M. (4 min)
- Indy SDK: get-validator-info command support, Nikita Zh. (4 min)
- Indy Node: Using separate NICs and different queue sizes for client-to-node and node-to-node communication, Sergey Sh. (4 min)
- Indy Node: Using request’s digest to identify requests uniquely, Renata. (4 min)
- Plans for next sprint, Richard. (3 min)

# Demo for Sprint EV 18.10 (2018-05-24)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: Libnullpay now behaves like a real payment plugin, has automated build and binary packages, Nikita Kh. (4 min)
- Indy SDK: Integration of a new wallet, Artem I. (4 min)
- Indy Node: View Change issues and tests, Sergey Kh. (4 min)
- Indy Node: New load scripts, Dmitry S. (4 min)
- Plans for next sprint, Richard. (5 min)

# Demo for Sprint EV 18.09 (2018-05-10)

- Welcome and Goals, Richard. (2 min)
- Indy SDK: Payments API, Nikita Kh. (4 min)
  
  - IS-661: Payments Interface: Java wrapper
  - IS-635: Tokens Interface: Null payment handler for tests
  - IS-638: Tokens Interface: Register tokens handler call integration tests
  - IS-637: Tokens Interface: Payment address calls integration tests
  - IS-639: Tokens Interface: Add request fees call integration tests
  - IS-640: Token Interface: Tokens-related transactions builders integration tests
- Indy SDK: CLI plugins and payments commands, Artem. (4 min)
  
  - IS-652: Tokens Interface: Design CLI payments support
  - IS-667: Tokens Interface: CLI user should be able to register custom payments and wallets plugins
  - IS-668: Tokens Interface: CLI user should be able to assign fees to Ledger transactions
  - IS-669: Tokens Interface: CLI user should be able to send payment-related transactions
  - IS-66x: Tokens Interface: CLI user should be able to manage payment addresses in CLI
- Indy Node: New txn format, Alex (4 min)
- Indy Node: Latest load testing results, Olga. (4 min)
- Plans for next sprint, Richard. (5 min)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
