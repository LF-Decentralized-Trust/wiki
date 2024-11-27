[invalid_url] err=parse "http://Greenhouse Gas Emissions from a Typical Passenger Vehicle": invalid character " " in host name url="http://Greenhouse Gas Emissions from a Typical Passenger Vehicle" 
1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Working Groups](Working-Groups_19005701.html)
4. [Carbon Accounting and Certification WG](Carbon-Accounting-and-Certification-WG_19005779.html)

# Climate Action SIG : Supply Chain Decarbonization

Created by Si Chen, last modified on Sep 29, 2022

### Objectives

This project will create a network for decarbonizing a Supply Chain, which could span multiple parties across industries and countries.  It will include an emissions ledger to record emissions data, a DAO for collectively deciding on decarbonization options, and a tokens network for transferring the emissions reductions (decarbonization) across the members of the network. 

### Use Cases

Decarbonization of supply chain, or Scope 3, emissions remains [a hard problem for many reasons](https://joshgreen.substack.com/p/why-is-it-so-hard-to-reduce-the-carbon), even as regulatory compliance, such as the [EU carbon border tax](https://www.greenbiz.com/article/eu-wants-carbon-tax-imports-would-it-be-effective-climate-solution#:~:text=What%20is%20a%20carbon%20border,companies%20to%20reduce%20their%20emissions.), the [EU Carbon Boarder Adjustment Mechanism](https://ec.europa.eu/info/sites/default/files/carbon_border_adjustment_mechanism_0.pdf) targeting imports of energy intense commodities, make it increasingly important.  Our solution offers the following advantages:

- Cost of carbon foot-printing - We're free. ![(smile)](images/icons/emoticons/smile.png)
- Creating incentives for suppliers - Customers, either big ones or a group of small ones, could set up their own "cap and trade" scheme: Declare their supply chain emissions targets which decline over time, aligning with the Paris Agreement (-50% by 2030, zero by 2050.)  Allocate tokens to suppliers based on those targets.  Suppliers can trade their emissions with each other but over time must reduce them as a whole.
- Providing turnkey solutions - Again using tokens, major customers could either invest in emissions projects directly and provide them to their customers (like [Apple](https://www.environmentalleader.com/2021/03/more-than-100-of-apples-global-suppliers-are-moving-to-100-renewable-energy/) and ["Enabling carbon neutrality across the value chain" in this article](https://chinadialogue.net/en/business/how-will-chinas-internet-giants-become-carbon-neutral/)) or provide financing or guarantees for financing for suppliers.
- Verification - Could be done through this ledger.
- Going deep - Suppliers could get their suppliers on the ledger, and tokens could be transferred further up the supply chain.
- Address the pain points, needs and interests of emerging regulations like the CBAM on the international stage
- Communicate the importance of corporate carbon reduction efforts

### Implementation

Information from a variety of sources, from freight bills of lading (BOL's) and carrier tracking information, to mobile and IOT devices attached to vehicles, will be compared against published emissions factors to determine the emissions from transportation.  

Product emissions databases can be used to determine the emissions of the component products.

The calculated emissions are either recorded on Hyperledger Fabric or encrypted and recorded on IPFS.  

Tokens are then issued using the [Emissions Tokens Network](Emissions-Tokens-Network_19006546.html).  Transportation and shipping emissions are calculated based on standard emissions factors such as the UK Government Greenhouse Gas Reporting Factors (see below) and stored as Audited Emissions.  The CarbonTracker tokens from the [Oil &amp; Gas Methane Emissions Reduction Project](19008903.html) will be used to calculate the actual carbon emissions of fuel based on the producer it was purchased from.  This is done by calculating the carbon intensity implied by the standard emissions factors and comparing it against the CarbonTracker tokens' fuel carbon intensity.  By presenting an Audited Emissions tokens based on the standard emissions factors and a CarbonTracker token for actual fuel purchased, the smart contract will calculate the difference and issue an additional Audited Emissions token.  This new token represents the adjustment for actual emissions based on the purchased fuel's carbon intensity, versus the "average" carbon intensity of the standard fuel.  It may be a positive or negative number, depending on the actual purchased fuel's carbon intensity versus the average.  

The [Decarbonization DAO](Decarbonization-DAO_19008927.html) will govern the auditing and calculation of the carbon intensity of the different producers' fuels, validation of sustainability attributes of different fuels, and any carbon offsets in addition to direct emissions reductions.

### References

- UK - Government Greenhouse Gas Reporting Factors: [2021](https://www.gov.uk/government/publications/greenhouse-gas-reporting-conversion-factors-2021), [2020,](https://www.gov.uk/government/publications/greenhouse-gas-reporting-conversion-factors-2020) and [2019](https://www.gov.uk/government/publications/greenhouse-gas-reporting-conversion-factors-2019)
- France  - [Resource centre for greenhouse gas accounting](https://bilans-ges.ademe.fr/en/basecarbone/donnees-consulter/choix-categorie/siGras/1)
- USA - 
  
  - [Greenhouse Gas Emissions from a Typical Passenger Vehicle](http://Greenhouse%20Gas%20Emissions%20from%20a%20Typical%20Passenger%20Vehicle) (EPA)
  - [GHG Protocol Emissions Calculator](https://ghgprotocol.org/ghg-emissions-calculation-tool)
  - [EPA Scope 3 Emisisons Factors](https://www.epa.gov/climateleadership/scope-3-inventory-guidance)
  - [Emissions &amp; Generation Resource Integrated Database (eGRID)](https://www.epa.gov/energy/emissions-generation-resource-integrated-database-egrid) for utilities emissions
- [Searates](https://www.searates.com/services/distances-time/) distance and time calculator for transport or similar
- [Ecoinvent](https://www.ecoinvent.org/) database or similar
- [Reformation RefScale methodology](https://www.thereformation.com/media/W1siZiIsIjIwMTgvMTAvMjMvMjAvNTIvMTYvOTg2MTk1ZjItNGVmMC00ZDZmLTk5ODgtMWIyYTQzYTc3MjczL1JlZm9ybWF0aW9uLVJlZnNjYWxlLU1ldGhvZG9sb2d5LnBkZiJdXQ/Reformation-Refscale-Methodology.pdf?sha=5b3e0143e40aea50) contains information about textile supply chain emissions calculations
- [Blockchain Mechanism for Tracking GHG Emissions through Supply Chain](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4082449)

## Examples

[Walmart Project Gigaton](https://www.walmartsustainabilityhub.com/climate/project-gigaton)

[Apple Supplier Clean Energy Program](https://www.apple.com/newsroom/2022/04/apple-helps-suppliers-rapidly-accelerate-renewable-energy-use-around-the-world/)

[IKEA Supplier Renewable Energy Program](https://about.ikea.com/en/newsroom/2021/06/10/ikea-launches-new-program-to-accelerate-suppliers-transition-to-100-per-cent-renewable-electricity)

## Development - Active Issues

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
