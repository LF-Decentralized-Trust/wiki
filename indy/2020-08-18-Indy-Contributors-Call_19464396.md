1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-08-18 Indy Contributors Call

Created by Stephen Curran, last modified on Aug 18, 2020

## Summary

Planned:

- Update on Indy Node release
- Preparations/pre-work for the Indy Interop-athon

## The call recording is available here: [20200818 Indy Contributors Call Recording](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;

## Related Calls and Announcements

- Join Us: Indy Interop-athon Virtual Conference - Sept. 1, 2 - [Indy Interop-a-thon - Making "Network of Networks" Real](https://lf-hyperledger.atlassian.net/wiki/spaces/II/overview)
  
  - Request for a sponsor to cover the cost of the conference platform

## Release Status and Work Updates

- Indy Node
  
  - Release in progress - update from Wade Barnes
- Indy SDK
  
  - Significant changes in LibVCX
  - Team at ABSA is considering a different architecture
    
    [https://github.com/AbsaOSS/libvcx/commits/master](https://github.com/AbsaOSS/libvcx/commits/master)
  - Next Release Timing TBD
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor) - Note moved to Hyperledger
- Indy/Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
      
      - has new go wrapper
    - indy-credx - [https://github.com/andrewwhitehead/indy-credx](https://github.com/andrewwhitehead/indy-credx)
      
      - plan is to merge with indy-shared-rs
    - indy-shared-rs - [https://github.com/bcgov/indy-shared-rs](https://github.com/bcgov/indy-shared-rs)
    - aries-credx
    - Aries Secure Storage initiatives:
  - Ursa
    
    - BBS+, Revocation work 2.0 work
    - Current Release: 0.3.4 is ready.

## Meeting Topics

- Preparation for the initial topics at the Indy Interop-athon - [Indy Interop-athon - Making "Network of Networks" Real](https://lf-hyperledger.atlassian.net/wiki/spaces/II/overview)
  
  - Topics planned for the Interop-athon - [Presentation](https://docs.google.com/presentation/d/1QH0R_AieTOv1-mTI_Y95ja-oPe37DmCBbTVbINWHWPc/edit?usp=sharing)
    
    - Creating an did:indy DID Method Specification, including namespacing mechanism
    - Method for finding network metadata (genesis file, governance information)
    - Indy and KERI: Ready for Prime Time?
    - Indy support for DID Docs ([Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)'s [document](https://docs.google.com/document/d/1PE1KQHf41zlHbLm27UbgzJ7t7m2xr09JnjZWFT2ApwE/edit#heading=h.2hcnku6wb1f9) discussed at a [recent Indy Contributors call](2020-07-21-Indy-Contributors-Call_19464392.html)).
    - Updating Indy SDK to store and use objects with network references
    - Updating Indy VDR and Aries Storage to use objects with network references
    - Defining the backlog
    - Getting the work done
- Indicio's networks.
- Demo of the new Indy Monitoring board setup for the Sovrin network.

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464396/19465462.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
