1. [Hyperledger Cacti](index.html)

# ![Home Page](images/icons/contenttypes/home_page_16.png) Hyperledger Cacti : Hyperledger Cacti Home

Created by Ry Jones, last modified by Jennifer Bell on Jun 26, 2024

  **Project**

**Status**

 [GRADUATED](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Project+Lifecycle#ProjectLifecycle-incubation) 

**CII Badge**

[![](https://bestpractices.coreinfrastructure.org/projects/4089/badge)](https://bestpractices.coreinfrastructure.org/projects/4089)

**Description**

Hyperledger Cacti is a plugin-based framework which aims to provide developers with an abstraction over protocol specific implementations and enabling interoperability.  

This enables solutions to adapt to new protocols and make transactions involving multiple public and/or permissioned ledgers more easily. 

# Key Characteristics

#### **What is Hyperledger Cacti?**

#### Cacti is a **pluggable enterprise-grade** **framework to transact on multiple distributed ledgers** without introducing yet another competing blockchain. An SDK of SDKs

Cacti aims to provide Decentralized, Adaptable and Secure Integration to and between Blockchain Networks. It's aims to cover as many protocols as possible through  
an **extensible plugin architecture** where new protocols or functionality can be added by creating new plugins.

#### **Why should I use Cacti?**

- To a**ddress blockchain** **fragmentation**; Allow developers to connect and perform transactions across different blockchain networks.
- **Save** (distributed) app developers **from re-inventing** **the wheel**; Simplify secure interactions with blockchain nodes using a standardized interface across protocols.
- **Lower risk of adopting blockchain** by businesses; Abstract your app layer from the blockchain protocol, allowing developers to easily change the blockchain
  
  protocol being used and reducing risks of your app being obsolete.
  

#### **What are Cacti Design principles?**

- **Key principles:** 
  
  - Plugin architecture: Maximize **flexibility** and **future-proofing** through plug-in architecture
  - Secure by Default: Avoid needing explicit action from users to have a **secure Cacti deployment**.
  - Toll Free: **Users** should not be required to use tokens for transactions &amp; **Operators** should not be required to take a cut of individual transactions
  - Low Impact Deployment: Do not interfere with or impede **existing** network requirements
- **Additional principles:**
  
  - Wide Support: Support as many blockchain protocols as possible, and constantly support new ones.
  - Prevent Double Spending: Whenever two networks are interacting with each other ensure that there is no double spend whenever possible.
  - Preserving Ledger Features: Using Cacti should allow you to use all the features which the protocol enables.
  - Horizontal Scalability: Cacti should never be the bottleneck of all the networks involved. IE: If 2 networks can do 100tps, Cacti should be able to handle 200

#### **What are Cacti current features?**

- **Connectors** for different blockchain protocols
  
  - Hyperledger Besu, Hyperledger Fabric, (WIP for Corda, Geth, and Quorum)
- **Atomic transfers** across legers
  
  - HTLCs for Ether, ERC20 (WIP Fabtoken)
- **Decoupled identity**
  
  - JWT, (WIP OpenAPI)
- **Metrics** 
  
  - Prometheus and Grafana based monitoring of the individual plugins

#### **How can I collaborate?**

To see a guide on how to use Hyperledger Cacti, take a look at the links below in the Documentation section. Keep in mind that this is currently being updated so please write us through the different means listed in the Communication section.

If you want to collaborate in Cacti' development, you can pick an issue directly from Github – we've linked to some good first issues below that are good places to start for new contributors. If you need extra guidance, contact us through the chat or join one of our meetings and we can help you.

Hyperledger Cacti is currently undergoing a major refactoring effort to enable the desired to-be architecture which will enable plug-in based collaborative development to increase the breadth of use cases &amp; Ledgers supported.

For a better understanding of where Hyperledger Cacti is heading please see the Whitepaper and Design Principles below!

# Documentation

- [Whitepaper](https://github.com/hyperledger/cactus/blob/master/whitepaper/whitepaper.md)
- [Original Design Principles Google Doc](https://docs.google.com/document/d/1oCF7q_or7EWlVEmCMYuGU3ksKrNjHf07pSTrviRfktk/edit)

# Project Management

[Hyperledger Cacti uses GitHub Issues to track work items.](https://github.com/hyperledger/cactus/issues)

# Repositories

Hyperledger Cacti uses GitHub for source code control.

- [Main repo](https://github.com/hyperledger/cactus)

# History

- [Approved by the TSC on 30 APR 2020](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Move+the+Blockchain+Integration+Framework+%28BIF%29+lab+to+a+Project)
- [Proposal the TSC voted on](https://lf-hyperledger.atlassian.net/wiki/download/attachments/21439256/Blockchain%20Integration%20Framework%20Proposal.pdf?version=1&modificationDate=1589393460757&api=v2)

# Getting Involved

You are invited to get involved with the Cacti project.  Here are some ways you can get started.

1. Join one of our pair programming calls
   
   1. [North America Morning/Europe Evening](https://lists.hyperledger.org/g/cactus/calendar)
   2. [Asia-Pacific Morning/Europe Morning](https://lists.hyperledger.org/g/cactus/calendar)
2. Instructions on [building Cacti](https://github.com/hyperledger/cactus/blob/main/BUILD.md) (the framework itself)
3. Join communication channels and introduce yourself and ask questions (details below)
4. Grab a good first issue based on your level of experience/technical area(s) of expertise or interests:
   
   1. All [Good First Issues](https://github.com/hyperledger/cactus/labels/good-first-issue)
   2. [Climate Action SIG Specific Good First Issues](https://github.com/hyperledger/cactus/labels/GFI_Climate_Action_SIG)
   3. [Level 100 - Introductory Good First Issues](https://github.com/hyperledger/cactus/labels/good-first-issue-100-introductory)
   4. [Level 200 - Intermediate Good First Issues](https://github.com/hyperledger/cactus/labels/good-first-issue-200-intermediate)
   5. [Level 300 - Advanced Good First Issues](https://github.com/hyperledger/cactus/labels/good-first-issue-300-advanced)
   6. [Level 400 - Expert Good First Issues](https://github.com/hyperledger/cactus/labels/good-first-issue-400-expert)

# Documentation

- [Cacti documentation](https://hyperledger.github.io/cacti/)

# Communication

## Mailing List

- [cactus@lists.hyperledger.org](mailto:cactus@lists.hyperledger.org)
  
  - [subscribe](https://lists.hyperledger.org/g/cactus)
  - [messages](https://lists.hyperledger.org/g/cactus/topics)

## Chat (for questions and ephemeral discussions)

Questions are welcome and best asked in Hyperledger Discord.  [Learn more about Hyperledger Discord here](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Our+chat+service), get the invite and check out one of the many Cacti project channels.  

# Meetings

[https://lists.hyperledger.org/g/cactus/calendar](https://lists.hyperledger.org/g/cactus/calendar)

[Calendar of Public Meetings](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595324/Calendar+of+Public+Meetings)

## Recent space activity

- [![](null/aa-avatar/557058:54be3a11-ffe8-43a5-b37d-c854a0aa21c3 "557058:54be3a11-ffe8-43a5-b37d-c854a0aa21c3")](null/display/~557058%3A54be3a11-ffe8-43a5-b37d-c854a0aa21c3)
  
  - [Peter Somogyvari](null/display/~557058%3A54be3a11-ffe8-43a5-b37d-c854a0aa21c3)
  - [2024-11-21 Cacti Maintainers Agenda](2024-11-21-Cacti-Maintainers-Agenda_53674097.html "data-linked-resource-id=") contributed Nov 14, 2024
  - [2024-11-14 Cacti Maintainers Agenda](2024-11-14-Cacti-Maintainers-Agenda_53182704.html "data-linked-resource-id=") contributed Nov 14, 2024
  - [2024-11-07 Cacti Maintainers Agenda](2024-11-07-Cacti-Maintainers-Agenda_48758836.html "data-linked-resource-id=") contributed Nov 07, 2024
  - [2024-10-31 Cacti Maintainers Agenda](2024-10-31-Cacti-Maintainers-Agenda_43286650.html "data-linked-resource-id=") contributed Oct 31, 2024
  - [2024-10-17 Cacti Maintainers Agenda](2024-10-17-Cacti-Maintainers-Agenda_33030223.html "data-linked-resource-id=") contributed Oct 16, 2024

[Show More](/wiki/plugins/recently-updated/changes.action?theme=social&pageSize=5&startIndex=5&searchToken=1&spaceKeys=cactus&contentType=page%2C%20comment%2C%20blogpost&cursor=_f_NQ%3D%3D_sa_WzE3MjkwOTU3NzQwMDAsIlx0MzMwMzAyMjMgb1o1UF1BUD5nJ1peYFxcV21nb3RXIGNwIl0%3D) ![Please wait](images/icons/wait.gif)

## Space contributors

- [Peter Somogyvari](/wiki/display/~557058%3A54be3a11-ffe8-43a5-b37d-c854a0aa21c3) (11 days ago)

## Attachments:

![](images/icons/bullet_blue.gif) [cactus.png](attachments/20414469/20414499.png) (image/png)  
![](images/icons/bullet_blue.gif) [coverphoto.png](attachments/20414469/20415529.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Cacti.png](attachments/20414469/20415774.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Cacti.svg](attachments/20414469/20415776.svg) (image/svg+xml)

Document generated by Confluence on Nov 26, 2024 12:37

[Atlassian](http://www.atlassian.com/)
