1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-07-12 Aries Working Group Call

Created by Sam Curren, last modified by Ry Jones on Jul 12, 2023

## Summary:

- Community Selector
- did:peer / Community Coordinated Update
- Open Discussion

## Date

12 Jul 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;
- [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence) (BC Gov) &lt;alex.metcalf@gov.bc.ca&gt;
- [Helen Garneau](https://lf-hyperledger.atlassian.net/wiki/people/60209b07618001006995b244?ref=confluence) (Indicio) &lt;helen@indicio.tech&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio) &lt;colton@indicio.tech&gt;
- [Tim Bloomfield](https://lf-hyperledger.atlassian.net/wiki/people/5a70c8faa02421507dce29c3?ref=confluence) (OPS) &lt;tim.bloomfield@ontario.ca)
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;
- [Clecio Varjao](https://lf-hyperledger.atlassian.net/wiki/people/557058:f9e1bfa2-a82c-4b68-85ee-627507d593d9?ref=confluence)  (BC Gov)&lt;clecio.varjao@gov.bc.ca&gt;

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
      
    - Breaking changes new version 1.0 CLSignatures library, removed ursa dependency.
      
      - (Pip requirements motivated the 1.0 version bump)
- Frameworks:
  
  - Aries-CloudAgent-Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
    
    - 0.8.2 released!
    - New documentation site: [https://aca-py.org](https://aca-py.org)
  - Aries-Framework-JavaScript [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript), Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
    
    - Version 0.3.3 released - [https://github.com/hyperledger/aries-framework-javascript/releases](https://github.com/hyperledger/aries-framework-javascript/releases)
    - Version 0.4.0 released! - [https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.4.0-alpha.87](https://github.com/hyperledger/aries-framework-javascript/releases/tag/v0.4.0-alpha.87) - HUGE!
  - Aries VCX ([https://github.com/hyperledger/aries-vcx](https://github.com/hyperledger/aries-vcx), Meetings: [Aries-VCX Meetings](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Community+calls)
    
    - Release 0.53.0 [https://github.com/hyperledger/aries-vcx/releases/tag/0.53.0](https://github.com/hyperledger/aries-vcx/releases/tag/0.53.0)
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

- Aries Marketing Update - Helen / Alex
  
  - Please complete this 3-minute survey right away:
    
    [https://docs.google.com/forms/d/e/1FAIpQLSfcgocuAzDNrk85Hk7m5v0IMTkz6lDuD6zqCrbN59rJZw84rQ/viewform?usp=sf\_link](https://docs.google.com/forms/d/e/1FAIpQLSfcgocuAzDNrk85Hk7m5v0IMTkz6lDuD6zqCrbN59rJZw84rQ/viewform?usp=sf_link)
- Community Selector Demo - James
- did:peer / unqualified did migration update
  
  - Issues with DID Peer 3 – can we address these?
  - [https://github.com/decentralized-identity/peer-did-method-spec/pull/55](https://github.com/decentralized-identity/peer-did-method-spec/pull/55) (fixes)
  - [https://github.com/hyperledger/aries-rfcs/pull/793](https://github.com/hyperledger/aries-rfcs/pull/793)
  - [https://identity.foundation/peer-did-method-spec/index.html#generation-method](https://identity.foundation/peer-did-method-spec/index.html#generation-method)
  - Migration Doc!
    
    - [https://github.com/TimoGlastra/legacy-did-transformation](https://github.com/TimoGlastra/legacy-did-transformation)
  - did:peer:2 or did:peer:3?
    
    - Stephen votes 3.
  - Community Coordinated Update - 
    
    - timing - a month
- VCX Update - Patrik (Next Week!)
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

[https://youtu.be/ieXRj-5dp\_8](https://youtu.be/ieXRj-5dp_8)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [2023 07 12 Aries Working Group transcript.txt](attachments/18506134/18518426.txt "Download")

Jul 12, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
