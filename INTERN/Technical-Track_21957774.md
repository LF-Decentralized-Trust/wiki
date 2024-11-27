1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [The Giving Chain](The-Giving-Chain_21957087.html)
6. [Project Plan Giving Chain](Project-Plan-Giving-Chain_21964753.html)

# Hyperledger Mentorship Program : Technical Track

Created by Bobbi Muscara, last modified on Oct 25, 2021

Determine next steps:

### Tech Team Updates

- The link to FireFly CLI: [https://github.com/hyperledger/firefly-cli](https://github.com/hyperledger/firefly-cli)
- All the code is being uploaded at our Github: [https://github.com/DecoratedWings/GivingChain-ui](https://github.com/DecoratedWings/GivingChain-ui)

GETTING STARTED FOR DEV's

Part 1

Github Repository  
 [https://github.com/DecoratedWings/GivingChain-ui](https://github.com/DecoratedWings/GivingChain-ui)

Part 2  
Play with Firefly CLI   (India Chapter youtube video has the best Demo)

Part 3  
FIREFLY's API: API and it what order (Postman file getting started from Mona )

PArt 4  
Token Connector?  
From ff team: Postman queries for "Mint w/ Data" and "Transfer w/ Data" can work on the very latest FireFly code.

### \*Strikethrough indicates Completion of Task

### 10/12

GET  Developers STARTED: Firefly creates a signing address on the bc for you. Not on Mainnet, on our FF instance.   

Issues for DevelopersAssignmentOwnerCommentsDatabase issuesPostgres or sequel lite,

leverage your API

Create Token pool for NFT

P[RESENTATIONScreate  the Platform team - we can transfer from 

mint it with **QR code**

QR code

Front endPOC hosting each node on a tab . Donor tabRegistration, Donor Transporter Recipient Page  
Solidity

pLocal -private ipfs upload, Docker named volume no server ff start, same data will be there.  ff reset of ff remove will clear out data.  

Token Connector  
token or requests of firefly endpoint to retrieve date erc721

Change how we mint nft :

Not using   
FF creates post requests to create the data, get back data-id that will reference image (w/in ff) the reference is what we will use.  I'm Local stack in the private IPFS 

smart-contract method to mint nft's

Set up contracts

Token to point to IPFS, Use Firefly IPfs, upload file to ff, it will put it on IPFS,  OPen to Giving chain consortium 9 HASH IPFS and w/ HTTP or FF API 

CIDHAsh of content identifier, the value returned might be hash returned in code or in data table in FF database and keep track of all data items.

We need a way to link back to the image.  If we feed is into the solidity contract, would we need URL of where the image is hosted. URL each member GE IS HOSTED. 

NFT will get minted with ID of Image

Authentication 

set up user authentication (REACT) 

User Authentication - Nodes registration in ff but we don't want users to have that capability. 

ff is private not using public, means with in-network, Public doesn't mean public to the entire world.n

Forms

Auth. and user input data  
1.(register usr  name, donation address) 

2\. Nodes - donor info form, Driver form, and recipient 

BroadcastBoth private and network broadcast, some piece of information open to all and some information available private example - Donors location only for transporter.   
Donor mints, broadcast, able to supply an address to driver PrivatelyCreation of Datatype  
Data type, play with API. FF's blockchain network lets you create data type, fill out info about the data type. Every time we make a donationtest run  
interact with stack, show screenshots, data type  
Ask FF people, reach out to Nicko for good examples JSON types

Issues for Developers

The FireFly project focuses on:

Task

- Providing a great developer API and experience

<!--THE END-->

- CLI to get you running in minutes
- Explorer UI as first class project component
- APIs that abstract hard constructs into simple actions
- REST APIs for your private history of participation in the network
- Events built for web and microservice developers

<!--THE END-->

- Pluggability for implementations of multi-party system infrastructure

<!--THE END-->

- Blockchains, off-chain data exchange, identity, compute etc.
- Microservice runtime architecture, embracing a variety of tech stacks

<!--THE END-->

- Making proven multi-party system patterns easy for new projects to adopt

<!--THE END-->

- On-chain/off-chain coordination
- Multi-party business processes
- Tokens - NFTs, value transfer, and common trade patterns like atomic swaps

<!--THE END-->

- Providing developer friendly access to custom transactions+events in the underlying platforms

<!--THE END-->

- Easy submission of transactions
- Reliable access to events
- Plugins customized to each blockchain protocol: Fabric, Ethereum, Corda

<!--THE END-->

- Visibility and control on the flow of data a multi-party system

<!--THE END-->

- Network map backed by pluggable identity
- Private audit of participation in a local pluggable database
- Easy pinning of proofs on data exchange to the blockchain

### 10/8

POC - create 3 **metamask addresses with** the Platform team - we can transfer from 

mint it with **QR code**

broadcast it with QR code (driver can agree to get it then Donor waits for driver and only triggers nft transfer from **metamask wallet** when the actually good are transferred. Goods transfer,  NFT to Drivers wallet, QR code is in back gathering additional metadata. Scan code will ask the user to scan /upload a picture that is stored in metadata. (or put metadata on a chain) transfer then Donor recipient **metamask** get nft at final transfer. 

**QR code**

Meeting Notes:   
Get Specific task:

Budget

Set up Database  
Sql Lite

Front end

Solidity  
Task Open ZepplinHard hat framework  
erc721

smart-contract method to mint nft's

while working on the token connector.

-Hardik has the whole contract, working fine, send to group

Solidity Provide

Set up contracts

Token to point to IPFS

The mint function takes the address and token id, normally **message.sender** mint toa dres of person who called function. Ties back to security, limited addresses for minting? or anyone log in with address?

The project manager will allow registration

Burn mint and check balance, we have every function the erc20 token possesses.  Each has own address or group for donors. Counter for minting (id1, d 2, id3 )counter

Counterpart import "@openzeppelin/contracts/token/ERC721/extensions/ERC721URIStorage.sol"; import "@openzeppelin/contracts/utils/Counters.sol";

Transaction part

Assignment  
Owner"solidity backend"smart contract to do mintingHardik, MonaQR CodesScanning and formatted HardikAuthentication 

set up user authentication (REACT) 

User Authentication - Nodes registration in ff but we don't want users to have that capability. 

DatabaseLow Level, must do but can skip for POC  
Forms

Auth. and user input data  
1.(register usr  name, donation address) 

2\. Nodes - donor info form, Driver form, and recipient 

Donor mints, broadcast, able to supply an address to driver Privately  
Front endusing FF we have two request 

1. can broadcasts to network - working
2. Private message - working
3. Donor uploads

Bobbi will try mock-up of forms needed for data collection and mintingCreation of DatatypeData type, play with API. FF's blockchain network lets you create data type, fill out info about the data type. Every time we make a donation  
test runinteract with stack, show screenshots, Hardik, Monadata typeAsk FF people, reach out to Nicko for good examples JSON typesMona

front end forms - independent orgs. Logins login as one of the three, have to check on the roles 

\* Wireframes?  API interactions frontend need minting functionalities, UX UI design secondary to the blockchain. Where do we get mockups and templates for design? 

Mint NFT, Broadcast NFT and  send private message. 

Form Questions  to gather front end info. Google Forms can translate to React form and we can use information

Both private and network broadcast, some piece of information open to all and some information available private example - Donors location only for transporter. 

[https://hyperledger.github.io/firefly/swagger/swagger.html](https://hyperledger.github.io/firefly/swagger/swagger.html)  
[https://chat.hyperledger.org/channel/firefly](https://chat.hyperledger.org/channel/firefly)

Timeline for Project Completion  
 Social Impact - 10/26,

Mentorship Presentation

November 17th at 5 pm CET (11 am EST).

The FireFly project focusses on:TaskCompleted

- Providing a great developer API and experience

<!--THE END-->

- CLI to get you running in minutes
- Explorer UI as first class project component
- APIs that abstract hard constructs into simple actions
- REST APIs for your private history of participation in the network
- Events built for web and microservice developers

<!--THE END-->

- Pluggability for implementations of multi-party system infrastructure

<!--THE END-->

- Blockchains, off-chain data exchange, identity, compute etc.
- Microservice runtime architecture, embracing a variety of tech stacks

<!--THE END-->

- Making proven multi-party system patterns easy for new projects to adopt

<!--THE END-->

- On-chain/off-chain coordination
- Multi-party business processes
- Tokens - NFTs, value transfer, and common trade patterns like atomic swaps

<!--THE END-->

- Providing developer friendly access to custom transactions+events in the underlying platforms

<!--THE END-->

- Easy submission of transactions
- Reliable access to events
- Plugins customized to each blockchain protocol: Fabric, Ethereum, Corda

<!--THE END-->

- Visibility and control on the flow of data a multi-party system

<!--THE END-->

- Network map backed by pluggable identity
- Private audit of participation in a local pluggable database
- Easy pinning of proofs on data exchange to the blockchain

### 10/6  Team meeting to determine Tasks that needs to be completed and who is responsible.

Timeline to complete projects. 

Bobbi Muscara is inviting you to a scheduled Zoom meeting.

Topic: Giving Chain Re-group  
Time: Oct 6, 2021 08:30 AM Eastern Time (US and Canada)

Join Zoom Meeting  
[https://us02web.zoom.us/j/88311174204?pwd=czBDR3laRXJWTmE2QWluUXNBVHZIQT09](https://us02web.zoom.us/j/88311174204?pwd=czBDR3laRXJWTmE2QWluUXNBVHZIQT09)

Meeting ID: 883 1117 4204  
Passcode: 870113

### 10/ 1 Tech team meeting

### 9/27

Review Presentation

Review Technical Options

Divide Work. 

### 9/24

Friday re-group meeting

Must prepare for Wednesdays Trade Finance Meeting and send Andrea the Final version Monday 9/27

### 9/22

An NFT solution

[https://ownest.io/en](https://ownest.io/en)

Regroup Meeting

Agenda

Recap

Business

Technical

Get initial things ready

Development: BAckend 

![](attachments/21957774/21965749.png?height=250)

1. Can we add Postgres or sequel lite, step it up now for further development?
2. Can we leverage your API
3. We can create a token pool but cant mint NFT yet
4. Store it all in FF-free database?
5. How are nodes/entities treated in Firefly?  Technically, do you have 1 node per project or Multiple nodes in a project?
6. Wallet - ff creates its own blockchain wallet? or need to create an external wallet to support the token end
7. Follow-up photos - the original NFT will be created and embed the subsequent metadata of the NFT. NFT is used as the digital twin to the physical donation.  Does API allow us to meta 
   
   ?

![](plugins/servlet/confluence/placeholder/unknown-macro)

### 9/20

Nicko

Mona - 

1. NFT portion - use a token pool that FF has. Can you explain token pool, what stage 1155? applicable still . Thin extension to NF VS NFT. Can create pools, in the meantime we can set a unique ... to track ownership.  Hoping FF will have tech lower Levels we need to focus on upper layers of tech stack
2. A token pool allocates unique IDs to track donor to recipient, minting and transfer happen with that ID. That id is unique for the asset class, each thing inside has an index. The pool represents class, Index represents items.
3. integer id represents different types of

ETH connect - Earlier code, just a more user-friendly web interface in front of Ethereum. Provides functionality - internal utilities.  system governance issues handled.  We should not have to worry about it.  

ERV 1155, or just FF, if the connector is sufficient, we should mainly deal with FF. That layer should  be done for us

CLI - FF API  is where e will build app to build token pool mint and transfer.  FF creates, soon mints,s, and transfer all on the FF API.  1155 is it good enough?  Yes we think so. 

Bare Bottoms:

### Next Steps:

Download FF CLI

Start a FF Environment, and explore API

Start by the backend, what does the app need to do and build against ff API. 

Big constructs: Messaging and DAta

Reference piece a data between token and message. Get transfers down _ data flow= points of hand off with proof of real-world asset, take for of message with data points mapped out. ,. 

API calls - FF goal is to develop the business logic of the problem trying to solve ( interface user mgt... )  build all of it today except the token part. 

Do we need to solve identity registering 

*Business id done for Friday*

*Backend side - complete first then we can plugin API* 

*Many member network*

### Agenda:

### Intro

Hardik - described where we are in the project. 

Discuss Email

Hi. I'm catching up with James Barry and Bill in person as Taekion are a partner.

My understanding is that you are interested in the RocksDB implementation we've open-sourced under Apache but haven't had time to contribute to Hyperledger Sawtooth core.

I gather from talking to James that you aren't interested in using this unless it is contributed.

It would be great to have a call to discuss this. Please choose a time that works for you using [calendly.com/duncanjw](http://calendly.com/duncanjw)

Best  
\--

Duncan Johnston-Watt

CEO, [BTP](https://t.sidekickopen10.com/s3t/c/5/f18dQhb0S7kF8bq5kNW10qfgt59hl3kW7_k2847sD3qkVPwN4N1DWrmzW2bzNK99g4FWr101?te=W3R5hFj26QkG-W3ZZmPc3F7xMDW41Yzhd3Fbt5S0&si=7000000002188340&pi=dbaf5680-5fc8-4098-f387-aaa1928e61c0)

[@duncanjw](https://t.sidekickopen10.com/s3t/c/5/f18dQhb0S7kF8bq5kNW10qfgt59hl3kW7_k2847sD3qkVPwN4N1DWrmzW2bzNK99g4FWr101?te=W3R5hFj4cm2zwW4fQ47l4fGCmnW3Fbt5S3Hcwzwf3zdZnZ04&si=7000000002188340&pi=dbaf5680-5fc8-4098-f387-aaa1928e61c0)

[+44 777 190 2653]()  
[calendly.com/duncanjw](http://calendly.com/duncanjw)  
[linkedin.com/in/duncanjohnstonwatt](http://linkedin.com/in/duncanjohnstonwatt) 

9/17 

![](attachments/21957774/21965719.png?height=250)  ![](attachments/21957774/21965720.png?height=250)![](attachments/21957774/21965721.png?height=250)

Nicko - Question At end of the chain how does the donor know what he received? He will be able to track the donation thru the QR code as well as digital pictures.  A Picture IS taken at each transfer. QR represents the unique id associated w/ transaction. The Collection of NFT's (IPFS) hash will be stored and used as a link. Each picture's hash links back to the QR code.  Donor generates the first instance of QR code.

Is this feasible? YES ![(smile)](images/icons/emoticons/smile.png)

NFT will be stored on a local database.

Still working on tokens, NFT ARE NOT READY TO BE used out of the box. Is there a way to do this in a different way w/o nfts?

Upload a blob,  Store Image, and store hash. The payload can be transferred to other members of the network. Roll them up into transaction ID.  Can we make a collection of these Blobs? 

No concept of the collection, but generate a topic within firefly. it defines a narrowing ordering system. Topics get assigned to several messages and need to be processed in order. Donation run in Parrelle by topics, an end to end joining messages in a certain order

1. Upload an image and get data id
2. Send a message with tx id. Nodes that are part of the network can query by topic.
3. The message does not associate with a topic until it is sent (set the topic) Donor
4. Driver uploads message under a topic he can be sure it is the right topic with QR code or is embedded into the QR code.
5. Scan QR code and take a picture, send a message,...HERE IS THE NEXT ISSUE IN THE TOPIC

TECHNICAL

Be stored in a Database

1. What Database
2. How does it plug in (reaCT, FIREFLY/)
3. Firefly has its own database, you can query FF database. can't write to it. Postgres Sequel Lite (no SQL ) Create their own data structure and what rights they have. These permissions responsibilities are good for FF's database,  Uses whatever database works for you.
4. Backend app will listen for the event (WebSocket) so when nodes broadcast, that is how backend. can use WebSocket or hooks
5. Frontend....Backend... Databaseplement The database has records that represent the entirety of the event. Store the "NFTS" successful when aLL THREE HASHES ARE BROADCASTED.  The f/u Implentent end compilation of the "NFTS".

Digital Images can be transferred into an NFT, not available in **D2R release 1**

Token pools -  Feasible to set up a smart contract to mint the NFT after all three pictures are broadcast to the network. The photo gets minted to NFT with the Hash that it creates. We can upload to an infura node.  QR code is a different NFT. How do you prove it ? What is an NFT and where is it useful. Have an asset (digital Twin or Digital assets) who owns it, prove It on-chain.  Transfer event of NFT until it reached the final destination. 1 nft for the donation or an NFT for each digital picture.

Proof of ownership

Pan out - photo linked to QR code and topic. The donor will create the first photo which creates the asset. We could transfer NFT

Dynamic NFT's Chainlink demo - logo changed to show the weather where the physical item was.

How did we get here?  Idea was to prove Providence of the donation but can we also make it proof of ownership. Have QR code on the product - evident in every photo (QR Code). 

Each time NFT transfers, the next photo stores data or hash, we put metadata that is an external pointer as proof of transfer (can look it up) solve for proof of ownership by looking at the flow. NFT has Meta data of transfer time with the matching photo.

The donor has 1 nft (proof of ownership) metadata in NFT that can be associated metadata with a transfer. If I am transferring an nft from me to you we can associate data with that transfer (on chain) Take a photo at step 1, get hash and ipfs address, associate that data with the transfer process. Prove it on the blockchain. Also look up on IPFS, state of thing when it was handed off. View on IPFS and the only NFT is the first on. Transfer - must provide picture at handoff that becomes part of the NFT in the metadata.   Minteing them on IPFS has

Next step for a demo

1. The hopeful token will finish soon and we can build on that. Today we can code * token connector, reference implementation.  Sort thru smart contract. Off the shelf, the solution will meet our needs.  Not use NFT use firefly to upload images and send that data to members grouped into a topic.  We can write that app today and then improve code when NFT capabilities are out.

DEMO is up and running. Which is the best representative document set up. Create using this link TOKEN CONNECTOR Build a separate app for the token connector. 

 [https://github.com/hyperledger-labs/firefly-tokens-erc1155](https://github.com/hyperledger-labs/firefly-tokens-erc1155)

Option 1 - tokens will be ready let's start building Yes ![(smile)](images/icons/emoticons/smile.png)

Option 2 - build today with what's available. Nah ![(sad)](images/icons/emoticons/sad.png)

The project end date is November 5th, we are willing to work on a token solution.

HOMEWORK  
[https://github.com/hyperledger-labs/firefly-tokens-erc1155](https://github.com/hyperledger-labs/firefly-tokens-erc1155)

1. 1155 Ethereum protocol - does it need our needs, we can use the token connector as is.
2. Set up a Monday meeting to regroup!

Great Team work!!!

Agenda 

![](attachments/21957774/21965715.png?height=126)

Brief Presentation

Questions and Answer

9/1 Hardik joined FireFly and mentioned the Bug Fix of Mona. He will incorporate it into their Documentation.

[https://github.com/accordproject/hlf-cicero-contract](https://github.com/accordproject/hlf-cicero-contract)

[https://www.meetup.com/Hyperledger-Bangalore/events/280318418/](https://www.meetup.com/Hyperledger-Bangalore/events/280318418/)

[![](attachments/thumbnails/21957774/21965556)](attachments/21957774/21965556.pdf)

**Name****Email Address****Talent**GithubHardik Gupta[hardikgupta068@gmail.com](mailto:hardikgupta068@gmail.com)Project Mentee / Project Management / Technical Lead7/26Mona Rassouli[mr1241@scarletmail.rutgers.edu](mailto:mr1241@scarletmail.rutgers.edu)Developer/ Marketing(social media)/Documentation/ Articles or Blogs  
Devrata Puri [devratapuri@gmail.con](mailto:devratapuri@gmail.con)Developer   
K Sanjay Kumar[ksanjay99kumar@gmail.com](mailto:ksanjay99kumar@gmail.com)Developer  
Madhu Bhatia[bhatia.madhu23@gmail.com](mailto:bhatia.madhu23@gmail.com)Documentation/Paper, Articles Publication  
Divyansh Garg[divyanshgh2@gmail.com](mailto:divyanshgh2@gmail.com)Developer/Network Architect  
Harsh Vardhan Singh Rawat[harsh.sinkara1@gmail.com](mailto:harsh.sinkara1@gmail.com)UI/UX Designer, Market Analyst, Content Writing

Business Process definition:  
NFT -  How will NFT is transferred correctly _ erc721 contract  (compares photos Before and after)

STEPS one

Contract  
Image  
Hosting

To Do

Build Interface 

USE Case

Princeton

- Enroll Participants
  
  The project manager enrolled as an Admin
  
  Transporter Donors and Recipients enrolled by Admin or directly thru a website
- Track Donations
  

. 

Enter as a Lab [https://labs.hyperledger.org/](https://labs.hyperledger.org/)

![](plugins/servlet/confluence/placeholder/unknown-attachment)

◦Is available as an instance of **Sawtooth chain** **on a single node** (Dev); with the ability to:

◦create key-pairs

◦create assets

◦Transfer assets ( accept or reject the asset)

◦ Explorer , a  view-able tracking of the current holder of the asset from the current front-end interface.

![](attachments/21957774/21965106.png?height=250)

TODO

Create three user interfaces that attach to the backend 

Backend Blockchain that can track giving chain donations from recipient to donor. 

### 9/27

Review Presentation

Review Technical Options: API looks Great .

Can we Demo something next week, next month , next year

Divide Work. 

### 9/24

Friday re-group meeting

Must prepare for Wednesdays Trade Finance Meeting and send Andrea the Final version Monday 9/27

### 9/22

An NFT solution

[https://ownest.io/en](https://ownest.io/en)

Regroup Meeting

Agenda

Recap

Business

Technical

Get initial things ready

Development: BAckend 

![](attachments/21957774/21965749.png?height=250)

1. Can we add Postgres or sequel lite, step it up now for further development?
2. Can we leverage your API
3. We can create a token pool but cant mint NFT yet
4. Store it all in FF-free database?
5. How are nodes/entities treated in Firefly?  Technically, do you have 1 node per project or Multiple nodes in a project?
6. Wallet - ff creates its own blockchain wallet? or need to create an external wallet to support the token end
7. Follow-up photos - the original NFT will be created and embed the subsequent metadata of the NFT. NFT is used as the digital twin to the physical donation.  Does API allow us to meta 
   
   ?

![](plugins/servlet/confluence/placeholder/unknown-macro)

### 9/20

Nicko

Mona - 

1. NFT portion - use a token pool that FF has. Can you explain token pool, what stage 1155? applicable still . Thin extension to NF VS NFT. Can create pools, in the meantime we can set a unique ... to track ownership.  Hoping FF will have tech lower Levels we need to focus on upper layers of tech stack
2. A token pool allocates unique IDs to track donor to recipient, minting and transfer happen with that ID. That id is unique for the asset class, each thing inside has an index. The pool represents class, Index represents items.
3. integer id represents different types of

ETH connect - Earlier code, just a more user-friendly web interface in front of Ethereum. Provides functionality - internal utilities.  system governance issues handled.  We should not have to worry about it.  

ERV 1155, or just FF, if the connector is sufficient, we should mainly deal with FF. That layer should  be done for us

CLI - FF API  is where e will build app to build token pool mint and transfer.  FF creates, soon mints,s, and transfer all on the FF API.  1155 is it good enough?  Yes we think so. 

Bare Bottoms:

### Next Steps:

Download FF CLI

Start a FF Environment, and explore API

Start by the backend, what does the app need to do and build against ff API. 

Big constructs: Messaging and DAta

Reference piece a data between token and message. Get transfers down _ data flow= points of hand off with proof of real-world asset, take for of message with data points mapped out. ,. 

API calls - FF goal is to develop the business logic of the problem trying to solve ( interface user mgt... )  build all of it today except the token part. 

Do we need to solve identity registering 

*Business id done for Friday*

*Backend side - complete first then we can plugin API* 

*Many member network*

### Agenda:

### Intro

Hardik - described where we are in the project. 

Discuss Email

Hi. I'm catching up with James Barry and Bill in person as Taekion are a partner.

My understanding is that you are interested in the RocksDB implementation we've open-sourced under Apache but haven't had time to contribute to Hyperledger Sawtooth core.

I gather from talking to James that you aren't interested in using this unless it is contributed.

It would be great to have a call to discuss this. Please choose a time that works for you using [calendly.com/duncanjw](http://calendly.com/duncanjw)

Best  
\--

Duncan Johnston-Watt

CEO, [BTP](https://t.sidekickopen10.com/s3t/c/5/f18dQhb0S7kF8bq5kNW10qfgt59hl3kW7_k2847sD3qkVPwN4N1DWrmzW2bzNK99g4FWr101?te=W3R5hFj26QkG-W3ZZmPc3F7xMDW41Yzhd3Fbt5S0&si=7000000002188340&pi=dbaf5680-5fc8-4098-f387-aaa1928e61c0)

[@duncanjw](https://t.sidekickopen10.com/s3t/c/5/f18dQhb0S7kF8bq5kNW10qfgt59hl3kW7_k2847sD3qkVPwN4N1DWrmzW2bzNK99g4FWr101?te=W3R5hFj4cm2zwW4fQ47l4fGCmnW3Fbt5S3Hcwzwf3zdZnZ04&si=7000000002188340&pi=dbaf5680-5fc8-4098-f387-aaa1928e61c0)

[+44 777 190 2653]()  
[calendly.com/duncanjw](http://calendly.com/duncanjw)  
[linkedin.com/in/duncanjohnstonwatt](http://linkedin.com/in/duncanjohnstonwatt) 

9/17 

![](attachments/21957774/21965719.png?height=250)  ![](attachments/21957774/21965720.png?height=250)![](attachments/21957774/21965721.png?height=250)

Nicko - Question At end of the chain how does the donor know what he received? He will be able to track the donation thru the QR code as well as digital pictures.  A Picture IS taken at each transfer. QR represents the unique id associated w/ transaction. The Collection of NFT's (IPFS) hash will be stored and used as a link. Each picture's hash links back to the QR code.  Donor generates the first instance of QR code.

Is this feasible? YES ![(smile)](images/icons/emoticons/smile.png)

NFT will be stored on a local database.

Still working on tokens, NFT ARE NOT READY TO BE used out of the box. Is there a way to do this in a different way w/o nfts?

Upload a blob,  Store Image, and store hash. The payload can be transferred to other members of the network. Roll them up into transaction ID.  Can we make a collection of these Blobs? 

No concept of the collection, but generate a topic within firefly. it defines a narrowing ordering system. Topics get assigned to several messages and need to be processed in order. Donation run in Parrelle by topics, an end to end joining messages in a certain order

1. Upload an image and get data id
2. Send a message with tx id. Nodes that are part of the network can query by topic.
3. The message does not associate with a topic until it is sent (set the topic) Donor
4. Driver uploads message under a topic he can be sure it is the right topic with QR code or is embedded into the QR code.
5. Scan QR code and take a picture, send a message,...HERE IS THE NEXT ISSUE IN THE TOPIC

TECHNICAL

Be stored in a Database

1. What Database
2. How does it plug in (reaCT, FIREFLY/)
3. Firefly has its own database, you can query FF database. can't write to it. Postgres Sequel Lite (no SQL ) Create their own data structure and what rights they have. These permissions responsibilities are good for FF's database,  Uses whatever database works for you.
4. Backend app will listen for the event (WebSocket) so when nodes broadcast, that is how backend. can use WebSocket or hooks
5. Frontend....Backend... Databaseplement The database has records that represent the entirety of the event. Store the "NFTS" successful when aLL THREE HASHES ARE BROADCASTED.  The f/u Implentent end compilation of the "NFTS".

Digital Images can be transferred into an NFT, not available in **D2R release 1**

Token pools -  Feasible to set up a smart contract to mint the NFT after all three pictures are broadcast to the network. The photo gets minted to NFT with the Hash that it creates. We can upload to an infura node.  QR code is a different NFT. How do you prove it ? What is an NFT and where is it useful. Have an asset (digital Twin or Digital assets) who owns it, prove It on-chain.  Transfer event of NFT until it reached the final destination. 1 nft for the donation or an NFT for each digital picture.

Proof of ownership

Pan out - photo linked to QR code and topic. The donor will create the first photo which creates the asset. We could transfer NFT

Dynamic NFT's Chainlink demo - logo changed to show the weather where the physical item was.

How did we get here?  Idea was to prove Providence of the donation but can we also make it proof of ownership. Have QR code on the product - evident in every photo (QR Code). 

Each time NFT transfers, the next photo stores data or hash, we put metadata that is an external pointer as proof of transfer (can look it up) solve for proof of ownership by looking at the flow. NFT has Meta data of transfer time with the matching photo.

The donor has 1 nft (proof of ownership) metadata in NFT that can be associated metadata with a transfer. If I am transferring an nft from me to you we can associate data with that transfer (on chain) Take a photo at step 1, get hash and ipfs address, associate that data with the transfer process. Prove it on the blockchain. Also look up on IPFS, state of thing when it was handed off. View on IPFS and the only NFT is the first on. Transfer - must provide picture at handoff that becomes part of the NFT in the metadata.   Minteing them on IPFS has

Next step for a demo

1. The hopeful token will finish soon and we can build on that. Today we can code * token connector, reference implementation.  Sort thru smart contract. Off the shelf, the solution will meet our needs.  Not use NFT use firefly to upload images and send that data to members grouped into a topic.  We can write that app today and then improve code when NFT capabilities are out.

DEMO is up and running. Which is the best representative document set up. Create using this link TOKEN CONNECTOR Build a separate app for the token connector. 

 [https://github.com/hyperledger-labs/firefly-tokens-erc1155](https://github.com/hyperledger-labs/firefly-tokens-erc1155)

Option 1 - tokens will be ready let's start building Yes ![(smile)](images/icons/emoticons/smile.png)

Option 2 - build today with what's available. Nah ![(sad)](images/icons/emoticons/sad.png)

The project end date is November 5th, we are willing to work on a token solution.

HOMEWORK  
[https://github.com/hyperledger-labs/firefly-tokens-erc1155](https://github.com/hyperledger-labs/firefly-tokens-erc1155)

1. 1155 Ethereum protocol - does it need our needs, we can use the token connector as is.
2. Set up a Monday meeting to regroup!

Great Team work!!!

Agenda 

![](attachments/21957774/21965715.png?height=126)

Brief Presentation

Questions and Answer

9/1 Hardik joined FireFly and mentioned the Bug Fix of Mona. He will incorporate it into their Documentation.

[https://github.com/accordproject/hlf-cicero-contract](https://github.com/accordproject/hlf-cicero-contract)

[https://www.meetup.com/Hyperledger-Bangalore/events/280318418/](https://www.meetup.com/Hyperledger-Bangalore/events/280318418/)

[![](attachments/thumbnails/21957774/21965556)](attachments/21957774/21965556.pdf)

**Name****Email Address****Talent**GithubHardik Gupta[hardikgupta068@gmail.com](mailto:hardikgupta068@gmail.com)Project Mentee / Project Management / Technical Lead7/26Mona Rassouli[mr1241@scarletmail.rutgers.edu](mailto:mr1241@scarletmail.rutgers.edu)Developer/ Marketing(social media)/Documentation/ Articles or Blogs  
Devrata Puri [devratapuri@gmail.con](mailto:devratapuri@gmail.con)Developer   
K Sanjay Kumar[ksanjay99kumar@gmail.com](mailto:ksanjay99kumar@gmail.com)Developer  
Madhu Bhatia[bhatia.madhu23@gmail.com](mailto:bhatia.madhu23@gmail.com)Documentation/Paper, Articles Publication  
Divyansh Garg[divyanshgh2@gmail.com](mailto:divyanshgh2@gmail.com)Developer/Network Architect  
Harsh Vardhan Singh Rawat[harsh.sinkara1@gmail.com](mailto:harsh.sinkara1@gmail.com)UI/UX Designer, Market Analyst, Content Writing

Business Process definition:  
NFT -  How will NFT is transferred correctly _ erc721 contract  (compares photos Before and after)

STEPS one

Contract  
Image  
Hosting

To Do

Build Interface 

USE Case

Princeton

- Enroll Participants
  
  The project manager enrolled as an Admin
  
  Transporter Donors and Recipients enrolled by Admin or directly thru a website
- Track Donations
  

. 

Enter as a Lab [https://labs.hyperledger.org/](https://labs.hyperledger.org/)

![](plugins/servlet/confluence/placeholder/unknown-attachment)

◦Is available as an instance of **Sawtooth chain** **on a single node** (Dev); with the ability to:

◦create key-pairs

◦create assets

◦Transfer assets ( accept or reject the asset)

◦ Explorer , a  view-able tracking of the current holder of the asset from the current front-end interface.

![](attachments/21957774/21965106.png?height=250)

TODO

Create three user interfaces that attach to the backend 

Backend Blockchain that can track giving chain donations from recipient to donor. 

## Attachments:

![](images/icons/bullet_blue.gif) [image2021-7-12\_14-57-37.png](attachments/21957774/21965018.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-7-19\_11-20-28.png](attachments/21957774/21965106.png) (image/png)  
![](images/icons/bullet_blue.gif) [FF-Setup.pdf](attachments/21957774/21965556.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [image2021-9-17\_11-56-46.png](attachments/21957774/21965715.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-9-17\_13-2-16.png](attachments/21957774/21965719.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-9-17\_13-3-1.png](attachments/21957774/21965720.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-9-17\_13-3-28.png](attachments/21957774/21965721.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-9-22\_10-31-41.png](attachments/21957774/21965749.png) (image/png)  
![](images/icons/bullet_blue.gif) [Registration Process](attachments/21957774/21965747) (application/gliffy+json)  
![](images/icons/bullet_blue.gif) [Registration Process.png](attachments/21957774/21965748.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-12\_13-31-6.png](attachments/21957774/21965854.png) (image/png)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/21957774/21965101.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 14:57

[Atlassian](http://www.atlassian.com/)
