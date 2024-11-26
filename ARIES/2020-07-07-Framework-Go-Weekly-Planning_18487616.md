1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2020-07-07 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by Tomisin Jenrola on Jul 07, 2020

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

07 Jul 2020 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (Securekey) &lt;george.aristy@securekey.com&gt;
- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com/)&gt;
- [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence) (SecureKey) &lt;tomisin.jenrola@securekey.com&gt;
- [Andriy Holovko](https://lf-hyperledger.atlassian.net/wiki/people/557058:1e0c58ac-58b3-490a-807d-e7d095a0b88d?ref=confluence) (Euristiq) &lt;andrii.holovko@euristiq.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey) &lt;sudesh.shetty@securekey.com&gt;
- [derektrider](https://lf-hyperledger.atlassian.net/wiki/people/60b7f69348b89500697aa128?ref=confluence) (SecureKey) &lt;derek.trider@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Mobile support - finalised a solution to type restrictions [#1923](https://github.com/hyperledger/aries-framework-go/issues/1923)  [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Mobile support - created the interface design [#1941](https://github.com/hyperledger/aries-framework-go/issues/1941) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Bug: didexchange.Client.SaveConnection() not saving did-key mappings to did store [#1989](https://github.com/hyperledger/aries-framework-go/issues/1989) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)
- JS/BDD Tests refactoring [#1957](https://github.com/hyperledger/aries-framework-go/issues/1957) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Introduce - added correlation id [#1982](https://github.com/hyperledger/aries-framework-go/pull/1982)[Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Issue Credential - added correlation id [#1969](https://github.com/hyperledger/aries-framework-go/pull/1969)[Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Disabled compression for websocket [#1966](https://github.com/hyperledger/aries-framework-go/issues/1966) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Add ecdh1pu key types to localkms #1978 [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)
- Add Default implementation for JWE Authcrypt Packer #986 [Baha A Shaaban](https://lf-hyperledger.atlassian.net/wiki/people/712020:c6fcc16a-f888-4bb1-bef3-41f4da326364?ref=confluence)

## Grooming updates (from the previous week)

## Design discussion

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- Mobile support - start porting verifiable protocol [#1958](https://github.com/hyperledger/aries-framework-go/issues/1958) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Mobile support - wrap up introduce protocol [#1958](https://github.com/hyperledger/aries-framework-go/issues/1958) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Describe attachments for the Issue Credentials [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)

## Future topics

- TBD

## Action items

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
