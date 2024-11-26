1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Design Documents](Design-Documents_22153916.html)

# Besu : Bonsai archive feature

Created by Matthew Whitehead, last modified on Oct 11, 2024

For background there is a design document relating to Bonsai DB in the wiki [here](Bonsai-Tries-Design-Overview_22154710.html)

The issue for Bonsai archive is [here](https://github.com/hyperledger/besu/issues/5846) and the PR is [here](https://github.com/hyperledger/besu/pull/7475). For context there was originally a [draft PR](https://github.com/hyperledger/besu/pull/5865) which was a start at delivering the feature, and a re-based branch of that PR [https://github.com/jframe/besu/tree/multi-version-flat-db-rebase](https://github.com/jframe/besu/tree/multi-version-flat-db-rebase) 

## Design

Bonsai makes use of additional DB segments to store flat data in addition to the state trie. These segments include:

- ACCOUNT\_INFO\_STATE
  
  - Key = hash of account
  - Value = RLP encoded account state
- ACCOUNT\_STORAGE\_STORAGE
  
  - Key = hash of account + hash of storage slot key
  - Value = RLP encoded storage value
- CODE\_STORAGE
  
  - Key = hash of code or hash or account (based on--Xbonsai-code-using-code-hash-enabled config option)
  - Value = the code

These are used to store account state, account storage, and code respectively.

Since the accounts are keyed off a hash of the account address, only one entry can exist in the flat DB for every account. To allow historic state to be stored in the flat DB, the key for an account must include the block number that the account state changed.

Regular bonsai account key:

- 0x4D95FBAF35Fc5A815983F9df94821C1c089DC02f -&gt; &lt;account state&gt;

Bonsai archive account key:

- 0x4D95FBAF35Fc5A815983F9df94821C1c089DC02f000000000000000a -&gt; &lt;account state at block 0x0a&gt;

A query can then be performed to request the state at a given block.

### Finding the nearest state entry for a block

With the above DB lookup scheme we can query state for any block at which that account's state changed. However, we also need a way to find the state of an account at a block where that account wasn't updated. Take the following example:

1. Block 0x0a: account 0x4D95FBAF35Fc5A815983F9df94821C1c089DC02f changes
2. Block 0x0b: account 0x4D95FBAF35Fc5A815983F9df94821C1c089DC02f doesn't change
3. Block 0x0c: account 0x4D95FBAF35Fc5A815983F9df94821C1c089DC02f changes again

With these state changes there will only be an entry in the flat DB for keys 0x4D95FBAF35Fc5A815983F9df94821C1c089DC02f000000000000000a and 0x4D95FBAF35Fc5A815983F9df94821C1c089DC02f000000000000000c. However, we still need to be able to ask what the state of an account is at block 0x0b.

The archive feature therefore implements getNearestBefore() and getNearestAfter() logic. The get-nearest functions perform a lexicographical search for the nearest entry in the DB to the requested key (in this case, 0x4D95FBAF35Fc5A815983F9df94821C1c089DC02f000000000000000b). On finding that the nearest previous lexicographical entry is 0x4D95FBAF35Fc5A815983F9df94821C1c089DC02f000000000000000a, Besu returns that state at that block. This provides the logic needed to satisfy calls such as `eth_getBalance` at an arbitrary block.

### New DB segments

Clearly the size of the flat DB for a Bonsai archive node is going to be considerably larger than that of a regular Bonsai node. This is the tradeoff made by a user who wishes to have access to all historic state of a chain. In order to reduce the performance impact on importing new blocks, the Bonsai archive approach uses different DB segments for historic entries:

- ACCOUNT\_INFO\_STATE\_ARCHIVE
  
  - Key = hash of account + block number
- ACCOUNT\_STORAGE\_ARCHIVE
  
  - Key = hash of account + hash of storage key + block number

Here is an example `ldb` query of the DB for a specific account at a specific block:

> ubuntu@localhost:~$ ldb --db=. get --key\_hex --value\_hex --column\_family=ACCOUNT\_INFO\_STATE\_ARCHIVE 0x3e26253c5a8b02bb30c92798fa8083f0c966a954b019cad73aa12cdf3b344a7e00000000000113a1  
0xF84D0389171FA691DC31EF9AA8A056E81F171BCC55A6FF8345E692C0F86E5B48E01B996CADC001622FB5E363B421A0C5D2460186F7233C927E7DB2DCC703C0E500B653CA82273B7BFAD8045D85A470

The original DB segments will typically only contain current state, therefore retaining the block-import performance of a regular Bonsai node. Asynchronously, the node will move old state from these segments to the archive segments. When state is queried, the node initially checks in the current state segment for the account and block. If it isn't found, the node then checks in the correct archive segment to see if it exists there.

The archive state (i.e. which block has the node archived state for) needs to be persisted to the DB as well. To do this, an additional entry exists in the `ACCOUNT_INFO_STATE_ARCHIVE` segment to record which block the node has archived up to. Note - archiving a block simply means moving all state that relates to changes in that block, from the primary DB segment(s) to the archive DB segment(s). If a block only includes new state (new account, new contract deploy etc) then no entries will be moved to the archive segments as part of archiving that block.

## Configuration

Bonsai archive is delivered as a new data storage format. Initially it will be experimental. To create a Bonsai archive node use --data-storage-format=X\_BONSAI\_ARCHIVE

## Rocks DB column families

Currently the column families are identified by an individual byte. You need to know that e.g. 0x0a maps to `TRIE_LOG_STORAGE` in order to make direct queries of the database for problem diagnosis. For example `ldb --db=. --column_family=$'\x0a' ...` is used to perform queries against the `TRIE_LOG_STORAGE` DB segment. The 2 new archive segments have been named with their full name. This makes direct DB queries much easier, as per the example given above querying `--column_family=ACCOUNT_INFO_STATE_ARCHIVE`. It may be useful in the future to change the existing DB segments to use their full names, but since this would require DB migration for existing state is has not been done as part of the archive work.

Document generated by Confluence on Nov 26, 2024 13:00

[Atlassian](http://www.atlassian.com/)
