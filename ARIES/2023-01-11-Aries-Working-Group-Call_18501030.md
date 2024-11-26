1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-01-11 Aries Working Group Call

Created by Sam Curren, last modified by James Ebert on Jan 11, 2023

## Summary:

- OCA update
- Mediator race conditions
- peer did methods
- AIP 3 tasks

## Date

11 Jan 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)(Indicio) &lt;sam@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Mike Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5ea322540d58350c2b066eeb?ref=confluence) (Indicio) &lt;mike@indicio.tech&gt;
- [Simon Henriksen](https://lf-hyperledger.atlassian.net/wiki/people/712020:23306fb2-e990-49b4-b9c6-9ef1a17f038b?ref=confluence) (Hyphen) &lt;simon@hyphenapp.xyz&gt;
- [Philip Essy-Ehsing](https://lf-hyperledger.atlassian.net/wiki/people/712020:493a701d-81ff-40c3-9ecd-d35e2f937163?ref=confluence) (Hyphen) &lt;philip@hyphenapp.xyz&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Aries Agent Test Harness ([https://aries-interop.info](https://aries-interop.info))
- Aries Shared Components - Indy SDK replacements
  
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs,)
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr,)
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
  - AnonCreds Rust - https://github.com/hyperledger/anoncreds-rs
- Frameworks:
  
  - Aries-CloudAgent-Python ([https://github.com/hyperledger/aries-cloudagent-python,](https://github.com/hyperledger/aries-cloudagent-python,) Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html))
  - Aries-Framework-JavaScript ([https://github.com/hyperledger/aries-framework-javascript,](https://github.com/hyperledger/aries-framework-javascript,) Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html))
    
    - Version 0.3.2 released - [https://www.youtube.com/watch?v=PGgUPPwa63g](https://www.youtube.com/watch?v=PGgUPPwa63g)
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
  - Picos as Aries agents ([https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
    
    - Bifold Summit Happening now – [Bifold Summit 2023](Bifold-Summit-2023_18500878.html)
    - BCGov has realeased an Aries Bifold version, rebranded w/ BC blue/theme/etc (BC wallet)
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
  
  - working on Pickup support
- [aries-endorser-server](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries-Toolbox](https://github.com/hyperledger/aries-toolbox)
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Discussion Topics

- OCA for Aries RFC update -- a [summary of the recent changes](https://docs.google.com/presentation/d/1kVibLBbETm8aZ33ZDHwy-4g0aZVH-sqrrn5tIJKmP2o/edit#slide=id.g181a2a9f280_0_5)
  
  - PR: [https://github.com/hyperledger/aries-rfcs/pull/755](https://github.com/hyperledger/aries-rfcs/pull/755)
  - RFC 0755 OCA for Aries: [https://github.com/swcurran/aries-rfcs/blob/oca4aries/features/0755-oca-for-aries/README.md](https://github.com/swcurran/aries-rfcs/blob/oca4aries/features/0755-oca-for-aries/README.md)
  - RFC 0756 OCA for Aries Style Guide: [https://github.com/swcurran/aries-rfcs/blob/oca4aries/features/0756-oca-for-aries-style-guide/README.md](https://github.com/swcurran/aries-rfcs/blob/oca4aries/features/0756-oca-for-aries-style-guide/README.md)
- Race conditions in establishing mediated connections
  
  - When the client of a mediator is establishing a connection to another agent, they must:
    
    - Send a message to the mediator to add the new DID/Key for the connection ([RFC 0211](https://github.com/hyperledger/aries-rfcs/tree/main/features/0211-route-coordination#keylist-update) *keylist-update* message)
    - Send a message to the other agent – RFC 0160 Connections or RFC 0023 DID Exchange "request" message.
    - Load testing shows that this is problematic – sometimes the response from the other agent comes to the mediator before the keylist-update is complete.
  - Found to be the case in ACA-Py – being serialized.  [Issue #2073](https://github.com/hyperledger/aries-cloudagent-python/issues/2073).
  - Suggest checking Aries Framework JavaScript / Aries Bifold to see if it is an issue there.
  - If performance is affected – could "pre-allocate" some number (even 1) Key and do the keylist-update as a background task, similar to the way revocation registries are handled in ACA-Py.
- Daniel Hardman's Grand Unifying Theory – [Presentation](https://docs.google.com/presentation/d/1ksqVxeCAvqLjr67htWZ4JYaSnI8TUZIO7tDMF5npHTo/edit?usp=share_link) – [Recording](https://us02web.zoom.us/rec/share/3T2MqVs6gUCnAosPzcegAPq_6dFN8i3zkuKI04nSlPnTaHTDs0tWusbX5G_-FH-Y.pS40kM3zazC_MaYz)
  
  - did:keri?
- did:legacypeer
  
  - draft beginning here: [https://hackmd.io/lY-QK03XQP6cTj2XfQyOZw](https://hackmd.io/lY-QK03XQP6cTj2XfQyOZw)
  - related issue: [https://github.com/hyperledger/aries-rfcs/issues/735](https://github.com/hyperledger/aries-rfcs/issues/735) (Timo)
  - usable, but un-creatable in DIDComm v2 (use did:peer?)
- AIP 3.0 Tasks
  
  - [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
  - Update Issue Credential and Present Proof to include .1 and .2 improvements
  - note to list which RFCs are included in the v2 spec
    
    - [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) will add this
  - Indy credws → Anoncreds
  - W3C format
  - BBS+ evolution
  - did:web RFC
    
    - [Alex Andrei](https://lf-hyperledger.atlassian.net/wiki/people/70121:00b65a7a-d5d0-4049-86d4-f9d8ebe69b62?ref=confluence) will do this
  - did:peer method 2 RFC
  - UX / OCA / Supplments
  - actionmenu
  - push notifications
  - BLE / NFC

## Other Business

## Future Topics'

- Thomas - Apache Camel AIP 1.0- done, touch base early next year.
- Issue Credential v2.1 learning
- State-of-union of Aries projects
- OIDC Credential Exchange in Aries - Mike Richardson
- decorator for redirection after proofs. - existing?

## Action items

## Call Recording

  File Modified

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
