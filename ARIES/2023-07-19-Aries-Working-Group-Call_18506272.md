1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-07-19 Aries Working Group Call

Created by Stephen Curran, last modified by Sean Bohan on Jul 26, 2023

## Summary:

- Aries Marketing Update
- Overview: Aries VCX
- Status of Indy SDK
- Open Discussion

## Date

19 Jul 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence) (BC Gov) &lt;alex.metcalf@gov.bc.ca&gt;
- [Helen Garneau](https://lf-hyperledger.atlassian.net/wiki/people/60209b07618001006995b244?ref=confluence) (Indicio) &lt;helen@indicio.tech&gt;
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio) &lt;kim@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Dave McKay](https://lf-hyperledger.atlassian.net/wiki/people/712020:24d508a3-ccfc-476f-b3c7-6b2549b19a23?ref=confluence) &lt;dave@verid.id&gt;
- [jkrupicka](https://lf-hyperledger.atlassian.net/wiki/people/712020:b1b8c987-e425-419a-908b-4ea45beea06a?ref=confluence) (Matrix Group International) &lt;jkrupicka@matrixgroup.net&gt;
- [Subhasis Ojha](https://lf-hyperledger.atlassian.net/wiki/people/6144ddd8e7c3280070b14906?ref=confluence)
- [Tim Bloomfield](https://lf-hyperledger.atlassian.net/wiki/people/5a70c8faa02421507dce29c3?ref=confluence) (OPS) &lt;tim.bloomfield@ontario.ca&gt;
- [Jason Sherman](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b5eb4a5-0d5d-4a7f-b2cc-b2d7597a7e8c?ref=confluence) (BC Gov/Quartech) &lt;jason@usingtechnolo.gy&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Jorge Flores](https://lf-hyperledger.atlassian.net/wiki/people/5c3f9ebb8ee3ae5b8b08422f?ref=confluence) (Entidad) &lt;jorge@entidad.io&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Aries Agent Test Harness -- [https://aries-interop.info](https://aries-interop.info)
- Aries Shared Components - Indy SDK replacements
  
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
    
    - Release 0.4.0-dev16
    - Release 0.5.0 will have breaking changes, including did:indy branch merged into main.
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
    
    - Release 0.2.9
  - AnonCreds Rust - [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
    
    - Release 0.1.0
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) - being replaced by AnonCreds Rust
    
    - Release 0.3.3 Bugfix (bug was in the python wrapper)
      
    - Release 1.0.0 Embeds new AnonCreds CL Signatures library with fixes, performance improvements
- Frameworks:
  
  - Aries-CloudAgent-Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
    
    - Release 0.9.0 pending – with new Release 1.0.0 CredX
    - New documentation site: [https://aca-py.org](https://aca-py.org)
  - Aries-Framework-JavaScript [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript), Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
    
    - Version 0.3.3 released - [https://github.com/hyperledger/aries-framework-javascript/releases](https://github.com/hyperledger/aries-framework-javascript/releases)
    - Version 0.4.0 released! - [https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.4.0](https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.4.0) - HUGE!
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
    
    - Release 0.56.0 [https://github.com/hyperledger/aries-vcx/releases/tag/0.56.0](https://github.com/hyperledger/aries-vcx/releases/tag/0.56.0)
  - Picos as Aries agents ([https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico))
    
    - Phil Windley has students working on a DIDComm v2 version of ACA-Pico
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
  - Time To Deprecate?
    
    - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native), Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
    
    - 0.4.0 in Bifold – including the shared components
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
  
  - Update to use SocketDock?
- [aries-endorser-server](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries-Toolbox](https://github.com/hyperledger/aries-toolbox)

## Discussion Topics

- Aries marketing update - survey results and new description
  
  - Survey results presentation: [https://docs.google.com/presentation/d/1n5wWNlySk4pUYAf-oUoi3CDDje4OPOVo9pPIjo80obQ/edit?usp=sharing](https://docs.google.com/presentation/d/1n5wWNlySk4pUYAf-oUoi3CDDje4OPOVo9pPIjo80obQ/edit?usp=sharing)
  - Latest description: [https://docs.google.com/document/d/1oys7g8y9iSOk5Lp1V6iC3BCHqvsKquonNPJl9v\_E3GE/edit?usp=sharing](https://docs.google.com/document/d/1oys7g8y9iSOk5Lp1V6iC3BCHqvsKquonNPJl9v_E3GE/edit?usp=sharing)
- Aries VCX - [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence) and team
  
  - All about VCX
- Status of the Indy SDK
- did:peer / unqualified did migration update
  
  - Work proceeding in ACA-Py to support did:peer:2/3
  - Issues with DID Peer 3 – can we address these?
  - [https://github.com/decentralized-identity/peer-did-method-spec/pull/55](https://github.com/decentralized-identity/peer-did-method-spec/pull/55) (fixes) – pending, but last change to be made
  - [https://github.com/hyperledger/aries-rfcs/pull/793](https://github.com/hyperledger/aries-rfcs/pull/793)
- Open Discussion

## Other Business

## Future Topics

- Niels Klomp offered a deeper dive into the openid4vc related flows

<!--THE END-->

- |State-of-union of Aries projects
- |decorator for redirection after proofs. - existing?

## Action items

## Call Recording:

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

File [GMT20230719-140306\_Recording.transcript.vtt](attachments/18506272/18518467.vtt "Download")

Jul 19, 2023 by [Sean Bohan](/wiki/people/634eef0301c2ff842c15f9e7)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

Text File [2023 07 19 Aries Working Group chat.txt](attachments/18506272/18518472.txt "Download")

Jul 19, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
