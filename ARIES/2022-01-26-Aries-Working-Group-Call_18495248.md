1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-01-26 Aries Working Group Call

Created by Robert Mitwicki, last modified by Stephen Curran on Jan 26, 2022

## Summary:

- Microledger: Ambient Provenance Log
- DKMS4SSI - how to bridge centralized world with decentralized via KERI infrastructure
- Update on KERI development (including JTC 19)

## Note: This call was recorded and the recording and chat transcript are at the bottom of the page.

## Date

26 Jan 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Welcome / Introductions

## Announcements

Meeting tomorrow on AnonCreds standardization – 7:00 Pacific / 16:00 CET- Zoom Link [https://us02web.zoom.us/j/82002952109?pwd%3DRlB5NGFUVlBWTzE4MXBKZUtBWjVRUT09](https://us02web.zoom.us/j/82002952109?pwd%3DRlB5NGFUVlBWTzE4MXBKZUtBWjVRUT09)

Release Status and Work Updates

- Aries Protocol Test Suite
- Aries Agent Test Harness
- Aries Shared:
- Aries-CloudAgent-Python
  
  - 0.7.3 Released Monday
  - ACA-Py Issues Reviewed and closed or tragged
- Aries-Framework-Go (Troy) #aries-go
  
  - Working on support for DIDComm v2, Credential Manifest, OOB v2 and v3 credential protocols (for DIDComm v2)
  - [RFC 700](https://github.com/hyperledger/aries-rfcs/pull/700) to enable web wallets
- NEW [aries-service-mediator](https://github.com/hyperledger/aries-mediator-service) repo added – a DIDComm Mediator in a Box
- Aries Mobile Agent React Native
- Aries-CloudAgent-Pico
- Aries-SDK-Ruby (Jack)
- Aries-Framework-DotNet (Tomislav)
- Aries-Toolbox
- Aries-SDK-Java
- Aries-Framework-JavaScript
  
  - New [aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext) repository for extensions
    
    - New package @aries-framework/rest as a rest wrapper around AFJ
  - Work going on for automatic multi indy ledger support
- Rich Schemas and W3C Verifiable Credentials (Brent &amp; Ken)
- Aries-MobileAgent-Xamarin (Aries MAX)
- Ursa

## Notes:

## Discussion Topics

- Microledger: Ambient Provenance Log
- DKMS4SSI - how to bridge centralized world with decentralized via KERI infrastructure
  
  - DKMS Controller client
    
    [https://github.com/THCLab/keri-bindings](https://github.com/THCLab/keri-bindings) (Rust along with Node.JS)
  - Witness service via DNS with HTTP REST API
    
    [https://github.com/THCLab/keri-witness-http](https://github.com/THCLab/keri-witness-http)
  - DKMS discovery based upon DHT (Kademlia)
    
    [https://github.com/THCLab/keri-resolver](https://github.com/THCLab/keri-resolver)
  - Reference implementation of an application DKMS4SSI infrastructureAuthentic Chain Data Container (ACDC) used in TDA as a VC/Attestation
    
    - [https://github.com/THCLab/tda-daemon](https://github.com/THCLab/tda-daemon)
    - [https://github.com/THCLab/acdc-rust](https://github.com/THCLab/acdc-rust)
- Update on KERI development (including JTC 19)
  
  - [https://keri.one/keri-resources/](https://keri.one/keri-resources/)
  - [https://github.com/webOfTrust/keri](https://github.com/webOfTrust/keri)

## Other Business

## Future Topics

## Action items

- [Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)  Bring on the next call information about how ACDC address problems of JSON-LD serialization of RDF

## Call Recording

  File Modified

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
