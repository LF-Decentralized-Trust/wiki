1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Programs &amp; Grants](22155199.html)
4. [Besu Execution Client Incentive Program](Besu-Execution-Client-Incentive-Program_22155201.html)

# Besu : Proposal #3.5

Created by Danno Ferrin on Jan 27, 2022

- [Guiding Principles](#Proposal%233.5-GuidingPrinciples)
- [Processes](#Proposal%233.5-Processes)
  
  - [Operator:](#Proposal%233.5-Operator:)
  - [Key Management](#Proposal%233.5-KeyManagement)
- [Transaction Fees &amp; Validator Rewards Funds Distribution](#Proposal%233.5-TransactionFees&ValidatorRewardsFundsDistribution)
  
  - [Operator Pool](#Proposal%233.5-OperatorPool)
  - [Hyperledger Pool](#Proposal%233.5-HyperledgerPool)
  - [Patronage Pool](#Proposal%233.5-PatronagePool)
  - [Ethereum Mainnet Development](#Proposal%233.5-EthereumMainnetDevelopment)
- [Distribution of Withdrawal Keys](#Proposal%233.5-DistributionofWithdrawalKeys)
  
  - [Proportional Distribution of Keys](#Proposal%233.5-ProportionalDistributionofKeys)
  - [Liquidation and Impact to Patronage Pool](#Proposal%233.5-LiquidationandImpacttoPatronagePool)
- [Exhibit A](#Proposal%233.5-ExhibitA)

## **Guiding Principles**

1. Per the Program’s [Terms](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Besu+Execution+Client+Incentive+Program), the Ethereum Foundation (EF) has the right to change and/or update the program at any point. That is, the EF acts as a check and balance that patrons and the Hyperledger Foundation (HLF) continue to meet the requirements of the program.
2. This program offers client teams ETH-denominated rewards which unlock over time, as long as they continue to build software which meets the performance and security requirements of mainnet. There are two types of rewards that will be granted:
3. 1. Transaction and Validator Fees
   2. Withdrawal Key Funds
4. The Ethereum Foundation will only provide future organizations (refered to as patrons in this document) who have demonstrated long term support for Besu's mainnet work, organizations that employ maintainers with a history of mainnet contribution, or organizations with significant recent contributions, access to the principal capital of the program. To date, these organizations are ConsenSys, Swirlds Labs (fka Hedera) and the Hyperledger Foundation. If future organizations want to be considered, the EF and HLF can agree to add them to the program.
5. Wit regard to any tokens or funds that are directed to patrons, the patron will has sole discretion on how to spend those funds, assuming it is meeting the EF’s expectations of funds’ usage.

## **Processes**

### Operator:

ConsenSys will be the operator running the validator nodes in the near/medium term. The EF and HLF can make a decision on whether to change that structure at any point and invite a new party to also run the validator nodes. There will be 144 validator nodes included in this Program. 

### Key Management

There are three types of keys that are being managed in this process: Withdrawal Keys, Block Signing Keys and Transaction Fee Keys.

**Withdrawal Keys**

The Ethereum Foundation holds the withdrawal keys. The EF sends the withdrawal keys based on the proportions outlined in the “Distribution of Withdrawal Keys” section. The withdrawal keys have control over the validators’ principal and rewards upon withdrawal.

**Block Signing Keys**

These keys are used by the validator to attest to blocks. The node operator holds the block signing keys.

**Transaction Fee Keys**

This key has control over the address where transaction fees are sent. This a regular Eth1 address. Unlike the other two keys, the Transaction Fee Keys can be updated easily.

## **Transaction Fees &amp; Validator Rewards Funds Distribution**

The proceeds of the validators (i.e. transaction fees and rewards) will be split into three pools: 20% to the node operator, 20% to HLF as a directed donation, and 60% to a patronage pool.  These funds will be distributed following the processes outlined above.

At the start of every vesting period, the transaction fees will be set up to be proportionally distributed based on prior 6 month’s contributions of maintainers. The node operator will set up coinbase and reward address for the validators based how the transaction fee keys are set up for that vesting period. This design is to get the transaction fees received to limit the tax exposure to all patrons. However, at the end of each vesting period, we can expect there will be a slight variation on the fees received, and the fees that were “over” sent to one party, will then be sent to the other parties.

For example, at the beginning of a vesting period it is determined that one patron receives 70% of fees, another receives 10%  of fees, and a third receives 20%. If at the end of that vesting period, the distribution is 80% with the first company, 5% with the second company, and 15% to the third, the first company will send one transaction to the second company's address with the 5% of funds it owes to match the patronage pool allocation and the third patron a similar 5% transaction.

*Exhibit A also demonstrated the breakdown for funds.*

### Operator Pool

20% of transaction fees and validator will go to the service provider operating the validator nodes, to be used at their sole discretion and without limitation. No other compensation wll be provided for the node operation service.

The node operator will provide access to the canary nodes to Hyperledger mainnet developers and all maintainers performing mainnet work for development and debugging purposes.  Access to performance nodes may be restricted to node operations, at the node operator's discretion. There is an expectation that if a contributor receives access to any nodes, they will then be added to the respective monitoring channels for those nodes.

The service provider can be changed by the Ethereum Foundation at their discretion and without any required warning.

The initial service provider will be ConsenSys or a fully owned subsidiary of ConsenSys.

### Hyperledger Pool

Hyperledger will receive or direct 20% of transaction fees and validator rewards, independent of any maintainer participation. This pool will be a directed donation towards Hyperledger Besu mainnet work paying for items including but not limited to:

- Payment of services consumed by the Hyperledger Besu project, such as
- - Continuous Integration,
  - Cloud Hosting fees for development (i.e. testnet nodes)
  - source code hosting,
  - any other such services directly related to development of mainnet capabilities in Hyperledger Besu
- *Note: These costs are separate from any incurred by any other participating organization.*
- Sending maintainers to speak at and promote Hyperledger Besu at Hyperledger events (such as the Global Forum and Members Summit) and Ethereum Foundation events (such as DevCon and AllCoreDevs meetings)
- Posting Bounties for work on Hyperledger Besu mainnet or mainnet related work
- Spending that would directly promote interoperability with Besu Mainnet functionality
- Other spending that would directly promote and improve Hyperledger Besu

### Patronage Pool

The remaining 60% will go to patrons (or where the patron designates) proportional to the number of qualifying maintainers they employ (or to HLF for maintainers without patrons). Maintainers contributing to mainnet functionality is the only metric used to determine distribution from the Patronage Pool. The Besu community will manage a list of maintainers with substantial contributions to mainnet in a vesting period. If there is a dispute around a maintainer’s contribution to mainnet, that will be escalated to the EF and HLF staff to decide on whether they meet eligibility.

Hyperledger Besu community will use the current process for maintainership to determine who becomes maintainers. Future participation in the patronage pool shall not be a basis for denying maintainership.

### **Ethereum Mainnet Development**

Ethereum Mainnet development works includes (without limitation) contributions to features, performance, and stability required for Ethereum Mainnet operation of the Besu client. This work includes supporting work necessarily deriving from this effort, such as build maintenance, code cleanup, documentation, test maintenance and development, etc. This includes work on EIPs and proposals in all core devs intended for Ethereum Mainnet deployment up until such a time as they are known to be excluded from Ethereum Mainnet deployment. (for example BLS-12 work still qualifies but alternative proof of work algorithms no longer count although they once did).

Excluded is work relating to Ethereum Classic development, GoQuorum compatibility, private transactions, private transaction enclaves, permissioning, etc., and supporting work deriving exclusively from these activities.

## **Distribution of Withdrawal Keys**

### Proportional Distribution of Keys

The Ethereum Foundation will only provide organizations who have demonstrated long term support for Besu's mainnet work, organizations that employ maintainers with a history of mainnet contribution, or organizations with significant recent contributions, access to the principal capital of the program. To date, these patrons are Hyperledger Foundation, ConsenSys (for organizational history) and Swirlds Labs (for employment of a prominent maintainer). 

The HLF funds received via the withdrawal keys will go directly to HLF. It will not be passed along to any other participating organization.

Maintainers who qualify to be counted in the patronage pool, but whose employer is not a patron, will be accounted to HLF or an organization directed by HLF (with EF consent).

Withdrawal keys will be sent proportionally to these patrons based on mainnet maintainers to Besu over the entirety of the incentive program by the Ethereum Foundation. The keys give each organization ownership over the principal (because you then have custody of the funds upon withdrawal). The EF only considers the funds “sent” to the patrons when the EF sends the withdrawal key. The EF will send the contributions to patrons or HLF based on the number of maintainers but will be accounted for on the rolling period as demonstrated in Exhibit A.

Validator rewards beyond the principal will be allocated similarly to the Transaction Fees in which there might have to be a transfer between participating patrons to account for the different contributions. One important difference between the Transaction Fees/Validator Rewards and Withdrawal credential allocation is that the share of the former will be based on each vesting period, while the allocation of the latter is based on the **number of mainnet maintainers** **over the entire program.**

The EF will make a best effort to distribute withdrawal keys based on the current vesting period allocation, and will take into account all previous over and under allocations when distributing keys.

### Liquidation and Impact to Patronage Pool

The EF releases the withdrawal credentials in the period (as identified in the contract under “[Milestones](https://lf-hyperledger.atlassian.net/wiki/display/BESU/Besu+Execution+Client+Incentive+Program)”) in the proportional manner identified above. Once withdrawals are received by a patron, that patron can choose to liquidate. 

No patron will have any influence on any other patron's choice to liquidate, regardless of maintainership participation.

If a patron chooses to liquidate based on the withdrawal (as proportional to the amount of maintainers credited over the duration of the program) that patron will reduce their share of the remaining program’s patronage pool participation. For example, if an organization liquidates 10% of their validators, that organization's share of the patronage pool (both validator rewards &amp; transaction fee as well as withdrawal credentials) will be reduced by 10% going forward. The extreme version is that an organization liquidates all its validators it is then ineligible for Patronage funds from the remaining validators.

Reductions to patronage pool participation shall have no impact on operator or hyperledger pool distributions.

## **Exhibit A**

**Vesting Period**

**Patron A**

**Patron B**

**Non-patroned Maintainers** 

**Rewards &amp; Fee Share**

**Withdrawal Credential Share**

1

7

1

2

70% A / 10% B / 20% HLF 

70% A / 10% B / 20% HLF

2

8

2

2

66.66% A / 16.66% B / 16.66% HLF

68.18% A / 13.64% B / 18.18% HLF

3

8

2

0

80% A / 20 % B / 0% HLF

71.88% A / 15.64% B / 12.5% HLF

Document generated by Confluence on Nov 26, 2024 12:59

[Atlassian](http://www.atlassian.com/)
