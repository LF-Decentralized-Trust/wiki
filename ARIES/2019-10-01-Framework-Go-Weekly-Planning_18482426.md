1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-10-01 Framework Go Weekly Planning

Created by Troy Ronda, last modified by Rolson Quadras on Oct 08, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

01 Oct 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)  (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence) (SecureKey) &lt;troy.ronda@[securekey.com](http://securekey.com)&gt;
- [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence)  (SecureKey)
- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)  (SecureKey)
- [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence)  (SecureKey)
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)  (SecureKey)
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)  (SecureKey)
- Sandra (SecureKey)
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@[securekey.com](http://securekey.com)&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Service eventing implementation complete - [Github#276](https://github.com/hyperledger/aries-framework-go/issues/276) ([Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) )
- Consume service events in client complete - [GitHub #249](https://github.com/hyperledger/aries-framework-go/issues/249) ([Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) )
- Add post event handle [#304](https://github.com/hyperledger/aries-framework-go/issues/304) ( [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- Create bddtest for basic flow [#260](https://github.com/hyperledger/aries-framework-go/issues/260) ( [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- Implement Send Exchange Acknowledgement [#293](https://github.com/hyperledger/aries-framework-go/issues/293) ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence) )
- Add SendverKey to outbound dispatcher in didexchange.Service [#299](https://github.com/hyperledger/aries-framework-go/issues/299) ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence) )
- Diagram for Introduce Protocol [#269](https://github.com/hyperledger/aries-framework-go/issues/269) ([Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) )
- Verifiable Claims WG Test Suite [#326](https://github.com/hyperledger/aries-framework-go/issues/326)(Dima[Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Add support for multiple proofs to DID Document  [#324](https://github.com/hyperledger/aries-framework-go/issues/324)([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) )
- Implement ED25519Signature2018 Signature Suite  [#248](https://github.com/hyperledger/aries-framework-go/issues/248)([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) )
- Implement LD Signature Create Verify Hash Algorithm  [#243](https://github.com/hyperledger/aries-framework-go/issues/243)([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) )
- Done implementation of crypto/envelope interoperability with agents using a more standard (IETF draft is WIP) JWK field for sender key ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence))
- Updated IETF draft for our JWE format using XChachaPoly1305 encryption example ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence))
- Working on separating Crypto logic from JWE building logic in current JWE package [#385](https://github.com/hyperledger/aries-framework-go/issues/385) ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence))
- Finished Legacy Authcrypter (with decrypt [#340](https://github.com/hyperledger/aries-framework-go/pull/340))
- Working on separating Crypto logic from envelope building logic in current legacy package ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) )
- Worked on DID creators for services ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )

## Grooming updates (from the previous week)

## Design discussion

1. How to calculate label of invitee in service ? ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence))
2. Support JWT with ES256K (secp256k1) signature ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))

## Milestone progress

- 0.1.0 due tomorrow

## Other business

- TBD

## Future topics

- TBD

## Action items

- Groom mapping between invitation and events [GitHub #387](https://github.com/hyperledger/aries-framework-go/issues/387) [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)[Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
