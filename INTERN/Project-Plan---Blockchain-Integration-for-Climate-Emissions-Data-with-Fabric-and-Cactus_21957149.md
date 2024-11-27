1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [Blockchain Integration for Climate Emissions Data with Fabric and Cactus](Blockchain-Integration-for-Climate-Emissions-Data-with-Fabric-and-Cactus_21954730.html)

# Hyperledger Mentorship Program : Project Plan - Blockchain Integration for Climate Emissions Data with Fabric and Cactus

Created by Si Chen, last modified by Pritam Singh on Oct 29, 2021

## **Abstract**

Use Cactus to implement integration between Fabric application such as the [emissions data channel](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19006106/Emissions+Data+Channel) and Ethereum [emissions token network](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19006546/Emissions+Tokens+Network):

1. Replace the current ethers connection to Ethereum with Cactus to perform "atomic swap" between Ethereum and Fabric.  Cactus connector will call Ethereum to tokenize emissions records from Fabric, wait for the Ethereum blocks to record, then come back to Fabric to update the emissions records with the Ethereum token information.
2. Instead of putting private key in a config file, use Cactus to integrate with [AWS Secret Manager](https://aws.amazon.com/secrets-manager/) or the open source [Vault](https://www.vaultproject.io/)
3. Implement Vault Transit key signing for fabric transaction

## **Mentor and Mentee**

MentorMentorMentorMentee

Si Chen

US PST

sichen@opensourcestrategies.com

Peter Somogyvari

US PST

peter.somogyvari@accenture.com

Kamlesh Nagware

IST

kamlesh.nagware@snapperfuturetech.com

Pritam Singh

IST

pkspritam10@gmail.com

Communication channel: Email on the Climate SIG mailing list + [Github](https://github.com/hyperledger-labs/blockchain-carbon-accounting/labels/mentorship-cactus)

**Project repo:** [https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/mentorship-cactus-integration](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/mentorship-cactus-integration)

## **Deliverables**

- Replace direct dependence of carbon accounting application on fabric-node-sdk and ethers pkg with cactus packages.
- Add Support for signing of HL Fabric Transactions with private key stored as transit key in vault server.
- Prevent  double minting of emissions token during \`record audited emissions token\` operation.
- Vault Identity management server for the carbon accounting application.

## **Milestones**

**Eval 1:**

- Replace direct dependence of carbon accounting application on fabric-node-sdk and ethers pkg with cactus packages.

**Eval 2:**

- Add Support for signing of HL Fabric Transactions with private key stored as transit key in vault server.

**Eval 3:**

- Prevent  double minting of emissions token during \`record audited emissions token\` operation.

**Eval 4:**

- Vault Identity management server for the carbon accounting application.

## **Timeline**

WeekTask/PlanDeliverable**May 24 - May 28**

- Clone and build cactus repository
- Clone and build blockchain-carbon-accounting repository

<!--THE END-->

- Development environment setup

**May 31 - June 11**

- Understand and try carbon accounting application
- Understand and try examples present in cactus repository
- Get cactus set up for blockchain-carbon-accounting working

<!--THE END-->

- Project Plan
- Understanding of carbon accounting project
- Understanding of ledger integration using cactus

**June 14 - June 25**

- Refactor carbon accounting application to use cactus's ethereum connector
- Refactor carbon accounting application to use cactus's fabric connector

<!--THE END-->

- Carbon accounting application uses cactus's ethereum connector
- Carbon accounting application uses cactus's fabric connector

**June 28 - July 2**

- Design request manager system
- Implement request manager chaincode

<!--THE END-->

- Design of request manager system

**July 5 - July 9**

- Implement request manager chaincode
- Test request manager chaincode

Eval 1

- Request manager chaincode
- First Evaluation

**July 12 - July 23**

- Implement request manager client
- Test request manager client

<!--THE END-->

- request manager client

**July 26 - August 6**

- Decide a approach for managing client's private keys
- Create a pull request to fabric-sdk-node for supporting asyn signing of messages

<!--THE END-->

- Approach for managing/securing client's private key

**August 9 - August 13**

- Make singing with vault transit engine work
- Propose secure-fabric-connector to HL cactus

<!--THE END-->

- fabric-sdk-node PR merged
- test vault Transit Engine as identity provider

**August 16 - August 27**

- Make PR to HL Cactus for supporting vault transit engine

Eval 2

- HL Cactus support vault transit engine
- Second Evaluation

**August 30 - Sept 3**

- Use vault signing inside carbon accounting's node application

<!--THE END-->

- carbon accounting's node application uses vault signing
- Demo of carbon accounting using Cactus, Vault signing

**Sept 6 - Sept 17**

- Vault Identity management server for the carbon accounting application.

<!--THE END-->

- Vault Identity management server

**Sept 20 - 24**

**Sept 27 - Oct 1**

Eval 3

**Oct 4 - Oct 15**

- Update Documentation

<!--THE END-->

- updated Documentation

**Oct 18 - Oct 29**

- Demo of End-to-End flow

<!--THE END-->

- End-to-End flow demo

**Nov 1 - Nov 5**

- Prepare for Final evaluation

<!--THE END-->

- Final evaluation

**Nov 8 - Nov 12**

Eval 4

Final evaluation and presentation of project 

## **Tasks**

****Explanation**  
**Replace direct dependence of carbon accounting application on fabric-node-sdk and ethers pkg with cactus packages :****

**carbon accounting application is a REST API server which connects to multiple ledgers (Ethereum and HL fabric ) to perform required business logic for the carbon accounting project. It was using fabric-node-sdk for making HL fabric transactions and ethers package for ethereum transactions.  In order to integrate hypelredger cactus with carbon accounting project, \`fabric-node-sdk\` is replaced with \`@hyperledger/cactus-plugin-ledger-connector-fabric\` and \`ethers\` with \`@hyperledger/cactus-plugin-ledger-connector-xdai\`**

**Add Support for signing of HL Fabric Transactions with private key stored as transit key in vault server.**

**`fabric-node-sdk` provide two different kind of approaches for managing client's private key.**

**storing client's private key and certificate together on some database (which implements wallet interface). For this approach a rough flow goes something like this**

**client send request to `org's application` server to `invoke` or `query` chaincode using a give `KEY`.`org's application` upon receiving the request , it fetches `private key` and `certificate` corresponding to `KEY`.uses the fetched private key to sign fabric `message` in order to query or invoke chaincode.  
NOTE : developer of the application has to implement authentication for client's `KEY`**

**store private key in HSM , but in this approach `application` and `HSM` have to be present on same physical machine (i.e `HSM` should directly be connected with `machine` running the application). This approach is mostly used for developing client's desktop application, which will be responsible for communicating with fabric peers.**

**Major Advantage in First approach : clients won't be responsible for communicating with fabric networkMajor Disadvantage in First approach : all private key are stored in single database which leads to Honey`pot` for hackers to exploit .Major Advantage in Second approach : client's private key are never exposed to `org's` application.Major Disadvantage in Second approach : clients are responsible for communicating with fabric network**

**Now comes the `fabric-secure-connector` which only brings the advantages from both the approaches. Secure Fabric connector provides a solution to the fabric organization for managing their client's private key such that the client's private key is never brought to `Node Server` for singing.**

**![](attachments/21957149/21965940.png)**

**Reference :** 

**[https://github.com/hyperledger/cactus/issues/1212](https://github.com/hyperledger/cactus/issues/1212)   (proposal to HL Cactus)[https://github.com/hyperledger/cactus/pull/1243](https://github.com/hyperledger/cactus/pull/1243)    (PR to HL cactus: feat(connector-fabric): add support for vault transit secret engine)[https://github.com/hyperledger-labs/blockchain-carbon-accounting/pull/287](https://github.com/hyperledger-labs/blockchain-carbon-accounting/pull/287) (PR : integration of vault signing in carbon accounting application)**

**Prevent  double minting of emissions token during \`record audited emissions token\` operation.**

**The \`record emissions token\` operation requires interaction with both ethereum and fabric network, due to which a problem of double minting of token for same emissions is introduced. To solve this dataLock chaincode is developed.**

**DataLock Chaincode :**

**It's a Fabric chaincode for locking fabric data, while transactions related to the locked data are executed on different ledger/dataSource. Use of MVCC (Multiversion concurrency control) makes fabric a perfect blockchain for locking data. In fabric, MVCC is used for the solving double spending problem. DataLock uses the same facts, such that a single process with a unique id can only acquire lock. To minimize number of call to fabric, business logic of data chaincode can be called from DataLock chaincode before locking or unlocking.**

**![](attachments/21957149/21965944.png)**

**Reference :** 

**More Details : [https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/utility-emissions-channel/chaincode/datalock](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/utility-emissions-channel/chaincode/datalock)**

**Vault Identity management server for the carbon accounting application.**

**Server exposing endpoint for clients to manage their vault identity. Each client is represented a identity inside vault with certain policy rule placed on them. Using this server two type identity can be created.**

**Client : Has access to managing one transit key.Manager : Identity responsible for create client's identity.**

**Reference**

**More Details : [https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities/vault-identity](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities/vault-identity)PR : [https://github.com/hyperledger-labs/blockchain-carbon-accounting/pull/326](https://github.com/hyperledger-labs/blockchain-carbon-accounting/pull/326)**Methodology****

**Design : Each new components/idea is first designed using PlantUMLMake It Work : This is the first iteration of the design implementation.Refactor/Optimise :   All the implementation are further refactored and optimised. Write Test : For the correctness and maintainability unit, integration and end-to-end test are added to the code base.** 

****Attachments:****

**![](images/icons/bullet_blue.gif) [secure-fabric.png](attachments/21957149/21965940.png) (image/png)  
![](images/icons/bullet_blue.gif) [cc-lock.png](attachments/21957149/21965944.png) (image/png)**

**Document generated by Confluence on Nov 26, 2024 14:55**

**[Atlassian](http://www.atlassian.com/)**
