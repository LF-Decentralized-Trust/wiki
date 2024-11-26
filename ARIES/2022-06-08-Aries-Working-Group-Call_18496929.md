1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-06-08 Aries Working Group Call

Created by Sam Curren, last modified by Mike Ebert on Jul 06, 2022

## Summary:

- URL Shortening Clarifications
- Interopathon?

## Date

08 Jun 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;
- [Mike Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5ea322540d58350c2b066eeb?ref=confluence)  (Indicio) &lt;mike@indico.tech&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Regis Eloi](https://lf-hyperledger.atlassian.net/wiki/people/712020:1f85fa5f-ff75-4f77-9f7b-b6eb5244e07f?ref=confluence)(IDLab) &lt;regis.eloi@idlab.org&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsId) &lt;rodolfo.miranda@rootsid.com&gt;

## Welcome / Introductions

## Announcements

- Cardea Interopathon June 16 (includes basic protocol testing–connection using connections v.1 and OOB invitations, issuance, presentations, basic message, question and answer). Registration [link](https://docs.google.com/forms/d/e/1FAIpQLScth275phIVSZfPewkBiY1Vzf0p2U_XHq3iKNrraz_a0LRoSw/viewform?_hsmi=214925417&_hsenc=p2ANqtz-8EQka4xy1rgTGhMF1Wqcf9lwSApoNGiw7Y2Oi1h8FOVPp1EmrQk4R5P5dCoxYvbiZur4VwG6eYFdZXMtwX9NhWpW1Uqg).
- Components looking for maintainership (as a result of Kiva sunsetting Kiva Protocol, see blog [here](https://www.kiva.org/blog/sunset-kiva-protocol))
  
  - Mobile Agent Xamerin (MAX - Legacy?)
  - Aries Framework .Net
  - Fingerprint Component
  - ACA-Py Components for onboarding
  - Reach out to Nathan, Cam, or Horatio

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
- [aries-service-mediator](https://github.com/hyperledger/aries-mediator-service) repo added – a DIDComm Mediator in a Box
- Aries-Toolbox
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Notes:

## Discussion Topics

- [PR #738](https://github.com/hyperledger/aries-rfcs/pull/738) URL Shortening Clarifications - Kolby
- Interopathon - Mike
  
  - Late August
    
    - TODO: Date Selection
  - Followup in proximity to Hyperledger Global Forum (Dublin)
  - Followup prior to November IIW
  - 3-4 hour time window
  - Targets
    
    - 557 Discover Features
    - 048 Trust Ping
    - 434 OOB
    - 023 DID Exchange
  - Bonus Targets
    
    - 455 Issue
    - 454 Present
    - 183 Revocation Notification
  - Outcomes
    
    - Improved coverage of Test Harness
    - Improved reporting / coverage of Mobile test results
    - New Discoveries
    - Better ideas
    - Surface Assumptions
    - Gather Best practices (add to DIDComm Book?)
- [PR #692](https://github.com/hyperledger/aries-rfcs/pull/692) - Multiple Issuance

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

Text File [chat.txt](attachments/18496929/18516358.txt "Download")

Jun 08, 2022 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18496929/18516358.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496929/18516359.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496929/18516357.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
