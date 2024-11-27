1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)
4. [BiniBFT - An Optimized BFT on Fabric](BiniBFT---An-Optimized-BFT-on-Fabric_20283476.html)
5. [Project Plan - BiniBFT](Project-Plan---BiniBFT_20283487.html)
6. [Evaluation Reports](Evaluation-Reports_20293727.html)

# Collaborative Learning Program : Evaluation 3

Created by A Anasuya Threse Innocent, last modified by Sahilsher Singh Sandhu on Dec 25, 2023

Evaluation 3 shows the proposed framework of BiniBFT consensus.

It is a group evaluation, and the report is given below.

# [BiniBFT - An Optimized BFT on Fabric](https://lf-hyperledger.atlassian.net/wiki/display/CLP/BiniBFT+-+An+Optimized+BFT+on+Fabric)

# **Evaluation 3 - Report**

## Submitted By: Riddhi Katarki , Ajitesh Kumar Soni , Abhishek Ranjan , Ashna P S , Sahilsher Singh , Siddhant Prateek Mahanayak

## Collaborative Learning Program

## Engagement Details

**Name of Mentee**

**Riddhi Katarki , Ajitesh Kumar Soni , Abhishek Ranjan , Ashna P S , Sahilsher Singh , Siddhant Prateek Mahanayak**

**Evaluation Period**

**08-10-2023 to 13-12-2023**

**Task**

**BiniBFT Framework**

**Date Submitted**

**14-12-2023**

**Mentor**

**Dr. Anasuya Threse Innocent**

# Consensus Mechanism with Random Polling

![](attachments/20293909/20295580.png?height=250)

1. **Transaction Initiation**: The process starts with the client initiating a transaction (Trx initiation). This is where a user or an application requests a transaction to be processed by the network.
2. **Transaction Batching**: After a transaction is initiated, it is grouped with other transactions into a batch (Batched trx) which improves the efficiency of processing multiple transactions together rather than individually.
3. **Leader Selection**: Once transactions are batched, a leader is selected to propose the batch of transactions to the rest of the network. The leader selection is aided by a Verifiable Random Function (VRF), which helps in choosing the leader in a way that is random but verifiable by other participants in the network.
4. **Transaction Proposal**: The leader then proposes the batched transactions (Trx proposal) to the network. This involves sending out the transaction data to other nodes in the network for validation.
5. **Polling**: Concurrently, there is a random polling of 33% of the network. This suggests that a subset of the network is selected randomly to vote on the proposed transactions. The chart indicates that the process waits until 1/3 of the votes are received.
6. **Transaction Commitment**: Once the leader has successfully proposed the transaction and the necessary votes are received, the transaction is committed (Commit Trx) by the network.
7. **Transaction Settlement**: After the transaction is committed, it is then settled (Finalised Trx), which means it is officially recorded on the blockchain. This completes the process, and the client is informed that the transaction has been finalised.

# Consensus Mechanism with Time Weighted Voting

![](attachments/20293909/20295588.png?height=250)

01. **Transaction Initiation**: A client starts the process by initiating a transaction.
02. **Transaction Batching**: Transactions are batched together for processing efficiency.
03. **Leader Selection**: A leader is selected through a Verifiable Random Function (VRF) to manage the batched transactions. This ensures randomness and fairness in leader selection.
04. **Transaction Proposal**: The selected leader proposes the batched transactions to the network.
05. **Time Weighted Voting (Polling)**:
06. - The network nodes participate in polling to approve the transaction proposal. This polling uses the Time Weighted Voting mechanism.
    - Each node in the network has a weight (w) that increases over time or epochs, representing their tenure in the network.
07. **Voting Constraints**:
08. - Individual node weight is capped to ensure no single node can dominate the decision due to its longevity (as shown in the second chart, where **w(i) &lt;= 0.33 * (network\_w)**).
    - The sum of the weights (**sum(w)**) from the nodes participating in the polling must be greater than or equal to 51% of the total network weight to reach a decision (**sum(w) &gt;= (0.51 * network\_w)**).
09. **Transaction Commitment**: If the proposal receives enough weighted votes (&gt;= 51% of network weight), the transaction is committed.
10. **Transaction Settlement**: The committed transaction is then finalized and recorded on the blockchain, and the client is notified of the transaction settlement.

# Dynamic Leader Allocation Process

01. **System Load Monitoring:** Continuously monitor the system's transaction rate, processing capacity, and overall network load.
02. **Load Thresholds:** Define load thresholds that trigger dynamic leader allocation. Consider factors such as transaction backlog and processing delays.
03. **Leader Availability:** Track the availability and performance metrics of potential leaders in the network.
04. **Allocation Trigger:** When the system load surpasses predefined thresholds, initiate dynamic leader allocation based on a Verifiable Random Function (VRF).
05. **VRF-Based Random Leader Selection:** Use a Verifiable Random Function to generate a random number that determines the leader selection. This ensures randomness while providing verifiability to other participants.
06. **Batch Queue Management:** If a batch queue exists, distribute batches among the selected leaders to ensure an even workload distribution.
07. **Concurrency Control:** Implement synchronization protocols to manage interactions between multiple leaders and maintain consistency.
08. **Transaction Proposal:** Each leader, determined by the VRF-based random selection, independently proposes its assigned batches to the network for validation.
09. **Polling and Voting:** Continue with the random polling and voting process for each proposed batch, ensuring decentralized agreement on transaction validity.
10. **Commitment Decision:** Based on the voting outcomes for each leader's proposed batches, make a commitment decision for each batch independently.
11. **Transaction Settlement:** Finalise the committed batches and record them on the blockchain.
12. **Leader Deallocation:** Periodically reassess the system load. If the load decreases and additional leaders are no longer needed, deallocate the surplus leaders.

[A Anasuya Threse Innocent](https://lf-hyperledger.atlassian.net/wiki/people/712020:661aa2f0-0e5a-4e8d-b57b-de10204ea99b?ref=confluence) 

[Riddhi Katarki](https://lf-hyperledger.atlassian.net/wiki/people/6199b998ebce470067ece3e1?ref=confluence) 

[Ajitesh kumar soni](https://lf-hyperledger.atlassian.net/wiki/people/712020:de501d57-4bf2-4ee4-956b-34b643026cbf?ref=confluence) 

[Abhishek Ranjan](https://lf-hyperledger.atlassian.net/wiki/people/712020:4f9b45e2-b67f-4ef0-8cc2-93dced1f556f?ref=confluence) 

[Ashna PS](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e42b48d-3ac2-4143-97b8-58b29768cece?ref=confluence) 

[Siddhant Prateek](https://lf-hyperledger.atlassian.net/wiki/people/606753900a6b3f0069a6871b?ref=confluence) 

[Sahilsher Singh Sandhu](https://lf-hyperledger.atlassian.net/wiki/people/6404e4350a4a47fb8d22ec2e?ref=confluence) 

## Attachments:

![](images/icons/bullet_blue.gif) [image-2023-12-16\_16-17-51.png](attachments/20293909/20295580.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-12-16\_16-19-32.png](attachments/20293909/20295581.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screenshot from 2023-12-20 02-20-58.png](attachments/20293909/20295586.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screenshot from 2023-12-19 23-55-49.png](attachments/20293909/20295587.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screenshot from 2023-12-18 14-44-26.png](attachments/20293909/20295588.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
