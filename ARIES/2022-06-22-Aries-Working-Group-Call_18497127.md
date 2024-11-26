1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-06-22 Aries Working Group Call

Created by Sam Curren, last modified by Thomas Diesler on Jun 22, 2022

## Summary:

- Apache Camel Demo
- OCA (Overlay Capture Architecture) with Aries &amp; AnonCreds
- Discussion Device Binding Alternatives

## Date

22 Jun 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;
- [Regis Eloi](https://lf-hyperledger.atlassian.net/wiki/people/712020:1f85fa5f-ff75-4f77-9f7b-b6eb5244e07f?ref=confluence)(IDLab) &lt;regis.eloi@idlab.org&gt;
- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence) (Bundesdruckerei) &lt;paul.bastian@bdr.de&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Thomas Diesler](https://lf-hyperledger.atlassian.net/wiki/people/557058:ef106bd5-665a-489d-a319-dfb455bd44c1?ref=confluence)(RedHat) &lt;tdiesler@redhat.com&gt;

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

## Notes:

I track stuff for the initial release in this milestone  
[https://github.com/tdiesler/nessus-aries/milestone/1](https://github.com/tdiesler/nessus-aries/milestone/1)

The plain Java impl of the Alice workflow is here  
[https://github.com/tdiesler/nessus-aries/blob/main/itests/smoke/src/test/java/io/nessus/aries/test/AriesGettingStartedTest.java#L82](https://github.com/tdiesler/nessus-aries/blob/main/itests/smoke/src/test/java/io/nessus/aries/test/AriesGettingStartedTest.java#L82)

The Camel equivalent is here  
[https://github.com/tdiesler/camel/blob/CAMEL-18156/components/camel-hyperledger-aries/src/test/java/org/apache/camel/component/aries/CamelGettingStartedTest.java#L86](https://github.com/tdiesler/camel/blob/CAMEL-18156/components/camel-hyperledger-aries/src/test/java/org/apache/camel/component/aries/CamelGettingStartedTest.java#L86)

The Camel component doc page is here (this will get formatted to Camel style automatically)  
[https://github.com/tdiesler/camel/blob/CAMEL-18156/components/camel-hyperledger-aries/src/main/docs/hyperledger-aries-component.adoc](https://github.com/tdiesler/camel/blob/CAMEL-18156/components/camel-hyperledger-aries/src/main/docs/hyperledger-aries-component.adoc)

The demo readme is here  
[https://github.com/tdiesler/nessus-aries/blob/main/demo/README.md](https://github.com/tdiesler/nessus-aries/blob/main/demo/README.md)

The code is here  
[https://github.com/tdiesler/nessus-aries/tree/main/demo/src/main/java/io/nessus/aries/demo](https://github.com/tdiesler/nessus-aries/tree/main/demo/src/main/java/io/nessus/aries/demo)

## Discussion Topics

- Apache Camel Demo - Thomas from Red Hat
- OCA (Overlay Capture Architecture) with Aries &amp; AnonCreds - Stephen Curran
- Discussion Device Binding Alternatives [https://hackmd.io/6hUuZIjGQpeLVAqcxdakZA#comparison-on-hardware-binding-linkage-mechanism](https://hackmd.io/6hUuZIjGQpeLVAqcxdakZA#comparison-on-hardware-binding-linkage-mechanism) (2 weeks out)

## Other Business

## Future Topics

- decorator for redirection after proofs. - existing?
- Standardized attribute names for AnonCreds - alignment with VC data model. (Paul Bastian)
  
  - terms and conditions (as link)
  - machine-readable governance?

## Action items

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18497127/18516387.txt "Download")

Jun 23, 2022 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18497127/18516387.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18497127/18516388.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18497127/18516386.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
