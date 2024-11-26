1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-10-22 Framework Go Weekly Planning

Created by Troy Ronda, last modified by Sudesh Shetty on Jan 05, 2021

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

22 Oct 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) (Euristiq)  &lt;[andrii.soluk@euristiq.com](mailto:andrii.soluk@euristiq.com)&gt;
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey) &lt;sudesh.shetty@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Protocol Failure - Update state to abandoned and trigger message notification [GitHub #480](https://github.com/hyperledger/aries-framework-go/pull/480) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- PeerDID Generation in Wallet [GitHub #485](https://github.com/hyperledger/aries-framework-go/issues/485) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Split service.Handle function for Inbound/Outbound type [GitHub #490](https://github.com/hyperledger/aries-framework-go/issues/490) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Introduce protocol service implementation (work in progress) [#464](https://github.com/hyperledger/aries-framework-go/issues/464) ([Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) )
- Refactored Crypto operations out of Legacy Wallet [#352](https://github.com/hyperledger/aries-framework-go/issues/352) ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence))
- Update wallet to include signature and encryption key pairs (work in progress) [#488](https://github.com/hyperledger/aries-framework-go/issues/488) ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) )
- Include key type (algorithm) to support multiple key types (Bundled with #488 above) [#272](https://github.com/hyperledger/aries-framework-go/issues/272) ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence))
- persistence layer for storing and retrieving connection record details issue-527/issue-526  (talwinder)[Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/609a972c5d67f20069b81542?ref=confluence) )
- Service update to consume connection recorder storage issue-397 ([Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/609a972c5d67f20069b81542?ref=confluence) )
- HTTP DID Resolver: bddtest using sidetree-node ([Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- HTTP DID Resolver: bddtest using sidetree-fabric ( [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- Support for public DID in create/handle invitation [#503](https://github.com/hyperledger/aries-framework-go/issues/503) ([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)  )
- BDD test for create invitation  with public DID  [#525](https://github.com/hyperledger/aries-framework-go/issues/525) ([Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)  )
- Completed persisting DIDs in wallet [#486](https://github.com/hyperledger/aries-framework-go/pull/486) ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )
- Currently working on REST API demo/bddtest [#94](https://github.com/hyperledger/aries-framework-go/pull/94) [#491](https://github.com/hyperledger/aries-framework-go/pull/491) ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )
- Finished basic Webhook flow with sample notification [#200](https://github.com/hyperledger/aries-framework-go/issues/200) ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- Make Webhook supply real data (in progress) [#472](https://github.com/hyperledger/aries-framework-go/issues/472) ([derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence))
- Support Verifiable Presentation data model [#371](https://github.com/hyperledger/aries-framework-go/issues/371) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))
- JWT proof of Verifiable Presentation [#483](https://github.com/hyperledger/aries-framework-go/issues/483) ([Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence))

## Grooming updates (from the previous week)

- Controller/Webhook/Rest API [GitHub #539](https://github.com/hyperledger/aries-framework-go/issues/539) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)

## Design discussion

## Milestone progress

- TBD

## Other business

- TBD

## Future topics

- TODO -  Storage of keys in the wallet - need to support multiple types of storages (leveldb, memcache/redis, hsm, etc.) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence)
- TODO - model separate storages - Transient data vs secrets vs did doc (public/peer did) vs connection info vs metadata vs persistent data

## Action items

- \[Groom] Introduce protocol (callback function) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Add stories for public DID [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence)
- Return recipient key  as correlation id from packager [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
