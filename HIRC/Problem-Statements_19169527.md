1. [Hyperledger India Regional Chapter](index.html)
2. [LF Decentralized Trust India Regional Chapter Home](LF-Decentralized-Trust-India-Regional-Chapter-Home_19169282.html)
3. [HIRC - Events](HIRC---Events_19169346.html)
4. [2020-Events](2020-Events_19169348.html)
5. [Hack-a-thons](Hack-a-thons_19169521.html)
6. [Hackathon Feb 2020](Hackathon-Feb-2020_19169522.html)

# Hyperledger India Regional Chapter : Problem Statements

Created by Arun .S.M. on Dec 06, 2020

# Topic 1 - Telecom CDR \[Call Detail Record] reconciliation

Inter-Carrier Settlement Problem Statement:

Consider 2 Telecom Operators who are Wholesale Interconnect Partners 

This is how they currently do their business 

Operator A is based out of India and Operator B is based out of the USA 

Operator A uses voice interconnect services from Operator B to send calls from India to USA 

Operator B uses voice interconnect services from Operator A to send calls from USA to India 

 

Everyday Operator A sends 50000 minutes spread across 10000 CDRs coming in 100 files as Operator B uses Switch C

 

Similarly Operator B sends 4000 minutes spread across 8000 CDRs coming in 80 files as Operator B uses Switch B

 

Now, this is a daily scenario where each party generates the CDRs for all the calls supported by their network, Operator A's Switch and Operator B's Switch both generates record for the call after termination.

 

Operator A have billing system A and Operator B have billing system B, after identification of CDRs the billing system applies rates and do billing at their end. 

 

Now at the end of the month (assuming Operator A and Operator B have agreed on monthly billing cycle)

 

Billing system A will send out an invoice to Operator B for calls sent from USA to India for termination 

 

Similarly, Operator B will send invoices to Operator A for calls sent from India to USA for termination. 

 

Once the invoice is received by Operator A will ingest the invoice and shall match it with Billing System A's recordings, this stage A will realize there are discrepancies in Volume or rate or both. 

 

This then goes through the Dispute management process where A will raise dispute on B's invoice, ask CDRs from B to reconcile with A's CDRs to find the GAP. Now this process is tedious, long and blocks disputed revenue for months to years. In many cases it results in writing off the amount all together. 

 

Keeping this problem in mind, we have to create a near real time CDR reconciliation solution on blockchain. Let us assume the reconciliation will only happen once in a day. 

 

Do consider that this solution is not just for A and B, A can have more than 100 partners who send similar or more minutes for more than 200 destinations. Hence, the solution has to be scalable. 

 

**Hint**: Invoices that are exchanged are summarized for a month for all A-Z destinations individually and current invoice reconciliation (before CDR reconciliation) is done for the monthly summarized values.

# Topic 2 - Supply Chain Traceability

2.1: Track-n-Trace of luxury goods

High-end brands have a real problem with counterfeit products. For companies like Rolex, they would like a simple way of proving that every watch they make is authentic. Everyone in the product life cycle Manufacturer, Dealer, Retailer, Customer, Insurer, Financer need trustworthy and transparent system of record (one truth of origin).

2.2:  Track and Trace Supply Chain for the special purpose drugs.

**Background:** Special category or high cost drugs such as cancer medicine or cannabis medicine. Such medicine needs to be traced from its manufacturing to distribution to consumption by patients. Government appointed agencies will also be carrying out audits on the entire process.

 

**Problem:** The problem statement in this use case is two-folded as follows –

1. Each of the party involved uses its own book keeping ledger for their respective part of role, transactions, tracking, etc. in the supply chain. This book of records may not be sharable with others (be it another participant or government agency, government official itself) and hence lacks reconciliation.

Seamless Asset tracking (from manufacturing-to-consumption) becomes difficult due to the problem stated in #1

Reconciliation of the drug to trace back how much was manufactured vis-à-vis consumed, leakage if any

 

**Participating Actors:**

Government and Agency

Drug Manufacturer

Distributor

Shipping Agent

Pharmacy

Family Physician (Doctor)

Consumer (Patient)

There could be more such participants

# Topic 3 - Identity &amp; Data Protection

Self-Sovereign Identity &amp; Credentials solution for data privacy which may comply with the International Data Protection Laws such as GDPR, Personal Data Protection (PDP) Law in India, California Consumer Privacy Act (CCPA), etc.

Key features of the law to consider while building a decentralized solution are:

1. Right to be Forgotten
2. Right to Consented Data sharing &amp; Access
3. Right to Correction of Data
4. Right to Portability of data from one service provider to another

Solution may follow the following guiding principles of the Self-Sovereign Identity.

[http://www.lifewithalacrity.com/2016/04/the-path-to-self-soverereign-identity.html](http://www.lifewithalacrity.com/2016/04/the-path-to-self-soverereign-identity.html)

References to international laws:

**CCPA -** [https://leginfo.legislature.ca.gov/faces/codes\_displayText.xhtml?lawCode=CIV&amp;division=3.&amp;title=1.81.5.&amp;part=4.&amp;chapter=&amp;article=](https://leginfo.legislature.ca.gov/faces/codes_displayText.xhtml?lawCode=CIV&division=3.&title=1.81.5.&part=4.&chapter=&article=)

**GDPR -**

[https://gdpr-info.eu/](https://gdpr-info.eu/)

**PDP Bill, India**

[https://www.dvara.com/research/wp-content/uploads/2020/01/Initial-Comments-on-the-Personal-Data-Protection-Bill-2019.pdf](https://www.dvara.com/research/wp-content/uploads/2020/01/Initial-Comments-on-the-Personal-Data-Protection-Bill-2019.pdf)

Document generated by Confluence on Nov 26, 2024 16:38

[Atlassian](http://www.atlassian.com/)
