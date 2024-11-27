1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Place of assets in Iroha model

Created by Nikita Puzankov, last modified on May 18, 2020

## Problem

\`Asset\` entity's duality in Iroha may be confusing, speaking about \`Asset\` as a type or category of all amount of this \`Asset\` spread across the ledger and \`Asset\` as a amount or quantity that may be associated with an account.

### v1 Definition

[Any countable commodity or value. Each asset is related to one of existing domains. For example, an asset can represent any kind of such units - currency unit, a bar of gold, real estate unit, etc.](https://iroha.readthedocs.io/en/master/concepts_architecture/glossary.html#asset)

At the same time:

[The purpose of add asset quantity command is to increase the quantity of an asset on account of transaction creator. Use case scenario is to increase the number of a mutable asset in the system, which can act as a claim on a commodity (e.g. money, gold, etc.)](https://iroha.readthedocs.io/en/master/develop/api/commands.html#purpose)

And:

[The purpose of сreate asset command is to create a new type of asset, unique in a domain. An asset is a countable representation of a commodity.](https://iroha.readthedocs.io/en/master/develop/api/commands.html#id21)

Also as has been implemented in Iroha v1:

[![](attachments/21012291/21016195.png?height=250)](https://soramitsu.atlassian.net/wiki/spaces/IS/pages/165734/Data+model)

We can see that both, Account and Domain were both partial containers (owners, holders, etc.) for an Asset entity, mixing it's type (asset\_id + precision) with it's values (asset\_id + account\_id + data + amount).

### v2 Definition

According to [v2 Model](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md):

```
                has one
   +--------------------------------+
   |                                |
   |     +------------+             |
   |     |Domain      |             |
   |     +---------+  |             |
+--+-+   ||Asset(s)|  |             |
|Peer|   +---------+  |             |
+--+-+   |            |             |
   |     +------------+             |
   |     ||Account(s)||  has  +-----v-----+
   |     |-------------------->Signatories|
   |     +------------+       +-----------+
   |                |
   |                |    has  +-------------+
   |                +--------->Permission(s)|
   |                          +-----^-------+
   |                                |
   |                     has        |
   +--------------------------------+
```

We do not have any association between \`Asset\` and \`Account\` entities, which means we can't \`Mint\` some \`Asset\` to the \`Account\` - only to the \`Domain\`.

> **Transfer**= Batch(Sub(WhatAsset, WhatAmount, Account1) &amp; Add(WhatAsset, WhatAmount, Account2)) NOTE: Should probably inline Transfer as a primitive because it is going to be one of the most common instructions that is executed.

So if we will \`Transfer\` instruction as an example, it is pointless to transfer Asset's Amount from one Account into another because we do not have an Asset's amount (or quantity) as an entity inside Iroha model.

Usage of v1 Id formats (asset\_name#domain\_name) will not save the situation or make it more clear because it will define identification of an Asset's type, not the "real" asset (which need account\_id in the format of account\_name@domain\_name).

### Conclusion

To be clear within our team and with our users we should define non-dual definition of an \`Asset\` entity, define it's schema (or make it schemaless to support non-digit assets) and update terminology both in code and in whitepaper.

## Entity Component Proposal

As a proposal, let me introduce some parts of Entity Component System approach.

We can define an \`Asset\` as an **Entity,** which is an identification of an \`Asset\` (we may use v1 format asset\_name#domain\_name here). Which will be used for operations on an \`Asset\` in general (for example to retrieve all assets from the domain or find all transactions which interact with this asset). At the same time we will have an \`Asset\` **Components**, which will represent "real" assets and will connect them with the\`Account\` entity.  The main question here is where to define the border between the interface and the implementation. Should users understand the difference or not?

Because Instructions may dependent on the \`Asset\` aspect, it looks like they should be aware of it and work with Components to Mint an Asset, while use Entity when making some analytic requests. So to make it clear for them (and provide a better implementation in the WorldStateView) we may have the following picture:

```
                has one
   +--------------------------------+
   |                                |
   |     +------------+             |
   |     |Domain      |             |
   |     +---------+  |             |
   |     ||Asset(s)|  |             |
   |     ||+------+|  |             |
   |     |||Entity||  |             |
   |   |----      ||  |             |
+--+-+ | ||+------+|  |             |
|Peer| | +---------+  |             |
+--+-+ | |            |             |
   |   | +------------+             |
   |   ->||Account(s)||  has  +-----v-----+
   |     |-------------------->Signatories|
   |     +------------+       +-----------+
   |                |
   |                |    has  +-------------+
   |                +--------->Permission(s)|
   |                          +-----^-------+
   |                                |
   |                     has        |
   +--------------------------------+
```

Where Asset entity under Domain has entities which knows about accounts they "belong" to. Asset Id in this case stay asset\_name#domain\_name, while entity Id can be represented as asset\_name#account\_name@domain\_name.

## Comments

```
Nikita Puzankov, [13.05.20 15:25]
[ Photo ]
Hi team - I pushed code that compiles (with tests) https://github.com/hyperledger/iroha/pull/499 and going to fix tests before making code "clean" - but the main idea already can be checked in iroha_clien tests - like transfer asset:
as you can see, Instructions are not coupled with their parameters

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [13.05.20 17:13]
[In reply to Nikita Puzankov]
Generally you are right, but it is a little more complicated than this. Assets modifications should be in accordance with permissions. Some users could in theory be able to create new assets, whereas others are allowed to not create, but transfer. Permissions can be granted, so it is not necessarily the same people who have create permission that were the initial account that registered.

Nikita Puzankov, [13.05.20 17:31]
[In reply to Makoto Takemiya 武宮誠 (Sora.org - Soramitsu)]
why can’t we lock permissions on assets names and store assets under accounts?

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [13.05.20 17:46]
Not sure what you mean

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [13.05.20 17:47]
What I mean is there is no asset "owner." Accounts have assets and they have permissions about what they can do with those assets

Nikita Puzankov, [13.05.20 18:11]
[In reply to Makoto Takemiya 武宮誠 (Sora.org - Soramitsu)]
So instead of transferring assets, they transfer permissions?

Nikita Puzankov, [13.05.20 18:12]
For example there is XOR asset with quantity 20. My account is the only one with permissions to use them. If I want to "give" 2 XOR to another account, I reduce the quantity in my permission to 18 and grant permission with quantity 2 to another account?

Nikita Puzankov, [13.05.20 19:12]
right now in paper we have no connection between accounts and assets, in impl we have assets in both - domains and account:
WorldStateView { peer: Peer { peers: {}, listen_address: "127.0.0.1:1338", domains: {"domain": Domain { name: "domain", accounts: {Id { entity_name: "account", domain_name: "domain" }: Account { id: Id { entity_name: "account", domain_name: "domain" }, assets: {}, signatories: [[101, 170, 80, 164, 103, 38, 73, 61, 223, 133, 83, 139, 247, 77, 176, 84, 117, 15, 22, 28, 155, 125, 80, 226, 40, 26, 61, 248, 40, 159, 58, 53]] }}, assets: {Id { entity_name: "xor", domain_name: "domain" }: Asset { id: Id { entity_name: "xor", domain_name: "domain" }, quantity: 200 }} }} } },

Nikita Puzankov, [13.05.20 19:12]
and to fix tests rights we need to define the place assets belongs to. let's skip permissions part and solve this task first.

Nikita Puzankov, [13.05.20 19:29]
https://wiki.hyperledger.org/display/iroha/Place+of+assets+in+Iroha+model I made a small RFC about this question

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [14.05.20 05:43]
[In reply to Nikita Puzankov]
It's correct from a philosophical standpoint, but not a very practical way to look at it. It's like giving you a 50 ruble note gives you permission to go spend it.

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [14.05.20 05:55]
What I mean is there are robust permissions that we need. For example, only designated accounts should be able to add to the quantity, some accounts (like a bank) need to be able to change signatories of another anount (like a bank's customer). For queries, some users may be able to query their own or their own domain's transactions, but not other users or other domains.

And of course permissions should have good defaults. For example, in the Sora network, only the xor@sora account can mint new XOR, though this account should be able to create events that can mint xor, like the XST stable coins. And no one else should be able to mint XOR. For the Sora network, anyone should be able to read all data as it is a public blockchain, but the criteria to become a validator is to hold 700,000 vested XOR in a locked up bond and other accounts should nominate you with a total of 5 million vested XOR in a locked up bond.

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [14.05.20 05:56]
[In reply to Nikita Puzankov]
querying by assets (e.g., all transactions for sora#xor) and querying by accounts (e.g., all transactions for makoto@sora) are both common use cases, so you need both views and the KV-maps in the WSV should store links to both

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [14.05.20 05:57]
BTW, we should follow the Iroha naming convention where assets are domain#asset and accounts are acct_name@domain. This can be on the SDK-side, though, so whatever is easiest internally is best

Nikita Puzankov, [14.05.20 10:58]
@salakhiev how did you associate assets and accounts in iroha 1?

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [14.05.20 11:04]
It's a sql database model

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [14.05.20 11:06]
In Iroha2 we are using a kv store to model wsv, so it makes sense to just store the data we will query via api

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [14.05.20 11:07]
For example, we want to know how many assets each account has, how many qty exists in total for an asset, and be able to get transactions that are incoming/outgoing for an account by asset and also transactions for an asset in general, across all accounts

Kamil' Salakhiev, [14.05.20 11:08]
[In reply to Nikita Puzankov]
This model can help I think. https://soramitsu.atlassian.net/wiki/spaces/IS/pages/165734/Data+model

Makoto Takemiya 武宮誠 (Sora.org - Soramitsu), [14.05.20 11:09]
[In reply to Kamil' Salakhiev]
@humb1t this is why I put Assets under Domain originally, though of course the Domain is just something like a namespacing of where the Asset definition is, not who owns instances of it.
```

## Attachments:

![](images/icons/bullet_blue.gif) [image2020-5-13\_19-24-20.png](attachments/21012291/21016179.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2020-5-13\_19-28-41.png](attachments/21012291/21016180.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2020-5-18\_16-38-40.png](attachments/21012291/21016195.png) (image/png)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
