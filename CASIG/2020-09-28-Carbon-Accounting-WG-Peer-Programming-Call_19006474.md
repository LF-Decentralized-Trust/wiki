1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Archive\_](Archive__19006062.html)
4. [Accounting &amp; Certification WG Peer Programming Call](19006574.html)
5. [2020 Peer Programming Call Notes Archive](2020-Peer-Programming-Call-Notes-Archive_19006254.html)

# Climate Action SIG : 2020-09-28 Carbon Accounting WG Peer Programming Call

Created by Si Chen, last modified on Nov 09, 2020

Today we showed a basic UI connecting [opentaps](https://github.com/opentaps/opentaps_seas) with the blockchain [carbon accounting ledger](https://github.com/opentaps/blockchain-carbon-accounting) through a REST api.  From a site in opentaps, we could use the utility bill data to record emissions on the ledger.  We could then see the emissions associated with the site.  Right now the UI is very basic, but we're working on implementing [additional functionality](https://github.com/opentaps/blockchain-carbon-accounting/issues) for it to calculate real emissions and see a list of emissions records. We will also be implementing a [registerAndEnrollUser function](https://github.com/hyperledger/fabric-samples/blob/master/test-application/javascript/CAUtil.js) similar to the one in the Fabric asset transfer sample so that each user would have their own key to access the ledger.  This is based on option 1 from [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)'s comments for [the August 31 call](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Carbon+Accounting+WG+Peer+Programming+Call+2020-08-31).  I made a diagram showing how our current architecture is planned:

![](attachments/19006474/19006475.png?height=400)

[Conor Svensson](https://lf-hyperledger.atlassian.net/wiki/people/557058:d2adae8a-8cf9-4b78-9790-cd7352deb58a?ref=confluence) then showed us the Epirus platform that his company has been developing.  It will create an open API for deploying tokens on an Ethereum chain.  He is preparing a big release in the next few days.  Using this platform, we will be able to integrate both permissioned fabric ledgers and public Ethereum channels.  

[Martin Wainstein](https://lf-hyperledger.atlassian.net/wiki/people/5af98bd1e608115790242590?ref=confluence) talked with us about how Renewable Energy Certificates (REC's) are created.  They are based on utility data and Independent System Operator (ISO) data and are created in a registry of the ISO, such as [WREGIS](https://www.wecc.org/WREGIS/Pages/Default.aspx).  They could be used for either flat or marginal (time of use) displacement of emissions.  For the latter there is a [Watt Time database](https://www.watttime.org/).

Long-term, we plan to put the pieces together like this:

![](attachments/19006474/19006481.png?height=400)

1. A group of people could get their utility, travel, and other data on permissioned data channels
2. An auditor could get access to those channels and calculate the total emissions
3. REC tokens could be integrated into the auditor's calculations to offset utility emissions
4. Total emissions would be minted as tokens
5. The group would then contribute towards offsetting their emissions
6. Based on their emissions and tokens, a DAO could set up a voting mechanism for them to vote on emissions offseting projects

We talked about integrating with Hyperledger Aries, which could be used to set up an automated or digital auditor that could verify claims in real time against data from IOT devices, utility meters, etc.  This could also be used to turn REC's into mitigation outcomes.

Since the next OpenClimate collabathon is in about a month, we should plan on some prompts to get more contributions and participation in this project.  Key questions are where we will be in early November, our overall vision of what to build, and what would need to be built next.

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [Blockchain Carbon Accounting 2020-09-25 (1).png](attachments/19006474/19006475.png) (image/png)  
![](images/icons/bullet_blue.gif) [Blockchain Carbon Accounting 2020-09-25.png](attachments/19006474/19006476.png) (image/png)  
![](images/icons/bullet_blue.gif) [Blockchain Carbon Accounting 2020-09-25 (2).png](attachments/19006474/19006481.png) (image/png)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19006474/19006478.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 13:10

[Atlassian](http://www.atlassian.com/)
