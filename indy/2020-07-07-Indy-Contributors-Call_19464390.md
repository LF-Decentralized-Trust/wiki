1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-07-07 Indy Contributors Call

Created by Stephen Curran, last modified on Jul 07, 2020

## Summary

Planned:

- The Issue Game - addressing PRs
- New repo: indy-node-monitor
- Backgrounder: indy-vdr

## The call recording is available here: [20200707 Indy Contributors Call](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Brent Zundel](https://lf-hyperledger.atlassian.net/wiki/people/557058:bf590372-a52e-4c12-b1da-0c07b8b0a512?ref=confluence) (Evernym) &lt;brent.zundel@evernym.com&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Related Calls and Announcements

- Identity Implementer Working Group call ([Wiki Page](https://lf-hyperledger.atlassian.net/wiki/display/IWG/Identity+WG+Implementers+Call)) - every 2nd Thursday
- Messages for John Jordan - [https://miro.com/app/board/o9J\_kp34wZs=/](https://miro.com/app/board/o9J_kp34wZs=/)

## Release Status and Work Updates

- Indy Node
  
  - Timing TBD:
    
    - Replacing Indy Crypto with Ursa(Kiva)
      
      - Test are running as I type...
    - ? More "rich schema" objects
    - ? Ubuntu 20.04 (Kiva) - other dependencies - [Jira Issue](https://jira.hyperledger.org/browse/INDY-2196)
- Indy SDK
  
  - Timing TBD:
    
    - Indy VDR into LibIndy
    - Indy Credx into LibIndy
- Indy/Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
      
      - Recent PRs from [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence) related to demo; start of a node-js wrapper
      - One open PR - callback ID
      - Simple example in the script that is a start point for indy-node-monitor
      - Working on the CI/CD pieces to produce multi-platform artifacts
    - indy-credx - [https://github.com/andrewwhitehead/indy-credx](https://github.com/andrewwhitehead/indy-credx)
      
      - No updates
      - To be moved to BC Gov and then to Hyperledger
    - indy-shared-rs - [https://github.com/bcgov/indy-shared-rs](https://github.com/bcgov/indy-shared-rs)
      
      - Shared features across indy-vdr and indy-credx
      - pack/unpack on Ursa (not libsodium)
      - To be moved to Hyperledger
      - Three crates - indy-utils, key derivation/pack/unpack/base58, indy-anon-creds (data types for credentials, reduce dependencies), indy-test (dev genesis file)
    - aries-credx
      
      - [https://github.com/sovrin-foundation/aries-credx-framework-rs](https://github.com/sovrin-foundation/aries-credx-framework-rs)
        
        - 6 most common attribute encodings (but not anoncreds 1 attribute encoding)
      - Can make a non-revocable credential and create proofs.
    - Aries Secure Storage initiatives:
      
      - Andrew is making progress on this. Covered on Aries WG call. Recording available on [this page](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=18487296).
      - Key management
      - Demo planned for this week's [ACA-Pug call](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/ACA-Pug+Meetings).
  - Ursa
    
    - BBS+, Revocation work 2.0 work
    - Current Release: 0.3.2, but 0.3.4 is ready. What's happening with the release?
      
      - Last PR merged yesterday, Ursa call this week
      - Attempts to use main branch in libindy – compile errors, so there is a cleanup needed.
      - indy-vdr is using pre-release 0.3.4, but needs published Ursa crate

## Meeting Topics

- [Brent Zundel](https://lf-hyperledger.atlassian.net/wiki/people/557058:bf590372-a52e-4c12-b1da-0c07b8b0a512?ref=confluence) The Issue Game: PRs to be reviewed:
  
  - [https://github.com/hyperledger/indy-node/pull/1604](https://github.com/hyperledger/indy-node/pull/1604)
  - [https://github.com/hyperledger/indy-node/pull/1607](https://github.com/hyperledger/indy-node/pull/1607)
  - [https://github.com/hyperledger/indy-node/pull/1608](https://github.com/hyperledger/indy-node/pull/1608)
  - [https://github.com/hyperledger/indy-plenum/pull/1486](https://github.com/hyperledger/indy-plenum/pull/1486)
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) indy-node-monitor repo
  
  - Simple docker image based on indy-vdr to collect validator info - if you have the authority
  - Help Wanted: Parse the JSON and extract useful information for notifications and trending.
- [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence) an introduction to [indy-vdr](https://github.com/hyperledger/indy-vdr)

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464390/19465438.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
