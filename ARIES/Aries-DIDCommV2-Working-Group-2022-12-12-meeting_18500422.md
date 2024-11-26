1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries DIDCommV2 Working Group](Aries-DIDCommV2-Working-Group_18499949.html)

# Hyperledger Aries : Aries DIDCommV2 Working Group 2022-12-12 meeting

Created by Lance Byrd, last modified by James Ebert on Dec 14, 2022

## Zoom: [https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09](https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09)

## Summary:

- Introduction
- Updates
- DIDCommV2 survey
- AIP3

## Date

12 Dec 2022 (6AM Los Angeles, 9AM New York, 2PM London, 3PM CET, 17H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence) (Technische Universität Berlin) &lt;hakan.yildiz@tu-berlin.de&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Brigham Young University) &lt;bruce\_conrad@byu-edu&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Aries Agent Test Harness ([https://aries-interop.info](https://aries-interop.info))
- Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
- Frameworks:
  
  - Aries-CloudAgent-Python ([https://github.com/hyperledger/aries-cloudagent-python,](https://github.com/hyperledger/aries-cloudagent-python,) Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html))
  - Aries-Framework-JavaScript ([https://github.com/hyperledger/aries-framework-javascript,](https://github.com/hyperledger/aries-framework-javascript,) Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html))
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
  - Picos as Aries agents (DIDComm v1: [https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico) ; DIDComm v2 work in progress)
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
  
  - working on Pickup support
- [Aries-Toolbox](https://github.com/hyperledger/aries-toolbox)
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Discussion Topics

- Introduction
- Our current spreadsheet [https://docs.google.com/spreadsheets/d/15noWiG\_zhhUpornhrZm9cLEjQ1aa6z9qgJgPCaaIbtY/edit?usp=sharing](https://docs.google.com/spreadsheets/d/15noWiG_zhhUpornhrZm9cLEjQ1aa6z9qgJgPCaaIbtY/edit?usp=sharing)
- AIP3
  
  - [HackMD from the last Aires WG meeting, regarding AIP 3.0](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
  - [Great document by Hakan](https://docs.google.com/document/d/1piGZ-0FW9DWEFRetviV1Vjxv7DDkIFQDWUs38VGqZ-Y/edit?usp=sharing), looking at past AIP definitions and beginning to consider AIP3 definition
  - Connectionless DIDComm v2 still needs management of the 'connection' between agents.  How should agents handle this?
    
    - Is this worth detailing/discussing or is it just agent specific?
    - OOB/handshake/discovery RFP for Aries agents?
      
      - WACI and what the overlap and distinction would be between the AIP and WACI.
        
        - There is some nuance to cred formats you have to support (Indy, BBS+, LD).
        - Can we use Discovery protocol to understand the level of WACI support?
          
          - perhaps we need more detailed information from the discovery protocol
          - per application protocol supported (formats, messages, crypto).
          - Some WACI information to consider [https://identity.foundation/waci-presentation-exchange/#format-property](https://identity.foundation/waci-presentation-exchange/#format-property).
      - Discussed DID Exchange for AIP 3. [https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Aires+DIDCommV2+Working+Group+2022-12-05+meeting](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Aires+DIDCommV2+Working+Group+2022-12-05+meeting)
      - Encryption envelope selection
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) is working with students to implement DIDComm v2 in their Pico environment.  Might benefit from JFF work
- DIDComm v2 agent discoverability/interop
  
  - [https://identity.foundation/didcomm-messaging/spec/v2.0/#iana-media-types](https://identity.foundation/didcomm-messaging/spec/v2.0/#iana-media-types)
  - [https://identity.foundation/didcomm-messaging/spec/v2.0/#discover-features-protocol-20](https://identity.foundation/didcomm-messaging/spec/v2.0/#discover-features-protocol-20)
- Documentation in terms of Trust Over IP (ToIP) tech stack?
  
  - [https://trustoverip.org/toip-model/](https://trustoverip.org/toip-model/)
  - Find Drummond's DIDComm v2 stack [https://trustoverip.org/toip-model/](https://trustoverip.org/toip-model/)
  - [https://trustoverip.org/wp-content/uploads/ToIP-Technical-Architecture-Specification-V1.0-PR1-2022-11-14.pdf](https://trustoverip.org/wp-content/uploads/ToIP-Technical-Architecture-Specification-V1.0-PR1-2022-11-14.pdf)
  - [https://github.com/trustoverip/TechArch/blob/main/spec.md](https://github.com/trustoverip/TechArch/blob/main/spec.md)
- ACA-PUG
  
  - Libraries for message envelope (Askar, Python impl, Rust impl)

## Other Business

## Future Topics

## Action items

## Call Recording

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

File [GMT20221212-135836\_Recording.transcript.vtt](attachments/18500422/18517202.vtt "Download")

Dec 19, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

Text File [GMT20221212-135836\_Recording.txt](attachments/18500422/18517203.txt "Download")

Dec 19, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
