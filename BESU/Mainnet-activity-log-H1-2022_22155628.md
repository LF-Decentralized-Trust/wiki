1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Programs &amp; Grants](22155199.html)
4. [Besu Execution Client Incentive Program](Besu-Execution-Client-Incentive-Program_22155201.html)

# Besu : Mainnet activity log H1 2022

Created by Sally MacFarlane, last modified by Gary Schulte on Jul 14, 2022

## *In-Progress Reports*

### Maintainer github handle: shemnon

Maintainer org: Hedera

Query for mainnet label on closed PRs: [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Ashemnon+label%3Amainnet](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Ashemnon%20label%3Amainnet)

Details on mainnet contributions

- EVM performance - tripled Gas Per Second through a number of enhancements
- EVM Compliance - updated code to handle nonce limits
- Reference Tests - bright ref tests to current revision
- Consulted for shadowfork consensus break
- Preliminary design discussions with Karim to validate checkpointing in sync.

### Maintainer Github handle: gezero

Maintener org: ConsenSys

Query for closed PRs: [https://github.com/hyperledger/besu/pulls?q=is%3Apr+author%3Agezero+is%3Aclosed+](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20author%3Agezero%20is%3Aclosed%20)

Details on mainnet contributions:

- Bacwards Sync:
  
  - [Backwards Sync is now adding blocks to BadBlocksManager](https://github.com/hyperledger/besu/pull/3999)
  - [Backward Sync should remember recent finalized blocks](https://github.com/hyperledger/besu/pull/3808)
  - [Improving backwards sync](https://github.com/hyperledger/besu/pull/3638)
  - [Batching backward sync](https://github.com/hyperledger/besu/pull/3532)
  - [Backward sync](https://github.com/hyperledger/besu/pull/3130)
- Full sync:
  
  - [FullSync Future should stop when total terminal difficulty is reached](https://github.com/hyperledger/besu/pull/3423)
- Fast sync:
  
  - [Clear previous version fast sync runs data](https://github.com/hyperledger/besu/pull/3270)
  - [When downloading the world state, persist children before parents](https://github.com/hyperledger/besu/pull/3202)
- Miscelanious fixes:
  
  - [findSyncTarget always called with Optional.empty](https://github.com/hyperledger/besu/pull/3364)
  - [Return GOQUORUM\_PRIVATE\_STORAGE where it was before i broke it](https://github.com/hyperledger/besu/pull/3617)

### Maintainer GitHub handle: daniellehrner

Maintainer org: ConsenSys

Query for mainnet label on closed issues: [https://github.com/hyperledger/besu/issues?q=is%3Aissue+is%3Aclosed+assignee%3Adaniellehrner+label%3Amainnet+](https://github.com/hyperledger/besu/issues?q=is%3Aissue%20is%3Aclosed%20assignee%3Adaniellehrner%20label%3Amainnet%20)

Details on mainnet contributions

- [Update reference tests to the latest version and include test for gray glacier](https://github.com/hyperledger/besu/pull/4011)
- [Gray glacier hard fork](https://github.com/hyperledger/besu/pull/3962)
- [fcU: Remove check if new finalized is descendant from the previous one](https://github.com/hyperledger/besu/issues/3966)
- [EngineForkchoiceUpdated: Verify if payload attributes are valid](https://github.com/hyperledger/besu/issues/3836)
- [Subcommand blocks import throws exception](https://github.com/hyperledger/besu/issues/3646)
- [Acceptance test for execution engine apis](https://github.com/hyperledger/besu/pull/3533)
- [MERGE: Rename field random to prevRandao](https://github.com/hyperledger/besu/issues/3490)
- [MERGE: Rename opcode RANDOM to PREVRANDAO](https://github.com/hyperledger/besu/issues/3489)
- [MERGE: Add Kiln test vectors](https://github.com/hyperledger/besu/issues/3484)
- [MERGE: Implement engine\_exchangeTransitionConfigurationV1 API](https://github.com/hyperledger/besu/issues/3471)
- [MERGE: extend semantics of executePayload / newPayload method](https://github.com/hyperledger/besu/issues/3365)
- [Change payloadId of engine\_forkchoiceUpdatedV1 API to fixed 8 bytes](https://github.com/hyperledger/besu/issues/3125)

### Maintainer GitHub handle: fab-10

Maintainer org: ConsenSys

Query for mainnet label on closed PRs: [https://github.com/hyperledger/besu/pulls?q=is%3Apr+author%3Afab-10+is%3Aclosed+label%3Amainnet](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20author%3Afab-10%20is%3Aclosed%20label%3Amainnet)

Details on mainnet contributions

- Feature: "The Merge" switch to PoS
  
  - [Extend block parameter methods to accept 'finalized' and 'safe' as block tags](https://github.com/hyperledger/besu/pull/3950)
  - [Do not require a minimum block height when downloading headers or blocks](https://github.com/hyperledger/besu/pull/3911)
  - [Allow to backward sync to request headers back to last finalized block if present or genesis](https://github.com/hyperledger/besu/pull/3888)
  - [Replace deprecated INVALID\_TERMINAL\_BLOCK with INVALID lvh 0x0](https://github.com/hyperledger/besu/pull/3882)
  - [Stop backward sync if genesis block has been reached](https://github.com/hyperledger/besu/pull/3869)
  - [Fix sync terminal condition, that should stop on difficulty &gt;= TTD](https://github.com/hyperledger/besu/pull/3866)
  - [Make pandas thread safe](https://github.com/hyperledger/besu/pull/3865)
  - [Fix: getMixHashOrPrevRandao to return the value present in the block header](https://github.com/hyperledger/besu/pull/3839)
  - [Stop the BlockPropagationManager when it receives the TTD reached event](https://github.com/hyperledger/besu/pull/3809)
  - [Fast sync with merge](https://github.com/hyperledger/besu/pull/3655)
  - [Persist last finalized block hash, prerequisite for The Merge](https://github.com/hyperledger/besu/pull/3432)
  - [Extend validateAndProcessBlock to return an error message in case of …](https://github.com/hyperledger/besu/pull/3411)
  - [refactor MergeCoordinator executeBlock to return validation reason](https://github.com/hyperledger/besu/pull/3384)
  - [Persist last finalized block hash](https://github.com/hyperledger/besu/pull/3372)
- Feature: transactions synchronization improvements
  
  - [Skip seen transactions](https://github.com/hyperledger/besu/pull/3626)
  - [Improve eth/66 support](https://github.com/hyperledger/besu/pull/3616)
  - [Tune transaction synchronization parameter to adapt to mainnet traffic](https://github.com/hyperledger/besu/pull/3610)
- Feature: JSON RPC response streaming
  
  - [Improve closing behavior of JsonResponseStreamer, and make clear it i…](https://github.com/hyperledger/besu/pull/3421)
  - [Response streaming: stop on IO error and remove queue management](https://github.com/hyperledger/besu/pull/3399)
- Code improvements
  
  - [Introduce RocksDbSegmentIdentifier to avoid changing the storage plug…](https://github.com/hyperledger/besu/pull/3755)
  - [Improve code readability](https://github.com/hyperledger/besu/pull/3667)
- Fix: block propagation and synchronization
  
  - [Refactor to async retrieve blocks, and change peer when retrying to get a block](https://github.com/hyperledger/besu/pull/3326)
  - [Do not exit ChainDownloader in case of a generic CancellationException](https://github.com/hyperledger/besu/pull/3319)
- Various
  
  - [Log initial sync stats every 10 secs at max to avoid spamming logs](https://github.com/hyperledger/besu/pull/3525)
  - [Disable RocksDB TTL compactions](https://github.com/hyperledger/besu/pull/3356)
  - [Filter Netty native lib errors likewise the pure Java implementation](https://github.com/hyperledger/besu/pull/3807)

Features for "The Merge" that I ported on the main branch, but have been originally written by others developers from ConsenSys on the merge branch.

Code for the following PRs was written by [Gary Schulte](https://lf-hyperledger.atlassian.net/wiki/people/6047b948b020eb00684030b6?ref=confluence) [Justin Florentine](https://lf-hyperledger.atlassian.net/wiki/people/60be12f85c64b100711c51d4?ref=confluence) [Daniel Lehrner](https://lf-hyperledger.atlassian.net/wiki/people/712020:65dd696b-014d-45f5-8ae1-776ca8026634?ref=confluence) [Jiri Peinlich (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/6182724316119e0069a00015?ref=confluence)

- [Execution specific RPC endpoint](https://github.com/hyperledger/besu/pull/3470)
- [Add components to handle the transition from PoW to PoS](https://github.com/hyperledger/besu/pull/3462)
- [Add The Merge core components](https://github.com/hyperledger/besu/pull/3461)
- [Add header validation rules needed to validate The Merge blocks](https://github.com/hyperledger/besu/pull/3454)
- [Add PostMergeContext that will stop syncing after the switch to PoS](https://github.com/hyperledger/besu/pull/3453)
- [Rename MergeOptions to MergeConfigOptions to follow the standard](https://github.com/hyperledger/besu/pull/3451)
- [New MutableBlockchain method rewindToBlock by hash prerequisite for T…](https://github.com/hyperledger/besu/pull/3444)
- [Merge: extend block creation and mining to support The Merge](https://github.com/hyperledger/besu/pull/3412)
- [Merge: port of backward sync](https://github.com/hyperledger/besu/pull/3410)
- [Merge: add terminal block number and hash to genesis config options](https://github.com/hyperledger/besu/pull/3392)

### Maintainer GitHub handle: macfarla

Maintainer org: ConsenSys

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Amacfarla+label%3Amainnet](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Amacfarla%20label%3Amainnet)

Details on mainnet contributions

- Trace APIs - implement the remaining endpoints - worked with frankisawesome, mark-terry and pinges on these 
  
  - trace\_callMany [#2886](https://github.com/hyperledger/besu/issues/2886)
  - trace\_rawTransaction [#2887](https://github.com/hyperledger/besu/issues/2887)
  - trace\_get [#2889](https://github.com/hyperledger/besu/issues/2889)
- bugfix
  
  - [Prevent connecting to self enode](https://github.com/hyperledger/besu/issues/3322)
  - [Fixed bug with contract address supplied to \`debug\_accountAt\`](https://github.com/hyperledger/besu/pull/3518)
  - [Fixed bug where GraphQL "any" topic does not return any results](https://github.com/hyperledger/besu/issues/3519)
  - [Handle null pointer caused by empty json](https://github.com/hyperledger/besu/pull/3298)
- CI improvements
  
  - [LGTM config file preventing out of memory errors](https://github.com/hyperledger/besu/issues/3670)
  - [CodeQL config file preventing out of memory errors](https://github.com/hyperledger/besu/pull/3877)
  - [Add trivy docker scan](https://github.com/hyperledger/besu/pull/3295)
  - [Separate CI steps for spotless and DCO](https://github.com/hyperledger/besu/issues/3456)

### Maintainer GitHub handle: pinges

Maintainer org: ConsenSys

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+author%3Apinges+is%3Aclosed+label%3Amainnet](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20author%3Apinges%20is%3Aclosed%20label%3Amainnet)

Details on mainnet contributions

- Trace APIs - implement the remaining endpoints - worked with frankisawesome, mark-terry and macfarla on these 
  
  - trace\_callMany [#2886](https://github.com/hyperledger/besu/issues/2886)
  - trace\_rawTransaction [#2887](https://github.com/hyperledger/besu/issues/2887)
  - trace\_get [#2889](https://github.com/hyperledger/besu/issues/2889)
- bugfix
  
  - [Fix Null pointer exception in VertxPeerDiscoveryController](https://github.com/hyperledger/besu/pull/3405)

### Maintainer GitHub handle: mark-terry

Maintainer org: ConsenSys

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Amark-terry+label%3Amainnet](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Amark-terry%20label%3Amainnet)

Details on mainnet contributions

- Trace APIs - implement the remaining endpoints - worked with frankisawesome, pinges and macfarla on these 
  
  - trace\_callMany [#2886](https://github.com/hyperledger/besu/issues/2886)
  - trace\_rawTransaction [#2887](https://github.com/hyperledger/besu/issues/2887)
  - trace\_get [#2889](https://github.com/hyperledger/besu/issues/2889)

### Maintainer GitHub handle: frankisawesome

Maintainer org: ConsenSys

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Afrankisawesome+label%3Amainnet](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Afrankisawesome%20label%3Amainnet)

Details on mainnet contributions

- Trace APIs - implement the remaining endpoints - worked with pinges, mark-terry and macfarla on these 
  
  - trace\_callMany [#2886](https://github.com/hyperledger/besu/issues/2886)
  - trace\_rawTransaction [#2887](https://github.com/hyperledger/besu/issues/2887)
  - trace\_get [#2889](https://github.com/hyperledger/besu/issues/2889)
- [Allow optional API methods with no authentication](https://github.com/hyperledger/besu/pull/3382)
- [Add uPNP only for P2P NAT method](https://github.com/hyperledger/besu/pull/3250)
- bugfix
  
  - [Fixed Null pointer exception in DeFramer](https://github.com/hyperledger/besu/pull/3711)

### Maintainer GitHub handle: taccatisid

Maintainer org: ConsenSys

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Ataccatisid+label%3Amainnet](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Ataccatisid%20label%3Amainnet)

Details on mainnet contributions

- code improvement
  
  - [Refactor timer from BesuRunner into TransactionPoolEvictionService](https://github.com/hyperledger/besu/pull/3172)

### Maintainer GitHub handle: wcgcyx

Maintainer org: ConsenSys

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Awcgcyx+label%3Amainnet](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Awcgcyx%20label%3Amainnet)

Details on mainnet contributions

- code improvement
  
  - [Make warnings consistent between CLI, ENV and TOML](https://github.com/hyperledger/besu/issues/2069)

### Maintainer GitHub handle: siladu

Maintainer org: ConsenSys

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Asiladu+label%3Amainnet](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Asiladu%20label%3Amainnet)

Details on mainnet contributions

- code improvement
  
  - [Ensure port clash is reported when engine-rpc-port clashes with default websocket port](https://github.com/hyperledger/besu/pull/3750)

### Maintainer GitHub handle: matkt

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Amatkt+is%3Amerged](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Amatkt%20is%3Amerged)

Maintainer org: ConsenSys

Details on mainnet contributions

- Fix mainnet launcher issue
  
  - [https://github.com/hyperledger/besu/pull/3352](https://github.com/hyperledger/besu/pull/3352)
- Snapsync implementation
  
  - [https://github.com/hyperledger/besu/pull/3572](https://github.com/hyperledger/besu/pull/3572)
  - [https://github.com/hyperledger/besu/pull/3601](https://github.com/hyperledger/besu/pull/3601)
  - [https://github.com/hyperledger/besu/pull/3625](https://github.com/hyperledger/besu/pull/3625)
  - [https://github.com/hyperledger/besu/pull/3656](https://github.com/hyperledger/besu/pull/3656)
  - [https://github.com/hyperledger/besu/pull/3703](https://github.com/hyperledger/besu/pull/3703)
  - [https://github.com/hyperledger/besu/pull/3710](https://github.com/hyperledger/besu/pull/3710)
  - [https://github.com/hyperledger/besu/pull/3754](https://github.com/hyperledger/besu/pull/3754)
  - [https://github.com/hyperledger/besu/pull/3761](https://github.com/hyperledger/besu/pull/3761)
  - [https://github.com/hyperledger/besu/pull/3773](https://github.com/hyperledger/besu/pull/3773)
  - [https://github.com/hyperledger/besu/pull/3920](https://github.com/hyperledger/besu/pull/3920)
- Checkpoint sync implementation
  
  - [https://github.com/hyperledger/besu/pull/3849](https://github.com/hyperledger/besu/pull/3849)
- Fix ethstats issue
  
  - [https://github.com/hyperledger/besu/pull/3729](https://github.com/hyperledger/besu/pull/3729)
- Fix issues on bonsai
  
  - [https://github.com/hyperledger/besu/pull/3712](https://github.com/hyperledger/besu/pull/3712) (bonsai issue with fastsync)
  - [https://github.com/hyperledger/besu/pull/3645](https://github.com/hyperledger/besu/pull/3645) (nullpointer on bonsai)
  - [https://github.com/hyperledger/besu/pull/3684](https://github.com/hyperledger/besu/pull/3684) (bonsai storage modification to work with snapsync)
- Candidate fix for the issue "Invalid column family specified in write batch"
  
  - [https://github.com/hyperledger/besu/pull/3940](https://github.com/hyperledger/besu/pull/3940)

### Maintainer GitHub handle: jflo

Query for mainnet label on closed PRs. [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Ajflo+is%3Amerged+updated%3A%3E%3D2022-01-01](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Ajflo%20is%3Amerged%20updated%3A%3E%3D2022-01-01)

Maintainer org: ConsenSys

Details on mainnet contributions

- JWT and Websockets, mostly on engine api
  
  - [https://github.com/hyperledger/besu/pull/4039](https://github.com/hyperledger/besu/pull/4039)
  - [https://github.com/hyperledger/besu/pull/4019](https://github.com/hyperledger/besu/pull/4019)
  - [https://github.com/hyperledger/besu/pull/3657](https://github.com/hyperledger/besu/pull/3657)
  - [https://github.com/hyperledger/besu/pull/3508](https://github.com/hyperledger/besu/pull/3508)
  - [https://github.com/hyperledger/besu/pull/3493](https://github.com/hyperledger/besu/pull/3493)
  - [https://github.com/hyperledger/besu/pull/3834](https://github.com/hyperledger/besu/pull/3834)
- Engine API
  
  - [https://github.com/hyperledger/besu/pull/3350](https://github.com/hyperledger/besu/pull/3350)
- Merge related
  
  - [https://github.com/hyperledger/besu/pull/3976](https://github.com/hyperledger/besu/pull/3976)
  - [https://github.com/hyperledger/besu/pull/3944](https://github.com/hyperledger/besu/pull/3944)
  - [https://github.com/hyperledger/besu/pull/3941](https://github.com/hyperledger/besu/pull/3941)
  - [https://github.com/hyperledger/besu/pull/3903](https://github.com/hyperledger/besu/pull/3903)
  - [https://github.com/hyperledger/besu/pull/3757](https://github.com/hyperledger/besu/pull/3757)
  - [https://github.com/hyperledger/besu/pull/3726](https://github.com/hyperledger/besu/pull/3726)
  - [https://github.com/hyperledger/besu/pull/3623](https://github.com/hyperledger/besu/pull/3623)
  - [https://github.com/hyperledger/besu/pull/3548](https://github.com/hyperledger/besu/pull/3548)
  - [https://github.com/hyperledger/besu/pull/3224](https://github.com/hyperledger/besu/pull/3224)
- Bugfixes and releases
  
  - [https://github.com/hyperledger/besu/pull/4032](https://github.com/hyperledger/besu/pull/4032)
  - [https://github.com/hyperledger/besu/pull/3979](https://github.com/hyperledger/besu/pull/3979)
  - [https://github.com/hyperledger/besu/pull/3978](https://github.com/hyperledger/besu/pull/3978)
  - [https://github.com/hyperledger/besu/pull/3965](https://github.com/hyperledger/besu/pull/3965)
  - [https://github.com/hyperledger/besu/pull/3937](https://github.com/hyperledger/besu/pull/3937)
  - [https://github.com/hyperledger/besu/pull/3861](https://github.com/hyperledger/besu/pull/3861)
  - [https://github.com/hyperledger/besu/pull/3844](https://github.com/hyperledger/besu/pull/3844)
  - [https://github.com/hyperledger/besu/pull/3840](https://github.com/hyperledger/besu/pull/3840)
  - [https://github.com/hyperledger/besu/pull/3657](https://github.com/hyperledger/besu/pull/3657)
  - [https://github.com/hyperledger/besu/pull/3305](https://github.com/hyperledger/besu/pull/3305)
  - [https://github.com/hyperledger/besu/pull/3258](https://github.com/hyperledger/besu/pull/3258)

### Maintainer GitHub handle: ahamlat

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+author%3Aahamlat](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Agaryschulte%20is%3Amerged%20)

Maintainer org: ConsenSys

Details on mainnet contributions, largely discovery and profiling for besu performance cases.

- performance tuning mainnet use cases:
  
  - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/document/d/18UIk2v-yUFZjpQGf-s2F8RdH82cDniO2y3nPcp73VlY/edit?usp=sharing)
  - rocksdb performance and memory consumption:
    
    - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/document/d/1S8EyilVZe3brBsRdpDqPZQoI6tmqnASgZrDLjlef8H0/edit?usp=sharing)
  - fast sync optimizations:
    
    - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/presentation/d/1yd6pnF1JdLwJINHwb8xsFYeL56pjWsBj/)
  - peering investigations
    
    - [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/document/d/1RmnnwW0LarFr-mN2TxMCZcebQ3shG_pan7dsUG9QVbM/edit?usp=sharing)

### Maintainer GitHub handle: garyschulte

Query for mainnet label on closed PRs [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed+author%3Agaryschulte+is%3Amerged+](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20author%3Agaryschulte%20is%3Amerged%20)

Maintainer org: ConsenSys

Details on mainnet contributions

- Support for arm64 native and docker images:
  
  - [https://github.com/hyperledger/besu-native/pull/61](https://github.com/hyperledger/besu-native/pull/61)
  - [https://github.com/hyperledger/besu/pull/3904](https://github.com/hyperledger/besu/pull/3904)
  - [https://github.com/hyperledger/besu/pull/3848](https://github.com/hyperledger/besu/pull/3848)
  - [https://github.com/hyperledger/besu/pull/3820](https://github.com/hyperledger/besu/pull/3820)
  - [https://github.com/hyperledger/besu/pull/3816](https://github.com/hyperledger/besu/pull/3816)
- Merge engine api and merge transition implementation:
  
  - [https://github.com/hyperledger/besu/pull/3248](https://github.com/hyperledger/besu/pull/3248)
  - [https://github.com/hyperledger/besu/pull/3302](https://github.com/hyperledger/besu/pull/3302)
  - [https://github.com/hyperledger/besu/pull/3341](https://github.com/hyperledger/besu/pull/3341)
  - [https://github.com/hyperledger/besu/pull/3379](https://github.com/hyperledger/besu/pull/3379)
  - [https://github.com/hyperledger/besu/pull/3393](https://github.com/hyperledger/besu/pull/3393)
  - [https://github.com/hyperledger/besu/pull/3437](https://github.com/hyperledger/besu/pull/3437)
  - [https://github.com/hyperledger/besu/pull/3447](https://github.com/hyperledger/besu/pull/3447)
  - [https://github.com/hyperledger/besu/pull/3486](https://github.com/hyperledger/besu/pull/3486)
  - [https://github.com/hyperledger/besu/pull/3501](https://github.com/hyperledger/besu/pull/3501)
  - [https://github.com/hyperledger/besu/pull/3547](https://github.com/hyperledger/besu/pull/3547)
  - [https://github.com/hyperledger/besu/pull/3554](https://github.com/hyperledger/besu/pull/3554)
  - [https://github.com/hyperledger/besu/pull/3565](https://github.com/hyperledger/besu/pull/3565)
  - [https://github.com/hyperledger/besu/pull/3569](https://github.com/hyperledger/besu/pull/3569)
  - [https://github.com/hyperledger/besu/pull/3575](https://github.com/hyperledger/besu/pull/3575)
  - [https://github.com/hyperledger/besu/pull/3607](https://github.com/hyperledger/besu/pull/3607)
  - [https://github.com/hyperledger/besu/pull/3615](https://github.com/hyperledger/besu/pull/3615)
  - [https://github.com/hyperledger/besu/pull/3696](https://github.com/hyperledger/besu/pull/3696)
  - [https://github.com/hyperledger/besu/pull/3728](https://github.com/hyperledger/besu/pull/3728)
  - [https://github.com/hyperledger/besu/pull/3748](https://github.com/hyperledger/besu/pull/3748)
  - [https://github.com/hyperledger/besu/pull/3871](https://github.com/hyperledger/besu/pull/3871)
  - [https://github.com/hyperledger/besu/pull/3875](https://github.com/hyperledger/besu/pull/3875)
  - [https://github.com/hyperledger/besu/pull/3889](https://github.com/hyperledger/besu/pull/3889)
  - [https://github.com/hyperledger/besu/pull/3894](https://github.com/hyperledger/besu/pull/3894)
  - [https://github.com/hyperledger/besu/pull/3913](https://github.com/hyperledger/besu/pull/3913)
- Bonsai support
  
  - [https://github.com/hyperledger/besu/pull/3707](https://github.com/hyperledger/besu/pull/3707)
  - [https://github.com/hyperledger/besu/pull/3720](https://github.com/hyperledger/besu/pull/3720)
  - [https://github.com/hyperledger/besu/pull/3734](https://github.com/hyperledger/besu/pull/3734)
  - [https://github.com/hyperledger/besu/pull/3793](https://github.com/hyperledger/besu/pull/3793)
  - [https://github.com/hyperledger/besu/pull/3930](https://github.com/hyperledger/besu/pull/3930)
- General UX
  
  - [https://github.com/hyperledger/besu/pull/3907](https://github.com/hyperledger/besu/pull/3907)
  - [https://github.com/hyperledger/besu/pull/3936](https://github.com/hyperledger/besu/pull/3936)
  - [https://github.com/hyperledger/besu/pull/3958](https://github.com/hyperledger/besu/pull/3958)

### Maintainer GitHub handle: diega

Query for mainnet label on closed PRs: [https://github.com/hyperledger/besu/pulls?q=is%3Apr+is%3Aclosed++label%3Amainnet+author%3Adiega+created%3A2022-01-01..2022-06-30+](https://github.com/hyperledger/besu/pulls?q=is%3Apr%20is%3Aclosed%20%20label%3Amainnet%20author%3Adiega%20created%3A2022-01-01..2022-06-30%20)

Maintainer org: Ethereum Classic Cooperative

Details on mainnet contributions:

- Code improvements
  
  - [SLF4J migration](https://github.com/hyperledger/besu/pull/3285)
  - Junit5 migrations ([here](https://github.com/hyperledger/besu/pull/3815), [here](https://github.com/hyperledger/besu/pull/3850) and [here](https://github.com/hyperledger/besu/pull/3814))
  - [New errorprone rule](https://github.com/hyperledger/besu/pull/3759)
- Features
  
  - [Add IPC transport](https://github.com/hyperledger/besu/pull/3695)
- Bug fixes
  
  - [Flacky tests fix](https://github.com/hyperledger/besu/pull/3852)
  - [Fix CORS regression](https://github.com/hyperledger/besu/pull/3296)

Document generated by Confluence on Nov 26, 2024 12:59

[Atlassian](http://www.atlassian.com/)
