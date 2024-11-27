1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Archive\_](Archive__19006062.html)
4. [Accounting &amp; Certification WG Peer Programming Call](19006574.html)
5. [2020 Peer Programming Call Notes Archive](2020-Peer-Programming-Call-Notes-Archive_19006254.html)

# Climate Action SIG : 2020-11-09 Carbon Accounting WG Peer Programming Call

Created by Si Chen, last modified on Nov 09, 2020

Today we covered some important topics from deployment of the [utility emissions channel](Emissions-Data-Channel_19006106.html) to the set up of the [net emissions channel](Emissions-Tokens-Network_19006546.html).  Thanks to [Conor Svensson](https://lf-hyperledger.atlassian.net/wiki/people/557058:d2adae8a-8cf9-4b78-9790-cd7352deb58a?ref=confluence), [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence), [Lam Nguyen](https://lf-hyperledger.atlassian.net/wiki/people/712020:61b84c88-58c9-4599-a9a5-6da98840b618?ref=confluence), [Vatsal Mishra](https://lf-hyperledger.atlassian.net/wiki/people/557058:44b0931b-9e39-4e47-8b4d-37a5af479d29?ref=confluence), SIJO ![(question)](images/icons/emoticons/help_16.png) for attending.

### Deploying the Utility Emissions Channel

We're currently working on deploying the utility emissions channel using docker swarm to Amazon web services cloud.

Once deployed, we'll set up a small test network, for example a node in the USA and a node in Europe.  Each node would serve as a "virtual auditor" of emissions for businesses and individuals in their respective regions.  As a virtual auditor, it needs only to furnish compute resources to run the business logic in the chain code, which will automate the auditing of carbon emissions based on data.  The operator of the node would be responsible for signing up new users in their area.

Each node will need to secure its REST api end point so that only authorized suers can access it.  We plan to do this with REST API keys.  More details will be coming on this one later.

Will there be one Fabric network or multiple Fabric networks, one for each region?  This we'll have to see.  On each Fabric network there will only be one version of chain code running, so all members of the network have to be running with the same business logic and base data set.  As long as the same business logic and data set can be used to map electricity used (KWH) to emissions (MtCO2e), we can all be on the same network.  If it's a question of getting different data sets we can expand the data set.  But if there will be different business logic altogether, then we'll have to have different networks.  In that case, the networks would have to collaborate together on the net emissions channel, which is denominated in MtCO2e, instead of the utility emissions channel, which is denominated in KWH. 

### Net Emissions Channel

Then the question of how to develop a net emissions channel.  The first question is: What exactly is the net emissions channel?  After some discussion, the best analogy (from Sijo@ibm.com) was a "Climate Fitness App".  Like a personal fitness app, it gathers data from many sources, then aggregates it together, and reports your overall fitness, in this case for climate-changing emissions.  So remember – If the potato chips don't get you, climate change will. ![(sad)](images/icons/emoticons/sad.png)

So should it be on a public or permissioned ledger?  [Conor Svensson](https://lf-hyperledger.atlassian.net/wiki/people/557058:d2adae8a-8cf9-4b78-9790-cd7352deb58a?ref=confluence)'s recommendation is that we start on a private ledger, and then put it on a public ledger if we need to expand the user base.  It is easier to manage a private ledger initially.  We can develop against an ethereum test net, and then later deploy either to a private or public ethereum network.  I thought this made a lot of sense.

How do utility emissions relate to net emissions?  Utility emissions are not really non-fungible tokens but immutable data.  They should be grouped together, with the net data stored as a hash on the emissions token. 

### Cloud vs Distributed Resources

Finally we had a fun discussion about using cloud vs distributed resources, specifically where to store archival copies of utility bills and backup data.  We can store a hash of the utility bill and supporting data on the ledger, but that will not get us back the original bill or data in case we need to verify the emissions calculations.  So where do we store the original bills and data inputs?

One option is cloud-based storage, like Google drive or Amazon Glacier.  Another option is to use IPFS for a distributed experience.

If we're already using cloud-based servers to run the network, then is it necessary to use IPFS for storage, or is cloud-based storage more convenient?

Or should we go towards a fully distributed setup, with peer to peer nodes and storage eventually?

### Upcoming Development

In case you'd like to join our development, we're working on quite a few things.

First, deployment of the utility emissions Hyperledger Fabric to the cloud.

Second, we have a list of outstanding issues on Github.

Finally, we'd like to expand to other countries and regions.  In the USA we're using the [EPA's eGRID database](https://www.epa.gov/egrid), which has very detailed emissions information for utilities and regional groups of utilities.  We'd like to find other datasets, for example [OurWorldInData.org's data set for India](https://ourworldindata.org/co2/country/india?country=~IND), that could be used to base reasonable emissions calculations upon.  

If you can help with any of these, please let us know with a comment.

Document generated by Confluence on Nov 26, 2024 13:10

[Atlassian](http://www.atlassian.com/)
