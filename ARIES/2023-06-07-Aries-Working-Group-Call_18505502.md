1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-06-07 Aries Working Group Call

Created by Sam Curren, last modified by Ry Jones on Jun 07, 2023

## Summary:

- OWF Presentation
- Open Discussion

## Date

07 Jun 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;
- [Helen Garneau](https://lf-hyperledger.atlassian.net/wiki/people/60209b07618001006995b244?ref=confluence) (Indicio) &lt;helen@indicio.tech&gt;
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence) (BC Gov) &lt;alex.metcalf@gov.bc.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [jkrupicka](https://lf-hyperledger.atlassian.net/wiki/people/712020:b1b8c987-e425-419a-908b-4ea45beea06a?ref=confluence) (Matrix Group International) &lt;jkrupicka@matrixgroup.net&gt;
- [Charles Lanahan](https://lf-hyperledger.atlassian.net/wiki/people/712020:50e56df1-41cf-415b-a802-ae0b89b9c75b?ref=confluence) &lt;charles.lanahan@gmail.com&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) (BC Gov / Petri Dish Development) &lt;amanji@petridish.dev&gt;
- [Ryan Koch](https://lf-hyperledger.atlassian.net/wiki/people/61032b0ce6e6f80071bb0d28?ref=confluence) (Indicio) &lt;ryan@indicio.tech&gt;
- Dr. Andre Kudra
- [Jorge Flores](https://lf-hyperledger.atlassian.net/wiki/people/5c3f9ebb8ee3ae5b8b08422f?ref=confluence) (Entidad) &lt;jorge@entidad.io&gt;

## Welcome / Introductions

## Announcements

- June 7-9 [https://diceurope.org/](https://diceurope.org/)
- Hackathon – [https://didhack.xyz/](https://didhack.xyz/) – need an Aries Developer to monitor Discord to answer questions from participants

Release Status and Work Updates

- Aries Agent Test Harness -- [https://aries-interop.info](https://aries-interop.info)
- Aries Shared Components - Indy SDK replacements
  
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
    
    - Release 0.4.0-dev14
    - Release 0.5.0 will have breaking changes, including did:indy branch merged into main.
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
    
    - Release 0.2.8
  - AnonCreds Rust - [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
    
    - Release 0.1.0-dev16
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) - being replaced by AnonCreds Rust
    
    - Release 0.3.2 tagged
- Frameworks:
  
  - Aries-CloudAgent-Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
    
    - 0.8.1 released – focused on the upgrade command, most relevant to multi-use invitations – including mediators.
    - New documentation site: [https://aca-py.org](https://aca-py.org)
  - Aries-Framework-JavaScript [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript), Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
    
    - Version 0.3.3 released - [https://github.com/hyperledger/aries-framework-javascript/releases](https://github.com/hyperledger/aries-framework-javascript/releases)
    - Version 0.4.0 in progress - [https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.4.0-alpha.87](https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.4.0-alpha.87)
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
    
    - Release 0.53.0 [https://github.com/hyperledger/aries-vcx/releases/tag/0.53.0](https://github.com/hyperledger/aries-vcx/releases/tag/0.53.0)
  - Picos as Aries agents ([https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico))
    
    - Phil Windley has students working on a DIDComm v2 version of ACA-Pico
  - Less active repos:
    
    - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
    - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native), Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
    
    - Bifold Summit Happening now – [Bifold Summit 2023](Bifold-Summit-2023_18500878.html)
    - BCGov has realeased an Aries Bifold version, rebranded w/ BC blue/theme/etc (BC wallet)
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
- [aries-endorser-server](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries-Toolbox](https://github.com/hyperledger/aries-toolbox)

## Discussion Topics

- AnonCreds Workshop Report - Stephen
- OWF Presentation
- Open Discussion

## Other Business

## Future Topics

- Niels Klomp offered a deeper dive into the openid4vc related flows
- Thomas - [Nessus DIDComm 0.23.2 First Release](https://github.com/tdiesler/nessus-didcomm/releases/tag/0.23.2)
  
  - Wallet abstraction for AcaPy + Nessus native
  - Camel Http Endpoint for Nessus agent
  - Support for RFC0434 Out-of-Band Invitation V1 &amp; V2
  - Support for RFC0023 Did Exchange V1
  - Support for RFC0048 Trust Ping V1 &amp; V2
  - Support for RFC0095 Basic Message V1 &amp; V2
  - CLI to work with supported protocols and model

<!--THE END-->

- State-of-union of Aries projects
- decorator for redirection after proofs. - existing?

## Action items

## Call Recording

[https://youtu.be/JTkfZuVHECk](https://youtu.be/JTkfZuVHECk)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [2023 06 07 Aries Working Group.txt](attachments/18505502/18518220.txt "Download")

Jun 07, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

File [2023 06 07 Aries Working Group.vtt](attachments/18505502/18518221.vtt "Download")

Jun 07, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
