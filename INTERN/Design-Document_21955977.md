1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2019 Projects](2019-Projects_21954613.html)
5. [﻿IoT and DLT in a telecom multi carriers architecture](21955764.html)

# Hyperledger Mentorship Program : Design Document

Created by Nachiket tapas, last modified by Zicheng Wang on Jan 17, 2020

# Creating Device Identity using Hyperledger Indy

Date

2019.06

Laura Spinaci ([lauraspinaci.biz@hotmail.com](mailto:lauraspinaci.biz@hotmail.com)) (Mentor)

## Introduction

Identity is the genesis of any operation of an IoT device. Without the device identification, the management and interoperability of IoT devices is not possible. In addition, the distributed nature of IoT makes centralized IoT solutions irrelevant. DLT architecture is a perfect fit for creating identity for IoT devices which are self governed. This gives devices and users of the system a complete control over their identities, at the same time enabled secure interaction between any two entities. Hyperledger Indy provides a self sovereign identity ecosystem based on DLT technology enabling secure and verifiable trust. 

## Motivation

- Identity is the first step for a lot of other IoT operations like access control, remote operation, etc. Currently most of the access control systems are either centralized or do not scale well.
- With the identity of a device known, the vision of autonomous IoT device functioning becomes much more realizable.
- The tracking of the device status during the supply chain provides critical management insights to the organization.

## Goal

To create an identity system for IoT devices and involved actors, thereby, laying the foundation for application to various IoT use cases. In particular, we focus on the identity access, identity association with id, monitor the supply chain. Further extending the system potentially in the future to enable device-to-device interaction enabling autonomous service exposure and consumption.

## Assumption

GSMA’s DLT vision document outlines identity of IoT devices and access control as the foundation use case for IoT. We assume that the POC resulting from the present work will act as a foundation work for the rest of their use cases like those related to supply chain, data sharing and integrity.

## Design Details

## The general architecture of the solution will be as follows:

 For our POC we will create a network with dummy organizations. Once the initial roles are created, with each step of the supply chain, creation of series of identities will occur. Consider the following steps:

![](attachments/21955977/21963134.png?height=250)

From the use case:

Device status is a particularly important attribute of the device because this is very difficult to trust at present especially when buying from less official channels. Device status can contain multiple attributes and permissions to add/ update attributes may differ according to the user role e.g.

○ only a manufacturer can allocate a serial number,

○ only the manufacturer QA team can mark a device as having passed QA,

○ only the manufacturer can change the ownership of the device to a

distributor,

○ only a distributor can only a Mobile Network Operator can allocate an MSISDN;

Detail Steps:

1. Schema Creation, Credential Definition Creation. 
   
   1. Distributor (Mobile Network Operator)  with create schema (Telecom Schema) as standard in the entire supply chain. Both Producer (Manufacturer, called pineapple in our demo) and QA team ( is the QA team of the Manufacturer) will together create Credential Definition.
   2. To simplify the reality, in the use case, the Manufacturer is a different entity compare to MNO (although could be the same some times). Also usually you have several distributors in this case GSMA, assumed only one to make it easier.
2. Device Creation
   
   1. Once the device is created, the corresponding identity (DID Documents) of the device will be created. The device will be treated as an independent thing and receive the credential from Producer. The device shall  shall be assigned the series number from manufacturer.
3. QA Testing
   
   1. The device will be passed through QA testing. In the demo, assume passing the QA.
   2. After QA pass, manufacturer will offer a Credential Offer for the device. The device shall receive the Credential from manufacturer. (currently, our credential including: manufacturer, sequence\_id, bandwidth, QA\_status, history = null)
4. Passing device through Distributor
   
   1. After receiving Credential from Producer and QA Team, the Distributor (Mobile Network Operator) will assigned and MSISDN in DID Documents of device. After that, the device can connect to the internet.

We simply use the DID to mark the ownership and access control. The KYC process and recycling process are not taken into consideration currently. The changing of ownership from manufacturer to operator, and from operator to end user is use the revoke of DID and claim new DID.

**Network:** The network will be designed with 3 organizations (Distributor, Producer, QA Team) with 3 peers (User, device A, device B) and will form a consensus among themselves. The DID documents and Verkeys will control the transactions being accepted into the network. 

**DID and Verkey:** DIDs work as the role of trust anchor to the ledger, as we create Steward’s DID. The actions (including owner’s action and manufacturer's action) is written on the ledger, generate new DID/Verkey pairs. After that, Prover uses Credential Offer to create Credential Request. Trust Anchor then uses Prover's Credential Request to issue a Credential. Steward is then responsible of creating other actors like manufacturer (production line), QA team, distributor (mobile operator) and end customer at various stages. For all the actors, the Steward will onboarding actors mentioned above and then grant verinym and a trust anchor role.

## Implementation

[https://github.com/quantumcatwang/Telecom-IoT-device-SSI](https://github.com/quantumcatwang/Telecom-IoT-device-SSI)

## Attachments:

![](images/icons/bullet_blue.gif) [Broad Architecture.jpg](attachments/21955977/21962774.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [image2019-10-19\_20-41-16.png](attachments/21955977/21963134.png) (image/png)

Document generated by Confluence on Nov 26, 2024 14:59

[Atlassian](http://www.atlassian.com/)
