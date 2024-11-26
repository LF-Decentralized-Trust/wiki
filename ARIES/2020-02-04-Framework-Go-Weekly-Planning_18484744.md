1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2020-02-04 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by Sandra Vrtikapa on Feb 11, 2020

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

04 Feb 2020 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com)&gt;
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq) &lt;dmytro.kinoshenko@euristiq.com&gt;
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey) &lt;sudesh.shetty@securekey.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) (SecureKey) &lt;filip.burlacu@securekey.com&gt;
- [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence) (SecureKey) &lt;derek.trider@securekey.com&gt;
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) (SecureKey) &lt;baha.shaaban@securekey.com&gt;
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@securekey.com&gt;
- [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) (SecureKey)

## Welcome / Introductions

## Announcements

- Aries Framework Go [v0.1.1](https://github.com/hyperledger/aries-framework-go/releases/tag/v0.1.1) Release

## Release status

- None

## Work updates (from the previous week)

- Add Metadata field to the thread decorator (on review) [#1164](https://github.com/hyperledger/aries-framework-go/issues/1164) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Messenger - simple implementation [#1132](https://github.com/hyperledger/aries-framework-go/issues/1132) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Add docs for introduce protocol [#1114](https://github.com/hyperledger/aries-framework-go/issues/1114) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- DIDComm Router BDD tests [#950](https://github.com/hyperledger/aries-framework-go/issues/950) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Support for Multiple Inbound Transport [#1124](https://github.com/hyperledger/aries-framework-go/issues/1124) [-](https://github.com/hyperledger/aries-framework-go/issues/1124) [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Linked Data proof of Verifiable Credential [#174](https://github.com/hyperledger/aries-framework-go/issues/174) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Support "jws" Linked Data proof [#1093](https://github.com/hyperledger/aries-framework-go/issues/1093) (PR review) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- verificationMethod for proof verification [#1156](https://github.com/hyperledger/aries-framework-go/issues/1156) (in progress) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- VC With DID Resolution [#1155](https://github.com/hyperledger/aries-framework-go/issues/1155) (in progress) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Basic messaging protocol [#959](https://github.com/hyperledger/aries-framework-go/issues/959) - [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- JS worker to use controller API  [#1070](https://github.com/hyperledger/aries-framework-go/issues/1070) (IN PROGRESS) - [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- Add SecretLock API service [#1144](https://github.com/hyperledger/aries-framework-go/issues/1144), [#1145](https://github.com/hyperledger/aries-framework-go/issues/1145) and [#1146](https://github.com/hyperledger/aries-framework-go/issues/1146) - [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

## Grooming updates (from the previous week)

## Design discussion

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- Introduce - the protocol should not depend on thread decorator [#1157](https://github.com/hyperledger/aries-framework-go/issues/1157)
- DIDComm Router/Mediator - REST API Binding [#989](https://github.com/hyperledger/aries-framework-go/issues/989) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- DIDComm Router/Mediator - BDD tests for REST binding [#1169](https://github.com/hyperledger/aries-framework-go/issues/1169) -  [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Refactoring creation of serialized JWT from Verifiable Credential [#339](https://github.com/hyperledger/aries-framework-go/issues/339) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- VC With DID Resolution [#1155](https://github.com/hyperledger/aries-framework-go/issues/1155) - implement for Linked Data Proofs - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- JS worker to use controller API  [#1070](https://github.com/hyperledger/aries-framework-go/issues/1070)  - [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- Create a new Storage type with Delete() function [#1147](https://github.com/hyperledger/aries-framework-go/issues/1147) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Add a new KMS API and mock [#1148](https://github.com/hyperledger/aries-framework-go/issues/1148) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Add a default (local) KMS implementation with SecretLock as option [#1149](https://github.com/hyperledger/aries-framework-go/issues/1149) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Hook the new KMS in framework and context [#1150](https://github.com/hyperledger/aries-framework-go/issues/1150) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Update Crypto unit tests to load a KMS with the new key formats [#1151](https://github.com/hyperledger/aries-framework-go/issues/1151) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

## Future topics

- TBD

## Action items

- VC client API and REST/WASM bindings
  
- VDRI client API and REST/WASM bindings
- JS API service for WASM

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
