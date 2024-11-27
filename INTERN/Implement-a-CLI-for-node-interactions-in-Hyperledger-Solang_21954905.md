1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : Implement a CLI for node interactions in Hyperledger Solang

Created by Cyrill Leutwiler, last modified by Min Yu on Dec 18, 2023

**Project Title**Implement a CLI for node interactions in Hyperledger Solang**Status**

COMPLETED

**Primary Focus**

CODING   

# Description

[Hyperledger Solang](https://github.com/hyperledger/solang) is a Solidity compiler written in Rust. It currently targets [Substrate](https://github.com/paritytech/substrate) [contracts pallet](https://github.com/paritytech/substrate/tree/master/frame/contracts) (Polkadot) and [Solana](https://github.com/solana-labs/solana) smart contract runtimes. After successful compilation, users need to upload the compiled contract artifacts to a blockchain node, so it can be interacted with. At the time of writing, this needs to be done manually via third-party web front-ends. Which results in an inefficient and tiring process during iterative contract development.

The goal of this mentorship is to implement a Command Line Interface (CLI) for Solang that can be used for node interactions instead. This includes uploading and deploying contracts on-chain as well as submitting transactions to contracts.

# Additional Information

We expect the Student to perform the following tasks:

- Gather requirements and outline a generic interface that will be usable for both supported targets (Substrate and Solana).
- Implement the CLI as a sub-commands for Solang.
  
  - For the Substrate target;  [cargo-contract](https://crates.io/crates/cargo-contract/) already provides a CLI for node interactions (Substrate target), however it does not yet support Solidity contracts.
  - For the Solana target
- Describe the CLI in Solang's [documentation](https://solang.readthedocs.io/en/latest/).

# Learning Objectives

By working on open source code bases, Students will learn and experience practical aspects of software engineering such as:

- Designing re-usable interfaces
- Analyzing and understanding code bases of reasonable sizes
- Refactoring existing components and implementing new features in Rust
- Contributing maintainable code to open source projects
- Getting proficient in working with tools like git

Additionally, students will learn about smart contracts, Substrate and Solana in general.

# Expected Outcome

- Solang provides a working and documented CLI for node interactions with Substrate and Solana. Options for sub-commands (like RPC end-point, account to use, dry-run flag, gas limits, verbosity and other specific options) must be configurable by the user.
  
  - A sub-command for uploading contracts.
  - A sub-command for instantiating contracts.
  - A sub-command for calling contract functions. This command must correctly encode transaction input, display and show the calls output and debug output as well as emitted events.
  - A sub-command for listening to emitted events.
- The student should factor the relevant parts of cargo-contract out into a dedicated library (crate) to make it usable in Solang.
- Developed source code is of adequate quality, merged in the projects upstream repositories and have undergone common Pull Request processes.

# Relation to Hyperledger

The Solang Solidity compiler is a Hyperledger project.

# Mentee Skills

We accept students from all educational levels with a background in computer science or a related field. We expect students to either be already familiar with Rust programming language basics such as [Understanding Ownership](https://doc.rust-lang.org/stable/book/ch04-00-understanding-ownership.html) and [Generics](https://doc.rust-lang.org/stable/book/ch10-00-generics.html), OR to demonstrate their ability and willingness to learn them in a timely manner.

Bringing any of the following skills is of advantage but not strictly required:

- Knowledge of blockchain technology and smart contracts
- Prior contributions to open source projects
- If no prior Rust experience, good knowledge of C++ is of advantage
- Basic knowledge of git

# Future plans

This feature is an important building block for integrations with common Solidity development tools like truffle or hardhat. Additionally, it will greatly improve the user experience of Solang. For Solidity developers, we expect it to become the default way of interacting with our target blockchain nodes.

# Mentor(s) Names and Contact Info

Mentor: Cyrill Leutwiler

Email: cyrill@parity.io

Discord: kägifret#8095

Please, join [the Solang channel on Discord](https://discord.gg/jhn4rkqNsT) for questions. This is the main means of communication we use in the project.

## Attachments:

![](images/icons/bullet_blue.gif) [\[Project plan\] LFX'23 Hyperledger - Implement a CLI for node interactions in Hyperledger Solang.pdf](attachments/21954905/21967755.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
