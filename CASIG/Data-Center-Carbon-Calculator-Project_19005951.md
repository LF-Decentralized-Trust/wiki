1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Project Ideas Board](Project-Ideas-Board_19005952.html)

# Climate Action SIG : Data Center Carbon Calculator Project

Created by Si Chen, last modified by Andrea Frosinini on Apr 23, 2023

A first application of the [Operating System for Climate Action](Operating-System-for-Climate-Action_19005889.html) of the [Carbon Accounting and Certification WG](Carbon-Accounting-and-Certification-WG_19005779.html) is an application to allow data centers to credibly prove that they're carbon neutral with trusted data and Renewable Energy Certificates (REC's) and carbon offsets.

We chose data centers as our first application because:

- Data center have high energy use.  Energy is a data center's highest operating expense and could be about half of all its expenses.  ([Uptime Institute's Simple Model for Determing True Total Cost of Ownership for Data Centers](https://www.missioncriticalmagazine.com/ext/resources/MC/Home/Files/PDFs/%28TUI3011B%29SimpleModelDetermingTrueTCO.pdf).)
- Globally, data centers use 103 terawatt hours of electricity (See [Recalibrating global data center energy-use estimates](https://science.sciencemag.org/content/367/6481/984.abstract)), about 1% of the global electricity output.  This is equivalent to the energy use of 17 million American households ([NYTimes.com](https://www.nytimes.com/2020/02/27/technology/cloud-computing-energy-usage.html)) with a total carbon emissions footprint on par with those of airlines ([BBC.com](https://www.nytimes.com/2020/02/27/technology/cloud-computing-energy-usage.html))
- Data center energy use can obtained from utility energy bills, many of which are electronically available via the [Green Button data standard](http://www.greenbuttondata.org/).
- Major cloud services providers are focused on improving data center energy efficiency, both as a competitive advantage and as a way to meet their climate goals.  Microsoft, for example, has committed to becoming carbon neutral, while Google has made both sigificant investments in data center efficiency and renewable energy.

The application would use several permissioned Hyperledger channels, as described in the the [Operating System for Climate Action](Operating-System-for-Climate-Action_19005889.html), on these inputs:

- Data center meta-data, such as its name and location.
- Data center activity metrics, such as the number of U-racks of servers or the amount of CPU compute units, storage, and bandwidth provided during a time period.
- Utility bills for the data center.
- CO2 emissions of the utilities, obtained from the [Emissions &amp; Generation Resource Integrated Database (eGRID)](https://www.epa.gov/energy/emissions-generation-resource-integrated-database-egrid) of the EPA.
- Renewable Energy Certificates (REC's) purchased and retired by the data center.
- Carbon offsets purchased by the data center.

The permissioned ledgers would include:

- Energy use data, which could come from any combination of
  
  - Utility channel – This would be a ledger for the utility bills, set up by utility or its service provider, for its customers.  It would issue tokens for each customer based on the carbon footprint of their energy purchased, which would be calculated based on the utility bill for the customers and the utility's overall emissions.
  - UPS log data – Uninterrupted Power Supply (UPS) for the servers which could provide a log of power use by the servers.  This could then be used to estimate the HVAC costs for the servers based on models of cooling requirements for the server's space.  This method could be used when the data center does not have its own meter or utility bill and is instead aggregated with other building or campus utility bills.
  - Server utilization data – This could come directly from the servers themselves, which could report their up time and load levels.  This data could then be combined with models of energy use for the servers and their required HVAC to come up with energy usage.  This would be useful for determining the effects of software running on the servers.
- RECs and carbon offsets from the [Emissions Tokens Network](Emissions-Tokens-Network_19006546.html)

The data center would subscribe to all of the above channels and use the tokens to calculate its energy use with a smart contract which:

1. Sum up the total energy (kWH of electricity) used by the data center,
2. Subtract the REC's
3. Calculate CO2 emissions from the difference of (1) - (2) using utility-specific emission data
4. Subtract carbon offsets

The total carbon footprint could then be divided by the activity metric of the data center.  Initially, that could simply be the number of U-racks.  An added enhancement would be to break out the equipment of the data center by type, for example by compute servers, storage, and network switches.  We can then use their power ratings to allocate the carbon footprint to the different equipment and come up with the carbon footprint per compute units, storage, and bandwidth. 

Finally, a token or asset could be issued for each unit of activity to the customers of the data center, so that they could use it in their CO2 accounting.

Note that such a calculator is only calculating the carbon footprint of the existing equipment in a data center.  It could be expanded eventually to cover the full Greenhouse Gas Protocol for data center, so that it could be used to certify a "carbon neutral" data center.  That would require accounting for all the Scope 3 emissions, including the carbon footprint of new capital assets (servers), employee commuting and business travel, and other purchased supplies and equipment.

We could implement this MVP application using the [True TCO Calculator for Data Centers](https://www.itbusinessedge.com/itdownloads/true-tco-calculator/88634), as described in this [Uptime Institute white paper](https://www.missioncriticalmagazine.com/ext/resources/MC/Home/Files/PDFs/%28TUI3011B%29SimpleModelDetermingTrueTCO.pdf).      

## References

- [Why green cloud optimization is profitable for you and the planet (ThoughtWorks)](https://www.thoughtworks.com/insights/articles/green-cloud)
- [Building Data Center of the Future (Data Center Frontier)](https://datacenterfrontier.com/building-data-center-of-the-future/)
- [Data centers are more energy efficient than ever (Google)](https://blog.google/outreach-initiatives/sustainability/data-centers-energy-efficient/)

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
