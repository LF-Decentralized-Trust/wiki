1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [aries-framework-go](aries-framework-go_18481606.html)
5. [Framework Go Meetings](Framework-Go-Meetings_18482076.html)

# Hyperledger Aries : 2020-07-28 Framework Go Weekly Planning

Created by Rolson Quadras, last modified by Dmitriy Kinoshenko on Jul 28, 2020

## Summary:

Planned topics

- Work updates (5 mins)
- Grooming (20 mins)
- Design discussion (20 mins)
- Open Discussion (10 mins)

## Date

28 Jul 2020 (7:30AM Los Angeles, 10:30AM Toronto/New York, 3:30PM London, 17:30H Moscow)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence) (Euristiq) &lt;andrii.soluk@[euristiq.com](http://euristiq.com/)&gt;
- [George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence) (SecureKey) &lt;george.aristy@securekey.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence) (SecureKey) &lt;rolson.quadras@securekey.com&gt;
- [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence) (Euristiq&gt; &lt;dmytro.kinoshenko@euristiq.com&gt;
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence) (SecureKey) &lt;sudesh.shetty@securekey.com&gt;

## Welcome / Introductions

## Announcements

- None

## Release status

- None

## Work updates (from the previous week)

- Mobile support: added IssueCredential wrappers [#2036](https://github.com/hyperledger/aries-framework-go/pull/2036) and docs [#2038](https://github.com/hyperledger/aries-framework-go/pull/2038) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Update Verifiable controllers [#2034](https://github.com/hyperledger/aries-framework-go/issues/2034) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Fixed Present Proof protocol according to RFC [#2046](https://github.com/hyperledger/aries-framework-go/pull/2046) [#2050](https://github.com/hyperledger/aries-framework-go/pull/2050) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Fixed storage behavior [#2027](https://github.com/hyperledger/aries-framework-go/pull/2027) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Added new linters (nestif,godot) [#2037](https://github.com/hyperledger/aries-framework-go/pull/2037) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- Check VP embedded proof [#2049](https://github.com/hyperledger/aries-framework-go/issues/2049) [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)
- BBS+ signature suite on-going work [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)

## Grooming updates (from the previous week)

## Design discussion

## Milestone progress

- TBD

## Other business

- TBD

## Upcoming work

- Mobile support: add PresentProof wrappers [#2039](https://github.com/hyperledger/aries-framework-go/issues/2039) and docs [#2040](https://github.com/hyperledger/aries-framework-go/issues/2040) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Mobile support: update verifiable interface and implementations [#2035](https://github.com/hyperledger/aries-framework-go/issues/2035) [Tomisin Jenrola](https://lf-hyperledger.atlassian.net/wiki/people/712020:f327bd6c-95a3-480e-a11b-4dcdc8cfbdb6?ref=confluence)
- Add handlers support based on RFCs [0510-dif-pres-exch-attach](https://github.com/hyperledger/aries-rfcs/tree/master/features/0510-dif-pres-exch-attach) and [0511-dif-cred-manifest-attach](https://github.com/hyperledger/aries-rfcs/tree/master/features/0511-dif-cred-manifest-attach) [Андрій Солук](https://lf-hyperledger.atlassian.net/wiki/people/557058:944bd0fe-c47d-4ef3-b564-b2165534d406?ref=confluence)
- BBS+ signature suite [Dmitriy Kinoshenko](https://lf-hyperledger.atlassian.net/wiki/people/557058:f8587cfb-189f-48fd-99b8-0f11f3d4fc50?ref=confluence)

## Future topics

- TBD

## Action items

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
