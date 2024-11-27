1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Requests for Comments](Requests-for-Comments_21016001.html)

# Hyperledger Iroha : Iroha Configuration

Created by Nikita Puzankov, last modified by Ivan Rybin on Apr 13, 2021

  Status

 IN PROGRESS 

Stakeholders

[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence) [Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence) [Iurii Vinogradov](https://lf-hyperledger.atlassian.net/wiki/people/5c6a88bf8a38a065324b355a?ref=confluence)

OutcomeDue date

11 Sep 2020 

Owner

[Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence)

## Background

Iroha has a lot of configuration options, such as \`TORII\_URL\` for client and peer-side web addresses, \`BLOCK\_STORE\_PATH\` for path to the blockstore in the OS and \`TRANSACTION\_RECEIPT\_TIME\` for peer-to-peer messaging timeouts.

All this parameters should be configured and a lot of them should have an ability to be changed in runtime.

## Problem

The problem is to define a concept for Iroha Configuration management. Because parameters differ in their aim, ability to be managed during runtime and other aspects, we may need to have different mechanism for their management which in turn will bring additional complexity to our solution. To keep it simple we need to have a minimum options and differences in it.

To find such a solution we need to make a list of possible configurations first:

- Public and Private keys of Iroha Peer
- Kura configuration:
  
  - Kura Mode (strict or fast)
  - Block Store Path
- Sumeragi configuration:
  
  - Peer Id
  - Block Time
  - List of Trusted Peers
  - Maximum Amount of Faulty Peers
  - Commit Time
  - Transaction Receipt Time
- Torii configuration
  
  - Client-side URL
  - Peer-side URL
  - Maintenance URL
- Block synchronization configuration:
  
  - Gossip Period
  - Batch Size
- Queue configuration:
  
  - Maximum transactions in block
  - Transactions time to live
- Logger configuration:
  
  - Maximum Logging Level
  - Terminal Color Enabled
  - Date Time Format
- Initial configuration is out-of-scope because will be solved in [Genesis Block and Network Setup](Genesis-Block-and-Network-Setup_21016904.html)

Documentation for configuration can be found [here](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/references/config.md).

Now we can analyze each parameter with several criterias:

ParameterPossible ValuesDefault ValueShould it be synchronized between PeersShould it pass consensusCan it be applied without restartWill it affect clients

### `block_sync.batch_size`

unsigned 32 bit integer4Yes?YesYesNo

### `block_sync.gossip_period`

unsigned 128 bit integer10\_000YesYesYesNo

### `kura.block_store_path`

Valid Unix path

```
"./blocks"
```

NoNoWith additional developmentNo

### `kura.init_mode`

strict/fast

```
strict
```

NoNoWith additional developmentNo

### `logger.max_log_level`

TRACE/INFO/DEBUG/WARN/ERROR

```
DEBUG
```

NoNoYesNo

### `key_pair`

Valid Key Hash  
NoNoYesYes

### `queue.maximum_transactions_in_block`

unsigned 32 bit integer

```
8192
```

YesYesYesNo

### `queue.maximum_transactions_in_queue`

unsigned 32 bit integer65536

Yes

### `queue.transaction_time_to_live`

unsigned 128 bit integer

```
86400000(ms)
```

YesYesYesNo

### `sumeragi.block_time`

unsigned 128 bit integer

```
1000(ms)
```

YesYesYesNo

### `sumeragi.commit_time`

unsigned 128 bit integer

```
1000(ms)
```

YesYesYesNo

### `sumeragi.max_faulty_peers`

unsigned 32 bit integer0YesYesYesNo

### `sumeragi.max_instruction_number_per_tx`

unsigned 32 bit integer4096Yes  
Yes

### `sumeragi.n_topology_shifts_before_reshuffle`

unsigned 32 bit integer1Yes  
Yes

### `sumeragi.peer_id`

Valid URL + Key Hash  
Yes (Other Peers should update old Id to the new one)NoWith additional developmentYes

### `sumeragi.trusted_peers`

Valid URL + Key Hash\[]YesYesYesNo

### `sumeragi.tx_receipt_time`

unsigned 128 bit integer

```
200(ms)
```

YesYesYesNo

### `torii.api_url`

Valid URL

```
"127.0.0.1:8080"
```

NoNo  
Yes

### `torii.max_instruction_number`

unsigned 32 bit integer

```
4096
```

Yes

### `torii.max_sumeragi_message_size`

unsigned 32 bit integer

```
16384000
```

Yes

### `torii.max_transaction_size`

unsigned 32 bit integer32768

Yes

### `torii.p2p_url`

Valid URL

```
"127.0.0.1:1337"
```

YesNo  
No

### `torii.Maintenance URL`

Valid URL  
NoNo  
Yes

### `wsv.account_metadata_limits`

Byte size and UTF length4096, 1048576

Yes

### `wsv.asset_metadata_limits`

Byte size and UTF length4096, 1048576

Yes

### `wsv.length_limits`

Range\[1; 128]

Yes

## Solution

So solution may be to use Iroha Special Instructions for management consensus dependent parameters like "Gossip Period", storing set of parameters under a Peer entity in World State View and propagating these parameters and their updates into subsystems via Iroha channels.

Parameters that can be managed without consensus can avoid usage of Iroha Special Instructions and implemented separately as API for system administrators.

### Decisions

- Split parameters into consensus dependent and maintenance related
  
  - Use Iroha Special Instructions for consensus related
  - Put management of other parameters under [Maintenance Endpoint](Maintenance-Endpoint_21012343.html)
- Implement "hot reload" mechanisms in Iroha subsystems

### Alternatives

- Use Iroha Special Instructions for all parameters - brings additional set of instructions to maintain, increases load on blocks store and blocks synchronization, won't guarantee non-functional requirements from system administrators perspective (each update will take time needed to finalize block)
- Use Maintenance Endpoint for all parameters - brings additional complexity in terms of parameters synchronization and open security related issues (who can change "Batch Size" on all Peers?)
- Do not synchronize any parameters between Peers - may be a good option

### Concerns

Lack of real use cases and strong opinions on topic from potential users gave no ability to make a really welcoming decision.

### Assumptions

Maintenance Endpoint will be "unstable" during 2.0 release.

### Risks

- Solution will not cover all needs \`\[4;6]\`
- Requirements will be simpler than expected \`\[3;3]\`
- "Hot reload" mechanisms will require a lot of work \`\[6;7]\`

## Additional Information

![](attachments/21012818/21017237.png?height=226)

## Attachments:

![](images/icons/bullet_blue.gif) [image2020-9-3\_12-53-3.png](attachments/21012818/21017237.png) (image/png)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
