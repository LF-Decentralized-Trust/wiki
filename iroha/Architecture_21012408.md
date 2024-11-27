1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)

# Hyperledger Iroha : Architecture

Created by Nikita Puzankov, last modified by Vadim Reutskiy on Aug 24, 2020

# Conceptual View

This section describes the object model of the design.

Layers

According to [Dan Boneh](https://youtu.be/V0JdeRzVndI) Blockchain applications may be divided into four layers:

3User Interface2Applications1.5Compute Layer1Consensus Layer

We will use this classifications to group Iroha components and 3rd party components that can be integrated with Iroha components.

## Components

LayerComponentsDescriptionUser Interface

Iroha Clients + 3rd Party Clients

Web/Mobile/CLI

User Facing ServicesApplicationsIroha Modules + Custom Iroha Special InstructionsRun on blockchain computerCompute LayerIroha + Iroha Modules + Iroha Special InstructionsApplication logic is encoded in a program that runs on blockchain  
• Rules are enforced by a public program (public source code)  
➔ transparency: no single trusted 3rd party  
• The APP program is executed by parties who create new blocks  
➔ public verifiability: anyone can verify state transitionsConsensus Layer

Iroha

Sumeragi

A public data structure (ledger) that provides:

- Persistence: once added, data can never be removed
- Consensus: all honest participants have the same data
- Liveness: honest participants can add new transactions
- Open(?): anyone can be a participant (no authentication)

![](attachments/21012408/21016609.png?height=250)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
cloud "User Interface" {
  [Mobile Application]
  [Web Application]
  [Command Line Interface]
}


database "Compute Layer" {
  [Iroha]

  node "Applications" {
    [Iroha Substrate]
  }

  folder "Consensus" {
    [Sumeragi]
  }
}


[Mobile Application] --> [Iroha]
[Web Application] --> [Iroha]
[Command Line Interface] --> [Iroha]
@enduml
```

## Application Programming Interface

FunctionalityProviderDescriptionSubmission of Iroha Special InstructionsClients

Clients receive declaration of desired actions from users in form of Iroha Special Instructions.

They build a Transaction from them, use User's cryptographics keys to Sign it (optionally?) and send them to Iroha.

Sending of Iroha QueriesClients

Clients receive declaration of desired search results from users in form of Iroha Queries.

They build a Request from them, use User's cryptographics keys to Sign it (optionally) and send them to Iroha.

Execution of Iroha Special InstructionsIroha

Iroha receives Transactions from Clients and process them in cooperation with Applications and Consensus.

More on that in [Process View Section](https://lf-hyperledger.atlassian.net/wiki/pages/resumedraft.action?draftId=21012408#Architecture-ProcessView).

Execution of Iroha QuerisIrohaIroha receives Queries from Clients and execute them. More on that in [Process View Section](https://lf-hyperledger.atlassian.net/wiki/pages/resumedraft.action?draftId=21012408#Architecture-ProcessView).

# Process View

This section describes the activities of the system, captures the concurrency and synchronization aspects of the design.

## Clients ↔ Peers Communications

Let's start with Iroha Peers - as described in [WhitePaper](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#21-p2p-network), Iroha as a system is build on top of a Peer to Peer Network.

So by Peer we will assume every Iroha instance  up and running.

![](http://www.plantuml.com/plantuml/png/TSin3eCm34RXFQVmrZ9m0OQAbR52FO19Z1efYP7pU-ZjYwgkh4_lcplOuBM4MvATlI103uBIfe1MIjaa8ciBqwkBqT8WjdEKYSRnGVVLjvf1Y-cRQJqaPYxdr67-OyELavR-wkbYdo7CP_5QlW00)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
'default
top to bottom direction
:User Interface: --> (Submit Iroha Special Instruction)
:User Interface: --> (Send Iroha Query)
@enduml
```

So basically we have two main interaction scenarios:

### Submission of Iroha Special Instructions

Every User Interface will use \`iroha-client\` under the hood, so we will look at the sequence with it:

![PlantUML diagram](http://www.plantuml.com/plantuml/png/VP31JiCm38RlUGfhftBW1Nf0aoOEEy2416UKjUuMDNMAxOZN9yagraY5I-Nw__xuj_UYbZLEtjXE0yFkGv1tO0LYAioSHDUvsPB2xiZXQk7W7Q4MfFCEIRUWLzJlm6EXw5PlO4LskQh5TxOaAOyB9F0MCM8Xlt9bJ0u6Zq_Bz1OadYUdpP54EHRJ0vYRkCREqVd-K-zFLuuDWxWBDQieQsRPAK58VGqjKgRAQYqmfkIYflok-hRhSDRQRRs2n2I83D53PmKDmA-pdA25ESgrzYrCbOrHva22pMdCmD9VhtWQK_--LRvi2uT0W-F9veSDUa6GC26CZde80mpM-SZu_yHdvi1_32tQnjpIXnSKiHSqIBtPfq-S_0y0)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
actor "User" as user
participant "Iroha Clinet" as client
participant "Iroha Network" as network
participant "Iroha" as iroha
participant "Transactions Queue" as queue

user -> client: submit(Instruction) 
client -> client: build_transaction(Instruction)
client -> client: sign(Transaction)
client -> network: send(Transaction)
network -> iroha: request
iroha -> iroha: accept(Transaction)
alt successful case
  iroha -> queue: push(Transaction)
  iroha -> network: response(Ok)
  network -> client: Ok
  client -> user: Confirmation
else some kind of failure
  iroha -> network: response(Error)
  network -> client: Error
  client -> user: Error Message
end
@enduml
```

### Sending Iroha Queries

![PlantUML diagram](http://www.plantuml.com/plantuml/png/VO-nJiCm48PtFyMfKplm0XrG9SJ000WGC5lEtsBLjSFTcSBRupW9959WYIx_zzdtUoTgMVCf6EiqCQsU1RmYAvJBODe2lVEjZKgh6qvlbgw2Zz2gkE0HTKcwWvuJ7wiL-tb1gzXtqno-9WuDFQbLq8l7kNeVPJ2cQqKNbyFgBJ7UCqJN3ndyjI7JvrD3_24EU4A7KWKZDYCUmexNLZ_Nc_fRyjfYI_Y4ouhnd0rAafs3o3u7SbPWgAgJgwhx2Cb13VNXh0X3sXG5w_lZUk9kDeP6QVgikTL9lu_B0jxIi0j1G99EeAEF3QKzxQqFcV5_Yslcn7_ihcnXOytf5YBs08FOc5tvv5Fu1W00)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
actor "User" as user
participant "Iroha Clinet" as client
participant "Iroha Network" as network
participant "Iroha" as iroha
participant "World State View" as view

user -> client: request(Query) 
client -> client: sign(Query)
client -> network: send(Query)
network -> iroha: request
iroha -> view: execute(Query)
alt successful case
  view -> iroha: QueryResult
  iroha -> network: response(Ok(QueryResult))
  network -> client: Ok(QueryResult)
  client -> user: Result
else some kind of failure
  iroha -> network: response(Error)
  network -> client: Error
  client -> user: Error Message
end
@enduml
```

## Peer ↔ Peer Communications

In this section we will look at Peer to Peer communications in different aspects:

### Iroha Qeuries Processing

Let's start from the quite simple Iroha Queries Processing.

![PlantUML diagram](http://www.plantuml.com/plantuml/png/JSunJeP04CNnVa_nIhW256AY1r0JhJVmO3SkEsHcLiFjHQgl-x_ycZUPH_Msbt1769Gpym_nrgZd6FAAxhbv4ir-8aK3gxGjuQ3ksInBjQSUdbZHdRG-04EH-HjVecN1XqSdFZD_nt_PeYSgNgB7UokzQSKxhHKV0uiHNPN-mLvLHI-gIrw3kHnXklfw_0S0)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
start
:receive Query;
if (Authority has enough permissions?) then (yes)
  :lock World State View;
  :gather Data;
  :return Result;
else (no)
  :return Error;
endif
stop
@enduml
```

### Iroha Transactions Processing

In this section we will cover only Transactions related part of the whole End to End process of Iroha Special Instructions execution.

Let's start from sequence:

![PlantUML diagram](http://www.plantuml.com/plantuml/png/VOwzJWCn48HxFyKeLLBm0YbG6WeQ418li7Bs5EjyjjaVyVhuVf3kA6ZiiMU-dRsfaPXFERH-fvWQ5SFfLUg3yCRsNMKyWHHbrSVOPvMK5jjczSSKAahHKYsA3sVd9Vargn2sUNXwNjahXBkb5fRdxfzYv6RdtRXBe6nGxuRgu1cHb0FmIwuTLpJNnu7RPxO5vbvjjIYVtyTBuAmChHDZJEMEEc2Wb5tuV_H5f4gdoptS-k5J_W40)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
participant "Iroha Network" as network
participant "Torii" as torii
participant "Transactions Queue" as queue

network -> torii: request
torii -> torii: accept(Transaction)
alt successful case
  torii -> queue: push(Transaction)
  torii -> network: response(Ok)
else some kind of failure
  torii -> network: response(Error)
end
@enduml
```

You already see this as a part of Submission of Iroha Special Instructions. Now we introduce Torii - which is Iroha Entity responsible for Network requests and Connections handling.

Queue is like a portal between Torii and another and the most important part of Iroha - Consensus.

### Blocks Processing

Consensus works with group of Transactions called Blocks. The whole set of actions that it does with them too big so let's describe each item one by one.

#### Validation

We will briefly discuss roles that Peer can have, for more information read the [White Paper](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#21-p2p-network).

In this case we will mainly consider Peer in a \`Leader\` role. We also will use \`Sumeragi\` as the only supported by the moment implementation of Consensus in Iroha.

![PlantUML diagram](http://www.plantuml.com/plantuml/png/NO-nRWCX44HxlcBAkr-m6ojr2aUHd9gOiOt2iHQxEChV1t1EEgL1myuRc3se-M9rIMu8jojISzYxUC7qLbc9crTOyLdzsQ9acE0XnXbsOyRqGvqTqFaZMGRU7BpIXtOjalwZmEwpnXHmP0unNr-IdB_sJwDBV4Xfxhjv8qwHtt_UmwSOscoJMsFQ9ZY9hQzXeQg_KdlRErcqWqnAJ5dcJMYpsO1xzJIgZqJxwEAUfvhStQ7fkgHV)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
start
:round;
if (Queue has transaction to vote) then (yes)
  if (Peer has the Leader role) then (yes)
    :build PendingBlock;
    :lock World State View;
    :validate PendingBlok;
    :send VotingBlock messages to peers;
  else (no)
    :send transactions to the leader;
  endif
endif
stop
@enduml
```

As you can see, validation triggers next Consensus step.

#### Voting

The science behind Consensus (and Sumeragi) is fully described in the [White Paper](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#29-consensus).

We will look at the high level and simple case of voting here:

![PlantUML diagram](http://www.plantuml.com/plantuml/png/VOwzJiKm38NtF8LrftRW1HXG1Ij39H2xIKo9S98gJX2yFKu2ebtka1_xVCV7YnJCfGOskxxU-XrZWSiZeQCCAr6-00fmhy_CIoe-RfsH3ktjTsRMdBw-uHaz3wALnenfS7CtBBTmpyb-F6J2Gixqta7yHFPEbUb8pGQvW5HhIUIjCbWKCW3_vXRrE_d9Rv6Sgir3CTNj7KHxM6ecqJuClFd6RdyhfH2yffsGaN6T6E6sYzDh0sSbA3hJpg9N3Vm3)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
participant "Leader Peer" as leader
participant "Voting Peers" as peers
participant "Proxy Tail" as proxy

leader -> peers: BlockCreated
peers -> peers: validate(BlockCreated)
alt successful case
  peers -> proxy: BlockSigned
  alt enough signatures
    proxy -> leader: BlockCommited
    proxy -> peers: BlockCommited
    proxy -> proxy: commit(block)
  end
end
@enduml
```

As we can see - in simple cases we just sign valid Blocks by Voting Peers and then move to the next stage.

#### Commitment

This stage involves new Iroha entity - Kura in cooperation with already familiar to you World State View.

![PlantUML diagram](http://www.plantuml.com/plantuml/png/LOszQiKm38LtFuN8b0nzWGmbD6F7G3eBHoqc_WcMrFlwr_755xpO1xxl72qic4M3DrVvdNKNHe5XJP4fiZACcmRA-EUc0P31Dj3xtvgnyhE47csIIfqgvLVkXP-K_G6Re13iZXxL_2_1cFSr-FYiqpFO58AJSKVlZY-Vx3cP6nIXhSyrKAUW5s2rbfX_rOD59WFGYlUn6IwLSQthr6eK3xEKHuD_0W00)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
participant "Consensus (Sumeragi)" as consensus
participant "Kura" as kura
participant "Storage" as storage
participant "World State View" as view

consensus -> kura: commit(ValidBlock)
kura -> storage: store(ValidBlock)
alt successful case
  kura -> view: put(CommitedBlock)
end
@enduml
```

#### Synchronization

Some Peers may be "out of work" because of network or other issues. New Peers may be added. All of them need a mechanism to receive already committed blocks and stay in sync with Ledger.

More on details in the [White Paper](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#210-data-synchronization-and-retrieval) and [Block Synchronization](Block-Synchronization_21012390.html) RFC

![PlantUML diagram](http://www.plantuml.com/plantuml/png/LOx13i8W38RlF4MpqtRm1NOmYruzcEm923QE26LfIw8-lSXYP0VWf__Vhvr4BMkEmQpbzSwlbXIwKqZk8J2_o2sSoB-HEx02qXJs7LT4bffPlsfldXC9acI1ViuHsTxzKBFkPnZJek5mt30ZNAoYQDt7sA3j7xm0uLD14-Y2zRZCZAGWMd86Dah1_IUDHSRejMz8Wq6wcQbSEOOF)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
participant "Blocks Synchronizer" as synchronizer
participant "Peers" as peers
participant "Consensus (Sumeragi)" as consensus

synchronizer -> peers: LatestBlock
alt LatestBlock is next to the the current state
  peers -> consensus: commit(LatestBlock)
end
@enduml
```

# Development View

This section describes the static organization or structure of the software in its development of environment.

```
.
├── Cargo.lock
├── Cargo.toml
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── docker-compose-single.yml
├── docker-compose.yml
├── Dockerfile
├── Dockerfile.debug
├── iroha
├── iroha_2_whitepaper.md
├── iroha_client
├── iroha_client_cli
├── iroha_client_no_std
├── iroha_macro
├── iroha_network
├── iroha_substrate
├── LICENSE
├── MAINTAINERS.md
├── README.md
├── scripts
└── target

```

Iroha repository consist of one Iroha [cargo workspace](https://doc.rust-lang.org/book/ch14-03-cargo-workspaces.html).

This workspace compose different crates:

CrateTypeDescriptionirohabinMain Iroha Application for Peers instantiations.iroha\_networklibIroha Networking library for encapsulation of protocols.iroha\_macrolibLibrary with Iroha related macroses (attribute and derive).iroha\_clientlibLibrary with Clients Facing (for User Interfaces, Applications and Peers) API.iroha\_client\_clibinCommand Line Interface wrapper on top of iroha\_client.

# Physical View

This section describes the mapping of software onto hardware and reflects its distributed aspect.

![PlantUML diagram](http://www.plantuml.com/plantuml/png/ROqn3eCm34LtJc6nC-0JS80E35NtgB4g94Ega5JjxIiSedvHbaX-ByyUrkHYohCsTmtPKtiHvoNIA19RSYkfpTNUGfgMXzdUzCj0V-8PF5S_nl3-qDLDQlQvZKqvGLrNj_qH1bAQ_US6YaAoHuYmOZnLqN4H_ofxeJa2BW1M3BBuFEiN)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
cloud "Leader Peer" as leader
cloud "Voting Peer1" as voting1
cloud "Voting Peer2" as voting2
cloud "Proxy Tail" as proxy
leader -- voting1
leader -- voting2
leader -- proxy
voting1 -- leader
voting1 -- voting2
voting1 -- proxy
voting2 -- voting1
voting2 -- leader
voting2 -- proxy
proxy -- voting1
proxy -- voting2
proxy -- leader
@enduml
```

As you can see - Peers Deployment is Cloud Native. Peers deployment via \`docker-compose\` can be used as an example:

![](images/icons/grey_arrow_down.png)Docker Compose Deployment Configuration

```
version: "3.3"
services:
  iroha:
    build:
      context: ./
      dockerfile: Dockerfile.debug
    image: iroha:debug
    environment:
      TORII_URL: iroha:1337
      TORII_CONNECT_URL: iroha:8888
      IROHA_PUBLIC_KEY: '{"inner": [207, 157, 30, 3, 197, 179, 35, 16, 222, 95, 102, 27, 234, 80, 45, 44, 152, 242, 69, 245, 24, 125, 189, 215, 62, 200, 92, 14, 37, 234, 246, 64]}'
      IROHA_PRIVATE_KEY: '{"inner": [19, 158, 252, 4, 218, 222, 30, 200, 21, 72, 109, 226, 132, 255, 6, 22, 159, 135, 12, 116, 227, 47, 82, 250, 30, 89, 89, 208, 245, 232, 114, 42, 207, 157, 30, 3, 197, 179, 35, 16, 222, 95, 102, 27, 234, 80, 45, 44, 152, 242, 69, 245, 24, 125, 189, 215, 62, 200, 92, 14, 37, 234, 246, 64]}'
      IROHA_TRUSTED_PEERS: '[{"address":"iroha:1337", "public_key":{"inner": [207, 157, 30, 3, 197, 179, 35, 16, 222, 95, 102, 27, 234, 80, 45, 44, 152, 242, 69, 245, 24, 125, 189, 215, 62, 200, 92, 14, 37, 234, 246, 64]}}, {"address":"iroha2:1338", "public_key": {"inner": [78, 192, 204, 27, 87, 91, 61, 147, 44, 246, 136, 104, 210, 72, 163, 26, 201, 143, 210, 62, 56, 33, 48, 182, 101, 14, 108, 235, 51, 94, 127, 209]}}, {"address": "iroha3:1339", "public_key": {"inner": [106, 192, 132, 99, 17, 107, 23, 45, 151, 112, 32, 242, 143, 142, 111, 57, 20, 151, 83, 12, 215, 253, 103, 126, 111, 96, 101, 17, 93, 110, 164, 255]}}, {"address": "iroha4:1340", "public_key": {"inner": [201, 179, 39, 127, 156, 2, 24, 107, 36, 178, 31, 0, 78, 108, 75, 196, 210, 113, 6, 41, 57, 7, 84, 173, 197, 196, 35, 59, 0, 14, 179, 130]}}]'
    ports:
      - "1337:1337"
  iroha2:
    depends_on:
      - iroha
    image: iroha:debug
    environment:
      TORII_URL: iroha2:1338
      TORII_CONNECT_URL: iroha2:8889
      IROHA_PUBLIC_KEY: '{"inner": [78, 192, 204, 27, 87, 91, 61, 147, 44, 246, 136, 104, 210, 72, 163, 26, 201, 143, 210, 62, 56, 33, 48, 182, 101, 14, 108, 235, 51, 94, 127, 209]}'
      IROHA_PRIVATE_KEY: '{"inner": [78, 231, 15, 158, 16, 4, 82, 126, 21, 219, 201, 40, 84, 34, 60, 215, 58, 143, 155, 187, 20, 27, 115, 137, 161, 120, 250, 70, 194, 80, 66, 87, 78, 192, 204, 27, 87, 91, 61, 147, 44, 246, 136, 104, 210, 72, 163, 26, 201, 143, 210, 62, 56, 33, 48, 182, 101, 14, 108, 235, 51, 94, 127, 209]}'
      IROHA_TRUSTED_PEERS: '[{"address":"iroha:1337", "public_key": {"inner": [207, 157, 30, 3, 197, 179, 35, 16, 222, 95, 102, 27, 234, 80, 45, 44, 152, 242, 69, 245, 24, 125, 189, 215, 62, 200, 92, 14, 37, 234, 246, 64]}}, {"address":"iroha2:1338", "public_key": {"inner": [78, 192, 204, 27, 87, 91, 61, 147, 44, 246, 136, 104, 210, 72, 163, 26, 201, 143, 210, 62, 56, 33, 48, 182, 101, 14, 108, 235, 51, 94, 127, 209]}}, {"address": "iroha3:1339", "public_key": {"inner": [106, 192, 132, 99, 17, 107, 23, 45, 151, 112, 32, 242, 143, 142, 111, 57, 20, 151, 83, 12, 215, 253, 103, 126, 111, 96, 101, 17, 93, 110, 164, 255]}}, {"address": "iroha4:1340", "public_key": {"inner": [201, 179, 39, 127, 156, 2, 24, 107, 36, 178, 31, 0, 78, 108, 75, 196, 210, 113, 6, 41, 57, 7, 84, 173, 197, 196, 35, 59, 0, 14, 179, 130]}}]'
    ports:
      - "1338:1338"
  iroha3:
    depends_on:
      - iroha
    image: iroha:debug
    environment:
      TORII_URL: iroha3:1339
      TORII_CONNECT_URL: iroha3:8890
      IROHA_PUBLIC_KEY: '{"inner": [106, 192, 132, 99, 17, 107, 23, 45, 151, 112, 32, 242, 143, 142, 111, 57, 20, 151, 83, 12, 215, 253, 103, 126, 111, 96, 101, 17, 93, 110, 164, 255]}'
      IROHA_PRIVATE_KEY: '{"inner": [73, 50, 145, 119, 184, 60, 237, 18, 5, 49, 208, 121, 40, 85, 139, 221, 27, 141, 251, 233, 30, 178, 143, 245, 214, 123, 113, 166, 3, 6, 124, 247, 106, 192, 132, 99, 17, 107, 23, 45, 151, 112, 32, 242, 143, 142, 111, 57, 20, 151, 83, 12, 215, 253, 103, 126, 111, 96, 101, 17, 93, 110, 164, 255]}'
      IROHA_TRUSTED_PEERS: '[{"address":"iroha:1337", "public_key": {"inner": [207, 157, 30, 3, 197, 179, 35, 16, 222, 95, 102, 27, 234, 80, 45, 44, 152, 242, 69, 245, 24, 125, 189, 215, 62, 200, 92, 14, 37, 234, 246, 64]}}, {"address":"iroha2:1338", "public_key": {"inner": [78, 192, 204, 27, 87, 91, 61, 147, 44, 246, 136, 104, 210, 72, 163, 26, 201, 143, 210, 62, 56, 33, 48, 182, 101, 14, 108, 235, 51, 94, 127, 209]}}, {"address": "iroha3:1339", "public_key": {"inner": [106, 192, 132, 99, 17, 107, 23, 45, 151, 112, 32, 242, 143, 142, 111, 57, 20, 151, 83, 12, 215, 253, 103, 126, 111, 96, 101, 17, 93, 110, 164, 255]}}, {"address": "iroha4:1340", "public_key": {"inner": [201, 179, 39, 127, 156, 2, 24, 107, 36, 178, 31, 0, 78, 108, 75, 196, 210, 113, 6, 41, 57, 7, 84, 173, 197, 196, 35, 59, 0, 14, 179, 130]}}]'
    ports:
      - "1339:1339"
  iroha4:
    depends_on:
      - iroha
    image: iroha:debug
    environment:
      TORII_URL: iroha4:1340
      TORII_CONNECT_URL: iroha4:8891
      IROHA_PUBLIC_KEY: '{"inner": [201, 179, 39, 127, 156, 2, 24, 107, 36, 178, 31, 0, 78, 108, 75, 196, 210, 113, 6, 41, 57, 7, 84, 173, 197, 196, 35, 59, 0, 14, 179, 130]}'
      IROHA_PRIVATE_KEY: '{"inner": [59, 70, 4, 158, 228, 9, 171, 131, 41, 157, 247, 31, 156, 94, 85, 52, 197, 131, 155, 26, 112, 192, 166, 50, 82, 111, 159, 14, 95, 15, 70, 30, 201, 179, 39, 127, 156, 2, 24, 107, 36, 178, 31, 0, 78, 108, 75, 196, 210, 113, 6, 41, 57, 7, 84, 173, 197, 196, 35, 59, 0, 14, 179, 130]}'
      IROHA_TRUSTED_PEERS: '[{"address":"iroha:1337", "public_key": {"inner": [207, 157, 30, 3, 197, 179, 35, 16, 222, 95, 102, 27, 234, 80, 45, 44, 152, 242, 69, 245, 24, 125, 189, 215, 62, 200, 92, 14, 37, 234, 246, 64]}}, {"address":"iroha2:1338", "public_key": {"inner": [78, 192, 204, 27, 87, 91, 61, 147, 44, 246, 136, 104, 210, 72, 163, 26, 201, 143, 210, 62, 56, 33, 48, 182, 101, 14, 108, 235, 51, 94, 127, 209]}}, {"address": "iroha3:1339", "public_key": {"inner": [106, 192, 132, 99, 17, 107, 23, 45, 151, 112, 32, 242, 143, 142, 111, 57, 20, 151, 83, 12, 215, 253, 103, 126, 111, 96, 101, 17, 93, 110, 164, 255]}}, {"address": "iroha4:1340", "public_key": {"inner": [201, 179, 39, 127, 156, 2, 24, 107, 36, 178, 31, 0, 78, 108, 75, 196, 210, 113, 6, 41, 57, 7, 84, 173, 197, 196, 35, 59, 0, 14, 179, 130]}}]'
    ports:
      - "1340:1340"

```

# Scenarios

- 1 [Conceptual View](#Architecture-ConceptualView)
  
  - 1.1 [Components](#Architecture-Components)
  - 1.2 [Application Programming Interface](#Architecture-ApplicationProgrammingInterface)
- 2 [Process View](#Architecture-ProcessView)
  
  - 2.1 [Clients ↔ Peers Communications](#Architecture-Clients%E2%86%94PeersCommunications)
    
    - 2.1.1 [Submission of Iroha Special Instructions](#Architecture-SubmissionofIrohaSpecialInstructions)
    - 2.1.2 [Sending Iroha Queries](#Architecture-SendingIrohaQueries)
  - 2.2 [Peer ↔ Peer Communications](#Architecture-Peer%E2%86%94PeerCommunications)
    
    - 2.2.1 [Iroha Qeuries Processing](#Architecture-IrohaQeuriesProcessing)
    - 2.2.2 [Iroha Transactions Processing](#Architecture-IrohaTransactionsProcessing)
    - 2.2.3 [Blocks Processing](#Architecture-BlocksProcessing)
      
      - 2.2.3.1 [Validation](#Architecture-Validation)
      - 2.2.3.2 [Voting](#Architecture-Voting)
      - 2.2.3.3 [Commitment](#Architecture-Commitment)
      - 2.2.3.4 [Synchronization](#Architecture-Synchronization)
- 3 [Development View](#Architecture-DevelopmentView)
- 4 [Physical View](#Architecture-PhysicalView)
- 5 [Scenarios](#Architecture-Scenarios)

[Egor Ivkov](/wiki/display/~5dd9631c1cf3c20ef5ff9f0f) 4, [Nikita Puzankov](/wiki/display/~5df113768998970e5b434e0a) 4, [Vadim Reutskiy](/wiki/display/~5b8d04b72786fb2bf79a7405) 2

Version Date Comment **[Current Version](/wiki/display/iroha/viewpage.action?pageId=21012408) (v. 26)** **Aug 24, 2020 06:55** [**Vadim Reutskiy**](/wiki/people/5b8d04b72786fb2bf79a7405) [v. 25](/wiki/display/iroha/viewpage.action?pageId=21017096) Aug 24, 2020 06:53 [Vadim Reutskiy](/wiki/people/5b8d04b72786fb2bf79a7405) [v. 24](/wiki/display/iroha/viewpage.action?pageId=21017095) Aug 24, 2020 06:53 [Vadim Reutskiy](/wiki/people/5b8d04b72786fb2bf79a7405) [v. 23](/wiki/display/iroha/viewpage.action?pageId=21017094) Aug 24, 2020 06:52 [Vadim Reutskiy](/wiki/people/5b8d04b72786fb2bf79a7405) [v. 22](/wiki/display/iroha/viewpage.action?pageId=21017093) Aug 24, 2020 06:51 [Vadim Reutskiy](/wiki/people/5b8d04b72786fb2bf79a7405) [v. 21](/wiki/display/iroha/viewpage.action?pageId=21017092) Aug 24, 2020 06:44 [Vadim Reutskiy](/wiki/people/5b8d04b72786fb2bf79a7405) [v. 20](/wiki/display/iroha/viewpage.action?pageId=21017091) Aug 24, 2020 06:37 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 19](/wiki/display/iroha/viewpage.action?pageId=21017090) Aug 23, 2020 23:27 [Vadim Reutskiy](/wiki/people/5b8d04b72786fb2bf79a7405) [v. 18](/wiki/display/iroha/viewpage.action?pageId=21017080) Jul 13, 2020 04:19 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 17](/wiki/display/iroha/viewpage.action?pageId=21016650) Jul 09, 2020 03:11 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 16](/wiki/display/iroha/viewpage.action?pageId=21016623) Jul 09, 2020 03:10 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 15](/wiki/display/iroha/viewpage.action?pageId=21016622) Jul 09, 2020 02:42 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a)  
Project Structure [v. 14](/wiki/display/iroha/viewpage.action?pageId=21016621) Jul 09, 2020 02:33 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a)  
Blocks Synchronization [v. 13](/wiki/display/iroha/viewpage.action?pageId=21016620) Jul 09, 2020 02:20 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a)  
Transactions and Blocks processing [v. 12](/wiki/display/iroha/viewpage.action?pageId=21016619) Jul 09, 2020 01:22 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a)  
Iroha Query Processing [v. 11](/wiki/display/iroha/viewpage.action?pageId=21016618) Jul 09, 2020 01:13 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a)  
Sending Iroha Queries [v. 10](/wiki/display/iroha/viewpage.action?pageId=21016617) Jul 09, 2020 01:05 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a)  
Submission of Iroha Special Instructions [v. 9](/wiki/display/iroha/viewpage.action?pageId=21016616) Jul 09, 2020 00:25 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a)  
Plant UML source for components diagram added. [v. 8](/wiki/display/iroha/viewpage.action?pageId=21016615) Jul 09, 2020 00:12 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 7](/wiki/display/iroha/viewpage.action?pageId=21016614) Jul 09, 2020 00:10 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 6](/wiki/display/iroha/viewpage.action?pageId=21016613) Jul 09, 2020 00:06 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 5](/wiki/display/iroha/viewpage.action?pageId=21016612) Jul 08, 2020 23:45 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 4](/wiki/display/iroha/viewpage.action?pageId=21016611) Jul 08, 2020 23:31 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 3](/wiki/display/iroha/viewpage.action?pageId=21016610) Jul 08, 2020 23:31 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 2](/wiki/display/iroha/viewpage.action?pageId=21016608) Jul 08, 2020 23:30 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a) [v. 1](/wiki/display/iroha/viewpage.action?pageId=21016606) Jul 08, 2020 22:27 [Nikita Puzankov](/wiki/people/5df113768998970e5b434e0a)

## Attachments:

![](images/icons/bullet_blue.gif) [RO-\_Ii103CRtF4NetbUGYbEXJaKSf4Ekb-h1\_Icvt23YknkfMiLkntU\_\_99lg4gYBKLOOsaUkuVAWcDMberMxl0D49\_kYmkHyNRVOrX9GydBP\_p8xbzsLrAYx74AcK\_F0ky0u4d9KMNiZDgRCaxqolArP9JoGWlOCnTlp2zpFP1l2EVcgWgfUH7DZBYLw5bCR33dsiw9kIKMUWu7QZ1SrS6-l\_avuIns-NjTyIyqSFOjnGy0.svg](attachments/21012408/21016607.svg) (image/svg+xml)  
![](images/icons/bullet_blue.gif) [RO-\_Ii103CRtF4NetbUGYbEXJaKSf4Ekb-h1\_Icvt23YknkfMiLkntU\_\_99lg4gYBKLOOsaUkuVAWcDMberMxl0D49\_kYmkHyNRVOrX9GydBP\_p8xbzsLrAYx74AcK\_F0ky0u4d9KMNiZDgRCaxqolArP9JoGWlOCnTlp2zpFP1l2EVcgWgfUH7DZBYLw5bCR33dsiw9kIKMUWu7QZ1SrS6-l\_avuIns-NjTyIyqSFOjnGy0.png](attachments/21012408/21016609.png) (image/png)

Document generated by Confluence on Nov 26, 2024 15:05

[Atlassian](http://www.atlassian.com/)
