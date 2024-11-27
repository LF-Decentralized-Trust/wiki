1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Key-centric accounts structure

Created by Aleksandr Petrosyan, last modified on Apr 08, 2022

## Background

The old account structure was identified via two strings: the account's name and domain to which it belongs. As a consequence of the design of permissions, it was also necessary to have access to an account in order to register a new one in that same domain. This imposes many limitations on how Iroha could be used, particularly in the case where a generating an account offline is desirable.

The current account structure is also tied too heavily to specific strings. For example, if a user wants to change the name of their account or move it to a different domain, they cannot do it without creating a new account, transferring the keys, and then closing the old accounts.

In the interest of solving all of the above issues, as well as bringing Iroha closer to compatibility with substrate, we propose a re-structuring of the Iroha account in the following manner.

## Overview

We propose identifying an account with a single key pair. The initial key exchange/generation algorithms are to be decided, however they are not to be fixed once and for the duration of the existence of the blockchain. Rather, the algorithms are to be versioned, and backwards compatible, so an account registered at genesis, can still be used 10-20 years after it was created.

The account's address is identified with the public key. As a consequence, users are not required to provide any personally identifying information at any point. Moreover, because of the way in which key generation algorithms are designed, it can be assumed that even offline-generated key pairs do not coincide.

As a result, we can accept transactions that mention a specific account's address even before that account is registered (by providing an alias) and accessed by its owner.

This opens several security issues, and entails a sweeping change across the code-base, which we shall discuss below. 

## Technical details

### Address format

Regardless of which address format we (eventually) choose, the address must be derived from the public key.

- The easiest address to implement is exposing the full public key
- For security might prefer to expose a subset of the public key. If we use the first half of the bytes as the address, the probability of two accounts sharing an address is astronomically small (1 in 1024).
- Also for security we can use the *RsDSA25519* key exchange algorithm which doesn't expose the public key at the cost of performance.
- For maximum compatibility with Substrate, we should choose the [SS58 format](https://docs.substrate.io/v3/advanced/ss58/).

#### Substrate compatibility

The SS58 format allows for secure transit of account data. As an added bonus, the accounts can be identified on [different networks](https://github.com/paritytech/ss58-registry) (because of the first byte) if we so choose.

Substrate-based networks typically use the same private key to generate multiple public keys. Specifically one is used in the **substrate-based** network, while the other is used in **Ethereum** networks. As such we should support three standards [Sr25519](https://wiki.polkadot.network/docs/learn-keys), [Ed25519](https://wiki.polkadot.network/docs/learn-keys) and [secp256k1](https://wiki.polkadot.network/docs/learn-keys).

We should also consider delineating in-code the difference between [stash keys](https://docs.substrate.io/v3/concepts/account-abstractions/) (which are attached to highly secure accounts with most if not all of an individual's assets) and [controller keys](https://docs.substrate.io/v3/concepts/account-abstractions/).

Session keys are part of the staking infrastructure. We should support this use case, but we might want to consider deviating from the uses of sessions keys *only* as part of staking and not in cases of handling large lump sums in general.

![](https://miro.medium.com/max/486/1*9rewWI0WcPnFDWdkJjAQfw.png)

### Account security upgrades

To upgrade the key pairs from an account using aliases, the user

1. un-registers the alias for the original account;
2. generates a new key pair with the new algorithm;
3. registers the old alias to the new account;
4. transfers assets from the old account to the new;
5. (optional) archives the old account;

Note the following. Iroha must check for alias collisions, so step 1. is necessary. The vast majority of transactions are to use the alias rather than the public key of the account, so forwarding funds from the old account to the new is done automatically and without additional cost.

This process is either done by a single instruction, or explicitly with instructions for each step.

#### Alias security

It is assumed that changing the alias of an account requires knowledge of primary and secondary keys, so gaining control of the alias is equivalent to gaining full control of the account. Security measures largely overlap, which includes account archival (freezing).

While a lot of attention is paid to [software security in Ethereum](https://dl.acm.org/doi/fullHtml/10.1145/3391195), most attacks on the Ethereum chain happen as a result of [social engineering](https://www.trendmicro.com/vinfo/us/security/news/cybercrime-and-digital-threats/ethereum-classic-wallet-a-victim-of-social-engineering) and [user error](https://coinfomania.com/ethereum-user-loses-500k-weth-transfer-error/).

For example, one attack vector we can protect against is account aliases that are sufficiently similar, but not identical in terms of name resolution. Compare:

`alice@wonderland`

`аliсе@wоndеrlаnd`

the strings look identical, but have different UTF-8 representation: the `а` and `е`, characters are taken from the Cyrillic code page, and the two accounts have different on-chain representations.

A potential solution would be to warn the user whenever they send funds to a new address, which crosses a (dynamically computed) Levenstein distance threshold from the known recipients. We need to have a low false-positive rate, so that users are not tempted to turn off the annoying notification.

#### Using a new custom instruction: `MigrateAccount<Account, Account>`

##### Pros:

- Encourages frequent security updates.
- Good user experience.
- Eliminates client error in forming the transaction.
- Technically easier to do than transferring each asset one by one.

##### Cons:

- Complex.
- Adds ways to circumvent transaction fees in public blockchains.

#### Using explicit usage of pre-existing instructions

##### Pros:

- No extra tooling/permissions.
- Simple.
- Works well with the existing event infrastructure.

##### Cons:

- Discourages frequent security upgrades.
- Objectively harder to do.
- Is subject to user error.
- Can be more computationally expensive, since all assets are moved one by one.

### Primary and secondary keys

One key-pair is used to identify the account, and is called the primary key. Users are advised to generate more key pairs, called secondary keys. The primary and secondary keys should not have any common source. We should allow users to use the same passphrase to generate the primary and secondary keys, but encourage users to generate a new key.

If the primary public key is visible to everyone on the blockchain in full. As such, the primary private key can be obtained using prime factorisation and is thus vulnerable to attack. Hiding the secondary keys prevents cracking all keys in parallel, and mitigates brute force decryption attempts.

As such users are advised to opt into one or all of the following:

- Using RsDSA instead of EdDSA for the primary key. This brings us closer to **Ethereum** than to **substrate** in terms of compatibility.
- Frequent and automatic expiry and replacement of secondary key pairs. Suitable for people with frequent access to the internet and a hardware wallet (Integration pending).
- Cascading encryption of secondary keys:
  
  - The n-th private secondary key is used to encrypt the *n+1*-st, public key on-chain. The first secondary public key is encrypted by the first primary key.
- Bidirectional encryption of traffic.
- Restricted visibility: even knowing the primary key, but without any of the secondary keys, you cannotquery the public keys of the account.

### Changes to the ISI execution

All instructions that accept an `EvaluatesTo<Account>` shall now not return a `FindError`if

- The account is specified via a public key
  
  - The account doesn't exist; **OR**
  - The account exists **AND** the account was not archived.

As a result, all instructions that check for the existence of an account before execution should check how the target account was specified, and adjust accordingly.

#### Account Archival

Security considerations, particularly related to identity theft must be taken into account. Specifically, one must be able to revoke access to an account temporarily, provided that the primary key had been compromised. While multi-signature transactions somewhat mitigate the problem of brute force cracking of the private key given a public key (to be able to send transactions on behalf of the account, one must crack all of the keys, not just the primary), social engineering is still a viable attack vector.

If your primary key got stolen, odds are that the secondary keys were also stored in accessible

As such, simply removing an account or de-registering it is not sufficient to guarantee that no funds will be transferred to or from said account. As a result it's necessary to introduce a new state for accounts: **archived.** It's a special marker state in which permissions for all operations on the account except for the **de-archive** instruction are forbidden. The archival option is useful in the following scenarios:

1. In case of a data breach, if the attacker managed to obtain the **primary key**, but *not the majority* of the **secondary keys** (e.g. by brute-forcing the public key), the owner of the original account has the option to change all secondary keys.
2. In case of a data breach, if the attacker managed to obtain the **primary key, and the majority of (but not all of) secondary keys**, the owner still has the option to freeze the assets. Only the person with access to all the original keys can freeze the account. Upon unfreezing the accounts, it's advisable to change all secondary keys.
3. In case of a data breach, if the attacker managed to obtain **all of the accounts keys,** the attacker can do two things:
   
   1. Immediately transfer all or part of the assets to a different account. This is countered by the archival request.
   2. Attempt to change the secondary keys. The original owner would still have access to the primary key, and potentially transfer access to law enforcement, exposing the identity thief to persecution. The original owner can also register a smartcontract that archives the account if more than a set number of secondary keys are de-registered in a set block. This has the added benefit of storing the de-archival key in an accessible account, thus making it impossible to recover without cracking another primary key.
   3. Try to archive or delete the account.

In the 3-rd case of data breach, the identity thief is indistinguishable from the original owner. As such it is preferable to reduce the likelihood of data breaches, rather than trying to mitigate the consequences of a tier 3 data breach. We should consider non-technical factors as well: encouraging good security practices, opting-in to features that trade security for convenience, providing good middle-grounds between security and convenience and so on.

**Key collision is not a factor:** It is astronomically unlikely that two ed2559 keys coincide. Specifically, it's 1 in 2256 or 1 in 1077. The probability of no two keys coinciding given that the ed25519 algorithm works as advertised is 10-69 (due to the birthday paradox), if there are 108 or one hundred million accounts on the same network. Even assuming that the number of historical accounts is larger, it is practically impossible to generate the same key twice.

This was not necessary originally, because the user was capable of (in theory) changing the public key of their account. As accounts are inseparable from the keys used to generate them. It is impossible to do so with the new architecture.

When an account is archived, it should be possible to reverse, provided a few conditions are met.

1. the account that wishes to de-archive another account must retain the private key corresponding to the archived account. If the key is lost the account is archived permanently. Only the owner of the primary key can request archival.
2. Before or during archival another account may be optionally nominated as a successor. If such an account exists, de-archival requires knowledge of both (primary) private keys. Losing either one locks the account permanently.
3. After archival, smartcontracts involving the archived account fail with an error message. After de-archival smartcontracts resume operation as normal.
4. It's possible to remove smartcontracts from an archived account. It's not possible to add any.
5. In case 3.c, a thief gains nothing from archiving an account with a pre-nominated successor. Financial gain can still be extracted from deleting accounts (blackmail).

For point 3 to work, triggers must be given facilities to accumulate information about previously failed execution attempts (e.g. special metadata). This is necessary, because archival can be used to avoid smart-contract-based payments. In principle, this would allow people to purposefully archive their accounts after benefiting from a specific arrangement (e.g. default on their loan payments). There is no blanket solution to this, however. It's all up to the specific case where default occurred. For example:

- Defaulting on a loan happens outside of blockchain contexts. It is the responsibility of the loan provider to handle default.
- Recurring payments for recurring services may automatically cancel the smartcontract after a set number of failed payments.
- If the user archives the account tactically, so as to avoid specific payments it is the responsibility of the smartcontract to exchange resources atomically.

#### Transaction rollback

After archival, all pending transactions submitted from an archived account, but not executed at the time of archival are frozen: removed from the queue and added to a special section in the Archived account. When the archival is reversed the transactions are remembered, but not automatically re-submitted. Which transactions are to be re-submitted is chosen by the user after de-archival.

We can freeze the transactions that are still in the pipeline and submitted from a potentially compromised and archived account and that is in line both with what banks can offer, and relatively easy to implement.

In a blockchain setting, services like [Kirobo](https://bitcoinist.com/peter-schiff-loses-access-to-bitcoin/) offer the option to reverse unclaimed transactions only. Claimed transactions cannot be reversed unless both parties agree to a transfer (which in case of a malicious actor is unlikely). Kirobo also uses a weak password system that is prone to [user error](https://bitcoinist.com/peter-schiff-loses-access-to-bitcoin/). Reverting already committed transactions is not something that even banks do, so the utility of first-party support on Iroha networks is dubious.

### Changes to the Client API

The client must adapt to the new APIs of the Instructions. Additionally, since the client is likely to be the only program capable of generating a key offline, it is advisable to merge the functionality of `iroha_crypto_cli`into the client libraries/binaries.

The exact set of requirements to the client API is to be determined.

This RFC will be updated as soon as the RFC on offline transactions is also complete.

#### Offline key generation process

We might consider integrating with the pre-existing [infrastructure from substrate](https://wiki.polkadot.network/docs/learn-accounts#seed-generation). We should consider adding our own guide to generating key pairs; substrate has a lot of features that trade security for convenience, which might not be worth encouraging.

The key gets generated with the help of the client as discussed above. The public key is stored on-chain fully. And is fully public or partially public.

External actors are free to target the specified public key for transactions. The funds transferred to a key are debited from the sender and credited to the recipient *immediately.* Since the user no longer has the safety net of `FindError`to protect against errors in key-based transactions. Most transfers should be done through aliases, and not directly through addresses.

**OPTIONAL:** it may be worthwhile to add the option to revert a funds transfer if an account hadn't been claimed in a specified time period. At which point a smartcontract reverts the debit/credit and archives the account.

### Key pair versioning (optional)

We want:

- backwards compatibility. An account registered near genesis should still work 10-20 years later if the network is still up.
- the ability to add new key pair exchange/generation algorithms.
- a method for upgrading key pairs.

As a result, Iroha must support more than one set of algorithms, and more than one kind of storage for accounts.

The versioning could be done either

1. by tying the account version to the API version.
2. by versioning the account with the key type/exchange algorithm

The first option has the advantage of making full backwards compatibility explicit. A user who registered an account early doesn't need to update the client in order to work with the blockchain.

The second option gives us more flexibility.

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
