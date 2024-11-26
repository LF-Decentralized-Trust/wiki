1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-09-14 Aries Working Group Call

Created by Lance Byrd, last modified on Sep 14, 2022

## Summary:

- ActionMenu
- AnonCreds
- PR Review

## Date

14 Sep 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io) &lt;warren@affinitiquest.io&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence)(Indicio) &lt;colton@indicio.tech&gt;
- [Regis Eloi](https://lf-hyperledger.atlassian.net/wiki/people/712020:1f85fa5f-ff75-4f77-9f7b-b6eb5244e07f?ref=confluence) (IDLab) &lt;[regis.eloi@idlab.org](mailto:regis.eloi@idlab.org)&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) &lt;a@[2060.io](http://2060.io)&gt;

## Welcome / Introductions

## Announcements

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
    
    - Version 0.2.4 released - bugfixes and ActionMenu support
    - Working on 0.3.0 release
      
      - Generalization - only need formats required to be supported in an instance
      - Documentation site!!!
      - Present Proof v2 - merged today - AnonCreds done, W3C JSON-LD VCs still in progress/DIF PE
      - Basic support for AIP 2.0
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
    
    - Aries Framework JavaScript 0.2.2 now merged into Aries Bifold
    - BCGov has realeased an Aries Bifold version, rebranded w/ BC blue/theme/etc (BC wallet)
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
  
  - working on Pickup support
- [aries-endorser-server](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries-Toolbox](https://github.com/hyperledger/aries-toolbox)
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Discussion Topics

- ActionMenu further discussions
  
  - [https://didcomm.org/search/?page=1](https://didcomm.org/search/?page=1)
  - [https://github.com/blu3beri/hgf-demo-wallet](https://github.com/blu3beri/hgf-demo-wallet)
- AnonCreds
  
  - For context, [AnonCreds overview and specifications](https://github.com/AnonCreds-WG/anoncreds-spec)
  - [Kaliya's post](https://identitywoman.net/being-real-about-hyperledger-indy-aries-anoncreds/)
  - [Daniel Hardman's post](https://daniel-hardman.medium.com/response-to-kaliyas-being-real-post-13fddb9410f0)
  - [Northern Block's post](https://northernblock.io/learnings-from-aries-indy-and-various-verifiable-credential-implementations/)
  - [Indicio's post](https://indicio.tech/hyperledger-aries-is-the-present-and-the-future-of-internet-scale-trusted-verifiable-credential-ecosystems/)
  - [Trinsic's post](https://trinsic.id/moving-toward-identity-technology-ready-for-mass-adoption/)
- PRs
  
  - [ACA-py outbound webhooks - data size](https://github.com/hyperledger/aries-cloudagent-python/pull/1941)

## Other Business

## Future Topics'

- State-of-union of Aries projects
- OIDC Credential Exchange in Aries - Mike Richardson
- Proxy Ledger Access Followup
- decorator for redirection after proofs. - existing?
- Standardized attribute names for AnonCreds - alignment with VC data model. (Paul Bastian)
  
  - terms and conditions (as link)
  - machine-readable governance?
- Multiple sigs on a credential - Shivam Sethi

## Action items

## Call Recording

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18498576/18516734.txt "Download")

Sep 14, 2022 by [Lance Byrd](/wiki/people/6346b13f754fb6b373b9af19)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18498576/18516734.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [recording.conf](attachments/18498576/18516735.conf) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498576/18516736.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498576/18516733.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
