1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)
4. [BiniBFT - An Optimized BFT on Fabric](BiniBFT---An-Optimized-BFT-on-Fabric_20283476.html)
5. [Project Plan - BiniBFT](Project-Plan---BiniBFT_20283487.html)
6. [Evaluation Reports](Evaluation-Reports_20293727.html)
7. [Evaluation 2](Evaluation-2_20293857.html)

# Collaborative Learning Program : Riddhi-Katarki

Created by Riddhi Katarki on Nov 07, 2023

# [BiniBFT - An Optimized BFT on Fabric](https://lf-hyperledger.atlassian.net/wiki/display/CLP/BiniBFT+-+An+Optimized+BFT+on+Fabric)

 

# **Evaluation 2 - Report**

## Submitted By: Riddhi Katarki

 

 

# Collaborative Learning Program

 

## Engagement Details

 

 

**Name of Mentee**

**Riddhi Katarki**

**Evaluation Period**

**12-08-2023 to 07-10-2023**

**Task**

**Comparative Study of BFT Protocols**

**Date Submitted**

**09-10-2023**

**Mentor**

**Dr. Anasuya Threse Innocent**

 

 

 

# Tasks, Objectives, and Results

 

This Evaluation report consolidates the candidate’s work for Hyperledger CLP - BiniBFT project by BiniWorld Innovations Pvt Ltd during the internship (Weeks 1-6). The report has been categorized into two sections: outline the key task assigned to the candidate and day-to-day activities undertaken by the candidate.

### **1.    Key Outline of the Task assigned to the candidate (This includes Project name, Problem statement, expected Output and other relevant details)**

 

Consensus algorithms play a crucial role in distributed systems and blockchain networks to ensure that nodes can agree on a consistent and reliable state of the system. Several major factors contribute to the design and evaluation of consensus algorithms:

1. **Fault Tolerance**: The ability of the consensus algorithm to maintain correctness and agreement among nodes, even when some nodes in the network are faulty or behave maliciously (Byzantine faults). Byzantine Fault Tolerance (BFT) is a key property.
2. **Security**: Consensus algorithms must be designed with robust security measures to prevent attacks, including Sybil attacks, double-spending attacks, and other malicious activities.
3. **Throughput**: The rate at which the consensus algorithm can process transactions or commands. High throughput is essential for scalable systems.
4. **Latency**: The time it takes for a transaction to be agreed upon and added to the blockchain or distributed ledger. Low latency is critical for responsive applications.
5. **Finality**: Whether the consensus algorithm provides deterministic finality, meaning once a decision is made, it cannot be reversed. Some algorithms offer probabilistic finality.
6. **Liveness**: Ensuring that the network makes progress, even in the presence of failures or adversarial behavior.
7. **Censorship Resistance**: The ability to prevent nodes or external entities from censoring or blocking transactions or network participation.

 

## **Mir BFT**

Mir BFT is a Byzantine fault-tolerant consensus algorithm that is designed to provide high throughput and low latency in distributed networks.

**Parallel Leaders**: In Mir, the responsibility of leading the epochs (i.e., rounds) is distributed among multiple leaders, chosen by the primary node. This allows for a more distributed and efficient leadership structure, as opposed to having a single leader in charge. Additionally, the epoch leaders are chosen subject to constraints, ensuring that the protocol is robust and secure. The parallel leader structure in Mir also enables the elimination of duplicates during agreement, improving performance and scalability.

One advantage of Mir BFT is its ability to handle large-scale networks with thousands of nodes. It has been successfully tested in a variety of use cases, including blockchain applications, financial systems, and internet of things (IoT) devices.

Overall, Mir BFT offers a robust and efficient solution for achieving consensus in distributed networks.

## **Zyzzvya**

Zyzzvya is a novel consensus algorithm that takes a unique approach to achieving distributed consensus.

Unlike traditional consensus algorithms that rely on a fixed set of nodes, Zyzzvya allows for dynamic membership. This means that new nodes can join the network and participate in the consensus process without requiring permission from existing nodes. Additionally, Zyzzvya uses a reputation-based system to determine which nodes are trustworthy and should be given more weight in the consensus process.

**Sharding**: Zyzzyva uses sharding to divide the state of a blockchain into multiple parts, which allows for better scalability and efficiency

Another benefit of Zyzzvya is its ability to handle Byzantine faults. In a Byzantine fault, a node may behave maliciously and attempt to disrupt the consensus process. Zyzzvya's reputation-based system helps mitigate the impact of these faults by giving less weight to untrustworthy nodes.

## **Comparison of Consensus Algorithms**

Mir BFT, and Zyzzvya are all consensus algorithms that enable distributed networks to reach agreement on a single state.

PBFT and Mir BFT are both Byzantine fault-tolerant algorithms, meaning they can handle malicious actors in the network. Zyzzvya takes a different approach and uses a reputation-based system to achieve consensus.

One key difference between PBFT and Mir BFT is that PBFT requires a leader node to initiate the consensus process, while Mir BFT does not. Additionally, PBFT requires multiple rounds of message passing, while Mir BFT only needs one round.

Zyzzvya's unique approach allows for faster consensus times and lower energy consumption compared to PBFT and Mir BFT. However, it may be less secure in certain scenarios due to its reliance on reputation rather than fault tolerance.

# **BDLS**

The BDLS protocol operates in rounds, with each round focusing on achieving consensus for a specific height h.

Protocol

- Participants send round-change messages to signal the start of a new round.
- If Pi receives enough round-change messages from participants, they broadcast a lock message for a specific candidate block B0, indicating that B0 is locked by a sufficient number of participants.
- If Pi does not receive enough round-change messages for a specific candidate block, they broadcast a select message for the maximum candidate block B00 from the received candidate blocks.
- If Pi receives enough commit messages for a candidate block, they decide on that block as the finalized block for height h and broadcast a decide message to all participants.

Participants maintain synchronization with height and round numbers during the protocol execution.

Participants set timeout counters to ensure progress, and if they do not receive enough messages within a specific time, they move to the next step or round.

BDLS guarantees the following properties:

- **Safety:**No faulty node can prevent the correct nodes from reaching consensus on a value.
- **Liveness:**The correct nodes will eventually reach consensus on a value, even if some of the nodes are faulty.

**Assumptions**

- **At most 1/3 of the nodes are Byzantine faulty.**
- **Messages are eventually delivered, but there is an unknown upper bound on the message delay.**
- **There is a bound on the number of messages that can be lost or delayed before Global Synchronization Time.**

 

**Unique Features**

- **Checkpointing:**The correct nodes periodically checkpoint their state. This ensures that if some messages are lost or delayed, the correct nodes can still recover their state and continue the protocol.
- **Flooding:**The correct nodes flood messages throughout the network. This ensures that all messages are eventually delivered, even if some nodes are faulty.

## **BDLS - Cons**

- Slower when compared to other protocols.
- Communication Overhead.

Protocol           Time to reach consensus       Tolerance of faulty nodes

BDLS                          Slow                                        High

PBFT                           Fast                                         Low

# **BFT - SMaRt**

- Orderer node: Assembler assembles transactions into blocks
- Peer receives a Header - metadata stream from a randomly selected orderer
- Consensus consists of 3 phases: Pre-prepare, Prepare and Commit
- Client sends transactions to all the nodes in the network

<!--THE END-->

1. **Block Handling**:
   
   - **Raft:** The block is separated before ordering and then given to the Raft library for ordering.
   - **BFT SMaRt**: Transactions are directly submitted to the BFT library. This is because the BFT system actively monitors to prevent transaction censorship.
2. **Trust &amp; Validation**:
   
   - **Raft**: Followers inherently trust the leader's block proposal because the leader can only fail due to crashes (it can't behave maliciously).
   - **BFT - SMaRt**: Followers don't just trust the leader. They revalidate the transactions within the block proposal to ensure correctness. This necessitated the addition of APIs in the library for transaction verification during the consensus process.
3. **Block Signing**:
   
   - **Raft**: Once consensus is reached, the delivered block is signed by the node just before it's stored in the block store.
   - **BFT SMaRt**: The block is signed during the consensus protocol itself, specifically in the commit phase. Not just by one node, but by Q nodes.

**Consensus Algorithm**

**Unique Features**

**BDLS**

Checkpointing – Nodes periodically check their state.

Flooding – messages are flooded throughout the network to ensure that messages are eventually delivered.

**Mir BFT**

Leaderless Protocol

Parallel Leaders

Optimized for high throughput and latency.

**Zyzzvya**

Uses speculation to reduce the cost of BFT replication

Clients can detect and correct inconsistencies among replicas

**BFT - SMaRt**

Assembler organizes transactions into blocks

Censorship Resistance

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
