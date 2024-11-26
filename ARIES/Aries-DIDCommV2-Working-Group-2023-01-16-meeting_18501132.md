1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries DIDCommV2 Working Group](Aries-DIDCommV2-Working-Group_18499949.html)

# Hyperledger Aries : Aries DIDCommV2 Working Group 2023-01-16 meeting

Created by Lance Byrd, last modified by Ry Jones on Feb 14, 2023

## Zoom: [https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09](https://zoom.us/j/94626752608?pwd=K0t4N3VqRzlscTNYajlxMHNPM08yQT09)

## Summary:

- Introduction
- Updates
- DIDCommV2 survey
- AIP3

## Date

16 Jan 2023 (6AM Los Angeles, 9AM New York, 2PM London, 3PM CET, 17H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence) (TU Berlin) &lt;hakan.yildiz@tu-berlin.de&gt;
- [Simon Henriksen](https://lf-hyperledger.atlassian.net/wiki/people/712020:23306fb2-e990-49b4-b9c6-9ef1a17f038b?ref=confluence) (Hyphen) &lt;simon@hyphenapp.xyz&gt;
- [Philip Essy-Ehsing](https://lf-hyperledger.atlassian.net/wiki/people/712020:493a701d-81ff-40c3-9ecd-d35e2f937163?ref=confluence) (Hyphen) &lt;philip@hyphenapp.xyz&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;

## Welcome / Introductions

## Announcements

Release Status and Work Updates

- Aries Agent Test Harness ([https://aries-interop.info](https://aries-interop.info))
- Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
- Frameworks:
  
  - Aries-CloudAgent-Python ([https://github.com/hyperledger/aries-cloudagent-python,](https://github.com/hyperledger/aries-cloudagent-python,) Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html))
    
    - Encryption envelope (Askar impl) not fully-developed yet. We could use different libraries (SICPA Rust). SICPA DIDComm impl is what will be used... resolves did peers natively. The keys will have to be transported out of Askar, but that is acceptable for now. SICPA is the most widely used.
      
      - SICPA for DIDComm and did:peer [https://github.com/sicpa-dlab/didcomm-python](https://github.com/sicpa-dlab/didcomm-python)
      - No near-term Askar support for the DIDComm v2 encryption envelope and core protocols.
    - Protocols related to credential exchange and connection establishment. Distinguish between DIDComm v1 and v2. DID Exchange will be adapted.  The main focus is on Out-of-Band protocol.
    - Very important to extend the AATH.
  - Aries-Framework-JavaScript ([https://github.com/hyperledger/aries-framework-javascript,](https://github.com/hyperledger/aries-framework-javascript,) Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html))
    
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1096#issuecomment-1343833016](https://github.com/hyperledger/aries-framework-javascript/pull/1096#issuecomment-1343833016)
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1211](https://github.com/hyperledger/aries-framework-javascript/pull/1211)
  - Picos as Aries agents (DIDComm v1: [https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico) ; DIDComm v2 work in progress)
    
    - students have returned and they are using SICPA for envelope encryption
    - DIF Picos working group, useful for IoT devices
  - Swift Framework
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
  
  - working on Pickup support

## Discussion Topics

Aries Agent Test Harness

- New tag in AATH that are not credential related, maybe DIDCommV2\_Peer or DIDCommV2\_Simple.
- See [https://github.com/tdiesler/aries-agent-test-harness/tree/camel/aries-backchannels/camel#aip-10-status](https://github.com/tdiesler/aries-agent-test-harness/tree/camel/aries-backchannels/camel#aip-10-status)

AIP3

- [HackMD from the last Aires WG meeting, regarding AIP 3.0](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)

Grand Unified Theory (GUT) Alliance

- Newer than even AIP3.0. KERI and DIDComm v3.0 (likely)
- Link to Daniel’s GUT presentation:
