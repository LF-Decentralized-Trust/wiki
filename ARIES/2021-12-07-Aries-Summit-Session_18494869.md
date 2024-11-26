1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Mobile Summit](Aries-Mobile-Summit_18494526.html)
5. [2021 Aries Mobile Summit](2021-Aries-Mobile-Summit_18494588.html)

# Hyperledger Aries : 2021-12-07 Aries Summit Session

Created by Sam Curren, last modified by Akiff Manji on Dec 14, 2021

## Summary:

- Credential UX part 2
  
  - Auto-approval of presentation requests (e.g.: trusted verifier, trusted preset, etc ...)
  - Revocation implications for Mobile
  - Consequences of Machine Readable Governance on UX

## Note: This call was recorded and the recording and chat transcript are at the bottom of the page.

## Date

07 Dec 2021 (7AM-9AM Los Angeles)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Dial-in link

[https://us02web.zoom.us/my/telegramsam](https://us02web.zoom.us/my/telegramsam) (updated!)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) &lt;sam@indicio.tech&gt;
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (BC Gov) &lt;jason.leach@fullboar.ca&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) &lt;amanji@petridish.dev&gt;

## Welcome / Introductions

## Focus

- Credential UX part 2

## Discussion Topics

- Report on OCA:
  
  - [https://github.com/hyperledger/aries-mobile-agent-react-native/issues/164](https://github.com/hyperledger/aries-mobile-agent-react-native/issues/164)
- Auto-approval of presentation requests (e.g.: trusted verifier, trusted preset, etc ...)
  
  - auto-approval of presentations can be risky (check box to auto-approve that verifier in the future.)
    
    - presentation for login - some other user could login on a computer, and your phone auto approves.
  - bulk-approval
    
    - one time bulk approval
    - present series of proofs with one user action to approve.
      
      - automate multiple presentations.
      - Aries RFC PRs:
        
        - Presentations (merged): [PR](https://github.com/hyperledger/aries-rfcs/pull/689), current [RFC 454](https://github.com/hyperledger/aries-rfcs/tree/main/features/0454-present-proof-v2) (note: not part of AIP 2.0)
        - Issuing multiple credentials: [Submitted PR](https://github.com/hyperledger/aries-rfcs/pull/692)
  - policy-approval
    
    - guardianship
    - biometric unlock allows policy approvals.
    - context matters
      
      - Location, for example – e.g. for entry into a building – but likely still needs a manual trigger - e.g. biometric
      - transport tech
    - How to get there: Do it manually first and then look for automation opportunities to make the policies crisp
    - Repeated Presentations authorized by user
    - Careful:
      
      - Have to watch for anti-patterns (e.g. a login with no human interaction).
      - Watching for the security vs. convenience trade-off.
      - Making sure that the SSI principles are followed – control is with the user.
      - A wallet is an agent – acts on behalf of the USER – fiduciary responsibility
  - Actions:
    
    - Need bulk presentation request (Present Proof) (mostly done, see above)
    - Policy to recommend bulk actions
  - Progress
    
    - Kiva - already doing multiple presentation with policy - looking forward to be policy file driven
- Consequences of Machine Readable Governance on UX
  
  - New types of user interactions
    
    - warnings of acting outside governance
    - selections of governance frameworks
    - communicating opinions of governance frameworks
    - governance framework discovery
      
      - Discover Features 2.0 Protocol can list supported frameworks
  - Types of Governance
    
    - Roots of trust
    - Identifying Participants
  - Progress:
    
    - Mike working on test applications of Machine Readable Governance
- Revocation implications for Mobile

## Action items

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [chat.txt](attachments/18494869/18515795.txt "Download")

Dec 09, 2021 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [chat.txt](attachments/18494869/18515795.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18494869/18515796.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18494869/18515794.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
