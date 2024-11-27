1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Multisignature transactions

Created by Nikita Puzankov, last modified by Egor Ivkov on Mar 04, 2021

Status

DECIDED

Stakeholders

[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) [Kamil Salakhiev](https://lf-hyperledger.atlassian.net/wiki/people/557058:07723e0b-a027-4cc4-ad6d-324e41cccb4d?ref=confluence) [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence)  [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence)

Outcome

Error rendering macro 'jira' : null

Due date

20 Jan 2021

Owner

[Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence)

## Background

At the time of writing Iroha works with single-signature transactions which are accepted by the peers signed only by one signatory. However in some cases it is not enough.

## Problem

There is a need for transactions that should be signed by several signatories from the same account for security purposes when dealing with large sums of money. Also it is planned to support conditional multisig (for example to support typical scenarios as two tellers should sign or one manager should sign). The detailed description of conditional multisig can be found in the [whitepaper](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#261-multisignature-transactions).

### Requirements

From [Iroha 1](https://iroha.readthedocs.io/en/master/concepts_architecture/glossary.html#multisignature-transactions):

> A transaction which has the **quorum** greater than one is considered as multisignature (also called mst). To achieve stateful validity the confirmation is required by the **signatories** of the creator account. These participants need to send the same transaction with their signature.

And from [Iroha 1](https://iroha.readthedocs.io/en/master/concepts_architecture/architecture.html#mst-processor) again:

> Multisignature Transactions Processor
> 
> It is an internal gRPC service that sends and receives messages from other peers through Gossip protocol. Its mission is to send out multisignature transactions that have not received enough signatures to reach the quorum until it is reached.

From [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence)

> 1. To have **quorum in each account** and possibility to change it by the command (+ corresponding permissions)  
2\. To have possibility to **configure list of signatories for the current accoun**t (+ corresponding permissions)  
3\. To have possibility to **get list of pending transactions** waiting for the additional signatures (related to the current account or in network in general + corresponding permissions)  
4\. Configuration of the **time**, while pending transactions will be in the **pending** list before being rejected  
5\. Corresponding checks in stateful validation to check all these rules  
6\. Corresponding checks and sync in the block proposal algorithm, consensus and mechanism of syncing the list of pending MST transactions between all nodes.  
7\. Place for future insertion of the conditional logic for MST checkups

#### Conditional multisignature

From the whitepaper: [https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha\_2\_whitepaper.md#conditional-multisignature](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#conditional-multisignature)

> Let's consider a situation where a bank wants to allow either 2 tellers or 1 manager to sign off on any transfer transaction over $500 and under $1000. In this case, the condition will be: Condition.asset("usd@nbc").qty(500).comparison("&gt;").qty(1000).comparison("&lt;") and the signatory\_sets for the tellers and manager will be OR unioned, so that either the m-of-n signatues from the tellers or the single signature from the manager will be acceptable for transaction signing.

## Solution

Second version of Iroha evolved the design of Iroha 1.x and can't use the same approach while it works to address requirements.

### **Conditional mutlisig**

The conditional multisig is planned to be implemented with the support of the [Expressions](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_data_model/src/expression.rs) that let the user to define their own conditions. An example implementation of the whitepaper scenario is given in [one of the expression tests](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha/src/expression.rs#L281).

### **Transaction Pipeline**

In Iroha2 there will not be a strict division between a multisig and a simple transaction. Instead transactions will be collected on the leader peer in a queue until the moment its account's \`signature\_condition\` (in the form of Expressions) is true for this transaction or dropped when its TTL is reached.

### **Client Side Interaction**

**Iroha 1.x Approach**

It was considered to use the same approach as in Iroha 1.x and to send the same transaction several times with different signatures from the client. But there is a following problem with this approach:

Transaction hash incorporates the timestamp of transaction creation in Iroha2. So even if transaction were sent with the same contents, the hash because of the timestamp will be different, and therefore it would be impossible to aggregate signatures (which have hash as a payload).

**Iroha 2 Approach**

Therefore in Iroha2 the following approach is planned to be used.

1. First client to submit the MST transactions, submits it normally as any other transaction
2. Other clients that want to add signatures to this tx request this pending tx from the Iroha peer and sign it with their signature and resubmit it.

But the UX does not need to change for the end user. For example:

1. User wants to submit a transaction
2. Client library requests if there are any transactions waiting for signatures from this account
3. If there are, it acquires them and compares to the one that user wants to submit
4. If contents of transaction match excluding the timestamp
5. Client library asks if the user wants to add a signature to already existing transaction

Therefore users may submit MST asynchronously without the knowledge of who submitted it first.

### Concerns

### Assumptions

### Risks

## Additional Information

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
