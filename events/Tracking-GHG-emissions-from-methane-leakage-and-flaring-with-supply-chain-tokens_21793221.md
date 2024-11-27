1. [Community Events](index.html)
2. [Community Events Home](Community-Events-Home_21790731.html)
3. [Challenges](Challenges_21792347.html)
4. [Hyperledger Challenge 2022](Hyperledger-Challenge-2022_21792351.html)
5. [Prototype Challenge](Prototype-Challenge_21792363.html)
6. [Prototype Submissions](Prototype-Submissions_21793182.html)

# Community Events : Tracking GHG emissions from methane leakage and flaring with supply chain tokens

Created by Bertrand WILLIAMSRIOUX, last modified on Nov 05, 2022

***Innovation Tagline:**  Using the blockchain to create supply chain incentives to reduce 1 Gt CO2e of from methane flaring and fugitive emissions* 

**Project Keywords:**  Methane emissions, oil &amp; gas, flaring, supply chain, NFT, 

## Project Members

1. [Bertrand WILLIAMSRIOUX](https://lf-hyperledger.atlassian.net/wiki/people/712020:57613290-3ad4-4f53-8166-19a9bdb9c047?ref=confluence) [Si Chen](https://lf-hyperledger.atlassian.net/wiki/people/557058:c49c10c4-25bf-4187-b582-b521c3c33223?ref=confluence) [Woody Moore](https://lf-hyperledger.atlassian.net/wiki/people/70121:310f5eae-a11b-435a-ae52-42b0a796fe0b?ref=confluence) [Arezkidji](https://lf-hyperledger.atlassian.net/wiki/people/557058:f648e1dc-1c53-470f-a796-f2f1c040b884?ref=confluence)

## Prototype Outcomes

### Presentation

Note: Font is not correct in the browser viewer.  Please download the presentation.

*[![](attachments/thumbnails/21793221/21793367)](attachments/21793221/21793367.pptx)*

### Project Repository

[https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/carbon-tracker](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/carbon-tracker)

### Demo

## Problem and Solution

Even as we reduce our Greenhouse Gas (GHG) emissions to stop climate change, the oil and natural gas industry will remain a central part of the global energy system for decades.  In this period, a top priority is to reduce the amount of methane, the primary component in natural gas, that is leaked and flared during production ([see original submission](https://lf-hyperledger.atlassian.net/wiki/display/events/Reducing+Methane+Leakage+and+Flaring+through+Supply+Chain+Tokens)). It is estimated that in 2020 more than 260 bcm of methane was wasted by the industry. Based on 5 year moving average natural gas prices globally, this is more than $60 billion dollars in market value. It represents 7% of global natural gas consumption, and more than 1.7 times what the EU imported from Russia.

The waste also represents at least 2.5 Gt of CO2e, equivalent to emissions from 1.3 billion cars and more than 5 % annual global GHG emissions. The IEA estimate that around 70% of global methane venting and leakage by the oil and gas industry can be technically avoided. Ina addition a significant portion at no net cost when accounting for the revenues that could be generated from selling the gas ([IEA 2022](https://www.iea.org/articles/methane-tracker-database)).

There is a real commercial opportunity to reduce this waste by delivering the methane as natural gas to local an international markets. However the commercial incentive is not always enough, as there are several technical and investment barriers associated with getting the fuel to market. Moving forward efforts to reduce wasted methane will require greater regulatory push and the voluntary pull from consumers concerned with the carbon footprint of the commodities they purchase.

There are several challenges that must be addressed. First improving the quality and accessibility of data about the methane emissions of specific facilities and producers, both to provide stronger regulatory oversight,  but also to enable consumer and investors to make informed decision about waste emissions, and tracking the indirect GHG impact across a value chain, i.e., Scope 3 emissions. 

We are developing a solution leveraging the following features of blockchain technology.

1. A Decentralized Autonomous Organization (DAO) to organize how Auditors are selected and paid to verify proposals to certify waste emission. This can include Oracle services to bridge real world emission data from different sources (corporate reports, onsite sensors, and independent satellite data) with the processing of emission proposals
2. A token network for issuing verified emission certificates. These certificates are programmed using a Non Fungible Token (NFT) model, [as detailed in this working paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4081426). The resulting token economy can serve different market/business applications:
   
   1. **Commodity differentiation (e.g., [Responsibly Sourced Gas](https://xpansiv.com/digital-fuels/?gclid=Cj0KCQjwspKUBhCvARIsAB2IYusto3i9K-hHUa0nfBc-O4xLOezPCA7mvNFZmLerEJFA9dT72l6EPNkaAiq5EALw_wcB) in sustainable commodity markets)** 
      
      1. Allow buyers of fuel (e.g., oil or natural gas) to purchase certificates at a premium verifying that they contain lower waste emissions than a regional benchmark or average.
      2. Facilitate the tracking of waste emissions in a fuel supply chain by linking emission certificate NFTs. This can help reduce the transaction costs associated with determining value chain emissions impacts (indirect Scope 3).
   2. **Comply with ESG commitments by investors and lender . Surrender NFTs for:**
      
      1. Preferential interest rates to finance emission reduction efforts
      2. Proof of compliance with investor ESG requirements

For more technical details, please see [Oil &amp; Gas Methane Emissions Reduction Project](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=19008903). 

#### Minimum viable product

Our final prototype presented in the video submission (above) is an extension of the [Net EmissionToken project](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/net-emissions-token-network) where emission certificates for oil and gas producers can be issued by auditors, detailing the total methane emissions and product details for a production facility. IN our prototype an auditor issues emission certificates for oil and natural gas producers in different basins in the U.S. (Bakken, Niobrara and Permian). These emission certificate NFTs can then be traded with a Natural Gas Utility distribution company (see Figure 1).

![](attachments/21793221/21793281.png?height=250)

Figure 1: Map of production based supplying a natural gas utility company

Within the portal 

1. Oil and natural gas producers and utility company are registered
2. A registered auditor issues a certificate for a producer in each basin [using available data collected in this google sheet](https://docs.google.com/spreadsheets/d/1PQ2qz-P9qing_3F3BmvH6g2LA1G9BdYe/edit#gid=689160760)
3. Each certificate (NFT) contains:
   
   1. individual audited emission tokens for total amount of flared and vented methane emissions.
   2. product details*
   3. the emission factor for each product: total amount of methane emissions attributed to each product / total emissions.
4. A buyer (Gas Utility Company) can view emission certificates from producers in each basin. Certificates are color-coded based on how the emission factor compare to a reference value (in our example we use the average oil and gas methane emissions of all U.S. producers)
   
   1. Dark green illustrate lower emission factors
   2. Dark red illustrate higher emission factors
5. Gas Utility acquires product shares in the NFT, certifying the total waste methane emissions from products purchased.

\* Not all product information needs to be stored within the blockchain NFT contract. Some information (e.g., customer details, product names, and phsycial product units may be considered private or sensitive commercial trade secretes. An auditors can produce an off-chain signature that can be used to independently verifies the product information provided to stakeholders provided ith product details by the certificate holder (e.g., a consumer, investor regulator)

### Why is our solution better than what exists?

Currently no comprehensive, transparent solution for tracking methane emissions exists.   Existing solutions are either proprietary and not open to the general public, or they only incorporate one source of data (company-reported, satellite-based, or ground instrument-based).  What solutions do exist only apply to the oil and gas producers and do not transfer the emissions impact to the energy users and the ultimate consumers.

Our solution is the only one which:

- Incorporates all sources of data, from governments and NGO's to satellites to ground instruments
- Is transparent and fully open for inspection
- Transfers emissions impact from oil producers to utilities to the end consumers

### Environmental, Social, and Governance Impact

This project is directly aimed at solving a major source of Greenhouse Gas (GHG) emissions.  Its potential Environmental impact is enormous, since methane leakage and flaring is approximately equal to the GHG emissions of all the cars in the world.  

Further, reducing methane leakage and flaring would improve air quality in remote and developing areas, which would help with social development in those areas.

Finally, this project aims to improve transparency of emissions disclosure in the energy industry and thereby the governance of the global energy industry.

### Community Engagement

We've posted regularly on the mailing list, started discussions on the github forum, and hosted a call with the Climate SIG:

- Mailing list: [April 25](https://lists.hyperledger.org/g/climate-sig/topic/update_on_the_methane_project/90697059?p=%2C%2C%2C20%2C0%2C0%2C0%3A%3Arecentpostdate%2Fsticky%2C%2C%2C20%2C2%2C0%2C90697059%2Cprevid%3D1652713202926910305%2Cnextid%3D1649091513846790517&previd=1652713202926910305&nextid=1649091513846790517), [April 19](https://lists.hyperledger.org/g/climate-sig/topic/hyperledger_blog_about_the/90565740?p=%2C%2C%2C20%2C0%2C0%2C0%3A%3Arecentpostdate%2Fsticky%2C%2C%2C20%2C2%2C0%2C90565740%2Cprevid%3D1652713202926910305%2Cnextid%3D1649091513846790517&previd=1652713202926910305&nextid=1649091513846790517), [April 15](https://lists.hyperledger.org/g/climate-sig/topic/update_on_methane_project_and/90491454?p=%2C%2C%2C20%2C0%2C0%2C0%3A%3Arecentpostdate%2Fsticky%2C%2C%2C20%2C2%2C0%2C90491454%2Cprevid%3D1652713202926910305%2Cnextid%3D1649091513846790517&previd=1652713202926910305&nextid=1649091513846790517), [April 6](https://lists.hyperledger.org/g/climate-sig/topic/update_on_the_methane_project/90301974?p=%2C%2C%2C20%2C0%2C0%2C0%3A%3Arecentpostdate%2Fsticky%2C%2C%2C20%2C2%2C0%2C90301974%2Cprevid%3D1652713202926910305%2Cnextid%3D1649091513846790517&previd=1652713202926910305&nextid=1649091513846790517), [March 18](https://lists.hyperledger.org/g/climate-sig/topic/methane_emissions_reduction/89877872?p=%2C%2C%2C20%2C0%2C0%2C0%3A%3Arecentpostdate%2Fsticky%2C%2C%2C20%2C2%2C20%2C89877872%2Cprevid%3D1649089504706495382%2Cnextid%3D1647270002019842719&previd=1649089504706495382&nextid=1647270002019842719)
- Github discussion: [Vote on methane global warming potential time horizon](https://github.com/hyperledger-labs/blockchain-carbon-accounting/discussions/530)
- Climate SIG call: [CA2 SIG - Meeting May 17](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19009226/CA2+SIG+-+Meeting+May+17)

Engaged members of the community include:

- [kamlesh nagware](https://lf-hyperledger.atlassian.net/wiki/people/557058:8e1fc425-f938-4b39-ad13-9cd8b0ddde52?ref=confluence)
- [David Rowe-Francis](https://lf-hyperledger.atlassian.net/wiki/people/712020:86eded58-dbcd-4998-9867-6a1f3649f491?ref=confluence)
- [Randy Givens](https://lf-hyperledger.atlassian.net/wiki/people/70121:bf83ef5d-4a48-4d3e-8ef4-457fb353a796?ref=confluence)
- [Vipin Bharathan](https://lf-hyperledger.atlassian.net/wiki/people/70121:4ac24c34-2385-41a8-8881-61e7a75c6d1e?ref=confluence)
- [Joseph Wyer](https://lf-hyperledger.atlassian.net/wiki/people/5efbbcd5deb6ca0baa2674e0?ref=confluence)

We have also held discussion with the [World Bank Global Gas Flaring Reduction Partnership](https://www.worldbank.org/en/programs/gasflaringreduction)

## Project Plan

So far we have completed the following for the prototype submission

- Collect the methane emissions and production of oil and gas producer at national and regioanl (U.S. basin level) combining industry reports and independent data: [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/spreadsheets/d/1PQ2qz-P9qing_3F3BmvH6g2LA1G9BdYe/edit#gid=689160760)
- Illustrate the verification of emissions in line with recognized standard setting body practices - e.g., GHG Corporate Protocol Reporting
- Setup a Non-Fungible Token (NFT) model for tracking value chain emissions. Used to issue emission certificates for oil and gas producers, and send product shares in the NFT to fuel buyers.
- Setup User interface to register Users (Auditors, Oil &amp; Gas Industry, Gas Utility Company) to participate in certificate market.

We plan on extending the prototype in several ways.

1. **June/July** Build the data management system for storing methane emission and production data used to issue emission certificate (NFT) proposals
   
   1. Includes transferring data from google spread sheet to a Fabric emission channel data network, or IPFS dataset.
   2. Develop system to manage different type commercially sensitive and public data
      
      1. Private product details (e.g.,physcial quantity of fuel produced and sold to consumers)
      2. Public audited emission data
2. **July/August** Setup procedure for processing emission data into emission certificates
   
   1. Setup a DAO to process emission certificate proposals:
      
      1. request NET and product tokens
      2. Link NET and product tokens to emission certificate NFTs
   2. Use DAO to select auditors that verify claims using available emissions data (Fabric, IPFS, ...)
3. **August/September** NFT Contract is run as a hardhat (Ethereum) development network. next step is to deploy to a live public Ethereum networks, and launch a public React Dapp to display emission performance across different oil and gas production regions.

## Project Resources &amp; Support

We are organizing a Hyperledger mentorship - [Multiple Data Integration to Fabric Climate Accounting Network](https://mentorship.lfx.linuxfoundation.org/project/79ce0bff-4a7c-4377-8d14-b0a347346f9c) to support development over the next 6 months.

Will start publishing development issues to encourage other young developers to participate

Actively participate in the development of the [blockchain-carbon-accounting](https://github.com/hyperledger-labs/blockchain-carbon-accounting/pull/549) project to take advantage of new features and improvements developed by the community

The project will be adopted and managed by Two Ravens Energy &amp; Climate (E&amp;C) Consulting Ltd., an independent consultancy set up by the Project lead [Bertrand WILLIAMSRIOUX](https://lf-hyperledger.atlassian.net/wiki/people/712020:57613290-3ad4-4f53-8166-19a9bdb9c047?ref=confluence). Bertrand will maintain the project for the next 9 months as the directory of Two Ravens E&amp;C Consulting Ltd, and will work towards aquiring staff to support both the devleopment and commercialization of the prototype.

## Industry Adoption

Two Ravens E&amp;C Consulting Ltd. is currently preparing application to incubator and accelerator programs to engage with stakeholders from the energy industry, regulators.

- Application for 2023 Techstars LaunchPool and Equinor programs  : [https://www.techstars.com/accelerators/equinor-energy](https://www.techstars.com/accelerators/equinor-energy), [https://www.techstars.com/accelerators/launchpool-web3](https://www.techstars.com/accelerators/launchpool-web3)
- Creative Destructive Lab mentorship program: [https://creativedestructionlab.com/application-triage/](https://creativedestructionlab.com/application-triage/)
- Applying for funding with the Government of Canada: Emissions Reduction Fund: working together to create a lower carbon future - [https://www.nrcan.gc.ca/science-and-data/funding-partnerships/funding-opportunities/current-funding-opportunities/emissions-reduction-fund/22781](https://www.nrcan.gc.ca/science-and-data/funding-partnerships/funding-opportunities/current-funding-opportunities/emissions-reduction-fund/22781)

## Attachments:

![](images/icons/bullet_blue.gif) [Flaring data EDF.png](attachments/21793221/21793222.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-5-18\_11-33-28.png](attachments/21793221/21793280.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-5-18\_11-36-7.png](attachments/21793221/21793281.png) (image/png)  
![](images/icons/bullet_blue.gif) [Methane Reduction Presentation.pptx](attachments/21793221/21793367.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/21793221/21793283.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:18

[Atlassian](http://www.atlassian.com/)
