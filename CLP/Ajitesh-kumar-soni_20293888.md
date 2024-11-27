1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)
4. [BiniBFT - An Optimized BFT on Fabric](BiniBFT---An-Optimized-BFT-on-Fabric_20283476.html)
5. [Project Plan - BiniBFT](Project-Plan---BiniBFT_20283487.html)
6. [Evaluation Reports](Evaluation-Reports_20293727.html)
7. [Evaluation 2](Evaluation-2_20293857.html)

# Collaborative Learning Program : Ajitesh-kumar-soni

Created by Ajitesh kumar soni, last modified on Nov 20, 2023

# [BiniBFT - An Optimized BFT on Fabric](https://lf-hyperledger.atlassian.net/wiki/display/CLP/BiniBFT+-+An+Optimized+BFT+on+Fabric)

# **Evaluation 2 - Report**

## Submitted By: Ajitesh kumar soni

# Collaborative Learning Program

## Engagement Details

**Name of Mentee**

**Aijtesh kumar soni**

**Evaluation Period**

**19-08-2023 to 09-11-2023**

**Task**

**Comparative study of BFT Protocols**

**Date Submitted**

**09-11-2023**

**Mentor**

**Dr. Anasuya Threse Innocent**

# Tasks, Objectives, and Results

This Evaluation report consolidates the candidate’s work for Hyperledger CLP - BiniBFT project by BiniWorld Innovations Pvt Ltd during the internship (Weeks 6-12). The report has been categorized into two sections: outline the key task assigned to the candidate and day-to-day activities undertaken by the candidate.

### **Key Outline of the Task assigned to the candidate (This includes Project name, Problem statement, expected Output and other relevant details)**

**Comparing Consensus Protocol in Hyperledger Fabric**

## **BFT SMART**

### **How Challenges Are Addressed in the New Attempt:**

1. 1. Simplified Architecture: The new implementation simplifies the system by using a single process and a consistent Go language for both orderer front-end and BFT server.
   2. MSP Integration: It seamlessly integrates with Fabric's MSP, ensuring compliance with Fabric's standards and including BFT cluster server identities in Fabric's configuration.
   3. Enhanced Block Validation: The new approach includes the signatures of 2F + 1 BFT cluster servers in blocks for better verification.
   4. Optimized Communication Rounds: Communication rounds are reduced to three by optimizing the consensus protocol, with acceptable performance for most use cases.

<!--THE END-->

- Effective Transaction Validation: The new BFT ordering service enables followers to validate leader-proposed transactions effectively, enhancing the correctness of the BFT protocol**.**

### **The BFT-SMART protocol in Hyperledger Fabric provides the following key features:**

1. Simplified Message Pattern: The protocol simplifies the message pattern, making it easier to understand and implement.
2. View Change Protocol: It includes a view change mechanism to elect a new leader when the current leader is faulty.
3. Consensus Safety and Liveness: BFT-SMART ensures that all correct nodes agree on the same valid values (safety) and guarantees that if one correct node delivers a value, others will eventually do so (liveness).
4. MSP Integration: It integrates seamlessly with Fabric's Membership Service Provider (MSP), ensuring compliance with Fabric's security and identity framework.
5. Proper Transaction Validation: BFT-SMART enables proper validation of transactions against Fabric's semantics without excessive code overhead.
6. Dynamic Consenter Set: The protocol allows dynamic updates to the consenter set, ensuring only authorized nodes participate in consensus.

### it's important to note that BFT-Smart may not be the best choice for scenarios where high throughput and low latency are the primary requirements, as it might exhibit slightly lower performance

## **MIR-BFT**

### **1.** Multiple Parallel Leaders: Supports concurrent proposal by multiple leaders, increasing throughput and eliminating single-leader bottlenecks.

### 2. Request Authentication: Uses signatures for request authentication, enhancing security and preventing faulty client attacks related to MAC authenticators.

### 3. Batching and Watermarks: Processes requests in batches and utilizes request and batch watermarks to improve throughput.

### 4. Request Duplication Prevention: Prevents request duplication attacks by partitioning the request hash space and assigning subsets to different leaders.

### 5. Client Signature Verification Sharding Optimization: Optimizes throughput by offloading CPU overhead through client signature verification sharding.

### 6. Robustness and Performance: Designed to be robust to Byzantine faults and delivers high performance, especially in wide-area networks (WANs).

### Overall, Mir-BFT combines robustness, high throughput, and security features to provide an efficient Byzantine fault-tolerant total order broadcast protocol for decentralized networks.

## **Zyzzyva**

- Speculative Byzantine Fault Tolerance: Zyzzyva implements speculative BFT, reducing replication costs by avoiding a three-phase commit protocol.
- Optimistic Order Adoption: Zyzzyva quickly processes requests based on the primary server's order proposal, minimizing all-to-all communication and replication overhead.
- Reduced Replication Overheads: Zyzzyva minimizes all-to-all communication and required replicas, achieving high throughput and practical BFT replication.
- Support for High-Contention Workloads: Designed to efficiently handle concurrent requests and high-contention workloads.
- Simplified State Machine Replication Semantics: Zyzzyva simplifies replication semantics for easier implementation and understanding.
- Ability to Handle Faulty Clients: Ensures consistent processing of erroneous or malicious client requests, helping correct replicas converge on a single order.
- Scalability and Performance: Zyzzyva achieves high throughput and low latency, outperforming other BFT protocols like PBFT and HQ in terms of performance and cryptographic overhead.

### In summary, Zyzzyva stands out for its performance improvements, speculative execution approach, support for high-contention workloads, simplified replication semantics, and fault scalability. These factors make it the best choice for applications that require efficient and reliable Byzantine Fault-Tolerant replication.

## **BDLS**

### 1. 2-Phase BFT Protocol: BDLS employs a 2-phase Byzantine Fault Tolerance protocol, reaching consensus through a two-step process.

### 2. Chained "**Decide**" Logic: It uses a chaining paradigm, spreading commitment phases across rounds, requiring a 2-chain with contiguous round numbers for certification.

### 3. Permissioned Blockchain Focus: Designed for permissioned blockchains like Libra, where BFT participants remain static. Less suitable for permissionless blockchains with frequent participant changes.

### 4. Reduced Round Complexity: Aims for consensus with fewer rounds compared to PBFT, Tendermint BFT, and HotStuff BFT, enhancing efficiency.

### 5. Reduced Communication Complexity: Minimizes messages needed for consensus in synchronized networks, improving communication efficiency.

### 6. Security in Type II Networks: Secure in Type II partial synchronous networks, ensuring liveness and safety in the presence of Byzantine faults.

### 7. Linear Authenticator Complexity: Achieves linear authenticator complexity with threshold digital signature schemes, minimizing authenticator operations for consensus.

### 8. Pacemaker Integration: Allows integration of Pacemaker functionality for round synchronization without additional workload, ensuring efficient consensus.

### In summary, BDLS excels in providing Byzantine Fault Tolerance for stable, permissioned blockchains like Libra, where participant changes are infrequent. However, its feasibility diminishes in dynamic, permissionless blockchains where frequent participant changes occur. In such scenarios, alternative BFT protocols designed for adaptability to changing participant sets may be more appropriate.

## **Comparison between these protocols**

![](attachments/20293888/20295519.png?height=250)

## Attachments:

![](images/icons/bullet_blue.gif) [Screenshot 2023-11-20 at 1.29.17 PM.png](attachments/20293888/20295519.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
