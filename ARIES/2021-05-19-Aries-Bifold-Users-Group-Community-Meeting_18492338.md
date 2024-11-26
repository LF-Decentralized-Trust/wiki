1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Bifold User Group](Aries-Bifold-User-Group_18490719.html)
5. [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
6. [2021 Bifold Meetings](2021-Bifold-Meetings_18514782.html)

# Hyperledger Aries : 2021-05-19 Aries Bifold Users Group Community Meeting

Created by James Ebert, last modified on May 19, 2021

## Summary:

Planned Topics:

- Code Status
- React Native versioning
- Work Items
- Questions / Discussions

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

Who you are, and what your interest is in the Bifold effort.

## Attendees

- Name (Organization) &lt;email&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)(Animo Solutions) &lt;timo@animo.id&gt;

## Announcements

- Aries Framework JavaScript calls every Thursday at 15:00 CET / 07:00 MST ([Framework JS Meetings](Framework-JS-Meetings_18482467.html))
- Code has moved to Hyperledger! [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)
- SITA, Indicio launch Aruba Health App, built using components of Aries Bifold: [https://www.sita.aero/pressroom/news-releases/sita-indicio-pave-way-to-safer-travel-experience-with-launch-of-aruba-health-app/](https://www.sita.aero/pressroom/news-releases/sita-indicio-pave-way-to-safer-travel-experience-with-launch-of-aruba-health-app/)

## Deployments and Work Updates

- In progress - QR Code generation and presentations - Indicio
  
  - [rn-indy-sdk Present Proof additions](https://github.com/AbsaOSS/rn-indy-sdk/pull/52) in iOS
- Aries Framework JavaScript
  
  - Released [0.0.19-unstable.0](https://www.npmjs.com/package/aries-framework)
  - In Progress - Revocation - Animo
  - In Progress - Mediation (coordinate-mediation) - Indicio
  - Dependency Injection
  - do not connect to ledger on startup -- only when needed
  - genesis transactions instead of genesis path
  - file system implementation
  - internalized WS and HTTP outbound transporters
  - Doing some testing with Electron
  - Custom errors for framework (makes it a lot easier to use the framework)
  - ISSUE: errors we create. Working on it.
- Aries Agent Test Harness (AATH) manual mobile backchannel
- Updating to React Native 0.64.1! [https://github.com/hyperledger/aries-mobile-agent-react-native/pull/45](https://github.com/hyperledger/aries-mobile-agent-react-native/pull/45)
  
  - [https://github.com/hyperledger/indy-sdk/issues/2346#issuecomment-841000640](https://github.com/hyperledger/indy-sdk/issues/2346#issuecomment-841000640)

## Agenda

- Code Status
  
  - Github Project
- React Native 0.64.1 Updates
- Shared Components
  
  - Separated Indy Components in AFJ (with interfaces)
  - Ledger operations - Indy VDR, Indy VDR as Proxy, Indy SDK
    
    - Create an interface
  - C wrapper with Turbo modules
  - Outline approach in Indy VDR Issue
  - Start with one component - Indy VDR
- Relevant componentization / state management discussion
- Questions for maintainers / other discussion?
  
  - User Data Storage
  - Machine Readable Governance Framework

<!--THE END-->

- Work Items
  
  - Github Projects / Work management
    
    - Assign people to issues / tasks
  - Basic Functionality - UI/UX around it -get on par with other apps
    
    - Connections
    - Receiving Credentials
    - Presenting Proof
      
      - Simple - automated select credential
      - Advanced - user selection
        
        - Attributes not to share - partial proof presentation (create a proposal)
    - Revocation notification
      
      - Simple UI - show revocation happened
        
        - Pair programming @ horacio
  - Android update to API 30+ - Horacio
  - Authentication - Pin / Biometrics
    
    - Background service accessible  - access wallet key
      
      - iOS concerns on processing time
      - Investigation on this - [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) to create an issue
  - Other work items from the group goals?
  - Credential Offers - Relevant [Github Issue #29](https://github.com/hyperledger/aries-mobile-agent-react-native/issues/29)
  - Basic Messaging - UI - Indicio
    
    - RN Chat Interface package - research
  - Multi-ledger detection - Timo talking with Lissi team
  - UI/UX
- Generic Storage - User/App data storage
  
  - Take into account wallet import/export
    
    - Standardize key:value pairs
    - Universal Wallet spec.
  - Settings format
  - Aries WG call

<!--THE END-->

- Group Goals
  
  - Last time's list:
  - Group Goals
    
    - Consolidate mobile app development effort among interested parties.
    - Codebase you can check out and run immediately in an emulator.
    - Active community
    - Production ready app.
    - Whitelabel or UI modules to be included in existing apps
    - Enable an app to collaborate via protocols with wallets
    - Interoperability
    - Ease of use
      
      - And Aries Protocols to support that ease of use, available to all Mobile implementations
  - Meta
    
    - Test against ourselves over versions
    - Mobile codebase whiteboard - test concepts/ideas
  - Short Term
    
    - Basic Functionality - Connection, Issuance, Present-Proof for Verification
    - Typescript config
    - Demo with two people to connect and send a basic message
    - Mediation - coordinate mediation protocol w/websockets
      
      - Runtime setup and configure
    - Agent Test Harness - AFJ for basic capabilities
    - Ability to clone and white-label the Aries Bifold app
  - Medium Term
    
    - Introduction protocol
    - Talk and demonstrate Export / Import
      
      - Backup / Restore
    - Agent Test Harness  - Manual Backchannel
    - Multi-ledger support
      
      - Similar to Lissi capabilities
    - UI/UX focus
      
      - Widget toolkit - building blocks – data exchange - data description language
    - UI components to be able to use in an existing RN app
    - Support for newer Aries protocols
    - Machine Readable Governance Frameworks
      
      - UI/UX
      - Ledger in governance framework
    - SVG credential rendering
  - Long Term
    
    - Log into a website, OICD?
    - Agent Test Harness - Automated Backchannel
    - Multiple apps on the same phone
      
      - Cross-app wallet - Aries WG Conversation
    - Mobile specific communication transports
      
      - NFC
      - Bluetooth - Animo &amp; Indicio have current work
    - Cloud Agent Custodial control from mobile app
    - Synchronization between wallets - Aries WG Conversation
    - Not tied to Indy -other credential formats
    - Continual AIP implementation
    - Ledger services to decouple agents from ledgers - Architecture level
      
      - Runtime vs compile time

## Next Meeting

- Requests?

## Future Topics

## Action items

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18492338/18515191.txt "Download")

May 19, 2021 by [James Ebert](/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18492338/18515191.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492338/18515192.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18492338/18515193.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
