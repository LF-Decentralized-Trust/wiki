1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2020 Projects](2020-Projects_21963347.html)
5. [Towards Blockchain Interoperability with Hyperledger](Towards-Blockchain-Interoperability-with-Hyperledger_21954710.html)

# Hyperledger Mentorship Program : Progress Report - Towards Blockchain Interoperability with Hyperledger

Created by Sara Ghaemi, last modified on Nov 12, 2020

# 1st Quarter Progress Report

As the first step of the project, a literature review was conducted to identify the current interoperability solutions and possible improvements that can be done in this area. After careful consideration, we decided to come up with a blockchain interoperability solution that works based on the publish/subscribe architecture. In this solution, a blockchain acts as a messaging broker and keeps track of all the topics in the system. Publisher blockchains can send messages to the topics and all the subscriber blockchains will get notified of the changes in the topic as soon as a publish request is received. 

During the first quarter, the working environment for the project as well as a sample broker blockchain was implemented. The broker currently has some basic functionalities and features which we are going to complete during the next quarters. To sum up, the following has been done in the first quarter of the project:

- A literature review on blockchain Interoperability was conducted.
- The required tools and components for the project were investigated.
- A working environment for multiple blockchain networks was implemented.
- The first version of the messaging broker blockchain was implemented.

# 2nd Quarter Progress Report

In the second quarter, the focus was on the implementation of the proposed platform. The platform has three main components: broker blockchain, subscriber blockchains, and publisher blockchain. The broker blockchain is implemented using Hyperledger Fabric V2 and has two chaincodes called *broker* and *pubsub*. The broker chaincode holds the topics that are on the pub/sub network. When a publish request to a topic is received, the topic is updated using the broker chaincode. The pubsub chaincode holds the information about all the publisher and subscriber blockchains and their communication interface. As for the subscriber blockchains, currently, Hyperledger Fabric V1.4 and Hyperledger Besu are supported. Example networks, as well as connector smart contacts, have been implemented for each network. Finally, an example publisher network is implemented using Hyperledger Fabric V2. Currently, all the components work together to form a network with a broker, a publisher, and two subscribers. 

To sum up, the following has been done in the second quarter of the project: 

- The broker blockchain keeps track of the topics and it also holds communication interfaces of the publisher and subscriber blockchains.
- Two example subscriber networks have been implemented using Hyperledger Fabric V1.4 and Hyperledger Besu.
- An example publisher network has been implemented using Hyperledger Fabric V2.

# 3rd Quarter Progress Report

In the third quarter, the main focus was on performance testing of the implemented solution. To test the performance of the network, Hyperledger Caliper was used as the benchmarking tool. Hyperledger Caliper allows the measurement of performance metrics such as send rate, latency, and throughput for a set of use cases. We connected Caliper to the existing broker network to monitor the performance. More information on the tests and the configuration of the benchmarking tool can be found on the project’s GitHub repository. Moreover, a study on relevant blockchain interoperability solutions was conducted so that they can be compared to our solution. 

To sum up, the following has been done in the third quarter of the project:

- Performance testing of the implemented solution using the Hyperledger Caliper benchmarking tool.
- A study on relevant blockchain interoperability solutions.

# 4th Quarter Progress Report

In the last quarter, we updated the project’s GitHub page by finalizing the documentation and refactoring all the codes. Moreover, we conducted a comprehensive performance analysis on the broker blockchain to better understand the performance of the broker blockchain and to identify the bottleneck of the system. We used the Hyperledger Caliper that was set up in the 3rd quarter to do so. We changed the transaction send rate over time for each functionality of the broker network and monitored the throughput and average latency. The *PublishToTopic* function was identified as the bottleneck of the broker network. Finally, we wrote a research paper about this project which is being finalized to be submitted in a journal or conference. To sum up, the following has been done in the last quarter:

- Documentation has been updated to include all the details of the project.
- Codes have been refactored.
- A comprehensive performance analysis has been conducted on the broker blockchain.
- A research paper has been written about the project.

Document generated by Confluence on Nov 26, 2024 14:59

[Atlassian](http://www.atlassian.com/)
