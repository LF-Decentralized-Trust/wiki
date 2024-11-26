1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-12-10 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by Firas Qutishat on Dec 10, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

10 Dec 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)  (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com/)&gt;
- [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) (SecureKey)
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq) &lt;dmytro.kinoshenko@euristiq.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SeccreKey) &lt;rolson.quadras@securekey.com&gt;
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Introduce - implement behavior when introducer stops the protocol [#935](https://github.com/hyperledger/aries-framework-go/issues/935) [#922](https://github.com/hyperledger/aries-framework-go/issues/922) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Introduce - Add validation to the service for incoming messages [#890](https://github.com/hyperledger/aries-framework-go/issues/890) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Introduce - add the possibility to pass To structure to the Proposal (on review) [#945](https://github.com/hyperledger/aries-framework-go/issues/945) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- fix: make run-openapi-demo fails [#918](https://github.com/hyperledger/aries-framework-go/issues/918) [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)
- Transport Return Route Protocol (RFC 0092) basic flow complete with support for WebSocket and route option "all' [#858](https://github.com/hyperledger/aries-framework-go/issues/858) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Route Coordination Protocol (RFC 0211) Implementation in progress [#837](https://github.com/hyperledger/aries-framework-go/issues/837) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- API for protocols to communicate using DIDs, in progress [#725](https://github.com/hyperledger/aries-framework-go/issues/725) - [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence)
- Drafted HTTP over DIDComm RFC, splitting this into two RFCs - [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence)
- Verify JWS when creating new presentation [#862](https://github.com/hyperledger/aries-framework-go/issues/862) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- A cache of custom credential schemas of Verifiable Credential [#185](https://github.com/hyperledger/aries-framework-go/issues/185) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Added design for pluggable interfaces [here](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Crypto+and+KMS+Plugins) for Crypto/KMS/JWEBuilder [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

## Grooming updates (from the previous week)

## Design discussion

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- Implement logic in did-exchange service for forwarding an invitation and notify introducee after receiving an invitation [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Reply on an inbound message (get destination) &amp; specify `senderVerKey` on outbound messages [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Route Coordination Protocol (RFC 0211) Implementation in progress [#837](https://github.com/hyperledger/aries-framework-go/issues/837) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Pass VC Test Suite tests [#947](https://github.com/hyperledger/aries-framework-go/issues/947) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Support JSON-LD for Verifiable Credentials [#952](https://github.com/hyperledger/aries-framework-go/issues/952) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Linked Data proof of Verifiable Credential [#174](https://github.com/hyperledger/aries-framework-go/issues/174) - at least start the dev [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Drafted HTTP over DIDComm RFC, splitting this into two RFCs [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence)
- Add first integration for Crypto/KMS with Tink [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

## Future topics

- TBD

## Action items

- Groom HTTP tunneling over DIDComm ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) , [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)  )
- DIDAuthZ RFC and groom stories ([George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)  )

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
