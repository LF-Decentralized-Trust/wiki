1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-09-06 Aries Working Group Call

Created by Sam Curren, last modified by Ry Jones on Sep 06, 2023

## Summary:

- Unqualified DIDs
- DIDComm v2
- Push Notifications

## Date

06 Sep 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)  (Indicio) &lt;sam@indicio.tech&gt;
- [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence) (BC Gov) &lt;alex.metcalf@gov.bc.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio) &lt;colton@indicio.tech&gt;

## Welcome / Introductions

## Announcements

DIF DIDComm Users Group Meets 2,3, and 4th Mondays: [https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.md](https://github.com/decentralized-identity/didcomm-usergroup/blob/main/schedule.md)

TOIP - DID:webs DID method compatible with did:web but adds some security in the form of KERI audit logs - Repo: [https://github.com/dhh1128/did-method-webs](https://github.com/dhh1128/did-method-webs), published spec: [https://dhh1128.github.io/did-method-webs/index.html](https://dhh1128.github.io/did-method-webs/index.html)

Indy Summit Sept 7th Thursday 6:00 Pacific / 15:00 Central Europe - [Register Here](https://zoom.us/meeting/register/tJAscumprD8rEtBbf4Gyt7vnelTGhpZrcckJ).

Oct 10-12 IIW

HL Member Summit Oct 23 in SF and Tokyo

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
    
    - Release 0.10.1 released yesterday. Notice to go out – [Changelog Entry](https://github.com/hyperledger/aries-cloudagent-python/blob/main/CHANGELOG.md#0101).
      
      - Fun times with PyPi forced the need for 0.10.1 after 0.10.0.
  - Aries-Framework-JavaScript [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript), Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
    
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

## Discussion Topics

- New Meeting Link - Check the HL Calendar for updaets.
- Aries marketing update - [Helen Garneau](https://lf-hyperledger.atlassian.net/wiki/people/60da2fc7285656006a667081?ref=confluence) [Alex Metcalf](https://lf-hyperledger.atlassian.net/wiki/people/70121:e519cb5b-f9e4-4e87-b5f7-bc99fea74168?ref=confluence)  
  
  - New Wiki page going live shortly: [New Hyperledger Aries Draft](/wiki/pages/createpage.action?spaceKey=ARIES&title=New%20Hyperledger%20Aries%20Draft&linkCreation=true&fromPageId=18507315)
  - Longer description being added to Aries landing page on Hyperledger website, based on above Wiki page content: [https://www.hyperledger.org/projects/aries](https://www.hyperledger.org/projects/aries)
  - We are exploring resource for short Aries introductory animated video
  - Join our marketing working group meeting, last Tuesday of every month: [Aries Marketing Working Group](Aries-Marketing-Working-Group_18505802.html)
- Unqualified DIDs
  
  - DID Rotation
    
    - [https://github.com/hyperledger/aries-rfcs/pull/794](https://github.com/hyperledger/aries-rfcs/pull/794)
  - did:peer:4
    
    - [https://github.com/decentralized-identity/peer-did-method-spec/issues/58](https://github.com/decentralized-identity/peer-did-method-spec/issues/58)
  - DID Exchange with no DID Document / Signature - [https://github.com/hyperledger/aries-rfcs/issues/717](https://github.com/hyperledger/aries-rfcs/issues/717)
  - Community Coordinated Update
  - Aries Agent Test Harness update for testing support
- DIDComm v2
  
  - Urgency
- Push Notifications - Stephen
- Open Discussion

## Other Business

## Future Topics

- Niels Klomp offered a deeper dive into the openid4vc related flows

<!--THE END-->

- |State-of-union of Aries projects
- decorator for redirection after proofs. - existing?
- in the [Aug 9 call](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2023-08-09+Aries+Working+Group+Call?src=contextnavpagetreemode) there was talk about EUDI compatibility. Maybe tracking the progress every now and then in these calls? Has there been any discussion about adding SD-JWT and OID4VC stuff to Aries Interop test suite?

## Action items

## Call Recording:

- [https://youtu.be/6E8-dySCq3c](https://youtu.be/6E8-dySCq3c)
- [2023 09 06 Aries Working Group Call.txt](attachments/18507315/18518666.txt)

## Attachments:

![](images/icons/bullet_blue.gif) [2023 09 06 Aries Working Group Call.txt](attachments/18507315/18518666.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
