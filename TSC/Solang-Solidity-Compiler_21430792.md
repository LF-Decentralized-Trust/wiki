1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Archived](Archived_21447696.html)
4. [Project Proposals](Project-Proposals_21430788.html)
5. [2020 Finished Proposals](2020-Finished-Proposals_21430790.html)

# Technical Oversight Committee : Solang Solidity Compiler

Created by Sean Young, last modified by Gari Singh on Jun 11, 2020

# Project Identifier

Solang, currently at version 0.1.0.

# Sponsor(s)

- Shawn Amundson &lt;amundson@[bitwise.io](http://bitwise.io)&gt;
- Silas Davis &lt;silas@monax.io&gt;
- Greg Hill &lt;greg.hill@[monax.io](http://monax.io)&gt;
- Sean Young &lt;sean@mess.org&gt;

# Abstract

Solang is a compiler for the Solidity language that can target ewasm (used by Hyperledger Burrow, future ethereum and others), Sawtooth Sabre, and Parity Substrate. It is written in rust and uses LLVM as the compiler backend. The aim is for full compatibility with the Solidity language where possible .

Once a compiler is written, other tooling can be written that depends on having compiler components available. Just like llvm is a *compiler toolkit,* Solang wants to be a *Solidity toolkit*. Linters, analysis tools, language servers, debuggers etc can be written by reusing the parsing/resolving phases of Solang.

# Context

Solidity as a language does have its quirks, however it has established itself as a defacto language commonly used for smart contracts. Having Solidity support for the Hyperledger ledgers would be a great feature, conversely it would be beneficial for those projects to collaborate on a common compiler component.

# Dependent Projects

Solang does not depend on any other project.

# Motivation

The Ethereum Foundation has a Solidity compiler, which is a large C++ code base.  It contains a handwritten Solidity parser, and code optimizer. It can only target EVM on Ethereum. In the first instance, Solang is a new implementation of a Solidity compiler with modern tooling: written in rust, generated parser, targeting wasm, and using llvm for code gen. This makes the code base much smaller and makes it possible to compile Solidity for a range of ledger projects.

Once this is done, a range of new further tooling can built on top of this:

- Improving the Solidity language itself, e.g. string processing or generics
- Implement a Solidity Language Server for IDEs, see [Create a new Solidity Language Server (SLS) using Solang Compiler](https://lf-hyperledger.atlassian.net/wiki/spaces/INTERN/pages/21954700/Create+a+new+Solidity+Language+Server+SLS+using+Solang+Compiler)
- Integer overflow detection in Solidity
- Link C code to Solidity using the LLVM Linker-as-a-library
- Implement Solidity linter/style hints like rust clippy
- Implement Solidity debug builds and debugger (using llvm debug codegen)
- Static analysis tools
- Formal methods
- Generate EVM code using experimental evm llvm backend

# Status

Solang would move into incubation, if approved.

# Solution

Solang does not have complete language support yet. The language features which are supported are clearly documented. See: [https://solang.readthedocs.io/](https://solang.readthedocs.io/)

Solang tries to be a traditional compiler

1. lexer
2. parser (outputs: AST)
3. resolver: (outputs: CFG)
4. code emitter (output: LLVM IR)
5. llvm wasm codegen
6. linker

The layout of the source code is as follows:

### src/parse/*

lexer and LALRPOP Solidity grammer

output: Abstract Syntax Tree

### src/resolve/*

Resolves types, variables, functions etc

Generates control flow graph

### src/emit/*

Converts Control Flow graph to LLVM IR

Has to do some tricks to generate PHI nodes

ABI encoder/decoder (eth/scale)

### src/link.rs

Converts wasm object file to final wasm file

### src/abi/*

Generates and reads ABIs

# Efforts and Resources

This project is funded through a Web3 Foundation grant. In order to receive the grant, the project commits to a roadmap.  This roadmap means Solang will have full Solidity language support in fall 2020.

# How To

The source code is hosted on github: [https://github.com/hyperledger-labs/solang](https://github.com/hyperledger-labs/solang) . Solang can compile Solidity for use with Hyperledger Burrow, and Hyperledger Sawtooth. How this can be done is documented: [https://solang.readthedocs.io/en/latest/running.html](https://solang.readthedocs.io/en/latest/running.html)

# References

# Closure

The aim is to provide great tooling for Solidity developers, whatever ledger they are using.  If developers start using our tooling, then we are succeeding.

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Christopher Ferris](https://lf-hyperledger.atlassian.net/wiki/people/5abb903a8724022aa9070581?ref=confluence)
- [Dan Middleton](https://lf-hyperledger.atlassian.net/wiki/people/712020:2979764a-3998-4ef1-8810-60b799067924?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Swetha Repakula](https://lf-hyperledger.atlassian.net/wiki/people/712020:7153872d-7890-4ca8-a633-d87fdf1e9a8d?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:62746046-52ae-43bb-827b-6dfdde9f07d7?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:24

[Atlassian](http://www.atlassian.com/)
