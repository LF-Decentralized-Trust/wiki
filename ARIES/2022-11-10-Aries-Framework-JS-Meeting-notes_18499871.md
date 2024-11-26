1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-11-10 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Nov 10, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Prepare for update to 0.3.0
  - Expose metadata directly through react hooks extensions
- Aries Call
  
  - ??
- DIDComm v2 Adoption
  
  - Comments welcome on [spreadsheet](https://docs.google.com/spreadsheets/d/15noWiG_zhhUpornhrZm9cLEjQ1aa6z9qgJgPCaaIbtY/edit?usp=sharing) for important DIDComm v2 considerations/attributes
  - Discussion welcome in the [discord channel](https://discord.com/channels/905194001349627914/1032736844053483621)
  - Join the discord or reach out to [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence)
  - [Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence) working on DIDComm TypeScript library
  - Plan to set up a DIDComm v2 working group call to share thoughts of implementing DIDComm v2 support across Aries frameworks
- IIW is coming up - [https://internetidentityworkshop.com](https://internetidentityworkshop.com/)
  
  - November 15 - 17

## Agenda

- Record the meeting
- Credential delay
  
  - First credential exchange has big delay from accepting offer to receiving credential
  - Doesn't return did when it has found it on one ledger, continues to resolve it from all ledgers
  - the more ledgers added, the larger the delay
  - Qualified dids can provide a solution to this (Because we don't need to fetch the did from all ledgers)
- DIDComm v2 support
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/1096](https://github.com/hyperledger/aries-framework-javascript/pull/1096)
  - Main points:
    
    - Do not add didcomm libarry to core, should be dynamically registered as didcomm/signing/key provider
    - Keys should not leave the wallet, rather the content should be given to the wallet and signed / encrypted content should be returned
    - [https://hackmd.io/6eXZcMhdQR-QCNPMFYTvuA](https://hackmd.io/6eXZcMhdQR-QCNPMFYTvuA)
    - Ask whether they can present their work at the AFJ WG Call
- 0.3.0 release .... continued
  
  - Docs: [https://github.com/hyperledger/aries-javascript-docs/pull/74](https://github.com/hyperledger/aries-javascript-docs/pull/74)
- Indy SDK
  
  - Migration to shared components
    
    - Aries Askar
    - Indy VDR
    - Indy CredX (AnonCreds)

## Meeting Notes

## Future topics

Next Week:

- Shared components how to finish asap
- Mikes PR merge
- potentially multi vs single use invite performance

Future Topics:

- Ledger Agnostic AnonCreds in AFJ

<!--THE END-->

- React Native testing
- Monorepo dependencies
  
  - TypeScript types

<!--THE END-->

- ACA-py and AFJ performance/scale documentation
- Mike's modularization, etc documentation
- Open ID Connect for Issuance/Verification
  
  - [https://openid.net/specs/openid-4-verifiable-credential-issuance-1\_0.html](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html)
  - [https://github.com/bcgov/vc-authn-oidc](https://github.com/bcgov/vc-authn-oidc)
- Hyperledger fabric and Aries wrapper new updates

**Meeting recording:**

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18499871/18516998.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
