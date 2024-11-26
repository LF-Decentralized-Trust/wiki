1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-08-31 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Alexander Shenshin on Aug 31, 2023

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) - 2060.io (a@2060.io)
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Animo Solutions (timo@animo.id)
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) - Indicio PBC(kim@indicio.tech)
- [Alexander Shenshin](https://lf-hyperledger.atlassian.net/wiki/people/63cf3328c565900ff404dda2?ref=confluence) (DSR Corporation) &lt;alexander.shenshin@dsr-corporation.com&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Meetings suspended until September
- Aries Call [2023-08-30 Aries Working Group Call](2023-08-30-Aries-Working-Group-Call_18507105.html)
  
  - Discussion on peer did migration
    
    - Proposed did:peer:4 to replace all previous methods
    - [https://github.com/dbluhm/did-peer-4](https://github.com/dbluhm/did-peer-4)
  - DID Rotate protocol
- New Code With Us from BC Gov
  
  - [https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/51d7c289-51a8-4307-939c-5a4271c7b2b6](https://marketplace.digital.gov.bc.ca/opportunities/code-with-us/51d7c289-51a8-4307-939c-5a4271c7b2b6)
  - Create a Load Generator for Testing BC Gov Issuers, Verifiers, and DIDComm Mediator

<!--THE END-->

- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
- AnonCreds
  
  - Ursa replacement with anoncreds-clsignatures-rs [https://github.com/hyperledger/anoncreds-rs/pull/226](https://github.com/hyperledger/anoncreds-rs/pull/226)
    
    - A few changes in the API (tails file not required anymore for issuing/revoking credentials

## Agenda

- Record the meeting
- 0.4.1 released
  
  - [https://github.com/hyperledger/aries-framework-javascript/blob/main/CHANGELOG.md](https://github.com/hyperledger/aries-framework-javascript/blob/main/CHANGELOG.md)
- OpenID4VCI, SIOP, OpenID4VP support
  
  - Project proposal:
