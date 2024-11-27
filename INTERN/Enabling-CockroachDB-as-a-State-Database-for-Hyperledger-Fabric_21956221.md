1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2020 Projects](2020-Projects_21963347.html)

# Hyperledger Mentorship Program : Enabling CockroachDB as a State Database for Hyperledger Fabric

Created by Senthilnathan N, last modified by Min Yu on Mar 18, 2020

**Title**Enabling CockroachDB as a State Database for Hyperledger Fabric**Status**

UNSELECTED

**Difficulty**

HIGH

# Description

### **Background**

Hyperledger Fabric v2.0 supports the following two databases to store the world states (a.k.a chaincode states)

1. goLevelDB
   
   - the default key-value state database that stores values as binary data and supports only key-based queries (including range queries on the key).
2. CouchDB.
   
   - a document database that stores both binary data and JSON documents. The CouchDB allows queries based on keys as well as values but does not support aggregate/join queries.

The transaction flow in Hyperledger Fabric involves four phases (as shown in Figure 1):

1. simulation – the client sends the transaction proposal to enough organization's peer as per the chaincode endorsement policy to collect the read-write set (no changes made to the ledger) and endorsements.
2. ordering – the client submits the collected proposal response (including the transaction proposal, read-write set, endorsements) to the ordering service which executes consensus protocol to create a block of transaction. Once a block is created, it is delivered to the peers.
3. validation – each peer individually performs the following two checks for each transaction in the block:
   
   1. whether enough endorsements are collected as per the pre-defined endorsement policy;
   2. whether the transaction is serializable (using the read-set).
4. commit – once the whole block is validated, valid transactions are committed.

![](attachments/21956221/21963441.png?height=250)

### Motivation

In order to support the above transaction flow, we needed the following features from an open-source database:

1. Snapshot isolation level &amp; transaction support
   
   1. To ensure a consistent view of data to provide repeatable read isolation.
   2. To allow transaction simulations to run in parallel with no contention of read-write locks which could degrade the performance.
   3. To rollback the transaction at end of the simulation.
2. Collection of read-write set as a result of a transaction execution
   
   1. To validate the transaction during commit phase.
3. Validation of read set &amp; commit the write set
   
   1. To ensure serializability isolation level needed by most blockchain applications.

However, none of the existing databases provide all the above features (though there are a few research papers that talk about collecting read/write set, etc...). Hence, the ledger middleware in Hyperledger Fabric sits above a database and takes care of the collection of the read-write set, and serializability checks. Due to this design, we couldn't use sophisticated queries within a transaction (i.e., write) and could support only range queries.

### Goal of this Project

Instead of building a lot of database concept in the ledger middleware, we propose to **modified** CockroachDB and make it work as a state database so that we can also support the following:

1. Relational model and Structured Query Language (SQL) in chaincodes.
   
   1. Ease smart-contract development.
   2. Ease analytics operations.
2. Sophisticated queries (both read and write) as a part of transactions.
   
   1. With no restriction on the type of queries (i.e., joins, nested queries, group by, etc…) and with the combination of both chaincodes (go, java, nodejs) and SQL, it would become easier to write smart contracts with more power. Even smart-contract can be implemented fully in SQL procedure by still retaining chaincode to do invoke of SQL procedure.
3. Read Your Own Write (within a chaincode transaction).
4. History/provenance query using SQL.
5. Use of Access Control (GRANT PERMISSIONS) features along with row-level security policies in PostgreSQL.
6. Simultaneous execution of both simulation and final commit.

In order to achieve the above-mentioned goal, we need to modify CockroachDB to allow

- simulation of transactions.
- collection of read-write set at the end of a simulation.
- validation of the read set (during the validation phase) including the detection of phantom reads without re-executing the query.

While doing all the above, it is necessary to keep the performance in mind as brute force implementation is always possible and easy to do. Our goal is to achieve what we want while not sacrificing performance.

# Additional Information

Why is CockroachDB chosen? – [https://www.cockroachlabs.com/](https://www.cockroachlabs.com/)

- Highly scalable, geo-replicated, ACID compliant, SQL database.
- Inspired from Google Spanner but CockroachDB is open-source.
- It allows the user to execute analytical queries and by default supports time travel queries to perform provenance queries.
- As it is a distributed database, we could even make multiple peers within an organization to share a single database.

# Learning Objectives

There is a huge opportunity for learning new things for both mentors and mentees.

**Learning opportunity for mentees:**

- Internals of Hyperledger Fabric (note that two mentors are Fabric maintainer).
- Internals of a distributed database.
- Ways to plan and attack a hard problem.

**Learning opportunity for mentors:**

- Internals of CockroachDB.
- Understanding the overall difficulties in supporting a different state database in Fabric (other than simple goLevelDB and CouchDB)

# Expected Outcome

- Potentially a new state database support for the Hyperledger Fabric.
- A research/industry track paper in one of the top-tier conferences (VLDB/SIGMOD/Middleware/Eurosys/SoCC/ICDCS).
- The whole project progress should be tracked using a repo in Hyperledger Labs.
- The project might continue even after the end of the internship if results are promising.

# Relation to Hyperledger

Hyperledger Fabric

# Education Level

Undergraduate or Master or Ph.D. students.

Willingness to work on a research problem is more than adequate.

# Skills

- Database concepts (ACID, Various Isolation Levels, Concurrency Control, Distributed Database, Distributed Transaction)
- Golang
- Familiarity with Hyperledger Fabric
- Navigating a large codebase and understand the internals

# Future plans

The project might continue even after the end of the internship if results are promising. It could eventually result in new database support for Hyperledger Fabric. For a year at least, the project would be maintained as Hyperledger Labs to collect feedbacks. Based on the demand, interest, and feedback, the project will move to the next stage (cockroachDB could become an officially supported pluggable state database for Fabric).

# Preferred Hours and Length of Internship

No preference, Both full time and part-time internship are fine if suitable candidate is found.

# Mentor(s) Names and Contact Info

Artem Barger, [bartem@il.ibm.com,](mailto:bartem@il.ibm.com) Rocket chat: *C0rWin*  
Hyperledger Fabric Maintainer, Research Staff Member, IBM Research, Haifa, Israel.

Yacov Manevich, [yacovm@il.ibm.com](mailto:yacovm@il.ibm.com), *Rocket chat*: *yacovm*  
Hyperledger Fabric Maintainer, Research Staff Member, IBM Research, Haifa, Israel.

Senthilnathan Natarajan, [snatara7@in.ibm.com](mailto:snatara7@in.ibm.com), *Rocket chat*: *Senthil1*  
Hyperledger Fabric Contributor, Research Staff Member, IBM Research, India.

Manish Sethi, [Manish.Sethi1@ibm.com](mailto:Manish.Sethi1@ibm.com), *Rocket chat: manish-sethi*  
Hyperledger Fabric Maintainer, Senior Software Engineer, IBM, USA.

## Attachments:

![](images/icons/bullet_blue.gif) [Screenshot 2020-02-26 at 6.10.45 PM.png](attachments/21956221/21963441.png) (image/png)

Document generated by Confluence on Nov 26, 2024 14:59

[Atlassian](http://www.atlassian.com/)
