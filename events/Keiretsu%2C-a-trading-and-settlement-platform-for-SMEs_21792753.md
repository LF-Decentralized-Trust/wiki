1. [Community Events](index.html)
2. [Community Events Home](Community-Events-Home_21790731.html)
3. [Challenges](Challenges_21792347.html)
4. [Hyperledger Challenge 2022](Hyperledger-Challenge-2022_21792351.html)
5. [Ideate Challenge](Ideate-Challenge_21792356.html)
6. [Submissions](Submissions_21790825.html)

# Community Events : Keiretsu, a trading and settlement platform for SMEs

Created by David Solis, last modified on May 18, 2024

***Innovation Tagline:**  Keiretsu provides a platform for an alternative securities market for SMEs*

**Project Keywords:**  #Mexico #securitiesmarket #SME

## Project Members

1. [David Solis](https://lf-hyperledger.atlassian.net/wiki/people/70121:8199b26d-e349-4d7d-b9f6-cda104e3a7d0?ref=confluence) – Blockchain enthusiast and researcher

## Project Description *(no more than 1,000 words including graphics)*

Keiretsu is a comprehensive issuing, trading, and settlement platform based on DLT that reduces intermediation, allowing direct buyers and sellers to trade, operating parallel to the current securities markets. Keiretsu enable SMEs to raise resources for their investment and growth projects.

We based our proposal core on the technology that allowed the conception of cryptocurrencies such as bitcoin, a distributed database known as the blockchain, eliminating the need for a centralized registry and considerably shortening settlement periods. Blockchain technology is disruptive because it makes it possible to shorten the settlement period (while providing data replication to replace conciliation processes between participants) and implies the possibility of radically transforming how securities markets carry out financial transactions from electronic trading to nowadays.

The success of this project will have a substantial economic and social impact that will boost Mexico's sustained growth.

The following figure shows the Keiretsu architecture.

![](attachments/21792753/21792754.png)

We identified two types of participants: issuer and customer (buyer or seller). The issuer type is for a sole proprietorship or SME. The customer type is an investor, a natural person, or an enterprise.

The participants interact with the platform through a web browser UI's front end. The front end invokes REST services to the middleware, which uses a database to persist or query customer information. The middleware uses a DLT to record the issuing or trading transactions via contracts (chaincode) written in Go.

The middleware services are written in Java using [Spring Boot](https://spring.io/projects/spring-boot) and reside in [Kubernetes](https://kubernetes.io/). The DLT is [Hyperledger Fabric](https://www.hyperledger.org/use/fabric).

### Problem

A *securities market* is a system in which participants such as issuers, brokers, investors, and other economic agents carry out the process of issuing, placing, distributing, and trading securities.

Securities markets are vital for any country's growth and economic development since they allow issuing companies to access capital for new products and investment projects. At the same time, they expand and diversify the options and investment portfolios available to the public, seeking to provide returns following the levels of risk that each investor is willing to assume.

For stock exchanges—the platforms for trading the sale and purchase of stock market securities—clearing and settlement processes are essential components of the capital market infrastructure.

Clearing refers to calculating the bilateral net liabilities of the purchases and sales of a securities transaction; settlement involves the conclusion of a securities transaction, that is, the exchange of securities for funds. Both processes are essential to reduce the risks inherent in the underlying market transactions and reduce the costs arising from the inefficiencies associated with market transactions. The ecosystem executes these processes in a phase after the trade, called post-trade.

Financial market infrastructures (FMIs) facilitate the clearing, settlement, and recording monetary and other financial transactions, such as payments, securities, and derivative contracts.

The following figure shows the current stock securities market.

![](attachments/21792753/21792755.jpg?width=600)

We identified several problems in the current securities markets. Below we explain each of them.

**Settlement execution time**. Even though stock exchanges reduced trade execution time to milliseconds, settlement is still a complex and redundant process that stretches out over several days. Overnight (T+1) or two-day (T+2) settlements remain the industry standard, but more complex transactions can take longer.

**Costly and risky reconciliation procedures**. Post-trade presents the most significant inefficiencies in the life cycle of the trade, which generates costs and risks for the institutions involved. Financial market participants must manage many interfaces and reconciliation procedures with central securities depositories and central counterparties in this phase. Each step of the clearing and settlement processes between financial institutions and infrastructures is costly and complex. Additionally, the functions often take several days to complete.

**Function duplication**. For the IPO, the issuing company must do it through an underwriter bank. The latter must carry out the issuance process with the stock exchange where the issue will be listed and with the Mexican central securities depository (CSD). Next, the CSD must generate the ISIN and publish it to the two exchanges and the central clearing counterparty (CCP) to trade the security.

**High intermediation**. Buyers and sellers of securities carry out their transactions through brokerage houses, which use the exchanges' trading platforms. After the trade of an operation, the stock exchange sends it to the CCP, which, through clearing processes, mitigates the risk of default of the clearing agents (the brokerage firm needs another institution, generally a bank, to operate with the CCP). The CCP then sends the transactions to the CSD for settlement. In the CSD, the financial institution deposits securities and cash via Central Bank payment systems to settle securities where it participates as a buyer or seller.

**Issuing of securities is not digital**. The dynamics of the Mexican financial market require the daily issuance of securities. This issuing occurs on a paper certificate generating a high risk to the transport and delivery of the documents. Due to the constant transportation of certificates that can be lost or stolen, it is necessary to have safer and more agile mechanisms. Likewise, in the case of the stock market, issuing generates friction since it implies that the issuer, through a private placement agent, registers the security in the Central Securities Depository (CSD) and in the Stock Exchange where the equity instrument will be listed.

**Lack of transparency** and high costs. The excessive intermediation and inefficiencies cause two impacts for shareholders: a burden for increased costs and concerns for the lack of transparency in the ownership of the shares.

**Exclusion of SMEs**. Most of the companies in Mexico are family SMEs that do not necessarily agree with making their financial statements transparent or delegating control by forming boards or other requirements that the authorities force them to list on the stock exchange. 

In summary, the securities markets in Mexico have ancient practices, high intermediation, unnecessary friction, and exclusion of SMEs.

We have identified other Mexico initiatives whose value proposition enables SMEs to access capital. However, they are like a digital marketplace for crowdfunding, lending, or custody of digital assets. As far as we know, no Mexican startup provides a solution similar to our proposal.

### Solution

Our project creates a new practice for the securities market that covers all phases of trading, promoting the financing of small investors and SMEs in a market niche that operates in parallel to the current securities markets with issues and investors on a larger scale.

Companies can issue their financial instruments directly on this platform, which would interest startups in offering shares via the placement agent. At the same time, smart contracts will automatically execute any corporate action.

Our proposal combines the best of the current model and cryptocurrency model, providing the following advantages:

- Digital issuing, each security is represented by a unique digital token
- A fully automated venue where settlement takes a short execution time.
- Direct ownership by investors
- Full transaction tracking
- Privacy of peer-to-peer transactions

We envision that our minimum viable product (MVP) will consist of the end-to-end implementation of the issuance and negotiation flows, which will allow us to test the concept and each component of the architecture. We will have a version that stakeholders can evaluate.

### Accomplishment and Team

David Solis is an enterprise architect with over 20 years of experience, focusing on developing mission-critical software systems highlighting two Mexican financial market infrastructures platforms. He has a Ph.D. in Actuarial Sciences, two master's degrees, one in Computer Science, and another in Quantitative Finance.

### Project Plan

As we can see in the following figure, our project plan consists of five milestones.

1. Concept definition. In Q4 2021, we identified a problem and a potential solution.
2. Minimum viable product. In Q2 2022, we will develop a product with the relevant features to test our concept.
3. Stakeholders’ evaluation. In Q3 2022, the stakeholders will evaluate the prototype and provide feedback.
4. Minimum marketable release (MMR). In Q4 2022, we will develop a product with sufficient features to satisfy early adopters.
5. Minimum marketable product (MMP). In Q2 2023, we will develop a small feature set that still addresses the customer needs and creates the right user experience.

![](attachments/21792753/21792756.png?width=1000)

We designed the core architecture with modularity and resiliency in mind using a stable version of the technology stack and identifying ancillary features for future phases to avoid the perils of wrong design decisions.

## Attachments:

![](images/icons/bullet_blue.gif) [keiretsu-architecture.png](attachments/21792753/21792754.png) (image/png)  
![](images/icons/bullet_blue.gif) [keiretsu-roadmap.png](attachments/21792753/21792756.png) (image/png)  
![](images/icons/bullet_blue.gif) [post-trade-processes.jpg](attachments/21792753/21792755.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 16:16

[Atlassian](http://www.atlassian.com/)
