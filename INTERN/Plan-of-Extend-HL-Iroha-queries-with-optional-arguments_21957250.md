1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [Extend HL Iroha queries with optional arguments](Extend-HL-Iroha-queries-with-optional-arguments_21956782.html)

# Hyperledger Mentorship Program : Plan of Extend HL Iroha queries with optional arguments

Created by baziorek, last modified by Piotr Pawłowski on Nov 02, 2021

## **Abstract**

Hyperledger Iroha allows us to query for transactions saved in database and blocks. PostgreSQL is used as a database and irohad is responsible for processing queries.

In order to add possibility to query for transactions in time interval, existing queries need to be extended.

Following queries are going to be modified:

- [GetAccountTransactions](https://iroha.readthedocs.io/en/main/develop/api/queries.html#get-account-transactions)
- [GetAccountAssetTransactions](https://iroha.readthedocs.io/en/main/develop/api/queries.html#get-account-asset-transactions)
- [GetPendingTransactions(optionally)](https://iroha.readthedocs.io/en/main/develop/api/queries.html#get-pending-transactions)

Also, new functionalities will be added to some of the client libraries.

## **Mentor and Mentee**

MentorMentee

Grzegorz Bazior

Piotr Pawłowski

Communication channel:

mail: ppawlowski\[at]student.agh.edu.pl

**Project repository:** [https://github.com/Pawlak00/iroha](https://github.com/Pawlak00/iroha)

## **Deliverables (fields marked * are optional)**

- 1 Extend get\*transactions with optional parameters such as date from, date to(Protobuf + Iroha base code)
- 2 Add the optional arguments to Python Iroha library.
- 3 Add unit tests to Iroha base code
- 4 Deliver necessary docs
- 5 Add the optional arguments to Java Iroha library.
- 6 Add the optional arguments to Js Iroha library.
- 7 Present results to Iroha community

## **Milestones**

**Eval 1:**

- a POC: Extend getTransactions with optional parameters such as date from, date to(Protobuf + Iroha base code)
- b POC: Add the optional arguments to Python Iroha library.

**Eval 2:**

- c Eval 1 production ready
- d Unit tests and documentation
- e Consult results with Iroha maintenance team and add necessary corrections

**Eval 3:**

- f Extend other Iroha client libraries: Java, NodeJs
- g Review all changes with Iroha team

**Eval 4:**

- h Cleanup, refactoring and debugging, adding examples to Iroha python client
- i Adding code changes to official Iroha repositories
- j Presenting results.

## **Timeline**

WeekTask/PlanStatus**June 1 - June 4**

1. Getting familiar with Iroha docs and starting example database.

  2. Building and running Iroha from code. done**June 7 - June 11**Reading Iroha code and changing protobufs. Finding database transaction queries.done**June 14 - June 25**

1. First try of modifying code: extending query protobuffs and changing corresponding code for SQL.

  2.  Modifying python library code.

  3\*. Ask about date format for protobuff, with explaining existing one.

 4\*.  Code clean.

done**June 28 - July 2**Modifying other queries specified in abstract.done**July 5 - July 9**

- Extending GetAccountTransactions and GetAccountAssetTransactions in Iroha Core Code + creating Pull Request with changes
- Eval 1

[done](https://github.com/hyperledger/iroha/pull/1092)

**July 12 - July 23**

- Testing those changes with iroha-python + creating Pull Requests
- Creating [Pull Request](https://github.com/hyperledger/iroha-python/pull/77) to Iroha-Python library
- Adding tests
- Adding documentation

done**July 26 - August 6**

- Corrections of the [pull request](https://github.com/hyperledger/iroha/pull/1092) with Iroha-Core-Team and merge into main iroha's code
- Creating [Pull request for iroha-js library](https://github.com/hyperledger/iroha-javascript/pull/63) + corrections

[done](https://github.com/hyperledger/iroha/pull/1092)**August 9 - August 13**

- Fixes of Pull Requests:
  
  - Extending GetPendingTransactions to main iroha's code: creating [Pull Request](https://github.com/hyperledger/iroha/pull/1300) + fixes
  - [Pull request for iroha-js library](https://github.com/hyperledger/iroha-javascript/pull/63) + corrections
  - [Pull Request for iroha-python library](https://github.com/hyperledger/iroha-python/pull/77) + corrections

done**August 16 - August 27**

- Creating Pull Request for iroha-java + corrections + review
- Eval 2

done

**August 30 - Sept 3**Extending queries: GetAccountTransactions, GetAccountAssetTransactions for RocksDB - learning codebasedone**Sept 6 - Sept 17**

 [Pull request](https://github.com/hyperledger/iroha-java/pull/83) for Iroha java + corrections

Getting familiar with iroha ios library and iroha-tui client

done**Sept 20 - 24**

Presenting results to Iroha team

done**Sept 27 - Oct 1**

Getting familiar with Iroha burrow integration

Eval 3

done

done

**Oct 4 - Oct 15**

[POC for missing commands and queries in Iroha burrow integration](https://github.com/hyperledger/iroha/pull/1443)

done**Oct 18 - Oct 29**

Investigation for adding MST to mentioned integration

done**Nov 1 - Nov 5**[Pull Request](https://github.com/hyperledger/iroha/pull/1443) review and correctiondone**Nov 8 - Nov 12**

Eval 4

Final evaluation and presentation of project 

Project results

- Merge Requests:
  
  - [GetAccountTransactions and GetAccountAssetTransactions for main iroha code](https://github.com/hyperledger/iroha/pull/1092)
  - [Changes in Iroha-Python library](https://github.com/hyperledger/iroha-python/pull/77)
  - [Changes in Iroha-JavaScript library](https://github.com/hyperledger/iroha-javascript/pull/63)
  - [GetPendingTransactions for main iroha code](https://github.com/hyperledger/iroha/pull/1300)
  - [Changes in Iroha-Java library](https://github.com/hyperledger/iroha-java/pull/83)
  - [![](attachments/thumbnails/21957250/21965772)](attachments/21957250/21965772.pptx)
- Issues:
  
  - [Issue](https://github.com/hyperledger/iroha/issues/1498) found in Iroha Core code
  - [Issue](https://github.com/hyperledger/iroha-python/issues/78) in Iroha Python library

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation Template - 2021.pptx](attachments/21957250/21965772.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)

Document generated by Confluence on Nov 26, 2024 14:56

[Atlassian](http://www.atlassian.com/)
