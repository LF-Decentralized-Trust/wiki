1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Set of OOB ISIs

Created by Nikita Puzankov, last modified by Egor Ivkov on Aug 16, 2021

Status

DECIDED

Stakeholders

[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) [Yuriy Vinogradov](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b85dbf9-2cc9-4bee-a3a0-2815e5bb51eb?ref=confluence) [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) 

OutcomeDue date

11 Sep 2020

Owner

[Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence) 

## Background

We should declare the initial set of OOB (Out-Of-the-Box) Iroha Special Instructions for Hyperledger Iroha 2.0.0 release.

## Problem

Iroha [whitepaper](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md), current implementation and users' expectations are different in terms of out-of-the-box Iroha Special Instructions set.

To have some expected result in Iroha 2.0.0 we need to define the stable set of these instructions. Part of this work was made in [Iroha Special Instructions DSL](Iroha-Special-Instructions-DSL_21012073.html), here we will focus on instructions set, not how they work and how to use them.

## Solution

The good solution will be to define taxonomy and ontology on some full set of Iroha Special Instructions, had a strong agreement on categories and naming, with an ability to modify resulting set with small changes.

Use this agreement to update the White Paper, build current implementation and align users' expectations. 

### Decisions

Split out-of-the-box instructions into the following categories:

- Domain related
  
  - Register/Unregister&lt;Identifiable&gt;
  - Mint/Burn&lt;Id, Value&gt;
  - Transfer&lt;Id, Value, Id&gt;
- Math
  
  - Integer
    
    - Add/Substract&lt;EvaluatesTo&lt;u32&gt;, EvaluatesTo&lt;u32&gt;&gt;
    - Multiply/Divide&lt;EvaluatesTo&lt;u32&gt;, EvaluatesTo&lt;u32&gt;&gt;
    - RaiseTo&lt;EvaluatesTo&lt;u32&gt;, EvaluatesTo&lt;u32&gt;&gt;
    - Mod&lt;EvaluatesTo&lt;u32&gt;, EvaluatesTo&lt;u32&gt;&gt;
  - Comparison:
    
    - Equate&lt;Value, Value&gt;
    - Greater/Less&lt;EvaluatesTo&lt;u32&gt;, EvaluatesTo&lt;u32&gt;&gt;
  - Bool
    
    - Not&lt;EvaluatesTo&lt;bool&gt;&gt;
    - And/Or&lt;EvaluatesTo&lt;bool&gt;, EvaluatesTo&lt;bool&gt;&gt;
- Compositions
  
  - Sequence&lt;Vec&lt;Instruction&gt;&gt;
  - Pair&lt;Instruction, Instruction&gt;
  - If&lt;EvaluatesTo&lt;bool&gt;, Instruction, Option&lt;Instruction&gt;&gt;
- Vectors
  
  - Contains&lt;EvaluatesTo&lt;Vec&lt;Value&gt;&gt;, EvaluatesTo&lt;Value&gt;&gt;
  - ContainsAny/ContainsAll&lt;EvaluatesTo&lt;Vec&lt;Value&gt;&gt;, EvaluatesTo&lt;Vec&lt;Value&gt;&gt;&gt;
- Variables
  
  - Where&lt;Value, BTreeMap&lt;String, Value&gt;&gt;
  - ContextValue&lt;String&gt;
- Queries
  
  - Execute&lt;Query&gt;
- Misc
  
  - Fail&lt;String&gt;

Provide a set of possible domain-related instructions:

- Register/Unregister
  
  - Register or unregister Domain in Peer
  - Register or unregister Account in Domain
  - Register or unregister Asset Definition in Domain
  - Register or unregister Peer Id in Peer
  - Register or unregister Signatory in Account
- Mint
  
  - Mint or burn value to or from an Asset
- Fees
  
  - Register or unregister TransactionFee (e.g., fixed, percentage, DEX-swapped)

Provide a set of tools for DeFi:

- Register DEX
  
  - Register or unregister DEX (DEXManager) in Domain
- Register Liquidity Source
  
  - Register or unregister XYK Pool in DEX
    
  - Register or unregister Order Book in DEX
- Set liquidity fees
  
  - Register or unregister LiquidityFee (e.g., buy back and burn, pool share, etc.)

Provide a set of tools for Digital Identity ([https://ieeexplore.ieee.org/abstract/document/8377927/](https://ieeexplore.ieee.org/abstract/document/8377927/?casa_token=5HNXeGild0YAAAAA%3A_jUAdsBeADKjTkVGR6OSAtldPed4e5VnZygfhW7bAGU6S4E-PyK9tXJlJ8-I1actMjrxQw)):

- W3C-DIDs
  
  - Register or unregister DID in Account
    
  - Register or unregister VerifiableCredential in Account ([https://www.w3.org/TR/vc-data-model/](https://www.w3.org/TR/vc-data-model/))

### Alternatives

- Do not have categories and generic instructions using a plain set of instructions like "AddDomain, RegisterAccount" - as cons we can point out naming and extensibility problems
- Do not have granularity and differences between register, mint, add - as cons we can point out different business-related meanings for similar actions and to a wide set of options in one bucket

### Concerns

- A too big or too small set of out-of-the-box instructions can be hard to maintain or not sufficient for users needs
- Iroha 1 users can struggle from the new naming

### Assumptions - document any assumption that you made

- We did not make a final decision about "Iroha Modules" related instructions (DEX, Bridge, Permissions, etc.) and their inclusion into out-of-the-box set yet

### Risks

- Set will be incomplete from the users' perspective \`\[5;2]\`
- We missed some categories \`\[2;7]\`

## Additional Information

- [https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha\_2\_whitepaper.md](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md)
- [Iroha Special Instructions DSL](Iroha-Special-Instructions-DSL_21012073.html)
- [Re: Triggers](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Triggers?focusedCommentId=21017018)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
