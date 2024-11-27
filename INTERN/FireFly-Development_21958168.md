1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [The Giving Chain](The-Giving-Chain_21957087.html)
6. [Project Plan Giving Chain](Project-Plan-Giving-Chain_21964753.html)
7. [Technical Track](Technical-Track_21957774.html)

# Hyperledger Mentorship Program : FireFly Development

Created by MONA RASSOULI, last modified by Bobbi Muscara on Oct 13, 2021

# 10/13

![](attachments/21958168/21965861.png?height=250)

# ![](attachments/21958168/21965862.png?height=250)

# ![](attachments/21958168/21965864.png?height=250)

![](attachments/21958168/21965863.png?height=250)

# D![](attachments/21958168/21965865.png?height=250)

![](attachments/21958168/21965866.png?height=250)

# ev![](attachments/21958168/21965867.png?height=250)

# ![](attachments/21958168/21965868.png?height=250)

# ![](attachments/21958168/21965869.png?height=250)

# ![](attachments/21958168/21965870.png?height=250)

![](attachments/21958168/21965871.png?height=250)

![](attachments/21958168/21965872.png?height=250)

![](attachments/21958168/21965873.png?height=250)

![](attachments/21958168/21965874.png?height=250)

![](attachments/21958168/21965875.png?height=250)

![](attachments/21958168/21965876.png?height=250)

![](attachments/21958168/21965877.png?height=250)

# elopment Needs

# Setup in Local:

Please see the following document for local setup: 

[![](attachments/thumbnails/21958168/21965544)](attachments/21958168/21965544.pdf)

# Good Resources:

- [https://www.youtube.com/watch?v=Ft1A9B9GPhU](https://www.youtube.com/watch?v=Ft1A9B9GPhU)
- [https://lf-hyperledger.atlassian.net/wiki/display/labs/FireFly](https://lf-hyperledger.atlassian.net/wiki/display/labs/FireFly)
- [https://github.com/hyperledger-labs/firefly-cli](https://github.com/hyperledger-labs/firefly-cli)
- [https://labs.hyperledger.org/firefly/gettingstarted/firefly\_cli.html](https://labs.hyperledger.org/firefly/gettingstarted/firefly_cli.html)

Start Your Environment:

Stack - the set of runtimes needed to simulate a multi-party network on one machine. These machines are automatically connected by FF CLI configuration specifications. 

Start with two members

Stack has a Data directory that holds all configurations

Stack starts and stops in docker using docker composer to manage cross container networking and to start/stop stacks runtimes together.

Examples:

[private-data-transfer-cli](https://github.com/hyperledger/firefly-samples/blob/main/private-data-transfer-cli), 

[private-data-transfer-ui](https://github.com/hyperledger/firefly-samples/blob/main/private-data-transfer-ui), 

### BROADCAST DATA a `message`

MESSAGES: WHO SENT

- Sends a `message` visible to all parties in the network
  
  - The message describes who sent it, and exactly what data was sent
- A `message` has one or more attached pieces of business `data`
  
  - Can be sent in-line, uploaded in advance, or received from other parties
  - Can include smaller JSON payloads suitable for database storage
    
    - These can be verified against a `datatype`
  - Can include references to large (multi-megabyte/gigabyte) BLOB data
- Sequenced via the blockchain
  
  - The blockchain does not contain any data, just a hash pin
- Batched for efficiency
  
  - One `batch` can pin hundreds of `message` broadcasts
  - The whole batch is written to the shared storage

### Privately send data

- Sends a `message` to a restricted set of parties
  
  - The message describes who sent it, to whom, and exactly what data was sent
- A `message` has one or more attached pieces of business `data`
  
  - Can be sent in-line, uploaded in advanced, or received from other parties
  - Can include smaller JSON payloads suitable for database storage
    
    - These can be verified against a `datatype`
  - Can include references to large (multi megabyte/gigabyte) BLOB data
- A `group` specifies who has visibility to the data
  
  - The author must be included in the group - auto-added if omitted
  - Can be specified in-line in the message by listing recipients directly
  - Can be referred to by hash
- Private sends are *optionally* sequenced via pinning to the blockchain
  
  - If the send is pinned:
    
    - The blockchain does not contain any data, just a hash pin
      
      - Even the ordering context (topic) is obscured in the on-chain data
      - This is true regardless of whether a restricted set of participants are maintaining the ledger, such as in the case of a Fabric Channel.
    - The message should not be considered confirmed (even by the sender) until it has been sequenced via the blockchain and a `message_confirmed` event occurs
    - Batched for efficiency
      
      - One `batch` can pin hundreds of private `message` sends
      - The batch flows privately off-chain from the sender to each recipient
  - If the send is unpinned:
    
    - No data is written to the blockchain at all
    - The message is marked confirmed immediately
      
      - The sender receives a `message_confirmed` event immediately
    - The other parties in the group get `message_confirmed` events as soon as the data arrives

### Listen for events

- Probably the most important aspect of FireFly is that it is an *event-driven programming model*.
- Parties interact by sending messages and transactions to each other, on and off chain. Once aggregated and confirmed those events drive processing in the other party.
- This allows the orchestration of complex multi-party system applications and business processes.
- FireFly provides each party with their own private history, that includes all exchanges outbound and inbound performed through the node into the multi-party system. That includes blockchain backed transactions, as well as completely off-chain message exchanges.
- The event transports are pluggable. The core transports are WebSockets and Webhooks. We focus on WebSockets in this getting started guide.
- *Check out the Request/Reply section for more information on Webhooks*

### Define a datatype

- As your use case matures, it is important to agree formal datatypes between the parties. These *canonical* datatypes need to be defined and versioned, so that each member can extract and transform data from their internal systems into this datatype.
- Datatypes are broadcast to the network so everybody refers to the same JSON schema when validating their data. The broadcast must complete before a datatype can be used by an application to upload/broadcast/send data. The same system of broadcast within FireFly is used to broadcast definitions of datatypes, as is used to broadcast the data itself.

## Responsibilities &amp; Pluggable Elements

More importantly, what the split of responsibilities is between `Connectors` and `Infrastructure Runtimes`.

- `Connectors` are the bridging runtimes, that know how to talk to a particular runtime.
  
  - They run separately to the core (like a microservice architecture of an app).
  - They can be written in any language (not just Go) - Java, TypeScript, Rust, Python, .NET etc.
  - They can use any network transport (not just HTTPS/Websockets) - GRPC, AMQP, UDP etc.
  - They connect to the core with a Golang shim - see separate *Plugin Architecture* discussion.
    
    > - In some special cases (like the Database) the Golang shim does not need a connector runtime.
- `Infrastructure Runtimes` are the core runtimes for multi-party system activities.
  
  - Blockchain nodes - Ethereum (Hyperledger Besu, Quorum, Geth), Hyperledger Fabric, Corda etc.
  - Public strorage - IPFS etc.
  - Database - PostreSQL, CouchDB etc.
- ![FireFly Plugin Architecture](https://hyperledger.github.io/firefly/images/firefly_plugin_architecture.svg)

## Attachments:

![](images/icons/bullet_blue.gif) [Giving Chain August 20-bobbi Slides gc.pptx](attachments/21958168/21965543.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)  
![](images/icons/bullet_blue.gif) [FF-Setup.pdf](attachments/21958168/21965544.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-14-1.png](attachments/21958168/21965861.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-14-18.png](attachments/21958168/21965862.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-15-0.png](attachments/21958168/21965863.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-15-24.png](attachments/21958168/21965864.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-15-52.png](attachments/21958168/21965865.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-16-13.png](attachments/21958168/21965866.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-16-27.png](attachments/21958168/21965867.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-16-43.png](attachments/21958168/21965868.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-17-3.png](attachments/21958168/21965869.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-36-43.png](attachments/21958168/21965870.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-36-57.png](attachments/21958168/21965871.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-37-20.png](attachments/21958168/21965872.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-37-32.png](attachments/21958168/21965873.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-37-46.png](attachments/21958168/21965874.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-37-59.png](attachments/21958168/21965875.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-38-11.png](attachments/21958168/21965876.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_11-38-23.png](attachments/21958168/21965877.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_14-13-6.png](attachments/21958168/21965879.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_14-13-32.png](attachments/21958168/21965880.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_14-13-50.png](attachments/21958168/21965881.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_14-14-4.png](attachments/21958168/21965882.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_14-14-58.png](attachments/21958168/21965883.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_14-15-12.png](attachments/21958168/21965884.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_14-15-20.png](attachments/21958168/21965885.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_14-15-43.png](attachments/21958168/21965886.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2021-10-13\_14-16-1.png](attachments/21958168/21965887.png) (image/png)

Document generated by Confluence on Nov 26, 2024 14:58

[Atlassian](http://www.atlassian.com/)
