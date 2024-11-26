1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2020 AFJ meetings](2020-AFJ-meetings_18513105.html)

# Hyperledger Aries : 2020-10-30 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by shonjs on Nov 01, 2020

## Date

30 Oct 2020

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo) &lt;timo@animo.id&gt;
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa) &lt;jakub.koci@gmail.com&gt;
- [shonjs](https://lf-hyperledger.atlassian.net/wiki/people/557058:b2736d63-185c-457c-88a1-e84b63da434d?ref=confluence) (KBA) &lt;rush2shon@gmail.com&gt;

## Status updates

- Issue credential protocol
  
  - Issue credential merged
  - Still needed:
    
    - Start with credential proposal
    - advanced threading
    - validation of protocol state
    - validate credential preview against actual credential
- Present proof protocol
  
  - First PR for presentation request message opened
- AFJ ↔ React Native
  
  - [https://github.com/TimoGlastra/aries-mobile-agent-javascript](https://github.com/TimoGlastra/aries-mobile-agent-javascript)
  - Erros thrown by rn-indy-sdk do not match errors thrown by indy
- Started work on \`@types/indy-sdk\`
  
  - DefinitelyType will be updated instantly, adding to indy-sdk repo limits us to their release cycle
  - I hope this would also allow us to reuse the types for rn-indy-sdk
  - [https://github.com/TimoGlastra/DefinitelyTyped/tree/%40types/indy-sdk/types/indy-sdk](https://github.com/TimoGlastra/DefinitelyTyped/tree/%40types/indy-sdk/types/indy-sdk)

## Agenda

- Record the meeting
- Issue credential PR's
- \`@types/indy-sdk\` possible approaches
- rn-indy-sdk doesn't work well with error handling
  
  - E.g. can't "catch" a \`WalletAlreadyExistsError\`
  - [https://github.com/TimoGlastra/aries-mobile-agent-javascript](https://github.com/TimoGlastra/aries-mobile-agent-javascript)

## Meeting Notes

- rn-indy-sdk doesn't work well with error handling
  
  - See: [https://github.com/AbsaOSS/rn-indy-sdk/issues/21](https://github.com/AbsaOSS/rn-indy-sdk/issues/21)
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) will create description of different \`@types/indy-sdk\` approaches

## Future topics

- State machines

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
