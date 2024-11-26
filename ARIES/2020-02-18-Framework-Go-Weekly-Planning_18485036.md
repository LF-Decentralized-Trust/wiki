1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2020-02-18 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by Troy Ronda on Feb 18, 2020

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

18 Feb 2020 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com)&gt;
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq) &lt;dmytro.kinoshenko@euristiq.com&gt;
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) (SecureKey) &lt;baha.shaaban@securekey.com&gt;
- [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)(SecureKey) &lt;derek.trider@securekey.com&gt;
- [Filip Burlacu](https://lf-hyperledger.atlassian.net/wiki/people/712020:954f178b-c612-4ebd-9960-433199bfe689?ref=confluence) (SecureKey) &lt;filip.burlacu@securekey.com&gt;
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey) &lt;sudesh.shetty@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- aries-js-worker: enabled browser usage (PRs: [#1224](https://github.com/hyperledger/aries-framework-go/pull/1224) [#1233](https://github.com/hyperledger/aries-framework-go/pull/1233) [#1239](https://github.com/hyperledger/aries-framework-go/pull/1239) [#1241](https://github.com/hyperledger/aries-framework-go/pull/1241) [#1242](https://github.com/hyperledger/aries-framework-go/pull/1242) [#1276](https://github.com/hyperledger/aries-framework-go/pull/1276)) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)
- aries-js-worker: implementing CI (task [#1238](https://github.com/hyperledger/aries-framework-go/issues/1238) in progress) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)
- Improve logging inside he framework [#1248](https://github.com/hyperledger/aries-framework-go/issues/1248) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Agent Rest Binding - Support to set LOGGER level [#1219](https://github.com/hyperledger/aries-framework-go/issues/1219) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Ignore Transport Return Route decorator for forward message [#1218](https://github.com/hyperledger/aries-framework-go/issues/1218) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Refactoring: Introduce protocol should not depend on the thread (on review) [#1157](https://github.com/hyperledger/aries-framework-go/issues/1157)[Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Support "jws" Linked Data proof [#1093](https://github.com/hyperledger/aries-framework-go/issues/1093) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Refactoring creation of serialized JWT from Verifiable Credential [#339](https://github.com/hyperledger/aries-framework-go/issues/339) (JWS) - lightweight JWT - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- JWT library with flexible signers [#1264](https://github.com/hyperledger/aries-framework-go/issues/1264) - PR review [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Create a new Storage type with Delete() function [#1147](https://github.com/hyperledger/aries-framework-go/issues/1147)  and Add a new KMS API and mock [#1148](https://github.com/hyperledger/aries-framework-go/issues/1148) - [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Add a default (local) KMS implementation with SecretLock as option [#1149](https://github.com/hyperledger/aries-framework-go/issues/1149) - in PR [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Hook the new KMS in framework and context [#1150](https://github.com/hyperledger/aries-framework-go/issues/1150)  and update Crypto unit tests to load a KMS with the new key formats [#1151](https://github.com/hyperledger/aries-framework-go/issues/1151) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- aries-js-worker : command handling through wasm [#1272](https://github.com/hyperledger/aries-framework-go/issues/1272), [#1262](https://github.com/hyperledger/aries-framework-go/issues/1262), [#1259](https://github.com/hyperledger/aries-framework-go/issues/1259), [#1250](https://github.com/hyperledger/aries-framework-go/issues/1250), [#1245](https://github.com/hyperledger/aries-framework-go/issues/1245), [#1221](https://github.com/hyperledger/aries-framework-go/issues/1221), [#1208](https://github.com/hyperledger/aries-framework-go/issues/1208) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)

## Grooming updates (from the previous week)

## Design discussion

- [didcomm:// protocol handlers](https://github.com/trustbloc/bloc-docs/issues/15) (context: [trustbloc/bloc-docs#15](https://github.com/trustbloc/bloc-docs/issues/15)) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- DIDComm Router - Support for Query router connID [#1217](https://github.com/hyperledger/aries-framework-go/issues/1217) - [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- DIDComm Router/Mediator - BDD tests for REST binding [#1169](https://github.com/hyperledger/aries-framework-go/issues/1169) -  [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)
- Issue Credential Protocol [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- JWT library with flexible signers [#1264](https://github.com/hyperledger/aries-framework-go/issues/1264) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- verificationMethod for proof verification [#1156](https://github.com/hyperledger/aries-framework-go/issues/1156) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- REST binding for Verifiable Credential docs [#1190](https://github.com/hyperledger/aries-framework-go/issues/1190) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- WASM/JS binding for verifiable credential docs [#1191](https://github.com/hyperledger/aries-framework-go/issues/1191) - [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- To Start working on JWE:
  
  - Review [JWM spec](https://tools.ietf.org/html/draft-looker-jwm-01)
  - Create a generic JWE format issue# to be created [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
  - Add Default implementation for JWE Authcrypt [#986](https://github.com/hyperledger/aries-framework-go/issues/986) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
    
    - Nested JWS version
    - ECDH-1PU version
  - Add Default implementation for JWE Anoncrypt [#987](https://github.com/hyperledger/aries-framework-go/issues/987) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
  - What happens to "legacy" Authcrypt/Anoncrypt?
- aries-js-worker: fixes and enhancements [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)

## Future topics

- "OutOfBand" protocol [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)
  
  - [https://hackmd.io/mVupMtg9RqWWUhMvWkDXGQ](https://hackmd.io/mVupMtg9RqWWUhMvWkDXGQ)
  - Moves invitation to its own protocol
  - Invitation will kickstart a workflow by including the next steps
  - Context: [trustbloc/bloc-docs#10](https://github.com/trustbloc/bloc-docs/issues/10)

## Action items

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
