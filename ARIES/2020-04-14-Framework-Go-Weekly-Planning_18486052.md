1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2020-04-14 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by Sandra Vrtikapa on May 12, 2020

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

14 Apr 2020 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)  (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com/)&gt;
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey) &lt;sudesh.shetty@securekey.com&gt;
- [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence) (Euristiq) &lt;andrii.holovko@[euristiq.com](http://euristiq.com)&gt;
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq) &lt;dmytro.kinoshenko@euristiq.com&gt;
- [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence) (SecureKey) &lt;derek.trider@securekey.com&gt;
- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) (SecureKey) &lt;firas.qutishat@securekey.com&gt;
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@securekey.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) (SecureKey) &lt;baha.shaaban@securekey.com&gt;
- [Sandra Vrtikapa](https://lf-hyperledger.atlassian.net/wiki/people/712020:ce049f56-7daf-45db-9d97-8c71991da019?ref=confluence) (SecureKey) &lt;sandra.vrtikapa@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Issue Credential - added command support (on review) [#1611](https://github.com/hyperledger/aries-framework-go/issues/1611) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Fixed JS BDD tests [#1587](https://github.com/hyperledger/aries-framework-go/pull/1587) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Updated DID Doc definition with new fields. Implement support for "did:key" method [#1537](https://github.com/hyperledger/aries-framework-go/issues/1537) [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence)
- Refactor public key verifiers in signature suites [#1584](https://github.com/hyperledger/aries-framework-go/issues/1584) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Linked data proof refactoring &amp; bugfix [#1577](https://github.com/hyperledger/aries-framework-go/issues/1577), [#1578](https://github.com/hyperledger/aries-framework-go/issues/1578), [#1595](https://github.com/hyperledger/aries-framework-go/issues/1595), [#1602](https://github.com/hyperledger/aries-framework-go/issues/1602) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Credential Status Check over DIDComm: [#1454](https://github.com/hyperledger/aries-framework-go/issues/1454) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)
  
  - fix inlined keys in didcomm service entries for did docs [#1603](https://github.com/hyperledger/aries-framework-go/pull/1603)
  - Refactor introduce service to respond with out-of-band message: [#1568](https://github.com/hyperledger/aries-framework-go/issues/1568)
- Add Default implementation for crypto Anoncrypt SPI #987  - Splitting Go Jose from the Primitive - wip almost done Crypto Side [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

## Grooming updates (from the previous week)

## Design discussion

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- Add command support for the Present Proof protocol [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Add rest support for the Present Proof and Issue Credential protocols [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- JSON-LD canonicalization enhancements [#1592](https://github.com/hyperledger/aries-framework-go/issues/1592), [#1614](https://github.com/hyperledger/aries-framework-go/issues/1614) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- Linked data proof options to support domain, challenge &amp; purpose [#1601](https://github.com/hyperledger/aries-framework-go/issues/1601) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)
- Complete with "did:key" method support [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence)
- New JWE deserialize function [#1507](https://github.com/hyperledger/aries-framework-go/issues/1507) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- Increase unit test coverage in tinkcrypto once panic in Tink is fixed [#1512](https://github.com/hyperledger/aries-framework-go/issues/1512) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- jose/jws: support pluggable verifiers, secp256k1 [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Support secp256k1 in VC / VP (JWS case) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Pick tasks from VC remaining work list [#886](https://github.com/hyperledger/aries-framework-go/issues/886) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Add couchdb store implementation [#1599](https://github.com/hyperledger/aries-framework-go/issues/1599) [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Include JWE message building in Jose package for Add Default implementation for Anoncrypt SPI crypto primitive from #987 [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

## Future topics

- TBD

## Action items

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
