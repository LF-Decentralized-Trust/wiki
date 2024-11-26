1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Bifold User Group](Aries-Bifold-User-Group_18490719.html)
5. [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
6. [2021 Bifold Meetings](2021-Bifold-Meetings_18514782.html)

# Hyperledger Aries : 2021-04-07 Aries Bifold Users Group Community Meeting

Created by Sam Curren on Apr 07, 2021

## Summary:

Planned Topics:

- Demo / Code Status
- Work Items
- UI/UX Discussions

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
- [David Clawson](https://lf-hyperledger.atlassian.net/wiki/people/603576291853760070159a87?ref=confluence)(Indicio) &lt;david.clawson@indicio.tech&gt;
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence)(Animo Solutions) &lt;karim@animo.id&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)(Animo Solutions) &lt;timo@animo.id&gt;

## Announcements

- Aries Framework JavaScript calls every Thursday at 15:00 CET / 07:00 MST ([Framework JS Meetings](Framework-JS-Meetings_18482467.html))
- Code has moved to Hyperledger! [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)
- Indicio open sourced a new wallet design: [https://indicio.tech/blog/indicio-contributes-novel-ui-messaging-design-for-digital-wallet-to-open-source-community/](https://indicio.tech/blog/indicio-contributes-novel-ui-messaging-design-for-digital-wallet-to-open-source-community/)

## Deployments and Work Updates

- iOS working and documentation added
- In progress - QR Code generation and presentations - Indicio
- Aries Framework JavaScript
  
  - In Progress - Revocation - Animo
  - In Progress - Mediation (coordinate-mediation) - Indicio
- rn-indy-sdk
  
  - Added missing present proof related operations. Now works in Android, iOS following
- Aries Agent Test Harness (AATH) manual mobile backchannel

## Agenda

- Demo / Code Status
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

- Bring your UI/UX Developers!
  
  - UI/UX Design Conversations
  - UI to functionality layers/interactions
  - principle -github discussion
    
    - UI flexibility/implementation
    - Format of exchange
  - Indicio wallet design showcase by Scott Harris
- Requests?

## Future Topics

## Action items

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18491801/18515078.txt "Download")

Apr 07, 2021 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18491801/18515078.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18491801/18515079.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18491801/18515077.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
