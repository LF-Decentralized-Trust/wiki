1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2020 Projects](2020-Projects_21963347.html)
5. [Reworking WSV Storage](Reworking-WSV-Storage_21956099.html)

# Hyperledger Mentorship Program : Research on Best Database Solution

Created by Arushi Singhal, last modified on Jun 30, 2020

The database which we are planning to select is a **NoSQL** database with **Key-value data stores**.  Key-value data stores have the simplest data model – arbitrary byte strings for keys, paired with a byte string for the corresponding value, they can be quickly incorporated into applications that have very simplistic storage needs. Their APIs tend to be equally simple, providing only very primitive operations.

We are choosing our database with **low-latency** with optimal read, write and query time. Along with it, the DB size required to store values should also be optimal.

The database should be an **embedded NoSQL (Key/Value store) database** engine and should not have a separate server process. The database should be able to read and write directly to ordinary disk files. An **in-memory database** is a database management system that primarily relies on main memory for computer data storage. But as we want to handle big data and hence our database should hold big volumes of data larger than RAM can hold so we want embedded database with **on-disk storage mode along with in-memory capabilities** to improve its performance speed.

The Database should be open-sourced and able to support APIs for multiple programming languages as it can be extended in future but should definitely support  **C++ APIs** as currently, we are using C++ APIs.

Popular Key-Value store NoSQL Databases comparison. Also, one of the good comparisons can be found [here](https://db-engines.com/en/system/LMDB%3BLevelDB%3BOracle+Berkeley+DB%3BRiak+KV%3BRocksDB).

DatabasesOpen SourceC++ APIsKey-Value Storage

Embedded database with on-disk storage mode

In-Memory (Caching) CapabilitiesNoteAerospike![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(error)](images/icons/emoticons/error.png)![(tick)](images/icons/emoticons/check.png)  
Berkeley DB (one of the best)  
![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)Developed by Oracle Inc. Support APIs for multiple programming languages. Support many Operating systems as the server. One of the oldest and developed in the year 1994.Redis![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(error)](images/icons/emoticons/error.png) only In-memory capabilities. Can only use it as cache store so cannot store data larger than RAM size.![(tick)](images/icons/emoticons/check.png)One of the best but cannot store big volumes of data larger than RAM hence cannot be used for our purpose.LevelDB  
![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)Developed by Google Inc. IoS is not supported as a server operating system. Developed in 2011.RocksDB (also very much recommended)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)Developed by Facebook Inc. Developed in 2013. Only supports APIs in language C++ and Java. RocksDB supports Transactions when using a TransactionDB or OptimisticTransactionDB. Transactions have a simple BEGIN/COMMIT/ROLLBACK API and allow applications to modify their data concurrently while letting RocksDB handle the conflict checking. RocksDB supports both pessimistic and optimistic concurrency control.LMDB (Very high performant)  
![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)  
BadgerDB![(tick)](images/icons/emoticons/check.png)![(error)](images/icons/emoticons/error.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(error)](images/icons/emoticons/error.png)When Badger is running in in-memory mode, all the data is stored in the memory. Reads and writes are much faster in in-memory mode, but all the data stored in Badger will be lost in case of a crash or close.  
Badger doesn't support on-disk and in-memory mode together.Amazon DynamoDB![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(error)](images/icons/emoticons/error.png)![(tick)](images/icons/emoticons/check.png)  
SQLite (Not very good performance)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)![(error)](images/icons/emoticons/error.png)![(tick)](images/icons/emoticons/check.png)![(tick)](images/icons/emoticons/check.png)Does not guarantee domain integrity. SQLite works great as the database engine for most low to medium traffic.

Considering multiple parameters mentioned above along with support for Transactions etc. We decided to move ahead with RocksDB.

Document generated by Confluence on Nov 26, 2024 14:59

[Atlassian](http://www.atlassian.com/)
