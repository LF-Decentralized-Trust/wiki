1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [How-to articles](How-to-articles_22154631.html)

# Besu : Limit Trie Logs for Bonsai

Created by Simon Dudley, last modified on Jun 14, 2024

**\*\*instructions only work for besu version 24.3.0 onwards**\**

**UPDATE**: Since [24.6.0](https://github.com/hyperledger/besu/releases/tag/24.6.0), this feature has been promoted to production ready and is enabled by default: \```--bonsai-limit-trie-logs-enabled` ``

## Step by Step Guide

**IMPORTANT**: we strongly recommend reading the rest of this documentation before running these commands because your node’s configuration may require changes to these commands…

1. Update besu config to add `--Xbonsai-limit-trie-logs-enabled` but don’t restart yet
2. Stop besu
3. (optional) Run:
   
   `sudo /usr/local/bin/besu/bin/besu --data-storage-format=BONSAI --data-path=/var/lib/besu --sync-mode=X_SNAP storage x-trie-log prune`
4. Start besu (remembering to run `sudo systemctl daemon-reload` if you use a systemd service file as per CoinCashew and Somer)
5. Look out for `Limit trie logs enabled: retention: 512; prune window: 30000` in your besu config printout during startup
6. Enjoy more GBs

## What?

We have a new experimental feature available: `--Xbonsai-limit-trie-logs-enabled` which aims to keep Besu’s database as small as it can be. After a brief grace period, we intend to make this enabled by default for stakers. This is only relevant if you're using `data-storage-format=BONSAI` .

From our testing, we estimate this will **save users &gt; 3 GB per week** in database growth. Early testing indicates Besu’s **overall database growth with this enabled is ~7 GB per week** (thanks Yorick!) which is on par with geth. See here for more details about resource usage: [https://eth-docker.net/Usage/ResourceUsage/#disk-ram-cpu-requirements](https://eth-docker.net/Usage/ResourceUsage/#disk-ram-cpu-requirements)

## Why?

Some users noticed that resyncing Besu can free up disk space, especially for longer running nodes. This is despite `--data-storage-format=BONSAI` having “implicit pruning”. More on this reddit thread: [https://www.reddit.com/r/ethstaker/comments/12xnxxi/clearing\_up\_besubonsai\_confusion\_on\_state\_growth/](https://www.reddit.com/r/ethstaker/comments/12xnxxi/clearing_up_besubonsai_confusion_on_state_growth/)

In reality, whilst the Merkle Patricia Trie is implicitly pruned, the BONSAI feature did introduce an extra data structure: the Trie Log (more detail about BONSAI and trie logs here: [https://consensys.io/blog/bonsai-tries-guide](https://consensys.io/blog/bonsai-tries-guide))

The Trie Logs are retained in order to cope with chain reorgs. After each block is finalized, Trie Logs older than that are no longer required so it is safe to remove them from both the node's and the network's point of view.

## How?

If you want to use this feature before it is enabled by default, simply add this option to your besu command: `--Xbonsai-limit-trie-logs-enabled`  
When you restart besu it will begin pruning, block by block (and a cheeky bit during besu startup).

If you want **maximum database size reduction**, read on…

If you have a long-running node, this will not immediately clear your backlog of trie logs in the same way that resyncing does. In order to do this we’re providing a “run once” **offline** command to immediately **prune all your old trie logs in a few minutes or less.** Note, this requires besu to be shutdown before running, but downtime will be minimal. You will **not** need to run this command a second time if you keep `--Xbonsai-limit-trie-logs-enabled`.

## I’m impatient, reduce my database size now!

Okay, okay - we got you! We built a one-off besu command to remove this extra data (usually ***in seconds**)* and avoid having to resync. For minimal downtime, we recommend running this command **before** restarting Besu `--Xbonsai-limit-trie-logs-enabled` (easiest to do it all at the same time).

If you followed Somer Esat’s ([https://someresat.medium.com/guide-to-staking-on-ethereum-ubuntu-teku-f09ecd9ef2ee](https://someresat.medium.com/guide-to-staking-on-ethereum-ubuntu-teku-f09ecd9ef2ee) ) or CoinCashew’s guide ([https://www.coincashew.com/coins/overview-eth/guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/step-3-installing-execution-client/besu](https://www.coincashew.com/coins/overview-eth/guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/step-3-installing-execution-client/besu)) then you likely have these options set in your `besu.service` or `execution.service` systemd file:

```
...
ExecStart=/usr/local/bin/besu/bin/besu \
...
  --sync-mode=X_SNAP \
  --data-path="/var/lib/besu" \
  --data-storage-format=BONSAI \
...
```

So in order to prune the trie logs, your command should be something like:

`sudo /usr/local/bin/besu/bin/besu --data-storage-format=BONSAI --data-path=/var/lib/besu --sync-mode=X_SNAP storage x-trie-log prune`

The logs should look something like this...

```
2024-02-02 05:45:41.162+00:00 | main | INFO  | KeyPairUtil | Attempting to load public key from /data/besu/key
 ...
2024-02-02 05:45:43.433+00:00 | main | INFO  | TrieLogSubCommand | Estimating trie logs size before pruning...
2024-02-02 05:45:43.837+00:00 | main | INFO  | TrieLogSubCommand | Estimated trie logs size before pruning: 9 GiB
2024-02-02 05:46:09.863+00:00 | main | INFO  | TrieLogHelper | Starting pruning: retain 512 trie logs, processing in 1 batches...
2024-02-02 05:46:09.918+00:00 | main | INFO  | TrieLogHelper | Saving trie logs to retain in file /data/besu/database/trieLogsToRetain-1 (batch 1)...
2024-02-02 05:46:09.926+00:00 | main | INFO  | TrieLogHelper | Obtaining trielogs from db, this may take a few minutes...
2024-02-02 05:46:10.100+00:00 | main | INFO  | TrieLogHelper | Clear trie logs...
2024-02-02 05:46:10.155+00:00 | main | INFO  | TrieLogHelper | Restoring trie logs retained from batch 1...
2024-02-02 05:46:10.222+00:00 | main | INFO  | TrieLogHelper | Key(0): 0xcd50706da7f6f2db7f9d54f3589122760900d9ab2508c20a4ca40b496d930368
... 
2024-02-02 05:46:10.336+00:00 | main | INFO  | TrieLogHelper | Key(511): 0x238f9649b59616430ad7e43b8f3cf65bc97cac4aa54a3eddf3ad6ee666ce733e
2024-02-02 05:46:10.441+00:00 | main | INFO  | TrieLogHelper | Deleting files...
2024-02-02 05:46:10.446+00:00 | main | INFO  | TrieLogSubCommand | Finished pruning. Re-estimating trie logs size...
2024-02-02 05:46:11.023+00:00 | main | INFO  | TrieLogSubCommand | Estimated trie logs size after pruning: 0 B (0 B estimate is normal when using default settings)
2024-02-02 05:46:11.023+00:00 | main | INFO  | TrieLogSubCommand | Prune ran successfully. We estimate you freed up 9 GiB!
Prune ran successfully. We estimate you freed up 9 GiB!
```

If you use a toml config file, then you can simply do something like:

`sudo /usr/local/bin/besu/bin/besu --config-file=besu-config.toml storage x-trie-log prune`

## Subcommand Troubleshooting

The prune command should look something like this for mainnet users…  
`sudo /usr/local/bin/besu/bin/besu --data-path=/var/lib/besu --data-storage-format=BONSAI --sync-mode=X_SNAP storage x-trie-log prune`

and besu should be shutdown before running it.

> java.lang.IllegalArgumentException: Subcommand only works with data-storage-format=BONSAI

Are you missing --data-storage-format=BONSAI? It must be add *before* the `storage` subcommand, i.e.

`sudo /usr/local/bin/besu/bin/besu --data-storage-format=BONSAI --data-path=/var/lib/besu --sync-mode=X_SNAP storage x-trie-log prune`

* * *

> java.lang.RuntimeException: Column handle not found for segment TRIE\_BRANCH\_STORAGE

Did you specify the \`data-path\`?

`sudo /usr/local/bin/besu/bin/besu --data-path=/var/lib/besu --data-storage-format=BONSAI --sync-mode=X_SNAP storage x-trie-log prune`

* * *

> … | INFO | RocksDBKeyValueStorageFactory | No existing database detected at /tmp/besu. Using version 2  
…  
java.lang.IllegalArgumentException: Trying to retain more trie logs than chain length (0), skipping pruning

Did you specify the correct `data-path` for your node?

`sudo /usr/local/bin/besu/bin/besu --data-path=/var/lib/besu --data-storage-format=BONSAI --sync-mode=X_SNAP storage x-trie-log prune`

* * *

> java.lang.IllegalArgumentException: Cannot store generated private key.

Did you specify the correct `data-path` for your node?

`sudo /usr/local/bin/besu/bin/besu --data-path=/var/lib/besu --data-storage-format=BONSAI --sync-mode=X_SNAP storage x-trie-log prune`

* * *

> … | INFO | KeyPairUtil | Attempting to load public key from /data/besu/key
> 
> java.lang.IllegalArgumentException: Supplied file does not contain valid keyPair pair.

Check your file permission, you made need to run the command as sudo:  
`sudo /usr/local/bin/besu/bin/besu --data-storage-format=BONSAI --data-path=/var/lib/besu storage --sync-mode=X_SNAP x-trie-log prune`

* * *

> java.lang.RuntimeException: Column handle not found for segment WORLD\_STATE

Are you using `data-storage-format=FOREST` instead of `data-storage-format=BONSAI` on an existing bonsai database?

* * *

> org.hyperledger.besu.plugin.services.exception.StorageException: org.rocksdb.RocksDBException: While lock file: /data/besu/database/LOCK: Resource temporarily unavailable

Is besu already running? You need to shut the besu client down before running this subcommand.

* * *

> java.lang.IllegalStateException: Unable to change the sync mode when snap sync is incomplete, please restart with snap sync mode

Have you specified the sync-mode? Default is sync-mode=FAST. Most mainnet users use X\_SNAP or X\_CHECKPOINT

`sudo /usr/local/bin/besu/bin/besu --sync-mode=X_SNAP --data-storage-format=BONSAI --data-path=/var/lib/besu storage x-trie-log prune`

* * *

> java.lang.RuntimeException: No finalized block present, can't safely run trie log prune

If your node is relatively new or recently resynced, you might not need to run this command.

* * *

> org.hyperledger.besu.util.InvalidConfigurationException: Supplied genesis block does not match chain data stored in /data/besu.

Are you running this command for a network other than mainnet? You need to specify the network…

`sudo /usr/local/bin/besu/bin/besu --network=holesky --sync-mode=X_SNAP --data-storage-format=BONSAI --data-path=/var/lib/besu storage x-trie-log prune`

## The Details

Too much detail for users but if you’re interested:

[https://github.com/hyperledger/besu/issues/5390](https://github.com/hyperledger/besu/issues/5390)  
[https://github.com/hyperledger/besu/pull/6026](https://github.com/hyperledger/besu/pull/6026)  
[https://github.com/hyperledger/besu/pull/6303](https://github.com/hyperledger/besu/pull/6303)

Document generated by Confluence on Nov 26, 2024 13:01

[Atlassian](http://www.atlassian.com/)
