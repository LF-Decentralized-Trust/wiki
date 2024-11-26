1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-05-31 Aries Working Group Call

Created by Sam Curren, last modified by Ry Jones on May 31, 2023

## Summary:

- Wallet VS Agent
- Scope and purpose of Aries

## Date

31 May 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;
- [Mike Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5ea322540d58350c2b066eeb?ref=confluence) (Indicio) &lt;mike@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Tim Bloomfield](https://lf-hyperledger.atlassian.net/wiki/people/5a70c8faa02421507dce29c3?ref=confluence) &lt;tim.bloomfield@ontario.ca&gt;
- [John Jordan](https://lf-hyperledger.atlassian.net/wiki/people/557058:1368af8b-9c11-4aa7-9519-52fcc6683f1f?ref=confluence) (BC Gov) &lt;john.jordan@gov.bc.ca&gt;
- [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence) (BC Gov) &lt;alex.metcalf@gov.bc.ca&gt;
- [Ken Ebert](https://lf-hyperledger.atlassian.net/wiki/people/70121:2cc4df0e-16de-40dc-ba52-09649099759a?ref=confluence)  (Indicio) &lt;ken@indicio.tech&gt;
- [Charles Lanahan](https://lf-hyperledger.atlassian.net/wiki/people/712020:50e56df1-41cf-415b-a802-ae0b89b9c75b?ref=confluence) &lt;charles.lanahan@gmail.com&gt;
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) (Animo) &lt;karim@animo.id&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)  (Animo) &lt;timo@[animo.id](http://animo.id)&gt;
- [Micah Peltier](https://lf-hyperledger.atlassian.net/wiki/people/6142380532c0cb006a9aa872?ref=confluence) (Indicio) &lt;micah@indicio.tech&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) (BC Gov / Petri Dish Development) &lt;amanji@petridish.dev&gt;
- [Maki Kato](https://lf-hyperledger.atlassian.net/wiki/people/557058:a7411769-6fd5-4123-8c6c-8366170983ea?ref=confluence) (Matrix Group International) &lt;mkato@matrixgroup.net&gt;
- [jkrupicka](https://lf-hyperledger.atlassian.net/wiki/people/712020:b1b8c987-e425-419a-908b-4ea45beea06a?ref=confluence) (Matrix Group International) &lt;jkrupicka@matrixgroup.net&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Welcome / Introductions)

## Announcements

- June 7-9 [https://diceurope.org/](https://diceurope.org/)
- Hackathon – [https://didhack.xyz/](https://didhack.xyz/) – need an Aries Developer to monitor Discord to answer questions from participants
- [AnonCreds Workshop](https://zoom.us/meeting/register/tJAqcOCurDstHdIAWH0mbPz2hLK55OPr1Hj_?utm_campaign=Hyperledger%20workshops&utm_content=246078071&utm_medium=social&utm_source=twitter&hss_channel=tw-2512683048#/registration) May 31, 2023 08:00 AM PDT

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

- Observations - VC Myopathy vs a focus on the results.
  
  - DIDComm is a large differentiator here
  - Also generally (and possibly unrelatedly?) associated with privacy features of VCs (this may be historical?)
- Wallet vs Agent
  
  - Agents
    
    - Non walletey protocols - q/a, basicmessage
    - protocols for interaction
    - Broader term than wallet
    - wallet with extra capabilities?
    - rich interactions, some of which involve keys and credentials.
  - Wallet
    
    - sometimes used for mobile devices
    - sometimes refers to the key/credential management functions
    - part of an app built for a larger purpose
    - much stronger term to those outside our sphere - easier to relate to
    - credentials are the easiest to grasp concept - first point of traction.
    - 'My' wallet - not wallet others have for me.
    - Business wallets different from personal wallets, but still super important for similar reasons.
    - Can we call it a 'smart' wallet?
    - key management / credential mangement
    - Overloading wallet is ok?
  - Misc
    
    - The term 'phone' has changed. The iPhone has a 'phone' app.
    - Real people don't care what it's called?
    - They care about what it does for them.
    - Context matters in what terms we use and when.

<!--THE END-->

- Open Wallet Foundation
  
  - Tracy Kuhrt - [https://discord.com/channels/905194001349627914/1108478336751108127](https://discord.com/channels/905194001349627914/1108478336751108127)
  - Important Things (opinion of Sam)
    
    - Continuity of Community
      
      - Meetings, Wikis, Calls, Calendars
      - All existing people, work continues with as little disruption as possible.
      - This should not be an issue, as long as organizational support is present.
    - Continuity of Brand
      
      - Aries as a brand needs to live in only one place, at least for the near future.
      - Wiki Page: [Hyperledger Aries](Hyperledger-Aries_18481154.html) (wiki page)
      - Announcement Post: [https://www.hyperledger.org/blog/2019/05/14/announcing-hyperledger-aries-infrastructure-supporting-interoperable-identity-solutions](https://www.hyperledger.org/blog/2019/05/14/announcing-hyperledger-aries-infrastructure-supporting-interoperable-identity-solutions)
    - Promotion of Community
- Notes from this meeting
  
  - Items that are expected by the community from OpenWallet Foundation
    
    - Education
    - Webinars
    - Blogs
    - Meetups
  - Marketing committee (Helen)
    
    - long overdue work that could help clarify Aries brand.
    - Hyperledger brand refresh under way (late June)
  - Two topics
    
    - Aries scope
      
      - What is it
        
        - Set of frameworks that can work with protocols, credential types, crypto, etc. from a wide variety of sources. - John Jordan
        - SSI built on top of DIDComm, primarily using HL Indy - Timo (what it is now)
          
          - Has grown past that - Andre
        - My own interpretation is that Aries is the protocol which verifiable credentials are issued, held, and presented. Right now the protocol is didcomm/anoncreds/indy based. But those are evolving to be abstracted and support other standards (transport, credential format/type, and ledger agnostic) - Clecio
        - foundation / underpinning is indy, anoncreds, and didcomm. Perception outside our group is that Aries IS those things. - Warren
        - Wallet vs Agent terms
      - What happens if work exceeds that scope?
    - Potential move to OWF
  - What is the pitch from OWF?
    
    - (every other week is a conflict for the OWF Technical Advisory Council)
  - Aries is a few things (mechanically)
    
    - Software
    - Protocol Design
    - Aries Interop Profile
    - Interop Testing
    - OCA
- Notes from last meeting on the topic 
  
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

[https://youtu.be/fiGquV7hEkQ](https://youtu.be/fiGquV7hEkQ)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [2023 05 31 Aries WG.txt](attachments/18505335/18518167.txt "Download")

May 31, 2023 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
