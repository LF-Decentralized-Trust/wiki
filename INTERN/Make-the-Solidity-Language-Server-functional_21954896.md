1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : Make the Solidity Language Server functional

Created by Sean Young, last modified by Min Yu on Dec 18, 2023

**Project Title**Make the Solidity Language Server functional**Status**

COMPLEED

**Primary Focus**

CODING    

# Description

A [language server](https://learn.microsoft.com/en-us/visualstudio/extensibility/language-server-protocol?view=vs-2022) is what makes it possible to rich editing like to go to definition or code completions in source code editors. The [Solang Solidity Compiler](https://github.com/hyperledger/solang) does have a [language server](https://solang.readthedocs.io/en/latest/extension.html), but it is very rudimentary. The aim of this mentorship is to make the language server much more complete, will make developing Solidity code using this language server will be a much greater developer experience.

During this mentorship you will learn how language servers work, and you'll need to walk the parsed Solidity abstract syntax tree in various ways to for example find where a variable is defined (Go to definition), or to find all usages of a variable (Find all references), or find the type definition (Go to type definition). This means walking a complex data structure, and understanding how source code is represented as a abstract syntax tree, which is the result of parsing and semantic analysis, the first stage of an compiler.

# Additional Information

General information on Language Servers and Solidity

- [https://learn.microsoft.com/en-us/visualstudio/extensibility/language-server-protocol?view=vs-2022](https://learn.microsoft.com/en-us/visualstudio/extensibility/language-server-protocol?view=vs-2022)
- [https://en.wikipedia.org/wiki/Solidity](https://en.wikipedia.org/wiki/Solidity)
- [https://en.wikipedia.org/wiki/Language\_Server\_Protocol](https://en.wikipedia.org/wiki/Language_Server_Protocol)
- [https://github.com/rust-lang/rls](https://github.com/rust-lang/rls) (rust language server)

About Hyperledger Solang:

- [https://github.com/hyperledger-labs/solang](https://github.com/hyperledger-labs/solang)
- The existing language server for VS Code: [https://solang.readthedocs.io/en/latest/extension.html](https://solang.readthedocs.io/en/latest/extension.html)
- The rust language server in solang: [https://github.com/hyperledger/solang/blob/main/src/bin/languageserver/mod.rs](https://github.com/hyperledger/solang/blob/main/src/bin/languageserver/mod.rs). This is the module where the bulk of the work should be done.

# Learning Objectives

- First and foremost the mentee will learn how to be a positive collaborator and contributor in an active open source project.
- Learn how to work within the Hyperledger open source ecosystem and culture.
- Understand smart contracts and the language Solidity language
- Increase understanding of compiler technology and development tooling

# Expected Outcome

Language server features to implement, and provide tests for:

#### Markdown formatting of hovers

When you hover over a variable, function, etc. you get some a hover with more information like the type. Currently the formatting is in plain text and quite ugly.

#### Do not require you to save the solidity file

In order for the language server to update with the latest text of the source file, you need to save the file. It would be much better if the language server updates as you type. Currently the language server reads the file, rather than using the source code which is sent to it over language server requests.

#### Drop diagnostics when closing solidity file with errors

When closing a file in VS code, all the warnings and errors remain in the list  
of problems. This should be fixed.

#### New feature: Go to definition

Go to where a variable, contract, event, function is defined.

#### New feature: Go to declaration

Go to where a function is declared (e.g. virtual) or its definition

#### New feature: Go to implementation

Go to where a function is defined (actual implementation, not virtual declaration).

#### New feature: Go to type defintion

Go to where the type of a variable is defined.

#### New feature: Go to/find all references

List all the instances where a contract, event, function, variable, etc is used.

#### New feature: Format code (using forge-fmt crate)

The forge-fmt crate can already format Solidity code. This crate should be imported and connected in the language server. Formatting has a few settings, that can be added in extensions settings.

#### New feature: Rename

Implement variable renaming. Using the same algorithm for find all references, replace the text in the source code with the new name. This should be done for variables, functions, and types.

#### New feature: code completion

Given a location in the code, determine which names are possible. For example, if the user has type \`block.\` then \`time\` and \`height\` are possible (amongst others).

# Relation to Hyperledger

This mentorship is for the Hyperledger Solang project.

# Mentee Skills

**Understanding of parsers and syntax tree**  
You will need to walk the syntax tree in various ways, so an understanding of this representation of source code is helpful.

**Some expose to Rust and TypeScript**  
The project is mostly written in rust, with some glue code in typescript. As Rust is a fairly new language, we don't expect you to know it, any other language will do.

# Mentee Open Source Contribution Experience

When applying for this mentorship, please provide:

- Please make a project plan for the mentorship. How will you approach the tasks, and in what order?
- Link to existing work (i.e. github profile) if available
- We will conduct a view interview (1 hour) and will ask some general coding questions

We are pretty active on [#solang Hyperledger discord](https://discord.gg/jhn4rkqNsT), please ask any question you have there.

# Future plans

The language server can be extended in many ways.

- We would like the language server to warn about Solidity constructs which are not optimal much like rust clippies
  
- Support all the features that language servers support
- Integrate the language server with other IDEs like neovim, helix, atom, etc

# Mentor(s) Names and Contact Info

Sean Young,

[sean@mess.org](mailto:sean@mess.org) 

github: [seanyoung](https://github.com/seanyoung/)

twitter/telegram: iamseanyoung

discord: @seanyoung [#solang on Hyperledger discord](https://discord.gg/jhn4rkqNsT)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
