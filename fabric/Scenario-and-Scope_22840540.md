1. [Hyperledger Fabric](index.html)
2. [Archives](Archives_22840389.html)
3. [Fabric Interop Working Group](Fabric-Interop-Working-Group_22839518.html)
4. [Interop Documents](Interop-Documents_22839726.html)

# Hyperledger Fabric : Scenario and Scope

Created by Brian Brian, last modified by Tong Li on Mar 20, 2019

# Abstract

This document represents the current effort of the Hyperledger Fabric community to specify and standardize an interoperability workflow that allows organizations hosted on different cloud vendors to establish and join business networks independent from the infrastructure where the ordering services are hosted. To archive this, this document lays out the necessary configuration artifacts that need to be provided by the joining organization, the high-level message flow and a chaincode based voting mechanism to approve or reject channel join requests. Furthermore, this proposal should be fully compatible with Hyperledger Fabric 1.4 LTS.

# Scenario Description

The scope for the Fabric interoperability group is initially limited to a defined scenario.

*In this scenario the working group defines the technical aspect of the interoperability, in another word, it is the process from programming aspect what actions organizations should take to add an organization into an existing fabric network channel. During the process, an organization already in the network may decide to approve or disprove the new organization's request, the decision is solely up to the representative of that organization based on their business considerations. The process this working group defines does not in any way determines that decision.*

![](attachments/22840540/22840551.png?height=250)

We assume that there already exists a Fabric channel relative to an ordering service. Attached to this channel can be any number of Fabric peer nodes. It is assumed for the discussion that each Fabric peer node has been provisioned by a (cloud) vendor in the name of the customer/organization. In a simpler variation, any organization can also be their own “vendor”.

Important: in this scenario there exists two levels of interconnection. At the business level, we have typically a business network, which is agreed between any number of organizations and governed by the business network rules and regulations. The second interconnected entity is the actual Fabric channel that spans the different Fabric nodes. It is NOT expected that any vendor will be part of the business network.

Integration story: OrgX, having provisioned a Fabric peer node with its preferred vendor, wishes to join its Fabric peer node into the business network Fabric channel.

## Assumed

- In general, all Fabric peers and orderers can be accessed using public DNS and public IP addresses.
- This proposal targets to be fully compatible with Hyperledger Fabric 1.4 LTS since that it is expected to be widely adopted over a long period of time.
- That orgX has an agreement with vendorX for the provisioning of a Fabric peer node. (Note that in all simplified scenarios orgX can be equal to vendorX and do their own provisioning.)
- Initially neither orgX, nor vendorX, has access to the existing Fabric channel.
- VendorX, not been part of the business network, does NOT have the mandate to interact with the business network (in the name of orgX). All interaction with the business network (the business entity) must be between ogrX and any/all parties of the business network (here organizations A,B&amp;C). No vendor is involved in this business interaction.
- A business agreement between orgX and the business network is reached before a technical interoperability is established.

## Out of Scope

- Interaction model between any organization and vendor. It is accepted that each vendor will have its own (cloud based) Fabric offering and will provide its customers/organizations a rich UI and process steps to complete all relevant actions, or require that organizations complete relevant actions via the Fabric SDK.
- The interaction between the organizations within the business network. It is used some form of interaction model is defined, for example via emails, faxes, websites or predefined APIs. For orgX to join the business network, it will require some form of interaction paradigm with other business network members.

## In Scope

- The artifacts that orgX must exchange with any/all organizations within the business network to enable the technical interoperability. This will include a definite description of all relevant artifacts that must be supplied (for example certificates, TCP/IP interconnectivity information, etc) and the format in which these artifacts must be encoded in for transport (JSON, protobuf, etc).
- Also, in scope is the definition of predefined “management” chaincode that can be used by business network members to facilitate the steps required by the business network to agree and execute the technical Fabric peer node join request. Note: this “management” chaincode is effectively business network “business” and could be enhanced by the business network to contain additional business logic. The Fabric interoperability working group can define and deliver an example of such a “management” chaincode. What is NOT defined, is how the business network interacts with the management chaincode, whether this is managed and done by the different organizations within the business network directly, or whether any vendor takes over part of this operation aspects.

Footnote: Optional, it should be considered to define (a subset of) chaincode functions which are standardized as mandatory, so as to enable a more homogenous management of business networks by either organizations and/or vendors.

## Approach

- KISS: The goal of the interoperability working group is to attempt to define a possible solution that uses existing Fabric technology without any additional development as far as possible.

## Expected Interaction Model

- OrgX interacts with the business network (any/all members) and reach a business agreement to join the business network.
- OrgX interacts with VendorX to obtain the defined artifacts encoded in the defined format for the interoperability.
- OrgX interacts with the business network (visualized above as the blue arrow between orgX and orgA) to transfer the artifacts to the business network (“join request”).
- The business network (organizations A,B&amp;C) interacts with their relevant vendors (A,B&amp;C) and/or the “management” chaincode (visualized in blue above) to complete the relevant technical steps to enable the interoperability.
- The business network returns to orgX defined artifacts in the defined format (“join response”).
- OrgX (possibly with the help of vendorX), based on the returned artifacts, joins the Fabric channel.

## Attachments:

![](images/icons/bullet_blue.gif) [image2019-2-1\_14-8-41.png](attachments/22840540/22840550.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-2-1\_14-10-2.png](attachments/22840540/22840551.png) (image/png)

Document generated by Confluence on Nov 26, 2024 16:22

[Atlassian](http://www.atlassian.com/)
