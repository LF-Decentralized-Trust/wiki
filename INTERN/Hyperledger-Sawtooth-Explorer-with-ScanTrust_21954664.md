1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2019 Projects](2019-Projects_21954613.html)

# Hyperledger Mentorship Program : Hyperledger Sawtooth Explorer with ScanTrust

Created by Ricardo Garcia, last modified by Minh Võ Ngọc on May 11, 2020

**Title**Creation of a functioning blockchain explorer for Hyperledger Sawtooth**Status**

PROJECT COMPLETED

**Difficulty**

MEDIUM

# Description

Blockchain is a back-end technology. However, for many of ScanTrust’s customer projects, customers still want a way to be able to “see” what is happening in the blockchain.  They want to see the blocks being created, transactions committed, and ideally be able to make sense of what is inside the transaction. For this you need a blockchain explorer.  

In our vision, the explorer is an application that both listens to events happening inside the blockchain (via websockets) as well as calling the sawtooth API, with an intuitive front-end for the user. The ideal explorer would be generic across sawtooth installations, but extensible by developers to add understanding of the customer data in the transactions (since it is often in a binary format) for display.  

ScanTrust uses Hyperledger Sawtooth for several customer projects. The task of the intern would consist of creating a generic blockchain explorer for Hyperledger Sawtooth that ScanTrust will be able to use in current and future customer projects. This means that the intern will use a front-end framework to build an application that listens to ScanTrust’s existing Sawtooth infrastructure.

# Additional Information

About ScanTrust:

[https://www.scantrust.com/](https://www.scantrust.com/)

Example of a ScanTrust Hyperledger Sawtooth Project:

[https://www.hyperledger.org/wp-content/uploads/2018/08/Hyperledger\_CaseStudy\_ScanTrust.pdf](https://www.hyperledger.org/wp-content/uploads/2018/08/Hyperledger_CaseStudy_ScanTrust.pdf)

Event subscriptions in Hyperledger Sawtooth

[https://sawtooth.hyperledger.org/docs/core/releases/latest/app\_developers\_guide/event\_subscriptions.html](https://sawtooth.hyperledger.org/docs/core/releases/latest/app_developers_guide/event_subscriptions.html)

Hyperledger Sawtooth Web Sockets:

[https://sawtooth.hyperledger.org/docs/core/releases/latest/app\_developers\_guide/web\_socket\_event\_subscription.html#](https://sawtooth.hyperledger.org/docs/core/releases/latest/app_developers_guide/web_socket_event_subscription.html)

# Learning Objectives

Hard skills:

- Learning about Hyperledger Sawtooth architecture, framework and consensus
- Usage of Hyperledger Sawtooth APIs
- Creation of blockchain web application
- Usage of front-end frameworks for blockchain development
- Introduction to the supply chain market

Soft skills:

- Work in a remote team across borders
- Work independently with little instructions

# Expected Outcome

- Functional web application with UI that can be used in customer projects, as described in paragraph “description”

Relation to Hyperledger 

The project is related to the Hyperledger Sawtooth project.

# Education Level

Undergraduate or above

# Skills

Must have:

- Previous front-end development experience in modern web frameworks such as Vue, React, or Angular
- Self starter and driven mindset
- Ability to work independently with limited supervision
- Good understanding of blockchain technology and distributed systems in general

Nice to have:

- Python development experience
- Basic DevOps experience (usage of docker images, docker files, docker containers etc.)
- Previous Hyperledger Sawtooth exposure would of be helpful

# Future plans

If the project is implemented successfully, it will be used in all customer projects that involve Hyperledger Sawtooth as a technology. It will become one critical element in ScanTrust’s blockchain tool set.

# Preferred Hours and Length of Internship

Full-time (40 hours a week for 12 weeks during the summer)

# Mentors and Mentee Names and Contact Info

Ricardo Garcia, [ricardo.garcia@scantrust.com](mailto:ricardo.garcia@scantrust.com), Head of Partnerships &amp; Blockchain Advisory

Andrew Backer, [andrew.backer@scantrust.com](mailto:andrew.backer@scantrust.com), Head of Engineering

[Vlad Bormisov](https://lf-hyperledger.atlassian.net/wiki/people/70121:f0846f42-3faf-459c-8031-4046d9131873?ref=confluence), bormisov1@gmail.com, mentee

# Project Plan

## Project Summary

SawTooth Explorer is an easy to install and use web-based frontend for navigating and understanding data stored in a sawtooth instance. It does not require customization, only access to the sawtooth REST API. The frontend provides easy searching, and friendly display of you

- Easy to use web frontend
- Sawtooth Metadata Caching &amp; Event Listener for fast searching
- Realtime
- Custom Transaction Family data model support

Project Deliverables

- Database - Metadata Caching &amp; Explorer Features
  
  - Block/Batch/Transaction/State/Address Data Model
- Sawtooth Event Listener
  
  - Real time, builds cache
  - Understanding of TxP families
- Metadata API
  
  - Search Metadata
  - Proxy calls to underlying sawtooth instance
- Web Frontend
  
  - Search &amp; Friendly Display of Block Data
  - Edit explorer specific metadata, such as friendly names for:
    
    - Signing keys seen
    - Transaction family names

## Stretch Deliverables

- Real-time notifications of transactions
- User account management
- Custom TxP schemas &amp; Navigation
- Ability to attach directly to an existing node and build history/cache

## Milestones

- Project Structure &amp; Data Design
- Real time event listener &amp; database
- API
- Frontend V1

Methodology

- Milestone Based
- Daily Meeting (30 minutes) - Scrum Light

# Summary Report

[![](attachments/thumbnails/21954664/21963059)](attachments/21954664/21963059.pdf)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Sawtooth Explorer Presentation.pdf](attachments/21954664/21963059.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 14:59

[Atlassian](http://www.atlassian.com/)
