1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-06-29 Aries Framework JS Meeting notes

Created by Ry Jones on Jun 29, 2023

**Meeting recording**

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Animo Solutions (timo@animo.id)
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest)&lt;warren@affinitiquest.io&gt;
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) - Animo Solutions &lt;karim@animo.id&gt;
- [Artem Ivanov](https://lf-hyperledger.atlassian.net/wiki/people/557058:490facf1-26c6-4490-955a-53ac8ac201a5?ref=confluence) - DSR &lt;artem.ivanov@dsr-corporation.com&gt;
- [Charles Lanahan](https://lf-hyperledger.atlassian.net/wiki/people/712020:50e56df1-41cf-415b-a802-ae0b89b9c75b?ref=confluence) &lt;charles.lanahan@gmail.com&gt;
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
  
  - Integrating AFJ 0.4.0, lot of updates to follow (e.g. react native update)
  - OCA package
- Aries Call [2023-02-08 Aries Working Group Call](2023-02-08-Aries-Working-Group-Call_18501917.html)
  
  - Scalable Mediation - DocketSock
    
    - Socket server separate from mediator agent

<!--THE END-->

- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)

## Agenda

- Record the meeting
- DIDComm v2 discussion
  
  - DIDComm v2 crypto implemented using Aries Askar, Indy SDK not supported
  - Wallet takes resolved DIDDocument for now (will be reworked as planned API refactor)
  - No support for sessions, queue, or priority yet
  - Supported protocols: OOB create invitation, trust ping send/receive
  - Specify DIDComm version when creating an invitation
  - did:peer:2 for p2p connections
  - how do we want to handle connections?
    
    - connection can be useful, but it can also be useful to be able to send a message to another connection
    - are we conflating a contact with a connection?
    - what if we receive a message from a did we've never seen before?
      
      - configuration to allow/disallow certain messages? → simple default behaviour
      - create dynamic connection?
      - allow application layer to decide whether the message is accepted, or discard the message → more complex custom behaviour
      - don't want junk in your connection list
  - DIDComm v2 protocols for issuance / etc..
    
    - [https://didcomm.org/issue-credential/3.0/](https://didcomm.org/issue-credential/3.0/)
  - issue: need to resolve our own did to send message
  - Can it be used with AFGO mediator?
    
    - Need to support mediator protocols as client as well: [https://didcomm.org/mediator-coordination/2.0/](https://didcomm.org/mediator-coordination/2.0/)
- Open Wallet Foundation
- Wallet API discussion continued
- Documentation and getting started – continued
- Revocation PR, other open issues/PRs

## Meeting Notes

- New meeting invite:
  
  - ```
    Hyperledger Community is inviting you to a scheduled Zoom meeting.

          
Topic: Aries JavaScript Meeting
Time: Mar 23, 2023 06:00 AM Pacific Time (US and Canada)
        Every week on Thu, until May 9, 2024, 60 occurrence(s)

          https://zoom.us/j/99751084865?pwd=TW1rU0FDVTBqUlhnWnY2NERkd1diZz09
          

          

          

        
    ```

## Recording / Slides

- [https://youtu.be/DKmifysoCY4](https://youtu.be/DKmifysoCY4)
- [2023 06 29 Aries JavaScript Meeting transcript.txt](attachments/18505964/18518361.txt)

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.
- Extracting parts of AFJ into generic libraries
- Cheqd integration ([Daev Mithran](https://lf-hyperledger.atlassian.net/wiki/people/5f74949b287870006af56f0e?ref=confluence) )
- AFJ Interop tests not running

[DSR\_AFJ\_DIDCommV2.pptx](https://lf-hyperledger.atlassian.net/wiki/download/attachments/18505828/DSR_AFJ_DIDCommV2.pptx?version=1&modificationDate=1687442009166&api=v2)

## Attachments:

![](images/icons/bullet_blue.gif) [2023 06 22 Aries JavaScript Meeting chat.txt](attachments/18505964/18518358.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [2023 06 22 Aries JavaScript Meeting transcript.txt](attachments/18505964/18518359.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [DSR\_AFJ\_DIDCommV2.pptx](attachments/18505964/18518360.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)  
![](images/icons/bullet_blue.gif) [2023 06 29 Aries JavaScript Meeting transcript.txt](attachments/18505964/18518361.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
