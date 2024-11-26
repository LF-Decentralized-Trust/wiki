1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-11-12 Framework Go Weekly Planning

Created by Rolson Quadras, last modified on Nov 12, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

12 Nov 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)  (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com)&gt;
- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) (SecureKey) &lt;firas.qutishat@securekey.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- 0.1.0 documentation [#739](https://github.com/hyperledger/aries-framework-go/issues/739) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Refactor DidResolver.Read() should return a did.Doc [#118](https://github.com/hyperledger/aries-framework-go/issues/118) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Refactor use did resolver to get the peer did doc [#703](https://github.com/hyperledger/aries-framework-go/issues/703) [#645](https://github.com/hyperledger/aries-framework-go/issues/645) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- DIDExchange - State Name update for Action Events [Github #690](https://github.com/hyperledger/aries-framework-go/issues/690) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- RestAPI - Accept Invitation API Implementation [Github #692](https://github.com/hyperledger/aries-framework-go/issues/692) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Fix for query connection not returning transient data - [Github #722](https://github.com/hyperledger/aries-framework-go/issues/722) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- DID exchange client refactoring  [#727](https://github.com/hyperledger/aries-framework-go/issues/727) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Fixed data race in introduce protocol [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
  
- Introduce protocol client implementation [#657](https://github.com/hyperledger/aries-framework-go/issues/657) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Added dependency interface to Client [#724](https://github.com/hyperledger/aries-framework-go/issues/724) (on review) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
  
- Custom mock was replaced with gomock (introduce protocol) (on review) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Refactor state tests #707 [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/609a972c5d67f20069b81542?ref=confluence)
- Create a connection between request and invitation, Sign the Exchange response with Invitation RecipientKey #issue-676, #issue728 [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/609a972c5d67f20069b81542?ref=confluence)
- Add support for public dids in did-exchange protocol [#561](https://github.com/hyperledger/aries-framework-go/issues/561) ([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence))
- Documentation, examples for didexchange client([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence))
- Verifiable Credential follow-up issues [#514](https://github.com/hyperledger/aries-framework-go/issues/514), [#712](https://github.com/hyperledger/aries-framework-go/issues/712) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- JWT from Verifiable Credential with ES256K (secp256k1) signature [#381](https://github.com/hyperledger/aries-framework-go/issues/381) - in progress ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Support environment variables in addition to command line arguments ([#473](https://github.com/hyperledger/aries-framework-go/issues/473)) - Complete ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- Grooming stories for issue-credential/ making technical flow diagram - In progress ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- 0.1.0 documentation - Running aries-agentd/CLI and webhooks - In progress ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- Minor fixes, linters and restructuring in bddtests &amp; aries-agentd go module [#738](https://github.com/hyperledger/aries-framework-go/issues/738), [#584](https://github.com/hyperledger/aries-framework-go/issues/584), [#713](https://github.com/hyperledger/aries-framework-go/issues/713), [#686](https://github.com/hyperledger/aries-framework-go/issues/686),  [#648](https://github.com/hyperledger/aries-framework-go/issues/648) ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )
- Get all connections [#429](https://github.com/hyperledger/aries-framework-go/issues/429) ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )
- Refactor Keys structure in KMS [#596](https://github.com/hyperledger/aries-framework-go/issues/596) - in progress should finish soon ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) )

## Grooming updates (from the previous week)

## Upcoming work

- Consolidate creator, storage and resolver DID under VDRI [#777](https://github.com/hyperledger/aries-framework-go/issues/777) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Define clear relationship between framework and context [#212](https://github.com/hyperledger/aries-framework-go/issues/212) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Continue working on design for issue-credential implementation. Need to figure out the format for request-credential ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- externalAddr scheme can be set by user [#747](https://github.com/hyperledger/aries-framework-go/issues/747) ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- DidExchange -Errors #112 ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/609a972c5d67f20069b81542?ref=confluence))
- Implicit Invitation #718 ([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)
- Implement service behavior according to Client dependency (introduce protocol) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
  
- event tech debts [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- JWT from Verifiable Credential with ES256K (secp256k1) signature [#381](https://github.com/hyperledger/aries-framework-go/issues/381) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Refactoring creation of serialized JWT from Verifiable Credential [#339](https://github.com/hyperledger/aries-framework-go/issues/339) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))

## Design discussion

- Showed first draft of issue-credential technical flow. More work to be done ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- DIDExchange Request Msg - Empty label

## Milestone progress

- TBD

## Other business

- TBD

## Future topics

- TBD

## Action items

- Groom discrepancies in rest api

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
