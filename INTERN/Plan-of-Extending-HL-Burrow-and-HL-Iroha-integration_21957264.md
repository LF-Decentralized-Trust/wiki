1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [HL Burrow and HL Iroha extend existing Solidity VM integration](HL-Burrow-and-HL-Iroha-extend-existing-Solidity-VM-integration_21956755.html)

# Hyperledger Mentorship Program : Plan of Extending HL Burrow and HL Iroha integration

Created by baziorek, last modified on Aug 30, 2021

## **Abstract**

The aim of the project is to extend the HL Burrow and HL Iroha integration, which will create an environment for smart contracts using the Ethereum Virtual Machine. All the Iroha commands, queries and permissions need to be integrated and then tested. The complete project has to be documented, as the documentation will help the community understand the project and use it. Examples need to be provided.

## **Mentor and Mentee**

MentorMentee

Grzegorz Bazior

CEST (UTC+2)

[g.bazior\[at\]yodiss.pl](mailto:g.bazior@yodiss.pl)

Ayush Jalan

IST (UTC+5:30)

ajalan@me.iitr.ac.in

Communication channel: Email/ Telegram/ Microsoft Teams 

**Project repo:** 

[https://github.com/Ayush-Jalan/iroha](https://github.com/Ayush-Jalan/iroha)

## **Deliverables**

- 1 Add any additional command and query to Iroha - Burrow integration, eg. set\_account\_detail, get\_account\_details and Add examples in python code and solidity
- 2 Add more commands and queries - as much as possible without Burrow code changes + examples in python and solidity
- 3 Add \*all commands, queries and permissions: [https://iroha.readthedocs.io/en/main/develop/api.html](https://iroha.readthedocs.io/en/main/develop/api.html) + samples of python and solidity code
- 4 Testing + documentation
- 5 Consulting with Iroha core team + correction
- 6 Presenting results during Iroha bi-weekly meeting

## **Milestones**

**Eval 1:**

- Understand the Iroha project through documentation
- Create a Project Plan
- Run an Iroha network and send commands and queries to the network

**Eval 2:**

- Add commands and queries to the HL Burrow integration
- Add examples in python code and solidity to run the added commands

**Eval 3:**

- Complete the integration of all commands, queries and permission with python and solidity code
- Start with testing of the integration
- Start the documentation of the project

**Eval 4:**

- Complete testing
- Documentation of the complete project
- Final Presentation and Project Report

## **Timeline**

WeekTask/PlanStatus**June 1 - June 4**

- Read [wiki-page connected with the project and provided materials](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/HL+Burrow+and+HL+Iroha+extend+existing+Solidity+VM+integration), try to build iroha

**June 4 - June 11**

- Read [Iroha documentation](https://iroha.readthedocs.io/en/main/) and integration of HL Burrow
- Have running Iroha network (single node is enough)
- Build Iroha with burrow support on docker

**June 11 - June 18**

**June 18**

- Send few commands from iroha-python client library:
- Send few commands to iroha: [https://iroha.readthedocs.io/en/main/develop/api/commands.html#create-account](https://iroha.readthedocs.io/en/main/develop/api/commands.html#create-account) [https://iroha.readthedocs.io/en/main/develop/api/commands.html#add-asset-quantity](https://iroha.readthedocs.io/en/main/develop/api/commands.html#add-asset-quantity) [https://iroha.readthedocs.io/en/main/develop/api/commands.html#set-account-detail](https://iroha.readthedocs.io/en/main/develop/api/commands.html#set-account-detail)
- Check queries, e.g.: [https://iroha.readthedocs.io/en/main/develop/api/queries.html#get-account-detail](https://iroha.readthedocs.io/en/main/develop/api/queries.html#get-account-detail)

**1st Quarter Evaluation**

**June 21 - June 25**

- try to create smart contracts according to sample: [https://iroha.readthedocs.io/en/main/integrations/burrow.html](https://iroha.readthedocs.io/en/main/integrations/burrow.html)
- try to modify: [https://github.com/hyperledger/iroha/blob/master/goSrc/src/vmCaller/iroha/commands.go](https://github.com/hyperledger/iroha/blob/master/goSrc/src/vmCaller/iroha/commands.go) and check smart contracts

**June 28 - July 2**

- Start adding Iroha commands in Burrow integration for EVM use
- Write python and solidity code examples

**July 5 - July 9**

**July 9**

- Successfully add one command to the integration and test it
- Add the python and solidity example code for the integrated Solidity command

**Midterm Evaulation**

**July 9 - July 16**

- Create Pull request with Midterm Evaluation work then review &amp; corrections
- Tests for interaction between Iroha and Burrow VM

**July 16 - July 23**

- Have sample code for integrated commands

**July 23 - July 30**

**July 30**

- Creating Pull request with changes for Iroha Core Team &amp; review &amp; merging into main iroha code

**3rd Quarter Evaluation**

**July 30 - August 6**

- Cleaning code  &amp;refactoring &amp; review &amp; corrections

**August 6 - August 13**

- Review code with Iroha core team
- Add and review documentation
- Tests for all commands
- Add the remaining commands and queries for the integration

**August 13 - August 20**

**August 20**

- Iroha core teams accepts solution
- Presentation of the solution

**Final Evaluation**

## **Explanation**

Explanation of the project goes here.

## **Methodology**

- Regular meeting every Friday
- joining iroha bi-weekly meeting
- mails or telegram when necessarily

### Result merge requests

- [Midterm evaluation: integration of few commands and queries](https://github.com/hyperledger/iroha/pull/1152)
- [Final evaluation: integration of almost all commands and queries](https://github.com/hyperledger/iroha/pull/1326)
- [Documentation of integration](https://github.com/hyperledger/iroha/pull/1334)

## **Presentation**

**[![](attachments/thumbnails/21957264/21965562)](attachments/21957264/21965562.pdf)**

**Practical presentation of completed project (not the same presentation as [on project site](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/HL+Burrow+and+HL+Iroha+extend+existing+Solidity+VM+integration)) - how to use result of the internship:**

[![](attachments/thumbnails/21957264/21965622)](attachments/21957264/21965622.pdf)

# Recommendations for future work:

1. Few commands have not been integrated, so it could be worked upon: GrantPermission, RevokePermission, CreateRole, CompareAndSetDetail, GetTransactions, GetPendingTransactions, GetAccountTransactions, GetAccountAssetTransactions
2. Currently, there are two in-built tests for Engine Call and Engine Receipts, more in-built tests can be made for the integration.
3. Integration of multi-signature transactions

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation - 2021.pptx.pdf](attachments/21957264/21965562.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Iroha Project Presentation - 2021.pdf](attachments/21957264/21965622.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 14:56

[Atlassian](http://www.atlassian.com/)
