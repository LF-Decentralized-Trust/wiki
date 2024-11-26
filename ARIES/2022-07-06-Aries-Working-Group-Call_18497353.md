1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-07-06 Aries Working Group Call

Created by Sam Curren, last modified by Mike Ebert on Jul 13, 2022

## Summary:

- Device Binding
- Proxy Ledger Access

## Date

06 Jul 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;
- [Mike Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5ea322540d58350c2b066eeb?ref=confluence)(Indicio) &lt;mike@indicio.tech&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;
- [Stéphane Harnois](https://lf-hyperledger.atlassian.net/wiki/people/62546dd59e7380006fb21f9b?ref=confluence) (Gouvernement du Québec) &lt;stephane.harnois@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca)&gt;
- [Regis Eloi](https://lf-hyperledger.atlassian.net/wiki/people/712020:1f85fa5f-ff75-4f77-9f7b-b6eb5244e07f?ref=confluence) (IDLab) &lt;[regis.eloi@idlab.org](mailto:regis.eloi@idlab.org)&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence)(RootsID) &lt;lance.byrd@rootsid.com&gt;
- Thomas Diesler(RedHat) &lt;tdiesler@redhat.com&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID) &lt;rodolfo.miranda@rootsid.com&gt;
- [José-Luis Pumahuanca](https://lf-hyperledger.atlassian.net/wiki/people/6256d62c13c2c8006a36474c?ref=confluence)(Gouvernement du Québec) &lt;joseluis.pumahuancacarrion@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca)&gt;
- @ Martin St-Pierre (Gouvernement du Québec) &lt;martin.st-pierre@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;

## Welcome / Introductions

## Announcements

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
    
    - Working on 0.3.0 release
      
      - Issue Credential / Present Proof v2
      - Merged: OOB / DIDExchange - merged last Friday
      - Merged: Holder revocation with revocation notifications support
    - PR open to support lower versions of a protocol
    - Nearing completion for JSON-LD and BBS+ credential support
    - Started working on writing a wrapper for Indy VDR for React Native – Almost ready now
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html)) 
    
    - Working on support for DIDComm v2, Credential Manifest, OOB v2 and v3 credential protocols (for DIDComm v2)
    - [RFC 700](https://github.com/hyperledger/aries-rfcs/pull/700) to enable web wallets
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) repo added – a DIDComm Mediator in a Box
- Aries-Toolbox
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Discussion Topics

- Device Binding Alternatives [https://hackmd.io/6hUuZIjGQpeLVAqcxdakZA#comparison-on-hardware-binding-linkage-mechanism](https://hackmd.io/6hUuZIjGQpeLVAqcxdakZA#comparison-on-hardware-binding-linkage-mechanism) - Paul
- Proxy Ledger Access Further Discussion - Stephen Curran - ([Slides](https://docs.google.com/presentation/d/1-CgRzMn10kYLnLOZVVQX4tAmG6f0E9b0O4Ybkcf-o70/edit?usp=sharing) from last week)
  
  - Will bring up on the AFJ call tomorrow - Jason
- Aries Interop Planning
  
  - Proposed date: August 31 7:00 am to 11:00 pm MDT
  - Targets:
    
    - 557 Discover Features
    - 048 Trust Ping
    - 434 OOB
    - 023 DID Exchange
    - OOB Reuse
  - Bonus Targets:
    
    - 455 Issue
    - 454 Present
    - 183 Revocation Notification
  - Preparation
    
    - Connection with existing test harness
    - Mobile back channel - use and improve (see [ticket](https://github.com/hyperledger/aries-agent-test-harness/issues/479) logged by [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence))
  - Outcomes:
    
    - Improved coverage of the Aries Test Harness
    - Improved reporting / coverage of mobile test results
    - New Discoveries
    - Better ideas
    - Surface Assumptions
    - Gather best practices (add to DIDComm Book?)

## Other Business

## Future Topics'

- Aries Interopathon planning
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
