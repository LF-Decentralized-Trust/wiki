1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)

# Hyperledger Mentorship Program : Making chaincode fault tolerant software

Created by Imre Kocsis, last modified by Min Yu on Dec 19, 2022

**Project Title**Applying fault-tolerant software patterns to Hyperledger Fabric chaincode**Status**

COMPLETED

**Difficulty**

MEDIUM  

# Description

Following some major fiascos (like the classic DAO attack), the Ethereum/Solidity community has been painfully aware for some time now that smart contracts are largely custom software (modulo rampant copypaste) and thus, bugs get introduced during development - against the effects of which the security and dependability of the underlying blockchain platform does not really provide any defences. Thus, a whole industry of development-time verification and validation tools is emerging to be able to "get smart contracts right the first time" - at least Solidity ones. (The lack of such tools for other platforms, as Hyperledger Fabric, is a problem, but not targeted by this proposal.)

In contrast, "consortial" blockchain networks in general, and Hyperledger Fabric-based ones in particular, carry at least the potential to also use *runtime dependability and security measures*. Informally, the user does not have to "pay" for each execution step and the incentives of node operators are not cryptoeconomic, so either the platform (through customized consensus) or the smart contracts (through additional code) can have the luxury to deploy measures which protect against chaincode bugs. For non-decentralized software, the techniques created by decades of fault-tolerant computing have been codified as *patterns* and *pattern languages*; better-known examples include (state) rollback and rollforward, modular redundancy and n-version programming.

Some of these patterns are straightforward to apply to Fabric chaincode; if an implementation "fails" (e.g., throws an exception), let's try another one (n-version programming). Others may want to rely on Fabric capabilities: different peers running different chaincode implementations (software diversification) is possible in Fabric, but would not really be possible in other leading distributed ledger technologies. And some patterns are really not trivial to introduce; e.g., equitable resource allocation is a pattern to share resources among clients equitably - which, in Fabric, translates to giving equitable access to the constrained resource of block capacity to clients (an important and as-yet unsolved problem for all IoT/cyber-physical applications where Age of Information concerns about ledger data arise).

The proposed project includes the following key activities:

1. A systematic review of the applicability of fault-tolerant software patterns to Hyperledger Fabric chaincode as the potentially faulty software
2. Creation of programming idioms for applying the applicable patterns to Hyperledger Fabric chaincode
3. Prototyping "fault tolerance gadgets" (libraries) for easy application to chaincode

The book "Patterns for Fault Tolerant Software" from R. Hanmer (Wiley, 2013) is a good reference of the patterns that the project will target.

This is a research-focused project which is relatively light on programming. At the same time, a rather deep dive into the workings of Hyperledger Fabric is expected.

# Additional Information

The project is expected to primarily focus on the patterns collected in the reference book *Hanmer, Robert S.Patterns for fault tolerant software. John Wiley &amp; Sons, 2013.* It also serves as a good general introduction to fault-tolerant computing. The scope will be extended towards other academic papers (and existing fault-tolerant computing APIs, as, e.g., SA Forum) as and if justified by the progress.

# Learning Objectives

- Introduction to open source culture and collaboration tools
- Deep knowledge of the operational principles of Hyperledger Fabric
- Software engineering techniques of fault tolerant computing

# Expected Outcome

D1: Report on the applicability of classic fault-tolerant software patterns to Hyperledger Fabric chaincode

D2: Report and example set of applying fault tolerance patterns to Hyperledger Fabric chaincode

D3: A set of prototype fault tolerance gadgets

# Timeline

**Week****Plan****Status****June 6  - June 13**Mentee intro with the mentor.  
Communicating the details of research objectives.  
Discussing the resources.Complete**June 13  - June 20**Literature review on:  
Fault tolerant software patterns.  
Fabric's architecture.  
Chaincode lifecycle.

Complete**June 20  - June 27**Identifying vulnerabilities.  
Identifying the respective mitigation approaches.  
Drafting the initial FMEA, including the software patterns.Complete**June 27  - July 4**Completing the FMEA:  
Differentiating Weakness from vulnerabilities(CEW, CVE).  
Including existing vulnerabilities and prospective vulnerabilities.  
Report progress for evaluation.In Progress**July 4 - July 11**Completing research work on:  
Background work on formal specification and run time verification of chain code.TBD**July 11 - July 18**Completing research work on:  
Runtime monitoring, observers and orderer metrics for chain code.  
Report progress for evaluation.TBD  
Evaluation**July 18 - July 25**Design I:  
Functionalities, architecture and properties.TBD**July 25 - August 1**Design II:  
Error detection, analysis of technical requirements.TBD**August 1 - August 8**Design III:  
Units of mitigation, system prototype, applicability of pattern.TBD**August 8 - August 15**Deployment I:  
Chaincode execution and error detection.TBD**August 15 - August 22**Deployment II:  
Chaincode execution and error detection.  
Report progress for evaluation.TBD**August 22 - August 29**Deployment III:  
Chaincode execution and error detection.TBD  
Evaluation**August 29 - September 5**Test case I:  
Chaincode execution and error detection.TBD**September 5 - September 12**Test case II:  
Chaincode execution and error detection.  
Report progress for evaluation.TBD**September 12 - September 19**Test case III:  
Chaincode execution and error detection.TBD**September 19 - September 26**Error Processing I:  
Error handling control flow, rollback , etc.TBD**September 26 - October 3**Error Processing II:  
Error handling control flow, roll forward, etc.  
Report progress for evaluationTBD**October 3 - October 10**Error Processing III:  
Error handling control flow, roll forward, etc.  
Report progress for evaluationTBD  
Evaluation**October 10 - October 17**Deliverables I:  
Completing the technical requirements and modules on applicability of fault-tolerant patterns.TBD**October 17 - October 24**Deliverables II:  
Completing the prototype fault tolerant libraries and patterns.TBD**October 24 - October 31**Documentation I:  
Complete documentation of the implementation.TBD**October 31 - November 7**Documentation II:  
Complete documentation of the implementation.

TBD**November 7 - November 14**Report progress for evaluation.TBD  
Evaluation

# Relation to Hyperledger

Hyperledger Fabric

# Education Level

Completed BSc level education in computer science or computer engineering (or the demonstration of equivalent competence in the core CS/CE topics) is a requirement; ongoing or finished MSc level studies are preferred.

# Skills

Highly analytical thinking and the ability to effectively "tinker with" existing software and code bases (i.e., Hyperledger Fabric) is preferred.

# Future plans

Depending on the results, proposal of a Hyperledger Labs project. Results are expected to be further utilized and improved on in academic research targeting Hyperledger Fabric.

# Preferred Hours and Length of Internship

No preference.

# Mentor(s) Names and Contact Info

Imre Kocsis, [kocsis.imre@vik.bme.hu](mailto:kocsis.imre@vik.bme.hu), assistant professor, Budapest University of Technology and Economics (BME), Budapest, Hungary

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
