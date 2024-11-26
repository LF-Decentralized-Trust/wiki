1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Design Documents](Design-Documents_22153916.html)

# Besu : Modular Besu

Created by Matt Nelson (Deactivated), last modified on Aug 02, 2023

Modularization of Hyperledger Besu - can we make Besu more flexible by factoring it into decoupled components which can be exchanged for alternate implementations?

**Goal of this document:** 

- **Starting a conversation about modularizing Besu.**

<!--THE END-->

- Keeping track of the discussions.

# General context

We are getting various signals that the future of blockchain technologies is all about modularity.  If L2 chains on top of L1 chains are the future, how can we make an L1 client that can be composed from various implementations of sub-components?  We also see evidence of this elsewhere - The Merge separated consensus from execution. MEV actors like Flashbots separate proposing a block from building it. Even within clients, we see teams like Erigon re-writing their client in different languages, and combining the best performing subcomponents regardless of language.

Apart from the general direction of blockchain, software has been trending away from monolithic implementations, in order to maximize developer efficiency, and reduce change fatigue. Smaller components can reach stability more easily than large monoliths can. 

[Current monolith structure](https://miro.com/app/board/uXjVMCPHPfg=/) - password: hyperledger

# Goals

The goals of this work are to expand the contexts in which Besu can be valuable to users and operators while reducing tech debt in maintenance of the code base and its release process. New use-cases require client modification (customization of Besu's rules). New use-cases may also want some, but not all of the functionality that Besu provides. These use-cases may also want an easy way to package and distribute their work with Besu's permissive licensing.

To support flexibility and development of Besu in novel context's going forward, the client needs a new approach to its existing monolithic architecture. Today, the protocol schedule defines how the monolith operates, with different sets of rules, but is unwieldy and hard to modify. We need a new approach that allows for the evolution of the client without the baggage of the monolithic approach. 

Enter modularity.

The modularity work can be largely set against three goals:

1. Resolution of tech debt - to support today's existing use-cases in Besu, we have an unwieldy monolithic approach. This is becoming hard to manage and should be addressed (with the added benefit of the two below goals).
   
   1. Incremental, mergeable, no big bangs, review cycle to warrant inclusion
2. Better Distribution - Tailoring the code-base by customizing a set of modules of "Besu" to provide users exactly what they need in context. I.e. I need a private network distribution of Besu, so I need PoA consensus, but not PoW validation rules. These distributions can also have their own CI/release process to adjust testing definition and quality standards. These can also be for individual modules like the EVM.
3. Better Client Modification - Tailoring the run-time to suit user/developer needs, allowing for deep customization of the client, its rules, and components. Here we have some approaches:
   
   1. Plug-ins and the plug-in API - Using the existing plug-in API, developers can inject modifications into the Besu code at start up that replaces the "vanilla" rule-sets and functionality. It also allows for new components to interface with Besu via the API, but does not allow for whole-sale swapping of components.
   2. Modules - Creating boundaries and interfaces in the code-base so Besu's existing components can stand-alone and/or be replaced with like modules. This opens up the client to flexibility of its modules, like replacing the EVM or consensus mechanisms with novel ones (or a new storage/peering stack, etc.). This can help with tech debt, but is a heavy handed approach to customization.
   3. Remote APIs - It is currently possible to drive a blockchain purely over the rpc-apis, using the Engine API developed to facilitate Proof of Stake. This approach could be expanded to allow for other use cases that want to interact with the blockchain.

The latter two goals are somewhat linked. Distributions can be tackled with any client modification approach. APIs vs. modules, however, should be considered as differing tracks. 

# Potential Benefits

With the above in mind - we outline some potential benefits:

1. Releases - finer grained components could have a finer grained release process, speeding up the release cycle.
   
   1. Distributions can be cut more easily for specific use-cases, based on what components and customizations to the base client are needed (Mainnet, ETC, Private nets, standalone EVM)
2. Customization - Modular components with plug-ins enable customization of the client to fit the needs of different use-cases in a clean way, with well defined APIs and module boundaries
   
   1. Linea Rollup definition, using plug-ins and novel components to allow Besu to operate a L2 network. Distributing these changes in a repeatable, reliable way to users and node operators.
3. Increases pace of innovation - experiments and prototypes become much easier, faster, and lower risk to pursue.
   
   1. New use-cases for Besu can be piloted quickly, without maintaining complex forks of the Besu client
4. End User Control - software modularity should lend itself easily to greater customizability for the end user. 
   
   1. Client modification can be done easily by swapping or altering components. Altered components are Besu at their core, but the plug-in system changes their behavior. Modular components may be Besu components or completely novel components that work with Besu via documented interfaces (i.e. a Rust EVM).
5. Reduces cognitive complexity - better defined scope for contributors to target a specific part of the codebase.  New developers can focus more narrowly, and get up to speed faster with fewer distractions.

# General Concerns and Challenges, Possible Mitigations

1. Engineering effort around Besu
   
   1. Large engineering effort - we will need to always prefer incremental delivery over greenfield or big-bang approaches.
   2. Series of workshops to define the work
2. Technical project organization
   
   1. Communication planning
      
      1. Internal - how do we make sure all Besu contributors can keep their finger on the pulse of this initiative.
      2. External - do we need to convey this to external users or interested parties. If so, how?
   2. multi stakeholders discussion, federating people around modular besu. Examples of stakeholders this would benefit:
      
      1. MEV searchers
      2. rollup implementers
      3. infrastructure providers like Infura or Alchemy
      4. developers

# Besu Minimum Useful Components

Hypothetical situations that would benefit from component composition:

- [Isolatable execution engine](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=22155856#BesuasaModularClientfortheMerge%28OLD%29-Approach%232%E2%80%9CAnExecutionEngineShellProject%E2%80%9D)
  
  - EVM and state are needed and not the Consensus. Ex: Rollups, Hedera Hashgraph, EVM testing tools
- Transaction pool, transaction validation, and block gossip needed. MEV searchers. 
  
  - Possibly EVM needed to for gas use analysis.
- [Use case specific builds](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=22155856#BesuasaModularClientfortheMerge%28OLD%29-Approach%231%E2%80%9CHyperledger/BesuasDebian%E2%80%9D)
  
  - All-in-one mainnet client that provides ethereum proof-of-stake as its only consensus mechanism.
- State Synch Testbed, rapid prototyping for data stores which can be populated with state changes from a moving chain.

# Potential First Steps

- [Catalog all components](Modularity-Implementation-Approach_22155496.html)
- Test approach on one or more situation listed above.
- Extrapolate out rough timeline on MVP scope and modules timing vs the catalog.
- Scope MVP (minimum viable platform)

# Questions

1. Plug-ins vs. modules - will we expand the plug-in API to be unwieldy and exposing too much?

* * *

# Debrief of meeting with Erigon

**Meeting #1 - 9/14/21**

Participants: Alexey, Madeline, Sajida

- Sentry component
- C++ and rust implementation are being done
- Each reimplem takes less time than the precedent
- Contrary to popular belief, it’s not hard to rewrite things from scratch. Might even be easier.
- Alexey wants to start a Java reimplementation, and they don’t have anyone to do it in java
- Besu in ⅔ years - he sees a dead end for the monolith model like besu, nethermind, openE
- Geth snapshotter; Geth realised that traversing the tree
- Collaboration would be:
- - Join their family of product
  - Reimplement core product like evm
  - Make them compatible with their others components
  - That will be a 4th compatible implement to their portfolio

<!--THE END-->

- Erigon is funded by EF, gnosis and small amount from various org
- They are hiring for the go implementation, they have 2 active dev, they might bring couple other, it is a small team
- - Cpp team : ⅘ ppl
  - Rust team: 2,5 ppl , some of them are not employed but just contributing part time

<!--THE END-->

- Cycles of modularization
- - 1st rewrite: 2017 - 4 years or 3,5 years
  - 2st rewrite may 2020 - c++ w/ couple ppl , now they are almost finish the core component (1 year and half) might get the core component roughly finished end of 2021
  - 3rd rewrite jan 2021 - rust, could get to the same level as the other by the end of 2021, so 1 year; Rust will be ahead of the C++ implementation
  - He predicts that with Besu in 6 months because we already have a codebase, we don’t start from scratch.
- Should we join the effort ? should we invest in Erigon?

**Meeting #2 - 10/6/21**

Participants: Artem +1, Gary, Sajida

- Starting from scratch is easier than refactoring existing code into Erigon architecture.
- Artem used to work on OE and is now working on Acula (rust) mainly alone for 4 months and it’s already passing consensus.
- Modularization
- - Breaking the monolith - reusable parts: tx pool, consensus engine, sync module
  - Sync module is interesting alone to process by block or by stage
  - might require a change of database, stage sync require MVCC database  (LMDB, Badger LSMbased, B+2
  - it might be possible to start module by module.
  - Data model could be a good start (might reduce space consumption).
  - We already have a pluggable storage engine that we could Interface of the pluggable storage resembles MDB/LMDB/DBX Peer 2 peer part (sentry) of Geth was re-used by Erigon but the plumbing is totally different
  - Erigon is heavily optimized toward sequential writes. Random reads / Sequential write - very fast for MDBX.
- EVM bug leveraging a hole in the memory as triggered by a tx, that was broadcasted everywhere and affected all clients (even on Binance smart chain) - spreads like wildfire.
- If they have a clique ethereum, fork the module, modify it and connect to JRPC and connect the rest of Erigon. You just had to invest time in creating a module and you get the rest of the client for free.
- Erigon can be run as a Kubernetes cluster.

<!--THE END-->

- Transaction pool should get EVM inside and be able to be part of the consensus. It is a security parameter. If we have a DOS attack, the tx pool should guard the blockchain from an attack. Having multiple tx pools that could coexist: one for MEV, on maybe getting DOS in this scenario and one running smoothly. And then you can pick the one that can do the work. Any tx pool could go down while the node is still up. Node is behind the “forest” of other P2P nodes. Ex: Besu sentry (x10 instances), all sentries go down but the core that runs the database/blockchain and stores the chain stays up.
- The idea of modularity; you make the core, the spec, and the rest is up to you.
- Andrew: maintainer of yellow paper, has an enum that maps to yellow paper parts. He runs silkworm - very good resource to start the work. Should be interesting to Justin.

<!--THE END-->

- Estimation: 2 engineers in 4 months. (Artem did it alone in 3/4 months)
- RandD type of work, 100% dedicated team; no mainnet work.
- [https://medium.com/@giulio.rebuffo/silkworm-and-akula-the-future-of-erigon-fda4d6813505](https://medium.com/@giulio.rebuffo/silkworm-and-akula-the-future-of-erigon-fda4d6813505)
- staged sync:
- - [https://github.com/ledgerwatch/erigon/blob/devel/eth/stagedsync/README.md](https://github.com/ledgerwatch/erigon/blob/devel/eth/stagedsync/README.md)
- download headers/download blocks: 2 first stages, then silkworm will run the blocks
- Leading C++ implementation at this point: Silkworm
- - [https://github.com/torquem-ch/silkworm](https://github.com/torquem-ch/silkworm)

<!--THE END-->

- Very fruitful to invest R&amp;D in this because lots of work has been done so the cycle of reimplementation are getting smaller
- Refactor: use case -&gt; modularity for l2 , rollups, pluggable, MEV
- Argument:
- - database - we (besu) have a trie in a trie MPT (access complexity is multiplied). so just switching to another data model would increase our performance.
  - Erigon threw out the MPT (merkle patricia trie) completely and computes state root post execution and other than that we have a flat state. Plain state table: value = account, key = account address. We are almost there with bonsai on the flat storage but we should work on simplifying
  - using JRPC sure adds communication overhead but it brings so much value in other places that they (erigon) can live with it - JRPC could be replaced of course by something else, like jar(?)

## Attachments:

![](images/icons/bullet_blue.gif) [image2022-11-1\_15-39-3.png](attachments/22155011/22155858.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:00

[Atlassian](http://www.atlassian.com/)
