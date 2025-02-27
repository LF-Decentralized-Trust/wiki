1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2020 AFJ meetings](2020-AFJ-meetings_18513105.html)

# Hyperledger Aries : 2020-02-07 Aries Framework JS Meeting Notes

Created by Jakub Koci, last modified by Ajay Jadhav on Jun 26, 2020

## Date

07 Feb 2020

## Agenda

- Attendees introduction
- Integration between framework and React Native/Node.js wrappers
- Check currently open PRs

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- Name (Employer) &lt;email&gt;
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) (Absa), jakub.koci@gmail.com
- Gaurav Narula
- Timo Glastra

## Meeting Notes

- Gaurav shared the status and goals of his project which is using the framework and what he would need to achieve that (mainly connections and messages with signatures). We agreed that credential exchange is not necessary right now, but we can discuss it more if someone needs it.
- Jakub showed React Native wrapper open-sourced by Absa ([https://github.com/AbsaOSS/rn-indy-sdk](https://github.com/AbsaOSS/rn-indy-sdk)). We discussed how we can use it with the framework.
- Check currently open PRs
  
  - #23, #24 is waiting for approval from some maintainer of the project
  - #15 will be updated and merged
  - #14 is on hold because it's not a priority for us right now and it's also an important and large change
- Jakub showed a solution how to use only DI container from Nest.js ([https://github.com/jakubkoci/nest-di](https://github.com/jakubkoci/nest-di))
- Discussion about persistence and storage mechanism
  
  - Subjects of persistence
    
    - Connections
    - Messages
  - Options
    
    - [pairwise](https://github.com/hyperledger/indy-sdk/blob/master/wrappers/nodejs/README.md#pairwise)
    - [non\_secrets](https://github.com/hyperledger/indy-sdk/blob/master/wrappers/nodejs/README.md#non_secrets)
    - Other storage defined by user of the framework library

## Action items

## Call Recording

Unfortunately, this call haven't been recorded.

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
