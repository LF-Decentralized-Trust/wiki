1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Archive\_](Archive__19006062.html)

# Climate Action SIG : Blockchain-enabled CSR reporting

Created by Robin Klemens, last modified on Jul 29, 2021

**This is a proposal.  Please leave your feedback as comments.**

Pitch Deck: [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/presentation/d/1cy31Jzk0tQ9UJyiMDGChA9MwwGDmd66fmiu4GBk3pZ0/edit?usp=sharing)

Value Proposition Canvas for Companies: [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/drawings/d/1AwDW3hXXyUIccjnw8lyDsh9QvOQ4urv4V8WLbZMOEhU/edit?usp=sharing)

# Tasks

- Formulate bullet points
- Make the use case solid proof and easy understandable
  
  - How much money do corporations spend for (1) internal CSR reporting and (2) third-party assurance
  - Formulate the use case 15 Jul 2021 [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)
- Doing some research on the existing solutions that are already based on blockchain technology 15 Jul 2021 [Woody Moore](https://lf-hyperledger.atlassian.net/wiki/people/70121:310f5eae-a11b-435a-ae52-42b0a796fe0b?ref=confluence)
- Gather information about the process of CSR reporting of companies (no blockchain here)
- Define the scope of a PoC
- Examine the [GRI standard](https://www.globalreporting.org/) and look for blockchain opportunities
- Create the first draft of the software architecture
- Put together high level presentation
- Share presentation with the CA2SIG for support and feedback
- Outreach: Hyperledger Social Impact, Finance &amp; Trade, and Supply Chain SIGs
- Set up meeting on a weekly basis (Thursday, 7 am PST) [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)

# Objectives

Corporate Social Responsibility (CSR) is the idea that a business has a responsibility to the society and environment in which it operates (acc. to [Sustainable Business Strategy](https://online.hbs.edu/courses/sustainable-business-strategy/)). 

Fortune Global firms spend around $20 billion a year on CSR activities, more than 90% of the 250 largest companies in the world now producing an annual CSR report

**Key global trends in sustainability reporting** ([KPMG Survey of Sustainability Reporting 2020](https://home.kpmg/xx/en/home/insights/2020/11/the-time-has-come-survey-of-sustainability-reporting.html))

- 80% of companies worldwide now report on sustainability
- North America has the highest regional sustainability reporting rate
- [GRI](https://www.globalreporting.org/) remains the dominant global standard for sustainability reporting
- Third-party assurance of sustainability information in corporate reporting is now a majority business practice worldwide

**Growing demand for CSR reporting from the people, governments, and  investors**

**People**

- "more than 9-in-10 millennials would switch brands to one associated with a cause" - 2015 Cone Communications Millennial CSR Study
- "prepared to make personal sacrifices to make an impact on issues they care about, whether that’s paying more for a product, sharing products rather than buying, or taking a pay cut to work for a responsible company" - 2015 Cone Communications Millennial CSR Study

**Governments:**

The European Commission adopted a proposal for a Corporate Sustainability Reporting Directive (CSRD), which would amend the existing reporting requirements of the NFRD. The proposal

- extends the scope to all large companies and all companies listed on regulated markets (except listed micro-enterprises)
- requires the audit (assurance) of reported information
- introduces more detailed reporting requirements, and a requirement to report according to mandatory EU sustainability reporting standards
- requires companies to digitally ‘tag’ the reported information, so it is machine-readable and feeds into the European single access point envisaged in the

**Investors**

- ESG (Environmental, Social, Governance) investing grew to more than $30 trillion in 2018, and some estimates say it could reach $50 trillion over the next two decades ([Source](https://www.cnbc.com/2019/12/14/your-complete-guide-to-socially-responsible-investing.html))
- SRI (Socially Responsible Investing)
- “Our conviction is that companies perform better when they are deliberate about their role in society and act in the interests of their employees, customers, communities and their shareholders.” —BlackRock, 2021
- According to the second annual [Corporate Social Responsibility Survey from Aflac, FleishmanHillard Research, and Lightspeed GMI](https://www.aflac.com/about-aflac/corporate-citizenship/default.aspx?utm_medium=multiple&utm_source=vanity&utm_campaign=corpcomm_2015&utm_term=acsr), more than 80 percent of professional investors prefer to invest a company known for its social responsibility

**Why CSR reporting?**

- Being a socially responsible company can bolster a company's image and build its brand.
- Social responsibility empowers employees to leverage the corporate resources at their disposal to do good.
- Formal corporate social responsibility programs can boost employee morale and lead to greater productivity in the workforce.

→ Socially responsible companies cultivate positive brand recognition, increase customer loyalty, and attract top-tier employees. These elements among the keys to achieving increased profitability and long-term financial success

# Use Cases

**Market**:

- Among the world’s 250 largest companies, the underlying trend for third-party assurance of sustainability data is 71 percent ([KPMG Survey of Sustainability Reporting 2020](https://home.kpmg/xx/en/home/insights/2020/11/the-time-has-come-survey-of-sustainability-reporting.html))
- PwC planning to Hire 100,000 over fice years in major ESG push. "The firm (PwC) is also setting aside $1 billion to further automate parts of its auditing process." ([source](https://www.reuters.com/business/sustainable-business/pwc-planning-hire-100000-over-five-years-major-esg-push-2021-06-15/#:~:text=The%20new%20hires%20will%20come,Moritz%20said%20in%20an%20interview.&text=Moritz%20said%20PwC%20had%20approached,before%2C%20focusing%20on%20reporting%20frameworks.))

**Potential Advantages of blockchain-enabled CSR reporting**

- Save money
- Simplify the reporting
- increase the participation of companies in CSR activities, socially responsible Businesses can also appear more attractive to investors → SRI and ESG investing (Link to Hyperledger Trade Finance SIG??)
- CSR costs money to implement. Costs fall disproportionally on small businesses
- Consumers are wise to greenwashing
- Audits could be simplified by granting access to standard-monitoring and regulation-enforcing entities.
- Compliance with voluntary standards could also be made more visible, accessible, and transparent for monitoring companies and those handing out certifications and consumers.
- costly, time-consuming, paper-based processes could be streamlined.
- More trust: Higher quality of data due to standardized non-financial reporting processes and internal controlling systems.
- More transparency: In response to established reporting standards, and future rules and regulations.
- Lower risks: A holistic overview of the company provides a solid foundation for making the right decisions.
- Increased value: Better access to finance when environmental, social, and governance considerations are incorporated into external reporting.

**How can blockchain technology support/replace external assurance to confirm the reliability of the data?**

In general, reporting processes for non-financial data do not offer the same level of maturity as those for financial reporting. External assurance helps to ensure the reliability of the data and can assist the supervisory board in performing its monitoring function. In addition, external assurance can identify gaps in the reporting process and the approach to controlling, which enables further improvements to the sustainability reporting approach. → Highlight potentials of how blockchain technology can (1) replace parts of the external assurance by the design of the technology (2) Evaluate costs of both approaches (3) increase the interoperability/integration of CSR reports of different companies

**Existing Solution Providers**

- Responsible Sourcing Blockchain Network (RSBN) - [https://www.ibm.com/blogs/blockchain/2020/12/blockchain-and-sustainability-through-responsible-sourcing/](https://www.ibm.com/blogs/blockchain/2020/12/blockchain-and-sustainability-through-responsible-sourcing/)

**GRI reporting:**

- GRI 101: Foundation ([https://www.globalreporting.org/standards/media/1036/gri-101-foundation-2016.pdf](https://www.globalreporting.org/standards/media/1036/gri-101-foundation-2016.pdf))  
  
  - principles for defining report quality  
    
    - accuracy
    - comparability
    - reliability
  - Presenting information
    
    - 2.6 If the reporting organization reports a required disclosure using a reference to another source where the information is located, the organization shall ensure:
      
      - 2.6.1 the reference includes the specific location of the required disclosure;
      - 2.6.2 the referenced information is publicly available and readily accessible.
  - Claims that a report has been prepared in accordance with the GRI Standards
    
    - → Opportunity: GRI digital signs the reports that are in accordance with the GRI Standards
  - Notifying GRI of the use of the Standards
    
    - 3.4.2 registering the report or published material at [www.globalreporting.org/standards](http://www.globalreporting.org/standards).
    - → Blockchain registry???
- GRI 102: General Disclosures (2016)
  
  - 1.  Organizational Profile
    
    - → Proof of origin of the organization's profile → Verifiable Credentials???
  - In general: 
    
    - → cryptographic signing of any document provided???
    - → Storing hash values of documents to blockchains?
  - Disclosure 102-56: External assurance 
    
    - Digitally sign the external reports??
    - publish a hash value or certain metadata on public blockchain???
    - Giving the auditors a digital identity?
    - Could a part of the external assurance be automated by smart contracts???
- GRI 103: Management Approach (2016)
  
  - see GRI 102: In general
- GRI 305: Emissions (2016)
  
  - Disclosure 305-1: Direct (Scope 1) GHG emissions
    
    - "apply emission factors and GWP rates consistently for the data disclosed;"
      
      - → document emissions factors used in an immutable ledger
  - Disclosure 305-2 Energy indirect (Scope 2) GHG emissions
    
    - The ‘GHG Protocol Scope 2 Guidance’ requires organizations to provide two distinct Scope 2 values:
      
      - A **location-based method** reflects the average GHG emissions intensity of grids on which energy consumption occurs, using mostly grid-average emission factor data
      - A **market-based method** reflects emissions from electricity that an organization has purposefully chosen. It derives emission factors from contractual instruments
      - → Utility emissions channel: location-based grid factors are already covered. market-based could be included: Great opportunity to use parts of our existing lab????
  - Disclosure 305-3 Other indirect (Scope 3) GHG emissions
    
    - ToDo: Great potential!!
- GRI 308: Supplier Environmental Assignment (2016)
  
  - "The reporting organization shall report its management approach for supplier environmental assessment using"
  - Disclosure 308-1 New suppliers that were screened using environmental criteria
  - Disclosure 308-2 Negative environmental impacts in the supply chain and actions taken
  - → Use there published and signed data (and/or reports) to verify their negative environmental impacts

# Implementation

TBD

# Resources

**CSR in general:**

[CSR Or Sustainability Report: Definition, Meaning, Benefits &amp; Examples From Companies](https://youmatter.world/en/definition/definitions-csr-report-important-examples/)

[The KPMG Survey of Sustainability Reporting 2020](https://assets.kpmg/content/dam/kpmg/be/pdf/2020/12/The_Time_Has_Come_KPMG_Survey_of_Sustainability_Reporting_2020.pdf)

[European Commission - Corporate sustainability reporting](https://ec.europa.eu/info/business-economy-euro/company-reporting-and-auditing/company-reporting/corporate-sustainability-reporting_en)

**Blockchain and CSR:**

[Blockchain and Corporate Social Responsibility — Synergies and Momentum](https://blog.b9lab.com/blockchain-and-corporate-social-responsibility-synergies-and-momentum-27a50de1225b)

[How Blockchain Helps with Corporate Social Responsibility](https://news.coinsquare.com/blockchain/corporate-social-responsibility-blockchain/)

[Blockchain reporting: The Opportunities &amp; Challenges for CSR](https://www.investisdigital.com/blog/corporate-communications/blockchain-reporting-opportunities-challenges-csr)

[3 Ways Blockchain Can Positively Influence CSR](https://boardmember.com/3-ways-blockchain-positively-influence-csr/)

[Blockchain Technology: Its Ability to Transform Corporations' Corporate Social Responsibility Practices](https://poseidon01.ssrn.com/delivery.php?ID=863073094087022022078097109087107072049033032050001006088089084085002120018121119089010103119001122038023007081098002117121066055043092008037069021113091064088069005070020042094004092101127087072112084076101073126087025114104102081065102065093105031000&EXT=pdf&INDEX=TRUE)

**Benefits for companies:**

[CSR Reports: Benefits for Businesses](https://www.nbs.net/articles/why-report-on-csr-activities)

[Corporate social responsibility (CSR) - Business benefits of corporate social responsibility](https://www.nibusinessinfo.co.uk/content/business-benefits-corporate-social-responsibility)

**Pain points in CSR reporting:**

[How to Take the Pain Out of CSR Reporting](https://sustainablebrands.com/read/new-metrics/how-to-take-the-pain-out-of-csr-reporting)

[Pain points of Corporate Responsibility managers across the world](https://www.wenck.com/wp-content/uploads/2016/04/ReScore_Full_report_Final.pdf)

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
