1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-09-22 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified on Sep 22, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID) &lt;rodolfo.miranda@rootsid.com&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Biometrics - working towards NIST standards.
  - Indicio working towards latest React Native
  - Working on holder requesting a proof
- Aries Call
  
  - [Rebooting Web of Trust](https://www.weboftrust.info/), The Hague, September 26-30

## Agenda

- Record the meeting
- DIDComm V2
  
  - HackMD: [https://hackmd.io/8QhG-zekRbaliJYDs6Y7-Q](https://hackmd.io/8QhG-zekRbaliJYDs6Y7-Q)
  - Ursa also has crypto, but not for DIDComm we think?
    
    - [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa)
  - Multiple approaches
    
    - Custom implemnation with lower level crypto (e.g. Askar)
      
      - lower level, more effort
      - [https://github.com/hyperledger/aries-askar](https://github.com/hyperledger/aries-askar)
      - [https://github.com/hyperledger/aries-cloudagent-python/blob/main/aries\_cloudagent/askar/didcomm/v2.py](https://github.com/hyperledger/aries-cloudagent-python/blob/main/aries_cloudagent/askar/didcomm/v2.py)
      - Askar has storage and crypto in one, while for a modular approach we want it separated
        
        - Already separated in AFJ through interface
        - In browser you don't need a native backend / advanced storage, but you do need the crypto
    - DIDComm library from SICPA (WASM)
      
      - WASM Support in react native is not great
      - React Native wrapper available, but only for Android: [https://github.com/sicpa-dlab/didcomm-react-native/tree/main/android/src/main/java/com/sicpa/didcomm/reactnative](https://github.com/sicpa-dlab/didcomm-react-native/tree/main/android/src/main/java/com/sicpa/didcomm/reactnative)
      - Could look at JSI interface wrapper like [https://github.com/animo/react-native-bbs-signatures](https://github.com/animo/react-native-bbs-signatures)
      - DIDComm v2 branch in AFJ: [https://github.com/sicpa-dlab/aries-framework-javascript/tree/didcomv2-contribution](https://github.com/sicpa-dlab/aries-framework-javascript/tree/didcomv2-contribution)
      - Use our own did resolver, need also our own secret resolver.
    - DIDComm library in typescript
      
      - [https://github.com/aviarytech/didcomm](https://github.com/aviarytech/didcomm)
- storage/data layer being abstracted into a well defined interface akin to what schema inversion technologies like PostgREST/Hasura end up providing
  
  - Wallet storage which takes advantage of Row Level Security would provide a long term option for the end user to be able to access their wallet while still enabling custodian ownership of their wallet by a identity service provider
  - Good discussion by Daniel Hardman about separation of Encryption and storage for wallets (starting from 49minutes)
- 0.3.0 release
- Docker container / image environments

## Meeting Notes

## Future topics

Next Week:

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

[meeting-recording.mp4](#)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498798/18516761.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
