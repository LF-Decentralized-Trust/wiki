1. [Hyperledger Solang](index.html)

# ![Home Page](images/icons/contenttypes/home_page_16.png) Hyperledger Solang : Hyperledger Solang

Created by Sean Bohan, last modified by Ry Jones on Apr 23, 2024

**Project**

**Status**

[INCUBATION](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Project+Lifecycle#ProjectLifecycle-incubation) [ACTIVE](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Project+Lifecycle#ProjectLifecycle-active)

**CII Badge**

[![](https://img.shields.io/badge/cii%20best%20practices-not%20started-red.svg)](https://bestpractices.coreinfrastructure.org/projects/new)

**Description**Solang is a portable compiler for the Solidity language that targets Solana and Substrate (Polkadot). It is written in Rust, and leverages the LLVM infrastructure for the compiler backend.

![](plugins/servlet/confluence/placeholder/unknown-macro)

The Solidity language is the [most popular programming language for smart contracts](https://101blockchains.com/smart-contract-programming-languages/). However, the existing Solidity compiler only targets the Ethereum virtual machine. The Solang project aims to make Solidity available for other blockchains, and focuses on maintaining source code compatibility with Solc, so that developers can use their existing codebase for blockchains other than Ethereum with minimal modifications.

The purpose of Solang is two-fold: first of all, developers with Solidity language knowledge can develop new smart contracts for non-ethereum blockchains in Solidity, so they do not have to learn a new language. Secondly, there is a large amount of existing Solidity contracts available, which can be recompiled for a different blockchain.

Currently, Solang targets the following blockchains:

\- [Solana](https://solana.com)  
\- [Substrate](https://substrate.io)

At the time of writing, these chains are the 9th, and 11th by market capitalization according [coinmarketcap.com](https://coinmarketcap.com/) (the coins are listed by market cap).

Any other blockchain that wishes to have Solidity language support is welcome to add a new target to the Solang project. The cosmos blockchain [grant foundation](https://interchain.io/) has said it would [support a grant for adding CosmWasm support](https://github.com/hyperledger-labs/Solang/issues/582).

The goal of Solang is to bring the Solidity language to as many blockchains as possible. Writing a production quality compiler is a complex task, so collaboration between blockchains will be hugely beneficial.

The success of the project can be measured by the number of projects that use Solang as a compiler.

Key Characteristics

Hyperledger Solang is a compiler: it knows how to transform Solidity source code into a binary program (or contract) which can be directly deployed on a blockchain. Hyperledger Solang does not provide tooling for this, however we do provide documentation on how to deploy and interact with your Solidity contracts, see the block-chain specific documentation below.

Hyperledger Solang has the following stages:

1. Parser stage. This parser Solidity. This is in the \`solang-parser\` crate. This crate is used by another project: foundry uses it for its Solidity code formatter.
2. Semantic Analysis Stage (sema). This validates that the source code is valid, and produces the AST. This is used by the Language Server.
3. Code generation (codegen). This transforms the AST into a CFG (control flow graph). This deals with contract inheritance too, and includes a few code optimization passes.
4. LLVM IR emit (emit). This transforms the CFG into LLVM IR.
5. LLVM Backend. The LLVM Libraries further optimize and compile the code into optimized binary files
6. LLD Linker. The LLVM Linker produces the final file.

# Documentation

[https://Solang.readthedocs.io/en/latest/](https://Solang.readthedocs.io/en/latest/)

How to run Solang on command line: [https://Solang.readthedocs.io/en/latest/running.html](https://Solang.readthedocs.io/en/latest/running.html)

Blockchain-specific instructions for:

Solana: [https://solang.readthedocs.io/en/latest/targets/solana.html](https://solang.readthedocs.io/en/latest/targets/solana.html)

Substrate: [https://solang.readthedocs.io/en/latest/targets/substrate.html](https://solang.readthedocs.io/en/latest/targets/substrate.html)

# Project Management and Issue Tracking

All Solang projects use GitHub for receiving issues, receiving pull requests and tracking releases.  The links to the GitHub repos for the project are below.

# Repositories

[https://github.com/hyperledger/solang](https://github.com/hyperledger/solang)

[https://github.com/hyperledger/homebrew-solang](https://github.com/hyperledger/homebrew-solang)

# Communication

## Mailing List

- [https://lists.hyperledger.org/g/solang](https://lists.hyperledger.org/g/solang)
  
  - [subscribe](https://lists.hyperledger.org/g/solang)
  - [messages](https://lists.hyperledger.org/g/solang/topics)

## Chat (for questions and ephemeral discussions)

Questions are welcome and best asked in Hyperledger Discord.  

[Learn more about Hyperledger Discord here](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Our+chat+service), get the invite and check out one of the many Aries project channels.  

# Meeting

People who want to learn about or contribute to Solang should join this call. This does not replace our asynchronous collaboration, but should help us keep everyone up-to-date and moving together.

Discussion items: upcoming releases, current PRs, work that will generate future PRs, architecture changes that will impact downstream teams, project standards, best practices, design, etc.

# Calendar

- [Hyperledger Calendar of Public Meetings](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Calendar+of+Public+Meetings)

# History

- [Proposed](https://github.com/hyperledger/hyperledger-hip/pull/6) by
  
  - Sean Young
  - Lucas Steuernagel
  - Tracy A. Kuhrt
  - Cyrill Leutwiler
- [Approved](https://lf-hyperledger.atlassian.net/wiki/display/TSC/2022+08+18+TSC+Meeting+Record)  by the TSC on 2022 -08-18

# Getting Involved

You are invited to get involved with the Solang project.  Here are some ways you can get started.

1. Join our team calls! We have a daily stand up meeting in [discord](https://discord.gg/nPGHEs4W).
2. [File us an issue report or pull request](https://solang.readthedocs.io/en/latest/contributing.html).
3. Join communication channels and introduce yourself and ask questions (details below)
4. Grab a good first issue based on your level of experience/technical area(s) of expertise or interests:
   
   1. [All](https://github.com/hyperledger/solang/issues?q=is%3Aissue%20is%3Aopen%20label%3A%22good%20first%20issue%22) [Good First Issues](https://github.com/hyperledger/solang/labels/good%20first%20issue)

# Communication

## Mailing List

- [solang@lists.hyperledger.org](mailto:solang@lists.hyperledger.org)
  
  - [subscribe](https://lists.hyperledger.org/g/solang)
  - [messages](https://lists.hyperledger.org/g/solang/topics)

## Chat (for questions and ephemeral discussions)

Questions are welcome and best asked in Hyperledger Discord.  [Learn more about Hyperledger Discord here](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Our+chat+service), get the invite and check out one of the many Cactus project channels.  

# Daily Meetings

Every day at 13:30 UTC we meet to discuss the project. Everyone is welcome.

[https://lists.hyperledger.org/g/solang/calendar](https://lists.hyperledger.org/g/solang/calendar)

[Calendar of Public Meetings](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595324/Calendar+of+Public+Meetings)

## Recent space activity

- [![](null/aa-avatar/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850 "557058:078cecfc-fb17-4d9a-8759-b5b74efa6850")](null/display/~557058%3A078cecfc-fb17-4d9a-8759-b5b74efa6850)
  
  - [Ry Jones](null/display/~557058%3A078cecfc-fb17-4d9a-8759-b5b74efa6850)
  - [Hyperledger Solang](index.html "Hyperledger Solang") contributed Apr 23, 2024

## Space contributors

- [Ry Jones](/wiki/display/~557058%3A078cecfc-fb17-4d9a-8759-b5b74efa6850) (217 days ago)
- [David Boswell](/wiki/display/~70121%3A0a14f738-3039-421f-a6a9-a83d19f23227) (782 days ago)
- [Sean Bohan](/wiki/display/~634eef0301c2ff842c15f9e7) (789 days ago)
- [Lucas Steuernagel](/wiki/display/~557058%3A462f99e6-acdc-4274-9a05-1769aebe0ee8) (794 days ago)
- [Sean Young](/wiki/display/~5cc8a4189e366e0e6582a2da) (796 days ago)
- [...](# "1 more...")
- [Cyrill Leutwiler](/wiki/display/~712020%3Ab4ef5b56-3c64-47ce-a71d-474106046847) (796 days ago)

## Attachments:

![](images/icons/bullet_blue.gif) [hl\_solang\_horizontal-color.png](attachments/20545558/20560784.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Solang.png](attachments/20545558/20560790.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Solang.svg](attachments/20545558/20560792.svg) (image/svg+xml)

Document generated by Confluence on Nov 26, 2024 15:04

[Atlassian](http://www.atlassian.com/)
