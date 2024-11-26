1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-10-29 Framework Go Weekly Planning

Created by Troy Ronda, last modified by Firas Qutishat on Nov 05, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

29 Oct 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq) &lt;dmytro.kinoshenko@euristiq.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) (SecureKey)
- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) (SecureKey)
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey)
- [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) (SecureKey)
- [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) (SecureKey)
- [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/609a972c5d67f20069b81542?ref=confluence) (SecureKey)
- [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence) (SecureKey)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence) (SecureKey)
- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)

## Welcome / Introductions

## Announcements

- None

## Release status

- Planning release 0.1.0 this week

## Work updates (from the previous week)

- Integrate Message events with Webhooks - [GitHub #551](https://github.com/hyperledger/aries-framework-go/issues/551) -  [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Add log DID com msgs in bdd test [#598](https://github.com/hyperledger/aries-framework-go/issues/598)  - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Controller API bddtests with webhook server [#545](https://github.com/hyperledger/aries-framework-go/issues/545) [#585](https://github.com/hyperledger/aries-framework-go/issues/585) [#491](https://github.com/hyperledger/aries-framework-go/issues/491) [#94](https://github.com/hyperledger/aries-framework-go/issues/94) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- Providing 'label' for create invitation rest endpoint (Work in progress) [#452](https://github.com/hyperledger/aries-framework-go/issues/452) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- OpenAPI UI based demo for controller API (Work in progress) [#94](https://github.com/hyperledger/aries-framework-go/issues/94) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- Introduce protocol service implementation (work in progress) [#464](https://github.com/hyperledger/aries-framework-go/issues/464) ([Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) )
- refactor: removed storage usage from Callback logic [#587](https://github.com/hyperledger/aries-framework-go/issues/587) [#438](https://github.com/hyperledger/aries-framework-go/issues/438) ([Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) )
- JWT proof of Verifiable Presentation [#483](https://github.com/hyperledger/aries-framework-go/issues/483) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Verifiable Presentation follow-up issues [#327](https://github.com/hyperledger/aries-framework-go/issues/327), [#570](https://github.com/hyperledger/aries-framework-go/issues/570), [#586](https://github.com/hyperledger/aries-framework-go/issues/586) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Update the service to save and retrieve connection record using connection recorder storage [#397](https://github.com/hyperledger/aries-framework-go/issues/397) ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence))
- persistence layer for storing the inviter and invitee connection details [#527](https://github.com/hyperledger/aries-framework-go/issues/527) ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence) )
- DIDExchange REST MsgEvent - Fetch Connections Details from DB [#595](https://github.com/hyperledger/aries-framework-go/issues/595) ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence))
- Update Peer DID [#611](https://github.com/hyperledger/aries-framework-go/issues/611)  / Add verification key from store [#353](https://github.com/hyperledger/aries-framework-go/issues/353) in progress ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence))
- Added Key type in KeyPair, use signing key as key ID and storing both encryption and signature keys in the wallet store [#510](https://github.com/hyperledger/aries-framework-go/pull/510) ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence))
- Make Webhook supply real data (Complete) [#472](https://github.com/hyperledger/aries-framework-go/issues/472) ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- Fix service endpoint in create invitation response (In Review) [#572](https://github.com/hyperledger/aries-framework-go/issues/572) ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- Move Creator interface from wallet [#577](https://github.com/hyperledger/aries-framework-go/issues/577) ([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) )
- Explore solutions for incorporating default public did in request/response message([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence))

## Grooming updates (from the previous week)

## Design discussion

- [Aries Architecture Diagrams](https://docs.google.com/presentation/d/1L5L4QcZOATrn9rj4bEMmlbvij9XWyqgQRoWO-HNiUGw/present?includes_info_params=1&eisi=CMS2l83PweUCFYJuHwodDQAMWA#slide=id.p) - Refactoring pluggable VDRI, KMS, Crypto, etc. Rewrite framework over a language wrapper? Many questions.

## Milestone progress

- TBD

## Other business

- TBD

## Future topics

- TBD

## Action items

- Update Key set in wallet store to include sub-keys and create a structure that stores subkeys as reference IDs (introduce metadatastore) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Storage - transient v permanent
- Cleanup state machine outbound(redundant code)
- Cleanup state machine unit-test
- Groom discrepancies in rest api

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
