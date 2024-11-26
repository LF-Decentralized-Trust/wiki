1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-07-20 Aries Working Group Call

Created by Sam Curren, last modified on Aug 04, 2022

## Summary:

- Followups
- Credential... attachments?
- Discussion on Device Binding Attachments and Alternative Solution

## Date

20 Jul 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io) &lt;warren@affinitiquest.io&gt;
- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence) Bundesdruckerei, paul.bastian@bdr.de
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID) &lt;rodolfo.miranda@rootsid.com&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Welcome / Introductions

## Announcements

- Aries Interop-a-thon: proposed for August 31 7:00 am to 11:00 pm MDT
- [Hyperledger Global Forum](https://www.hyperledger.org/), Dublin, Sept. 12-14
- [Rebooting Web of Trust](https://www.weboftrust.info/), Den Hague, September 26-30

Release Status and Work Updates

- Aries Agent Test Harness ([https://aries-interop.info](https://aries-interop.info))
- Aries Shared Components - Indy SDK replacements
  
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs,)
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr,)
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
    
    - 0.2.5 release - performance/load work and testing – specific load errors reduced (down to 0.05% error rate), performance up 11%
- Frameworks:
  
  - Aries-CloudAgent-Python ([https://github.com/hyperledger/aries-cloudagent-python,](https://github.com/hyperledger/aries-cloudagent-python,) Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html))
  - Aries-Framework-JavaScript ([https://github.com/hyperledger/aries-framework-javascript,](https://github.com/hyperledger/aries-framework-javascript,) Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html))
    
    - Version 0.2.1 released - follow up to major 0.2.0 release
    - Working on 0.3.0 release
      
      - Issue Credential / Present Proof v2
      - Merged: OOB / DIDExchange - merged last Friday
      - Merged: Holder revocation with revocation notifications support
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
    
    - Aries Framework JavaScript 0.2.0 now merged into Aries Bifold
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) repo added – a DIDComm Mediator in a Box
- Aries-Toolbox
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Discussion Topics

- Device Binding Alternatives [https://hackmd.io/6hUuZIjGQpeLVAqcxdakZA#comparison-on-hardware-binding-linkage-mechanism](https://hackmd.io/6hUuZIjGQpeLVAqcxdakZA#comparison-on-hardware-binding-linkage-mechanism) - [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)
- Followup
- Credential.... Attachments? -Sam
  
  - Images with hashlink in credential
  - JSON-LD Creds about issuer
  - Questions:
    
    - What do we name these? Attachments is overloaded.
      
      - Sidecars?
    - How do we know which attachments are what?
    - What is expected when attachments are received?
    - Expected UX experience?
      
      - Some are about others (issuer)
      - Some might not want to be revealed, or only if an attribute is shared.

## Other Business

## Future Topics'

- Aries Interop-a-thon planning
- Proxy Ledger Access Followup
- decorator for redirection after proofs. - existing?
- Standardized attribute names for AnonCreds - alignment with VC data model. (Paul Bastian)
  
  - terms and conditions (as link)
  - machine-readable governance?

## Action items

## Call Recording

  File Modified

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
