1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-06-03 Aries Framework JS Meeting notes

Created by Jakub Koci, last modified by Timo Glastra on Jun 03, 2021

## Date

03 Jun 2021

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa) &lt;jakub.koci@gmail.com&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call

## Agenda

- Record the meeting
- Mediation protocol
- Multiple transport support
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/268](https://github.com/hyperledger/aries-framework-javascript/issues/268)
- Breaking changes
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/305](https://github.com/hyperledger/aries-framework-javascript/issues/305)
- Paving the way for shared components
  
  - IndyHolderService, IndyIssuerService, IndyVerifierService should become interface
    
    - With implementation IndySdkHolderService, IndySdkIssuerService, IndySdkVerifierService
    - IndyCredXHolderService, IndyCredXIssuerService, IndyCredXVerifierService
  - LedgerService should become IndyLedgerService interface
    
    - With implementation IndySdkLedgerService, IndyVdrLedgerService, IndyVdrProxyService
  - New wallet interface implementation for Aries Askar
  - Extend config to pass in platform specific libraries
  - [https://github.com/hyperledger/indy-vdr/issues/59](https://github.com/hyperledger/indy-vdr/issues/59)

## Meeting Notes

## Future topics

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
