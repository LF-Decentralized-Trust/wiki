1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Requests for Comments](Requests-for-Comments_21016001.html)
5. [zzz\_\[ARCHIVE\]](21016320.html)

# Hyperledger Iroha : Transaction tags

Created by Kamil Salakhiev, last modified on Jun 10, 2020

## Problem

1. We need to guarantee certain order of transaction execution
2. Transactions could be sent in arbitrary order
3. Transactions that depend on each other might be either valid or invalid

In theory if we could guarantee that Iroha clients have all transactions that depend on each other at hand, then they would be able to utilize [batch](https://iroha.readthedocs.io/en/master/concepts_architecture/glossary.html?highlight=batch#batch-of-transactions) approach. Otherwise another solution is needed.

## Proposal – Transaction tags

### Tags

Tags are optional fields in transactions. Tags are arbitrary byte arrays that could be of two kinds:

1. \`requires\` – tags that current transaction require to be further sent into transaction pipeline
2. \`provides\` – tags that current transaction provide

### Requires tags

If transaction A submitted into transaction queue has \`requires\` tags, then it is stored in some \`waiting\_txs\` collection (makes sense to implement this collection as Multimap&lt;Tag, Transaction&gt; for a quick look up by tag). Otherwise if \`requires\` tags are empty, transaction is put into the \`ready\_txs\` collection.

### Provides tags

If transaction B received by transaction queue has \`provides\` tags, then all transactions that require that tags are removed from \`waiting\_txs\` collection and are put into the ready collection (assuming these transactions do not depend on other tags). The transaction B itself is included into the ready collection, assuming it does not depend on other tags.

### Getting ready transactions

Whenever peer is selected as the leader and creates a block from the transactions stored in ready collection.

**Important:** ready transactions collection should be returned in topological order defined by the tags, to guarantee in-order execution.

### Transaction longevity

Transactions that never receive required tags should not be stored forever. Iroha can define some default longevity for every transaction (either in maximum amount of blocks transaction will remain valid for (eg 100 blocks), or in maximum time duration (eg 24 hours)). However, it also makes sense to be able to specify custom longevity for any transaction by Iroha clients.

Therefore we can introduce another optional transaction field: *longevity*

Transaction should stay in \`waiting\_txs\` for the *longevity* period starting from the moment of transactions submission to the queue unless it is removed due to transaction being invalid or included into the finalized block. 

### Removal

There are two kinds of removal: **removeInvalid** and **removeValid**

#### removeInvalid

If some transaction is considered invalid during stateful validation it is removed from the transaction queue completely. All transactions from the same block that depend on removed transactions should be removed from the block and queue's \`ready\_txs\` collection and moved back to the \`waiting\_txs\` (assuming they do not have enough \`requires\` tags anymore). **Removed invalid transactions should not provide any tags after removal from the queue.**

#### removeValid

When some block is finalized all transactions from that block are removed from the queue's \`waiting\_txs\`. **Valid** **transactions being removed that way can still provide some tags for a period defined by transaction longevity (described above).** This is because if we have dependency A←B (B depends on A), then if A is applied and is not in the \`ready\_txs\` anymore, transaction B submitted later should have all required tags (assuming B was submitted within A's longevity period).

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
