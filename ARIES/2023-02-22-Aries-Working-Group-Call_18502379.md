1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-02-22 Aries Working Group Call

Created by Sam Curren, last modified on Feb 22, 2023

## Summary:

- did:keri lite
- LegacyPeer vs Transition to did:peer:1 or did:peer:2?

## Date

22 Feb 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)(Indicio) &lt;sam@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io) &lt;warren@affinitiquest.io&gt;
- [Simon Henriksen](https://lf-hyperledger.atlassian.net/wiki/people/712020:23306fb2-e990-49b4-b9c6-9ef1a17f038b?ref=confluence) (Hyphen) &lt;simon@hyphenapp.xyz&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [Michael Richardson](https://lf-hyperledger.atlassian.net/wiki/people/712020:1ffc962e-d389-4a7a-9f37-5d9fa45873e5?ref=confluence) (NorthernBlock) &lt;mike.richardson@northernblock.io&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio) &lt;alex.walker@indicio.tech&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Welcome / Introductions

## Announcements

- AnonCreds v2.0 Working Group's first meeting was held Monday – Meetings Page: [Meetings: AnonCreds v2.0 Working Group](/wiki/pages/createpage.action?spaceKey=ANONCREDS&title=Meetings%3A%20AnonCreds%20v2.0%20Working%20Group)
  
  - Meetings will be every 2nd Monday at 10:00 Pacific / 19:00 Central Europe starting this week (next meeting March 6)
  - Summary of discussion on Monday [2023-02-20 AnonCreds v2.0 Working Group Meeting](https://lf-hyperledger.atlassian.net/wiki/spaces/ANONCREDS/pages/20291946/2023-02-20+AnonCreds+v2.0+Working+Group+Meeting), and [slides](https://docs.google.com/presentation/d/1RlZbId6EvOgIHQfndFDYtTb7zY_xjA3lyhE0vOU5hG0/edit?usp=sharing)
- Aries Meeting at OWF – recording to be posted here: [https://github.com/openwallet-foundation/architecture-task-force/wiki/2023-02-20-Meeting-Minutes](https://github.com/openwallet-foundation/architecture-task-force/wiki/2023-02-20-Meeting-Minutes)

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
    - PR from SICPA for DIDComm v2 on AFJ need help:
      
      - [https://github.com/hyperledger/aries-framework-javascript/issues/1038](https://github.com/hyperledger/aries-framework-javascript/issues/1038)
      - [https://github.com/hyperledger/aries-framework-javascript/pull/1096](https://github.com/hyperledger/aries-framework-javascript/pull/1096)
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
  - Picos as Aries agents ([https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico))
    
    - Phil Windley has students working on a DIDComm v2 version of ACA-Pico
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

- OWF Presentation
- did:keri lite - Rodolfo
  
  - Has support for 'short-version' and 'long-version'
  - Currently has a dependence on larger keri libraries
  - Currently has a dependency on the larger did:keri method spec
- LegacyPeer DID Method vs did:peer:1 or did:peer"2
  
  - LegacyPeer DID Method
    
    - [https://github.com/hyperledger/aries-rfcs/pull/768](https://github.com/hyperledger/aries-rfcs/pull/768)
    - Community Coordinated Update?
    - Phase 1 - Everybody can read, defaults remain using old - April?
    - Phase 2 - Everybody switches default to fully qualified DIDs - June?
    - Phase 3 - Support for Old may be removed. - Sept?
  - did:peer:1
    
    - Supported in AFJ
    - lacks test vectors to verify serialization/normalization
  - did:peer:2
    
    - Contains endpoint info (large)
    - will exist in DIDComm v2
    - will require deterministic construction on both sides
- Timo: translating to existing DID makes the most sense.
  
  - requirements: translate by both sides of connection
  - recommends did:peer:2
  - skip legacy peer (also stephen, james agrees)

## Other Business

## Future Topics

- Thomas - [Nessus DIDComm 0.23.2 First Release](https://github.com/tdiesler/nessus-didcomm/releases/tag/0.23.2)
  
  - Wallet abstraction for AcaPy + Nessus native
  - Camel Http Endpoint for Nessus agent
  - Support for RFC0434 Out-of-Band Invitation V1 &amp; V2
  - Support for RFC0023 Did Exchange V1
  - Support for RFC0048 Trust Ping V1 &amp; V2
  - Support for RFC0095 Basic Message V1 &amp; V2
  - CLI to work with supported protocols and model

<!--THE END-->

- Issue Credential v2.1 learning
- State-of-union of Aries projects
- decorator for redirection after proofs. - existing?

## Action items

## Call Recording

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18502379/18517654.txt "Download")

Feb 22, 2023 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18502379/18517654.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18502379/18517652.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18502379/18517653.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
