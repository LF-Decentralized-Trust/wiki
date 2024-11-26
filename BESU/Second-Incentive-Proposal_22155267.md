1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Programs &amp; Grants](22155199.html)
4. [Besu Execution Client Incentive Program](Besu-Execution-Client-Incentive-Program_22155201.html)

# Besu : Second Incentive Proposal

Created by Danno Ferrin, last modified on Jan 16, 2022

# Overview

The proceeds of the validators will be split into three pools: 20% to the node operator, 20% to Hyperledger Foundation as a directed donation, and 60% to a patronage pool. The employers (or who the employer directs) of the maintainers receive a share of that pool in proportion to the amount of maintainers and their level of time working on Besu for mainnet functionality.

# Endowment Model

Hyperledger or a legal entity established by Hyperledger for the sole purpose of this program (the entity) will have ownership of the vested validators and proceeds from validation and block rewards, to the extent that any entity can or should have ownership. The tokens will be held and used as the stake for the validators that are intended to be run as part of this program.  Distributions will consist of validator balances above the initial rate of 32 eth per node (i.e. validators that were slashed will need to regain balance above 32 eth) as well as any block rewards from block production(also known as the "coinbase").  The entity will hold the ether between distributions and will distribute funds based on the appropriate pool amounts to the appropriate recipients.

## Operator Pool

20% of proceeds will go to the service provider operating the validator nodes. The service operator will custody the keys only to the extent needed to operator the validators and any custody shall not be considered any claim to ownership.

The node operator will provide access to the canary nodes to Hyperledger mainnet developers for development and debugging purposes.  Access to performance nodes may be restricted to node operations. 

The service provider can be changed by consent of Hyperledger and the approval of 80% of the Hyperleder Besu mainnet maintainers.

The initial service provider will be ConsenSys or a fully owned subsidiary of ConsenSys.

## Hyperledger Pool

Hyperledger will receive or direct 20% of the proceeds. This pool will be a directed donation towards Hyperledger Besu mainnet work paying for items including but not limited to

- Administration, accounting, operations, and legal costs of the entity
- Costs relating to distribution of tokens by the entity
- Payment of services consumed by the Hyperledger Besu project, such as
  
  - Continuous Integration,
  - Cloud Hosting fees for development (i.e. testnet nodes)
  - source code hosting,
  - any other such services directly related to development of mainnet capabilities in Hyperledger Besu
- Sending maintainers to speak at and promote Hyperledger Besu at Hyperledger events (such as the Global Forum and Members Summit) and Ethereum Foundation events (such as DevCon and AllCoreDevs meetings)
- Posting Bounties for work on Hyperledger Besu mainnet or mainnet related work
- Spending that would directly promote interoperability with Besu Mainnet functionality and other Hyperledger projects
- Other spending that would directly promote and improve Hyperledger Besu

## Patronage Pool

60% will go to employers  of maintainers (or where the employer designates) allocating at least 25% of their work effort towards ethereum mainnet development. Each quarter time work is 1 share (hence a full time maintainer is 4 shares), with no fractional shares considered, and each employer get a portion proportional to their share per allocation period.

Allocations will adjust when the merge activates and when each block of validators starts to vest (i.e. 6 months).

Each maintainers first block is "probationary" and will have their share delivered at the end of the period, while other maintainers shares will accrue as fast as the entity choses to disbursed earned shares.

Each new allocation period must be consented to by Hyperledger and approved by two thirds of the maintainers who qualified in the previous or proposed allocation round and maintainers from at least two employers (unless all qualified maintainers are from one employer). In the event of a deadlock the Ethereum Foundation may arbitrate allocations, but this is considered a failure and multiple occurrences may be grounds by EF to terminate the program.

### Ethereum Mainnet Development

Ethereum mainnet development works includes (without limitation) contributions to features, performance, and stability required for Mainnet operation of the Besu client. This work includes supporting work necessarily deriving from this effort, such as build maintenance, code cleanup, documentation, test maintenance and development, etc. This includes work on EIPs and proposals in all core devs intended for mainnet deployment up until such a time as they are known to be excluded from mainnet deployment. (for example BLS-12 work still qualifies but alternative proof of work algorithms no longer count although they once did).

Excluded is work relating to Ethereum Classic development, Quorum compatibility, private transactions, private transaction enclaves, permissioning, etc. and supporting work deriving exclusively from these activities.

(i.e. a maintainer working half time on mainnet and half time on ethereum classic will only could as half time total).

## Liquidation

Liquidation will terminate the entity as well as Hyperleder Besu's participation in the incentive program.

Liquidation will occur in one of four situations

- 6 months after the last validator is fully vested.
- The Ethereum Foundation terminates Besu's participation
- With the consent of the Hyperledger Foundation and approval of two thirds of the Hyperledger Besu maintainers
- With approval of all of the Hyperledger Besu maintainers

Each share allocated as part of each patronage pool cycle is also a share to the stake pool in the event of liquidation (i.e. a full time maintainer working across three cycles has 12 shares), and will be directed in the same way patronage shares are directed.

All stake and remaining validation and block rewards will be distributed based on the proportion of shares.

Document generated by Confluence on Nov 26, 2024 12:59

[Atlassian](http://www.atlassian.com/)
