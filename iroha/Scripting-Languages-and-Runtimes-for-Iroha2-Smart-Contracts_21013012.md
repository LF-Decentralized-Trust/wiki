1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Scripting Languages and Runtimes for Iroha2 Smart Contracts

Created by Egor Ivkov, last modified by Marin Versic on Dec 29, 2021

  Status

DECIDED 

Stakeholders[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) [Bogdan Mingela](https://lf-hyperledger.atlassian.net/wiki/people/5be3e71f26831505ca194c39?ref=confluence) [Pavel Golovkin](https://lf-hyperledger.atlassian.net/wiki/people/5f1e5ec88b83b700292a9e8e?ref=confluence)OutcomeWASM will be introduced into Iroha2Tasks[https://app.zenhub.com/workspaces/iroha-v2-60ddb820813b9100181fc060/issues/hyperledger/iroha/1425](https://app.zenhub.com/workspaces/iroha-v2-60ddb820813b9100181fc060/issues/hyperledger/iroha/1425)Due date

01 Sep 2021 

Owner

[Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence)

## Background

Currently we have Iroha Special Instructions and Expressions as a main smart contract language. Later we will call both Instructions and Expressions simply ISI.

1. Instructions - mutate global state (domains and other entities) in WSV
2. Expressions - do not mutate state (are more like mathematical calculations) and can also incorporate queries to WSV
3. Instructions can use complex input parameters in a form of Expressions.

Scripts written in ISI can be executed in 2 places:

1. As part of the transaction that user submits
2. Inside a trigger that is registered and executed on chain based on some events (see Trigger RFC) - not developed yet

## Problem

Current state of ISI has several important limitations preventing it from being a fully usable smart contract language:

1. Different instruction and expressions might operate on complex values (like structs, enums), but they do not have an ability to destructure/access inner fields/variants of this complex values.
2. ISI do not have an std lib to operate Vec(s), String(s), etc.
3. In ISI it is not possible to define new structures, objects, closures, functions, modules etc. which is needed to write big programs
4. ISI can not be written in text
5. ISI do not have loops or recursion (needed for most of the programs)
6. They do not manage memory in any way

Given time all this can be solved and ISI can be turned into a fully interpreted language or compiled (JIT/or precompiled) language with a VM and assembly set. But this will take a lot of time as any language and compiler/interpreter development does and would require the team to dive heavily into this mostly new area of expertise. I would estimate about 6 month for 1 full time developer before we have a tangible prototype.

Also ISI as they are have several good important features:

1. They are relatively simple to understand and support
2. They can be easily permissioned
3. They can provide both low level and high level high performance native features

Therefore let's get to suggested solution.

## Solution

It is suggested to proceed in the following way:

1. Keep ISI runtime:
   
   1. For simple use cases
   2. For high level features provided by Iroha natively
2. Add some other established interpreter/VM with existing scripting language such as (WASM, eBPF, Lua, Rhai)
3. Let the ISI calls be the interface between this full scripting language and our WSV (scripts will call ISI and queries to change and get information from WSV) - for universality of common interface and easy permission management

Preliminarily it is suggested to use Rust with WASM target with [wasmtime](https://github.com/bytecodealliance/wasmtime) runtime.

### Decisions

### Alternatives

Here the list of possible alternative runtimes and languages is listed with their pros and cons:

#### Rust - WASM

Language: Rust

Assembly: WASM

Runtime: [wasmtime](https://github.com/bytecodealliance/wasmtime)

Prototype: [https://github.com/soramitsu/iroha2-wasm-prototype](https://github.com/soramitsu/iroha2-wasm-prototype)

proscons

1. Well known and established in Blockchain space (Polkadot, Kusama, other Substrate based networks)
2. Well known and developing fast in web programming space
3. Officially supported by Rust compiler as a target
4. Rust core team is contributing to wasmtime
5. It might be required for bridging Substrate based networks
6. We have experience in it within our team and teams closely working to us
7. Developed by wide community
8. Execution can be easily limited with \`fuel\` (approximate of number of assembly instructions that any script is allowed to execute at most)

<!--THE END-->

1. Requires nightly* for the smart contracts themselves
2. Difficult to limit memory further than 3GB in wasmtime (needs more research)
3. No Interface Types Support - so it has to be simulated through passing serialized bytes or mapping memory

\*- Nightly Rust means that some of it its features are unstable and may be removed or changed in the later versions of the language.

#### Rust - eBPF

Language: Rust

Assembly: eBPF

Runtime: [solana\_rbpf](https://crates.io/crates/solana_rbpf) [rbpf](https://github.com/qmonnet/rbpf)

proscons

1. Might be faster than alternatives
2. Simple low level instruction set (simpler than wasm)
3. More mature than wasm and battle tested in linux kernel and in other blockchains
4. Developed by wide community
5. Officially supported by [rust team](https://github.com/rust-lang/rust/pull/79608)
6. Has static analyzers and it is possible to easily make specific one
7. Execution can be easily limited with \`fuel\` (approximate of number of assembly instructions that any script is allowed to execute at most)

<!--THE END-->

1. Runtime for Rust is supported only by one specific blockchain company

Needs more research

#### Lua

Language: [Lua](https://www.lua.org/)

Runtime: [rlua](https://github.com/amethyst/rlua)

proscons

1. Well established as scripting language for game engines and many other tools
2. easily embedded

<!--THE END-->

1. has gc and would be slower than alternatives

Needs more research

**Rhai**

Language: [Rhai](https://rhai.rs/book/)

Runtime: [custom](https://rhai.rs/book/)

proscons

1. Minimalist
2. Easy interoperability with Rust types at the first glance
3. Looks similar to Rust but simpler
4. Interpretable (no jit)

<!--THE END-->

1. Developed by small community

Needs more research if deemed necessary

### Concerns

Other projects developing on Iroha2 might strongly depend on this decision.

### Assumptions

Projects developing on Iroha2 need a more robust scripting language

### Risks

## Additional Information

Useful links:  
[https://www.w3.org/TR/wasm-core-1/#control-instructions%E2%91%A0](https://www.w3.org/TR/wasm-core-1/#control-instructions%E2%91%A0)  
[https://learnxinyminutes.com/docs/wasm/](https://learnxinyminutes.com/docs/wasm/)  
[https://blog.dbrgn.ch/2019/12/24/testing-for-no-std-compatibility/](https://blog.dbrgn.ch/2019/12/24/testing-for-no-std-compatibility/)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
