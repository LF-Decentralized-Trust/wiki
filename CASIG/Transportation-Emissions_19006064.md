1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Working Groups](Working-Groups_19005701.html)
4. [Carbon Accounting and Certification WG](Carbon-Accounting-and-Certification-WG_19005779.html)
5. [Supply Chain Decarbonization](Supply-Chain-Decarbonization_19006065.html)

# Climate Action SIG : Transportation Emissions

Created by Si Chen, last modified on Apr 20, 2022

Transportation accounts for 1/4 to 1/5 of global Greenhouse Gas (GHG) emissions, or 8 billion tCO2e per year.  Of this 75% comes from road vehicles, 12% from aviation, and 10% from shipping.  (Source: [Our World in Data](https://ourworldindata.org/co2-emissions-from-transport))

![](attachments/19006064/19008694.png?height=250)

This project builds a blockchain network to calculate emissions from transportation and verify emissions reductions in transportation.  It could be used with a mobile app to track your own personal emissions for traveling or transportation and logistics emissions as part of the [Supply Chain Decarbonization](Supply-Chain-Decarbonization_19006065.html). 

## Requirements

### Mobile App

Using a mobile phone to track travel is quite complex.  Fortunately, there is an open source project called "e-mission" which provides a lot of the infrastructure for it.  See "E-Mission Mobile App" below and the paper "[e-mission: an open source, extensible platform for human mobility systems](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2019/EECS-2019-180.html)"

We could build upon e-mission to create a mobile app which will capture travel information and integrate with the Blockchain network (see below.)  The mobile app could be used by an individual to track their travel, or attached to a truck, ship, airplane, or cargo container to track its transportation.  The mobile app could offer useful services in addition to tracking trips and calculating emissions, such as maps for drivers and cyclists, looking for shared rides or bikes, or booking or checking on flights, etc.

Features of the mobile app:

- Set up vehicles - Set up type of car or other mode of transportation
- Initiate trip - Choose vehicle and click on Start
- Trip tracking - GPS signals record location of the device during the trip
- End trip - Click on End
- Sync - Use web socket security to sync travel information with Blockchain network
- Status - Visualize trips and emissions.

Integration with the blockchain network will be via the [web socket security](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities) wallet on the mobile client.

See our [2021-12-20 Peer Programming Call](2021-12-20-Peer-Programming-Call_19008698.html) for a discussion about developing this mobile app and integrating it with the blockchain network.

### Blockchain Network

A Fabric blockchain will receive the travel records from either the mobile app or other sources such as shipping manifests (UPS, freight carriers) or employee travel systems (Concur).

The blockchain will not store the travel records.  Instead, each record will be hashed to preserve audit trail.

Blockchain will calculate and record the emissions from the travel records and link back to the original source with a record of its keys.

To do this correctly, the Blockchain will need to validate:

- Mode of transportation (ie drive, bike, fly, type of car), based on origin, destination, and time of travel to calculate the average speed and verify that this is reasonable given the mode of transportation.
- Fuel use - electronic certificate or token of sources of electricity for EV's or sustainable fuel for aviation and cars.
- Sharing - Simultaneous record of travel from other people on the network to prove you shared a ride.
- Claimed emissions - Programs such as [UPS Carbon Neutral](https://www.ups.com/gb/en/help-center/shipping-support/carbon-neutral/recipient.page) or the [Delta Airlines Flight to Net Zero](https://news.delta.com/update-our-path-net-zero) involve both reductions and offsets.  The blockchain can collectively validate these programs' claimed emissions reductions.

### Tokens of Emissions Reduction

Tokens of emissions reduction from travel will be issued by a DAO.  The DAO will vote on:

- Chain code for validating the mode of travel, emissions calculations, and ride sharing
- Validity of fuel certificates
- Baseline for travel emissions based on expected mode and fuel use

The DAO can issue tokens for verified travel reduction.

### E-Mission Mobile App

[NREL OpenPath](https://www.nrel.gov/transportation/openpath.html) (formerly e-mission) provides a [mobile app](https://github.com/e-mission/e-mission-phone) which captures travel information and send them to a server. 

Here are some screenshots of what it looks like:

![](attachments/19006064/19008722.jpeg?height=250) ![](attachments/19006064/19008726.jpg?height=250) ![](attachments/19006064/19008723.jpg?height=250)

You can try it out yourself by downloading this APK and installing it on an Android phone:

[![](attachments/thumbnails/19006064/19008721)](attachments/19006064/19008721.apk) 

Once you download it:

- Turn off Power Saving Mode in your phone
- Do not optimize power savings or monitoring for this app.
- When signing in, it will prompt you for an email.  You just need a username from our server.  Email Si on the [Climate-Sig mailing list](https://lists.hyperledger.org/g/climate-sig) for one.

See their github issues #[693](https://github.com/e-mission/e-mission-docs/issues/693) and #[694](https://github.com/e-mission/e-mission-docs/issues/694) for how to set it up correctly, as well as details about how this interesting app works.  See [this page](https://github.com/e-mission/e-mission-server/blob/master/front/server/carbon_calc_details.html) for how it calculates emissions from travel.

## Other resources

- [This program](https://www.prnewswire.com/news-releases/worlds-first-validated-and-registered-carbon-offset-project-for-electric-vehicle-chargers-announced-by-scs-global-services-electrify-america-and-verra-301097406.html) from the Connecticut Green Bank serves as an example of certifying emissions reductions from electric vehicles.
- The [emissions calculation channel](Emissions-Data-Channel_19006106.html) (currently being refactored from just utility emissions) will calculate emissions based on the type of travel and distance and store them on Fabric.
- Emissions factors for different types of travel and transportation is available from the data sources of the [Supply Chain Decarbonization](Supply-Chain-Decarbonization_19006065.html).
- Calculated Emissions could then be tokenized on an [emissions tokens network](Emissions-Tokens-Network_19006546.html)
- Emissions reduction certification by the [DAO](DAO_19007052.html).

## Attachments:

![](images/icons/bullet_blue.gif) [Transport-CO2-emissions-by-mode-bar-chart-1536x606.png](attachments/19006064/19008694.png) (image/png)  
![](images/icons/bullet_blue.gif) [e-missions-phone.apk](attachments/19006064/19008721.apk) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [145657454-b766ec0d-2c34-4dbf-a711-4d4a050901f0.jpeg](attachments/19006064/19008722.jpeg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [Screenshot\_20211216-084559\_emission.jpg](attachments/19006064/19008723.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [Screenshot\_20211210-164404\_emission.jpg](attachments/19006064/19008726.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
