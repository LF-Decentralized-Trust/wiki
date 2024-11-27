1. [Hyperledger](index.html)
2. [LF Decentralized Trust](LF-Decentralized-Trust_19595266.html)
3. [Special Interest Groups](Special-Interest-Groups_19595400.html)
4. [SIG Process - Launch &amp; Operations](19595382.html)
5. [SIG Proposals](SIG-Proposals_19595405.html)
6. [SIG Archived Proposals](SIG-Archived-Proposals_19599815.html)

# Hyperledger : Capital Markets SIG Proposal

Created by Marta Piekarska-Geater, last modified by Natalia Garciagonzalez on Aug 28, 2019

### The CM-SIG has been launched, please visit the [wiki page](https://lf-hyperledger.atlassian.net/wiki/display/CMSIG/Capital+Markets+SIG) to get the latest status. Most of this material has been imported into the wiki in one form or another.

### Welcome! Sign up below in the Interested Parties table to join as a founding participant of this group. The Interested Parties table has been imported as the members table for the launch.

### Introduction

Capital Markets are a way to connect investors and borrowers for long term provision of capital. A way to invest in enterprises, so that funds from investors are put to productive use. Investors or lenders can be individuals or other entities.  Borrowers are companies and governments. Although the term market applies to exchanges and associated infrastructure; financial intermediaries like banks connect the various parties together. Investors are compensated directly by borrowers or are rewarded by appreciation of long-term securities. Capital Markets include the stock market and the bond market dealing with equities, bonds, and credit markets. They can also include derivatives.   

### Why should this group be launched?

This large vertical is not currently covered by any SIG in Hyperledger.  Finance is the Ur Use Case for blockchain.

We have a Trade Finance SIG in Hyperledger. Trade Finance deals with financing international and domestic trade primarily by banks. There is exposure to the primary documents connected to trading of goods and services. On the other hand, the Capital Markets SIG will focus on Markets which deal in securities that are fungible, open, regulated heavily and have a lot more flow and participation. Please see the scope section below to get a better feel for the Capital Markets proposal.  

### Scope

The Capital Markets SIG will study how Hyperledger DLTs interact with Capital Markets use cases.  From issuance and trading of instruments to continued market-making, dispersal of risk ; program-trading; regulation; capital requirements; traceability; pre-trade analysis and valuation; post-Trade settlement with custody; bookkeeping and corporate actions; repos. Are there architecture, identity, performance related considerations specific to Capital markets and DLTs. These are questions to be answered by this SIG. In the beginning we attempt to develop a taxonomy of the domain by viewing it in a couple of dimensions.

We will not discuss commodities and currency markets; although there are integration points with respect to hedging.  No macro economic or general policy discussions. Payment systems remain a question mark. Retail banking also a question mark. Even if we do not discuss these, we may have to build bridges to them.

Just like the Healthcare SIG, this might have a number of sub-groups to be decided by the participants and by the natural sub-domains, but the Capital Markets SIG can remain the overall umbrella over these sectors. The use of DLTs which is a collaborative and unifying technology can also knit together these sub-domains under the Capital Markets SIG.   

What are the oracles (external sources) needed, pricing/market data, analytics- rules and regulations, continuous KYC and other concerns and emerging trends are also the domain of the Capital Markets SIG.

Work Products

The anticipated initial work products will include (but is not limited to):

Develop a simple taxonomy of Capital Markets; first concentrating on the flow and fungibility of securities (bonds and stocks) ; issuance, trading, settlement, custody and corporate actions (payment of dividends, shareholder communications, buy backs etc).

### Collaborators (other groups):

Performance and scale WG to look at generating benchmarks in the Capital Markets phase. What are the architectural implications (architecture WG). Banking &amp; KYC with IDWG. Look at already developed use cases in this sector in Hyperledger DLTs (Fabric, Sawtooth, Iroha, Quilt, Burrow).  Collaborate with the Public Sector SIG for getting a window into Capital Markets regulation.

Look at the work being done by the Trade Finance SIG which covers a specific sector of the financial markets.

### Interested Parties:

The following individuals have already expressed an interest in joining this SIG, and we hope they will become contributors over the first year:

List of interested parties listed with their consent, including name, association, and optionally email addresses.

#NameAssociationContactTo be moved into member directory (optional)

1

Vipin Bharathan[DLT LLC](http://www.dlt.nyc)[vip@dlt.nyc](mailto:vip@dlt.nyc)Vipin has many years of experience in Capital Markets implementing and running front-to-back systems concentrating on Risk and P&amp;L systems, now working on applied DLT.2Jonathan LeviHACERA, The Unbounded Networkjonathan@hacera.comwho transitioned his banking career to focus on decentralized and distributed systems, also in highly regulated markets.3Kelly MathiesonDigital Assetkelly.mathieson@digitalasset.com

Head of Enterprise Solutions at Digital Asset.  Over 30 years of financial services and capital markets experience, predominantly at J.P.Morgan (Corporate &amp; Investment Bank, Asset Management and Treasury &amp; Securities Services).

4Dixing XuNanyang Technological Universitydixingxu@gmail.comDixing is one of the maintainers of fabric-sdk-py and has two years of experience developing blockchain related applications, currently a research assistant at NTU, Singapore.5Stanislav LibermanCME Group, Inclirm604@gmail.comStan has 15 years of hands-on experience in Capital Markets technology and spent last 4 years researching and exploring the applications of blockchain and DLT to the domain.6Bobbi MuscaraLedger AcademyBobbi@LedgerAcademyWorking with the Learning and Materials Working Group to assist in documentation and training support for the Special Interest Groups.7Al BrandtBlocLedgeral.brandt@blocledger.comWorking with Financial Services companies on proof of concepts using Hyperledger Fabric.8Edmund ToIndustrie&amp;Co[Edmund.to@industrie.co](mailto:Edmund.to@industrie.co)Software Engineer with commercial experience across a number of blockchain technologies now. Prior to working in tech, experience in investment banking industry with equity and equity derivatives trading and structuring with UBS, Barclays Capital and BBVA.9

Jane Kenyon

janekenyon@me.com

Extensive experience as Product Manager in Securities Services, Global Custody. Work with clients and technology teams to analyze needs, to define products and strategy and to deliver solutions to market.  Most recently at R3 managing projects and proofs-of-concept.

10Kirthi KCivitas Fintechkirthi@civitasgroup.co.ukTransitioned from Management Consulting to Blockchain Solutions Architecture. Kirthi has 15 year of Business Transformation &amp; IT Change experience in Asset Management and Insurance. Data buff with special interstes in ML, Digital Sovereign Identity and Asset backed securities digitisation.11James KossGoldman Sachs - CIMDjames.koss@unitedcp.com

12John DeeterBond.One[jde@bond.one](mailto:jde@bond.one)  
13Teana Baker-TaylorGlobal Digital Finance[Teana@gdf.io](mailto:Teana@gdf.io)

GDF is an industry membership body that promotes the adoption of best practices for digital and crypto assets and digital finance technologies, through the development of conduct standards, in a shared engagement forum with market participants, policymakers and regulators.

14Araby PatchSecuritize Inc.[araby@securitize.io](mailto:araby@securitize.io)

Director of marketing for Securitize, a primary issuance and lifecycle management platform and protocol for digital securities (security tokens) on public and permission blockchains. Securitize is working with IBM on a Hyperledger based projected to tokenize commercial paper. 

15Ron QuarantaWall Street Blockchain Alliance[ron@wsba.co](mailto:ron@wsba.co)  
16Chris PainterOmnitudechris@omnitude.techCEO of Omnitude.17Rashad Kurbanoviownit capital and markets, Inc.rashad\_kurbanov@iownit.usCEO18Natalia Garcia  
natalia.garciagonzalez@gmail.comNatalia is a capital markets professional with 10 years of experience in debt origination (bonds, commerical paper and project finance). Before joining CaixaBank she worked at J.P. Morgan Corporate and Investment Banking division in London. Interested in exploring the applications of Blockchain in capital markets origination &amp; settlement processes. and banking in general.19

20

### Proposed Chair

The following individual(s) have volunteered to serve as the initial Chair/Co-Chair’s of the SIG:

1. Vipin Bharathan.
   

NOTE: As part of this proposal, the Hyperledger SIG working processes as described here will be followed: [https://wiki.hyperledger.org/groups/sig-application](https://wiki.hyperledger.org/groups/sig-application)

Document generated by Confluence on Nov 26, 2024 16:46

[Atlassian](http://www.atlassian.com/)
