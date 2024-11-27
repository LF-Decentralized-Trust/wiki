1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Product requirements](Product-requirements_21016037.html)

# Hyperledger Iroha : Needs and Requirements

Created by Nikita Puzankov, last modified by lazaridiscom on Dec 02, 2021

Target release2.0.0Epic  
Document status

DRAFT

Document owner

[Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence)

Designer

[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence)

Developers

[Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) [Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence)

QA

## Goals

> Hyperledger Iroha v2 aims to be an even more simple, highly performant distributed ledger platform than Iroha v1. V2 carries on the tradition of putting on emphasis on having a library of pre-defined smart contracts in the core, so that developers do not have to write their own code to perform many tasks related to digital identity and asset management.

## Background and strategic fit

- [Iroha2 Whitepaper](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#11-relationship-to-hyperledger-fabric-hyperledger-sawtooth-hyperledger-besu-and-others)

## Assumptions

- [Users will work with provided client libraries (iOS, Android, JS)](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#12-mobile-and-web-libraries).
- [3f+1 nodes are enough to tolerate f Byzantine nodes in the network](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#21-p2p-network).
- [Iroha uses a simple data model made up of domains, peers, accounts, assets, signatories, and permissions, as shown in the figure below - all other entities are built on top of them](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#24-data-model).

## Requirements

### Sources

There are the following sources for all requirements:

1. The main source of core structure: [Iroha 2 white paper](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md), authored by [武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence)
2. [List of requests from the Soramitsu projects regarding features](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Requirements+from+leads+and+community)
3. Decisions made during the discussion, which are fixed in the [list of RFCs](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Requests+for+Comments)

### Functional

#### Peer to peer communication

IDItemEPICImportanceStatusADR/RFCNotesIF2-100[Peer to Peer Network Library](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#21-p2p-network)

[HI2-6](https://soramitsucoltd.aha.io/features/HI2-6)

[HI2-30](https://soramitsucoltd.aha.io/features/HI2-30)

MUST

DONE

[Networking stack](Networking-stack_21012097.html)

Plain TCP\\IP based protocol with [SCALE](https://github.com/paritytech/parity-scale-codec/) as de\\serialization format.

Iroha must have a specific peer-to-peer protocol for effective communication and provided it as a detachable library.

IF2-101[Transactions Time to Live](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Prevent+replay+of+rejected+transactions)[HI2-38](https://soramitsucoltd.aha.io/features/HI2-38)

MUST

[Prevent replay of rejected transactions](Prevent-replay-of-rejected-transactions_21016013.html)Iroha must provide the possibility to explicitly state time-to-live (TTL) for each transaction, so the clients can set time interval in which transactions should be confirmed and put into the block store or removed from the queue by timeout.IF2-102[Multisignature Transactions](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#25-smart-contracts)[HI2-13](https://soramitsucoltd.aha.io/features/HI2-13)

MUST

Iroha must provide the possibility to configure each account to have a list of signatories, which needs to provide their signatures to confirm the transaction.

Also, Iroha should provide the possibility to perform conditional multi-signature transactions, so the conditions will automate transaction creation or signing them

IF2-103Transaction dependencies

NOT DEFINED

[Transaction tags](Transaction-tags_21012333.html)(Proposed by Kamil') Iroha may provide a possibility to perform tag-based dependencies between transactions for making their sequence configurable by the client

#### Blocks storage

IDItemEPICImportanceStatusADR/RFCNotesIF2-200[World State View](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#28-data-storage)

MUST

DONE

In-memory, read fast data representation of the current World's State.IF2-201[Kura](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#28-data-storage)

[HI2-1](https://soramitsucoltd.aha.io/features/HI2-1)

[HI2-17](https://soramitsucoltd.aha.io/features/HI2-17)

[HI2-18](https://soramitsucoltd.aha.io/features/HI2-18)

[HI2-5](https://soramitsucoltd.aha.io/features/HI2-5)

MUST

DONE

Kura is a decorator on top of Disk Block Storage and provides validation and World State View synchronization functionality. IF2-202[Blocks Synchronization](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#210-data-synchronization-and-retrieval)

[HI2-2](https://soramitsucoltd.aha.io/features/HI2-2)

[HI2-43](https://soramitsucoltd.aha.io/features/HI2-43)

MUST

DONE

[Block Synchronization](Block-Synchronization_21012390.html)

Peers periodically gossip with each other, sharing the latest block hash. If the hashes differ, then the peers discover they are out of sync and request synchronization.

IF2-203Merkle Tree

MUST

DONE

[Merkle Tree](Merkle-Tree_21016011.html)Iroha provides a general purpose implementation of a Merkle Tree, which is used to verify the state of committed blocks and their transactions.

#### Consensus

IDItemEPICImportanceStatusADR/RFCNotesI2-300[Sumeragi](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#29-consensus)[HI2-3](https://soramitsucoltd.aha.io/features/HI2-3)

MUST

DONE

Iroha must have a reliable BFT consensus of blocks between all peers, which should keep effectively prevent attacks and malfunctioning in case of `n` of `2n+1` nodes are malicious/failing.

(details of Sumeragi are described in the white paper)

Sumeragi should be implemented as a detachable component and be available as a library, so other Hyperledger solutions can reuse it.

#### Queries

IDItemEPICImportanceStatusADR/RFCNotesI2-400[Iroha Queries](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#30-queries)[HI2-31](https://soramitsucoltd.aha.io/features/HI2-31)

MUST

DONE

Iroha Queries provide information about World State View based on client permissions.

#### Smart Contracts

IDItemEPICImportanceStatusADR/RFCNotesIF2-500Iroha Special Instructions mechanism

MUST

DONE

IF2-501Out of the box set of Iroha Special Instructions

[HI2-28](https://soramitsucoltd.aha.io/features/HI2-28)

[HI2-29](https://soramitsucoltd.aha.io/features/HI2-29)

[HI2-35](https://soramitsucoltd.aha.io/features/HI2-35)

MUST

DONE

Several Tiers of Iroha Special Instructions provide:

- Basic building blocks that can be used to build Custom Iroha Special Instructions
- Maintenance-related Iroha Special Instructions (Add Peer, Change Build Block Time, etc.)
- "Iroha Modules"-related Iroha Special Instructions (Bridge, DEX, etc.)

IF2-502[Permissions](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#211-data-permissions)[HI2-36](https://soramitsucoltd.aha.io/features/HI2-36)

MUST

IN-PROGRESS

[Permissions](Permissions_21012321.html)Permissions in Iroha implemented based on Assets and Iroha Special Instructions.IF2-503Triggers[HI2-37](https://soramitsucoltd.aha.io/features/HI2-37)

MUST

IN-PROGRESS

[Triggers](Triggers_21012568.html)Triggers in Iroha implemented based on Assets and Iroha Special Instructions.IF2-504Domain-Specific Language

COULD

[Iroha Special Instructions DSL](Iroha-Special-Instructions-DSL_21012073.html)Custom Iroha Special Instructions and usage of the full set of Iroha Special Instructions should be easy for developers.IF2-505Advanced Permissions Model

COULD

IN-PROGRESS

[Expand Iroha Permission model](Expand-Iroha-Permission-model_21012394.html)Full-fledged rights model in Iroha will greatly reduce the amount of server development for Iroha-based applications.

#### Modules

IDItemEPICImportanceStatusADR/RFCNotesIF2-600[Bridge](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#25-smart-contracts)

MUST

IN-PROGRESS

[Bridges](Bridges_21012327.html)The mechanism for communication between third-party blockchains.  
DEX

MUST

IN-PROGRESS

[DEX Generic Scenarios](DEX-Generic-Scenarios_21012490.html)The ability to exchange assets between accounts.

#### Maintenance

IDItemEPICImportanceStatusADR/RFCBrief descriptionNotesIF2-700Maintenance Endpoint

[HI2-26](https://soramitsucoltd.aha.io/features/HI2-26)

[HI2-27](https://soramitsucoltd.aha.io/features/HI2-27)

[HI2-46](https://soramitsucoltd.aha.io/features/HI2-46)

MUST

IN-PROGRESS

[Maintenance Endpoint](Maintenance-Endpoint_21012343.html) Iroha must provide a maintenance endpoint, which can be used for performing operations (control over node status), requesting statistics and health information and subscribing on the updates (new blocks, transaction status changes, etc.).

#### Clients

IDItemEPICImportanceStatusADR/RFCNotes  
HTTP API

MUST

IN-REVIEW

[Iroha API for Clients](Iroha-API-for-Clients_21012472.html)Because of clients restrictions decision about HTTP API was pushed forward.IF2-800Rust Client Library[HI2-32](https://soramitsucoltd.aha.io/features/HI2-32)

MUST

DONE

Iroha Client encapsulates network-related functionality and provides "local" Rust Interface for:

- Submitting of Iroha Special Instructions to Iroha Peer
- Querying Data from Iroha Peer
- Maintenance Endpoint API

IF2-801\`no-std\` client

COULD

CANCELLED

[Migration from Strings](Migration-from-Strings_21016362.html)  
IF2-802Mobile SDK

[HI2-33](https://soramitsucoltd.aha.io/features/HI2-33)

[HI2-9](https://soramitsucoltd.aha.io/features/HI2-9)

[HI2-8](https://soramitsucoltd.aha.io/features/HI2-8)

COULD

CANCELLED

IF2-803Web SDK

[HI2-34](https://soramitsucoltd.aha.io/features/HI2-34)

[HI2-10](https://soramitsucoltd.aha.io/features/HI2-10)

COULD

CANCELLED

[Web API](Web-API_21012259.html)

### Non-Functional

#### Security

- [Support configurable crypto algorithms](https://soramitsucoltd.aha.io/features/HI2-42)
- [Support for server-side HSM integration](https://soramitsucoltd.aha.io/features/HI2-22)
- [Security and consistency improvements](https://soramitsucoltd.aha.io/features/HI2-44)
- [Encapsulation of crypto-related functionality](Encapsulation-of-crypto-related-functionality_21016068.html)
- Transport Layer Security Configuration

#### Maintenance

- [Logging](Logging_21012113.html)

#### Target Platforms

Iroha deployment should support GNU/Linux, macOS and Windows machines with x86 and Arm64 CPUs.

#### Transactions Processing

Iroha Peer should be able to process 20,000 transactions per second.

#### Blocks Processing

Iroha should be able to commit a new block every 3 seconds.

### Development related

#### Benchmarks

- [Transaction performance benchmarking framework](https://soramitsucoltd.aha.io/features/HI2-21)
- [Memory usage benchmarking framework](https://soramitsucoltd.aha.io/features/HI2-20)

#### Maintenance

- [Logging](Logging_21012113.html) - 
  
  Error rendering macro 'jira' : null
- Service Discovery

#### Continuous Delivery

- Docker images publish
- Binary and documentation publish

#### Longevity Stand

- [HI2-41](https://soramitsucoltd.aha.io/features/HI2-41)

#### Distributed testing

- 10 servers, each on a different machine and in different geographies.
- Run data through them for several minutes to really get some meaningful data.
- Here is what each peer should do:
  
  - sync with peers about the latest blocks
  
  - gossip about (forward) transactions that are pending that they have
  
  - propose or vote on a block (as part of consensus)
  
  - ping and verify peers as part of the Hijiri reputation system (basically something like eigentrust++)
  
  - share time information as part of a p2p network time service

## User interaction and design

![](http://wiki.hyperledger.org/plugins/servlet/confluence/placeholder/unknown-attachment?locale=en_US&version=2)

## Questions

Below is a list of questions to be addressed as a result of this requirements document:

QuestionOutcome

## Not Doing

- Genesis Block

## Attachments:

![](images/icons/bullet_blue.gif) [Iroha.gif](attachments/21012123/21016038.gif) (image/gif)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
