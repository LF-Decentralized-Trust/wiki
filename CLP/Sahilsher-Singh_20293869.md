1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)
4. [BiniBFT - An Optimized BFT on Fabric](BiniBFT---An-Optimized-BFT-on-Fabric_20283476.html)
5. [Project Plan - BiniBFT](Project-Plan---BiniBFT_20283487.html)
6. [Evaluation Reports](Evaluation-Reports_20293727.html)
7. [Evaluation 2](Evaluation-2_20293857.html)

# Collaborative Learning Program : Sahilsher-Singh

Created by Sahilsher Singh Sandhu, last modified on Oct 17, 2023

# [BiniBFT - An Optimized BFT on Fabric](https://lf-hyperledger.atlassian.net/wiki/display/CLP/BiniBFT+-+An+Optimized+BFT+on+Fabric)

# **Evaluation 2 - Report**

## Submitted By: Sahilsher Singh

# Collaborative Learning Program

## Engagement Details

**Name of Mentee**

**Sahilsher Singh**

**Evaluation Period**

**19-08-2023 to 06-10-2023**

**Task**

**Comparative study of BFT Protocols**

**Date Submitted**

**09-10-2023**

**Mentor**

**Dr. Anasuya Threse Innocent**

**Byzantine Generals' Problem: Unraveling the Essence of BFT**

In the realm of distributed systems, the Byzantine Generals' Problem stands as a classic and essential challenge to achieve consensus in a network prone to faults and deceit. This blog post delves into the depths of the Byzantine Generals' Problem, explores the concept of Byzantine Fault Tolerance (BFT), and investigates the intriguing notion of Byzantine failures. We'll also provide links to the original research papers that laid the foundation for this fascinating field.

**Understanding the Byzantine Generals' Problem**

**The Scenario:**

Imagine a group of Byzantine generals commanding their armies to launch a coordinated attack on a common enemy. Communication between the generals is established through messengers, but some of these messengers might be traitors loyal to the enemy. The challenge is to devise a strategy that ensures consensus among the loyal generals regarding the time to attack while considering the potential misinformation from traitorous messengers.

**The Problem**

The Byzantine Generals' Problem can be generalized as follows:

- A group of nodes (generals) needs to agree on a common decision or value.
- Some nodes in the network might be malicious and provide false information.
- The system must tolerate these Byzantine (malicious) failures and still reach a consensus.
- Byzantine Fault Tolerance (BFT)

**BFT: The Solution**

Byzantine Fault Tolerance (BFT) is the quality of a system to function correctly and reach consensus even when some of its components (nodes) are faulty or act maliciously. BFT algorithms address the Byzantine Generals' Problem by ensuring that nodes can agree on a single value despite misinformation or deceit from a portion of the nodes.

**Practical Byzantine Fault Tolerance (PBFT): A Milestone in Distributed Consensus**

In the realm of distributed systems, achieving consensus in the presence of faulty or malicious nodes has long been a central challenge. Practical Byzantine Fault Tolerance (PBFT) is a groundbreaking algorithm that addresses this problem and paves the way for robust, fault-tolerant distributed systems. In this blog post, we'll explore the concepts behind PBFT and provide links to the original research papers that introduced and expanded on this revolutionary algorithm.

**Understanding Practical Byzantine Fault Tolerance**

**The Consensus Challenge**

Consensus in a distributed system involves ensuring that all participating nodes agree on a single value or decision. However, this becomes complicated when some nodes are faulty or malicious, as they may provide conflicting information.

**Introducing PBFT**

PBFT, first introduced in the paper "Practical Byzantine Fault Tolerance" by Miguel Castro and Barbara Liskov, presents an elegant solution to the Byzantine Generals' Problem. This algorithm enables a distributed network of nodes to reach consensus even when a significant portion of the nodes is Byzantine (faulty or malicious).

**Key Concepts of PBFT**

PBFT operates by involving a set of nodes in a consensus protocol. Here are some key concepts:

- View Change: PBFT uses view changes to recover from failures or misbehaving primary nodes.
- Request Processing: Clients submit requests, and the primary node orders them.
- Commit Phase: Nodes multicast their votes to accept or reject a request.
- Checkpointing: Periodic checkpoints are taken to optimize recovery.

**Applications of PBFT**

PBFT has found applications in various domains, including:

- Blockchain: Many permissioned blockchains, such as Hyperledger Fabric, use PBFT-based consensus mechanisms.
- Secure Communication: PBFT can ensure secure and fault-tolerant communication in distributed systems.
- Financial Services: It's employed in financial systems to ensure transaction consistency.

**Zyzzyva: Speculating Byzantine Fault Tolerance - A Deep Dive**

In the world of distributed systems, Byzantine Fault Tolerance (BFT) is a critical concept to ensure the reliability and security of a network. "Zyzzyva: Speculating Byzantine Fault Tolerance" is an innovative research paper that explores new possibilities in achieving BFT. In this blog post, we'll take a closer look at the concepts behind Zyzzyva and provide links to the original research papers for those eager to delve deeper.

**Understanding Zyzzyva: Speculating Byzantine Fault Tolerance**

**The Byzantine Generals' Problem**

Before we dive into Zyzzyva, let's revisit the Byzantine Generals' Problem. This classic problem involves a group of generals, some of whom may be traitors, trying to reach a consensus on a coordinated action without being undermined by the traitorous generals.

**Introducing Zyzzyva**

Zyzzyva, introduced in the paper "Zyzzyva: Speculative Byzantine Fault Tolerance" by Ramakrishna Kotla et al., introduces a fascinating concept to improve the efficiency and performance of BFT protocols. This innovation is a speculative approach that significantly reduces the latency of BFT systems.

**Key Concepts of Zyzzyva**

Zyzzyva brings unique concepts to the world of BFT:

- Speculative Execution: It enables nodes to execute requests speculatively before receiving full consensus.
- Quorum Levels: Zyzzyva defines different quorum levels for normal and speculative requests.
- Reduced Latency: Speculative execution reduces the latency of BFT systems, making them more efficient.

**Applications of Zyzzyva**

Zyzzyva's innovative approach has potential applications in:

- Blockchain: It can be applied to blockchain networks for faster transaction confirmations.
- Finance: In financial systems, reduced latency can enhance trading platforms.
- IoT Networks: Zyzzyva's efficiency is valuable in Internet of Things (IoT) networks.

**Demystifying Mir-BFT: A Deep Dive into Byzantine Fault Tolerance**

**Introduction**

In the world of distributed systems, ensuring the reliability and security of a network can be a daunting task, especially when faced with potential malicious actors and system failures. This is where Byzantine Fault Tolerance (BFT) comes into play, offering a robust solution to these challenges. One notable BFT protocol that has gained attention is Mir-BFT, which leverages several innovative techniques to ensure the integrity and availability of distributed systems. In this blog post, we will explore Mir-BFT, its key components, and how it works.

**Mir-BFT in a Nutshell**

Mir-BFT is a Byzantine Fault Tolerance protocol designed to provide a high level of security and fault tolerance in distributed systems. It is particularly well-suited for blockchain platforms, where maintaining consensus among a network of nodes is critical.

**Key Implementation Details**

Mir-BFT comprises several important implementation details that enable its robust operation:

- The Client: When a client wants to make a request (BCAST(r)), it creates a message containing the request along with a timestamp (t). Timestamps are essential for maintaining order and consistency in a distributed system. Clients use a sliding window mechanism to manage their timestamps, ensuring that requests are processed in order.

<!--THE END-->

- Sequence Numbers and Buckets: In each epoch, leaders are assigned specific sequence numbers for proposing batches. These sequence numbers are distributed evenly among leaders, preventing bottlenecks. Buckets are used to group requests, and their assignment to leaders is carefully managed to ensure liveness.

<!--THE END-->

- Common Case Operation: The protocol's common case operation involves handling client requests, pre-prepare messages, and validations. It ensures that only valid requests are processed, preventing malicious attacks and ensuring the protocol's correctness.

<!--THE END-->

- Epoch Changes: Epoch changes can occur gracefully or ungracefully. Graceful changes happen when an epoch reaches its maximum sequence numbers, while ungraceful changes occur due to timeouts or failures. The protocol smoothly transitions from one epoch to another, ensuring that nodes remain in sync.

<!--THE END-->

- Checkpointing (Garbage Collection): Checkpoints are used to prune message logs and ensure the system's efficiency. Nodes periodically send checkpoint messages to each other, allowing for the removal of old data.

<!--THE END-->

- Signature Verification Sharding (SVS): To optimize performance, Mir-BFT employs signature verification sharding, where not all nodes verify all client signatures. This technique reduces CPU load during stable epochs without compromising security.

<!--THE END-->

- State Transfer: In case of node failures or asynchrony, Mir-BFT implements a state transfer mechanism to synchronize nodes' states. This ensures that recovered nodes can rejoin the network seamlessly.

<!--THE END-->

- Membership Reconfiguration: Adding or removing nodes and clients is handled through configuration requests, which are ordered and executed during checkpoints to maintain consensus.

<!--THE END-->

- Durability (Persisting State): While Mir-BFT doesn't require state persistence, nodes can choose to persist state information for recovery purposes. This optional feature ensures nodes can recover from crashes without compromising system integrity.

<!--THE END-->

- Implementation Architecture: The Mir-BFT protocol is implemented in Go and leverages multi-threading and parallelism to maximize performance. It utilizes multiple network connections between nodes and handles client requests independently of the main protocol.

**How Mir-BFT Works**

Mir-BFT achieves Byzantine Fault Tolerance by carefully orchestrating the interactions between nodes and clients. Here's a simplified overview of how it works:

- Client Requests: Clients send requests to the network, and these requests are timestamped to maintain order. These requests are initially sent to a subset of nodes.

<!--THE END-->

- Common Case Operation: Nodes validate and process incoming client requests, creating batches and pre-prepare messages. These messages are used to reach consensus among nodes.

<!--THE END-->

- Epoch Changes: When an epoch ends, nodes transition to the next epoch, either gracefully or ungracefully. During this transition, nodes update their configurations and continue processing requests.

<!--THE END-->

- Checkpointing: Periodically, nodes perform checkpointing to remove old data and keep the network efficient.

<!--THE END-->

- Signature Verification Sharding: In stable epochs, only a subset of nodes verifies client signatures, reducing the computational load.

<!--THE END-->

- State Transfer: In the event of node failures, state transfer mechanisms ensure that recovered nodes can synchronize with the rest of the network.

<!--THE END-->

- Membership Reconfiguration: Adding or removing nodes and clients is handled during checkpoints to maintain consensus.

**Demystifying BFT-SMART: A Deep Dive into Byzantine Fault-Tolerant Replication**

**Introduction**

Blockchain technology and distributed systems have reshaped the way we think about trust and decentralization. One of the cornerstones of these innovations is the Byzantine Fault-Tolerant (BFT) consensus mechanism. Among the various implementations of BFT, BFT-SMART stands out as a powerful and efficient solution. In this blog post, we will delve into the inner workings of BFT-SMART, demonstrating a comprehensive understanding of its architecture, principles, and configurations.

**Understanding BFT-SMART**

**BFT-SMART in a Nutshell**

BFT-SMART is a Java-based library designed to implement BFT consensus in a distributed system efficiently. Unlike other systems, it boasts a compact codebase of less than 13.5K lines, offering a refreshing simplicity that prioritizes correctness over complexity.

**Architectural Robustness**

The heart of BFT-SMART's success lies in its architecture, which thrives on robustness and efficiency. It breaks down tasks into threads that communicate through bounded queues, enabling seamless data flow and processing. Notably, the architecture handles hundreds of client-to-replica connections efficiently, catering to modern multicore and multiprocessor systems.

**Client Request Handling**

Client requests are received through a Netty-based thread pool, ensuring efficient processing. BFT-SMART distinguishes between ordered and unordered requests, delivering read-only commands directly to the service while placing complex requests in the client manager's queue. This design leverages the power of modern hardware by verifying multiple client signatures in parallel.

**The Proposer Thread**

The proposer thread, active only on the leader replica, assembles request batches and transmits them via the PROPOSE message of the consensus protocol. BFT-SMART dynamically fills batches until they reach a limit or run out of requests, ensuring efficiency in the agreement process.

**Message Handling and Processing**

Messages between replicas follow a structured path, going through sender and receiver threads that handle serialization, security features, and validation. Message processor threads focus on processing messages within the current consensus, efficiently managing data flow.

**Delivery and Reply Handling**

Once consensus is reached on a replica, a batch of decisions is placed in a queue. The delivery thread processes these batches, executing requests and sending replies back to clients, thus completing the consensus cycle.

**Request Timer Thread**

A request timer thread periodically checks for pending requests that exceed a pre-defined timeout. It helps maintain system integrity, forwarding delayed requests to the leader replica and, in extreme cases, triggering a synchronization phase.

**Alternative Configurations**

BFT-SMART's flexibility extends to its fault tolerance configurations:

- Crash Fault Tolerance: When activated, this feature ensures the system tolerates a simple minority of replica crashes, making it resilient in scenarios where replicas may fail.
- Malicious Byzantine Faults: To guard against malicious attacks, BFT-SMART can use public-key signatures on requests. Although it doesn't currently protect against all malicious leader attacks, it offers a strong defense against many types of threats.

**Understanding the Differences Between Mir-BFT and BFT-SMART**

Blockchain and distributed ledger technologies have evolved significantly over the years, with various consensus algorithms and protocols emerging to address scalability, security, and performance challenges. Two such consensus protocols are Mir-BFT and BFT-SMART, each designed to facilitate agreement among network nodes. In this article, we'll delve into the nuances of these protocols, exploring their differences and unique features.

**The Basics of Byzantine Fault Tolerance**

Before we dive into the distinctions between Mir-BFT and BFT-SMART, let's recap the concept of Byzantine Fault Tolerance (BFT). BFT is a critical property of distributed systems that ensures the network can continue to operate correctly, even in the presence of faulty or malicious nodes. Byzantine failures refer to nodes in a network exhibiting arbitrary and potentially harmful behavior.

BFT consensus algorithms aim to achieve consensus among nodes in a distributed network. In other words, they ensure that all nodes agree on the state of the network, even when some nodes are dishonest or fail.

**Mir-BFT: Understanding the Approach**

Mir-BFT is a BFT-based consensus protocol that aims to provide robustness, scalability, and performance in a distributed network. Let's explore some key aspects of Mir-BFT:

1. **Client Requests and Batching**

Mir-BFT organizes client requests into batches. Each batch contains a sequence of client requests and is assigned a unique sequence number. Batching helps optimize the processing of multiple requests simultaneously, enhancing system throughput.

1. **Client Watermarks**

Mir-BFT employs a concept known as "client watermarks." These watermarks define a range of sequence numbers that a client can use. This approach allows multiple requests from the same client to be in progress simultaneously, ensuring high throughput without overwhelming the system.

1. **Sequence Numbers and Buckets**

Mir-BFT partitions sequence numbers into buckets, distributing them among different nodes. This partitioning is achieved using modulo arithmetic, and it helps balance the workload among nodes. Leaders are responsible for proposing batches, and multiple leaders can propose batches in parallel.

1. **Common Case Operation**

In the common case, when a client sends a request, Mir-BFT checks if it falls within the appropriate sequence number range and bucket. The protocol ensures that requests are processed correctly and that client signatures are valid. This robust validation process is essential for maintaining the security of the network.

1. **Epoch Changes and State Transfer**

Mir-BFT handles epoch changes gracefully, allowing the network to transition from one epoch to the next without disruptions. Additionally, the protocol supports state transfers, ensuring that nodes can recover and synchronize after temporary failures or asynchrony.

1. **Durability**

Mir-BFT provides an option for persisting state and message logs, enhancing fault tolerance. However, enabling durability may impact latency, especially in scenarios with a small number of nodes.

**BFT-SMART: An Overview**

BFT-SMART is another Byzantine Fault Tolerant consensus protocol designed to address the challenges of distributed systems. Let's explore some of its distinctive features:

1. **View Changes**

BFT-SMART incorporates a "view change" mechanism to handle Byzantine failures and achieve consensus. When a node detects a failure or malicious behavior, it initiates a view change, allowing the network to continue functioning with honest nodes.

1. **Multi-Consensus**

One of the notable features of BFT-SMART is its support for multi-consensus. It can run multiple instances of the consensus protocol concurrently. This capability is beneficial for applications with diverse requirements, such as handling different types of transactions simultaneously.

1. **Dynamic Membership**

BFT-SMART is designed to accommodate dynamic changes in network membership. It allows nodes to join and leave the network without disrupting consensus. This feature is crucial for blockchain networks that may experience nodes going offline or new nodes joining.

1. **Flexible Configuration**

BFT-SMART offers flexibility in configuration, enabling network administrators to adjust parameters according to their specific needs. This adaptability is essential for optimizing the protocol's performance and resilience.

**Key Differences Between Mir-BFT and BFT-SMART**

Now that we've explored the fundamental aspects of both Mir-BFT and BFT-SMART, let's highlight the key differences between these two Byzantine Fault Tolerant consensus protocols:

1. **Batching vs. Multi-Consensus**

Mir-BFT primarily focuses on batching client requests to optimize throughput. In contrast, BFT-SMART emphasizes multi-consensus, allowing multiple consensus instances to run concurrently. This distinction makes BFT-SMART more versatile in handling different types of transactions simultaneously.

1. **Client Watermarks vs. Dynamic Membership**

Mir-BFT employs client watermarks to manage the sequence of client requests effectively. BFT-SMART, on the other hand, excels in accommodating dynamic changes in network membership, making it suitable for networks with frequently changing participants.

1. **Epoch Changes vs. View Changes**

Mir-BFT gracefully handles epoch changes to ensure network continuity. BFT-SMART, on the other hand, utilizes view changes as a mechanism for recovering from Byzantine failures. These differing approaches reflect their respective strategies for fault tolerance.

1. **Durability vs. Flexible Configuration**

Mir-BFT offers durability as an optional feature, allowing state and message logs to be persisted. BFT-SMART, in contrast, provides a more flexible configuration, enabling administrators to fine-tune parameters to meet their specific requirements.

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
