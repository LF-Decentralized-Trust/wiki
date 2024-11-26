1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Performance &amp; Stability](22155524.html)

# Besu : Q4 2022 Stability and Performance Improvements

Created by Matt Nelson (Deactivated), last modified on Nov 04, 2022

## Stability

**Some solutions already implemented** 

- Sync stalling
- - Rules about what is considered our best peer post-merge is not implemented
  - Trying the same peer over and over again (shuffling the peers)
- Invalid block errors
- - Consensus layer is on the fork with bad data
  - Besu has a storage exception to report the invalid block to the consensus layer, which sets us off to a wrong fork (potential fix by Justin; [GH issue](https://github.com/hyperledger/besu/issues/4512))
  - Potentially another Besu internal error could cause invalid blocks of which we don’t know about yet

**Potential solution identified**  

- Worldstate root mismatch
- - Bonsai and snapshots
  - Solution: Confirmed working for many cases, needs more testing and handling of any corner cases

**Issues around peering**

- Need restart to find new peers sometimes during sync
- - Potentially because of the lack of evaluating of peers during sync and post sync
  - Solution: ??
- Losing many peers
- - Because threads were blocked, we lost many peers
  - Vertx for example uses different approaches to threading
  - Solution: ??

**Issues on user experience** 

- Difficulty in reliably communicating with new/inexperienced users
- - Docs &amp; lack of education
  - More complicated set up post-merge
  - Solution: Write up ‘What to expect from staking at home’ and FAQ for Besu Docs
- Out of Memory errors
- - Documentation on how kind of memory config is needed
  - No mechanism to detect memory leaks
  - Potential mitigation: make deploying Besu easier by providing default configs
  - Solution: ??
- Users don’t know how much syncing is done
- - Insufficient logging &amp; bad log UX
  - Solution/plan: ??
- Users hesitant to update or restart Besu with the latest version due to the impression of being unstable

**Issues with RPC calls**

- Incompatibilities with RPC spec / not-same-as-geth causing crashes
- - Does not meet Chainlink and other orgs needs for RPC calls (accuracy, speed)
  - Do we implement all of the RPC interfaces that Geth does? I.e. Logger, Trace (all the methods)
  - Solution: ??
- Some specific RPC calls (trace/debug) take a long time or OOM
- - Lack of testing of large RPC calls
  - Might need to understand the root cause better
  - Solution: ?

## Performance

**Staking Performance**

- Poor execution performance leading to missed attestations
- - More investigation ongoing, and some user stories being created
- Poor block production
- - As we tweak the tx pool to build the best block for the user with valuable/DOS-resistant transactions, we need to ensure no performance hit to the client - uses a lot of CPU because we are repeating the block production until CL asks for it
  - Late blocks could also cause import challenges, would cause restart of the building of the block
  - Snapshots could help with concurrency in this case
  - 4844 could alter this process and requires good performance as well

**I/O and Disk Performance** 

- Besu has problems with slow IO/disks → Besu is generating a lot of IO
- - We are not using the flat DB during block processing, so have to gather a lot of data from disk
  - Need caching in more areas - R/W caching
  - Doing less work, persisting less to the disk, persisting trie logs but not the worldstate (Amez / Karim)
  - The first hotspot in Besu is reading data from RocksDB using the RocksDB.get method. This is mainly caused by the fact that we have to get most of the WorldState nodes from the Patricia Merkle Trie
  - Need to identify more areas where IO contention is commonplace

**Trace Performance** 

- Poor performance of tracing of blocks / transactions
- - Not sure why we are slow
  - Many times Besu would crash when tracing a full block
  - OOM errors
  - Short timeout can cause issues
  - Is db tuned for tracing?
  - [3786](https://github.com/hyperledger/besu/issues/3786)
  - Will need good performance for any rollups use-cases
  - Solution?: Instead of replaying each time the traces for each user request why not saving this trace result in a separate database or a separate module instead of saving the block and the worldstate for each block

<!--THE END-->

- Solution?: Separate into a different microservice

<!--THE END-->

- Solution?: Separate the query part of Besu into a completely separate process. Queries that are asking Besu questions related to the chain do not need to slow down the main flow.

**Sync Performance**

- Poor syncing performance (still the case with 22.10.0?)
- - Do we need to verify the proof of work blocks on Mainnet?
  - Useless conversion from byte to RLP and back during sync
  - Sometimes we are stuck for some time during a snap sync (need investigation)
- Full sync / forest performance (also snapsync for the block downloading part)
- - Persisted worldstate changes may be able to help with full sync on Bonsai
  - Forest we need to determine what the areas are for performance improvements - some of the recent bonsai improvements can be tweaked to suit forest use-case (unknown though)

**EVM Performance - Pending Amez Availability and IMAPP Testing** 

- We need analysis that will tell us Gas cost of each operation corresponds to the algorithmic complexity of Besu implementation. Bonsai might have consequences on algorithmic complexity for some operations.
- - [IMAPP testing](https://github.com/imapp-pl/gas-cost-estimator/blob/master/docs/gas-cost-estimator.md) - we need an overall analysis (Matt has connected with this team for a profile)
  - Do not have a profile of Besu’s EVM performance (work with Danno?)
  - SLOAD, SSTORE - slowest vs gas cost?
  - EVM performance improvements often appear without context and the broader team is unsure of how the optimizations are created. Is there a standard playbook of optimizations that we are running through, or are there EVM specific performance observations that we are reacting to?

**Do we know how we can solve these problems?**

- Having automatic test on nightly/ci to detect regression asap
- Having more modularity
- Having a tracing solution on the JAVA level (improve observability)
- Using torrent for downloading the block during the initial sync (archive)?
- Separate the query part of Besu into a completely separate process. Queries that are asking Besu questions related to chain do not need to slow down the main flow.

# Process Improvements (Q1?)

**Performance Testing**

- Lack of performance testing, especially on RPC methods
- - How do we get alerts and be aware that there is an actual performance regression?
  - Automated performance testing each release, nothing for the moment

<!--THE END-->

- - Hive tests return the time the calls are taking, but small load
  - Can we separate some RPC methods into separate microservices?

**Slow Release / Testing Process** **(CPU, test bounding, process)** 

- Manual release process with a lot of wasted time waiting for builds that could be avoided
- - Waiting for multiple full builds to complete because you are merging a PR or changing version number, doesn’t need a full build
  - With code changes, then a full build should be required
- Make it easier/faster to run all the tests locally, or avoid the need to create a draft PR for running tests remotely
- - Support for many features causes tests to be slow (ETC tests, Quorum tests, etc.) when they are not necessarily needed for certain modifications

**Issues with the process** 

- Late discovered regressions
- - Need a more comprehensive testing strategy across contributors
  - Solution: ??

**Establish better process on how to respond to the problem we discover** 

- Good case study: sepolia issue over the weekend on Oct 29/30

Document generated by Confluence on Nov 26, 2024 13:01

[Atlassian](http://www.atlassian.com/)
