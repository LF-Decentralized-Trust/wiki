1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-11-24 Aries Framework JS Meeting notes

Created by Jakub Koci, last modified on Nov 25, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence)(Absa) &lt;jakub.koci@gmail.com&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call

## Agenda

- Record the meeting
- Credential delay
  
  - There is an open issue in AFJ
  - The delay is caused by delayed connection to ledgers. It might help to update the genesis file(s).
- 0.3.0 release .... continued
  
  - We're waiting for the last smaller PRs to be merged.
  - Version 0.3.0 is part of the main branch already.
  - Alpha versions are released from the main branch regularly.
- DIDComm v2 support
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/1096](https://github.com/hyperledger/aries-framework-javascript/pull/1096)
  - Main points:
    
    - Do not add didcomm libarry to core, should be dynamically registered as didcomm/signing/key provider
    - Keys should not leave the wallet, rather the content should be given to the wallet and signed / encrypted content should be returned
    - [https://hackmd.io/6eXZcMhdQR-QCNPMFYTvuA](https://hackmd.io/6eXZcMhdQR-QCNPMFYTvuA)
    - Ask whether they can present their work at the AFJ WG Call
  - Main points 2:
    
    - cosmetic changes
    - public API (send ping v2, ...)
    - didcomm lib (double check if the current interface is good enough)
  - Next week:
    
    - Code presentation by SICPA
    - Code presentation by AFJ
- SICPA Open source mediator for didcomm v2
  
  - [https://github.com/sicpa-dlab/didcomm-v2-mediator-ts](https://github.com/sicpa-dlab/didcomm-v2-mediator-ts)
  - [https://github.com/sicpa-dlab/aries-framework-javascript/tree/main/packages/peer-did-ts/src](https://github.com/sicpa-dlab/aries-framework-javascript/tree/main/packages/peer-did-ts/src)
- Indy SDK
  
  - Migration to shared components
    
    - Aries Askar
    - Indy VDR
    - Indy CredX (AnonCreds)

## Meeting Notes

## Future topics

Next Week:

- Code presentation by SICPA
- Code presentation by AFJ

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

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18500081/18517074.txt "Download")

Nov 25, 2022 by [Jakub Koci](/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
