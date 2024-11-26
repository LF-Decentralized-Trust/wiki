1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-05-17 Aries Working Group Call

Created by Sam Curren, last modified by Ariel Gentile on May 18, 2023

## Summary:

- DID Peer / Unqualified DIDs
- Open Wallet Foundation

## Date

17 May 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio) &lt;alex.walker@indicio.tech&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio) &lt;colton@indicio.tech&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Alexander Manecke](https://lf-hyperledger.atlassian.net/wiki/people/70121:605aa4e3-8e6c-40d5-ac0b-f63c777a633c?ref=confluence) (Deutsche Telekom, IDunion) &lt;a.manecke@telekom.de&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) (Linux Foundation)
- [Helen Garneau](https://lf-hyperledger.atlassian.net/wiki/people/60209b07618001006995b244?ref=confluence) (Indicio) &lt;helen@indicio.tech&gt;
- [Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence) (Animo) &lt;berend@animo.id&gt;
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) (Animo) &lt;karim@animo.id&gt;
- [Tim Bloomfield](https://lf-hyperledger.atlassian.net/wiki/people/5a70c8faa02421507dce29c3?ref=confluence) (OPS) &lt;tim.bloomfield@ontario.ca&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [Andre Kudra](https://lf-hyperledger.atlassian.net/wiki/people/5edd3b799c72bd0ac03bc93b?ref=confluence) (esatus AG) &lt;a.kudra@esatus.com&gt;
- [Christopher Hempel](https://lf-hyperledger.atlassian.net/wiki/people/5d25a35dfd3b8b0c278eb2d8?ref=confluence) (esatus AG / IDunion) &lt;c.hempel@esatus.com&gt;
- [Sebastian Bickerle](https://lf-hyperledger.atlassian.net/wiki/people/712020:c993a7aa-74a4-4102-9f1d-29af164a9ff9?ref=confluence) (neosfer GmbH / lissi / IDunion) &lt;sebastian.bickerle@neosfer.com&gt;
- [Peter Janes](https://lf-hyperledger.atlassian.net/wiki/people/70121:2ec8ae7c-995e-4832-a270-bbf1843e8ba1?ref=confluence) (Abdagon AG) &lt;peter.janes@abdagon.com&gt;
- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) (2060.io) &lt;a@2060.io&gt;

## Welcome / Introductions

## Announcements

- June 7-9 [https://diceurope.org/](https://diceurope.org/)
- Hackathon – [https://didhack.xyz/](https://didhack.xyz/) – need an Aries Developer to monitor Discord to answer questions from participants
- [AnonCreds Workshop](https://zoom.us/meeting/register/tJAqcOCurDstHdIAWH0mbPz2hLK55OPr1Hj_?utm_campaign=Hyperledger%20workshops&utm_content=246078071&utm_medium=social&utm_source=twitter&hss_channel=tw-2512683048#/registration) May 31, 2023 08:00 AM

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

- DID Peer Update?
  
  - Alex added PR for Method 3: [https://github.com/decentralized-identity/peer-did-method-spec/pull/49](https://github.com/decentralized-identity/peer-did-method-spec/pull/49)
- Unqualified DID Conversion to did:peer:2
  
  - [https://github.com/hyperledger/aries-framework-javascript/blob/main/packages/core/src/modules/dids/methods/peer/peerDidNumAlgo2.ts#L94](https://github.com/hyperledger/aries-framework-javascript/blob/main/packages/core/src/modules/dids/methods/peer/peerDidNumAlgo2.ts#L94)
  - RFC? - Volunteer Needed!
- Open Wallet Foundation
  
  - The Opportunity
    
    - A potential re-homing of Aries to OWF
  - The Circumstances
    
    - Community needs decisions together
  - The Challenges
  - Notes on discussion and questions to be clarified
    
    - High ambition level of OWF
      
      - Goal is to create code that has relevance in code that meets regulatory requirements (e.g. as part of the EU Digital Identity Wallet)
      - Aries features and approaches can gain better representation in compliance and regulatory settings employing wallets (key leverage point for Aries community)
      - Outreach to European Commission already established at OWF
    - Funding
      
      - 300 orgs listed in doc
      - [https://openwallet.foundation/wp-content/uploads/sites/11/2023/02/OpenWallet-Foundation-Overview.pdf](https://openwallet.foundation/wp-content/uploads/sites/11/2023/02/OpenWallet-Foundation-Overview.pdf)
      - 41 listed current sponsors
      - 7 million draft budget?
      - Funding state? Will fundraising match needs?
      - Difficulty of orgs being members of All The Things.
        
        - Time
        - Money
    - Project Support from Hyperledger
      
      - Hyperledger social reach is larger
      - Training workshop organized by HyperLedger
    - Code and Standards being co-located in the same org is difficult
    - Aries implementing standards designed outside of Aries
      
      - mDL
      - OpenID4VerifiableCredentials
      - Beyond Aries?
    - OWF explicitly does not want to create standards, OWF core is creating code to implement standards
    - Perception of the scope of Aries? What Aries does/is:
      
      - RfCs
      - Code matching RfCs
      - Interop Profiles
    - ToDo: More clearly communicate what Aries does, also towards OWF

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

[https://youtu.be/ed58MI2Mviw](https://youtu.be/ed58MI2Mviw)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [GMT20230517-140514\_RecordingnewChat.txt](attachments/18505039/18518085.txt "Download")

May 17, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

File [GMT20230517-140514\_Recording.transcript.vtt](attachments/18505039/18518090.vtt "Download")

May 17, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
