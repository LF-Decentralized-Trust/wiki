1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Bifold User Group](Aries-Bifold-User-Group_18490719.html)
5. [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html)
6. [2022 Bifold Meetings](2022-Bifold-Meetings_18515892.html)

# Hyperledger Aries : 2022-04-12 Aries Bifold Users Group Community Meeting

Created by James Ebert, last modified on Apr 12, 2022

## Summary:

Planned Topics:

- Basic Messaging Demo
- Q&amp;A w/Maintainers

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

Who you are, and what your interest is in the Bifold effort.

## Attendees

- Name (Organization) &lt;email&gt;
- James Ebert (Indicio) &lt;james.ebert@Inidicio.tech&gt;
- [Regis Eloi](https://lf-hyperledger.atlassian.net/wiki/people/712020:1f85fa5f-ff75-4f77-9f7b-b6eb5244e07f?ref=confluence)(IDLab) &lt;regis.eloi@idlab.org&gt;
- Ryan Koch (Indicio) &lt;ryan@indicio.tech&gt;
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (BCGov) &lt;jason.leach@fullboar.ca&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;

## Announcements

- Aries Framework JavaScript calls every Thursday at 15:00 CET / 07:00 MST ([Framework JS Meetings](Framework-JS-Meetings_18482467.html))

## Deployments and Work Updates

- Aries Framework JavaScript
  
  - Multi-ledger support added
  - Revocation

## Agenda

- IIW scheduling discussion? - [https://internetidentityworkshop.com/](https://internetidentityworkshop.com/)
  
  - Canceling next call
- Basic Messaging Demo - Ryan Koch
- Yarn Discussion
  
  - RN boilerplate prefers yarn
- Ledger Configuration Followup Discussion
- Open PRs:
  
  - [Indy Post-Install Script](https://github.com/hyperledger/aries-mobile-agent-react-native/pull/139)
  - [Bifold Framework Draft PR](https://github.com/hyperledger/aries-mobile-agent-react-native/pull/274)
  - [https://github.com/hyperledger/aries-mobile-agent-react-native/pull/277](https://github.com/hyperledger/aries-mobile-agent-react-native/pull/277/files)
    
    - Workflows changes discussion
      
      - Goal Codes
      - Machine Readable Governance
      - Verifiable connections
        
        - Verified email connection
        - Verifier social network
        - DID .well-known file domain ownership - proves control of domains
        - Connection metadata - AFJ
- Verifying businesses/organizations discussion
  
  - Direct method: Machine Readable Governance Files - approved issuers, verifiers via public dids
    
    - Lists public DIDs
    - Limited by scale
  - Indirect method: Smaller list of top level issuers, if the connection can present a credential from that smaller list
    
    - Scales more effectively
    - Can use machine readable governance file
    - Request and present credentials
    - Protocol update perspective - additional information may be useful in the presentation or issuance of a credential
      
      - optional information update, not necessarily required
    - Cases for implementing indirect method:
      
      - BCGov - Orgbook
  - Europe QR Code spoofing - man in the middle attack

<!--THE END-->

- Open Issues:
  
  - [Push notifications](https://github.com/hyperledger/aries-mobile-agent-react-native/issues/52)
    
    - ACA-Py plugin coming soon
    - Aries Framework JavaScript Extension [here](https://github.com/hyperledger/aries-framework-javascript-ext/tree/main/packages/push-notifications)
  - [https://github.com/hyperledger/aries-framework-javascript/issues/647](https://github.com/hyperledger/aries-framework-javascript/issues/647)
- Development Roadmap Planning
  
  - Clarify Bifold goals 
    
    - Make it as easy as possible to incorporate ssi pieces
    - Make a UI framework / toolkit
    - Start Componentization within Bifold
      
      - Start with exporting Bifold everything
      - Tackle component customizations
    - Move away from "fork and forget"
  - Features:
    
    - Transition to Out of Band Invitations - [https://github.com/hyperledger/aries-rfcs/tree/main/features/0496-transition-to-oob-and-did-exchange](https://github.com/hyperledger/aries-rfcs/tree/main/features/0496-transition-to-oob-and-did-exchange)
    - Componentization (moving components to afj-extensions)
    - Revocation UIs
      
      - Functionality
        
        - TODO: [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) to create GH issue
      - Revocation notifications
        
        - TODO: [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) to create GH issue
    - Connection-less presentations using Out of Band
    - Update Credential UI/Logical
      
      - Archiving credentials
    - Messaging
    - ODCA - Credential Overlay Capture
    - Auto Present Feature
      
      - Machine readable governance - trust issuers, verifiers
    - Contact branding - trusting issuers, verifiers
    - Accessibility standards
    - Handling length credential issuance processes
    - Predicate Proofs
    - QR-Code generation
    - Deep Linking
    - Indy Shared Components - Indy VDR, Indy Credx, Aries Askar
    - Biometrics
- Questions for maintainers / other discussion?

## Next Meeting

- SVG Credential Package updates?
- Discuss: planning improvements to the wallet for the community

## Future Topics

- Machine Readable Governance Presentation - Mike
- How should we implement Machine Readable Governance?

## Action items

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18496126/18516146.txt "Download")

Apr 12, 2022 by [James Ebert](/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18496126/18516146.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496126/18516147.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496126/18516145.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
