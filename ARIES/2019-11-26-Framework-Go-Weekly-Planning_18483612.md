1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-11-26 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by Firas Qutishat on Dec 03, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

26 Nov 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) (Securekey) &lt;firas.qutishat@securekey.com&gt;
- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com)&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)  (SecureKey) &lt;troy.ronda@securekey.com&gt;
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) (SecureKey)
- [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) (SecureKey)

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Support for IndexedDB [#830](https://github.com/hyperledger/aries-framework-go/pull/830) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Allow user to inject inbound transport in rest cli [#878](https://github.com/hyperledger/aries-framework-go/pull/878) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Allow user to inject multiple outbound transport in rest cli [#870](https://github.com/hyperledger/aries-framework-go/pull/870) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Allow user to inject multiple outbound transport [#863](https://github.com/hyperledger/aries-framework-go/pull/863) - [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- DIDComm WebSocket Transport [#813](https://github.com/hyperledger/aries-framework-go/issues/813) [#827](https://github.com/hyperledger/aries-framework-go/issues/827) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- DIDComm Router : Initial Analysis [#837](https://github.com/hyperledger/aries-framework-go/issues/837) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Error handling in controller REST API [#756](https://github.com/hyperledger/aries-framework-go/issues/756) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- Create public DID in VDRI [#845](https://github.com/hyperledger/aries-framework-go/issues/845) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- Accept Invitation and Accept Exchange request to support public DIDs [#871](https://github.com/hyperledger/aries-framework-go/issues/871) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- BDD tests for DIDexchange with public DIDs using controller - In Progress [#796](https://github.com/hyperledger/aries-framework-go/issues/796) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- Implicit Invitation [#817](https://github.com/hyperledger/aries-framework-go/issues/817)([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence))
- Design discussions for issue-credential protocol [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)
- Introduce - add requesting state to the service (on review) [#853](https://github.com/hyperledger/aries-framework-go/issues/853) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Added dependency interface to the Client (Introduce) [#724](https://github.com/hyperledger/aries-framework-go/issues/724) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Introduce - replace custom mock with gomock [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Design discussion for issue-credential protocol [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- Created a new RFC proposal for request credential flow (on hold) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- Implement client layer for issue-credential flow (holder starts with request) (on hold) [#850](https://github.com/hyperledger/aries-framework-go/issues/850) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- Understanding verifiable credential and implement service layer for issue credential (on hold) #875 [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/609a972c5d67f20069b81542?ref=confluence)
- Refactor creation of VC which extends the base data model [#263](https://github.com/hyperledger/aries-framework-go/issues/263)  ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) )
- Construct Verifiable Credential object (encoding side) [#831](https://github.com/hyperledger/aries-framework-go/issues/831) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Add GoDoc documentation with examples to verifiable package [#856](https://github.com/hyperledger/aries-framework-go/issues/856) - in progress ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))

## Grooming updates (from the previous week)

- Transport Return Route Protocol (RFC 0092) [#858](https://github.com/hyperledger/aries-framework-go/issues/858) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)

## Design discussion

- DIDAuthZ: resource authorization/discovery
- Generic tunnels: HTTP over DIDcomm
- JWE Envelope

## Milestone progress

- TBD

## Other business

- Differentiating between fundamentals and domain-specific payload features. [See RFCs#332.](https://github.com/hyperledger/aries-rfcs/issues/332)
  
  - How do we indicate what to instantiate when starting the framework? TODO.
- DID Exchange should have a way to indicate default for simplex vs duplex.

## Upcoming work

- Get destination from the inbound message, add functionality to finish state machine, add validation to the introduce service [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Implementation of Transport Return Route Protocol (RFC 0092) [#858](https://github.com/hyperledger/aries-framework-go/issues/858) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Update Crypto logic - [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence)
- Implicit Invitation REST API [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)
- Add GoDoc documentation with examples to verifiable package [#856](https://github.com/hyperledger/aries-framework-go/issues/856) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Verify JWS when creating new presentation [#862](https://github.com/hyperledger/aries-framework-go/issues/862) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) )
- Convert Verifiable Credential into Verifiable Presentation [#861](https://github.com/hyperledger/aries-framework-go/issues/861) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))

## Future topics

- TBD

## Action items

- JWE Envelope RFC and groom stories ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence))
- Groom routing stories ([Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- UI components ([Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence) ) 
  
  - Higher level agent interface and where does this go (and particularly for UI component planning)?
- HTTP tunneling over DIDcomm RFC and groom stories ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence)  [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence) [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence) )
- DIDAuthZ RFC and groom stories ([George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) )
- Document remaining plan for Introduce protocol ([Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence))
- Document remaining plan for Verifiable Credentials ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
