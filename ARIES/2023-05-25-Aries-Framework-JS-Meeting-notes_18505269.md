1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-05-25 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Ry Jones on May 25, 2023

**Meeting recording**

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Animo Solutions (timo@animo.id)
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) - (AffinitiQuest) &lt;warrren@affinitiquest.io&gt;
- [Charles Lanahan](https://lf-hyperledger.atlassian.net/wiki/people/712020:50e56df1-41cf-415b-a802-ae0b89b9c75b?ref=confluence) &lt;charles.lanahan@gmail.com&gt;
- [Berend Sliedrecht](https://lf-hyperledger.atlassian.net/wiki/people/601bca34332cbe007020eab0?ref=confluence) (Animo) &lt;berend@animo.id&gt;
- [Tim Bloomfield](https://lf-hyperledger.atlassian.net/wiki/people/5a70c8faa02421507dce29c3?ref=confluence) &lt;tim.bloomfield@ontario.ca&gt;
- [Sai Ranjit Tummalapalli](https://lf-hyperledger.atlassian.net/wiki/people/5f620f169109170076f8dc96?ref=confluence) &lt;sairanjit.tummalapalli@ayanworks.com&gt;
- [Alexander Shenshin](https://lf-hyperledger.atlassian.net/wiki/people/63cf3328c565900ff404dda2?ref=confluence) (DSR Corporation) &lt;alexander.shenshin@dsr-corporation.com&gt;
- [Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence) (DSR Corporation) &lt;renata.toktar@dsr-corporation.com&gt;
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
  
  - Making the app more accessible
    
    - better support for people with vision problems, etc..
  - PR open for shared components (draft)
    
    - [https://github.com/hyperledger/aries-mobile-agent-react-native/pull/666](https://github.com/hyperledger/aries-mobile-agent-react-native/pull/666)
  - Testing Bifold with issuance and verification (will open issues in Aries Framework JavaScript)
- Aries Call [2023-02-08 Aries Working Group Call](2023-02-08-Aries-Working-Group-Call_18501917.html)
- Releases
  
  - AFJ 0.4.0-alpha releases (104)
- DIDComm v2
  
  - [April IIW DIDComm v2 connect-a-thon](https://hackmd.io/j6U6JpQ2SRexSUKL7i2XRg)
- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
- Shared Components
  
  - Node.JS still same state. Working with some performance issues that are resolved in Node 18 (with patch from Ariel)
  - PR for Indy VDR merged that adds support for React Native 0.66+ (until 0.71) and Expo.
    
    - Now making PRs to Askar and AnonCreds
  - Lower Android version support with custom cross images
    
    - Custom repo that has cross images with our desired Android versions
      
      - [https://github.com/hyperledger/aries-builder-images](https://github.com/hyperledger/aries-builder-images)
    - Cross images lowest is Android 5
    - Tested until Android API: 24+, with Android 7+
    - Still have to test Askar and AnonCreds with these custom images as Jason ran into some issues with simulators, etc...
- Open Source Summit in Vancouver
  
  - [https://ossna2023.sched.com/event/1K58t?iframe=no](https://ossna2023.sched.com/event/1K58t?iframe=no)

## Agenda

- Record the meeting
- Future of Aries
  
  - Make sure to read the meeting notes: [2023-05-24 Aries Working Group Call](2023-05-24-Aries-Working-Group-Call_18505163.html)
  - Where did the initiative come from?
    
    - OWF doesn't make standards, Aries has RFCs
    - RFCs could be moved to DIF
  - We get a lot of things from HL (runners, infrastructure, marketing, workshops)
  - Problem from Hyperledger?
    
    - assumption = Hyperledger == blockchain
    - misconceptions about Aries
  - OWF = wallet, that doesn't make sense maybe?
  - Purpose / goal of Aries = rooted in blockchain (should goal be revamped?) 
    
    - Aries is not tied to indy, but not tied to blockchain at all
  - indy-pendence is not well-known, move to OWF could help in making that more clear
  - not as much activity / support?
  - other communities view Aries as AnonCreds, CL, Indy, DIDComm
    
    - perception is very difficult to change
    - Note from Tim Bloomfield:
      
      - In terms of marketing and branding here is a great example of the current confusion on Aries - this is paper from the FIDO alliance (provides a great summary of eIDAS):
      - “Hyperledger Indy SDK Wallet \[74] is a cloud-based wallet, which is accessed by the Hyperledger Aries
        
        protocols. This cloud-based architecture is most relevant for the EUDI Wallet Form Factor 2.”
      - [https://media.fidoalliance.org/wp-content/uploads/2023/04/FIDO-EUDI-Wallet-White-Paper-FINAL.pdf](https://media.fidoalliance.org/wp-content/uploads/2023/04/FIDO-EUDI-Wallet-White-Paper-FINAL.pdf)
  - wallet is the anchor where people start (so open wallet foundation can help)
  - components split up, so not one indy-sdk but separate components. Not connected to just indy.
  - Discussion in Aries repo: [https://github.com/hyperledger/aries/discussions/20](https://github.com/hyperledger/aries/discussions/20)
- Future architecture of Aries Framework JavaScript
- Getting started with AFJ
  
  - difficult to keep up with versions, alpha vs stable, what to use, and install instructions are sometimes incorrect if in alpha stages
    
    - documentation not clear on what the release cycle looks like
  - getting the demo working (alice-faber walkthrough)
    
    - extracting it into a separate repo
    - or as acapy: add it in a docker container
  - lack of documentation/demo (for plugins)
    
    - bbs+, jsonld, cheqd not documented, also not in the demo
    - openid4vci
  - example repos setup with the latest version and having simple flows implemented
    
    - different examples
    - examples: [https://github.com/vercel/next.js/tree/canary/examples](https://github.com/vercel/next.js/tree/canary/examples)
- Release 0.4.0
  
  - shared components
  - not wait for revocation
- DIDComm v2
  
  - What to do to get it merged?
  - do not call did resolver from wallet, but keep didcomm implemetnation in wallet for now.

## Meeting Notes

- New meeting invite:
  
  - ```
    Hyperledger Community is inviting you to a scheduled Zoom meeting.

          
Topic: Aries JavaScript Meeting
Time: Mar 23, 2023 06:00 AM Pacific Time (US and Canada)
        Every week on Thu, until May 9, 2024, 60 occurrence(s)

          https://zoom.us/j/99751084865?pwd=TW1rU0FDVTBqUlhnWnY2NERkd1diZz09
          

          

          

        
    ```

## Recording

[https://youtu.be/Xw4Wc6dU8jk](https://youtu.be/Xw4Wc6dU8jk)

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.
- Wallet API redesign ([Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) )
- Cheqd integration ([Daev Mithran](https://lf-hyperledger.atlassian.net/wiki/people/5f74949b287870006af56f0e?ref=confluence) )
- AFJ Interop tests not running

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
