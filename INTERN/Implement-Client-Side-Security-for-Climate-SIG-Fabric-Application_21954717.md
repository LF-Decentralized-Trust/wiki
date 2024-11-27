1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)

# Hyperledger Mentorship Program : Implement Client Side Security for Climate SIG Fabric Application

Created by Si Chen, last modified by Min Yu on Nov 29, 2021

**Project Title**Implement Client Side Security for Climate SIG Fabric Application**Status**

COMPLETED

**Difficulty**

  HIGH

# Description

The [Carbon Accounting and Certification Working Group](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Carbon+Accounting+and+Certification+Working+Group) is developing an [Operating System for Climate Action](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Operating+System+for+Climate+Action), where there is a Hyperledger Fabric [Emissions Data Channel](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19006106/Emissions+Data+Channel) with utility data.  Currently, the security certificates for accessing Fabric are held server side.  A client application authenticates the user through standard username/password authentication and then access the Fabric chain code on behalf of the user. 

We would like to explore a client driven authentication for the Fabric application, similar to how Metamask is used with Ethereum dApps such as the [Emissions Tokens Network](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19006546/Emissions+Tokens+Network).  In such a use case, the user would sign into a web portal, enter and upload their information, and then sign the transaction with a local security key or a dApp wallet such as Metamask.  

# Additional Information

For background, see the [Carbon Accounting and Certification Working Group](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Carbon+Accounting+and+Certification+Working+Group) wiki page.

To check out the code, see [https://github.com/hyperledger-labs/blockchain-carbon-accounting](https://github.com/hyperledger-labs/blockchain-carbon-accounting), specifically [utility-emissions-channel/README.md](https://github.com/hyperledger-labs/blockchain-carbon-accounting/blob/main/utility-emissions-channel/README.md) for more details on the Hyperledger Fabric utility emissions channel.

There is currently a [task for testing offline signing](https://github.com/hyperledger-labs/blockchain-carbon-accounting/issues/11). 

We have also started looking at [TrustId](https://github.com/hyperledger-labs/TrustID) and have a [pull request](https://github.com/hyperledger-labs/blockchain-carbon-accounting/pull/50) for integrating with it.  Maria from TrustId also made a [presentation](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19006691/2021-01-18+Peer+Programming+Call) during our peer programming call.

# Learning Objectives

As part of this project, you will learn about

- Hyperledger Fabric chain code development
- REST APIs
- dApp security and wallets
- Open source development and project management

# Expected Outcome

Implementation of an application with client side authentication for Hyperledger Fabric utility emissions data channel.  Documentation and tutorials showing how this is done.

# Relation to Hyperledger

This project is part of the Hyperledger Labs blockchain-carbon-accounting project and the [Climate Action SIG](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/).  It will work with Hyperledger Fabric and Cactus as the main technologies and main involve Besu as well.

TrustId is also a Hyperleger Labs project.

# Education Level

# Skills

Familiarity with Hyperledger Fabric, Node.js, web and dApp security frameworks.

# Future plans

After the conclusion of the project, you can join us for more development in the [Climate Action SIG](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/) as well as get involved in production climate [blockchains that drive climate action](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Operating+System+for+Climate+Action) that include tokens and DAO's.

# Preferred Hours and Length of Internship

Full time or part time.  Three months.

# Mentor(s) Names and Contact Info

Si Chen, Open Source Strategies, Inc. - [sichen@opensourcestrategies.com](mailto:sichen@opensourcestrategies.com)

Vatsal M - [mevatsal@gmail.com](mailto:mevatsal@gmail.com)

María Teresa Nieto, Telefónica - [mariateresa.nietogalan@telefonica.com](mailto:mariateresa.nietogalan@telefonica.com)

Kamlesh Nagware, Snapper Future Tech, kamlesh.nagware@gmail.com

# Mentee

[Bertrand WILLIAMSRIOUX](https://lf-hyperledger.atlassian.net/wiki/people/712020:57613290-3ad4-4f53-8166-19a9bdb9c047?ref=confluence)

# Results

[https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Project+Plan+-+Implement+Client+Side+Security+for+Climate+SIG+Fabric+Application](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Project+Plan+-+Implement+Client+Side+Security+for+Climate+SIG+Fabric+Application)

# Final Report

[https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Project+Plan+-+Implement+Client+Side+Security+for+Climate+SIG+Fabric+Application](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Project+Plan+-+Implement+Client+Side+Security+for+Climate+SIG+Fabric+Application)

Document generated by Confluence on Nov 26, 2024 14:57

[Atlassian](http://www.atlassian.com/)
