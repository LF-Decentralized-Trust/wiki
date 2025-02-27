1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : Implement an SSA intermediate representation for the Solang compiler

Created by Lucas Steuernagel, last modified by Min Yu on Feb 02, 2024

**Project Title**Implement an SSA intermediate representation for the Solang compiler**Status**

INCOMPLETE

**Primary Focus**

CODING    

# Description

Solang is an open-source Solidity compiler written in Rust. It generates an intermediate representation in a Control Flow Graph (CFG) for each function in a Solidity contract during compilation. The CFG contains high level expressions and instructions, which help in some aspects of code analysis and optimization, but are not suitable for more advanced optimization passes, such as liveness analysis and partial redundancy elimination.

In this project, mentees will have hands-on experience implementing a modern Single Static Assignment intermediate representation for the Solang compiler. This addition will bring many advantages for the compiler, such as the possibility to break down complex constructs into lower level instructions and the facilitation of code analysis. We propose for the mentorship the introduction of a new intermediate representation to live between the existing one (the CFG representation - read more about it at the Additional Information section below) and the LLVM-IR. It should feature three-address code in a Single Static Assignment (SSA) minimal form. The construction of such a form happens in two steps:

1. Phi function insertion
2. Variable renaming

The objective is to decouple the types and expressions we have used for the AST from the existing CFG intermediate representation. In addition, the new low level intermediate code must contain assertions that ensure the instructions are created with valid operands and expressions.

# Additional Information

The compilation pipeline for the Solang compiler consists of five steps:

1. Parse the source code and build a parse tree.
2. Run semantic analysis and build an Abstract Syntax Tree (AST)
3. Build an intermediate code representation based on a control flow graph (CFG) from the AST to perform code optimizations.
4. Generate LLVM-IR from our CFG representation.
5. The LLVM backend transforms LLVM-IR into an executable binary.

Solang repostory: [https://github.com/hyperledger/solang](https://github.com/hyperledger/solang)

Solang documentation: [https://solang.readthedocs.io/en/latest/](https://solang.readthedocs.io/en/latest/)

# Learning Objectives

We expect the mentees to acquire a deeper understanding in compilers, specifically code generation. In addition, developing the ability to analyze the trade offs between different approaches to problems is a highly valuable lesson to be learnt. Lastly, as the mentorship involves creating a new intermediate representation for Solang, the mentee should be able to understand at the end of the program LLVM-IR and static single assignment techniques.

# Expected Outcome

 For the context of the mentorship, we propose the following tasks:

1. Design a new intermediate representation and document it.
2. Devise a builder interface that makes the creation of the representation convenient, documenting it alongside task #1.
3. Implement it in the code base so that it becomes part of the compilation pipeline.
4. Implement SSA form validations to ensure the code is correctly generated.

We'll provide the mentee with references for any necessary algorithms for SSA construction. The third task is the largest one, so most of the time should be reserved for it.

# Relation to Hyperledger

The Solang Solidity compiler is a Hyperledger project.

# Mentee Skills

We accept mentees from all educational levels, provided that they have a background in compiler construction, either through university classes, online courses, personal projects or previous contributions to open-source compilers. Basic knowledge of Rust, common data structures and algorithms is desirable. Willingness to learn new concepts will help mentees succeed in the program.

# Future plans

The addition of a new code representation in the Solang compiler is essential for us to create newer compiler optimizations and generate more efficient binaries. Future plans, thus, include leveraging the new representation to implement liveness analysis for dead code elimination and partial redundancy elimination.

# Mentor(s) Names and Contact Info

Mentor: Lucas Steuernagel

Email: [lucas.tnagel@gmail.com](mailto:lucas.tnagel@gmail.com)

Discord: LucasSte#2331

Please, join [the Solang channel on Discord](https://discord.gg/jhn4rkqNsT) for questions. This is the main means of communication we use in the project.

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
