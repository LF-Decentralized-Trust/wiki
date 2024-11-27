1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 1](Iroha-1_21015959.html)
4. [Architecture Decision Records](Architecture-Decision-Records_21015958.html)

# Hyperledger Iroha : Asset Amount

Created by Михаил Болдырев, last modified on Jul 11, 2019

- [Glossary](#AssetAmount-Glossary)
- [Vision](#AssetAmount-Vision)
  
  - [Current state](#AssetAmount-Currentstate)
  - [Problem statement](#AssetAmount-Problemstatement)
  - [Solution Criteria](#AssetAmount-SolutionCriteria)
  - [Choosing a solution](#AssetAmount-Choosingasolution)
    
    - [Using integers](#AssetAmount-Usingintegers)
      
      - [Description:](#AssetAmount-Description:)
      - [Pros:](#AssetAmount-Pros:)
      - [Cons:](#AssetAmount-Cons:)
    - [Using string &amp; integer](#AssetAmount-Usingstring&integer)
      
      - [Description:](#AssetAmount-Description:.1)
      - [Pros:](#AssetAmount-Pros:.1)
      - [Cons:](#AssetAmount-Cons:.1)
    - [Staying with a string](#AssetAmount-Stayingwithastring)
      
      - [Description:](#AssetAmount-Description:.2)
      - [Pros:](#AssetAmount-Pros:.2)
      - [Cons:](#AssetAmount-Cons:.2)
- [Functional details](#AssetAmount-Functionaldetails)
  
  - [Changelog](#AssetAmount-Changelog)
  - [Research strategy](#AssetAmount-Researchstrategy)
  - [Documentation effort](#AssetAmount-Documentationeffort)
  - [QA activity](#AssetAmount-QAactivity)
  - [Tasks](#AssetAmount-Tasks)

Priority

MUST

Type of change request

FEATURE

Epic link  
Status

DRAFT

Target release

# **Glossary**

- **quantity** - an entity of Iroha state that is used to measure *assets*
- **floating point notation** - a representation of a rational number `N`  in a predefined range with fixed relative precision: `N = K * 10e`, where `K` and `e` are some integer numbers from a fixed range.
- **significand** - the `K` number in *floating point notation*
- **precision** - the number `p`  equal to `-e` in *floating point notation* and to the number of rightmost digits of *significand* that form the decimal fractional part (separator position)
- **uint256** - integer type with range from 0 to 2256

# **Vision**

## Current state

Iroha model has Asset entity, which is measured by *quantity*. The quantity is a floating point number with the following constraints:

- *significand:* 0 &lt; `K`  &lt; 2256
- *precision:* 0  ≤ `p` &lt; 256

Iroha has several commands that include asset quantity specification:

- AddAssetQuantity
- SubtractAssetQuantity
- TransferAsset

and a query that contains asset quantity in response:

- GetAccountAssets

Also there are ways of retrieving submitted transactions that can include the commands listed above (that contain asset quantity):

- GetBlock
- FetchCommits
- GetPendingTransactions

In all of them the asset quantity is represented as a string, while it semantically means a floating point number.

The API of Iroha uses Protocol Buffers, which built-in integer types are capable of representing numbers up to 264.

## Problem statement

Using the string representation of floating point number causes several problems:

- what are the valid forms of number representation (consider `000.0000` - is it a valid quantity?)
- quantities equality (`01` seems equal to `1.0` , but the strings differ)
- parsing strings into numbers (we have the *significand* limit of 2256 which is larger than c++ standard types allow, and we used regular expressions to parse them, which seems a poor architectural decision)
- overflow detection - it just gets undetected now

## Solution Criteria

- each valid number (see current state) is represented in exactly one way
- simple parsing
- convenient API

## Choosing a solution

### Using integers

#### Description:

All the described problems proceed from representing a floating point number as a string. So one approach consists in changing the representation of asset quantity to integers. Inside Iroha we already use a 256-bit integer type, so the transition will be comfortable. But protobuf does not support such large integers, which implies some tricks. For example, we can create the following protobuf message to represent *uint256*:

```
message Uint256le {
	uint64 i0 = 1;
	uint64 i1 = 2;
	uint64 i2 = 3;
	uint64 i3 = 4;
}
message Quantity {
	Uint256le significand = 1;
	uint32 precision = 2;
}
```

The conversion is done like little-endian number (de)serialization.

```
n = i0 + i1 << 64 + i2 << 64^2 + i3 << 64^3
```

```
i0 = n
i1 = n << 64
i2 = n << 64^2
i3 = n << 64^3
```

#### Pros:

- conversion rules are very straightforward
- invalid quantity is almost impossible to create (the only exception is out-of-range *precision*, but all other approaches also suffer from that)
- memory efficiency
- best CPU efficiency (fast single-pass conversion)

#### Cons:

- manual protobuf  (de)serialization with bit shifting
- additional protobuf message type for *uint256*

### Using string &amp; integer

#### Description:

We can simplify the representation by moving the *precision* part out of the string into an integer. *significand*  is left in string representation, but we need less complicated rules and parsing algorithm for that string.

```
message Quantity {
	string significand = 1;
	uint32 precision = 2;
}
```

The rules for *significand* string:

- only decimal digits are allowed
- number range limit

There is a tricky part in dealing with range limit. The boost multiprecision library *uint256*  type that we use now will not report does not provide overflow detection when parsing a string. So a KISS approach would be:

1. first char is zero → error
2. length exceeds 78 → error
3. length is exactly 78 and the most significant digit is greater than 1 → error
4. length is exactly 78 and parsed number is less than 1078 → error (the largest number possible after overflow is 2 * 1078 - 1 - 2256 &lt; 1078)

These rules guarantee the 1-to-1 mapping between *uint256* and any valid quantity.

#### Pros:

- simple protobuf API
- good CPU efficiency (fast string checks)

#### Cons:

- worst memory efficiency (1 string + 1 32-bit int)
- dark byte magics for efficient overflow detection

### Staying with a string

#### Description:

We still can stay with a single string to represent a quantity, while improving the rules and parsing algorithms to satisfy the *solution criteria*. Possible algorithm of string validation:

- first chat is zero → error
- any char is not digit or decimal separator → error
- more than one decimal separators → error
- last char is decimal separator → error
- there is a decimal separator and the last char is zero → error
- the string with decimal separator removed does not pass overflow test (see the algorithm above) → error

#### Pros:

- no changes to API structure

#### Cons:

- dealing with the string becomes very tricky - harder to guarantee reliable bugprone operation
- bad memory and CPU efficiency
- the format of the number representation is not very intuitive, because most interpreters that we got used to do not provide 1-to-1 mapping, so the API users will have to struggle with the rules we define for the string.

# **Functional details**

**Environmental objectives:** None

## Changelog

#Change descriptionAffected componentChange motivationDependency (optional)1What is changedWhere it is changed

Why it is done

After #1

Before #1

etc.

## Research strategy

#Research activityDetailsAcceptance criteriaResponsible (accepter) 1

## Documentation effort

#Target readerDocumentation description1

## QA activity

#Validation activityIntentionActionsExpected result 1TestingTest component X and check if …

Given X,

When Y

*AND*

When Y1

Then Z

*OR*

Then Z1

## Tasks

key summary type created updated due assignee reporter priority status resolution

Unable to locate Jira server for this macro. It may be due to Application Link configuration.

* * *

Template data

Priorities MUST SHOULD COULD WON'T

Change request type FEATURE BUG FIX

Status BACKLOG WORK IN PROGRESS DONE

Document generated by Confluence on Nov 26, 2024 15:05

[Atlassian](http://www.atlassian.com/)
