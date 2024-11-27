1. [Community Events](index.html)
2. [Community Events Home](Community-Events-Home_21790731.html)
3. [Challenges](Challenges_21792347.html)
4. [Hyperledger Challenge 2022](Hyperledger-Challenge-2022_21792351.html)
5. [Ideate Challenge](Ideate-Challenge_21792356.html)
6. [Submissions](Submissions_21790825.html)

# Community Events : Transparency in the Interoperability of the National Electronic Toll network

Created by ozymandias, last modified on Mar 14, 2022

***Innovation Tagline:**  Hybrid Blockchain Network that seeks the route of Transparency, Traceability and Correct collection Payment between operators at Electronic Toll Collection(ETC)*

**Project Keywords:**  #peajenacional #peajeinteroperable #peajetrazabilidad

## Project Members

1. Elvia Osorio (LegalTech)
2. *David Arellano (Business Model)*
3. *Ramsés Hernández (System Architect) @hades2022*

## Project Description *(no more than 1,000 words including graphics)*

In the Mexican Republic there are bridges and road sections concessioned by the Federal or State Government to public organizations and/or private companies. The concessionaires must guarantee the operation, that is: take care of the road infrastructure and provide security, charge for traffic or circulation on highways, tunnels or bridges, defined as tolls.

The toll, although it is true that it can be paid in cash or with a bank card, this also has the electronic modality through a device arranged in the vehicle, known as TAG, with which transit or circulation will be allowed if it complies with the conditions of validity and balance.

In Mexico you can acquire a TAG through a public body, concessionaire or electronic toll operator (Electronic toll). As already mentioned, with the TAG device it is possible to transit or circulate on highways, tunnels or bridges through the Electronic Toll booths by some public or private body.

The diversity of electronic toll operators and existing TAGs devices in Mexico, which by official provision must be interoperable, that is, accepted on any highway, tunnel or bridge; generates flow of information and its correct treatment in the operational applications of electronic toll collection, which must comply with three fundamental aspects: 1) Transparency, 2) Traceability and 3) Correct collection; key points that require electronic toll operators to generate efficient reconciliations and meet the objective of providing the end user with the certainty of what is being charged and that the electronic toll operators reconcile clearly and efficiently.

In order to fulfill the three fundamental aspects mentioned in the previous paragraph, the implementation of hybrid blockchain technology is proposed, which can provide the security of obtaining information directly and without intermediaries, guaranteeing its integrity, the above from the moment that the capacity is generated through the Electronic Toll booths, this being the first stage to contemplate and providing technological elements that shield, thus complying with the interoperability of the companies that are currently in charge of the Electronic Toll.

In short: Electronic Toll operators will be able to reconcile their information from interoperability with the guarantee of integrity provided by a blockchain network.

### Problem

In order for a TAG device to be accepted on a highway, tunnel or bridge affiliated with interoperability, the operators have the task of exchanging data among themselves of any transaction registered in their Electronic Toll infrastructure, with the primary purpose of having an updated global pattern of TAGs.

The current interoperability process is carried out through the use of SFTP servers, in which each Electronic Toll operator deposits the tolls associated with any TAG, with XML being the standard format for exchanging information used between them.

It has been observed that the Electronic Toll operators have manual and, in the best of cases, semi-automated mechanisms to exchange transaction data from both their own and third-party TAGs. The current solution has drawbacks in the data collection and delivery processes, the following being the most relevant:

1.- Loss of communication when exchanging obtaining the XML file, that is, the information may not be completely obtained, since there may be data losses during the transmission of the file.

2.- Review the SFTP server from time to time, it can generate that the allowed number of asynchronous sockets can remain in "TIME WAIT" status, adding said status to the number of sockets allowed by server and user with "ESTABLISHED" status, said behaviors without importing the operating system, Windows or Llinux, which are governed by POSIX, can lead to loss of access to SFTP servers, putting at risk the integrity of the TAGs in terms of their status and/or available balance.

3.- The information could be modified directly in the SFTP servers, by both internal and external attacks, this being a problem when carrying out the toll reconciliation processes, with totally incongruous figures, generating a waste of time and money when generating the tolls. collection invoices for both operators and end customers

The current scenario, in which consumers are increasingly demanding about the quality of the services they demand, forces us to implement alternatives different from how the data is processed. An ideal mechanism is the use of disruptive technologies that can put the Electronic Toll sector in ideal circumstances of connectivity and avant-garde competitiveness.

### Solution

Derived from the current technical situation, the development of an interface capable of being able to insert each of the crossings made at the toll booths through electronic tolls in a private blockchain network is proposed, where in the same way it can send data of control figures to a network. public; Once the previous steps have been carried out, you can immediately filter and determine which operator the toll belongs to, complying with the interoperability process, leaving SFTP servers out, and adapting a queuing system that can comply with fault tolerance.

In order to comply with transparency in the transactions carried out and if it is necessary to request information directly from the private network to reconcile information that the regulatory entity may question, where the private blockchain will be its main source of information, NEAR blockchain will be used. public for the issuance of delivery document receipt of requested information, generating document as NFT, and can be used as unique proof, using IPFS as a file storage system, where in the same way the integrity of the generated document can be counted on.

With the foregoing, the acquisition of the NEAR Token by the client is determined to carry out requests to extract information directly from the private blockchain, said fee will be to meet transaction expenses for the creation of receipt delivery receipt; a web portal will be created where the transfer of funds can be made, which will be able to interact with the smart contract developed in NEAR.

Once the transfer of funds for the acquisition of information from the company/operator, a temporary channel will be created that will expose the corresponding information of the applicant, said information extracted from the private blockchain network.

Continuing with the flow of information transparency, said funds transferred through the NEAR token will continue to be transparent for the client, since they will be in a public network, said protocol was selected, since the cost of transactions is lower. to others such as ETHEREUM, in addition to the use of the Proof Of Stake (PoS) protocol, making transactions per second (TPS) more agile and faster.

The cost in the transactions of transparency of control figures, may be assumed by the company that will regulate the electronic toll booths, these figures being uploaded in accordance with what is proposed by it, that is, on a weekly or monthly basis, for validation by the the managing companies.

The infrastructure of the private network will be carried out through the use of AWS, assembling HyperLedger BAF as a framework, making use of Fabric, BAF is contemplated derived from the entire automation environment created.

![](attachments/21792967/21792968.png?height=400)

The phases of the MVP are marked below, where the server processes, smart contracts and web portal will be developed where each client and regulatory entity in charge of managing private information will interact.

![](attachments/21792967/21792969.png?height=204)

### Accomplishment and Team

**Bio Elvia Osorio**. Graduated in Law trained in different lines of business in the sector, Electronic Toll, Operational Finance, Transport, Food, personally related to blockchain issues for 3 years personally, as well as the analysis of the way in which they are created smart contracts because of the complexity of the legal with the technological.

**Bio David Arellano.** Computer Systems Engineer and Master in Information Technology Administration. Experience in the migration of distributed applications to centralized solutions, as well as in the administration and monitoring of data centers, guaranteeing high availability models. Project leader, negotiator, decision maker and integrator of work teams with diverse and complementary skills.

**Bio Ramsés Hernández.** Bachelor Degree Computer Systems and Master Degree Information Technology and Decision Analysis, Diploma in Cybersecurity, having taken different training in Blockchain such as LegalTech, HyperLedger, Ethereum, NEAR, BlockChain Consultant, the above guided by passion, knowledge and understanding of a disruptive technology. Active member of the Blockchain Academy community. Trained in different business lines of the sector, Logistics, Metallurgy, Aviation, Autotransport, Maritime and Electronic Toll. In research having Innovative projects with the Mexican Navy, through the National Institute of Optical and Electronic Astrophysics (INAOE).

### Project Plan

**LEGAL TECH(LT) - BUSINESS MODEL(BM) - ARCHITECT(A)**

IDActivitiesTeam Members  
**Prototype Phase**  
1WorkFlow Model to ETC ProcessLT/BM/A2WorkFlow Model ETC FiltersLT/BM/A3Architecture Design LT/BM/A4Design Mockups UX/UILT/BM/A5Data Model to Save on Public BlockchainLT/BM/A6Data Model to Save on Private BlockchainLT/BM/A7Create Architecture DockersA8Installing Fabric FrameWorksA9Development Front-End and Back-EndA10Development Chain CodeA11Development SmartContractA12Integration aplicationsA13Test CasesLT  
**Launch Phase**   
14Create and Configure AWS InfraestructureA15Upload AplicationsA16Test Cases LT

IDActivitiesTeam Members  
**One-Year Goal**  
1Design ThinkingLT/BM/A2We will make to Customer Presentation to get FeedbackLT/BM/A3Workflow new Model JudgmentLT/BM/A4Workflow new Model ConciliationLT/BM/A5Workflow new Model TraceabilityLT/BM/A

**RISK**

Not get more support to dev some modulesUnavailability full Time resources 

**MITIGATION**

Achievable goalsGetting Mentoring HyperLedger

## Attachments:

![](images/icons/bullet_blue.gif) [MVP PHASES.png](attachments/21792967/21792969.png) (image/png)  
![](images/icons/bullet_blue.gif) [HYPERLEDGER\_ROAD-MAP.png](attachments/21792967/21792968.png) (image/png)

Document generated by Confluence on Nov 26, 2024 16:17

[Atlassian](http://www.atlassian.com/)
