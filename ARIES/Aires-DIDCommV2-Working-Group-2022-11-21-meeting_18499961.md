1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries DIDCommV2 Working Group](Aries-DIDCommV2-Working-Group_18499949.html)

# Hyperledger Aries : Aires DIDCommV2 Working Group 2022-11-21 meeting

Created by Lance Byrd, last modified by Ry Jones on Feb 14, 2023

## Zoom: [https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09](https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09)

## Summary:

- Introduction
- Updates
- IIW
- DIDCommV2 survey

## Date

21 Nov 2022 (6AM Los Angeles, 9AM New York, 2PM London, 3PM CET, 17H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence)
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence)
- [Alex Andrei](https://lf-hyperledger.atlassian.net/wiki/people/70121:00b65a7a-d5d0-4049-86d4-f9d8ebe69b62?ref=confluence)

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
- Status Updates
  
  - Hakan - 
    
    - Backwards compatibility between v1 and v2
    - Connections using v2? Non-Aries and Aries agent compatibility.
      
      - [https://github.com/hyperledger/aries-rfcs/blob/main/features/0160-connection-protocol/README.md](https://github.com/hyperledger/aries-rfcs/blob/main/features/0160-connection-protocol/README.md)
      - If Aries is mandating connections, how do we reconcile the v2 spec which has no concept of connections?
        
        - If issuance is tied to connections
    - We'd like to engage ACA-py, AFJ, Aries Framework Go, and DIF to work through these inconsistencies
    - [https://github.com/hyperledger/aries-cloudagent-python/pull/2019](https://github.com/hyperledger/aries-cloudagent-python/pull/2019)
      
      rfc 160
    - [https://docs.google.com/document/d/1piGZ-0FW9DWEFRetviV1Vjxv7DDkIFQDWUs38VGqZ-Y/edit#](https://docs.google.com/document/d/1piGZ-0FW9DWEFRetviV1Vjxv7DDkIFQDWUs38VGqZ-Y/edit)
    - [https://github.com/hyperledger/aries-rfcs/blob/main/features/0160-connection-protocol/README.md](https://github.com/hyperledger/aries-rfcs/blob/main/features/0160-connection-protocol/README.md)
    - [https://github.com/hyperledger/aries-rfcs/blob/main/features/0434-outofband/README.md](https://github.com/hyperledger/aries-rfcs/blob/main/features/0434-outofband/README.md)
    - [https://github.com/hyperledger/aries-rfcs/blob/main/features/0434-outofband/README.md#invitation-httpsdidcommorgout-of-bandverinvitation](https://github.com/hyperledger/aries-rfcs/blob/main/features/0434-outofband/README.md#invitation-httpsdidcommorgout-of-bandverinvitation)
    - [https://identity.foundation/didcomm-messaging/spec/v2.0/#invitation](https://identity.foundation/didcomm-messaging/spec/v2.0/#invitation)
- IIW Recap
  
  - JFF DIDComm v2 track
    
    - key agreement and encryption problems, preventing interop
  - DIDComm v2 demos
  - DIDComm v2 interop
  - GoDIDdy
    
    - key agreement embedded in the DIDDoc
      
      - dependent on DID method implementation for getting this necessary information
        
        - did:peer provides this
        - did:web does not
- DIDCommV2 survey
  
  - profiles managed and discovered
  - interoperability fail points

## Other Business

## Future Topics

## Action items

## Call Recording

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
