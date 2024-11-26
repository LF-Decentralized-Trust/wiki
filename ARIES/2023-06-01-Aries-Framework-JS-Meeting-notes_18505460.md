1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-06-01 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Ry Jones on Jun 01, 2023

**Meeting recording**

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Animo Solutions (timo@animo.id)
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence) (Animo Solutions) &lt;berend@animo.id&gt;
- [Charles Lanahan](https://lf-hyperledger.atlassian.net/wiki/people/712020:50e56df1-41cf-415b-a802-ae0b89b9c75b?ref=confluence) &lt;charles.lanahan@gmail.com&gt;
- [Alexander Shenshin](https://lf-hyperledger.atlassian.net/wiki/people/63cf3328c565900ff404dda2?ref=confluence) (DSR Corporation) &lt;alexander.shenshin@dsr-corporation.com&gt;
- [Artem Ivanov](https://lf-hyperledger.atlassian.net/wiki/people/557058:490facf1-26c6-4490-955a-53ac8ac201a5?ref=confluence) (DSR Corporation) &lt;artem.ivanov@dsr-corporation.com&gt;

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
- Aries Call [2023-02-08 Aries Working Group Call](2023-02-08-Aries-Working-Group-Call_18501917.html)
  
  - Discussion on Agents vs Wallets
  - We have a phone, but the phones have a "Phone" app (in case of iOS)
    
    - Purpose of a phone has expanded greatly, it is now a computer
  - Too puristic on the naming
- DIDComm v2
  
  - PRs open for tests and splitting up the demo
  - Outstanding work?
    
    - Non-standardized approach for creating connections
      
      - Can create instant connection from invitation
      - No did exchange

<!--THE END-->

- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)

## Agenda

- Record the meeting
- Update on JWT VCs, extended crypto support and OpenID4VC
- AFJ 0.4.0 Release
  
  - [https://github.com/hyperledger/aries-framework-javascript/pull/1475](https://github.com/hyperledger/aries-framework-javascript/pull/1475)
- Making it easier for people to get started with AFJ
- Rethinking the Storage Layer

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

- [presentation.pdf](attachments/18505460/18518181.pdf)
- [https://youtu.be/u4-BgCCkcSw](https://youtu.be/u4-BgCCkcSw)
- [2023 06 01 AFJ chat.txt](attachments/18505460/18518189.txt)

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.
- Wallet API redesign ([Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) )
- Cheqd integration ([Daev Mithran](https://lf-hyperledger.atlassian.net/wiki/people/5f74949b287870006af56f0e?ref=confluence) )
- AFJ Interop tests not running

## Attachments:

![](images/icons/bullet_blue.gif) [presentation.pdf](attachments/18505460/18518181.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [2023 06 01 AFJ chat.txt](attachments/18505460/18518189.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
