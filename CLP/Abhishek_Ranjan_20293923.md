1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)
4. [BiniBFT - An Optimized BFT on Fabric](BiniBFT---An-Optimized-BFT-on-Fabric_20283476.html)
5. [Project Plan - BiniBFT](Project-Plan---BiniBFT_20283487.html)
6. [Evaluation Reports](Evaluation-Reports_20293727.html)
7. [Evaluation 2](Evaluation-2_20293857.html)

# Collaborative Learning Program : Abhishek\_Ranjan

Created by Abhishek Ranjan, last modified on Dec 15, 2023

# [BiniBFT - An Optimized BFT on Fabric](https://lf-hyperledger.atlassian.net/wiki/display/CLP/BiniBFT+-+An+Optimized+BFT+on+Fabric)

 

### **Evaluation 2 - Report**

### Submitted By: Abhishek Ranjan

### Collaborative Learning Program

### Engagement Details

### **Name of Mentee**

### **Abhishek Ranjan**

### **Evaluation Period**

### **12-08-2023 to 07-10-2023**

### **Task**

### **Comparative Study of BFT Protocols**

### **Date Submitted**

### **09-11-2023**

### **Mentor**

### **Dr. Anasuya Threse Innocent**

### Tasks, Objectives, and Results

### This Evaluation report consolidates the candidate’s work for Hyperledger CLP - BiniBFT project by BiniWorld Innovations Pvt Ltd during the internship (Weeks 6-12). The report has been categorized into two sections: outline the key task assigned to the candidate and day-to-day activities undertaken by the candidate.

### **Key Outline of the Task assigned to the candidate (This includes Project name, Problem statement, expected Output and other relevant details)**

### **Comparing Consensus Protocol in Hyperledger Fabric**

### **Introduction**

Consensus algorithms play a critical role in blockchain networks to ensure that all participants agree on the validity of transactions and the state of the ledger. In the context of Hyperledger, which is an open-source blockchain platform for enterprise use cases, several consensus algorithms are available, and the choice of algorithm depends on the specific requirements of the blockchain network. Here's a brief summary of some of the key consensus algorithms used in Hyperledger

### **What is Mir BFT (Mir Byzantine Fault Tolerant)?**

Mir BFT (Mir Byzantine Fault Tolerant) is a consensus algorithm designed for permissioned blockchain networks. It offers high throughput and Byzantine fault tolerance, ensuring the security and reliability of transactions. While it excels in providing low-latency consensus, it may not be as scalable as some other consensus mechanisms, and its implementation can be complex. Mir BFT is well-suited for applications where known and trusted participants require fast and secure transaction validation.

#### Advantages:

- High Throughput: Mir BFT is designed for high transaction throughput, making it suitable for applications requiring fast and efficient consensus.
- Resilience: It provides Byzantine fault tolerance, ensuring the network remains secure and operational even in the presence of malicious nodes.
- Permissioned Networks: Well-suited for permissioned blockchain networks, where all participants are known and trusted.
- Low Latency: Achieves low latency in reaching consensus, crucial for real-time applications.

#### Limitations:

- Scalability: Mir BFT's scalability is limited compared to some other consensus algorithms, making it less suitable for large networks.
- Complexity: Implementing Mir BFT can be complex and may require significant development effort.
- Resource Intensive: It can be resource-intensive, which may pose challenges in terms of hardware requirements.
- Centralization of Power: In permissioned networks, the concentration of power among a limited set of known participants can raise concerns about centralization.

### What is Zyzzvya?

Zyzzvya is a novel consensus algorithm that takes a unique approach to achieving distributed consensus. it is executed by 3f + 1 replicas, and execution is organized into a sequence of views. Within a view, a single replica is designated as the primary responsible for leading the agreement sub-protocol.

Zyzzvya uses a reputation-based system to determine which nodes are trustworthy and should be given more weight in the consensus process

Zyzzyva uses sharding to divide the state of a blockchain into multiple parts, which allows for better scalability and efficiency

## **comparison**

Consensus Approach:

- PBFT: Uses a traditional Byzantine fault-tolerant approach, where nodes must reach an agreement through multiple rounds of communication and voting.
- Mir BFT: Also employs a Byzantine fault-tolerant approach but simplifies the consensus process by requiring only a single round of message passing.
- Zyzzvya: Takes a unique approach by using a reputation-based system to determine consensus, allowing for faster agreement without multiple rounds of communication.

Leader Node Requirement:

- PBFT: Requires the presence of a leader node to initiate the consensus process, which can introduce a single point of failure or centralization.
- Mir BFT: This does not require a leader node, which can make it more resilient against leader failures or attacks targeting the leader.
- Zyzzvya: It also does not require a leader node, enhancing decentralization and reducing the risk of a single point of failure.

Message Passing Rounds:

- PBFT: Involves multiple rounds of message passing and voting, making the consensus process relatively complex and resource-intensive.
- Mir BFT: Simplifies the process by achieving consensus in a single round of message passing, which can lead to faster agreement.
- Zyzzvya: Due to its reputation-based system, it aims for faster consensus, potentially requiring fewer rounds of communication.

Security Mechanisms:

- PBFT: Offers a high level of security through its Byzantine fault-tolerant design, making it suitable for mission-critical applications.
- Mir BFT: Also provides Byzantine fault tolerance but with a simplified approach, which may be more efficient but potentially less secure in some scenarios.
- Zyzzvya: Relies on a reputation-based system, which can be efficient and faster but may be less secure in certain situations, especially when dealing with malicious actors.

Performance and Energy Efficiency:

- PBFT: Known for its reliability and security but can be resource-intensive, impacting performance and energy consumption.
- Mir BFT: Strives for improved efficiency and performance with its single-round consensus process.
- Zyzzvya: Aims for faster consensus times and lower energy consumption, potentially making it more efficient than PBFT and Mir BFT.

The choice between these consensus algorithms would depend on the specific requirements and constraints of the distributed network or blockchain system. PBFT is often chosen for applications where security and reliability are paramount, while Mir BFT and Zyzzvya may be considered for scenarios that prioritize efficiency and performance. However, the actual effectiveness and security of Zyzzvya would depend on its specific implementation and the real-world dynamics of the network it operates in.

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
