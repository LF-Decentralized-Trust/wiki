1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-10-15 Framework Go Weekly Planning

Created by Troy Ronda, last modified by Firas Qutishat on Oct 22, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

15 Oct 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@securekey.com&gt;
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence) (SecureKey) &lt;troy.ronda@[securekey.com](http://securekey.com)&gt;
- [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence)  (SecureKey)
- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)  (SecureKey)
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)  (SecureKey)
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)  (SecureKey)
- Sandra (SecureKey)
- [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence) (SecureKey)
- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Protocol Failure - Update state to abandoned and trigger message notification - In progress [GitHub #480](https://github.com/hyperledger/aries-framework-go/pull/480) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Properties variable in Action/Msg event struct Refactored [GitHub #458](https://github.com/hyperledger/aries-framework-go/pull/458) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Moved messages and events code from dispatcher [GitHub #444](https://github.com/hyperledger/aries-framework-go/pull/444) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Add signer to did exchange service context [GitHub #476](https://github.com/hyperledger/aries-framework-go/pull/476) - [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)
- Implement SignMessage in the wallet [GitHub #450](https://github.com/hyperledger/aries-framework-go/pull/450) - [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)
- Introduce protocol service implementation (work in progress) [#464](https://github.com/hyperledger/aries-framework-go/issues/464) ([Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) )
- Define public server methods for introduce protocol [#448](https://github.com/hyperledger/aries-framework-go/issues/448) ([Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) )
- Unsecured JWT for Verifiable Credential [#372](https://github.com/hyperledger/aries-framework-go/issues/372) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Support Verifiable Presentation data model [#371](https://github.com/hyperledger/aries-framework-go/issues/371) - in PR review ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- Store Handle invitation Details (In progress) [#397](https://github.com/hyperledger/aries-framework-go/pull/443) ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence))
- [Inviter](/wiki/pages/createpage.action?spaceKey=ARIES&title=Inviter&linkCreation=true&fromPageId=18482537) ExResponse - Creation store data [#400](https://github.com/hyperledger/aries-framework-go/issues/400) (In progress)([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence))
- Key prefixes while persisting connection related records  [#433](https://github.com/hyperledger/aries-framework-go/issues/433) ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )
- Name spacing capability in store provider [#434](https://github.com/hyperledger/aries-framework-go/issues/434) ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )
- Working on persistence while processing invitation [#398](https://github.com/hyperledger/aries-framework-go/issues/398)  ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )
- Add ability to query connection from did exchange persistence [#424](https://github.com/hyperledger/aries-framework-go/issues/424) ([Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- Webhook for aries-agentd [#200](https://github.com/hyperledger/aries-framework-go/issues/200) (In progress) ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- Created Packager interface for Pack/Unpack and make the crypter use the Wallet for private keys [#385](https://github.com/hyperledger/aries-framework-go/issues/385) / [#459](https://github.com/hyperledger/aries-framework-go/pull/459) ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) )

## Grooming updates (from the previous week)

## Design discussion

## Milestone progress

- TBD

## Other business

- Groom 0.1.0 issues - need to close this milestone.

## Future topics

- TBD

## Action items

- \[Groom] REST API integration - Team
- \[Groom] Support for Public DID in Aries - Team

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
