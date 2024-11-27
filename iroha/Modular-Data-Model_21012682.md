1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Modular Data Model

Created by Nikita Puzankov, last modified on Aug 21, 2020

Status

DECIDED

Stakeholders

[Ales Zivkovic](https://lf-hyperledger.atlassian.net/wiki/people/5b3a36d1d38a522e77ff78c0?ref=confluence) [Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence) [Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence) [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence) 

OutcomeThis functionality moves out of scope of 2.0.0Due date

21 Aug 2020

Owner

[Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence) 

## Background

Iroha Modular Data Model is a concept of "low-level" API for Iroha Peers processes configuration. It should be compared with Iroha DSL and decision about inclusion of this functionality in 2.0.x versions should be made.

More details on initial research: [![](attachments/thumbnails/21012682/21017016)](attachments/21012682/21017016.pdf)

## Problem

> The idea behind DM or HL Transact is to decouple business logic from the blockchain. It will allow to run Iroha with a subset of ISIs required for a specific deployment, or solely with Burrow EVM, or WASM as business logic layer, for example.

## Solution

> A data model (further referred to as **DM**) is a business model abstraction. It may provide interfaces to execute some commands and query some state. A DM implementation is a module that can be attached to an Iroha node. In that case, the set of commands delivered to a DM module is strictly determined by the ledger, which enables to build extensible blockchain applications.

Data Model approach gives an ability to extend basic Peer-side (server-side) functionality with general purpose languages (python, C++, etc.) and environments.

Iroha Users can deploy payload schemes for commands and queries:

[**https://raw.githubusercontent.com/hyperledger/iroha/master/example/data\_models/test\_kv/kv\_schema.proto**](https://raw.githubusercontent.com/hyperledger/iroha/master/example/data_models/test_kv/kv_schema.proto)

```
message Set {
string key = 1;
string value = 2;
}
message Nuke {}

message Command {
// extends CallModel
message Payload {
oneof command {
Set set = 1;
Nuke nuke = 2;
}
}
Payload payload = 1;
.iroha.protocol.DataModelId dm_id = 2;
}
```

And their implementations:

![](images/icons/grey_arrow_down.png)Click here to expand...

```
_save_file_path = str()
_persistent_kv_storage = dict()
_block_kv_storage = dict()
_tx_kv_storage = dict()


def get_supported_data_model_ids():
    return [('test_kv', '0.1.0')]


def execute(cmd_serialized: memoryview):
    cmd = kv_schema_pb2.Command()
    cmd.ParseFromString(cmd_serialized)
    which = cmd.payload.WhichOneof('command')
    global _tx_kv_storage
    if which == 'set':
        key = cmd.payload.set.key
        val = cmd.payload.set.value
        if not key in _tx_kv_storage:
            if len(_tx_kv_storage) >= MAX_SIZE:
                return (3, "storage limit exceeded")
        _tx_kv_storage[key] = val
        print(f'storage[{key}] is set to {val}')
        return None
    elif which == 'nuke':
        _tx_kv_storage.clear()
        print(f'storage cleared')
        return None


def commit_transaction():
    global _tx_kv_storage
    global _block_kv_storage
    _block_kv_storage = _tx_kv_storage.copy()


def commit_block():
    commit_transaction()
    global _block_kv_storage
    global _persistent_kv_storage
    _persistent_kv_storage = _block_kv_storage.copy()
    _save_persistent()


def rollback_transaction():
    global _tx_kv_storage
    global _block_kv_storage
    _tx_kv_storage = _block_kv_storage.copy()


def rollback_block():
    global _block_kv_storage
    global _persistent_kv_storage
    _block_kv_storage = _persistent_kv_storage.copy()
    rollback_transaction()


def _save_persistent():
    global _save_file_path
    global _persistent_kv_storage
    with open(_save_file_path, 'wt') as out:
        json.dump(_persistent_kv_storage, out)
    print(f'saved persistent data to {_save_file_path}')


def _load_persistent():
    global _save_file_path
    global _tx_kv_storage
    global _block_kv_storage
    global _persistent_kv_storage
    if (os.path.isfile(_save_file_path)):
        with open(_save_file_path, 'rt') as inp:
            _persistent_kv_storage = json.load(inp)
        _block_kv_storage = _persistent_kv_storage.copy()
        _tx_kv_storage = _persistent_kv_storage.copy()


def initialize(save_file_path: str):
    global _save_file_path
    _save_file_path = save_file_path
    _load_persistent()
```

Implementation has no strict API, so it can work with disk and network I/O, use available libraries, global static memory, etc.

It also has no Iroha API inside, but it can be added if needed.

### Decisions

- Use protobuf schema for Commands and Queries payloads  Use some schema for Commands and Queries descriptions
- Commands and Queries implementation should align to appropriate interfaces (rollback\_block, load\_persistent, etc.) in available SKDs?
- Executor makes a decision to proceed with command/query or not

### Alternatives

- Use client-side transformers and adapters to support 3rd party tools via Client-side Iroha API
- Use already existing WASM runtimes as a backend

### Concerns

- No strict requirements to environment is powerful yet dangerous solution
- Solution did not align well with Iroha 2.0 in it's current form

### Assumptions

- Clients and Iroha use gRPC or another protocol with Protobuf
- Custom commands and queries has no obvious API for Iroha

### Risks

- Protobuf will not be enough for 3rd party applications and users \`\[9;7]\`
- Powerful environments will require a lot of resources \`\[9;5]\`

## Additional Information

- [https://docs.rs/transact/0.2.4/transact/#modules](https://docs.rs/transact/0.2.4/transact/#modules)

## Attachments:

![](images/icons/bullet_blue.gif) [Modular DM for Iroha v1.x.pdf](attachments/21012682/21017016.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
