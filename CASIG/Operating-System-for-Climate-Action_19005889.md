1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Working Groups](Working-Groups_19005701.html)
4. [Carbon Accounting and Certification WG](Carbon-Accounting-and-Certification-WG_19005779.html)

# Climate Action SIG : Operating System for Climate Action

Created by Si Chen, last modified by Andrea Frosinini on Apr 23, 2023

*An operating system like Linux is a set of resources for building applications.  There's a low level tier that connects to hardware and devices, a middle tier of services for building applications, and a user interface tier at the top.  Similarly, blockchain services could be combined to empower climate action:*

### Emissions Data Channels

*This is the first layer of trusted data which is the foundation of all climate action.* 

These are data channels used by auditors to record audited emissions data.  Like the hardware and devices tier of an operating system, these channels store data gathered from the real world and recognized emissions factors.  The data could be audited emissions from emissions auditors, or they could be digital Measurement, Reporting, Verification (MRV) data for verifying Greenhouse Gas (GHG) emissions, reduction, or sequestration.  In both cases, the data could then be used to create tokens. 

The data channel could be implemented with Hyperledger Fabric or stored on IPFS.  For example, the [Supply Chain Decarbonization](Supply-Chain-Decarbonization_19006065.html) takes transportation and shipping data, including flights and tracking numbers and calculates their emissions based on standard emissions factors.  

By following the [Multi Channel Data Architecture](Multi-Channel-Data-Architecture_19006054.html), data from different sources could be stored immutably to improve trust in the integrity of climate and emissions data.    

Click here for a [video of the audited emissions chanel](https://youtu.be/zIYfjF4U2G8).

### Token Networks

*This is the middle layer that gives financial value to climate activities and allow smart contracts to execute transactions and coordinate different parties' actions.*

Once data for emissions and offsets are tokenized, they allow transactions to take place: paying for emissions reductions and offsets with tokens and smart contracts.  These transactions are like the middle tier of services in an operating system.

For example, the [Net Emissions Tokens Network](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Net+Emissions+Tokens+Network) could be deployed on a permissioned Hyperledger Besu or any Ethereum-compatible public network where carbon offsets and renewable energy certificates (REC’s) are traded and retired against audited emissions.  As a “gated” network, only audited emissions, offsets, and REC’s from accepted sources are allowed to transact in this network.  

This network could form the basis of organized climate action at a variety fo scales, from supra-national and national carbon emissions cap and trade to community energy projects to nature-based offset projects. 

Click here for a [video of the emissions token network](https://youtu.be/C-cUjQLDGJw).

#### Distributed Autonomous Organization (DAO)

*This is the user engagement layer that connects the users – consumers, members of the public, monitoring agencies -- with climate action.*

A DAO allows members of a network to vote on governance issues, such as whether to accept certain emissions offsets or auditors, accept the data from an audited emissions channel, and upgrade the models for emissions accounting.  

For example, they can decide if a particular certifying entity's offset tokens would be accepted as a valid offsets.  They can decide the relative value of different offsets by voting on exchange rates or bonding curves.  They could validate the MRV results on an audited emissions channel before issuing offset tokens.  They could vote on whether emissions factors or emissions calculation methodologies should be updated on the emissions channels.  

Because many of the topics are technical, we need to balance experts vs. community members.  At the same time, though, it's important to create an inclusive model of collaboration, just like in open source software, to avoid the dangers of being locked into obsolete models and ineffective climate action.

Click here for a [video of the DAO](https://youtu.be/GeWETTG_eGc).

## Products Being Developed

- [Oil &amp; Gas Methane Emissions Reduction Project](19008903.html)
- [Supply Chain Decarbonization](Supply-Chain-Decarbonization_19006065.html)

## Get Involved

Here are some good first issues to get started with:

* * *

### Coding Standards

Even though, or perhaps because we're building open source software, code quality is very important.  We're writing code that others would see long after we're finished, so we'd better leave them something they could actually understand and work with.  We'd also like to avoid being featured in an "Anti Pattern" book or blog post.

The most important coding standard is to keep things very modular, so separate each function as much as possible.  The UI and application logic must be completely separated, to the point of being separate projects, and talk to each other only through clearly defined (REST) API's.  This means that we could have several different UI's, like Linux.  It also means we don't start putting our business logic in the UI, like some PHP or JSP code did.  Similarly, different application domains such as user management, application logic, and standards data management must be kept apart as well. 

### **Cryptocurrency Policy and Disclaimer**

This project does not endorse nor recommend any cryptocurrency for investment.  No integrations with any cryptocurrency are planned for this project.  Cryptocurrencies are very volatile and risky, so do your own research and stay within your risk tolerance. 

# Get Involved

#### This is an open source project and anyone is welcome to get involved and we will be happy to see you contribute.

1\) Start by subscribing to the [Climate SIG mailing list](https://lists.hyperledger.org/g/climate-sig) for updates and meeting notifications.

2\) Join our bi-monthly Peer Programming Zoom call for developers on Mondays at 9 AM US Pacific time (UTC-07:00 America/Los Angeles.) Please [check the calendar for the next call](https://lists.hyperledger.org/g/climate-sig/calendar). 

3\) Check out the [good first issues from our blockchain-carbon-accounting in Hyperledger-labs](https://github.com/hyperledger-labs/blockchain-carbon-accounting/issues) and feel free to contribute a fix for one that looks interesting to you.

4\) See our [How to Contribute](How-to-Contribute_19006806.html) page for other ways how you could get involved. 

![](plugins/servlet/confluence/placeholder/unknown-macro)

## Attachments:

![](images/icons/bullet_blue.gif) [Carbon\_Neutral\_Certification\_HLFabric\_Architecture.png](attachments/19005889/19005942.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
