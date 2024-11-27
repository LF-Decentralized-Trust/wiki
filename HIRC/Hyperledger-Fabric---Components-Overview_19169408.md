1. [Hyperledger India Regional Chapter](index.html)
2. [LF Decentralized Trust India Regional Chapter Home](LF-Decentralized-Trust-India-Regional-Chapter-Home_19169282.html)
3. [HIRC - Documents](HIRC---Documents_19169406.html)

# Hyperledger India Regional Chapter : Hyperledger Fabric - Components Overview

Created by Rajesh Krishnan on Nov 26, 2020

# **Key Notes to Understand Hyperledger Fabric effectively**

Source  : [https://blog.knowledgesociety.tech/hyperledge-fabric-key-notes-to-understand/](https://blog.knowledgesociety.tech/hyperledge-fabric-key-notes-to-understand/)

In the past few years, blockchain becomes one of the most popular technologies in the world. As the success of Bitcoin provided by **Nakamoto**, many organizations and companies increase their interest in blockchain for  x reasons like, Security, transparent ledger, consensus and other reasons.

Blockchain can be classified into two types: public and private,  in other terms it's a called permission-less and permission-ed blockchain.   **Hyperledger - Fabric** is one of the permission-ed blockchain platforms and developed by the **Linux foundation** open-source community.

Hyperledger Fabric consists of various major components such as **peer nodes, clients, ordering service, membership, and Chaincode**. Each component has a unique role for different purposes. The transaction flow contains four main phases, **endorsement, ordering, validation and committing**. The beauty and the hard part of the components is customization. You need to customize and configure before the blockchain network start.

As part of customization, Administrators  &amp; Developers must deal with hundreds of parameters around all components to bootstrap their blockchain network. Many of these parameters are correlated with each other for security reasons or efficiency or stability of the network. In other terms, i can say the Fabric functionality designed in such a way to setup.

Let's see how it structured and customize,

## Fabric components :

**1, Node/Fabric network structure  
2, Cryptogen &amp; Configtxgen  
3, Orderer  
4, Peer Node  
5, Channels  
6, MSP - Member Service Provider  
7, Chaincode ( Smartcontract)  
8, State Database  
9, Connection profile  
10, Private data**

1. **Node/Fabric network structure**

![](https://blog.knowledgesociety.tech/content/images/2020/08/image-5.png)

**2. Cryptogen &amp; Configtxgen:**

Fabric provides a tool called cryptogen to generate the required cryptographic materials, these are **x509 certificates** and **signing keys**, for the whole network entities. Cryptogen uses a file, usually named crypto-config.yaml to generate a set of certificates and keys for the organizations, peers, orderers and users. The crypto-config.yaml also contains the basic topology of the network. In fabric, any information should be **signed by the private key** and **verified by the corresponding public key.**

![](https://blog.knowledgesociety.tech/content/images/2020/08/image-6.png)

Configtxgen consumes a file named configtx.yaml. Configtx.yaml specifies the definitions of the target network. The definitions contain organizations, peers, policies, ACLs, capabilities, and other structure configurations.Configtxgen tool is used to generate the following necessary initial configuration materials.

1) **Genesis block,**   is the ***first block*** or ***block zero*** in any blockchain-based system, It is the prototype of all other blocks in the blockchain network. Based on this which additional blocks are added to form a **chain of blocks**, hence we call them blockchain. In theory, there is no real need for a Genesis Block. However, it is necessary to have a starting point that everyone can trust.

Without Genesis Block, it would be really difficult for the participant to trust a blockchain and to know how and when it started.

Technically it means that the Genesis Block has its “previous hash” value set to **0**. Which means that no data was processed before the Genesis Block. All other blocks will have sequential numbers starting by **1**, and will have a “previous hash” set to the hash of the previous block.

It’s a configuration block that initializes the ordering service and the original network structure.  

2) **Channel configuration** transaction This transaction will be broadcast to the ordering service after network startup for the channel creation operations. It defines and determines channels for this network.

3) **Anchor peer transactions,** these transactions will specify anchor peers for each organization on this channel one by one. Anchor peers are used by gossip to make peers in different organizations know about each other. There must be at least one anchor peer exist in one channel, and it’s recommended that there should be a set of anchor peers in every organizations for crash fault-tolerant and high performance.  

**3.  Orderer:**  The ordering service implements the consensus protocol to order the transactions, will sort the transactions submitted by members(clients) using consensus methods in the fabric. Hyperledger recommends three consensus methods as Solo (dev), kafka, Raft and implements as per the configuration. Orderer uses an Atomic broadcast protocol to receive data instructions.

![](https://blog.knowledgesociety.tech/content/images/2020/08/image-25.png)

&gt;***Solo :*** Recommended for Development environment only as it doesn't have fault-tolerant system.(expected to deprecate in version 2.+)

**&gt;**Kafaka** :** Its is implemented on several nodes outside of the orderer nodes.

***&gt;RAft** :* [Raft](https://raft.github.io/raft.pdf) (Reliable, Replicated, Redundant, And Fault-Tolerant ) is a crash fault-tolerant ordering service based on the Raft protocol in [etcd.](https://etcd.io/) The main difference from Kafka is that, everything is embedded in the orderer nodes.  Fabric provides several configuration parameters such as block timeout and block size in ordering service for the customized purposes.

**4.  Peer : It's** a one of the main fundamental element comprised primarily a set of *peer nodes in* HLF network. It is a kind of node that hosts the ledger and chain code in the Hyperledger Fabric System. Peers are connected by channels each other and can be grouped as per the needs to manage the ledgers and contracts.

![](https://blog.knowledgesociety.tech/content/images/2020/08/image-27.png)

 Peers can be grouped by the organization and contributed to the network. Peer plays two major roles in the network, Endorsement &amp; Committing to the ledger.  The peer can hold more than one ledgers, which can be governed by one or more chaincodes.

**5.  Channels :**  Hyperledger Fabric channel is a private “subnet” of communication between two or more specific network members, for the purpose of conducting private and confidential transactions. A channel is defined by members (organizations), the shared ledger, chaincode application and the ordering node.

![](https://blog.knowledgesociety.tech/content/images/2020/08/image-28.png)

The peer that joins a channel, has its own identity given by a membership services provider (MSP), which authenticates each peer to its channel peers and services.

**6.  MSP  \[Membership Service Provider ]**

Membership Service Provider (MSP)  : Any of the components in Fabric has an identity &amp; according to the identity, the exact permissions and role of the component are decided. MSP is the entity that defines rules, permissions and roles of different components in the Fabric network and manages the identities of all participants in this blockchain network. The identities of participants are implemented by **Certificate Authority** (CA) ,  Public Key Infrastructure (PKI). MSP abstracts all cryptographic operations such as issuing and validating the certificates. Developers can use MSP to define their required identities related with the organizations, peers, ordering service and users or applications. All the nodes, users and clients use digital certificates to verify each other and communicate with each other.

**7.  Chaincode : ( Smart-contract)**

Enterprise specific chaincode is what most people call smart contracts.Chaincode is deployed over channels.

Chaincode is packaged for deployment on the  Hyperledger Fabric blockchain network. Chaincode is one of the key components and there are 2 types of chaincode, a **general chaincode** provided by a developer or user and a **system chaincode** hosted by Fabric framework to communicate. As a blockchain system, a Chaincode defines a series of executable business logic that are stored in the ledger. Fabric uses a general-purpose programming language called as chaincode to fulfill the business logic and access the ledger data.  It encapsulates both the asset definitions and the business logic (or transactions) for modifying those assets.

The business logic inside the chaincode governs all the transactions.

![](https://blog.knowledgesociety.tech/content/images/2020/06/image-8.png)

**8.  State database**

The peer state database are LevelDB and CouchDB and officially supported in Fabric. **LevelDB** is embedded into the peer node and its default key-value state database embedded in the peer process. LevelDB is the default state database in the official document of Fabric. **CouchDB** is another optional state database that can support rich data query function when the chaincode data is constructed as JSON format. Compared to LevelDB,  t**he shortcoming is that the CouchDB has lower efficiency on data processing.**

![](https://blog.knowledgesociety.tech/content/images/2020/08/image-29.png)

A chaincode persists a set of data which called world state that contains all current state values of objects. All world state data are organized as key-value pairs. Chain codes can use put, get and delete operations to interact with world states. The latest values of all keys in chaincodes are stored in a state database.

**9.  Connection Profile**

A connection profile is primarily used by an application to configure a [gateway](https://hyperledger-fabric.readthedocs.io/en/release-2.2/developapps/gateway.html) that handles all network interactions, allowing it to focus on business logic. A connection profile is normally created by an administrator who understands the network topology. The connection profile contains a description of a network view, expressed in a technical syntax, which can either be JSON or YAML

![](https://blog.knowledgesociety.tech/content/images/2020/08/image-7.png)

**10. Private data**

Private Data Collection is the feature, where the **data** considered private and can be shared with only authorized organizations whereas the public **data** can be shared with all organizations on a channel, without the need to create a separate channel.

Document generated by Confluence on Nov 26, 2024 16:42

[Atlassian](http://www.atlassian.com/)
