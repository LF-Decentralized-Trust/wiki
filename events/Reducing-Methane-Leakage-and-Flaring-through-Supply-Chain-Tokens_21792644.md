1. [Community Events](index.html)
2. [Community Events Home](Community-Events-Home_21790731.html)
3. [Challenges](Challenges_21792347.html)
4. [Hyperledger Challenge 2022](Hyperledger-Challenge-2022_21792351.html)
5. [Ideate Challenge](Ideate-Challenge_21792356.html)
6. [Submissions](Submissions_21790825.html)

# Community Events : Reducing Methane Leakage and Flaring through Supply Chain Tokens

Created by Bertrand WILLIAMSRIOUX, last modified by Arezkidji on May 11, 2022

**1) Project Name:** Reducing Methane Leakage and Flaring through Supply Chain Tokens

**2) Innovation Tagline: Using the blockchain to create supply chain incentives to reduce 1 Gt CO2e of from methane flaring and fugitive emissions** 

3) **List the** **Hyperledger Projects that will be leveraged to develop your solution:** We are building a carbon tracking network to tie together supply chain emission data. This will include a set of smart contracts as part of the open source blockchain carbon accounting tools built by the CA2SIG: a [Utility Emissions Channel Project](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Utility+Emissions+Channel+Project) for auditing emission from electricity purchases, [Net Emissions Token (NET) Project](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Emissions+Tokens+Network+Project) to tokenize emissions and offset credits, and a [Climate DAO Project](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/DAO+Project), the elements of an [operating system for climate action](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Operating+System+for+Climate+Action).  These projects are built on top of Hyperledger Fabric, Besu, and Bevel.

4\) Project Members

1. [Bertrand WILLIAMSRIOUX](https://lf-hyperledger.atlassian.net/wiki/people/712020:57613290-3ad4-4f53-8166-19a9bdb9c047?ref=confluence)
2. [Woody Moore](https://lf-hyperledger.atlassian.net/wiki/people/70121:310f5eae-a11b-435a-ae52-42b0a796fe0b?ref=confluence)
3. [Si Chen](https://lf-hyperledger.atlassian.net/wiki/people/557058:c49c10c4-25bf-4187-b582-b521c3c33223?ref=confluence)
4. [Arezkidji](https://lf-hyperledger.atlassian.net/wiki/people/557058:f648e1dc-1c53-470f-a796-f2f1c040b884?ref=confluence)

### Problem

Even as we reduce our Greenhouse Gas (GHG) emissions to stop climate change, the oil and gas industry will remain a central part of the global energy system for decades.  In this period, a top priority is to reduce the amount of methane that is leaked and flared during the production of oil and natural gas. Methane trapped in the geological formations of oil and gas wells is often disposed of as a safety measure, but also leaked or vented to the atmosphere when infrastructure is not available to gather, process and distribute it as natural gas for a profit. This is typical in remote and undeveloped areas (the highest rates are observed in Africa, Figure 1) where methane is burned (flared) and converted into Carbon Dioxide (CO2), or worse, vented or leaked. 

Figure 1 flaring and venting data from [EDF (2021)](https://business.edf.org/files/ESG-by-EDF-Flaring-Report-Book-V2-Reduced.pdf) 

![](attachments/21792644/21792645.png?width=463)

The Greenhouse Gas (GHG) warming potential of uncombusted methane is more that 25 times on a CO2 equivalent (CO2e) basis. While, flaring was estimated at 142 billion cubic meters (bcm) in 2020 (figure 1), 265 million tons (Mt) CO2e, 8 Mt of methane were released at 240 Mt CO2e ([IEA 2020](https://www.iea.org/reports/flaring-emissions)). Assuming a lower combustion efficiency total emissions could reach as high as 1 Gt of CO2e, greater than the total emissions of Germany or all the world's airlines.   

Although major oil companies, NGO's, and investors have all committed to reducing oil and gas methane emissions, it remains a challenge because of a lack of quality data about the methane emissions of specific facilities and producers.  As a result, it's difficult to allocate the needed investment to the right places.

### Solution

We propose a solution using two important blockchain features:

- An oracle which could integrate multiple sources of data, from satellite images to company reported data to facility level instruments, that together could provide the best estimate of methane emissions at the facilities and company levels.
- A tokens network that would allow the value of lower methane emissions to be transferred to buyers looking for fuel with lower carbon intensity.

For more technical details, please see [Oil &amp; Gas Methane Emissions Reduction Project](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19008903/Supply+chain+tokens+for+oil+gas+emissions+reductions). 

#### Minimum viable product

Our target product is a portal where data from multiple sources of methane emissions could be viewed, and the final methane emissions for a production facility is calculated.  Then an oil &amp; gas producer could also:

- registers as an industry dealer of the NET network
- construct a (voluntary) emission profile (C-NFT) for current inventories (using VCT) based on the calculated methane emissions
- connects its C-NFT profile to the waste emission verification system (Figure 3)
- list inventories as digital VCT that can be transferred to other industry/consumer accounts.

### Accomplishment and Team

Our team-members has been working on the [Supply Chain Decarbonization](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19006065/Supply+Chain+Decarbonization) for some time, with the [Operating System for Climate Action](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19005889/Operating+System+for+Climate+Action) providing much of the underlying code needed for this challenge.

[Bertrand WILLIAMSRIOUX](https://lf-hyperledger.atlassian.net/wiki/people/712020:57613290-3ad4-4f53-8166-19a9bdb9c047?ref=confluence)  is an independent consultant with 15 years of experience in energy economics, climate science and computer programming.  He has worked as an analyst and advisor on energy market and climate policy issues, and is currently creating a startup offering carbon accounting and management services for energy intensive commodity industries.

[Si Chen](https://lf-hyperledger.atlassian.net/wiki/people/557058:c49c10c4-25bf-4187-b582-b521c3c33223?ref=confluence) is the founder of [Open Source Strategies, Inc.](https://www.opensourcestrategies.com/) and coordinates the [Carbon Accounting and Certification WG](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19005779/Carbon+Accounting+and+Certification+WG) of the hyplerledger [Climate Action and Accounting (CA2 SIG)](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/overview).  He is the author of the open source book, [Open Climate Investing](https://climate-investing-book.opensourcestrategies.com/v/main/book), and a co-editor of an upcoming book "Sustainable Carbon Economy with Blockchain: The Role of Oil and Gas Industry in The Energy Transition". 

[Woody Moore](https://lf-hyperledger.atlassian.net/wiki/people/70121:310f5eae-a11b-435a-ae52-42b0a796fe0b?ref=confluence) is currently acting Co-chair of the Climate Action and Accounting Special Interest Group (CA2SIG). He holds a MBA with 10+ years of experience planning and executing Go-to-Market strategies for early stage tech start-ups. He also has expertise in the field of internet governance, where he supports ICANN's (Internet Corporation for Assigned Names and Numbers) multistakeholder decision-making model to help the global community reach consensus around the protocols, standards and policies needed to support the security, stability and resiliency of the internet's Domain Name System.

Additional resources needed:

- Front end user interface development
- Hyperledger Fabric - Integration of remote sensing data to Fabric and integration of Fabric with Layer 2 Ethereum network.

### Project Plan

We set the following goals for the a prototype methane reduction C-NFT

- Construct the methane emissions of an oil and gas producer by combining industry repots with with independent data
- Illustrate the verification of emissions in line with recognized standard setting body practices
- Track embedded emissions though to the final producer of a consumer fuel (gasoline/diesel).

Launch phase

1. Collect and prepare emission data (4 weeks)
   
   1. Select a set of typically of oil/gas well and gather relevant data, sourced from company reports, independent sources, ([Flaring Monitor](https://github.com/flaringmonitor)), sensors, or simulated.
   2. Create/select a representative model/data set for intermediate processing of oil and gas in a refinery and a power plant to produce a consumer fuel.
   3. Setup up data sources to be storage within a fabric emission channel or IPFS database (Figure 3)
2. Build the blockchain oracle (8 weeks)
   
   1. Select an oracle service
   2. Integrate the distributed database (fabric/ipfs) with the oracle
   3. Register "real-world" methane emission data as digital token in the layer 2 NFT contracts.
3. Construct emission profiles  (4 weeks)
   
   1. Design UI/UX for for constructing and linking emission inventories
   2. Using the NET network compile emission inventories (accounting boundaries) for each facility using the [GHG Protocol corporate reporting standard](https://ghgprotocol.org/corporate-standard)
   3. Using C-NFT Bridge accounting boundaries following the [Value chain (scope 3) reporting standards](https://ghgprotocol.org/standards/scope-3-standard):
4. Simulate trading of methane performance tokens / CI certificate using C-NFT (4 weeks)

## Attachments:

![](images/icons/bullet_blue.gif) [Flaring data EDF.png](attachments/21792644/21792645.png) (image/png)  
![](images/icons/bullet_blue.gif) [CarbonTrackerSimple.drawio (3).png](attachments/21792644/21792646.png) (image/png)  
![](images/icons/bullet_blue.gif) [CarbonTrackerSimple.drawio (4).png](attachments/21792644/21792647.png) (image/png)  
![](images/icons/bullet_blue.gif) [CarbonTrackerSimple.drawio (5).png](attachments/21792644/21792648.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-2-9\_9-6-17.png](attachments/21792644/21792658.png) (image/png)  
![](images/icons/bullet_blue.gif) [CarbonTrackerSimple.drawio (6).png](attachments/21792644/21792674.png) (image/png)  
![](images/icons/bullet_blue.gif) [CarbonTrackerSimple.drawio (7).png](attachments/21792644/21792675.png) (image/png)  
![](images/icons/bullet_blue.gif) [CarbonTrackerSimple.jpg](attachments/21792644/21792710.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 16:16

[Atlassian](http://www.atlassian.com/)
