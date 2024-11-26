1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2022 AFJ meetings](2022-AFJ-meetings_18515835.html)

# Hyperledger Aries : 2022-08-04 Aries Framework JS Meeting notes

Created by Lance Byrd, last modified on Aug 04, 2022

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence) (Animo Solutions) &lt;berend@animo.id&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (RootsID) &lt;rodolfo.miranda@rootsid.com&gt;
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (Fullboar Creative / BC Gov.) &lt;jason.leach@fullboar.ca&gt;
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa) &lt;jakub.koci@gmail.com&gt;

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
  
  - Aries Interop-a-thon: proposed for August 31 7:00 am to 11:00 pm MDT
  - [Rebooting Web of Trust](https://www.weboftrust.info/), Den Hague, September 26-30
  - Aries Survey (Vasileios Konstantinou MSC student at AUEB): [https://docs.google.com/forms/d/e/1FAIpQLSfgJyIXZg8LAOvzWm9-r8NGnQOKzF4XJRaHC85sGHQh6WobeA/viewform?usp=sf\_link](https://docs.google.com/forms/d/e/1FAIpQLSfgJyIXZg8LAOvzWm9-r8NGnQOKzF4XJRaHC85sGHQh6WobeA/viewform?usp=sf_link)
  - Wallet Backup and Restore conversation - Thursday 1pm US/Mountain (Ask Sam for Invite)
- Hyperledger Global Forum
  
  - September 12-14
  - [Workshop: How To Build a Self-Sovereign Identity Agent With Hyperledger Aries Framework JavaScript](https://hgf22.sched.com/event/15Bjb)

## Agenda

- Record the meeting
- From our last meeting:
  
  - Support for Deno
  - Generic ledger module + using qualified identifiers
- Mediator scalability issues ([Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence))
  
  - AFJ as a mediator.  Needed by edge agents.
    
    - More than 5 clients causes failures, if you start 10 then maybe 1 or 2 will timeout during provisioning
    - Do we have a guide for configuring an AFJ mediator?
    - Latest version fixes 15 second timeout
  - ACA-py mediator
    
    - Timo has done some work with ACA-py mediator, scaling to millions of agents
    - ACA-py based Indicio mediator was also tried, behaved similar to ACA-py results
  - The PR for mediation issue: [https://github.com/hyperledger/aries-framework-javascript/pull/946](https://github.com/hyperledger/aries-framework-javascript/pull/946)
- Karim Documentation discussions, to get your feedback and suggestions
  
  - [https://github.com/hyperledger/aries-javascript-docs/discussions/66](https://github.com/hyperledger/aries-javascript-docs/discussions/66)
  - [https://github.com/hyperledger/aries-javascript-docs/discussions/65](https://github.com/hyperledger/aries-javascript-docs/discussions/65)
- Pain points and improvements
- - When to favor documentation?
    
    - ESLint
    - Issue Templates
    - Continous Integration checks
  - How to incentivize or guide developers towards building documentation?
  - List of things that could be added for new developers
    
    - Code Style
    - Patterns
    - Tips
  - [Docusaurus](https://docusaurus.io/docs) contributions
    
    - Framework considerations?
- Special considerations for AFJ, AFJ-Extensions, and Bifold?
- Cross repo documentation
- Contributors want to get on-board rapidly
  
  - Rating issues for beginner, intermediate, advanced?

## Meeting Notes

## Future topics

- React Native testing
- Monorepo dependencies
  
  - TypeScript types

<!--THE END-->

- ACA-py and AFJ performance/scale documentation
- Mike's modularization, etc documentation

**Meeting recording:**

[**Meeting Zoom Recording 2022-08-04**](https://lf-hyperledger.atlassian.net/wiki/download/attachments/18497920/Meeting2022_08_04.mp4?api=v2)

  File Modified

No files shared here yet.

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
