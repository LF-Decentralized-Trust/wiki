1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)
4. [BiniBFT - An Optimized BFT on Fabric](BiniBFT---An-Optimized-BFT-on-Fabric_20283476.html)
5. [Project Plan - BiniBFT](Project-Plan---BiniBFT_20283487.html)
6. [Evaluation Reports](Evaluation-Reports_20293727.html)
7. [Evaluation 1](Evaluation-1_20293737.html)

# Collaborative Learning Program : Riddhi Katarki

Created by Riddhi Katarki, last modified on Sep 05, 2023

# [BiniBFT - An Optimized BFT on Fabric](https://lf-hyperledger.atlassian.net/wiki/display/CLP/BiniBFT+-+An+Optimized+BFT+on+Fabric)

# **Evaluation 1 - Report**

## Submitted By: Riddhi Katarki

# Collaborative Learning Program

## Engagement Details

**Name of Mentee**

**Riddhi Katarki**

**Evaluation Period**

**06-07-2023 to 11-08-2023**

**Task**

**RAFT familiarization &amp; an application implementation using it**

**Date Submitted**

**13-08-2023**

**Mentor**

**Dr. Anasuya Threse Innocent**

# Tasks, Objectives, and Results

This Evaluation report consolidates the candidate’s work for Hyperledger CLP - BiniBFT project by BiniWorld Innovations Pvt Ltd during the internship (Weeks 1-6). The report has been categorized into two sections: outline the key task assigned to the candidate and day-to-day activities undertaken by the candidate.

- ### **Key Outline of the Task assigned to the candidate (This includes Project name, Problem statement, expected Output and other relevant details)**

**Hyperledger Fabric**

Hyperledger Fabric is a permissioned blockchain platform, supports multiple consensus algorithms, including Byzantine Fault Tolerance (BFT) and Raft. While both BFT and Raft offer fault tolerance and consensus within a distributed network, BFT holds several advantages over Raft within the context of Hyperledger Fabric:

1. Immediate Finality: BFT delivers instant finality upon block commitment, ensuring irreversible transactions. In contrast, Raft necessitates multiple communication rounds, leading to delayed transaction finality.
2. Enhanced Security: BFT is meticulously designed to thwart malicious attacks, particularly from Byzantine nodes. Conversely, Raft consensus remains susceptible to manipulation attempts by Byzantine nodes.
3. Optimized Performance: BFT is optimized for high-performance consensus, particularly in smaller to mid-sized networks. In contrast, Raft consensus may exhibit slower performance, especially in larger networks.
4. Flexibility: BFT's implementation on Fabric permits dynamic membership changes, enabling seamless addition or removal of nodes without disrupting consensus. On the other hand, Raft's consensus process can be susceptible to disruptions during node changes due to its leader election mechanism.

Collectively, BFT proves more fitting for permissioned blockchain platforms like Hyperledger Fabric, aligning with critical requirements such as security, immediate finality, and efficient performance.

**Raft Consensus**

- A node can have 3 states: Leader, candidate and follower
- Consensus is achieved through a simple majority Q = ½ N + 1
- Raft implements consensus by first electing a distinguished leader, then giving the leader complete responsibility for managing the replicated log.
- The leader accepts log entries from clients, replicates them on other servers, and tells servers when it is safe to apply log entries to their state machines. Having a leader simplifies the management of the replicated log.
- A leader can fail or become disconnected from the other servers; in which case a new leader is elected.

**Problems with Raft**

1. Transaction censorship - Client only sends transactions to a single orderer.
2. Followers need to trust the leader. There is no procedure for the clients to verify the logs of the leader.
3. If the leader acts maliciously, there is no mechanism that allows the network to recover.
4. Leader can overwrite the logs of follower nodes.

**Hyperledger Fabric – Mango Tracking System**

The application which is implemented on Hyperledger Fabric is a Mango Tracking System. The Fabric network is setup using microfab.

The network can be used to track the transactions between Producers and Sellers. An asset named ‘Mango’ is created which can be transacted between the entities.

**Install Chaincode**

**![](attachments/20293789/20295459.png?height=49)**

2023-08-11 17:54:11.739 IST 0001 INFO \[cli.lifecycle.chaincode] submitInstallProposal -&gt; Installed remotely: response:&lt;status:200 payload:"\\nHmango\_1:5af17586d37e69f875edd2f8259144f1aef932615170320576ad8aae4d2f220\\022\\007mango\_1" &gt; 

2023-08-11 17:54:11.740 IST 0002 INFO \[cli.lifecycle.chaincode] submitInstallProposal -&gt; Chaincode code package identifier: mango\_1:5af12579d37e69f985edd2f8259164f1aef932615170320544ad1aae4d2f63d0

**Approve Chaincode**

**![](attachments/20293789/20295460.png?height=55)**

2023-08-11 17:00:41.182 IST 0001 INFO \[chaincodeCmd] ClientWait -&gt; txid \[fab1bf99613fcbadc0537638e16ec776b51d1e0ae472d6a1be82ce8abd4beb20] committed with status (VALID) at [producersorgpeer-api.127-0-0-1.nip.io](http://producersorgpeer-api.127-0-0-1.nip.io):8080

**Commit Chaincode**

2023-08-11 18:01:39.315 IST 0001 INFO \[chaincodeCmd] ClientWait -&gt; txid \[73bc9ecd80ee1efbef639e110d02b11aac05618bd4243191c726d2643066b2d1] committed with status (VALID) at [producersorgpeer-api.127-0-0-1.nip.io](http://producersorgpeer-api.127-0-0-1.nip.io):8080

**Upgrade Chaincode**

**![](attachments/20293789/20295461.png?height=67)**

2023-08-11 18:38:56.809 IST 0001 INFO \[cli.lifecycle.chaincode] submitInstallProposal -&gt; Installed remotely: response:&lt;status:200 payload:"\\nHmango\_2:8aa4967cd1561b59d6c256ca9cf1d227ad05f7db8effaf312b330a3d750b47b8\\022\\007mango\_2" &gt;   
![](attachments/20293789/20295462.png?height=66)

2023-08-11 18:38:56.810 IST 0002 INFO \[cli.lifecycle.chaincode] submitInstallProposal -&gt; Chaincode code package identifier: mango\_2:8aa4967cd1561b59d6c256ca9cf1d227ad05f7db8effaf312b330a3d750b47b8

**Create Asset**

peer chaincode invoke -o [orderer-api.127-0-0-1.nip.io](http://orderer-api.127-0-0-1.nip.io):8080 --channelID mango-channel -n mango -c '{"function":"CreateMango","Args":\["MANGO1","1","mango corp","5000","10000"]}'

**Query**

peer chaincode query  -o [orderer-api.127-0-0-1.nip.io](http://orderer-api.127-0-0-1.nip.io):8080 --channelID mango-channel -n mango -c '{"function":"ReadMango","Args":\["MANGO1"]}'

## Attachments:

![](images/icons/bullet_blue.gif) [1.png](attachments/20293789/20295459.png) (image/png)  
![](images/icons/bullet_blue.gif) [3.png](attachments/20293789/20295460.png) (image/png)  
![](images/icons/bullet_blue.gif) [4.png](attachments/20293789/20295461.png) (image/png)  
![](images/icons/bullet_blue.gif) [5.png](attachments/20293789/20295462.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
