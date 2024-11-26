1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2021 AFJ meetings](2021-AFJ-meetings_18514593.html)

# Hyperledger Aries : 2021-05-20 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Jakub Koci on May 20, 2021

## Date

20 May 2021

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa) &lt;jakub.koci@gmail.com&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- [Ajay Jadhav](https://lf-hyperledger.atlassian.net/wiki/people/557058:4c9b11a5-2616-4abe-af94-bbc11c984654?ref=confluence)(AyanWorks) &lt;ajay@ayanworks.com&gt;

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call

## Agenda

- Record the meeting
- Custom errors
  
  - [https://github.com/hyperledger/aries-framework-javascript/issues/281](https://github.com/hyperledger/aries-framework-javascript/issues/281)
- Cleanup
  
  - Too much duplicate code
  - Dependencies for multiple platforms
  - mediator-ws, mediator-client, mediator-server, e2e, e2e-ws
    
    - Seems like there is some duplication between the separate mediator work?
  - samples is not 'samples', it's our e2e tests. We should rename to not confuse
    
    - PR created [https://github.com/hyperledger/aries-framework-javascript/pull/284](https://github.com/hyperledger/aries-framework-javascript/pull/284)
- Paving the way for shared components
  
  - IndyHolderService, IndyIssuerService, IndyVerifierService should become interface
    
    - With implementation IndySdkHolderService, IndySdkIssuerService, IndySdkVerifierService
    - IndyCredXHolderService, IndyCredXIssuerService, IndyCredXVerifierService
  - LedgerService should become IndyLedgerService interface
    
    - With implementation IndySdkLedgerService, IndyVdrLedgerService, IndyVdrProxyService
  - New wallet interface implementation for Aries Askar
  - Extend config to pass in platform specific libraries
  - [https://github.com/hyperledger/indy-vdr/issues/59](https://github.com/hyperledger/indy-vdr/issues/59)
- Waiting for review
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/263](https://github.com/hyperledger/aries-framework-javascript/pull/263)
  - [https://github.com/hyperledger/aries-framework-javascript/pull/266](https://github.com/hyperledger/aries-framework-javascript/pull/266)

## Meeting Notes

## Future topics

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18492291/18515205.txt "Download")

May 20, 2021 by [Jakub Koci](/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
