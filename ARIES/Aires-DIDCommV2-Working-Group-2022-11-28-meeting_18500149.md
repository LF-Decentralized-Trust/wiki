1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries DIDCommV2 Working Group](Aries-DIDCommV2-Working-Group_18499949.html)

# Hyperledger Aries : Aires DIDCommV2 Working Group 2022-11-28 meeting

Created by Lance Byrd, last modified by Ry Jones on Nov 29, 2022

## Zoom: [https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09](https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09)

## Summary:

- Introduction
- Updates
- DIDCommV2 survey

## Date

28 Nov 2022 (6AM Los Angeles, 9AM New York, 2PM London, 3PM CET, 17H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;
- [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence) (Technische Universität Berlin) &lt;hakan.yildiz@tu-berlin.de&gt;
- [Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence) (Animo Solutions) &lt;berend@animo.id&gt;

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
  - Picos as Aries agents ([https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico))
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
- Implementations
  
  - Look over and document Veramo DIDComm v2 impl
  - [Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence) Typescript impl
    
    - No Secret Resolver or DID Resolver
    - Heavily influenced by SICPA Rust impl
      
      - DID Document updates and feedback to the SICPA team
    - Will have examples
  - ACA-py impl
    
    - message structure
    - encryption work coming
    - [add isue\_credential and present\_proof v3 for DIDComm v2](https://github.com/hyperledger/aries-cloudagent-python/pull/2019)
    - didcomm/v2 profile not there yet [https://identity.foundation/didcomm-messaging/spec/#defined-profiles](https://identity.foundation/didcomm-messaging/spec/#defined-profiles) 
      
      - Raise this in other Aries Working Groups (ACA-PUG)
      - Start a draft?
- Aries Agent Test Harness
  
  - Exploring, so far we haven't identified an agent that supports the DIDCommV2 related tests
- Status Updates
  
  - Hakan and Judith -
  - JFF teams
    
    - Flow diagrams [https://github.com/aviarytech/jff-didcomm-issuance/issues/2](https://github.com/aviarytech/jff-didcomm-issuance/issues/2)
    - Is WACI spec sufficient? [https://github.com/decentralized-identity/waci-presentation-exchange/blob/main/issue\_credential/README.md](https://github.com/decentralized-identity/waci-presentation-exchange/blob/main/issue_credential/README.md)
    - [https://github.com/sicpa-dlab/didcomm-rust/issues/91](https://github.com/sicpa-dlab/didcomm-rust/issues/91)
- DIDCommV2 survey
  
  - profiles managed and discovered
  - interoperability fail points

## Other Business

## Future Topics

## Action items

## Call Recording

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

File [GMT20221128-135934\_Recording.transcript.vtt](attachments/18500149/18517090.vtt "Download")

Nov 29, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

Text File [GMT20221128-135934\_Recording.txt](attachments/18500149/18517091.txt "Download")

Nov 29, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
