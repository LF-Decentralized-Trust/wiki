1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2019 Projects](2019-Projects_21954613.html)

# Hyperledger Mentorship Program : Hyperledger Fabric Based Access Control

Created by Rafael Belchior, last modified by Sara Rouhani on Jun 08, 2020

**Title***Hyperledger Fabric Based Access Control***Status**

PROJECT COMPLETED

**Difficulty**

HIGH  

# Description

Access control systems exist to protect resources from unauthorized accesses. Auditability plays an important role and has its importance increased when it comes to public and private administration, and can be leveraged within a blockchain-based access control system. Hyperledger Fabric will leverage a solution that aims to discourage unauthorized accesses to confidential information while decentralizing trust when it comes to access control. This work will not only be focused on the implementation of such Proof-Of-Concept but also leveraging effective techniques to its provisioning and deployment.

Building such a system based on the blockchain technology is challenging. Distributed ledger technologies are indeed a complex distributed system. Concerning blockchain access control, there are two main challenges:

1\) Provisioning, especially for scenarios with requirements on permissions, data privacy, and security.

2\) Lack of standardized processes for development and operations, i.e., continuous integration, continuous deployment and continous improvement.

The internship aims to:

1. Contribute to the open-source community, by advancing the state-of-the-art on the access control using the blockchain
2. Create a blockchain-based access control system using Hyperledger Fabric
3. Develop an efficient, practical DevOps framework to provision and deploy the created system
4. If time suffices, propose alterations to Fabric in order to facilitate the creation of such system (i.e., creating a tutorial, scripts)
5. If time suffices, develop a small web application to help visualize the solution
   

Although this project solves real-world problem, it will also be research-focused. The goal is to give a contribution in the state of the art of blockchain-based access control with Hyperledger Fabric.

# Additional Information

[https://www.hyperledger.org/projects/fabric](https://www.hyperledger.org/projects/fabric) - Fabric's overview

**Some relevant papers:**

[https://pdfs.semanticscholar.org/6192/f0308dc8d7782b55a0557dfb66f323638853.pdf](https://pdfs.semanticscholar.org/6192/f0308dc8d7782b55a0557dfb66f323638853.pdf)

[https://www.researchgate.net/publication/330468939\_Blockchain\_Based\_Access\_Control\_Services](https://www.researchgate.net/publication/330468939_Blockchain_Based_Access_Control_Services)

**Relevant technologies:**

1. **Hyperledger Fabric**
2. MEAN stack (MongoDB, Express, Angular, NodeJS)
3. Docker and Kubernetes

# Learning Objectives

- You will learn about Hyperledger Fabric and general concepts about blockchain.
- You will learn how to program chaincode using Javascript.
- You will learn how to research a topic like a researcher.
- You will learn how to contribute (and lead) an open source project, document your work and create tests.
- You will learn about access control paradigms - and its application with regard to the distributed ledger technologies.
- You will learn how to implement security, privacy and access control features in distributed systems.
- You will have the opportunity to experience first hand of what is to research a topic and apply knowledge gathered from the research
- You will learn DevOps practices and DevOps practices applied to distributed ledger technologies.
- You will learn how all the pieces work as a whole, by developing a small web app, that serves as the client of the system developed (along with a frontend)

# Expected Outcome

1. Contribute to the **open-source community**, by a**dvancing the state-of-the-art on the access control using blockchain**
2. Create a **blockchain-based access control system using Hyperledger Fabric**
3. Develop an efficient, practical **DevOps framework to provision and deploy the created system**
4. If time suffices, write an **academic paper** with the work developed
5. If time suffices, develop a **simple web application** to help visualize the solution

# Relation to Hyperledger

Hyperledger Fabric

# Education Level

Any level is applicable, undergraduate or masters student. Experience in research is preferred, but not mandatory.

# Skills

**Desirable Skills:**

- Experience in programming with Javascript (NodeJs)
- Knowledge about Hyperledger Fabric's architecture
- Basic knowledge of chaincode programming
- Basic understanding of general blockchain concepts
- Basic understanding of access control concepts
- Ability to modela system/architecture, under the mentors' supervision
  

**Bonus:**

- You have some experience in scientific research (if you don't, no worries - we can help)
- You are familiarized with the MEAN stack or other web stacks.
- You are familiarized with Docker, Kubernetes or other deployment tools
- You understand in depth Fabric's architecture

# Future plans

The end of the internship does not need to mean an end to collaboration. The ideal goal is to build a blockchain based access control system capable of others to use. On top of that, an academic paper might be written as the sum of the knowledge learned.

# Preferred Hours and Length of Internship

Both Full-time or Part-time are possible options. Full-time is preferred. 

# Mentor(s) Names and Contact Info

Rafael Belchior, Teaching Assistant at Instituto Superior Técnico, Universidade de Lisboa: [rafael.belchior@tecnico.ulisboa.pt](mailto:rafael.belchior@tecnico.ulisboa.pt)

Rui Cruz,  Ph.D., *Senior Member IEEE*, Assistant Professor at Instituto Superior Técnico, Universidade de Lisboa: [rui.cruz@ieee.org](mailto:rui.cruz@ieee.org), [rui.s.cruz@tecnico.ulisboa.pt](mailto:rui.s.cruz@tecnico.ulisboa.pt)

# Mentee

[sara.rouhani@usask.ca](mailto:sara.rouhani@usask.ca)

[Sara Rouhani](https://lf-hyperledger.atlassian.net/wiki/people/5cfffbbea315460bc8468abc?ref=confluence)

# Project Deliveries:

- Designing the system architecture and application components

Choose the tools for implementing the attribute-based access control model

Design system architecture and initial model

- Deliverable: System Architecture Design Document

<!--THE END-->

- Configuring Hypereldger Fabric 1.4 based on the project application

<!--THE END-->

- Deliverable: configuration code for HF 1.4

<!--THE END-->

- Implementing Chaincodes/ smart contracts based on attribute-based access control components

Implementing the chaincodes, which are responsible for storing subject and objects attributes

Implement chainCode that record policies on blockchain

Implement PDP chainCode, which is a chainCode that evaluates requests and checks requests access permissions (Policy Decision Point)

Implement tests for chainCode

- Deliverable: Application ChainCodes and smart contracts

<!--THE END-->

- Testing and analyzing system based on a designed case study

Defining a case study and defining attributes and policies based on the case study

Evaluating the implemented system based on designed case study

- Deliverable: Test results and Documentation

<!--THE END-->

- Writing an academic paper based on system design, implementation, and analysis

Outline the paper

Writing the paper based on system features and capabilities

- Deliverable: Academic paper

<!--THE END-->

- Throughout the documentation, including:

<!--THE END-->

- Project Wiki
- Presentation slides
- Demo video

# Project milestones:

## First Quarter:

- Project kick-off, discuss project steps, investigate the required tools and components of the project, design project objectives, milestones, and planning the project (June 14)
- Hyperledger Fabric 1.4 network configuration and running, design system architecture and components using ArchiMate (July 5th)
- ChainCodes/ Smart contracts implementation for attribute and policy recording (July 18th)
- 1st Evaluation and report (July 18th)

## Second Quarter:

- ChainCodes/ Smart contracts implementation for access control evaluation (PDP) (August 2nd)
- Define a case study to implement for evaluating the system (August 4th)
- Implementing the case study and application API for sending requests to the blockchain applications and receiving responses from it. (August 30th)
- 2nd Evaluation and report (August 29th)

## Third Quarter:

- Testing the system (September 12th)
- Analyzing the result (September 22th)
- Investigating the possibility to present a project as a module for Hyperledger Fabric (October 17th)
- 3rd Evaluation and report. (October 17th)

## Final Quarter:

- Drafting the paper outline (October 20th)
- and writing the academic paper (November 5th)
- Completing documentation and project wiki and creating project presentation slides and video tutorial for running the project (November 15th)
- Final Evaluation and report (November 15th)

**Summary reports**

**[![](attachments/thumbnails/21954647/21963200)](attachments/21954647/21963200.pdf)**

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation- 2019-V2.pdf](attachments/21954647/21963200.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 14:59

[Atlassian](http://www.atlassian.com/)
