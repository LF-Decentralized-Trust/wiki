1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)

# Hyperledger Iroha : Architecture Decision Records Log

Created by Nikita Puzankov, last modified by Vadim Reutskiy on Jul 05, 2020

- [Iroha Special Instructions DSL](Iroha-Special-Instructions-DSL_21012073.html)
- [Serialization Format](Serialization-Format_21012087.html)
- [Networking stack](Networking-stack_21012097.html)
- [Rust Async Runtime](Rust-Async-Runtime_21012109.html)
- [Prevent replay of rejected transactions](Prevent-replay-of-rejected-transactions_21016013.html)
- [Logging](Logging_21012113.html)
- [Web API](Web-API_21012259.html)
- [Blocks sign off](Blocks-sign-off_21016055.html)
- [Sumeragi Error Handling](Sumeragi-Error-Handling_21016065.html)
- [Encapsulation of crypto related functionality](Encapsulation-of-crypto-related-functionality_21016068.html)
- [Async-std API usage](Async-std-API-usage_21012267.html)
- [Place of assets in Iroha model](Place-of-assets-in-Iroha-model_21012291.html)
- [Different key types](Different-key-types_21012305.html)
- [Permissions](Permissions_21012321.html)
- [Bridges](Bridges_21012327.html)
- [Use serde-json for deserialization of \`config.json\`](21012339.html)
- [Maintenance Endpoint](Maintenance-Endpoint_21012343.html)
- [Multisignature transactions](Multisignature-transactions_21012372.html)
- [Query Permissions Do Not Apply to Validators](Query-Permissions-Do-Not-Apply-to-Validators_21016423.html)
- [Block Synchronization](Block-Synchronization_21012390.html)
- [Cloud Events](Cloud-Events_21012424.html)
- [DEX Generic Scenarios](DEX-Generic-Scenarios_21012490.html)
- [Genesis Block and Network Setup](Genesis-Block-and-Network-Setup_21016904.html)
- [Triggers](Triggers_21012568.html)
- [Library usage for HTTP and WebSocket protocols](Library-usage-for-HTTP-and-WebSocket-protocols_21012656.html)
- [Modular Data Model](Modular-Data-Model_21012682.html)
- [Set of OOB ISIs](Set-of-OOB-ISIs_21012751.html)
- [Iroha crates naming for crates.io](Iroha-crates-naming-for-crates.io_21012808.html)
- [Change View Drawback in Sumeragi](Change-View-Drawback-in-Sumeragi_21012889.html)
- [Message Versioning](Message-Versioning_21012905.html)
- [Pluggable modules and actor model](Pluggable-modules-and-actor-model_21012952.html)
- [Scheme generation of model-objects](Scheme-generation-of-model-objects_21012972.html)
- [P2P network](P2P-network_21012982.html)
- [Scripting Languages and Runtimes for Iroha2 Smart Contracts](Scripting-Languages-and-Runtimes-for-Iroha2-Smart-Contracts_21013012.html)
- [Key-centric accounts structure](Key-centric-accounts-structure_21013242.html)

## Open questions

DescriptionDue dateAssigneeTask appears on

- Register or unregister DID in Account
  

[Set of OOB ISIs](/wiki/spaces/iroha/pages/21012751/Set+of+OOB+ISIs?focusedTaskId=227)

- Register or unregister VerifiableCredential in Account ([https://www.w3.org/TR/vc-data-model/](https://www.w3.org/TR/vc-data-model/))

[Set of OOB ISIs](/wiki/spaces/iroha/pages/21012751/Set+of+OOB+ISIs?focusedTaskId=228)

- Register or unregister TransactionFee (e.g., fixed, percentage, DEX-swapped)
  

[Set of OOB ISIs](/wiki/spaces/iroha/pages/21012751/Set+of+OOB+ISIs?focusedTaskId=225)

- Register or unregister LiquidityFee (e.g., buy back and burn, pool share, etc.)
  

[Set of OOB ISIs](/wiki/spaces/iroha/pages/21012751/Set+of+OOB+ISIs?focusedTaskId=226)

- Register or unregister DEX (DEXManager) in Domain

[Set of OOB ISIs](/wiki/spaces/iroha/pages/21012751/Set+of+OOB+ISIs?focusedTaskId=220)

- Register or unregister XYK Pool in DEX
  

[Set of OOB ISIs](/wiki/spaces/iroha/pages/21012751/Set+of+OOB+ISIs?focusedTaskId=221)

- Register or unregister Order Book in DEX

[Set of OOB ISIs](/wiki/spaces/iroha/pages/21012751/Set+of+OOB+ISIs?focusedTaskId=222)

- [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence)implement the maintenance endpoint with the selected libraries

[Egor Ivkov](/wiki/display/~5dd9631c1cf3c20ef5ff9f0f)[Library usage for HTTP and WebSocket protocols](/wiki/spaces/iroha/pages/21012656/Library+usage+for+HTTP+and+WebSocket+protocols?focusedTaskId=1)

- [武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) review solution

[武宮誠](/wiki/display/~557058%3A12c320e6-5d17-404f-b20e-bfa5721ae960)[DEX Generic Scenarios](/wiki/spaces/iroha/pages/21012490/DEX+Generic+Scenarios?focusedTaskId=8)

- When Peers send accepted transactions? **Right after acceptance** or each tick of Block Build Step

[Web API](/wiki/spaces/iroha/pages/21012259/Web+API?focusedTaskId=4)

- What is the difference between Block commit message handling and Block synchronization

[Web API](/wiki/spaces/iroha/pages/21012259/Web+API?focusedTaskId=5)

- How to update configuration which requires instance reloading (new address, etc)

[Web API](/wiki/spaces/iroha/pages/21012259/Web+API?focusedTaskId=6)

Document generated by Confluence on Nov 26, 2024 15:05

[Atlassian](http://www.atlassian.com/)
