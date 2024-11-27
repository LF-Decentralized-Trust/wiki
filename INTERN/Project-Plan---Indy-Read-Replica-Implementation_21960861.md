1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2024 Projects](2024-Projects_21954934.html)
5. [Hyperledger Indy Read Replica Implementation](Hyperledger-Indy-Read-Replica-Implementation_21960795.html)

# Hyperledger Mentorship Program : Project Plan - Indy Read Replica Implementation

Created by Stephen Curran, last modified by Bryan Elee on Sep 15, 2024

## **Abstract**

A Hyperledger Indy "read replica” is a web service that holds copies of the ledger transactions from one or more Indy ledgers and can be used by clients that trust the replica. While an instance of the service is intended to be accessed by arbitrary agents, an enterprise might run a read replica on their own servers for the use of their own agents – the agents "trust" the deployment of the read replica. In turn, the use of read replicas will reduce the read load on the Indy ledgers it replicates. Each replica must stay up to date with the transactions on the ledgers it supports, and agents using the replica need not connect directly with the ledger.

## **Mentor and Mentee**

Mentors: Sam Curren, Stephen Curran

Timezone: US Mountain and Canadian Pacific

Mentee: Bryan Elee Atonye

Timezone: West Africa

**Project repo:** [T](https://github.com/hyperledger-labs/solang-vscode)BD

## **Deliverables**

- JavaScript-based Web Service that maintains a database copy of one or more Indy Ledgers.
- An API for clients (such as Aries Agents – ACA-Py and Credo) to invoke to receive transaction and objects from those Indy ledgers.
- Unit and integration tests for the service.
- GitHub Actions to invoke the tests, and when triggered, release artifacts for published versions of the implementation.
- Documentation for deploying and configuring a horizontally scalable instance of the web service.

## **Milestones**

**Eval 1:**

- Create a new GitHub repository with any useful code from the open source [IndyScan](https://github.com/Patrik-Stas/indyscan) project. Include a suitable acknowledgement about the initial codebase. We agree that while there are components of IndyScan useful to this project, forking IndyScan is not appropriate, as the goals of the two projects are quite different.
- Define and implement an API call that mimics the Indy “[GET\_TXN](https://hyperledger-indy.readthedocs.io/projects/node/en/latest/requests/#read-requests)” request to allow a client to retrieve transactions from the replica.
- Get the new implementation running using Docker and document how to run a local instance.

**Eval 2:**

- Define and implement an appropriate set of GitHub actions to test Pull Requests, and when triggered, create a version and publish artifacts.
- Consult with Mentors to decide how to implement the API calls for the object “GET” – NYM, ATTRIB, SCHEMA, CLAIM\_DEF, REVOC\_REG\_DEF, REVOC\_REG, REVOC\_REG\_DELTA
- Implement the agreed upon design for the “GET” object API calls.
- Implement an appropriate authorization scheme to protect the web service.

**Eval 3:**

- Design and implement an appropriate mechanism for dealing with the “startup issue” – getting all existing transactions without having to do transaction-by-transaction reads of the ledger.  Note that this feature may require updates to the Indy Node project that may or may not be possible as part of this effort.

**Eval 4:**

- Design and, if feasible, implement a pub/sub mechanism such that the read replicas need not continually poll the ledger for updates. Note that this feature may require updates to the Indy Node project that may or may not be possible as part of this effort.

## **Timeline**

WeekTask/PlanStatus**June 03 - June 23**On boarding/orientation sessions. Meet with the mentors, discuss project implementation details,  
deliverables and scope. Prepare the project plan.

COMPLETED    

**June 24 - July 7**

Design Hyperledger Indy Read Replica web service component and Spec out API endpoints with  
input from mentors.

Set up a simple set of tests for verifying correctness of implementation

COMPLETED    

**July 8 - July 22**

Evolve IndyScan to include and support a client agent API with an HTTP version of the existing  
GET\_TXN ledger API to handle any ledger read request.

COMPLETED    

**July 22 - July 26**Prepare docker deployment and instructions.

1ST QUARTER MENTEE EVALUATION

COMPLETED    

**July 27 - August 18**Consult with the Mentors to design the remainder of the API calls for getting Indy Objects.

COMPLETED

**August 19 - September 01**Implement agreed upon design.

COMPLETED

**September 02 - September 06**

Implement GitHub CI/CD Pipeline for testing pull requests and preparing release artifacts.

Implement an appropriate authorization scheme to protect the web service.

MIDTERM EVALUATIONS

IN PROGRESS    

**September 08 - September 22**

Continue work on GitHub CI/CD pipeline as necessary.

Consult with Mentors on approach to address the “startup issue” – loading a replica without querying the ledger transaction by transaction.

**September 23 - October 19**

Implementation of the agreed upon replica start strategy.

**October 14 - October 18**3RD QUARTER MENTEE EVALUATION  
**October 19 - November 10**Implement Pub-Sub APIs for notifying read replicas of new transactions using an approach agreed  
upon with the mentors.  
**November 11 - November 29**

Buffer for project wrap up.

Revaluate work done so far. Review the code and make changes where necessary; Complete testing.  
Preparation of the final report and Submission of the final project report.

## **Explanation**

## **Methodology**

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
