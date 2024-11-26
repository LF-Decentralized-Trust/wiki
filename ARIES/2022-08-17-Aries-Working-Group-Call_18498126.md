1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-08-17 Aries Working Group Call

Created by Stephen Curran, last modified on Aug 17, 2022

## Summary:

- Unrevealed Attributes
- Issuer encoding strings that are integers
- Interopathon Planning
- Other topics

## Date

17 Aug 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Helen Garneau](https://lf-hyperledger.atlassian.net/wiki/people/60209b07618001006995b244?ref=confluence) (Indicio) &lt;helen@indicio.tech&gt;
- [Bruno Hivert](https://lf-hyperledger.atlassian.net/wiki/people/712020:0ef3e380-8e1e-45be-82e1-708b65f236da?ref=confluence)([https://idlab.org)](https://idlab.org%29) &lt;bruno.hivert@idlab.org&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence)(RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID) &lt;rodolfo.miranda@rootsid.com&gt;

## Welcome / Introductions

## Announcements

- Aries Interop-a-thon: August 31 7:00 am to 11:00 am MDT
  
  - Sign up here: [https://forms.gle/yrhYTocTe6iEXWbw6](https://forms.gle/yrhYTocTe6iEXWbw6)
  - Register for Zoom here: [https://indicio-tech.zoom.us/meeting/register/tZMtde6trzwvE9IptkYg\_rcUsNm6M4b0mtYJ](https://indicio-tech.zoom.us/meeting/register/tZMtde6trzwvE9IptkYg_rcUsNm6M4b0mtYJ)
- [Hyperledger Global Forum](https://www.hyperledger.org/), Dublin, Sept. 12-14
  
  - Hyperledger Member Summit Sept 11
  - ToIP Member Summit, Sept. 14
- [Rebooting Web of Trust](https://www.weboftrust.info/), Den Haag, September 26-30

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
    
    - Version 0.2.2 released - follow up to major 0.2.0 release
    - Working on 0.3.0 release
      
      - Generalization - only need formats required to be supported in an instance
      - Documentation site!!!
      - Present Proof v2 - merged today - AnonCreds done, W3C JSON-LD VCs still in progress/DIF PE
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
    
    - Aries Framework JavaScript 0.2.0 now merged into Aries Bifold
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
- [aries-endorser-server](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries-Toolbox](https://github.com/hyperledger/aries-toolbox)
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Discussion Topics

- Handling unrevealed attributes – ACA-Py Issue [1893](https://github.com/hyperledger/aries-cloudagent-python/issues/1893)
- Encoding integer strings – AFJ Issue [883](https://github.com/hyperledger/aries-framework-javascript/issues/883)
- Interopathon Steps (Notes from last time)
  
  - Plan Review
  - Project goals in preparation
  - Wiki: [Interoperability Event](https://lf-hyperledger.atlassian.net/wiki/spaces/events/pages/21793489/Interoperability+Event)
  - Planning Doc: [https://docs.google.com/document/d/1J17OWi5u77zUHT3ALNGCpFNV1TNzH32gtBRFrSD4g7U/edit](https://docs.google.com/document/d/1J17OWi5u77zUHT3ALNGCpFNV1TNzH32gtBRFrSD4g7U/edit)
  - Room Host Sign up here: [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/spreadsheets/d/1sWhOS1Eq3gk1wwYHx2qeOxupoktE0KsxlrEPw6jFaew/edit?usp=sharing)[![](plugins/servlet/confluence/placeholder/unknown-macro)](https://identity.foundation/trust-establishment/)
  - Attendee registration form: [https://docs.google.com/forms/d/e/1FAIpQLSd2-0Q9ysAbUiILNuyuIbXumBqS6xxSGfxJgHOYRUn2bLU5lg/viewform](https://docs.google.com/forms/d/e/1FAIpQLSd2-0Q9ysAbUiILNuyuIbXumBqS6xxSGfxJgHOYRUn2bLU5lg/viewform)
  - Aries Interop Planning
    
    - Proposed date: August 31 7:00 am to 11:00 am MDT
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
      - Mobile back channel - use and improve (see [ticket](https://github.com/hyperledger/aries-agent-test-harness/issues/479) logged by [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence))
    - Outcomes:
      
      - Improved coverage of the Aries Agent Test Harness
      - Improved reporting / coverage of mobile test results
      - New Discoveries
      - Better ideas
      - Surface Assumptions
      - Gather best practices (add to DIDComm Book?)
  
  <!--THE END-->
  
  - Follow-up

## Other Business

## Future Topics'

- Aries Interop-a-thon planning
  
  - Aries Test Harness Demo, to prepare us?
    
    - IDLab suggested [demo recording](https://lf-hyperledger.atlassian.net/wiki/download/attachments/18496997/video1383435188.mp4?version=1&modificationDate=1657226562000&api=v2) (starting around the 3 minutes mark, from [this](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2022-07-07+AATH-AMTH+Users+Group+Meeting) AATH-AMTH user group meeting)
- Proxy Ledger Access Followup
- decorator for redirection after proofs. - existing?
- Standardized attribute names for AnonCreds - alignment with VC data model. (Paul Bastian)
  
  - terms and conditions (as link)
  - machine-readable governance?

## Action items

## Call Recording

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18498126/18516636.txt "Download")

Aug 17, 2022 by [Stephen Curran](/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18498126/18516636.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [recording.conf](attachments/18498126/18516637.conf) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498126/18516634.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498126/18516635.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
