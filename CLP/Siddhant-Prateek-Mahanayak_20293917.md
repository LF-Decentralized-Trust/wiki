1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)
4. [BiniBFT - An Optimized BFT on Fabric](BiniBFT---An-Optimized-BFT-on-Fabric_20283476.html)
5. [Project Plan - BiniBFT](Project-Plan---BiniBFT_20283487.html)
6. [Evaluation Reports](Evaluation-Reports_20293727.html)
7. [Evaluation 2](Evaluation-2_20293857.html)

# Collaborative Learning Program : Siddhant-Prateek-Mahanayak

Created by Siddhant Prateek on Dec 15, 2023

# [BiniBFT - An Optimized BFT on Fabric](https://lf-hyperledger.atlassian.net/wiki/display/CLP/BiniBFT+-+An+Optimized+BFT+on+Fabric)

# **Evaluation 2 - Report**

## Submitted By: Siddhant Prateek Mahanayak

# Collaborative Learning Program

## Engagement Details

**Name of Mentee**

**Siddhant Prateek Mahanayak**

**Evaluation Period**

**19-08-2023 to 06-10-2023**

**Task**

**Comparative study of BFT Protocols**

**Date Submitted**

**07-11-2023**

**Mentor**

**Dr. Anasuya Threse Innocent**

### Byzantine Fault Tolerance (BFT)

In a Byzantine Fault Tolerance (BFT) scenario, there are `n = 3t + 1` participants, and the goal is to ensure that all participants agree on the same bit, even when there are at most t traitorous participants. This **consensus can be achieved when all participants have direct communication channels with each other**. However, if the network is not a complete graph, meaning that not all participants have direct communication channels with each other, achieving consensus becomes more challenging. Incomplete network connectivity can lead to difficulties in ensuring that all participants reach an agreement on the bit value.

### Hyperledger Ordering Service

Hyperledger Fabric employs an orderer node that handles transaction ordering, forming an ordering service when combined with other orderer nodes. This ordering service is critical in maintaining ledger consistency across all peers in the network.

## **Role of Orderers in a Transaction Flow**

Orderers play a central role in the transaction flow of a blockchain network, particularly in Hyperledger Fabric. Their responsibilities include:

1. **Packaging Proposed Ledger Updates:** Orderers receive proposed ledger updates from various applications. They organize these updates into well-defined sequences, creating batches that will later become blocks in the blockchain.
2. **Distributing Blocks to Peers:** Once the blocks are formed, orderers distribute them to the network's peers. This ensures that all participants in the network receive the same blocks, maintaining ledger consistency.

The transaction flow in a Hyperledger Fabric network typically involves three phases:

- **Proposal Phase:** Applications propose ledger updates.
- **Ordering Phase:** Orderers package and arrange the transactions into blocks.
- **Validation and Commit Phase:** Peers validate and commit the transactions from the received blocks to their ledgers.

Ordering service nodes collaborate to create the ordering service, which is essential for ensuring that all participants in the network maintain consistent and synchronized ledgers.

### Raft

Raft is a consensus algorithm designed for simplicity while providing fault tolerance and performance equivalent to Paxos. It decomposes the consensus problem into three sub-problems: **leader elections, log replication**, and **ensuring safety.**

### Paxos

Paxos is an algorithm used for achieving consensus in a distributed system, particularly when **nodes communicate via an asynchronous network**. It can be complex and is known for its **multiple rounds of communication.**

### Raft vs. Paxos

The main difference between Raft and Paxos is that Raft decomposes the consensus problem into more manageable sub-problems, making it easier to understand and implement. This includes leader elections, log replication, and ensuring safety.

### Leader Election in Raft

Raft nodes can be in one of three states: follower, candidate, or leader. Initially, all nodes start as followers. If they don't receive messages for a certain time, they become candidates and request votes from other nodes. If they secure a majority of votes, they become leaders and are responsible for accepting and replicating new log entries.

### Adding a New Node to a Raft Cluster

To add a new node to a Raft cluster, several steps are involved. These include configuring TLS certificates, fetching the latest system channel configuration block, ensuring the node's presence in the system channel, starting the new node, and updating the channel configuration for all relevant channels.

### Requirements and Drawbacks of Raft

Raft requires a majority of nodes to be accessible and sufficient disk space and persistence for log and configuration data. Its single leader design simplifies consensus but may introduce latency and resource usage issues.

### Requirements and Drawbacks of Paxos

Paxos requires more than half of the nodes to function correctly, reasonably synchronized clocks, and can be slow in certain cases, particularly during network partitions. It may also involve multiple rounds of communication, have a single leader, and face challenges when changing the cluster membership.

### Mir-BFT

Mir-BFT is a consensus protocol designed for use in distributed systems, particularly in the context of blockchain technology. It aims to address several challenges commonly faced by such systems. Below, I'll provide an explanation of Mir-BFT's key features and principles:

**Inherent Problems:**

- **Higher Energy Consumption:** Mir-BFT acknowledges the high energy consumption of traditional Proof-of-Work (PoW) blockchain networks, such as Bitcoin, which can be compared to the energy consumption of entire countries like Switzerland and Austria.
- **No-Finality:** In Mir-BFT, there is no finality, meaning that when two nodes solve the PoW puzzle at roughly the same time, forks can occur. This leads to temporary inconsistencies in the blockchain.
- **Low Throughput:** The protocol has low throughput, supporting only 7 transactions per second (tps), which is significantly lower than what is required for many real-world applications.
- **High Latency:** The high latency of 10 minutes to 1 hour can be problematic, especially when quick transaction confirmation is needed.

**Mir-BFT's Purpose:**

- Mir-BFT is designed as a robust Byzantine Fault Tolerant (BFT) total order (consensus) protocol. It is specifically tailored for Wide Area Networks (WANs) and can accommodate a large number of nodes, potentially more than 100.

**Suitable Use Cases:**

- Mir-BFT is suitable for both Permissioned Blockchains (e.g., Hyperledger Fabric) and Permissionless Blockchains that rely on Proof-of-Stake (PoS) consensus mechanisms.

**BFT Problem Statement and Model:**

- **Mir-BFT deals with networks consisting of N nodes**, where **F of them may be Byzantine faulty**, meaning **they can deviate from the protocol or act maliciously**.
- **N must be greater than or equal to 3F+1 for robustness**.
- The **network is assumed to be asynchronous**, but eventually, it becomes synchronous after some time GST (Global Stabilization Time).
- The main problem tackled by Mir-BFT is achieving total order broadcast, which involves 
  
  - agreement,
  - validity,
  - no-duplication, and liveness.

**Robust BFT:**

- Mir-BFT introduces the concept of "Robust BFT," which focuses on sustaining the performance of a BFT protocol despite active attacks. This concept was introduced by the Aardvark protocol, which highlighted the pitfalls of fragile optimizations.
- The protocol addresses issues like client request dissemination and client authentication.

**Mir BFT Total Order Broadcast Protocol: Main Principles:**

- It **employs multiple leaders to propose requests in parallel**, in contrast to PBFT (Practical Byzantine Fault Tolerance), which typically has a single leader.
- To **prevent request duplication**, Mir-BFT uses **rotating assignment of partitioned hash space.**
- The protocol is built on the foundation of PBFT and Aardvark, making it easier to reason about correctness.

**Optimizations:**

- Mir-BFT includes optimizations like Light Total Order (LTO) broadcast, signature sharing, and parallelized networking and implementation, which enhance performance and efficiency.

**Preventing Transaction Duplication: Bucket Rotation:**

- Transactions are partitioned into "buckets" using a collision-free hash function, ensuring that each transaction is mapped to a unique bucket.
- Each leader is responsible for proposing transactions from an active bucket.
- The assignment of the active bucket rotates within a stable epoch and across recovery epochs.

**Growing and Shrinking Leader Set:**

- The protocol defines stable and recovery epochs to accommodate changes in the leader set.
- The number of leaders in the stable epoch must be greater than or equal to "m," and the duration of the epoch is unbounded.
- In case of faults or partitions, a recovery epoch is initiated, which is limited in duration.
- Epoch changes can be gracious or ungracious depending on network conditions.

**Mir-BFT Summary:**

- Mir-BFT offers high scalability, particularly in WANs with a large number of nodes, potentially exceeding 100 nodes.
- It demonstrates superior performance on WANs compared to existing protocols.
- The protocol is robust against performance attacks, making it a promising option for distributed systems and blockchain networks.

In summary, Mir-BFT is a BFT consensus protocol with a focus on robustness, scalability, and efficiency, making it suitable for a range of blockchain applications, particularly in the context of WANs with a high number of nodes.

### Drawbacks of Mir-BFT

Mir-BFT demands redundancy to ensure robustness and can be resource-intensive due to high message volumes and cryptographic operations. It generates substantial network traffic, which may impact system performance. Achieving consensus can introduce additional latency, especially with many faulty nodes or cryptographic operations.

### BDLS

BDLS, which stands for Byzantine Diamond-Leader Selection, is a protocol used in distributed systems to achieve consensus among participants in the presence of Byzantine faults. Byzantine faults refer to participants who may behave arbitrarily, including acting maliciously, and the consensus protocol must be designed to tolerate their actions.

In the context of BDLS, there are **several participants, denoted as P1, P2, ..., Pn**, where each participant has a **role in reaching a consensus on a candidate block**. Here's an explanation of the key elements and steps in the protocol:

ProtocolStepCommunicationPBFT1Leader broadcasts message to all participants  
2All Participants send authentication messages  
3All Participants broadcasts commit messageTendermint BFT1Leader broadcasts message to all participants  
2Pre-vote phase: validators vote on whether to accept the block  
3Pre-commit phase: validators vote on whether to commit the block  
4Commit phase: validators commit the block to the blockchainLibraBFT1Hotstuff: leader proposes block to validators  
2Pacemaker: validators vote on whether to accept the block  
3Timeout: if leader does not receive enough votes, a new leader is elected  
4Synchronisation: validators synchronise their views of the blockchain  
5Leader broadcasts message to all participants  
6Participants send messages to leader  
7Leader broadcasts commit message to all participantsBDLS1Participants send messages to leader  
2Leader broadcasts message to all participants  
3Participants send messages to each other to synchronize their views of the blockchain  
4Leader broadcasts commit message to all participants

![](https://siddhantprateek.notion.site/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F2070ac55-c276-4173-9277-81be741fea48%2Ff2da562d-1c23-4adb-869e-ee07d464a432%2FScreenshot_2023-11-07_at_10.16.27_AM.png?table=block&id=d86696bf-95b8-4670-9e8b-493a4ca8704d&spaceId=2070ac55-c276-4173-9277-81be741fea48&width=2000&userId=&cache=v2)

1. **Round-Change Message**: Each participant Pj, including Pi (the leader), sends a signed message ((h, r);, (h, r, Bj)) to the leader Pi. This message is considered a "round-change message." Let's break down the components of this message:
   
   - `(h, r)` represents the **height (h) and round (r) of the consensus process.** These parameters help track the progress of the consensus protocol.
   - `(h, r, Bj)` signifies that **participant Pj is suggesting a candidate block Bj for the current round (r).** In a Byzantine fault-tolerant consensus, participants propose candidate blocks, and the **protocol aims to agree on a single block among the proposed candidates.**
2. **Maximal Acceptable Candidate Block**: The participant Pj specifies a "maximal acceptable candidate block" Bj. This means that, among the proposed blocks, Pj is willing to accept any block that is not better than Bj. It's a way of setting a standard for the quality of candidate blocks in the current round.
3. **Round-Change Constraint**: **After sending the round-change message**, the participant Pi (the **leader**) **imposes a constraint on itself**. It will **not accept any more messages for this round (r)** except for a "decide" message pertaining to a previous round r' where r' &lt; r. In other words, the **leader Pi locks in the round r after sending the round-change message**. This constraint is designed to **prevent further communication and decisions for the current round**, **ensuring that participants proceed to the next round**.

The BDLS protocol is used in distributed systems to reach consensus on a candidate block among a group of participants, even when some participants may act maliciously. Participants communicate by sending round-change messages, and once such a message is sent by the leader, the round is locked, and no more messages for the current round are accepted. This protocol helps ensure that participants converge on a single decision despite adversarial behavior.

## References

[https://github.com/yonggewang/bdls](https://github.com/yonggewang/bdls)

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
