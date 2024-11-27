1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : DEX Generic Scenarios

Created by Nikita Puzankov, last modified on Aug 13, 2020

Status

DECIDED

Stakeholders

[Yuriy Vinogradov](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b85dbf9-2cc9-4bee-a3a0-2815e5bb51eb?ref=confluence) [武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) [Vladislav Markushin](https://lf-hyperledger.atlassian.net/wiki/people/5ecbc0c8eb77320c1f684409?ref=confluence) 

Outcome

Iroha 2 will provide all functionality needed to support these scenarios.

- [Iroha Special Instructions DSL](Iroha-Special-Instructions-DSL_21012073.html)
- [Cloud Events](Cloud-Events_21012424.html)

Due date

28 Jul 2020

Owner

[Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence) 

## Background

DEX is planned to be implemented as Iroha 2.0 module.

## Action items

- [Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence)write down scenarios
- [Yuriy Vinogradov](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b85dbf9-2cc9-4bee-a3a0-2815e5bb51eb?ref=confluence) validate scenarios
- [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) [Vladislav Markushin](https://lf-hyperledger.atlassian.net/wiki/people/5ecbc0c8eb77320c1f684409?ref=confluence) provide implementation options
- [武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) review solution

## Problem

Decentralized exchange provides an ability to transfer assets between accounts in exchange for other assets. Let's use a simple case as an example:

### Peer to Peer Scenario

![PlantUML diagram](http://www.plantuml.com/plantuml/png/XOyn2y9038Nt_8etMgXG7Jj84HsSAbR1DLnJErnRo5r1_xtbuk0YBbdolYzvLOYiSHuyxUUNADOxd7JgkSJPinCSdwxdyI6ejHLTROjxVScnAOfRSyYe4U__GvREaU2CKlIBkIgFeHErFJgT1dp4SK9wYzX7DBDp4a99m4-5dJB7Gfh2P2HZIzKobh9l)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
Buyer -> Iroha: Place Exchange Order(20XOR, 100USD)
Seller -> Iroha: Place Exchange Order(100USD, 20XOR)
Iroha -> Iroha: Transfer 20XOR from Seller to Buyer
alt Success:
  Iroha -> Iroha: Transfer 100USD from Buyer to Seller
end
@enduml
```

So Iroha should secure peer to peer exchanges across the ledger from malicious actions. In this case Iroha does a good job, the only thing it should check is an ability to transfer assets from and to accounts.

But there are more corner cases when we deal with exchanges via bridge:

### Peer to Peer across Bridge Scenario

- Cross blockchain rates should be taken into consideration
- Iroha should prevent double spent of assets
- Additionally to transferring assets, Iroha should mint and de-mint them

Simple scenario:

![PlantUML diagram](http://www.plantuml.com/plantuml/png/XP3B2i8m44Nt-OgXAmiLr6KNKYe5NOX2-mCndJuWJM6IWlwzURW8HNJHMPGvvzv9eGqdiqoIbSiB2RP7kD0yy1pkaWk4wYa6hdg46xL8cyEkQiuPxClcbB8QfVoFkDqCF9Wol-Y8nFw51urjZqaErr4PBmKpGz0oBWtKYn2eTSuWH4HP3N6bEwI0TJHF7z0f_2qMMZaYIsBhhF9znPZ-ml_e4N1N90YYKno7gcLXkg-mmpxw6m00)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
Buyer -> Iroha: Place Exchange Order(20ETH, 1BTC)
Seller -> Iroha: Place Exchange Order(1BTC, 20ETH)
Iroha -> "BTC bridge": Mint 1BTC to Seller
alt Success:
  Iroha -> Iroha: Transfer 1BTC from Seller to Buyer
  alt Success:
    Iroha -> "ETH bridge": Mint 20ETH to Buyer
    alt Success:
      Iroha -> Iroha: Transfer 20ETH from Buyer to Seller
    end
  end
end
@enduml
```

### Liquidity Pool Scenario

[Liquidity Pools](https://defiprime.com/uniswap-liquidity-pools) is another dimension in this set of scenarios for Decentralized Exchanges. Basically it can be used in pair with or without bridges, so let's take a more *clean* example without them. But let's not stick to an Exchange Pair and work with multi-currency liquidity:

![PlantUML diagram](http://www.plantuml.com/plantuml/png/TP11ImCn48Nl-HMFd1Ggr1xt84KfA2WjxHu4yH2JwJQGJN2I5VttRZOB0LaFoI6yxykRsSQaE0sz4_BPVWxMsFI30uSlQuWbRkxmnE6Y6Xofip4HO_UjByftX9f_swnVzySLDkjT-xZ2xNtxy2vEv1mngk7WbAQAxzaGN-Ni35wBAPW9ERxYWwtfI3PuiJvDKgI0eXNA9Pm6hId6HW25h7-rh7my4nVipA6VmQnOcbG0VvJ_IqlTObroeTO4o1kHptQynZN_0W00)

![](images/icons/grey_arrow_down.png)Plant UML

```
@startuml
"Liquidity Provider" -> Iroha: Register Exchange Liquidity [20XOR, 20ETH, 1BTC]
Seller -> Iroha: Place Exchange Order(1BTC, 20ETH)
Iroha -> "BTC bridge": Mint 1BTC to Seller
alt Success:
  Iroha -> Iroha: Transfer 1BTC from Seller to "Liquidity Provider"
  alt Success:
    Iroha -> Iroha: Transfer 20ETH from "Liquidity Provider" to Seller
  end
end
@enduml
```

From the high level perspective this scenario looks very similar with two previous because all of them are based on top of two Iroha functions:

- Assets Transfer
- Iroha Triggers

### Resulting Behavior

Let's write all three scenarios as one feature description according to BDD with more details:

![](images/icons/grey_arrow_down.png)Click here to expand...

```
Feature: Decentralized Exchange

  Scenario: Buyer exchanges 20xor for 100usd
    Given Iroha Peer is up
    And Iroha DEX module enabled
    And Peer has Domain with name exchange
    And Peer has Account with name buyer and domain exchange
    And Peer has Account with name seller and domain exchange
    And Peer has Asset Definition with name xor and domain exchange
    And Peer has Asset Definition with name usd and domain exchange
    And buyer Account in domain exchange has 100 amount of Asset with definition usd in domain exchange
    And seller Account in domain exchange has 20 amount of Asset with definition xor in domain exchange
    When buyer Account places Exchange Order 20xor for 100usd
    And seller Account places Exchange Order 100usd for 20 xor
    Then Iroha transfer 20 amount of Asset with definition xor in domain exchange from seller account in domain exchange to buyer account in domain exchange
    And Iroha transfer 100 amount of Asset with definition usd in domain exchange from account buyer in domain exchange to seller account in domain exchange

  Scenario: Buyer exchanges 1btc for 20eth across bridges
    Given Iroha Peer is up
    And Iroha Bridge module enabled
    And Iroha DEX module enabled
    And Peer has Domain with name exchange
    And Peer has Account with name buyer and domain exchange
    And Peer has Account with name seller and domain exchange
    And Peer has Asset Definition with name btc and domain exchange
    And Peer has Asset Definition with name eth and domain exchange
    And Peer has Bridge with name btc and owner btc_owner
    And Peer has Bridge with name eth and owner eth_owner
    And eth Brdige has buyer Account in domain exchange registered
    And btc Brdige has seller Account in domain exchange registered
    When buyer Account places Exchange Order 20xor for 100usd
    And seller Account places Exchange Order 100usd for 20 xor
    Then Iroha mint 1 amount of Asset with definition btc in domain exchange to seller Account in domain exchange using btc Bridge
    And Iroha mint 20 amount of Asset with definition eth in domain exchange to buyer Account in domain exchange using eth Bridge
    And Iroha transfer 1 amount of Asset with definition btc in domain exchange from seller account in domain exchange to buyer account in domain exchange
    And Iroha transfer 20 amount of Asset with definition eth in domain exchange from buyer account in domain exchange to seller account in domain exchange

  Scenario: Buyer exchanges 20xor for 100usd
    Given Iroha Peer is up
    And Iroha DEX module enabled
    And Peer has Domain with name exchange
    And Peer has Account with name liquidity_provider and domain exchange
    And Peer has Account with name seller and domain exchange
    And Peer has Asset Definition with name xor and domain exchange
    And Peer has Asset Definition with name btc and domain exchange
    And Peer has Asset Definition with name eth and domain exchange
    And liquidity_provider Account in domain exchange has 1 amount of Asset with definition btc in domain exchange
    And liquidity_provider Account in domain exchange has 20 amount of Asset with definition eth in domain exchange
    And liquidity_provider Account in domain exchange has 20 amount of Asset with definition xor in domain exchange
    And seller Account in domain exchange has 20 amount of Asset with definition eth in domain exchange
    When liquidity_provider Account registers Exchange Liquidity 20xor and 20eth and 1btc
    And seller Account places Exchange Order 20eth for 1btc
    Then Iroha transfer 1 amount of Asset with definition btc in domain exchange from seller account in domain exchange to liquidity_provider account in domain exchange
    And Iroha transfer 20 amount of Asset with definition eth in domain exchange from liquidity_provider account in domain exchange to seller account in domain exchange
```

## Solution

DEX realated entities could be represented via Iroha model (Domains, Assets and their definitions), while complex sequences of actions could be implemented via Iroha Special Instructions + Triggers.

### Decisions

- Introduce a new module "DEX" with a dependency on "Bridge" module with additional set of Iroha Special Instructions and Queries and new Abstractions like Order (Combination of a Trigger and Asset with a predefined Asset Definition)
- Implement [Use cases](Use-cases_21016413.html)
- Implement [Iroha Special Instructions DSL](Iroha-Special-Instructions-DSL_21012073.html)

### Alternatives

- Provide out-of-the-box entities and instructions for DEX - breaks modular approach giving to much information about private API to DEX module and making it mandatory for all peers once it introduced to the ledger
- Make World State View public API - removes possibility to improve internal processes without breaking back compatibility

### Concerns

- Users without deep knowledge of Iroha model and instructions may fail to implement this

### Assumptions

- Iroha modules need to be optional Iroha features
- Iroha Special Instructions DSL is separated from execution implementations

### Risks

- Given functionality will not cover all corner cases \`\[3;8]\`
- Performance may be insufficient for DEX \`\[2;9]\`

## Additional Information

[![](attachments/thumbnails/21012490/21016867)](attachments/21012490/21016867.pdf)

## Attachments:

![](images/icons/bullet_blue.gif) [image2020-7-22\_18-42-52.png](attachments/21012490/21016735.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2020-7-28\_20-12-2.png](attachments/21012490/21016813.png) (image/png)  
![](images/icons/bullet_blue.gif) [DEX.pdf](attachments/21012490/21016867.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 15:05

[Atlassian](http://www.atlassian.com/)
