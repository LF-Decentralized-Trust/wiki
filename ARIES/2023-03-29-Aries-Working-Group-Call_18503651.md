1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-03-29 Aries Working Group Call

Created by Sam Curren, last modified by Thomas Diesler on Mar 30, 2023

## Summary:

- PR and Issue Review

## Date

29 Mar 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

## Recording: [dummyfile.txt](#)

Nessus Demo: [dummyfile.txt](#)

[Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) wanted to see messages with their respective direction

Here an attempt for this: [youtube.com/watch?v=6CBAf29-HQY](http://youtube.com/watch?v=6CBAf29-HQY)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio, PBC) &lt;alex.walker@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest)&lt;warren@affinitiquest.io&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Thomas Diesler](https://lf-hyperledger.atlassian.net/wiki/people/557058:ef106bd5-665a-489d-a319-dfb455bd44c1?ref=confluence) (RedHat) &lt;tdiesler@[redhat.com](http://redhat.com/)&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Alex Andrei](https://lf-hyperledger.atlassian.net/wiki/people/70121:00b65a7a-d5d0-4049-86d4-f9d8ebe69b62?ref=confluence) (RootsID) &lt;alex.andrei@rootsid.com&gt;

## Welcome / Introductions

## Announcements

- IIW - April 18-20, 2023, Mountain View, California.
  
  - Community Plans:
    
    - [DIDComm v2 Connect-a-thon](https://hackmd.io/j6U6JpQ2SRexSUKL7i2XRg) - HackMD lists the participants and live connections.
    - Hyperledger AnonCreds Update and V2.0 Progress

Release Status and Work Updates

- Aries Agent Test Harness -- [https://aries-interop.info](https://aries-interop.info)
- Aries Shared Components - Indy SDK replacements
  
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
    
    - Release 0.4.0 soon/this week(?) (0.4.0.dev.12 most recent)
    - Release 0.5.0 will have breaking changes, including did:indy branch merged into main.
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
    
    - Release 0.2.8 soon/this week(?) (0.2.8.dev.6 most recent)
  - AnonCreds Rust - [https://github.com/hyperledger/anoncreds-rs](https://github.com/hyperledger/anoncreds-rs)
    
    - Release 0.1.0 soon/this week(?) (0.1.0.dev.11 most recent)
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) - being replaced by AnonCreds Rust
    
    - Release 0.3.2 tagged
- Frameworks:
  
  - Aries-CloudAgent-Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
    
    - 0.8.0 released
    - 0.8.1 pending – upgrade command needs immediate work – arrgghhh... Relevant to multi-use invitations – including mediators.
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
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Discussion Topics

- Pending Items awaiting further action
  
  - did:peer:3
  - Issue Credential Short Circuit PR
  - Issue Credential 2.1 learning
- PR Review
  
  - [777](https://github.com/hyperledger/aries-rfcs/pull/777) - format identifiers
  - [778](https://github.com/hyperledger/aries-rfcs/pull/778) - fix mime type
  - [776](https://github.com/hyperledger/aries-rfcs/pull/776) - cred to credential in identifiers
- Issues
  
  - [779](https://github.com/hyperledger/aries-rfcs/issues/779) - cred attribute for images
- Nessus DIDComm demo - Thomas Diesler (Red Hat) - [recording of the presentation, demo and discussion](#)
  
  - DIDComm v2.0 Playground Server:  [http://nessus-tech.io:9100/](http://nessus-tech.io:9100/)
  - Nessus Repository: [https://github.com/tdiesler/nessus-didcomm/](https://github.com/tdiesler/nessus-didcomm/)
  - Sample CLI Script:
    
    - [https://github.com/tdiesler/nessus-didcomm/blob/main/cli/etc/script/travel-with-minor.txt](https://github.com/tdiesler/nessus-didcomm/blob/main/cli/etc/script/travel-with-minor.txt)
  - Example of a named object in the CLI – in this case "Airport.DID", but also used for VCs
    
    - [https://github.com/tdiesler/nessus-didcomm/blob/main/cli/etc/script/travel-with-minor.txt#L20](https://github.com/tdiesler/nessus-didcomm/blob/main/cli/etc/script/travel-with-minor.txt#L20)

Not Discussed, but left in the notes just because...

- DID Peer 2/3 – processing approach – is this the plan:
  
  - Identifiers:
    
    - Long Identifier – as defined today, entire encoded DIDDoc in identifier
    - Short identifier is the first 22(?) characters of 64 character string sha256 of long identifier (or something else?)
  - On receipt of a did:peer:2&lt;identifier&gt;, process as follows:
    
    - Detect length of identifier — short or long (assumption: long peer:did:2 will never be less than 23(?) bytes)
    - If short - resolve DID locally to get DIDDoc - on success, exit
    - If short and resolution failed — error, exit
    - If long
      
      - Convert long DID to short DID - resolve DID locally to get DIDDoc - on success, exit
    - If long and short DID resolution failed
      
      - Resolve long DID locally to get DIDDoc — on success, exit
    - if both short and long DID resolution fails
      
      - If on a “create DID” step (e.g. receiving DID Exchange “request” or “response” or DIDComm 2 new protocol step)
        
        - Extract DIDDoc from long DID, store short DID and DIDDoc, get DIDDoc — on success, exit
    - Otherwise — error

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

- State-of-union of Aries projects
- decorator for redirection after proofs. - existing?

## Action items

## Call Recording

  File Modified

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18503651/18517873.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18503651/18517872.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
