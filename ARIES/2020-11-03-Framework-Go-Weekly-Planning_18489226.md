1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2020-11-03 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by derektrider on Nov 03, 2020

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

03 Nov 2020 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)(SecureKey) &lt;firas.qutishat@securekey.com&gt;
- [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)(SecureKey) &lt;derek.trider@securekey.com&gt;
- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com)&gt;
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@securekey.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq) &lt;dmytro.kinoshenko@euristiq.com&gt;
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey) &lt;sudesh.shetty@securekey.com&gt;
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence) (SecureKey) &lt;troy.ronda@securekey.com&gt;
- [Kevin Griffin](https://lf-hyperledger.atlassian.net/wiki/people/70121:e8ea9141-eaa8-4587-8b69-bf1f7ba0a013?ref=confluence) (Scoir/Canis) &lt;kg@scoir.com&gt;
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) (SecureKey) &lt;baha.shaaban@securekey.com&gt;
- [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence) (Euristiq) &lt;andrii.holovko@euristiq.com&gt;
- [Philip Feairheller](https://lf-hyperledger.atlassian.net/wiki/people/557058:17f3102b-ea71-467d-a28a-19e046028e12?ref=confluence) (Scoir/Canis) &lt;phil@scoir.com&gt;
- [Mikaela Tarkocheva (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/557058:12be0949-3465-4537-a616-3e5d3fa61ab4?ref=confluence) (Scoir/Canis) &lt;mikaela@scoir.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- fix panic: cannot parse did document with \`@base\`[#2280](https://github.com/hyperledger/aries-framework-go/pull/2280) [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- Generalize EDV FormatProvider [#2273](https://github.com/hyperledger/aries-framework-go/issues/2273) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- EDV REST provider [#2208](https://github.com/hyperledger/aries-framework-go/issues/2208) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- Support capabilityChain in LD proofs [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) [#2282](https://github.com/hyperledger/aries-framework-go/pull/2285)
- Create Wrap/Unwrap Crypto API - [#2256](https://github.com/hyperledger/aries-framework-go/issues/2256)  [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) - wrap up the full task
- BBS+ Linked data proof signer [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Remove phoreproject/bls dependency (to use Fr from kilic lib) [#2248](https://github.com/hyperledger/aries-framework-go/issues/2248) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)

## Grooming updates (from the previous week)

## Design discussion

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- EDV REST provider ZCAP support [#2289](https://github.com/hyperledger/aries-framework-go/issues/2289) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- Allow EDV provider to be configurable from WASM and mobile bindings [#2290](https://github.com/hyperledger/aries-framework-go/issues/2290) [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- Create Wrap/Unwrap Crypto API - [#2256](https://github.com/hyperledger/aries-framework-go/issues/2256)  [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) - wrap up the full task
- BSS+ signature suite interop tests (with Mattr) [#2223](https://github.com/hyperledger/aries-framework-go/issues/2223) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Start to work on BSS+ selective disclosure [#2224](https://github.com/hyperledger/aries-framework-go/issues/2224) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)

## Future topics

- Let's have common DID mutation aries-framework-go interface that works for generic sidetree, TrustBloc , Indy and peer DID's [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) [Philip Feairheller](https://lf-hyperledger.atlassian.net/wiki/people/557058:17f3102b-ea71-467d-a28a-19e046028e12?ref=confluence)
  
  - Note: the trustbloc DID method CLI client can than be enhanced to be generic against supported framework VDRs. [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence)
- EDV BDD test for interop  [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- Docker image (agent-rest) to support EDV configuration [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- Refactor storage folder structure to better accommodate EDV/SDS [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence)
- KMS/Crypto/Key Server: add BDD tests in the framework that call a remote key server [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence)
- WebKMS client in the framework. [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Docker image (agent-rest) to support WebKMS configuration. [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

## Action items

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
