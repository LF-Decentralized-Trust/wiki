1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-08-02 Aries Working Group Call

Created by Sam Curren, last modified by Ry Jones on Aug 04, 2023

## Summary:

- Quarterly Update Review
- did:peer:3
- Unqualified DIDs Coordinated Update
- Aries Marketing Update
- Open Discussion

## Date

02 Aug 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence) (BC Gov) &lt;alex.metcalf@gov.bc.ca&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) (BC Gov / Petri Dish Development) &lt;amanji@petridish.dev&gt;
- [Peter Janes](https://lf-hyperledger.atlassian.net/wiki/people/70121:2ec8ae7c-995e-4832-a270-bbf1843e8ba1?ref=confluence) (Abdagon) &lt;peter.janes@abdagon.com&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Jorge Flores](https://lf-hyperledger.atlassian.net/wiki/people/5c3f9ebb8ee3ae5b8b08422f?ref=confluence) (Entidad) &lt;jorge@entidad.io&gt;
- [jkrupicka](https://lf-hyperledger.atlassian.net/wiki/people/712020:b1b8c987-e425-419a-908b-4ea45beea06a?ref=confluence) (Matrix Group International) &lt;jkrupicka@matrixgroup.net&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (BC Gov / Fullboar Creative) &lt;jason.leach@fullboar.ca&gt;

## Welcome / Introductions

## Announcements

Bifold paused for August

AFJ is bi-weekly with meetings (during summer, read: august)

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
  
  - Aries-CloudAgent-Python [https://github.com/hyperledger/aries-cloudagent-python](https://github.com/hyperledger/aries-cloudagent-python), Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html), Documentation: https://aca-py.org
    
    - Release 0.9.0 – with new Release 1.0.0 CredX
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
- [aries-endorser-service](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries-Toolbox](https://github.com/hyperledger/aries-toolbox)

## Discussion Topics

- Aries marketing update - [Helen Garneau](https://lf-hyperledger.atlassian.net/wiki/people/60da2fc7285656006a667081?ref=confluence) [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence)  
  
  - Draft Page: [New Hyperledger Aries Draft](/wiki/pages/createpage.action?spaceKey=ARIES&title=New%20Hyperledger%20Aries%20Draft&linkCreation=true&fromPageId=18506518)
  - HL Staff Marketing this quarter is focused on Identity - HL staff eager to use resources from HL community - reach out to Helen, Sean, etc.
- Aries Quarterly Update - Stephen Curran - Draft in [Google Doc](https://docs.google.com/document/d/1nbhYWib9u9_yTOgSLQY9bxDU-fMNnupLb7P77T0-tgg/edit?usp=sharing) - to be a PR that can be reviewed, commented upon.
- did:peer:3 - Sam
  
  - [https://github.com/decentralized-identity/peer-did-method-spec/pull/55](https://github.com/decentralized-identity/peer-did-method-spec/pull/55)
  - Discover Features did method, stretched to did:peer:3?
- Aries RFCs – PR reviews:
  
  - Unqualified to Qualified DID Community Coordinated Update
    
    - Issues for transforming unqualified DIDs to DIDDoc 3:
      
      - Should we include both a Verification Key and a (derived) Key Agreement Key in the did:peer:2?
        
        - we should ignore this during the transition.
      - What should the DIDComm Messaging "type" be?  "IndyAgent", "did-communications", "DIDCommMessaging"?
        
        - needs research to do the right thing.
  - Goal Codes for simulated Connection-less Presentations
  - AIP 2.0 Clarifications
- Indy VDR / Askar
  
  - Transition from Indy SDK
  - Speed?
- EUDI/ARF Common goals?
  
  - per message in Discord
  - community time would be valuable here
  - +3
- Open Discussion

## Other Business

## Future Topics

- Niels Klomp offered a deeper dive into the openid4vc related flows

<!--THE END-->

- |State-of-union of Aries projects
- decorator for redirection after proofs. - existing?

## Action items

## Call Recording:

- [https://youtu.be/9NsR7BRGeJs](https://youtu.be/9NsR7BRGeJs)
- [2023 08 02 Aries Working Group transcript.txt](attachments/18506518/18518564.txt)
- [2023 08 02 Aries Working Group chat.txt](attachments/18506518/18518565.txt)

## Attachments:

![](images/icons/bullet_blue.gif) [2023 08 02 Aries Working Group transcript.txt](attachments/18506518/18518564.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [2023 08 02 Aries Working Group chat.txt](attachments/18506518/18518565.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
