1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2019-09-17 Framework Go Weekly Planning

Created by Troy Ronda, last modified by Firas Qutishat on Sep 24, 2019

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

17 Sep 2019 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)  (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence) (SecureKey) &lt;troy.ronda@securekey.com&gt;
- [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence)  (SecureKey)
- Derek (SecureKey)
- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)  (SecureKey)
- [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence)  (SecureKey)
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)  (SecureKey)
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)  (SecureKey)
- Sandra (SecureKey)
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Protocol Service eventing implementation in progress ([Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) )
- Selection criteria RFC (done) ([George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) )
  
  - New RFC 0214: [help-me-discover](https://github.com/hyperledger/aries-rfcs/tree/master/features/0214-help-me-discover)
  - New RFC 0217: [linkable-message-paths](https://github.com/hyperledger/aries-rfcs/tree/master/concepts/0217-linkable-message-paths)
  - Small tweak to RFC 0028: [introduce](https://github.com/hyperledger/aries-rfcs/tree/master/features/0028-introduce) in PR [#219](https://github.com/hyperledger/aries-rfcs/pull/219)
- Consent Receipts (in discovery) ([George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) )
- State Actions-Requested/Refactor Destination for sending outbound messages (Peer Review)
- Create default Implementation for Wallet CreateKey ([Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- Set ServiceEndpoint value from InboundTransport ([Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- Create Pack() for Authcrypt logic ([Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- Authcrypt Encrypt updated with JWK this weekend - work will resume to update the format ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) )
- Added all remaining controller API endpoints including exchange request/response workflow ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )
- Improvement of Verifiable Credential model extension. On-going work on JSON Web Token proof of Verifiable Credential (Dima)

## Grooming updates (from the previous week)

- Verification [#96](https://github.com/hyperledger/aries-framework-go/issues/96) groomed ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) / Sandra)
- BDD test framework (basic flow) groomed ([Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)  / Sandra / [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)  / [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) )
- To insure interoperability - must create tests matching  test data from IETF chacha20poly1035 standard: [https://tools.ietf.org/html/rfc7539#page-29](https://tools.ietf.org/html/rfc7539#page-29) ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence))
- Wallet pack/unpack proposal groomed (Firas / Baha)

## Design discussion

1. What to persist in the storage ?
   
   1. Encryption before storage
2. DID Exchange Flow - [Wiki](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/DID+Exchange+Flow+-+Framework+Go)/[Issue #258](https://github.com/hyperledger/aries-framework-go/issues/258) ([Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) )
3. Options for crypto/envelope interop with agents using libsodium: ([Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence)  / [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) )
   
   1. Convince other agents to switch from EC 25519 (Ed25519 signing, salsa/chacha encrypt) to more mature alternatives
   2. [Port](https://github.com/hyperledger/aries-framework-go/issues/210) the functions needed from libsodium to native golang
   3. Introduce libsodium dependency (using [GoKillers/libsodium-go](https://github.com/GoKillers/libsodium-go) wrapper)
   4. If libsodium is in some way incompatible/out of compliance with IETF specs (eg with chacha), get them to update, and convince other agents using libsodium to update

## Milestone progress

- No updates.

## Other business

- None.

## Future topics

- Outbound dispatcher ([Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) )
- Encryption before storage ([George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) / [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)  / Others? )
- Design and grooming for introduction protocol (Andrii)

## Action items

- Refactor Wallet/Crypter interface so the wallet holds all crypto, all secrets, but doesn't do the work of building the JSON envelope
- Groom Outbound dispatcher ([Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) / Sandra / [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)  / [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence) )
- Updated Sender Key encryption to JWK format ([Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) )
- Update DID Exchange flow to show completion event ([Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence))
- Groom service handle return types ([George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence) @Sandra [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Create and persist DID in the wallet ([Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) [Talwinder Kaur](https://lf-hyperledger.atlassian.net/wiki/people/557058:efba1922-111a-45bd-ada7-5e21ae89a9b5?ref=confluence) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) @Sandra

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
