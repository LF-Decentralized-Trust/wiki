1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Working Groups](Working-Groups_19005701.html)

# Climate Action SIG : Carbon Accounting and Certification WG

Created by Si Chen, last modified by Kentaro Vadney on Jul 11, 2024

The mission of this working group is to

- identify how blockchain or distributed ledger technologies (DLT's) could improve corporate or personal carbon accounting
- make carbon accounting and certifications more open, transparent, and credible
- build collaboration between consumers, businesses, and investors across industries and national boundaries.

We're here to help 

- Businesses and organizations take action on climate change by making the process easier and less costly.
- Certifying entities scale by streamlining the verification of corporate climate action.
- General public and consumers trust corporate climate action.
- Lenders and investors align their capital decisions with climate goals.

# We're Live!

The [Emissions Data Channel](Emissions-Data-Channel_19006106.html) and [Emissions Tokens Network](Emissions-Tokens-Network_19006546.html) are now deployed in production:

To sign up for a beta please email the [Climate SIG mailing list](https://lists.hyperledger.org/g/climate-sig).

# Good First Issues

We're using Github to host the code for this lab.  Check out the [blockchain-carbon-accounting repo](https://github.com/hyperledger-labs/blockchain-carbon-accounting) and take one of the good first issues that are posted there.

# Scope

The current scope of this working group includes:

- Identifying standards for corporate climate accounting and certifications.
- Implementing open source DLT software to demonstrate climate accounting and certifications.
- Providing recommendations on how DLT's could complement or improve current industry processes.
- Promoting awareness and positive action in the larger Hyperledger and DLT community.
- Educating other stakeholders on the value of DLT's and Hyperledger in climate change.

# Active Members

To help group members meet and interact with each other, people are welcome to add their contact information and your time zone to this page so that other participants can contact you directly. 

**Adding your name here is optional and is not required to be a part of the group.** 

To add your name in the directory below: you will need edit access to the wiki, and for this you need to get a free [Linux Foundation ID](https://identity.linuxfoundation.org/). Once you have your LF ID (which you can use to log in the chat as well) you can log in and edit the table below with your information. After adding your name here, please also [subscribe to the group's mailing list](https://lists.hyperledger.org/g/climate-sig) and post an introduction there so other group members can get to know you. You can also join the [CA2 Hyperledger Chat](https://chat.hyperledger.org/channel/climate-action-sig) group and make a personal introduction there and join the regular group meetings. 

NameCompanyTime Zone  
[Si Chen](https://www.linkedin.com/in/opentaps/)[Open Source Strategies, Inc.](http://opensourcestrategies.com)US Pacific  
[Kentaro Vadney](https://www.linkedin.com/in/kentarov/)[Carbon Sustain](https://www.linkedin.com/company/carbon-sustain/)US Pacific

Christiaan Pauw

Nova Institute

[Robin Klemens](https://www.linkedin.com/in/robinklemens/)

[Blockchain Lab - Institute for Internet Security](https://bl.internet-sicherheit.de/index.html)

CET  
[Lam Nguyen](https://www.linkedin.com/in/lamnguyenduc/)

Connectivity AAU

[Kamlesh Nagware](https://www.linkedin.com/in/kamlesh-nagware-1456094b/)Snapper Future Tech

vaneet sharma

peregrines computing s.l

Carlos Germano Ferreira Costa&amp;Cho - Green Fintech

Brazil

[Vatsal M](https://www.linkedin.com/in/ethicalvats/)

Solligence Digital Solutions LLP

India

Umesh GhodkeWestern Climate Initiative, Inc. US Pacific  
Kris SternNCSIHong Kong  
Sherwood MooreICANNPST  
Lucy LowFarmerNet.OrgSan Francisco  
Chris AdamsCiscoLondon GMT  
Jeff Pribichblockchainindustrygroup,orgChicago 

# Background

As the world gets serious about climate change, the discussion is increasingly shifting from "Should" to "How":

- How do consumers know that a "green product" is really better for the climate?
- How do investors know that portfolio companies are achieving their climate goals?
- How do offset buyers know that the offsets work?
- How do lenders know that green bonds and transition bonds are driving positive climate action?

The only way we could do this is with a climate accounting system, similar to the financial accounting system that drives all economies.  Yet today, such an accounting system does not really exist.  This is because of the challenges of **data** and **trust**.  

### The Challenge of Data

A GHG emissions audit requires data from a lot of different sources, many outside of the company.  The [Greenhouse Gas Protocol](https://ghgprotocol.org/) specifies three levels of emissions: Scope 1, 2, and 3, covering direct energy use (fuel burned on site), indirect energy use (energy purchased from utilities), and all other significant activities of the business, including products purchased, transportation of goods, travel and commuting of employees, and leased assets.

The problem is that most emissions come from activities which are hard to get data for.  At a minimum, the data would need to come from every part of the business, from purchasing to manufacturing to facilities management to human resources.  More importantly, it also involves data from a company's supply chain partners, such as the manufacturers of its products or components.  Those manufacturers, in turn, may not have this data or may not wish to publish it for competitive reasons.  Finally, what data could be obtained must often be gathered manually and entered into spreadsheets.   

The high cost or complexity of obtaining the data has limited both the quantity and quality of data used for emissions calculations.  Often, emissions are calculated based on national and industry level economic activity–for example, the plastics industry in the United States as a whole.  If that's case, how do we know what the emissions of a particular plastic packaging manufacturer are?  What incentive does a particular manufacturer have to reduce its emissions?

### The Questions of Trust

At the same time, it's not hard to see why the general public could be skeptical of a company's climate action claims.  After all, as consumers,

- Can we trust the data that the company has provided?
- Can we trust judgement calls, made by either the company or a certifying entity, about which activities are not relevant and thus do not require data and auditing?
- How do we know if the company is in fact working on its emissions reduction plan?
- Can consumers and investors trust that the certifying entity is objective?

Meanwhile, institutional investors such as the [Net Zero Asset Owner Alliance](https://www.unepfi.org/net-zero-alliance/) or [Climate Action 100+](http://www.climateaction100.org/) have a different trust issue.  They are used to more in-depth analysis and independent verification of companies' claims, and carbon neutral certifications do not have the same level of detail as other financial ratings they are accustomed to.  For example, when investing in bonds, it's not enough that one rating agency, such as Standard &amp; Poors or Moody's, considers a bond "investment grade."  They typically require credit ratings by more than one rating agency, and the ratings are in tiers from AAA (highest credit quality) to CCC (high default risk.)   As climate neutrality becomes important to them, they would probably demand the same level of detail in ratings of corporate climate action.

### **Why Blockchain (DLT's)**

Fortunately, blockchains or distributed ledger technologies (DLT's) are by design made for solving these issues.  With blockchains, we can

- Automate data collection from a large number of sources, as is typical in supply chains.
- Maintain audit trail of immutable records, so that emissions calculations could be verified later without relying on one central repository.
- Create trust in CO2 emissions accounts as they are transacted across industry and national boundaries, where no trusted central repository exists.
- Allow consumers to participate in climate action plans of the companies they buy from and invest in.

DLT's differ from Software as a Service (SAAS) in a fundamental way: They are designed for collaboration across a large number of potential users/participants without signing on to a central service provider.  They are thus ideal for crossing traditional industry or national boundaries or for allowing small entities (SME's) or even individuals to interact with large ones (multinationals and government agencies.) 

Why Open Source

By making the source code available, we make the carbon emissions accounting and certification process transparent, so that all stakeholders could see what went into it.  This increases the trust in the results.

Furthermore, by creating free tools for gathering data, we allow certifying entities to focus on analysis, while reducing the cost of carbon emissions reporting so that it becomes possible for companies of all sizes, instead of just the large, public ones.  

### Getting Started

Our goal is to create software that could be used to deploy climate action at a variety of scales, from supra-national cap and trade to community renewable energy projects.  Take a look at what we're building -- an [Operating System for Climate Action](Operating-System-for-Climate-Action_19005889.html).  

# Get Involved

#### This is an open source project and anyone is welcome to get involved and we will be happy to see you contribute.

1\) Start by subscribing to the [Climate SIG mailing list](https://lists.hyperledger.org/g/climate-sig) for updates and meeting notifications.

2\) Join our bi-monthly Peer Programming Zoom call for developers on Mondays at 9 AM US Pacific time (UTC-07:00 America/Los Angeles.) Please [check the calendar for the next call](https://lists.hyperledger.org/g/climate-sig/calendar). 

3\) Check out the [good first issues from our blockchain-carbon-accounting in Hyperledger-labs](https://github.com/hyperledger-labs/blockchain-carbon-accounting/issues) and feel free to contribute a fix for one that looks interesting to you.

4\) See our [How to Contribute](How-to-Contribute_19006806.html) page for other ways how you could get involved. 

![](plugins/servlet/confluence/placeholder/unknown-macro)

## Attachments:

![](images/icons/bullet_blue.gif) [cop26 (4).png](attachments/19005779/19006118.png) (image/png)  
![](images/icons/bullet_blue.gif) [Diagram of HDxe SDR Schema.pdf](attachments/19005779/19006119.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [screenshot-915256e590bd48299eb271dc83e0a948-ibpconsole-console.uss02.blockchain.cloud.ibm.com-2020.08.07-19\_15\_30.png](attachments/19005779/19006120.png) (image/png)  
![](images/icons/bullet_blue.gif) [screenshot-cloud.ibm.com-2020.08.12-20\_00\_54.png](attachments/19005779/19006162.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
