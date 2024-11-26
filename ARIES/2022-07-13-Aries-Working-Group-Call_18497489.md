1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-07-13 Aries Working Group Call

Created by Sam Curren, last modified by Stephen Curran on Jul 13, 2022

## Summary:

- Device Binding
- AATH Wrapper for Mobile
- Proxy Ledger Access

## Date

13 Jul 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (Sr Dev at AffinitiQuest.io - warren@affinitiquest.io)
- [Regis Eloi](https://lf-hyperledger.atlassian.net/wiki/people/712020:1f85fa5f-ff75-4f77-9f7b-b6eb5244e07f?ref=confluence)  (IDLab) &lt;[regis.eloi@idlab.org](mailto:regis.eloi@idlab.org)&gt;
- [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence) (IDLab) &lt;[patrick.st-louis@idlab.org](mailto:patrick.st-louis@idlab.org)&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;
- [Stéphane Harnois](https://lf-hyperledger.atlassian.net/wiki/people/62546dd59e7380006fb21f9b?ref=confluence)(Gouvernement du Québec) &lt;stephane.harnois@mcn.gouv.qc.ca&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs)&lt;smccown@anonyome.com&gt;
- [Mike Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5ea322540d58350c2b066eeb?ref=confluence)(Indicio) &lt;mike@indicio.tech&gt;
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (Fullboar Creative / BC Gov) &lt;jason.leach@fullboar.ca&gt;
- [Jean-Francois Blier](https://lf-hyperledger.atlassian.net/wiki/people/712020:ade5ffa7-c63b-4953-bc8d-920f85585c86?ref=confluence) (Amplitude Technologies) &lt;jfblier@amplitudetech.com&gt;

## Welcome / Introductions

## Announcements

- Aries Interop-a-thon: proposed for August 31 7:00 am to 11:00 pm MDT
- [Hyperledger Global Forum](https://www.hyperledger.org/), Dublin, Sept. 12-14
- [Rebooting Web of Trust](https://www.weboftrust.info/), Den Hague, September 26-30
- The DIDComm v2 spec has been updated to “DIF Ratified Specification” status! ([https://identity.foundation/didcomm-messaging/spec/](https://identity.foundation/didcomm-messaging/spec/))
  
  - [DIDComm Guide Book](https://didcomm.org/book/v2/) also available

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

- AATH Wrapper for testing Mobile Wallet - IDLab
- Proxy Ledger Access Followup

## Other Business

## Future Topics'

- Device Binding Alternatives [https://hackmd.io/6hUuZIjGQpeLVAqcxdakZA#comparison-on-hardware-binding-linkage-mechanism](https://hackmd.io/6hUuZIjGQpeLVAqcxdakZA#comparison-on-hardware-binding-linkage-mechanism) - [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)
- Aries Interop-a-thon planning
- Proxy Ledger Access Followup
- decorator for redirection after proofs. - existing?
- Standardized attribute names for AnonCreds - alignment with VC data model. (Paul Bastian)
  
  - terms and conditions (as link)
  - machine-readable governance?

## Action items

## Call Recording

- [dummyfile.txt](#)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18497489/18516486.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
