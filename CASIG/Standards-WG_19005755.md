1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Working Groups](Working-Groups_19005701.html)

# Climate Action SIG : Standards WG

Created by Martin Wainstein, last modified by Alfonso Govela on Aug 01, 2024

# **Mission**

The mission and goals of the Climate Action and Accounting SIG include "to turn this network into action under a common open source project that defines shared protocols, standards, and platform tools for a globally integrated climate accounting system to be operationalized."

This working group will focus particularly on the "protocols and standards" that will enable consistent climate accounting.  

# **Work plan for 2023**

We coordinate most of the work for this working group through the bimonthly Standards WG call. The work plan for the working group is set out in [this](https://drive.google.com/file/d/1luI_bR3RdXP9EBxsQ58PQMdRKwREkvwm/view?usp=sharing) document. The most practical way to get involved is to join this call. Please [check the calendar for the next call](https://lists.hyperledger.org/g/climate-sig/calendar)[.](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Meetings) 

The 2023 work plan involves:

- SSSOM maps that map AIAO to at least two prominent greenhouse gas accounting standards.
- A SHACL shape graph that can be used to validate the conformation of annotated data to AIAO.
- Tagged impact documents from at least 10 representative case studies, stored in an appropriate open source graph database. One of the case studies will be the work of our sister working group, the [Carbon Accounting and Certification WG](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Carbon+Accounting+and+Certification+WG) of CA2-SIG.
- EITHER (a.) an AI model to annotate further documents according to AIAO, OR (b.) a SPARQL endpoint for querying annotated climate impact data.

# **Progress and opportunities to contribute**

For the latest version of our taxonomy of protocols, standards, methodologies and certifications, head over to [this page](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Taxonomy+of+protocols%2C+standards%2C+methodologies+and+certifications). The taxonomy is by no means complete yet, so feel free to add, improve and expand! You'll find some TODOs at the bottom of the page.

For the latest version of our ontology and its application guide, check out [this page](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/An+ontology+for+anthropogenic+impact+accounting). You will find a bunch of TODOs there that you can pick up and run with, e.g., embedding our ontology into the ISO/IEC Basic Formal Ontology (BFO).

Some further results and ideas are taking shape under the [New ideas, debates and discussions](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/New+ideas%2C+debates+and+discussions#Premise) page. If you like to go down rabbit holes or debating things, this page is for you.

The best way to start contributing is, however, by joining our biweekly calls. Please [check the calendar for the next call](https://lists.hyperledger.org/g/climate-sig/calendar)[.](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Meetings) 

# **Clarification**

## What do we mean by 'standards'?

The term 'standard' is used in a variety of contexts - even within the scope of the CA2-SIG a variety of things are denoted with the term 'standard'. These include:

- technical standards like those of the [W3C](https://www.w3.org/standards/);
- accounting standards, including:
  
  - [Greenhouse Gas Protocol;](https://ghgprotocol.org/standards)
  - the standards used for compliance purposes in different jurisdictions (e.g., the [CDM project standard](https://cdm.unfccc.int/filestorage/e/x/t/extfile-20181221092046529-Reg_stan04v02.pdf/Reg_stan04v02.pdf?t=TVR8cWEwbTRxfDA9HR0ljUuM6fH2xXZGHP3D), California Air Resources Board (CARB));
  - voluntary standards like the Verra's Verified Carbon Standard ([VCS](https://verra.org/project/vcs-program/rules-and-requirements/)), the [Gold Standard](https://www.goldstandard.org/project-developers/standard-documents), [Social Carbon](http://www.socialcarbon.org/wp-content/uploads/2012/11/SOCIALCARBON_STANDARD_v-5-.0-final-II1.pdf), American Carbon Registry (ACR), Climate Action Reserve (CAR), and The Plan Vivo Foundation;
  - standards for entity-level accounting within various scopes;
  - standards for local/regional/national inventories;
- environmental performance standards like those of the [IFC](https://www.ifc.org/wps/wcm/connect/24e6bfc3-5de3-444d-be9b-226188c95454/PS_English_2012_Full-Document.pdf?MOD=AJPERES&CVID=jkV-X6h);
- standards related to products; and
- standards for accounting for policy impacts.

## What are standards used for?

Standards are used for many things, among which:

- personal climate footprinting
- product/service footprinting
- entity accounting (scope 1, 2 and 3)
- regional accounting
- policy impact assessments

Standards are relevant at different phases of the climate accounting process:

1. There are standards for measuring aspects of activities and processes. Let's call these *measurement collection standards*. These standard are focussed on measurements and concern things like the calibration and correct use and instruments. Application of these standards produce valid measurement data.
2. There are other standards that standardise the transformation, evaluation and aggregation of data and metadata. We can call these *calculation methodologies* or *data processing standards*. Application of such standards produces indicators, metrics and indices with a well-defined meaning. Such outputs can be tokenised.
3. Another type of standard concerns claims or assertions about entities or activities, such as the yearly emissions of a company or the climate impact of a project. We can call these *reporting standards.* Application of these standards yield standards compliant reports. The contents of such reports can also be tokenised.
4. There are also standards that concern the process of measuring, reporting and verifying itself and the persons who carry out such assessments. We can call these *quality standards* and *verification or certification standards.* Application of such standards produce certifications or assurance.

## What is standardised?

- **Entities:** This is the problem of identity. We mean the identity of people, organisations and things. It is needed to connect an unambiguous identifier to all the entities involved in the accounting process. In the case of businesses, this may be difficult because businesses may have complicated structures of ownership and control (see for example Chapter 3 of the [GHG Protocol: Corporate Accounting Standard](https://ghgprotocol.org/sites/default/files/standards/ghg-protocol-revised.pdf)).
- **Agency:** This is the problem of responsibility - how do we show and prove that an entity (be that a person or organisation) is responsible for a certain action or outcome?
- **Activities and events:** Agents do things that affect their surroundings at some point in time.
- **Counterfactuals:** This is the problem of what would have happened if certain decisions had not been taken or certain actions had not been undertaken.

## What will the working group deliver and who will use it?

There are other bodies that create the types of standards mentioned above. This working group will be more concerned with how such standards themselves and compliance to these standards are encoded and captured in a distrubuted ledger and how such representations can be used. 

## What is the relationship between standards, authority and freedom in the context of the work of the CA2-SIG?

The CA2-SIG will not act as an authority that compels entities to engage in specific actions. 

The standards to be generated by this working group will enable agents to clearly communicate the implications of their actions. This will enable others to have a clear understanding of the state of affairs regarding the activities and states covered by the standards. 

## How will we translate standards into software?

Find the most generic articulation of what a standard, method and transaction is and develop protobuffer examples of each.

- Namespaced Merkle tree
- Protobuf examples

Refer to [this page](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/An+ontology+for+anthropogenic+impact+accounting) for more information.

# Get Involved

#### This is an open source project. Anyone is welcome!

1\) Start by subscribing to the [Climate SIG mailing list](https://lists.hyperledger.org/g/climate-sig) for updates and meeting notifications.

2\) Add your name to the active members list below.

3\) Join the CA2-SIG Standards WG calls that are held on every other Tuesday of the month at 8 AM US Pacific time (UTC-07:00 America/Los Angeles). Please [check the calendar for the next call](https://lists.hyperledger.org/g/climate-sig/calendar)[.](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Meetings) 

# **Meetings**

Join the CA2-SIG Standards WG calls that are held on every other Tuesday of the month at 8 AM US Pacific time (UTC-07:00 America/Los Angeles). Please [check the calendar for the next call](https://lists.hyperledger.org/g/climate-sig/calendar)[.](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Meetings) 

# **Active Members**

  NameCompanyChristiaan PauwNova InstituteAlex Howard

(Independent)

Alfonso GovelaHyperledger Latinoamerica Regional ChapterKyle RobinsonBrairtech Consulting Inc.

# **Other Contributors**

 

NameCompanyTom BaumannClimate Chain CoalitionMartin WainsteinYale OpenlabJohn BarassiOhvationSi ChenOpen Source Strategies, Inc.Sherwood MooreICANNJeff PribichIndependent

## Attachments:

![](images/icons/bullet_blue.gif) [ghg\_climate-change.pdf](attachments/19005755/19005912.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [TomBaumann-UEF-FS-CMT-Scottsdale-Public.pdf](attachments/19005755/19005916.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Baumann\_Blockchain for Planetary Stewardship Framework\_Blockchain Research Institute.pdf](attachments/19005755/19005918.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [PLACARD-Transforming-knowledge-for-climate-action-2020.pdf](attachments/19005755/19005920.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Towards Ontology and Blockchain Based Measurement, Reporting, and Verification For Climate Action - SSRN-id3717389.pdf](attachments/19005755/19006636.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Consumption-based accounting tool.xls](attachments/19005755/19006791.xls) (application/vnd.ms-excel)

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
