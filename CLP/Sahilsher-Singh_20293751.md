1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)
4. [BiniBFT - An Optimized BFT on Fabric](BiniBFT---An-Optimized-BFT-on-Fabric_20283476.html)
5. [Project Plan - BiniBFT](Project-Plan---BiniBFT_20283487.html)
6. [Evaluation Reports](Evaluation-Reports_20293727.html)
7. [Evaluation 1](Evaluation-1_20293737.html)

# Collaborative Learning Program : Sahilsher Singh

Created by Sahilsher Singh Sandhu, last modified on Oct 17, 2023

# [BiniBFT - An Optimized BFT on Fabric](https://lf-hyperledger.atlassian.net/wiki/display/CLP/BiniBFT+-+An+Optimized+BFT+on+Fabric)

# **Evaluation 1 - Report**

## Submitted By: Sahilsher Singh

# Collaborative Learning Program

## Engagement Details

**Name of Mentee**

**Sahilsher Singh**

**Evaluation Period**

**06-07-2023 to 11-08-2023**

**Task**

**Blockchain and RAFT familiarization &amp; an example application implementation using it**

**Date Submitted**

**18-08-2023**

**Mentor**

**Dr. Anasuya Threse Innocent**

# Tasks, Objectives, and Results

This Evaluation report consolidates the candidate’s work for Hyperledger CLP - BiniBFT project by BiniWorld Innovations Pvt Ltd during the internship (Weeks 1-6). The report has been categorized into two sections: outline the key task assigned to the candidate and day-to-day activities undertaken by the candidate.

- ### **Key Outline of the Task assigned to the candidate (This includes Project name, Problem statement, expected Output and other relevant details)**

<!--THE END-->

- Team Introduction: Introduce team members to each other, including their roles and responsibilities.
- Project Overview: Provide an overview of the project, its goals, and objectives. Expectations and Goals: Set clear expectations for team members, clarify project goals, and ensure everyone is aligned.
- Setting up Communication Channels: Establish communication channels for the team to collaborate effectively (e.g., Slack, email, project management tools).
- Kick-off Meeting: Hold a kick-off meeting to discuss the project's scope, deliverables, and timeline.
- Project Planning: Initiate the project planning phase, including defining tasks, milestones, and dependencies.
- Start learning: The public blockchain and its consensus algorithms, as I don't have prior experience of it.
- Research and Background: Conduct any necessary research to gain a deeper understanding of the project domain. The team discussed the use case and identified the need for a consensus algorithm, specifically the Raft consensus algorithm. Raft Consensus Shortcomings: During discussions, the limitations of the Raft consensus algorithm were analyzed, highlighting potential areas for improvement.
- Ongoing journey of learning: Creating little projects to get familiar with public blockchain.

**Hyperledger Fabric**

Hyperledger Fabric is a permissioned blockchain platform, supports multiple consensus algorithms, including Byzantine Fault Tolerance (BFT) and Raft. While both BFT and Raft offer fault tolerance and consensus within a distributed network, BFT holds several advantages over Raft within the context of Hyperledger Fabric:

1. BFT Consensus Methods and Blockchain Interaction: Researched and examined existing Byzantine Fault Tolerant (BFT) consensus methods and their interaction with blockchain systems. Evaluated how BFT algorithms enhance the security and reliability of blockchain networks.

<!--THE END-->

1. Overview of Raft Consensus Algorithm: Provided a concise overview of the Raft consensus algorithm. Described its key components, including leader election, log replication, and safety properties. Understood the algorithm's role in achieving consensus in distributed systems.

<!--THE END-->

1. Raft Consensus Algorithm Limitations: Analyzed the limitations of the Raft consensus algorithm, including its inability to tolerate Byzantine faults. Identified potential areas for improvement.

<!--THE END-->

1. Hyperledger Labs BDLS: Explored Hyperledger Labs BDLS, a distributed ledger system designed to work with various consensus algorithms. Understood how it can be used to implement the Raft consensus algorithm.

<!--THE END-->

1. Architecture of Hyperledger Labs BDLS: Examined the architecture of Hyperledger Labs BDLS, including its components and their interactions. Understood how the Raft consensus algorithm is implemented in Hyperledger Labs BDLS (will be discussed in detail in the next week).

<!--THE END-->

1. Getting hands dirty: On the basis of my research, I started to create a little project to get a better understanding of the blockchain and its consensus algorithms. Also continuing my journey of further learning.

Collectively, BFT proves more fitting for permissioned blockchain platforms like Hyperledger Fabric, aligning with critical requirements such as security, immediate finality, and efficient performance.

- Byzantine: I have started to learn about Byzantine and its consensus algorithms. Byzantine fault tolerance is the dependability of a fault-tolerant computer system, particularly distributed computing systems, where components may fail and there is imperfect information on whether a component has failed. In a "Byzantine failure", a component such as a server can inconsistently appear both failed and functioning to failure-detection systems, presenting different symptoms to different observers. The term takes its name from an allegory, the "Byzantine Generals' Problem", developed to describe this behavior. 1/3 of the nodes can be faulty.

<!--THE END-->

- Raft: I have started to learn about Raft and its consensus algorithms. Raft is a consensus algorithm that is designed to be easy to understand. It's equivalent to Paxos in fault-tolerance and performance. The difference is that it's decomposed into relatively independent subproblems, and it cleanly addresses all major pieces needed for practical systems. We hope Raft will make consensus available to a wider audience, and that this wider audience will be able to develop a variety of higher quality consensus-based systems than are available today. It contains a leader, follower, and candidate. The leader is responsible for managing the log and replicating it to other nodes. The follower is responsible for responding to requests from the leader and forwarding requests to the leader. The candidate is responsible for requesting votes from other nodes.

<!--THE END-->

- Paxos: I have started to learn about Paxos and its consensus algorithms. Paxos is a consensus algorithm that is used to achieve consensus in a network of unreliable processors. It was first introduced by Leslie Lamport in 1989. It is a two-phase protocol that allows a collection of machines to agree on a value even if some of the machines fail. It is a leaderless algorithm that works in rounds. In each round, every node proposes a value and votes for a value proposed by some node. The algorithm guarantees that a single value will be agreed upon by all the non-faulty nodes. It contains three roles: proposer, acceptor, and learner. The proposer proposes a value, the acceptor accepts a value, after the decision all are converted into the learner learns the value.

<!--THE END-->

- Corda: I have started to learn about Cordo and its consensus algorithms. In this the transaction is not broadcasted to all the nodes, instead it is shared with the nodes which are involved in the transaction and the notary node. Notary node is the node which validates the transaction and then broadcasts it to the other nodes.

**Problems with Raft**

1. Transaction censorship - Client only sends transactions to a single orderer.
2. Followers need to trust the leader. There is no procedure for the clients to verify the logs of the leader.
3. If the leader acts maliciously, there is no mechanism that allows the network to recover.
4. Leader can overwrite the logs of follower nodes.

**Task outline and assignment:**

- I was a total dumb student in the blockchain field, so I started with the public blockchain first. I completed a full course in almost 15-20 days.
- - [https://learnweb3.io/degrees/ethereum-developer-degree/freshman/](https://learnweb3.io/degrees/ethereum-developer-degree/freshman/)
  - Completed freshman, sophomore, junior, senior all parts in it.

<!--THE END-->

- After Public Blockchain I moved to private Blockchain: Hyperledger theory understanding.

<!--THE END-->

- Read papers on Hyperledger consensus mechanism and tried to implement it.

<!--THE END-->

- For example implementation I used
- - [https://github.com/Sandhu-Sahil/fabric-samples](https://github.com/Sandhu-Sahil/fabric-samples)
  - Also Fiber docs: [https://hyperledger-fabric.readthedocs.io/en/latest/](https://hyperledger-fabric.readthedocs.io/en/latest/)
  - Implemented test networks and performed transactions on it.

<!--THE END-->

- Built a mango tracking system using microFab and performed testing on it.
- - Helping docs: [https://learn.kba.ai/course/hyperledger-fabric-fundamentals-golang/](https://learn.kba.ai/course/hyperledger-fabric-fundamentals-golang/)

<!--THE END-->

- Further Implementation:
- - The provided links lead to two GitHub repositories: "bootstrapping-hyperledger" and "mango-tracking-sys." The former appears to be related to bootstrapping Hyperledger blockchain projects, while the latter seems to involve a mango tracking system. Further details about their purposes, technologies used, and goals would enhance the understanding of these projects within the documentation.
  - - [https://github.com/Sandhu-Sahil/bootstrapping-hyperledger](https://github.com/Sandhu-Sahil/bootstrapping-hyperledger)
    - [https://github.com/Sandhu-Sahil/mango-tracking-sys](https://github.com/Sandhu-Sahil/mango-tracking-sys)

<!--THE END-->

- Raft Implementation
- - The GitHub repository you're referring to likely involves the implementation of the Raft consensus algorithm. Raft is a distributed consensus algorithm that ensures the consistency of a replicated log in a distributed system. This repository could provide valuable insights into how Raft is implemented and utilized within the context of distributed systems and consensus algorithms.
  - - [https://github.com/Sandhu-Sahil/raft-implementation](https://github.com/Sandhu-Sahil/raft-implementation)
    - ![](attachments/20293751/20295457.png?height=250)

## Attachments:

![](images/icons/bullet_blue.gif) [Screenshot from 2023-08-30 21-50-43.png](attachments/20293751/20295457.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
