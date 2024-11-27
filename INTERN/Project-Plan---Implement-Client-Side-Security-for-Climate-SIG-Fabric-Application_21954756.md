1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [Implement Client Side Security for Climate SIG Fabric Application](Implement-Client-Side-Security-for-Climate-SIG-Fabric-Application_21954717.html)

# Hyperledger Mentorship Program : Project Plan - Implement Client Side Security for Climate SIG Fabric Application

Created by Si Chen, last modified by Bertrand WILLIAMSRIOUX on Nov 29, 2021

## **Abstract**

Implement client side security for the Climate SIG's Hyperledger Fabric application, so that transactions could be signed using Metamask through TrustId.

## **Mentor and Mentee**

MentorMentorMentorMentorMentee

Si Chen

US PST 

[sichen@opensourcestrategies.com](mailto:sichen@opensourcestrategies.com)

Vatsal Mishra

IST 

[mevatsal@gmail.com](mailto:mevatsal@gmail.com)

Maria Teresa Nieto

CEST 

[mariateresa.nietogalan@telefonica.com](mailto:mariateresa.nietogalan@telefonica.com)

Kamlesh Nagware

IST 

[kamlesh.nagware@gmail.com](mailto:kamlesh.nagware@gmail.com)

[Bertrand WILLIAMSRIOUX](https://lf-hyperledger.atlassian.net/wiki/people/712020:57613290-3ad4-4f53-8166-19a9bdb9c047?ref=confluence)

AST (UTC +3)

[bertrand.rioux@gmail.com](mailto:bertrand.rioux@gmail.com)

Communication channel: Email + Github 

**Project repo:** [https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/mentorship-trustid](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/mentorship-trustid)

## **Explanation**

This project originally targeted using TrustID to registed ID credentials used to access the [fabric utility emissions channel](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/mentorship-trustid), and storing private keys for these ID's in a clientwallet (e.g. Metamask). While TrustID offers interesting features, it implements a proxy contract that can be used to connect an external DID with a fabric network using its own Admin (or user) IDs. Instead of creating a new set of admin proxy identities to access the Fabric app using exernal keys, we want to create an integrated client side identity management solution for the actual Fabric crednetials registered with the utility emission channel (i.e. private key associated with the identity crednetial are not stored on the fabric app). To achieve this we set up a custom WsX509 identity provider using the [fabric node.jd sdk](https://hyperledger.github.io/fabric-sdk-node/release-2.2/module-fabric-network.html), that uses a [ws-identity](https://github.com/brioux/blockchain-carbon-accounting/tree/main/secure-identities/ws-identity) proxy server that connects a fabric app (e.g. [Utility Emissions Channel](https://github.com/brioux/blockchain-carbon-accounting/tree/main/utility-emissions-channel)) to a clients secure external [ws-wallet](https://github.com/brioux/blockchain-carbon-accounting/tree/main/secure-identities/ws-wallet) where private keys are stored. See methodology below for more details.

## **Deliverables**

- 1 Integrate TrustID with Fabric utility emissions channel (dropped)
- 2 Web socket based identity provider for fabric network :
- 3 Integration of web-socket identity provider into Blockchain carbon accounting using Cactus as fabric identity/security package -
- 4 Web-socket client wallet application that handles the actual private keys and signing (Node.js/CLI server application) + implementation docs and use case justification decision tree

## **Links**

- [**WsX509 identity provider in Cactus PR 1333**](https://github.com/hyperledger/cactus/pull/1333)
- [**Add WsX509 support in blockchain carbon accounting project PR 293**](https://github.com/hyperledger-labs/blockchain-carbon-accounting/pull/293)
- [**restAPI to reach external ws-wallet (node.js server) from blockchain carbon accounting app - PR 361**](https://github.com/hyperledger-labs/blockchain-carbon-accounting/pull/361)
- [**Other PRs for carbon accounting app**](https://github.com/hyperledger-labs/blockchain-carbon-accounting/pulls?q=is%3Apr%20is%3Aclosed%20brioux%20)
- [**Secure identities directory with documentation and subdirectories for**](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities)
  
  - [ws-identity server](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities/ws-identity)
  - [ws-wallet client side key management](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities/ws-wallet)
- [**ws-identity docker image (github package)**](https://github.com/users/brioux/packages/container/package/ws-identity)
- **Peer programming sessions highlighting progress on  WSX509 implementation**
  
  - [2021-08-16 Peer Programming Call](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19008098/2021-08-16+Peer+Programming+Call)
  - [2021-09-27 Peer Programming Call](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19008359/2021-09-27+Peer+Programming+Call)
  - [2021-11-08 Peer Programming Call](https://lf-hyperledger.atlassian.net/wiki/spaces/CASIG/pages/19008599/2021-11-08+Peer+Programming+Call)

## **Report (Presented Nov. 17, 2021)**

[![](attachments/thumbnails/21954756/21966098)](attachments/21954756/21966098.pptx)

## **Milestones**

**Eval 1:**

- a Integrate TrustID with Fabric
- b Demonstrate how to sign transactions with offline private key stored in clients browser session

**Eval 2:**

- c Create WebSocket identity server
- d WebSocket client wallet

**Eval 3:**

- e. Integrate web socket into blockchain carbon accounting
- f. Command line scripts to generate keys, register and enroll users, invoke, and query Fabric chain code

**Eval 4:**

- g. Demo full cycle of generating security keys at client, registering and enrolling users, and invoking and querying on Fabric chain code.
- h. Documentation of  identity solutions to access Fabric application with third party key management toolsEstablish authentication protocol to connect client application (e.g., mobile app and cyrpto wallet) to Fabric application.

## **Timeline**

WeekTask/PlanStatus**May 24 - May 28**Set up project plan.    
**May 31 - June 11**Review [TrustID from our previous call](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/2021-01-18+Peer+Programming+Call).  Develop plan for integrating Fabric, TrustID, and Metamask.  Integrate TrustID with Fabric.  
***June 14 - June 25***

*Finish integration of TrustID with Fabric.  Integrate Metamask into TrustID to sign Fabric transactions.*

**This Task has been revised as these weeks I have simply been understanding how to sign transactions on Fabric with private key and csr generated by the client offline (not the Fabrik SDK).   The key only needs to be stored on the client wallet ( metamask), as singing can be done off the server.**

**We could also share the pKey generated by the Fabric (TrustID app) with the client to upload to their wallet. However, the key generator must be compatible with the client Wallet. In the case of Ethreum (e.g. Metamask) we need to generate secp256k1 key, however fabric certificate signer does not support this EC.**

**Trust ID is a good solution as it can register a public key (DID) generated from custom private key that is authorized by Fabric CA to commit endorsements to the chaincode. Note, Trust ID currently only supports infra EC P-521, but this should be easy to update.**

Based on discussion with the mentors, the first task was reframed as completing the offline signing of transactions on Fabric using a private key (secp256k1 for ethereum compatibility) generated by the client and store on their wallet (not on the server). The next task Next we want to use the private key to establish a DID (e.g. using TrustID) that can be used to access other networks

**June 28 - July 2**

Get ready for first Evaluation.

Return to TrustID integration to register secp256k1 DID to execute transactions on Fabric.

**July 5 - July 9**

Integrate Hardware Security Module (HSM) into utility emission channel client app using softHSM. Include softHSM libraries when building API docker image. Initialize softHSm token to be used when enrolling new users.

Update register and enrol typescript to save HSMX.509 identity to local filesystem.

Complete

**July 12 - July 23**

Prepare schematic for HSM integration with fabric node. Research HSM cloud integration. Understand how to create a proxy pod that connects the client app/service to the HSM device. I.e., the HSM device (e.g. softHSM) is not part of the same container image as the hyper-ledger Fabric node. E.g., see [https://developer.ibm.com/articles/leverage-ibm-cloud-hsm-in-your-ibp-network/](https://developer.ibm.com/articles/leverage-ibm-cloud-hsm-in-your-ibp-network/)

Complete**July 26 - August 6**Implement proxy to link external HSM device (e.g., softHSM) to fabric client app. Understand how to configure HSMoptions to setup and add external HSMprovider to a wallet with HSMX509 types.Abandoned**August 9 - August 13**

Shift focus from HSM to implementing web-socket based identity provider for fabric client security.

Review web-socket functionality. Understand how to run test with web-socket. 

Complete**August 16 - August 27**

Set-up severs side logic for web-socket identity provider.

Client that handles communication with the external key client (e.g. browser extension).

Server key file that handles crypto logic like generating CSR files and requesting client signature

Identity provider logic that establishes the web socket server and wait for incoming connection from external client that will handle the signing. 

Complete

**August 30 - Sept 13**

Integrate web socket into blockchain carbon accountin

Command line scripts to generate keys, register and enroll users, invoke, and query Fabric chain code

complete

**Sept 13 - Sept 27**Eval 3 on October 1complete**Sept 27 - Oct 11**

Demo full cycle of generating security keys at client, registering and enrolling users, and invoking and querying on Fabric chain code.

Develop documentation for 3rd party identity management and key storage solutions

complete**Oct 11 - Oct 25**

Establish authentication protocol to connect client application to Fabric typescript app (e.g. utility emissions channel), and authenticate Fabric app to access client's external private key signing tools.

Complete

**Oct 25 - Nov 8**

**Nov 8 - Nov 12**

Wrap up of the project

Final evaluation and presentation of project on November 12

Complete

## **Tasks**

## **Methodology:** offline signing of transactions using private keys stored in the client browser.

1. This [demo](https://github.com/brioux/fabric-client-signer) illustrates the process for offline signing and could be extended to implement a browser signer extension (something like Metamask) for a Fabric network.
   
   1. generate a csr using some client provided private key / encryption algorithm. (e.g. ECDSA prime256v1);
   2. include the self-signed csr generated from the private key when enrolling new user with the fabric CA client;
   3. build endorsement proposal with transaction payload and sign using the private keys encryption algorithm;
   4. send signed proposal to required peers and check responses;
   5. if valid build a new commit with the endorsement from (2), sign commit with the private key encryption and send to peers;
2. A better approach to achieve off-line signing is to create a custom identity provider that implements the fabric-network IdentityProvider class.
3. In this project we developed a web-socket based identity provider for WsX509 identity credential types. A secure web-socket connection handles the sending of digests from a fabric network server/application to be signed by an external client. [The components fo the web-socket identity provider can be found here](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities). The include:
   
   1. A [ws-identity](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities/ws-identity) server that relays signature requests made to fabric network as digest to the external client
   2. A [ws-wallet](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities/ws-wallet) that signs digests using a key-file stored on the clients external device (e.g. encrypted keyfile or HSM). The wallet handles the generation and management of key files. The ws-wallet can also be configured to store certificates (i.e. CSR pem files) signed by the external client when enrolling with the Fabric application.
   3. The fabric application that requests signatures from the external ws-wallet client. It requres API keys to access the session tickets opened on the ws-identity server with an external client
   4. A custom identity provider that setups the connection between the Fabric app, the ws-identity server and the external clients ws-wallet. An identity provider has been setup in using the cactus fabric connector in [cactus PR 293](https://github.com/hyperledger-labs/blockchain-carbon-accounting/pull/293).
   5. A dedicated [ws-identity-client](https://github.com/hyperledger-labs/blockchain-carbon-accounting/tree/main/secure-identities/ws-identity-client) is used to handle html requests between the identity provider of the Fabric app or the ws-wallet instance and the ws-identity server. However, this could be replaced by promise based http client like [axios](https://github.com/axios/axios)
4. A web-socket based identity provider is being built with typescript as an extension of the [IdentityProvider](https://hyperledger.github.io/fabric-sdk-node/release-2.2/module-fabric-network.IdentityProvider.html) interface of the Fabric network nodes.js SDK
5. The identity provider can be used to connect to any external client, such as a browser, mobile app, client wallet operating on a dedicated server or IoT devicep.

## Entity-control-boundary for ws-identity sessions

- control WsClient : web-socket client of the external User
- boundary WsWallet : crypto wallet of the User
- actor User : External user of the Fabric App
- boundary FabricApp : The Fabric app
- control WsIdentityServer : web-socket identity server
- control WsClientServer : User's web-socket client on the identity server

[![ws-identity session](https://github.com/hyperledger-labs/blockchain-carbon-accounting/raw/main/secure-identities/docs/WsIdentity.png)](https://github.com/hyperledger-labs/blockchain-carbon-accounting/blob/main/secure-identities/docs/WsIdentity.png)

Another effort in this project is to integrate a Hardware Security Module (HSM) using the [HSMX509Provider](https://hyperledger.github.io/fabric-sdk-node/release-2.2/module-fabric-network.HsmX509Provider.html) class, however at the time of writting this did not support asynchronous requests to an external client. A secure proxy server, similar to the ws-identity server described above, is needed to relay requests between the Fabric app and the external HSM. Infact, ws-wallet could be setup to use an HSM for local key storage and signing when handling requests from ws-identity. A pin should be provided to access the HSM singing algorithm.

![](attachments/21954756/21965208.jpg)

## Attachments:

![](images/icons/bullet_blue.gif) [Fabric HSM Identity (1).jpg](attachments/21954756/21965208.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation Template - Nov2021.pptx](attachments/21954756/21966098.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)

Document generated by Confluence on Nov 26, 2024 14:57

[Atlassian](http://www.atlassian.com/)
