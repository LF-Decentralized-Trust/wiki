1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2020-04-21 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by derektrider on Apr 23, 2020

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

21 Apr 2020 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey) [sudesh.shetty@securekey.com](mailto:sudesh.shetty@securekey.com)
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@securekey.com&gt;
- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com/)&gt;
- [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence) (Euristiq) &lt;andrii.holovko@[euristiq.com](http://euristiq.com)&gt;
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq) &lt;dmytro.kinoshenko@euristiq.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence) (SecureKey) &lt;derek.trider@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Credential Status Check over DIDComm: [#1454](https://github.com/hyperledger/aries-framework-go/issues/1454) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)
  
  - Refactor introduce service to respond with out-of-band message: [#1568](https://github.com/hyperledger/aries-framework-go/issues/1568)
  - outofband events [#1635](https://github.com/hyperledger/aries-framework-go/pull/1635)
  - didexchange - handle oob invitations [#1630](https://github.com/hyperledger/aries-framework-go/pull/1630)
  - outofband: support \`invitation\` message [#1488](https://github.com/hyperledger/aries-framework-go/issues/1488)
  - outofband: parse requests in diddcomm attachments [#1493](https://github.com/hyperledger/aries-framework-go/issues/1493)
- Issue Credential - adds REST support (in progress) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) [#1650](https://github.com/hyperledger/aries-framework-go/issues/1650)
- Present Proof - adds command support (on review) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) [#1633](https://github.com/hyperledger/aries-framework-go/issues/1633)
- Fixed minor issues: Present Proof unit tests, BDD test. [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Completed with did:key method support [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence) [#1537](https://github.com/hyperledger/aries-framework-go/issues/1537)
- Improve Presentation.SetCredentials() [#1620](https://github.com/hyperledger/aries-framework-go/issues/1620) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Support \`publicKeyHex\` verification key in EcdsaSecp256k1Signature2019 signature suite [#1609](https://github.com/hyperledger/aries-framework-go/issues/1609) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Multiple proof array in VC [#1645](https://github.com/hyperledger/aries-framework-go/issues/1645) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Check all verification relationships of DID when resolving public key of VC [#1652](https://github.com/hyperledger/aries-framework-go/issues/1652) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Fix JWK.PublicKeyBytes() for ed25519 and ecdsa [#1660](https://github.com/hyperledger/aries-framework-go/issues/1660) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Add Default implementation for JWE Anoncrypt SPI [#987](https://github.com/hyperledger/aries-framework-go/issues/987) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

<!--THE END-->

- Create new Key types to support ECDH-ES primitives (using NIST approved keys) [#1469](https://github.com/hyperledger/aries-framework-go/issues/1469)
- Replace HKDF with ConcatKDF in new ECDH-ES Tink primitive [#1472](https://github.com/hyperledger/aries-framework-go/issues/1472)
- Update created Tink Key types to return JWE components from crypto primitives [#1470](https://github.com/hyperledger/aries-framework-go/issues/1470)
- Add JWE build/parse support with new Tink key type created above [#1638](https://github.com/hyperledger/aries-framework-go/issues/1638)

<!--THE END-->

- Increase unit test coverage in tinkcrypto HMAC once panic in Tink is fixed [#1512](https://github.com/hyperledger/aries-framework-go/issues/1512) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)

## Grooming updates (from the previous week)

## Design discussion

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- Follow-up tickets on did:key method (e.g. [#1659](https://github.com/hyperledger/aries-framework-go/issues/1659), need discussion) [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence)
- Integration DIDComm protocols with edge-service [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence)
- Present Proof - need to add REST support [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- VC BDD tests extension - need to add new KMS/Crypto support [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Improvements in JWS, VC JWS [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- New JWE deserialize function [#1507](https://github.com/hyperledger/aries-framework-go/issues/1507) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)

## Future topics

- TBD

## Action items

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
