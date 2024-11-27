1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-06-23 Indy Contributors Call

Created by Stephen Curran, last modified on Jun 23, 2020

## Summary

Planned:

- Sovrin MainNet Needs and Indy Collaborations

## The call recording is available here: [2020.06.23 Indy Contributors Call](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Sovrin Foundation and Indicio Tech) &lt;lynn@sovrin.org&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Brent Zundel](https://lf-hyperledger.atlassian.net/wiki/people/557058:bf590372-a52e-4c12-b1da-0c07b8b0a512?ref=confluence)  (Evernym) &lt;brent.zundel@evernym.com&gt;

## Related Calls and Announcements

- Identity Implementer Working Group call ([Wiki Page](https://lf-hyperledger.atlassian.net/wiki/display/IWG/Identity+WG+Implementers+Call)) - every 2nd Thursday

## Release Status and Work Updates

- Indy Node
  
  - Security Release - 1.12.3 is current release.
    
    - Need an official release.
  - June/July Release Planned 
    
    - Replacing Indy Crypto with Ursa(Kiva)
      
      - Test are running as I type...
    - ? More "rich schema" objects
    - ? Ubuntu 20.04 (Kiva) - other dependencies - [Jira Issue](https://jira.hyperledger.org/browse/INDY-2196)
- Indy SDK
  
  - June(?):
    
    - Indy VDR into LibIndy
    - Indy Credx into LibIndy
- Indy/Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
      
      - No change - only outstanding issue - merge refactoring PR
      - New GUI-based app for Signing Transactions created using indy-vdr - [https://github.com/andrewwhitehead/endorser-tool](https://github.com/andrewwhitehead/endorser-tool)
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
      
      - Andrew is making progress on this. Covered on Aries WG call. Recording (should be) available on [this page](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=18487296).
  - Ursa
    
    - BBS+, Revocation work 2.0 work
    - Current Release: 0.3.2

## Meeting Topics

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) Indy efforts needed by Sovrin
  
  - Operations - Monitoring, Maintainability, Contributors to Indy
  - Functions - Revocation 2.0, etc.
  - Scalability - Performance Test Process, Optimizations - evolutionary and revolutionary
- Sovrin Network update [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)
  
  - Some churn on the networks
  - Security update
  - Some issues with today - "Unreachable nodes" - to be addressed. Still in consensus - 2 nodes can't talk to one other node each.
  - 25 nodes on BuilderNet, 12 nodes on StagingNet and 20 Nodes on MainNet

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464388/19465434.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
