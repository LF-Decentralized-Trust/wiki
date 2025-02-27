1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Requests for Comments](Requests-for-Comments_21016001.html)

# Hyperledger Iroha : Extensible serialization

Created by Andrei Lebedev on Sep 01, 2020

Status

NOT STARTED

Stakeholders

[Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence) [Kamil Salakhiev](https://lf-hyperledger.atlassian.net/wiki/people/557058:07723e0b-a027-4cc4-ad6d-324e41cccb4d?ref=confluence) [Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence) [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) 

OutcomeDue dateOwner

[Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence) 

## Background

## Problem

## Solution

Messages have a general structure with:

- Header, which contains meta information about the message, such as payload hash
- Payload
- Header signature

Header and payload are opaque, so that versioning can be managed by appending the fields.

### Decisions

### Alternatives

### Concerns

### Assumptions

### Risks

## Additional Information

[https://doi.org/10.6028/NIST.IR.8202](https://doi.org/10.6028/NIST.IR.8202)

[https://github.com/w3f/polkadot-spec/blob/master/host-spec/polkadot-host-spec.pdf](https://github.com/w3f/polkadot-spec/blob/master/host-spec/polkadot-host-spec.pdf)

[https://filecoin-project.github.io/specsheader payload/#systems\_\_filecoin\_blockchain\_\_struct](https://filecoin-project.github.io/specs/#systems__filecoin_blockchain__struct)

[https://sawtooth.hyperledger.org/docs/core/nightly/master/architecture/transactions\_and\_batches.html](https://sawtooth.hyperledger.org/docs/core/nightly/master/architecture/transactions_and_batches.html)

## Action items

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
