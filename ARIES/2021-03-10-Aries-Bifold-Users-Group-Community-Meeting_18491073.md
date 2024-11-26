1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Bifold User Group](Aries-Bifold-User-Group_18490719.html)
5. [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
6. [2021 Bifold Meetings](2021-Bifold-Meetings_18514782.html)

# Hyperledger Aries : 2021-03-10 Aries Bifold Users Group Community Meeting

Created by Sam Curren, last modified by James Ebert on Mar 10, 2021

## Summary:

Planned Topics:

- Call recap
- Code Review
- Group Goals
  
  - Short Term
  - Medium Term
  - Long Term
- Code Contributions

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
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) (Indicio) &lt;sam@indicio.tech&gt;
- [David Clawson](https://lf-hyperledger.atlassian.net/wiki/people/603576291853760070159a87?ref=confluence)(Indicio) &lt;[david.clawson@indicio.tech](mailto:david.clawson@indicio.tech)
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence)(Animo Solutions) &lt;karim@animo.id&gt;
- [Ken Ebert](https://lf-hyperledger.atlassian.net/wiki/people/70121:2cc4df0e-16de-40dc-ba52-09649099759a?ref=confluence)(Indicio) &lt;ken@indicio.tech&gt;

## Announcements

Rocket Chat Channel: [https://chat.hyperledger.org/channel/aries-bifold](https://chat.hyperledger.org/channel/aries-bifold)

- Aries Framework JavaScript calls every Thursday at 15:00 CET / 07:00 MST ([Framework JS Meetings](Framework-JS-Meetings_18482467.html))

## Deployments and Work Updates

- Code State to be reviewed in agenda.
- Aries Framework JavaScript
- rn-indy-sdk
  
  - Added missing present proof related operations. Now works in Android, iOS following

## Agenda

- Previous Call Recap
  
  - Naming
- Code Review
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
- Code Contributions
  
  - Legal Troubles?
  - Aries Mobile Agent React Native - [https://github.com/Indicio-tech/aries-mobileagent-react-native](https://github.com/Indicio-tech/aries-mobileagent-react-native)
  - rn-indy-sdk - [https://github.com/AbsaOSS/rn-indy-sdk](https://github.com/AbsaOSS/rn-indy-sdk)
    
    - Jakub  - Ask at AFJ

## Next Meeting

- UI/UX Design
- Requests?

## Future Topics

## Action items

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18491073/18514982.txt "Download")

Mar 10, 2021 by [James Ebert](/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18491073/18514982.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18491073/18514980.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18491073/18514981.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
