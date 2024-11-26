1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Archived](Archived_21447696.html)
4. [Project Proposals](Project-Proposals_21430788.html)
5. [2020 Finished Proposals](2020-Finished-Proposals_21430790.html)

# Technical Oversight Committee : No-Code Development Platform For Blockchain and EAI

Created by Tim OBrien, last modified by Nathan George on Jun 11, 2020

# Project Identifier

LCDP- -00001

Sponsor(s)

Tim O'Brien  Tim.n.obrien@outlook.com

# Abstract

Overture is a No-Code Development Platform (NCDP) that has been under research and development for 2 years. Overture allows users to create programs, including  Ethereum smart contracts and Fabric chaincode using a  drag-and-drop visual  languages.  Contracts can be deployed directly from the platform to Ethereum, Hyperledger Fabric or any EVM based blockchain. Before a contract is deployed it undergoes a rigorous formal verification process using state of the art formal methodologies . Our technology uses several never before seen inventions that allow us to add never before seen capability to blockchain including the ability make the cost of running a process on blockchain independent of the   complexity of the process and the ability to use advanced for  Our roadmap includes using Reinforcement Learning and providing integration with Apache Camel and Spring integration to achieve our vision of allowing companies to transparently add blockchain capabilities-Trustlessness and Transparency - to business processes with minimum blockchain knowledge or skills requirements.  Our roadmap also includes performance tuning our application an deploying to kubernetes cloud. 

Watch the video of Overture below. 

 

# Context

We can fill the void left by the departure of Hyperledger Composer. 

# Dependent Projects

None

# Motivation

our product removes the risk of starting a blockchain project 

# Status

We are GA with our product and have designed for a follow up version. 

Solution

Overture is a No-Code Application Development platform that lets you build smart contracts and other applications using a drag and drop interface (see video). Once built smart contracts can be  deployed from our platform to  Hyperledger, Ethereum or any blockchain that supports the EVM. Overture can be used to (1) integrate blockchain with enterprise back office systems using  industry best practices including integration design patterns and tested connectors; (2)  supports a multi-view architecture that encourages collaboration between business and IT by allowing each user, business, power user, and engineer to select a visual language that fits their need for a balance of capability and abstraction.; (3) de-risks blockchain projects by reducing the number of moving parts and providing realtime in-platform pre-deployment formal verification. (4) Supports the use of blockchain in mission critical applications by using powerful formal verification and emulation techniques (5) supports mapping complex business processes into blockchain including Ethereum and EVM based blockchains,  

Overture is a deployed as a  SAAS based No-Code Development Platform (NCDP)  for supporting enterprises with digital transformation. NCDPs are becoming popular in enterprise development with Gartner projecting 65% of software being developed with NDCP by 2024.   

The logical diagram in figure 1 describes the layers in our stack. 

1. Interface layer with public facing web and mobile interface and a public facing REST based API.
2. A set of persona targeted languages with synthesizers that translate the languages   instruction sets that supply the control logic of a program.
3. A set of 370+ adapters and components that implement the 65 integration patterns documented in the book by Bob Woolf [website.](https://www.enterpriseintegrationpatterns.com/patterns/messaging/)
4. A set of programs (standalone or  smart contracts) that know how to interpret our control logic instructions set.

![](attachments/21438826/21450519.png?width=1000)

Overture Design Studio is a SAAS based cloud application that supports (i) creation of programming  logic using visual language; (ii) creation of a specification, (iii) testing the design against the specification (iv) persisting the models to a database for storage and deployment(v) Synthesizing the models into a compact mathematical  based format.

# ![](attachments/21438826/21450520.png?width=1000)

# How To

We can provide you with a link to the application used in the demo below for verification.  The application  installs as a NodeJS application and can be configured to use any number of blockchains.

  References

# Closure

We have a working product now (see video in Solution section).  We think we would be a valuable addition to the Hyperledger product line and an excellent progression from Hyperledger Composer. 

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Christopher Ferris](https://lf-hyperledger.atlassian.net/wiki/people/5abb903a8724022aa9070581?ref=confluence)
- [Dan Middleton](https://lf-hyperledger.atlassian.net/wiki/people/712020:2979764a-3998-4ef1-8810-60b799067924?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Swetha Repakula](https://lf-hyperledger.atlassian.net/wiki/people/712020:7153872d-7890-4ca8-a633-d87fdf1e9a8d?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:62746046-52ae-43bb-827b-6dfdde9f07d7?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

## Attachments:

![](images/icons/bullet_blue.gif) [LogicalArchitecture.png](attachments/21438826/21450512.png) (image/png)  
![](images/icons/bullet_blue.gif) [Logical-Diagram.png](attachments/21438826/21450513.png) (image/png)  
![](images/icons/bullet_blue.gif) [overview.png](attachments/21438826/21450514.png) (image/png)  
![](images/icons/bullet_blue.gif) [Logical.png](attachments/21438826/21450519.png) (image/png)  
![](images/icons/bullet_blue.gif) [Description.png](attachments/21438826/21450520.png) (image/png)

Document generated by Confluence on Nov 26, 2024 11:24

[Atlassian](http://www.atlassian.com/)
