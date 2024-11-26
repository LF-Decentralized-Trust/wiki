1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-11-09 Aries Working Group Call

Created by Sam Curren, last modified by James Ebert on Nov 09, 2022

## Summary:

- Push Notifications
- Error Reporting
- Issue Credential v2.1 learning
- Replacing Indy SDK
- IIW Topics

## Date

09 Nov 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)(Indicio) &lt;sam@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence)(AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) &lt;bruce\_conrad@byu.edu&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;

## Welcome / Introductions

## Announcements

- [IIW](https://www.eventbrite.com/e/internet-identity-workshop-iiwxxxv-35-2022b-tickets-368643531727) (November 15-17)
  
  - No meeting next week!

Release Status and Work Updates

- Aries Agent Test Harness ([https://aries-interop.info](https://aries-interop.info))
- Aries Shared Components - Indy SDK replacements
  
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs,)
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr,)
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
    
    - 0.2.5 release - performance/load work and testing – specific load errors reduced (down to 0.05% error rate), performance up 11%
- Frameworks:
  
  - Aries-CloudAgent-Python ([https://github.com/hyperledger/aries-cloudagent-python,](https://github.com/hyperledger/aries-cloudagent-python,) Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html))
    
    - ACA-Py 1.0.0 RC1 released
      
      - AnonCreds presentations - handling of unrevealed attributes
      - Mediation race conditions
  - Aries-Framework-JavaScript ([https://github.com/hyperledger/aries-framework-javascript,](https://github.com/hyperledger/aries-framework-javascript,) Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html))
    
    - Version 0.2.4 released - bugfixes and ActionMenu support
    - Working on 0.3.0 release - test phase
      
      - Generalization - only need formats required to be supported in an instance
      - Documentation site!!!
      - Present Proof v2 - merged today - AnonCreds done, W3C JSON-LD VCs still in progress/DIF PE
      - Basic support for AIP 2.0
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
  - Picos as Aries agents ([https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico))
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

- Can We Close This? 
  
  - [#745](https://github.com/hyperledger/aries-rfcs/pull/745), [#737](https://github.com/hyperledger/aries-rfcs/pull/737), [#736](https://github.com/hyperledger/aries-rfcs/pull/736) Push Notification PRs (need the right people)
  - #[757](https://github.com/hyperledger/aries-rfcs/pull/757) Push Notification Concept RFC
- Minor Versions / Error Reports
  
  - PR [752](https://github.com/hyperledger/aries-rfcs/pull/752) - agreement to merge this - need approval and announcement on Discord to confirm.
  - PR [756](https://github.com/hyperledger/aries-rfcs/pull/756) - unknown error handling
- IIW Topics?
  
  - Governance Demo - Mike / Simon / Sam
  - AnonCreds as a project
  - Open Wallet Foundation 
    
    - AnonCreds
    - as related to Aries Projects
  - OCA - Stephen
  - Bifold - shipping two apps from the same codebase.
- Replacing Indy SDK
  
  - Enable shared components in all Aries Framework – notable AFJ and Aries VCX
    
    - React Native wrappers for React Native (needed for Bifold)
  - indy-vdr with did:indy support – how do we get that released?
  - indy-vdr is using Ursa, which is using a deprecated Rust module "failure" – [https://github.com/hyperledger/ursa/issues/199](https://github.com/hyperledger/ursa/issues/199); [CVE](https://rustsec.org/advisories/RUSTSEC-2020-0036) - very high score! Possibly not critical for us, but looks bad.
  - Create a migration tool to export indy-wallet contents and load into aries-askar
  - Create a "shared components" version of the Indy CLI
  - Indy Node internals:
    
    - New transaction types in indy-vdr – draft PR, but needs work and testing
    - Indy Test Automation relies on the indy-sdk, needs to be moved to indy-sdk
    - Tools on the indy-node nodes – do they use libindy?  Investigation needed – [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) / [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) to look at/create issue.
  - Community impact on the use of the indy-sdk – a need to migrate

## Other Business

## Future Topics'

- Issue Credential v2.1 learning
- State-of-union of Aries projects
- OIDC Credential Exchange in Aries - Mike Richardson
- decorator for redirection after proofs. - existing?
- Standardized attribute names for AnonCreds - alignment with VC data model. (Paul Bastian)
  
  - terms and conditions (as link)
  - machine-readable governance?
- Multiple sigs on a credential - Shivam Sethi

## Action items

## Call Recording

  File Modified

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18499781/18516991.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18499781/18516992.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
