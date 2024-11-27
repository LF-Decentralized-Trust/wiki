1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)

# Hyperledger Mentorship Program : Implement cross chain contract invocation using ServiceMesh way

Created by GrapeBaba, last modified by Shritesh Jamulkar on Dec 11, 2021

**Project Title**Implement cross chain contract invocation using 'ServiceMesh' way**Status**

COMPLETED

**Difficulty**

MEDIUM  

# Description

Since permissioned blockchain has been adopted widely in various industries, the need to integrate different permissioned blockchains rises up recently. The two core problems of this case are chain contract interoperability and transaction atomic. 

Many frameworks and solutions proposed currently are a bit complex. We introduced a lightweight protocol and reference implementation inspired by the ‘ServiceMesh’ pattern in the microservice integration area. Combine with a stateless off-chain relay and an extended on-chain contract development kit as a ‘SideCar’ for different permissioned blockchains. 

Contract developers can focus on writing business logic since the on-chain contract development kit uses an AOP(aspect-oriented programming) approach to delegate the contract interoperability. In addition it also provides a lock API for locking contract state which can be used in two-phase commit cases. The off-chain relay uses an event based architecture to coordinate different permissioned blockchains.

# Additional Information

Current we already defined a set of chain interoperability lifecycle events and we already have a reference implementation for Hyperledger fabric on-chain contract development kit using Go and off-chain relay which support a Hyperledger fabric plugin. We also have a sample program which demonstrates chain contract interoperability and two-phase commit case through three Hyperledger fabric networks.

The initial design doc at [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/document/d/1ODcQl_JGduqHks0GnPObaI-ZOYX2LLT7C1_v4M0MYJE/edit).

Mesher Repo: [https://github.com/GrapeBaBa/mesher](https://github.com/GrapeBaBa/mesher)

Sidemesh Repo: [https://github.com/GrapeBaBa/sidemesh](https://github.com/GrapeBaBa/sidemesh)

ChainMesh Samples Repo: [https://github.com/GrapeBaBa/crossmesh-samples](https://github.com/GrapeBaBa/crossmesh-samples)(There is a three fabric networks cross chaincode invocation demo)

# Learning Objectives

- Contributing and collaborating in an open-source project.
- Understand the chain contract interoperability in permissioned blockchain integration cases.
- Design and implement chain interoperability lifecycle protocol.
- Understand the contract state locking scheme and two-phase locking protocol.
- Writing good documentations

# Expected Outcome

- Implement the on-chain contract development kit for Hyperledger fabric using JAVA.
- Implement the on-chain contract development kit for Consensys quorum or Hyperledger Besu using Solidity.
- Implement the off-chain relay plugin for Consensys quorum or Hyperledger Besu.

# Relation to Hyperledger

Hyperledger fabric, Hyperledger Besu

# Education Level

Undergraduate or graduated student with developing experience preferred.

# Skills

- Master Go and JAVA programming language
- Familiar with Solidity language
- Understand Hyperledger fabric or Consensys quorum or Hyperledger Besu

# Future plans

Looking forward to contribute this project to Hyperledger community

# Preferred Hours and Length of Internship

Full-time (40 hours a week for 12 weeks during the summer)

# Mentor(s) Names and Contact Info

- [GrapeBaba](https://lf-hyperledger.atlassian.net/wiki/people/70121:9d3e098c-7104-4922-a304-f5a035cd60ad?ref=confluence) , [281165273grape@gmail.com](mailto:281165273grape@gmail.com), rocketchat: grapebaba
- [zhen peng](https://lf-hyperledger.atlassian.net/wiki/people/62ddf7043aaeedcae7558af7?ref=confluence) ,[pengzhen9278@gmail.com](mailto:pengzhen9278@gmail.com)

# Mentee

[Shritesh Jamulkar](https://lf-hyperledger.atlassian.net/wiki/people/5b1558835c1b4f1bc453c590?ref=confluence), National Institute of Technology Raipur

# Project Results

- ChainMesh org: [https://github.com/Chain-Mesh](https://github.com/Chain-Mesh)
- Design Doc: [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/document/d/1ODcQl_JGduqHks0GnPObaI-ZOYX2LLT7C1_v4M0MYJE/edit)
- Wiki: [Project Plan - Implement cross chain contract invocation using 'ServiceMesh' way](Project-Plan---Implement-cross-chain-contract-invocation-using-%27ServiceMesh%27-way_21957509.html)
- Sidemesh Library: [https://github.com/Shritesh99/sidemesh-solidity](https://github.com/Shritesh99/sidemesh-solidity)
- Mesher Library: [https://github.com/Shritesh99/Mesher-Solidity](https://github.com/Shritesh99/Mesher-Solidity)
- Sample Implementation: [https://github.com/Shritesh99/samples/tree/besu2fabric](https://github.com/Shritesh99/samples/tree/besu2fabric)

# Final Report

[![](attachments/thumbnails/21956839/21966128)](attachments/21956839/21966128.pptx)

# Project Presentation Session Recording

[https://youtu.be/6NnrDSr651A](https://youtu.be/6NnrDSr651A)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation - Nov2021.pptx](attachments/21956839/21966128.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)

Document generated by Confluence on Nov 26, 2024 14:57

[Atlassian](http://www.atlassian.com/)
