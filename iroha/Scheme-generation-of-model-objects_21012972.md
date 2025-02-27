1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Scheme generation of model-objects

Created by Rinat Kharisov, last modified by Egor Ivkov on Aug 17, 2021

Status

DECIDED

Stakeholders

[Ivan Rybin](https://lf-hyperledger.atlassian.net/wiki/people/602171f07db80e006a08ad45?ref=confluence) [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) [武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) 

OutcomeIt was decided to proceed an implement schema generationDue date  
Owner

[Rinat Kharisov](https://lf-hyperledger.atlassian.net/wiki/people/5d023e5bb674950c52db6547?ref=confluence)

## Background

- Iroha 2 peer receive messages from it clients primarily serialized in *[SCALE](https://github.com/paritytech/parity-scale-codec)  codec, but also some endpoint accept JSON messages*
- Iroha 2 has some client libraries in development (Rust, Java/Kotlin, JavaScript, Python)
- Scale codec do not need the name of the properties and containers, but JSON do need

## Problem

Iroha 2 has a lot of model-objects that peer can receive as input from blockchain clients and can respond with. Currently Iroha 2 in the active development process and set of this model-objects changes very often. These changes must be reflected in the Iroha 2 client's library and it requires a lot of affords to keep client's implementation up to date.

## Solution

We can generate a scheme which would introspect details of object-models. The scheme brings such benefits:

- Code generation of models and serialization/deserialization tests
- Type safe checks in clients code (if programming language support type safety)

Basically we can consider 3 types of items

1. *Scalars* 

*In SCALE integers can be encoded as fixed-width integer and compact integer. Compact integer itself has 4 modes. So generally we have 5 ways to serde integer (1 fixed-width + 4 modes of compact integers)* 

```
{
  "u8": {
    "Int": "FixedWidth"
  },
  "iroha_introspect::Compact<u8>": {
    "Int": "Compact"
  }
}
```

2\. Built-in basic types

- *bool: no tricks here*
- *String*

```
{
  "alloc::string::String": "String",
  "bool": "Bool"
}
```

*3. Built-in containers* 

- *Option / Result / Map / Vec : basically we are interested in only inner values of the container*
  
  ```
  {
  "core::option::Option<iroha_data_model::isi::Instruction>": {
    "Option": "iroha_data_model::isi::Instruction"
  },
  "core::result::Result<i32, i32>": {
    "Result": {
      "ok": "i32",
      "err": "i32"
    }
  },
  "alloc::collections::BTreeMap<alloc::string::String, i32>": {
    "Map": {
      "key": "alloc::string::String",
      "value": "i32"
    }
  },
  "alloc::vec::Vec<i32>": {
    "Vec": "i32"
  }
}
  ```

*4. Custom containers* 

- *Named structures – structures which have field names*
- *Unnamed structures – structures with no field names (like zero sized structures in rust, or tuples, or struct WrappedTuple(i32, i32))*
- *Enums*
  
  ```
  {
  "iroha_crypto::PublicKey": {
    "NamedStruct": {
      "declarations": [
        {
          "name": "digest_function",
          "ty": "alloc::string::String"
        },
        {
          "name": "payload",
          "ty": "alloc::vec::Vec<u8>"
        }
      ]
    }
  },
  "iroha_data_model::account::SignatureCheckCondition": {
    "UnnamedStruct": {
      "types": [
        "iroha_data_model::expression::EvaluatesTo<bool>"
      ]
    }
  },
  "iroha_data_model::events::pipeline::EntityType": {
    "Enum": {
      "variants": [
        {
          "name": "Block",
          "discriminant": 0,
          "ty": null
        },
        {
          "name": "Transaction",
          "discriminant": 1,
          "ty": null
        }
      ]
    }
  },
}
  ```

## Concerns

Currently we are not support polymorphism via TraitObjects, but it can be implemented if necessary

## Additional Information

1. *Scale codec description in Substrate docs \[[https://substrate.dev/docs/en/knowledgebase/advanced/codec](https://substrate.dev/docs/en/knowledgebase/advanced/codec)]*
2. *Scale codec Github page \[[https://github.com/paritytech/parity-scale-codec](https://github.com/paritytech/parity-scale-codec)]*

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
