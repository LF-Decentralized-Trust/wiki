1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Iroha Special Instructions DSL

Created by Vadim Reutskiy, last modified by Nikita Puzankov on Aug 13, 2020

Status

DECIDED

Stakeholders

 [武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) [Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence)

Outcome

Error rendering macro 'jira' : null

Error rendering macro 'jira' : null

Due date

14 Aug 2020

Owner

[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence)

## Background

Smart contracts have the potential to automate business processes and create logic that can be executed without human interaction. This can be useful for minimizing trust and creating truly decentralized applications.

In Iroha v1 a finite set of commands was provided, but they were inflexible and Turing complete computation was not possible. To increase the usefulness of Iroha, in v2 we allow full, Turing complete computation, while still making common tasks easy by providing Iroha Special Instructions (ISI).

In other blockchain platforms, complex smart contract features exist, for example Ethereum Solidity. However, the style of creating a contract, deploying it, and then sending tokens, etc., to the contract to interact with it seems to not only have a lot of overhead, but is itself quite prone to mistakes and attacks. In Iroha we take the approach where we use a simple data model consisting of domains, accounts, and assets, which then can go through various interactions to change their properties. In this way, if someone wants to create some logic involving an asset, for example, an Event trigger can be put on transactions for the asset that matches certain parameters and instructions can be executed on the asset. In this way, ISI works more like database triggers than deployed smart contracts, as in Ethereum.

[https://github.com/hyperledger/iroha/blob/iroha2-wp/iroha\_2\_whitepaper.md](https://github.com/hyperledger/iroha/blob/iroha2-wp/iroha_2_whitepaper.md)

## Problem

Iroha Special Instructions should provide safe, fast and user-friendly way to make development of custom and basic smart contracts easier with Turing complete computations supported in it.

- Simple usage
- Compile time safety and checks if possible
- Turing Completeness

## Solution

Iroha 2.0 will provide Iroha Special Instructions and Domain Specific Language for their description.

Iroha Special Instructions with all possible actions provided out-of-the-box with an ability to compose them and combine them with Triggers to create "custom" Iroha Special Instructions.

Good example of simple to use yet powerful DSL is [Scratch](https://scratch.mit.edu/). It has events (start, key\_pressed, etc.), control (repeat, if, etc.),  actions (move, sound, etc.) types of blocks with possibility to combine them.

We can give several types of out-of-the-box Iroha Special Instructions and gave an ability to combine them.

### Decisions

Iroha Special Instructions will have actions which can be applied to different domain entities:

- Register/Unregister (account or asset definition in a domain)
- Add/Remove (signatory to or from an account, trigger to the peer, domain to the peer, trusted peer to the peer)
- Transfer (asset from one account to another)
- Mint/Demint (asset quantity)

Iroha Special Instructions placed as triggers can listen to changes in the system:

- OnBlockCreated
- OnBlockchainHeight
- OnWorldStateViewChange
- OnTimestamp

Computational operations:

- Add
- Subtract
- Multiply
- Divide
- RaiseTo
- Mod

[Permissions](Permissions_21012321.html) checks:

- Can...

Read only operations with World State View:

- Execute(IrohaQuery)

Composable types:

- Pair(Instruction1, Instruction2)
- Sequence(Vec&lt;Instruction&gt;)
- If(Condition&lt;Instruction&gt;, Then&lt;Instruction&gt;, Else&lt;Option&lt;Instruction&gt;&gt;)

Custom Iroha Special Instructions can be build using composition of out-of-the-box Instructions:

- Swap - \`Pair(Transfer(A→B), Transfer(B→A))
- [Exchange](DEX-Generic-Scenarios_21012490.html)
- etc.

Execution of Iroha Special Instruction can be successful or can fail. If it was successful it may return changed World State View and return \`Output\` as a value. 

Different Iroha Special Instructions can obtain different arguments and return different Outputs. Type of Iroha Special Instruction inputs and output defines possible compositions of Iroha Special Instructions.

For example we can mint \`u32\` quantity of some asset, so we have two arguments (\`u32\`, \`AssetId\`) for \`Mint\` Iroha Special Instruction. Instead of *hardcoding* quantity value we can place \`Execute\` Iroha Special Instruction and get it's result in \`Mint\`:

```
Mint(ExecuteQuery(dex::query::getExchangeRate), asset_id)
```

### Alternatives

#### Smart Contract Runtime with direct API to World State View

Another solution that can be used here is to provide Iroha clients with direct access to World State View API and store all Iroha Special Instructions (out-of-the-box and custom) as WA artifacts.

Pros:

- High degree of customization
- Low-level control over execution (programming language control mechanism like loops, mathematical operators, conditions, etc.)
- Extensibility - new Iroha Special Instructions will not depend on existing ones by any measure

Cons:

- High level of security risks - direct usage of low-level API (World State View) may give hackers a possibility to execute malicious scenarios
- Direct dependency on WASM runtime - we make it a part of our public API without possibility to optimize it and tune a lot
- Low control over custom Iroha Special Instructions - harder to check permissions and more strict requirements to custom Iroha Special Instructions review process
- Wide spread of client side tools and technologies - with an ability to use low-level API it will be harder to develop and maintain client-side tools, like explorers

### Concerns

- Set of out-of-the-box instructions should be well-defined, it's also good to have an ability to add new OOB instructions with new versions of Iroha if needed
- Mechanism of arguments passing should be made as close to compile time as possible to prevent runtime errors in custom instructions

### Assumptions

- We value simplicity and security over low-level control and customization (extensibility)
- Any Iroha fork can deal with own set of out-of-the-box Iroha Special Instructions if all peers in their ledger will run this fork
- Iroha Special Instructions domain specific language will be client oriented with less user-friendly "backend"

### Risks

- Solution will not meet requirements of Iroha modules and 3rd party applications \`\[2;7]\`
- Performance of initial version will be slow \`\[7;7]\`
- We will need to extend set of out-of-the-box instructions soon \`\[5;5]\`

## Additional Information

### Resources

Code blocks visualization:

- [https://github.com/LLK/scratch-www](https://github.com/LLK/scratch-www)
- [https://github.com/LLK/scratch-blocks](https://github.com/LLK/scratch-blocks)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
