1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-06-15 Indy Contributors Call

Created by Stephen Curran, last modified on Jun 15, 2020

## Summary

Planned:

- Revocation 2.0 and BBS+ Progress in Ursa
- Draft Sovrin MainNet Roadmap

## The call recording is available here: [20200615 Indy Contributors Call](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Calls and Announcements

- Identity Implementer Working Group call ([Wiki Page](https://lf-hyperledger.atlassian.net/wiki/display/IWG/Identity+WG+Implementers+Call)) - every 2nd Thursday

## Release Status and Work Updates

- Indy Node
  
  - Security Release
  - June Release Planned 
    
    - Replacing Indy Crypto with Ursa (Kiva)
    - ? More "rich schema" objects
    - ? Ubuntu 20.04 (Kiva) - other dependencies - [Jira Issue](https://jira.hyperledger.org/browse/INDY-2196)
- Indy SDK
  
  - June(?):
    
    - Indy VDR into LibIndy
    - Indy Credx into LibIndy
- Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
      
      - No progress - only outstanding issue - merge refactoring PR
    - indy-credx - [https://github.com/andrewwhitehead/indy-credx](https://github.com/andrewwhitehead/indy-credx)
      
      - No progress
      - To be moved to BC Gov and then to Hyperledger
    - indy-shared-rs - [https://github.com/bcgov/indy-shared-rs](https://github.com/bcgov/indy-shared-rs)
      
      - Shared features across indy-vdr and indy-credx
      - pack/unpack on Ursa (not libsodium)
      - To be moved to Hyperledger
    - aries-credx
      
      - [https://github.com/sovrin-foundation/aries-credx-framework-rs](https://github.com/sovrin-foundation/aries-credx-framework-rs)
        
        - 6 most common attribute encodings (but not anoncreds 1 attribute encoding)
      - Can make a non-revocable credential and create proofs.
    - Aries Secure Storage initiatives:
      
      - Andrew is making progress on this. Aries WG topic on Wednesday.
  - Ursa
    
    - BBS+, Revocation work 2.0 work
    - Current Release: 0.3.2

## Meeting Topics

- Moving the meeting time - proposed: every second Tuesday, 8AM Pacific, other suggestions?
- Mike Lodder - Revocation 2.0 and BBS+ progress in Ursa - what's happening?

## Future Calls

Next call:

- Draft Sovrin Roadmap - Presentation
  
  - Operations - Monitoring, Maintainability, Contributors to Indy
  - Functions - Revocation 2.0, etc.
  - Scalability - Performance Test Process, Optimizations - incremental and larger

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464386/19465427.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
