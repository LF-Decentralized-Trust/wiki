1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [Aries Framework JavaScript](Aries-Framework-JavaScript_18482463.html)
5. [Framework JS Meetings](Framework-JS-Meetings_18482467.html)
6. [2023 AFJ meetings](2023-AFJ-meetings_18517262.html)

# Hyperledger Aries : 2023-05-18 Aries Framework JS Meeting notes

Created by Timo Glastra, last modified by Ry Jones on May 18, 2023

**Meeting recording**

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at  [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy) . If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Animo Solutions (timo@animo.id)
- [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) - Animo Solutions (karim@animo.id)
- [Clecio Varjao](https://lf-hyperledger.atlassian.net/wiki/people/557058:f9e1bfa2-a82c-4b68-85ee-627507d593d9?ref=confluence)  - Government of BC (clecio.varjao@gov.bc.ca)
- [Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) - 2060.io (a@2060.io)
- [Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence) - DSR Corporation (renata.toktar@dsr-corporation.com)
- [Alexander Shenshin](https://lf-hyperledger.atlassian.net/wiki/people/63cf3328c565900ff404dda2?ref=confluence)  - DSR Corporation (alexander.shenshin@dsr-corporation.com)
- Aziz Karabashov - DSR Corporation (aziz.karabashov@dsr-corporation.com)

## Resources

- Hyperledger Discord: [https://discord.gg/hyperledger](https://discord.gg/hyperledger) (#aries-javascript and #aries-bifold)
- Aries JavaScript Docs: [https://aries.js.org/](https://aries.js.org/)
- Repositories:
  
  - Aries Framework JavaScript: [https://github.com/hyperledger/aries-framework-javascript](https://github.com/hyperledger/aries-framework-javascript)
  - Aries Framework JavaScript Extension: [https://github.com/hyperledger/aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext)
  - Aries Mobile Agent React Native: [https://github.com/hyperledger/aries-mobile-agent-react-native](https://github.com/hyperledger/aries-mobile-agent-react-native)

## Status updates

- Aries Bifold ([Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  
  - Short meeting to catch up on open PRs
    
    - Restructuring of repo to monorepo/workspaces has been merged
  - PR open for shared components (draft)
    
    - [https://github.com/hyperledger/aries-mobile-agent-react-native/pull/666](https://github.com/hyperledger/aries-mobile-agent-react-native/pull/666)
    - Issue with older android versions fixed
    - New issue discovered with missing symbols in x86 architecture
    - [https://hackmd.io/rUDkxrRzQNCSd4koK67ncA](https://hackmd.io/rUDkxrRzQNCSd4koK67ncA)
    - [https://github.com/android/ndk/issues/1614](https://github.com/android/ndk/issues/1614)
- Aries Call [2023-02-08 Aries Working Group Call](2023-02-08-Aries-Working-Group-Call_18501917.html)
- Releases
  
  - AFJ 0.4.0-alpha releases (104)
- DIDComm v2
  
  - [April IIW DIDComm v2 connect-a-thon](https://hackmd.io/j6U6JpQ2SRexSUKL7i2XRg)
- Aries Interop Profile 3.0 continues to be discussed [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ)
- Shared Components
  
  - Indy VDR 0.1.0-dev.12
    
    - React Native &amp; Node.JS
    - No support for older Android versions yet
  - Aries Askar 0.2.8-dev.6
    
    - React Native &amp; Node.JS
    - [https://github.com/hyperledger/aries-framework-javascript/pull/1211](https://github.com/hyperledger/aries-framework-javascript/pull/1211)
    - ACA-Pug Call talking about Askar profiles: [2023-01-24 Aries Cloud Agent - Python Users Group Community Meeting](2023-01-24-Aries-Cloud-Agent---Python-Users-Group-Community-Meeting_18501358.html)
  - AnonCreds 0.1.0-dev.11
    
    - Node.JS
    - React Native
  - Berend made a demo: [https://www.loom.com/share/8497e12cb1c64383aa01768ac2551078](https://www.loom.com/share/8497e12cb1c64383aa01768ac2551078)
- Open Source Summit in Vancouver
  
  - [https://ossna2023.sched.com/event/1K58t?iframe=no](https://ossna2023.sched.com/event/1K58t?iframe=no)

## Agenda

- Record the meeting
- Status update on Shared components
  
  - iOS lower version support 
    
    - Updates made to Aries Askar &amp; AnonCreds
    - Still need to do Indy VDR
  - Custom repo for cross images for Android builds
- Presentation from [Karim Stekelenburg](https://lf-hyperledger.atlassian.net/wiki/people/712020:c1a35915-1263-4367-b8e3-59469f567436?ref=confluence) - Future architecture of Aries Framework JavaScript
  
  - Makes sense that they're together because they're so intertwined and version synced
  - Feels more like AFJ is a thin layer that brings all existing libraries together instead of re-implementing things
  - Aries framework javascript as a generic SSI framework
    
    - what will it be called in that case?
  - What's the relation of openid to Aries (is there an Aries RFC for OpenID interop?)
  - Aries is mostly DIDComm, it wouldn't make that much sense to externalize DIDComm
    
    - Externalize can mean two things: out of the core package, same repo, or external repo
  - Survey to ask how people are using AFJ? What features are people interested in?
  - Diagram to see the different components and how they relate to each other?
  - Supported features / roles for production use case
    
    - Mobile 
      
      - (holder/verifier) wallet
      - issuer wallet
      - Issues: Performance (startup, etc.)
    - Server
      
      - issuer/verifier)
      - Mediator
      - Issues: Scalability
- Scalability / Performance issues
  
  - Startup time
  - High load, lot of records
  - (customer) encrypted database layer
  - Pagination and querying of encrypted data
  - Storing stringified JSON (and limitations when working with multiple processes)

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

[https://youtu.be/xu2cBjZGcyc](https://youtu.be/xu2cBjZGcyc)

## Future topics

Future Topics:

- It would be good to discuss OCA implementation in AFJ and in Aries Bifold and where should be a boundary between the two in this feature.
- Wallet API redesign ([Ariel Gentile](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb1c9202-3b9c-40d0-9223-41e801ce4e6e?ref=confluence) )
- Cheqd integration ([Daev Mithran](https://lf-hyperledger.atlassian.net/wiki/people/5f74949b287870006af56f0e?ref=confluence) )
- AFJ Interop tests not running

Document generated by Confluence on Nov 26, 2024 11:27

[Atlassian](http://www.atlassian.com/)
