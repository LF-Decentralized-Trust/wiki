1. [Hyperledger Fabric](index.html)
2. [Archives](Archives_22840389.html)
3. [Quality Assurance: Tests, Strategy, Reports](22839728.html)

# Hyperledger Fabric : Hyperledger Fabric v1.0 Alpha Release Testing

Created by Tracy Kuhrt, last modified on Jan 04, 2019

This document describes the testing completed on the v1.0.0-alpha tag in the [Hyperledger Fabric](https://github.com/hyperledger/fabric/ "https://github.com/hyperledger/fabric/") repo. The document is a work-in-progress and will continue to be enhanced.

## Environment

The following environment was used for testing:

### Network

4 Peers (which include Endorser and Committer roles) and 1 membership services (fabric-ca only) with ordering service running different orchestrations. There are two organizations, each containing two peers.

1. In scenario one, SOLO was tested.
2. In scenario two, a Crash Fault Tolerant (CFT) consensus algorithm was tested:

<!--THE END-->

- Kafka with 2 Kafka brokers and a ZooKeeper
- Consensus up to 100 channels
- Up to 10 chaincodes per channel

#### OS/Hardware

- Peers and Ordering Service with membership services nodes running as Docker containers defined in the Hyperledger Fabric environment. The PC used was a Lenovo W540 with Intel(R) Core™ i7-4800MQ CPU@2.70GHz 2.70GHz with 16GB RAM and 475GB disk space.
- Peers and Ordering Service with membership services nodes running as LinuxONE guests running in a Secure Service Container environment were also validated with the HSBN vNext Beta environment.

**Note:** Docker images are available for easy deployment of Hyperledger Fabric v1.0. Docker images will be available for all major components to run a network (peers, orderer, Kafka, ZooKeeper, CouchDB). A “Getting Started” section is available in the documentation. The end-to-end flow will help anyone easily start the network, run a simple application, and learn the basics of running Fabric v1.0.

## Test/Scenario Execution

The following test scenarios were executed:

### Basic Chaincode Functions

Chaincode interfaces were exercised to ensure that transactions work properly. There are two interfaces–init and invoke–which the chaincode developer must code. The remaining interfaces are implemented in the Fabric and are considered chaincode APIs.

1. The following APIs were tested using marbles02, chaincode\_example02, chaincodeAPIDriver(marbles02+other API):
   
   - GetState, PutState, DelState
   - GetStateByRange (picks up extra results)
   - CreateCompositeKey, GetStateByPartialCompositeKey, SplitCompositeKey, - Read keys that start with a common prefix. For example, for a chaincode key that is composed of K1-K2-K3 (composite key), ability to query on K1 or K1-K2 (performs range query under the covers). Replacement for v0.6 GetRows() table API.
   - GetQueryResult(Rich queries against ledger data content - CouchDB only)
   - GetArgsSlice, GetCreator, GetBinding
2. API tested on ‘qscc’ (query system chaincode):
   
   - GetChainInfo, GetBlockByNumber, GetTransactionByID - though output is a binary structure and therefore requires SDK to parse

### Ledger

The following ledger tests were run:

1. Tested ledger with the following load:
   
   - 20 million keys
   - 100 transactions per block
   - 200,000 blocks
   - Spread across 10 channels
2. Tested both serial and concurrent transaction execution.
3. Tested all chaincode functions against state databases:
   
   - LevelDB using range and composite key queries
   - CouchDB using range, composite key queries, and rich queries against data content
4. Values in Ledger History index verified using GetHistoryForKey chaincode API.

These tests were performed using CLI commands on marbles02, chaincodeAPIDriver chaincode (ccAPIDriver.sh) on docker-compose, 1 Orderer, 2 Kafka Brokers, 4 peer setup, one/multiple channels and one/multiple chaincodes installed on all peers.

Transactions invoked on ledger were tested for data accuracy on state database using chaincode\_example02 in scalability tests mentioned below.

### Scalability

Scalability testing ensured that the network can handle serialized flows while increasing the number of channels and chaincode applications. The flow for each channel and chaincode application is:

1. Each peer joins the channel
2. Chaincode applications installed on each peer.
3. Chaincode applications instantiated on each channel. Copies of chaincode example02 were used and given unique names.
4. Create a loop that does an invoke and query on each chaincode on every channel on every peer.

Number of ChannelsNumber of Chaincode Applications114410102510501010010

The ability to add a peer was also verified. This was done by starting with three peers, running several transactions, and then adding a peer in a different organization (already defined within the genesis block) and ensuring it could synchronize its ledger with the running peers.

### Negative Flows

Negative flows were executed to confirm that we see rejections when we expect them.

1. Expected failures due to Endorsement/Validation Policy being violated:
   
   - Using the Boolean Operators (AND/OR) with multiple peers. The transaction was rejected when using policy AND (Org0.member,Org1.member) in the validation phase when only one endorsement is provided. The transaction was successful with using the OR operator.
2. Expected failures due to state validation check:
   
   - Peers perform a versioning check against the transaction read set, to ensure data integrity and protect against threats such as double-spending. The fabric has concurrency control whereby transactions are executed in parallel (by endorsers) to increase throughput, and upon commit (by all peers) each transaction is verified to ensure that no other transaction has modified data it has read. In other words, it ensures that the data that was read during chaincode execution has not changed since execution (endorsement) time, and therefore the execution results are still valid and can be committed to the ledger state database. If the data that was read has been changed by another transaction, then the transaction in the block is marked as invalid and is not applied to the ledger state database. The client application is alerted, and can handle the error or retry as appropriate.
   - Using chaincode\_example02, multiple concurrent transactions were invoked that modified the current state data of the same key. The client tool had counters that kept track of how many invokes succeeded and how many failed. The test verified that only one Tx per chaincode was written to the ledger for a specific version of the current state key/value pair.
3. Expected failures due to non-deterministic chaincode. Non-deterministic chaincode will destroy the blockchain as it leads to variances on the ledger.
   
   - Chaincode that calculated a PutState of a key value pair based on timestamps were attempted to be stored on the ledger. Two peers were used and the non-determinism of the timestamp resulted in expected failures due to different Proposal Responses.

### Concurrency

The v1.0 architecture is designed for concurrency by eliminating serialization and allowing transactions to run in parallel. The concurrency testing will continue to evolve and below describes the current testing:

1. Basic controlled test to ensure two valid unique concurrent transaction proposals are accepted: On same channel and chaincode and peer, we sent two concurrent transactions that were ordered within batch timeout threshold of 10s, ensuring they were batched together and delivered in same block, and thus were based on the same read-state hash. We verified both were accepted and written to the ledger.
2. Controlled test for more dimensions of concurrency: We generated multiple transaction proposals on multiple chaincodes, peers and channels. For example, we sent 4 transactions, on 4 different chaincodes on 4 peers, all duplicated on 4 channels. Thus, there is a concurrency of 64 in-flight transactions. The configuration had a batchtimeout (10s) and a batchsize &gt;= 64 (enough to handle all transactions on each channel). We verified they were all successfully delivered and written to the ledger. The picture below shows the flow on a single peer. The four peers share the same channels and chaincodes. The architecture allows for the same chaincode to exist on separate ledgers.

[![](https://wiki.hyperledger.org/_media/projects/fabric/channel_diagram.png)](https://wiki.hyperledger.org/_detail/projects/fabric/channel_diagram.png?id=projects%3Afabric%3Aalpha_release_testing "projects:fabric:channel_diagram.png")

### Multiple membership, using the provided Fabric-ca

Membership services authenticates, authorizes, and manages identities for a permissioned blockchain network have been tested. Membership services code runs in peers and orderers and both authenticates and authorizes blockchain operations utilizing a PKI-based implementation. Fabric-ca has been tested for membership services, handling the issuance of enrollment certificates (enrollment certificate is a long term identity credential).

1. Used the Fabric-ca to register and enroll 1000 users.

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
