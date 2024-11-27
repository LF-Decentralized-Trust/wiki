1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Product requirements](Product-requirements_21016037.html)
5. [Needs and Requirements](Needs-and-Requirements_21012123.html)

# Hyperledger Iroha : Requirements from leads and community

Created by Vadim Reutskiy, last modified by Zilya Yagafarova on Sep 03, 2020

Initial authors:

- [Sara Garifullina](https://lf-hyperledger.atlassian.net/wiki/people/5b6c115b2c9bd83c03707f95?ref=confluence)
- [Zilya Yagafarova](https://lf-hyperledger.atlassian.net/wiki/people/5a77f08162323e24eaf7d41f?ref=confluence)

\#

Title of the change

Description

Comments from Iroha team

Author (if known)

1

Group account

What is a group account:

This is a UNIX-like function, but the account belongs to a group. Enables you to perform authorization management by permissions and roles on a group basis. This feature makes role-based or department-based authorization management easy and explicit.

In addition, I think that more detailed authorization management will be possible if signatures can be shared by groups.

Especially for customizable queries, I think that implementation with enhanced security is essential. (Easy to contain vulnerabilities)

Can be made as a group for accounts in which they can share permissions. That can be made through roles.

The thing with signatures might be implemented through MST or a group account? 

Need technical details.

Takeshi Yonezu

2

Assets of Things

Non-fungible tokens? 

3

Data model based smart contract

Burrow wrap can already do that it seems. 

4

API function names

API function names have become many API names on a name basis, but I think it would be nice to be able to organize them on an attribute basis. In particular, APIs for queries are applicable.

More specifically, GetTransactions, GetAccountTransactions, and GetAccountAssetTransactions are all variants of GetTransactions, and differ only in what they do to restrict the acquisition. Therefore, it would be nice to be able to search for transactions with GetTransactions and specify accounts and assets as attributes. For assets, you can specify Any. For the account, the default value is "My", but if you have permission, you can specify the domain or "All". This sort of organization will make it easier to use and less likely to introduce bugs during implementation. In addition, GetPendingTransactions should be integrated with GetTransactions so that the "Pending" state can be specified.

Similarly, if attribute-based permissions can be realized, business usage will be further promoted. Currently, it is very good that the query API can be managed with "All", "Domain", and "My". If this becomes available on an attribute basis, for example, "Domin", it will be possible to specify in which domain the operating authority is to be set. Some systems may need to be implemented off-chain at this time due to lack of implementation.

Also, in the permissions of GetTransactions, there are can\_get\_my\_txs and can\_get\_all\_txs, but do you know why there is no can\_get\_domain\_txs?

Might be implemented with Smart Contracts or do this in 2.0 with a better API

5

gRPC Errors

At present, it would be nice to be able to deal with errors that may occur depending on conditions during the initial connection of gRPC.

What is on the client-side? What library it is?

6

Name resolution service

Apart from Iroha itself, I also consider the need to define and implement a name resolution service for intercommunication between blockchains to implement DID. (I think this will also be a patent case)

7

Attribute-based peers

(with or without consensus building)

See Kamil’s idea

8

Subdomains

It is imperative for subdomain implementations to define the inherited attributes and restrictions.

See inherited roles by Bogdan M.

9

Define Iroha queries, commands and business validation rules in runtime/VM

Now if one wants to change business logic, for example, by introducing a new command they need :

1. Fork Iroha and make changes in source code
2. Stop current Iroha peers
3. Update binaries and
4. Re-launch network again

Instead, if we keep this logic as a runtime blob stored in Iroha state, then updating business logic will only require to execute transaction containing new runtime blob. The same approach is used in Substrate now. 

Pros:

1. Less deployment effort to business logic update
2. Backward compatibility (we can keep old runtime in case we receive an older version of the transaction)
3. Arbitrary format of transaction: runtime can process transactions of arbitrary format if it contains such logic

Cons:

1. A small decrease in performance, due to running VM code instead of the native one
2. Fewer security guarantees, as business logic rules now are the responsibility of users of Iroha rather than the responsibility of developers of Iroha

Cons 2 can be mitigated by providing Iroha clients with Runtime containing default business logic. 

Pros 3 can only be achieved as part Iroha 2.0

Other required changes are possible to introduce in Iroha 1.0 without breaking backward compatibility

I can help to introduce that in Iroha

Burrow might be able to solve that if we rework it to allow adding-on other VMs 

Burrow atm is only an addition to our current data model but its features can be extended to replace the current model

[Kamil Salakhiev](https://lf-hyperledger.atlassian.net/wiki/people/557058:07723e0b-a027-4cc4-ad6d-324e41cccb4d?ref=confluence)

10

Introduce chain-based consensus

The current consensus in Iroha finalises every block it is creating. Therefore block production and block finalisation are sequential processes, whereas they can be executed in parallel

Now Iroha team is putting big efforts to create fast BFT consensus, to improve latency of transactions. However, by introducing parallel block production we can combine fast latency with high throughput. Please note that any BFT consensus (even YAC) can be used for finalisation. The process is the following:

Blocks are broadcasted as soon as they are created and in parallel with the finalisation

When new finalisation round starts consensus finalises the most recent block

When the block is finalised all blocks preceding finalised one is also considered a finalised

Polkadots Babe/Grandpa consensus is one of the examples where such mechanism is used

Andrei: this might not be about the consensus being chain-based or not. 

Need technical details, will talk to Kamil’.

11

Syncing and light client nodes

At the moment all peers in Iroha are homogeneous, thus every node participates in consensus, creates blocks and etc.

However, in many use cases, there is only a need to have syncing node, which does not participate in consensus, does not create blocks, but rather only synchronizes its state with blockchain it is connected to. 

The system can benefit from such an approach as there will be more nodes that can be queried to get the state without increasing networking overhead required for consensus.

At the same time, light clients can be introduced. They would allow avoiding storing entire history in blocks and only keep light-weighted block headers. Thus, in order to check the consistency of light-client node, it will only need to calculate the Merkle root of its state and compare it with Merkle root in the last block header

Artem G. Suggested dividing the types of nodes. 

Seems like a good idea, need to talk to Artem about his idea of how he thought to implement this

12

Retrieving different types of transactions

If we talking about payment network, then there is an existing issue with Transaction History. Ideally, clients should be able to retrieve their transaction history from the blockchain. Each payment transaction should have a status (basic set is PENDING, SUCCESS, FAILED). For now, clients can retrieve only SUCCESS outgoing transactions from the Iroha, so that PENDING and FAILED would be lost and cannot be tracked with all information required (from, to, amount, description and so on). Also, for retrieving incoming transactions you have to listen to the blockstore since you can retrieve a list of them by the query to your account, and querying every account in Iroha to retrieve transactions which belong to you is certainly a painful way. It is understandable why we are not storing in Iroha all of them — because otherwise, clients would be able to spam blockchain with garbage-like FAILED transactions. But we still should come up with a better solution for that. Currently, in Bakong and Sora, we handled this using storage for transaction history on the middleware, but the implementation of it is complicated and it's kinda demotivating developers when they had to write such code.

This and many other problems would be mitigated if we will have smart-contracts in addition to our commands in Iroha, so that developers will be able to choose — to use predefined secured commands to communicate with the blockchain, or they will have opportunity to write their own custom logic on the blockchain.

In our Burrow wrapper, EngineCall results can be pulled out.

Need to see results of Igor’s burrow’s GetEngineResponse work 

Anton Khvorov

13

Join the network by token

currently add peer process is not convenient, You have to create the node, then connect to the network from different node with a different account and copy public key and all info about the new node to run command AddPeer. And then the network will connect to a new peer. 

In most distributed systems nodes have the ability to connect and leave the network by their own decision. 

On of solution is to issue the token. The current network can issue token to one or multiple uses. We will just specify this token and node will connect to the network and provide his public key.

Sounds NEZAKONNO (illegal) in Iroha context

Bulat Saifullin

14

Introduce pending transaction streaming

An ability to subscribe to a peer's MST state changes would boost services that are listening to pending transaction performance.

Sounds good. Should not be very difficult to implement. 

Bogdan Mingela

15

Introduce more domain\*, my* permissions to have the permission more flexible

Sometimes requirements such as having only inter-domain transfer would be really good to be implemented on Iroha side

Can be solved by Smart Contracts without expanding API for everything

16

Rework Iroha permissions model to inherit other permissions

Example:

can\_get\_all\_signatories, can\_get\_domain\_signatories and can\_get\_my\_signatories are treated like completely different permissions. 

Hence we have to assign all of the permissions to an account that is used to create other accounts with less privileged permissions. It would be much more convenient if can\_get\_all\_signatories was enough to create an account with a role having just can\_get\_domain\_signatories or can\_get\_my\_signatories

Sounds legit but cannot yet be done - will be breaking. 

Will be postponed will 2.0

17

Field description for command and transaction with around 500 letter size

Implemented in [https://github.com/hyperledger/iroha/pull/133](https://github.com/hyperledger/iroha/pull/133)

[Yuriy Vinogradov](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b85dbf9-2cc9-4bee-a3a0-2815e5bb51eb?ref=confluence)

18

IOU tokens

[https://lf-hyperledger.atlassian.net/wiki/display/iroha/Personal+Domains](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Personal+Domains)

Good idea

John from the community

19

GUI

Please, make GUI modules for next Iroha.

I meant we need such "user-friendly" GUI developments,

for servers side as well as clients side. Both backend and frontend with intuitive GUI will be very nice.

Iroha helpers can help with that? 

Indra K. Hartono

20

BFT consensus

Maksim Skorikov

21

Integrate libp2p

[Kamil Salakhiev](https://lf-hyperledger.atlassian.net/wiki/people/557058:07723e0b-a027-4cc4-ad6d-324e41cccb4d?ref=confluence)

22

Create parachain for Polkadot

[Kamil Salakhiev](https://lf-hyperledger.atlassian.net/wiki/people/557058:07723e0b-a027-4cc4-ad6d-324e41cccb4d?ref=confluence)

23

Interoperability Between Blockchains

24

Extend the role model for Iroha

In some of our projects, especially Byacco, we already facing a situation when extended Role model can ease development. We already have a proposal for this update which can be additionally clarified if needed. [https://soramitsu.atlassian.net/wiki/spaces/SL/pages/1086357514/Expand+Iroha+Permission+model](https://soramitsu.atlassian.net/wiki/spaces/SL/pages/1086357514/Expand+Iroha+Permission+model)

[Yuriy Vinogradov](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b85dbf9-2cc9-4bee-a3a0-2815e5bb51eb?ref=confluence)

25

Add events support to Iroha

By the events we mean having an ability to subscribe to a certain event, e.g.: I want to receive a notification when tx will reach TX\_COMMITED state

Maksim Skorikov

26

Valuables abstraction

Along with assets nice to have "valuables" abstraction  
There are different cases to use:  
We can assess valuable things in some asset amounts and trade with them using Iroha.  
This may be tokens for real goods and things in Internet Trading, or booking different time slots for hotels, sports clubs, etc...

Anton Kitov

27

Transaction fee

28

Checking for used genesis block when adding a new node to the network

When adding a new node to the Iroha network, there is no check for the genesis used in the added node. So it may happen that the network uses genesis block "A" and the added node uses genesis block "B". This node will be added correctly into the network, but will not be able to work correctly in the network because of the difference in the blockchain.

[lavrentev@soramitsu.co.jp]()

29

ALL variables (old and new) in a configuration file must have analogical environment variables.

Their names have to be similar as in a configuration file.

Example here: [https://docs.google.com/document/d/1ZsI3DJ6eVN5oPH18eC98EZ9S1PpVOg1qF0-YKOpMQTI/edit](https://docs.google.com/document/d/1ZsI3DJ6eVN5oPH18eC98EZ9S1PpVOg1qF0-YKOpMQTI/edit)

DevOps Team

30

The priority of environment variables

A priority of environment variables has to more than the priority of configuration file variables.

DevOps Team

31

Additional environment variables for storing node keys

We need additional environment variables for storing node keys. It has to be stored as a string.

DevOps Team

32

Old mechanism of storing node keys has to be saved for compatibility

Old mechanism of storing node keys has to be saved for compatibility (like as a path to key files). Old and new parameters have to conflict.

DevOps Team

33

Additional environment variables for storing a genesis block

We need additional environment variables for storing a genesis block. It has to be stored as a string with JSON.

DevOps Team

34

Old mechanism of storing the genesis block has to be saved for compatibility

Old mechanism of storing the genesis block has to be saved for compatibility (as file). We need an additional configuration parameter to set a path to the genesis block file. This parameter has contained a default path for compatibility. These parameters have to conflict with parameters from paragraph 33

DevOps Team

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
