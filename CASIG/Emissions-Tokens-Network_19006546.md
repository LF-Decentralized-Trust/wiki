1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Working Groups](Working-Groups_19005701.html)
4. [Carbon Accounting and Certification WG](Carbon-Accounting-and-Certification-WG_19005779.html)
5. [Operating System for Climate Action](Operating-System-for-Climate-Action_19005889.html)

# Climate Action SIG : Emissions Tokens Network

Created by Si Chen, last modified on Jan 05, 2024

*This is the emissions token network from the [Operating System for Climate Action](Operating-System-for-Climate-Action_19005889.html).*

## A Demo

You can try it yourself at [https://emissions-test.opentaps.org/](https://emissions-test.opentaps.org/).  You will need to an Avalanche Fuji testnet wallet and some test eth (which you can get [here](https://docs.avax.network/build/dapp/smart-contracts/get-funds-faucet).)  Then please email [Climate SIG mailing list](https://lists.hyperledger.org/g/climate-sig) with your address to be added to it.

## How it Works

The emissions tokens network uses tokens to represent the emissions of an entity, which could be an organization, a building, or even a person.  It is the sum of all the emissions from different channels such as the [utility emissions channel](Emissions-Data-Channel_19006106.html), plus offsetting Renewable Energy Certificates and carbon offsets.  Each token represents either an emissions debt, which you incur through activities that emit greenhouse gases, or an emissions credit, which offset the debt by removing emissions from the atmosphere.

The carbon emissions token is a fungible token, whereas data on the utility emissions channel are just immutable data (not tokens), as they represent the emissions from a particular meter tied to a particular utility during a particular period of time.  Following examples from capital markets, we can link this kind of data to the fungible tokens by:

1. The underlying data, such as the utility emissions records, should be updated to link to the particular fungible token.
2. The fungible token should contain a manifest of all the underlying data which went into it.

We propose to implement a carbon emissions token based on the [eThaler](https://lf-hyperledger.atlassian.net/wiki/spaces/CMSIG/pages/20546360/eThaler+lab) project from the [Financial Markets SIG](https://lf-hyperledger.atlassian.net/wiki/spaces/CMSIG).  eThaler is a Central Bank Digital Currency (CBDC) implemented on a private Ethereum network running Hyperledger Besu.  It supports a central bank which creates and mints tokens and transfers them to member banks, who would then distribute them to retail customers of the banks. 

In the case of carbon emissions, the eThaler smart contracts could support the following participants on a tokens network:

- Token authority –  a network operator or a supranational/national/regional carbon authority (see below) which authorizes a number of issuers of tokens.
- Token issuers –  auditors of carbon emissions or certifiers of renewable energy or carbon offsets.  Auditors would issue tokens based on audits of companies' operations.   Certifiers would issue tokens based on projects they've certified.
- Token consumers – businesses and individuals who buy REC's or offsets to offset their own emissions.

#### Token Types

- Audited emissions - represents the actual emissions of an organization, as reported by an auditor.
- Carbon offsets - represents reduction of emissions through projects such as forestry, sequestration, etc.
- Renewable Energy Certificates (REC's) - represents energy generated from renewable sources such as wind and solar

The audited emissions tokens are "retired" (see below) as soon as they're issued from an auditor to a company or consumer.  The offsets and REC's could be traded but are eventually retired when used to count as emissions offsets.

#### Token Operations

- Add new token definition – Multiple types of emissions tokens can be supported on the network, such as emissions, Renewable Energy Certificates (REC's), and offsets.
- Register/Unregister issuer – In our case, it would be registering and unregistering auditors or project certifiers authorized to issue tokens.
- Register/Unregister consumer – Auditors and project certifiers would register their customers on the network.
- Issue – Issues tokens based on results of operations from audited companies and renewable/offsets projects.  Note that each issuer would be able to only issue allowed types of tokens, so an emissions auditor can issue Audited Emissions, a carbon offset developer or certifier Carbon offset tokens, and renewables developer REC's.
- Transfer – Emissions audit tokens cannot be transferred: They are retired as soon as issued and stay with the organization that was audited as a record of their emissions.  Offsets and REC's can be transferred until they are retired.  The total amount that could be transferred from one account to another is the sum of the tokens in their account minus the amount that has been retired.
- Retire - this is not in eThaler but would need to be implemented.  When a token is marked as "retired," it is counted towards the emissions reduction of the retiring organization and cannot be transferred again.
- Burn – this would not be implemented.

The [Carbon Emissions token taxonomy developed by the Interwork Alliance](https://github.com/InterWorkAlliance/TokenTaxonomyFramework/blob/master/artifacts/token-templates/specifications/CET/latest/CET-spec.pdf) is similar to eThaler's token taxonomy.  The differences are:

1. Currency could be repeatedly transferred between parties, where as emissions records, offsets, and REC's should not be.
2. Currency could be removed from circulation or "burned", but emissions records could not be, because the physical greenhouse gases stay in the atmosphere (hundreds of years at least.)

The emissions tokens would have the following fields:

- issuer identifier
- recipient identifier
- token type
- quantity
- UOM
- from date/time stamp
- thru date/time stamp
- metadata
- manifest
- date/time stamp of when the asset was created
- automatic retirement date, when the token will be retired in the account of whoever holds it.  Usually the end of a calendar year.

Examples of these tokens/assets include:

- Renewable Energy Certificate:
  
  - Issuer ID = Generator of REC
  - Recipient ID = Buyer of REC
  - Asset Type = REC
  - Quantity = 1
  - UOM = MWH
  - From/thru date time stamp = *do we need this for REC's? time period of the energy generation?*
  - Metadata = Region and Time of energy generated
  - Manifest = URL linking to the registration for the REC purchased
- Carbon emissions offest:
  
  - Issuer ID = Certifier or Issuer
  - Recipient ID = Buyer
  - Asset Type = Emissions Offset
  - Quantity = amount
  - UOM = MtCO2e
  - From/thru date time stamp = *do we need this for emissions offset?*
  - Metadata = type of project, location, etc.
  - Manifest = URL linking to the registration of the emissions offset
- Audited Emissions:
  
  - Issuer ID = auditor
  - Recipient ID = organization or entity
  - Asset Type = CO2 emissions
  - Quantity = amount of emissions
  - UOM = MtCO2e
  - Metadata = *Region and Time of emissions?*
  - From/thru date time stamp = time period of the net emissions *(Why not gross emissions (before offset)?)*
  - Manifest = links to access all the emissions tokens/assets used to prepare this net emissions

With these tokens, we can calculate the net emissions by first subtracting the effect of Renewable Energy Certificates (REC's.)  REC's offset the energy produced by non-renewable sources in designated jurisdictions. This feature requires differentiation of the non-renewable from renewable energy to be specified in the original emissions tokens/assets from utility emissions data channel.  Then we subtract the offsets to get the net emissions in the jurisdictions that allow that accounting method.

### **Integration with Hyperledger Fabric**

This network would be connected with Fabric channels such as the [utility emissions channel](Emissions-Data-Channel_19006106.html) through the auditors.  The utility emissions channel is operated by an auditor on behalf of its customers.  The auditor would also be on this network and would issue audited emissions tokens to its customers' wallets.  The customers would then transact in emissions and offsets on this network using their wallets. 

### **Possible Use Cases**

Cap and Trade:

- The central bank could be the cap and trade authority.
- Tokens for allowable emissions could be issued to all members of the cap and trade regime.
- They can trade the tokens amongst themselves.
- As emissions are counted, during an audit, cap and trade tokens should be retired.

Green Bank:

- The central bank is a green bank, which raises funds for climate projects.
- For approved projects, the bank would issue emissions tokens to project developers based on the projected emissions reductions of the projects. *Wouldn't that make the bank an issuer? Shouldn't the issuer only issue offsets upon verification that the projected emissions reductions have actually been reduced or projected emissions removals have actually been removed?*
- When the *actor's* emissions reductions are verified, the *certificate authority* exchanges them for tokens.
- The tokens can then be redeemed for money. *Don't issuers have yet to validated verified reductions before node operators register them on blockchain thus making them available for exchange?*

Network Operator Model:

- The network operator is a neutral, blockchain technology vendor who runs the network for a (very very very small) fee.
- It could mint and issue tokens in response to requests from network members, who pay a fee for the tokens to be issued.

### **Outstanding Issues**

Transfer of emissions down the supply chain and avoiding double counting are major issues to be addressed in the future.  The problem is that emissions are counted in multiple ledgers, for example [this document from Gold Standard](https://www.goldstandard.org/sites/default/files/documents/a_new_paradigm_for_voluntary_climate_action.pdf) describes how they could be counted in both offsets and national registries.  See also the [Gold Standard double counting guidelines document](https://www.goldstandard.org/sites/default/files/documents/2015_12_double_counting_guideline_published_v1.pdf). *Doesn't including the interval dates, location coordinates, and tax map key in the metadata prevent double counting?*

## Get Involved

# Get Involved

#### This is an open source project and anyone is welcome to get involved and we will be happy to see you contribute.

1\) Start by subscribing to the [Climate SIG mailing list](https://lists.hyperledger.org/g/climate-sig) for updates and meeting notifications.

2\) Join our bi-monthly Peer Programming Zoom call for developers on Mondays at 9 AM US Pacific time (UTC-07:00 America/Los Angeles.) Please [check the calendar for the next call](https://lists.hyperledger.org/g/climate-sig/calendar). 

3\) Check out the [good first issues from our blockchain-carbon-accounting in Hyperledger-labs](https://github.com/hyperledger-labs/blockchain-carbon-accounting/issues) and feel free to contribute a fix for one that looks interesting to you.

4\) See our [How to Contribute](How-to-Contribute_19006806.html) page for other ways how you could get involved. 

![](plugins/servlet/confluence/placeholder/unknown-macro)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Climate SIG Presentation.png](attachments/19006546/19006569.png) (image/png)  
![](images/icons/bullet_blue.gif) [Emissions Tokens Network.png](attachments/19006546/19006739.png) (image/png)  
![](images/icons/bullet_blue.gif) [Blockchain Transparency and Access to Liquidity v 1.1 March 23 2017 \[Autosaved\] (1).jpg](attachments/19006546/19006794.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [image2021-3-7\_17-57-52.png](attachments/19006546/19006859.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
