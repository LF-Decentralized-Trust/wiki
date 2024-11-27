1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [Implement cross chain contract invocation using ServiceMesh way](Implement-cross-chain-contract-invocation-using-ServiceMesh-way_21956839.html)

# Hyperledger Mentorship Program : Project Plan - Implement cross chain contract invocation using 'ServiceMesh' way

Created by Shritesh Jamulkar, last modified on Nov 16, 2021

## **Abstract**

The aim of the project is to implement cross chain contract interoperability between Hyperledger Fabric and Hyperledger Besu in the 'ServiceMesh' way. The project is implemented using an extended on-chain contract development kit as a 'SideCar’ and a stateless off-chain relay. The contract is implemented with an on-chain lock protocol which provides a two phase commit mechanism to guarantee cross chain transaction atomicity.

**Design doc:**

**![](plugins/servlet/confluence/placeholder/unknown-macro)**

## **Mentor and Mentee**

Mentor

Mentor

Mentee

Kai Chen

GMT+8

[281165273grape@gmail.com](mailto:281165273grape@gmail.com)

rocketchat: grapebaba

Zehn Peng

[pengzhen9278@gmail.com](mailto:pengzhen9278@gmail.com)

Shritesh Jamulkar

IST

[shritesh.sj@gmail.com](mailto:shritesh.sj@gmail.com)

rocketchat: Shritesh99

Communication channel: Email + Github + Chat + Weekly meetings over Google Meet

**Project repository(s):** 

- ChainMesh org: [https://github.com/Chain-Mesh](https://github.com/Chain-Mesh)
- Sidemesh Library: [https://github.com/Shritesh99/sidemesh-solidity](https://github.com/Shritesh99/sidemesh-solidity)
- Mesher Library: [https://github.com/Shritesh99/Mesher-Solidity](https://github.com/Shritesh99/Mesher-Solidity)
- Sample Implementation: [https://github.com/Shritesh99/samples/tree/besu2fabric](https://github.com/Shritesh99/samples/tree/besu2fabric)

## **Deliverables**

- 1. **SideMesh Component:** It contains a set of transaction lifecycle interfaces and a set of lock manager interfaces.
- 2. **Mesher Component:** It is an off-chain service for monitoring events and orchestrating transactions between different blockchains.
- 3\. Sample network with Solidity based Smart Contract Interoperability with Hyperledger Besu and Hyperledger Fabric.

## **Milestones**

**Eval 1:**

- a. A new design document with a new sidemesh transaction lifecycle.
- b. Sample network-scripts for BESU.

**Eval 2:**

- c.  Working Sidemesh component.

**Eval 3:**

- e. Working Mesher component.

**Eval 4:**

- g. Working Fabric and BESU cross chain invocation.

## **Timeline**

Week

Task/Plan

Status

**May 24 - May 28**Familiar with the design document on a google doc and current code repository.**May 31 - June 11**Run the current code sample and understand the sample.**June 14 - June 25**Understand the sidemesh component and investigate BESU sodility.**June 28 - July 2**Refactor sidemesh transaction lifecycle event data structure and generate new design doc.**July 5 - July 9**

Provide a new design document.

Eval 1

**July 12 - July 23**Follow the design doc to implement sidemesh in the BESU blockchain.**July 26 - August 6**Follow the design doc to implement sidemesh in the BESU blockchain.**August 9 - August 13**Follow the design doc to implement sidemesh in the BESU blockchain.**August 16 - August 27**

Finish BESU blockchain sidemesh component.

Eval 2

**August 30 - Sept 3**Follow the design doc implement mesher in BESU blockchain**Sept 6 - Sept 17**Follow the design doc implement mesher in BESU blockchain**Sept 20 - 24**

Follow the design doc implement mesher in BESU blockchain

**Sept 27 - Oct 1**

Finish BESU blockchain mesher component.

Eval 3

**Oct 4 - Oct 15**

Refine sidemesh component following the new design.

**Oct 18 - Oct 29**

Refine mesher component following the new design.

**Nov 1 - Nov 5**Make Fabric and BESU cross chain invocation work.**Nov 8 - Nov 12**

Eval 4

Final evaluation and presentation of the project.

## **Explanation**

The project aims to achieve cross chain contract interoperability between Hyperlegder Fabric and Hyperledger BESU in a loosely coupled architecture. Hence, an on-chain lock protocol that provides a two phase commit mechanism is required to guarantee cross chain transaction atomicity. The project consists of two main components which are as follows. 

- **SideMesh Component:** It includes a set of transaction lifecycle interfaces and a set of lock manager interfaces which is extended by cross chain contracts. Every cross chain contract on the network exposes three functions which are prepare, confirm, and queryGlobalStatus. Prepare and confirm functions are used for two phase commit protocol, while queryGlobalStatus function provides a unified entrance for querying global transaction final status.
- **Mesher Component:** It is the off-chain service that follows an event-driven architecture for monitoring events and orchestrating transactions between different blockchains. Every blockchain network needs to deploy a Mesher service that delegates the cross chain transaction lifecycle management off-chain.

A more detailed explanation of transaction flow and architecture is given in the design doc. 

## **Methodology**

- Quarterly review and evaluations based on the project timeline.
- Communication and Updates:
  
  - Emails
  - Chat
  - Weekly meetings over Google Meet on Mondays
  - Github + Github Projects
- Documentation:
  
  - Simultaneous documentation for each component.
  - New design document before Eval 1.

## **Final Presentation**

**[![](attachments/thumbnails/21957509/21965998)](attachments/21957509/21965998.pptx)**

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation - Nov2021.pptx](attachments/21957509/21965998.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)

Document generated by Confluence on Nov 26, 2024 14:57

[Atlassian](http://www.atlassian.com/)
