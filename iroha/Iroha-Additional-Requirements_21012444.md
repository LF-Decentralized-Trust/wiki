1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Requests for Comments](Requests-for-Comments_21016001.html)
5. [zzz\_\[ARCHIVE\]](21016320.html)

# Hyperledger Iroha : Iroha Additional Requirements

Created by Nikita Puzankov, last modified on Jul 13, 2020

## Abstract

Based on [Yuriy Vinogradov](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b85dbf9-2cc9-4bee-a3a0-2815e5bb51eb?ref=confluence)requirements:

> 1. We want ability to have turing complete functions with own protected storage.  
2\. We want that we can control interfaces to access to this functions. Now looks like it is possible to call internal functions of the complex ISI/  
3\. There are not enough abilities for ISI to work with storage(parse, verify data...)  
5\. JS client library.  
6\. We want an easy understandable framework to send arguments from one ISI to another.  
Now there is a proposal about sharing arguments through Assets, but it has many questions. how ISI will know from which asset to get data? How ISI will know how to parse it? How to validate?.... So, dedicated solution might be more clear that try to use assets for everything.  
7\. We need math in ISI for DEX logic if we want to implement it thorough complex ISI&gt;  
8\. We want Cycles in ISI.

RequirementTarget ReleaseAlready addressed in[Turing complete functions](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Iroha+Additional+Requirements#IrohaAdditionalRequirements-TuringCompleteFunctions)

[Whitepaper](https://github.com/hyperledger/iroha/blob/iroha2-dev/iroha_2_whitepaper.md#251-event-listeners)

[Use cases](Use-cases_21016413.html)

[Protected Storage](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Iroha+Additional+Requirements#IrohaAdditionalRequirements-ProtectedStorage)

[Data related ISI](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Iroha+Additional+Requirements#IrohaAdditionalRequirements-DataRelatedIrohaSpecialInstructions) (parse, verify, etc.)

[JavaScript client library](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Iroha+Additional+Requirements#IrohaAdditionalRequirements-JavascriptClientLibrary)  
[Web API](Web-API_21012259.html)[ISI Arguments Passing framework](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Iroha+Additional+Requirements#IrohaAdditionalRequirements-IrohaSpecialInstructionArgumentsPassingFramework)2.0.0[Query results as isi argument in complex ISI](Query-results-as-isi-argument-in-complex-ISI_21016401.html)[Math ISI](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Iroha+Additional+Requirements#IrohaAdditionalRequirements-MathematicalIrohaSpecialInstructions)2.0.0  
[Cycles ISI](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Iroha+Additional+Requirements#IrohaAdditionalRequirements-CyclesIrohaSpecialInstructions)

## Discussion

### Turing Complete Functions

As described in the whitepaper Iroha Special Instructions in combination with "listeners" will provide Turing Completeness for Iroha.

If there are additional details or user stories - they should be provided.

### Protected Storage

Iroha has \`Kura\` as a wrapper on top of \`BlockStorage\` with an ability to store encrypted data. 

If there are additional details or user stories - they should be provided.

### Data Related Iroha Special Instructions

As we understand the requirement, Iroha should be able to make verification of asset's based on some form of schema and following questions should be answered:

- what  data and schema formats should we support?
- do we need to have native support of these formats?
- what "etc." part consist of?

### Javascript Client Library

As planned we will port \`iroha-client\` to the \`no-std\` environment having an ability to compile it into \`WebAssembly\` module and use directly from Javascript.

### Iroha Special Instruction Arguments Passing Framework

In more details described in a separate PR, TL;DR - we may store results of previous Iroha Special Instructions as Assets and retrieve them from later Iroha Special Instructions via execution of Iroha Queries.

### Mathematical Iroha Special Instructions

The full list of operations we need to support Out-of-the-Box should be defined.

### Cycles Iroha Special Instructions

We may provide Iroha Special Instructions for finite cycles Our-of-the-Box.

For example \`For(n\_times, instruction\_to\_execute)\` and it will be just a "sugar" on top of \`Sequence\` instruction.

- [Abstract](#IrohaAdditionalRequirements-Abstract)
- [Discussion](#IrohaAdditionalRequirements-Discussion)
  
  - [Turing Complete Functions](#IrohaAdditionalRequirements-TuringCompleteFunctions)
  - [Protected Storage](#IrohaAdditionalRequirements-ProtectedStorage)
  - [Data Related Iroha Special Instructions](#IrohaAdditionalRequirements-DataRelatedIrohaSpecialInstructions)
  - [Javascript Client Library](#IrohaAdditionalRequirements-JavascriptClientLibrary)
  - [Iroha Special Instruction Arguments Passing Framework](#IrohaAdditionalRequirements-IrohaSpecialInstructionArgumentsPassingFramework)
  - [Mathematical Iroha Special Instructions](#IrohaAdditionalRequirements-MathematicalIrohaSpecialInstructions)
  - [Cycles Iroha Special Instructions](#IrohaAdditionalRequirements-CyclesIrohaSpecialInstructions)

## Attachments:

![](images/icons/bullet_blue.gif) [image2020-7-13\_19-18-35.png](attachments/21012444/21016662.png) (image/png)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
