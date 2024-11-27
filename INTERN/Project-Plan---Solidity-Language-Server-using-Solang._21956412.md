1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2020 Projects](2020-Projects_21963347.html)
5. [Create a new Solidity Language Server (SLS) using Solang Compiler](21954700.html)

# Hyperledger Mentorship Program : Project Plan - Solidity Language Server using Solang.

Created by Shivam Balikondwar, last modified on Nov 19, 2020

## **Abstract**

Solang is the compiler for the Solidity language which is used to write smart contracts for fabric and ethereum. A Language server for Solidity language is developed that can help the developers with providing proper code compilation messages along with features like diagnostics, syntax coloring and hovers.

## **Mentor and Mentee**

Mentor: Sean Young 

Timezone: UK

Rocketchat(Hyperledger): seanyoung

Mentee: Shivam Balikondwar

Timezone: IST

Rocketchat(Hyperledger): sbalikondwar

Mail: [cha0sk1ng101010@gmail.com](mailto:cha0sk1ng101010@gmail.com)

Communication channel: Jitsi + Rocketchat + Github

**Project repo:** [https://github.com/hyperledger-labs/solang-vscode](https://github.com/hyperledger-labs/solang-vscode)

## **Deliverables**

- VScode extension that can be used to use the implementation.
- Language Server for Solidity.
- Tests for the implementation.
- Documentation of the Language Server.

## **Milestones**

**Eval 1:**

- VScode extension(basic functionality) + Syntax highlighting.
- Implemented Rust server to receive and send JSON-RPC responses from VScode client.

**Eval 2:**

- Diagnostics for compiler warnings, errors and hints.
- Tests and Documentation implemented for same.

**Eval 3:**

- Basic hover implementation for variable types.
- Tests and Documentation implemented for same.

**Eval 4:**

- Extending hover implementation for function, struct, enum, events, built-ins documentation lookups.
- Test and Documentation implemented for same.

## **Timeline**

WeekTask/PlanStatus**May 25 - May 29**Mentee intro with the mentor. I already communicated with the mentor(Sean)  Done**June 1 - June 14**Implement basic functionality of VScode extension. Syntax highlighting of Solidity language. Done**June 15 - June 28** Rust server for receiving the incoming requests from VScode clients.Done**June 29 - July 5** Buffer period to complete the remaining work and co-op with difficulties during implementation.Done**July 6 - July 12**

Complete tests and documentation of the Rust server impl.

Eval on July 10: Provide reports for first quarter to the program organisers.

Done

Eval completed

**July 13 - July 26**Work on implementing diagnostics. Prepare the backend to process incoming code.Done**July 27 - August 9**Work on diagnostics, fixing Range issues and fixing minor bugs.Done**August 10 - August 16**Buffer period to complete the remaining work and co-op with difficulties during implementation.Done**August 17 - August 23**

Complete tests and documentation of the diagnostics implementation.

Eval on August 21: Provide reports for the second quarter to the program organisers.

Done

Eval completed

**August 24 - Sept 6**Work on the hover feature. List out all possible grammar definitions and start implementing.Done**Sept 7 - Sept 20**Follow up on the work.Done**Sept 21 - 27**

Finished the basics of hover implementation. Added hover for variable definition and types.

Done**Sept 28 - Oct 4**

Complete tests and documentation of the implementation.

Eval on Oct 2: Provide reports for third quarter to the program organisers.

Done

Eval completed

**Oct 5 - Oct 18**

Week1: Work on adding support for Function + Return-type + Function params hover.

Week2: Work on adding support for Emit token in hover.

Done**Oct 19 - Nov 1**

Week1: Work on adding support for struct entries in hover.

Week2: Buffer period to follow up on the work.

Done**Nov 2 - Nov 8** Used this week to work on hover implementation.Done**Nov 9 - Nov 13**

Time to complete remaining details and documentation.

Done

Eval completed

## **Explanation**

A language server is a program that communicates with the editor to provide different editing features for a programmer. The communication takes place in the form of IO buffers and JSON-RPC messages.

The client(extension) uses VScode API's to send queries in JSON-RPC format to the server. The server runs different processes(like file open, edit, hover) which respond to specific requests from client.

For Diagnostics info the server watches for changes in the file and compiles the edited code using Solang, the compiler info for the respective code is then formatted and returned back to the server as compiler errors, warnings and hints.

For Hovers the server first traverses the AST(syntax tree) resolved by the Solang compiler on the edited code. While traversing it creates a map containing line, column and messages for the respective tokens from the AST. This map is then used to map cursor positions on the client side(line, column) to return the respective hovers. Eg: If on client side the mouse is hovered over a variable 'a' of type uint256 at line no 10 and column 10. The server will look into the map and check for entries that are defined for line 10 and column 10. For variable 'a' the map has message 'uint256 a' which is then returned to the client.

The process flow of the same is shown below:

![](attachments/21956412/21963764.png?width=700)

## **Methodology**

I followed the **“Design-Code-Test-Document​”** methodology.

My first step while developing any software is to **design** the **process** **flow** by **understanding** its **inner** **workings**. During the initial mentorship, I along with my mentor did some planning of the implementation and set important milestones for same as represented in the **schedule** for the work(given above) for the **respective** **feature**. Once I develop each feature, I wrote **tests** for the implementation to make sure whatever I wrote is working **correctly**. At the end of the **tests**, I **documented** its implementation. I used​ **GIT​** for **version** **control** with **reviews** taking place on Github(Repo: [https://github.com/hyperledger-labs/solang-vscode](https://github.com/hyperledger-labs/solang-vscode)).

I believe in constantly **sharing** my progress with the **mentor** and the **community**, a **​weekly​** **update** regarding my work is shared with mentor as a weekly meet. The VScode extension uses typescript for client side scripting and the server side implementation is in Rust.

The work has been interesting and I happy that me and my mentor have established good communication throughout the mentorship. You can usually find me discussing the project related queries on the solang channel of Hyperledger Rocketchat.

## Attachments:

![](images/icons/bullet_blue.gif) [sls\_conf.png](attachments/21956412/21963764.png) (image/png)

Document generated by Confluence on Nov 26, 2024 14:59

[Atlassian](http://www.atlassian.com/)
