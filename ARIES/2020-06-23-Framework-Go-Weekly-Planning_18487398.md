1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2020-06-23 Framework Go Weekly Planning

Created by George Aristy, last modified by Tomisin Jenrola on Jun 23, 2020

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

16 Jun 2020 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)  (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com/)&gt;
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@securekey.com&gt;
- [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence) (Euristiq) &lt;andrii.holovko@euristiq.com&gt;
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq) &lt;dmytro.kinoshenko@euristiq.com&gt;
- [Firas Qutishat](https://lf-hyperledger.atlassian.net/wiki/people/712020:81a7fd70-5c04-4c64-80bd-5701a34d4bb8?ref=confluence) (Securekey) &lt;firas.qutishat@securekey.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence) (SecureKey) &lt;tomisin.jenrola@securekey.com&gt;
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey) &lt;sudesh.shetty@securekey.com&gt;
- [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence) (SecureKey) &lt;baha.shaaban@securekey.com&gt;

## Welcome / Introductions

## Announcements

- Starting support for mobile (Android and iOS) devices

## Release status

- None

## Work updates (from the previous week)

- fix: presentproof (Go SDK): unable to correlate requests to responses [#1942](https://github.com/hyperledger/aries-framework-go/issues/1942) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)
- feat: Added MyDID and TheirDID to the action event [#1933](https://github.com/hyperledger/aries-framework-go/pull/1933) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- feat: Updated present proof protocol to v2 [#1931](https://github.com/hyperledger/aries-framework-go/pull/1931) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Attachments for the Present Proof protocol (in progress) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- BBS+ Signatures 2020 - verification part (under review) [#1725](https://github.com/hyperledger/aries-framework-go/issues/1725) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- VC extension of Credential Subject (PR preparation) [#1943](https://github.com/hyperledger/aries-framework-go/issues/1943) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Mobile support - completed writing scripts for mobile binding [#1921](https://github.com/hyperledger/aries-framework-go/issues/1921) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Mobile support - creating solution to type restrictions [#1923](https://github.com/hyperledger/aries-framework-go/issues/1923) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Mobile support - creating an interface [#1941](https://github.com/hyperledger/aries-framework-go/issues/1941) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Create ECDH-1PU primitives factories [#1911](https://github.com/hyperledger/aries-framework-go/issues/1911)  [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Create ECDH-1PU default key templates [#1912](https://github.com/hyperledger/aries-framework-go/issues/1912) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Custom Verifiable Presentation structure [#1936](https://github.com/hyperledger/aries-framework-go/issues/1936) [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)

## Grooming updates (from the previous week)

## Design discussion

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- Attachments for the Present Proof protocol [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)
- Attachments for the Issue Credential protocol [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)[George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)
- BBS+ Signatures 2020 [#1725](https://github.com/hyperledger/aries-framework-go/issues/1725) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- Implement ECDH-1PU core Key Wrapping logic [#1913](https://github.com/hyperledger/aries-framework-go/issues/1913) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Implement ECDH-1PU core Key UnWrapping logic [#1914](https://github.com/hyperledger/aries-framework-go/issues/1914) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Implement Authcrypt Packer [#986](https://github.com/hyperledger/aries-framework-go/issues/986) [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Port more packages from Aries over to mobile [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)

## Future topics

- TBD

## Action items

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
