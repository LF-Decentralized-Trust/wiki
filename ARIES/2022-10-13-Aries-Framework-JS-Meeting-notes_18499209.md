1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-10-13 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Oct 14, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID)&lt;rodolfo.miranda@rootsid.com&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Make contributions to Bifold easier
  - First PR opened for OCA integration into Bifold
- Aries Call
  
  - Presentation about DIDComm Group Messaging
  - Wallet initiatives (Open Wallet Foundation)
    
    - [https://www.linuxfoundation.org/press/linux-foundation-announces-an-intent-to-form-the-openwallet-foundation](https://www.linuxfoundation.org/press/linux-foundation-announces-an-intent-to-form-the-openwallet-foundation)
    - [https://github.com/openwallet-foundation/architecture-task-force/blob/main/docs/conceptual-architecture.md](https://github.com/openwallet-foundation/architecture-task-force/blob/main/docs/conceptual-architecture.md)
    - Focus on SDKs over wallet implementation
  - [Fall IIW 2022](https://internetidentityworkshop.com/) - Un-Conference, [November 15-17](https://www.eventbrite.com/e/internet-identity-workshop-iiwxxxv-35-2022b-tickets-368643531727) - San Francisco, CA

## Agenda

- Record the meeting
- 0.3.0 release
  
  - Write migration guide like [https://aries.js.org/guides/updating/versions/0.1-to-0.2](https://aries.js.org/guides/updating/versions/0.1-to-0.2)
  - Plan
    
    - Release 0.2.5
    - Merge inconsistencies PR
    - Merge 0.3.0-pre into main
      
      - triggers 0.3.0-alpha.0 release → test it out!
    - Write migration guide
    - Make 0.3.0 release
- Documentation
  
  - API Section
    
    - Add folder per version that contains tutorials, api and installation instructions
    - When a new major version is released (0.x version) we copy the docs for the latest version and modify it for new major release
    - [https://docusaurus.io/docs/versioning](https://docusaurus.io/docs/versioning)
- Indy SDK React Native
  
  - Crash in newer RN versions
- Post 0.3.0

## Meeting Notes

## Future topics

Next Week:

- Indy SDK React Native crash

Future Topics:

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

[video1897399618.mp4](#)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
