1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-12-03 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by Firas Qutishat on Dec 10, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

03 Dec 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- Name (organization) &lt;email&gt;
- [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) (SecureKey)
- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)  (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com/)&gt;
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq) &lt;dmytro.kinoshenko@euristiq.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) (SecureKey)
- [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) (SecureKey)
- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) (Securekey) &lt;firas.qutishat@securekey.com&gt;

## Welcome / Introduction

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Implicit Invitation: REST API [#897](https://github.com/hyperledger/aries-framework-go/issues/897)([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence))
- Implicit Invitation: Go sdk enable invitee to specify own did for connection  [#892](https://github.com/hyperledger/aries-framework-go/issues/892) ([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence))
- Implementation of Transport Return Route Protocol (RFC 0092) [#858](https://github.com/hyperledger/aries-framework-go/issues/858) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Introduce - finish state machine [#883](https://github.com/hyperledger/aries-framework-go/issues/883) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Introduce - add requesting state to the service [#802](https://github.com/hyperledger/aries-framework-go/issues/802) [#853](https://github.com/hyperledger/aries-framework-go/issues/853) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Add GoDoc documentation with examples to verifiable package [#856](https://github.com/hyperledger/aries-framework-go/issues/856) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) )
- Convert Verifiable Credential into Verifiable Presentation [#861](https://github.com/hyperledger/aries-framework-go/issues/861) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Verify JWS when creating new presentation [#862](https://github.com/hyperledger/aries-framework-go/issues/862) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) )
- [Draft RFC](https://github.com/hyperledger/aries-rfcs/compare/master...Moopli:http-over-didcomm) for HTTP over DIDComm tunnel ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence))
- [Draft Aries RFC-0335](https://github.com/hyperledger/aries-rfcs/pull/334) for JWE envelopes FIPS/NIST compliant ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) )

## Grooming updates (from the previous week)

- High level tasks breakdown for DIDComm Router/Mediator [#807](https://github.com/hyperledger/aries-framework-go/issues/807) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)

## Design discussion

- Design Crypto/KMS [Issue 913](https://github.com/hyperledger/aries-framework-go/issues/913) ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence))

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- Completion of Transport Return Route Protocol (RFC 0092) [#858](https://github.com/hyperledger/aries-framework-go/issues/858) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Design/Implementation of Route Coordination Protocol (RFC 0211) [#837](https://github.com/hyperledger/aries-framework-go/issues/837) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Introduce - implement the state machine behavior when introducer stops the protocol [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Introduce refactoring (need to discuss with [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) ) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Refactoring creation of serialized JWT from Verifiable Credential [#339](https://github.com/hyperledger/aries-framework-go/issues/339) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)

## Future topics

- TBD

## Action items

- Groom FIPS compliant, JWE compliant Packer ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) , [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) )
- Groom HTTP tunneling over DIDComm ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) , [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) )
- DIDAuthZ RFC and groom stories ([George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) )

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
