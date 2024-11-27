1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-09-15 Indy Contributors Call

Created by Stephen Curran, last modified by Mikaela Tarkocheva on Sep 16, 2020

## Summary

Planned:

- Catch up on Indy Interop-athon
- Getting started on a new release
- Getting started on a CI/CD migration
- Getting started on the did:indy Method

## The call recording is available here: [20200915 Indy Contributors Call](#)

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- @name (Employer) &lt;email&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- Kevin Griffin (Scoir, Inc) &lt;kg@scoir.com&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) (Anonyome Labs) &lt;smccown@anonyome.com&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio.tech) &lt;lynn@indicio.tech&gt;
- Wade Barnes &lt;wade.barnes@shaw.ca&gt;
- Ajay Jadhav (AyanWorks) &lt;ajay@ayanworks.com&gt;
- [Mikaela Tarkocheva (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/557058:12be0949-3465-4537-a616-3e5d3fa61ab4?ref=confluence)  (Scoir, Inc) &lt;mikaela@scoir.com&gt;

## Related Calls and Announcements

- IIW coming soon - October

## Release Status and Work Updates

- Indy Node
  
  - Released and deployed to Sovrin MainNet on Aug. 28, 2020
- Indy SDK
  
  - Team at ABSA is considering a different architecture [https://github.com/AbsaOSS/libvcx/commits/master](https://github.com/AbsaOSS/libvcx/commits/master)
  - Next Release Timing TBD
  - Libindy on IOS Challenges: XCode 11 has a change in it to the simulator name ("-sim" added to the name) – prevents Libindy to running on the simulator - building for Sim/Linking for platform running on.
    
    - [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) investigating and looking for collaborators.  Follow ups on indy channel on RC.
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor) - Note moved to Hyperledger
  
  - Prometheus PR being reviewed/revised
    
    - Dockerizing happening, (Wade/BC Gov) expanded dashboard
- Indy/Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
    - indy-credx - [https://github.com/andrewwhitehead/indy-credx](https://github.com/andrewwhitehead/indy-credx)
    - indy-shared-rs - [https://github.com/bcgov/indy-shared-rs](https://github.com/bcgov/indy-shared-rs)
    - aries-credx
    - Aries Secure Storage
  - Ursa

## Meeting Topics

- Catch up on Indy Interop-athon - [Presentation](https://docs.google.com/presentation/d/1Dy9B7-b2fcjDvzYs68OrfNFIXJ6Z5Ixzuo4Fj6pyE-I/edit?usp=sharing)
- Getting started on a new release of indy-node
  
  - Schedule a meeting - to review the release contents.
  - This Thursday at 6AM Pacific, 3PM CET to discuss.  We'll use this Zoom room, Richard to invite interested parties.
- Getting started on a CI/CD migration
- Getting started on the did:indy Method
- Discussion
  
  - Why did the Sovrin node hard requirements get bumped to where they are today?
    
    - Factors: 
      
      - Primarily based on load testing, including load testing the Sovrin token and in particular, a token launch event.
        
        - This would trigger a spike in usage plus an ongoing higher load, plus a gradual load increase as payment events rise.
      - Also based on the load expected from revocation (gradual climb).
    - Any Indy Network must set the node hardware spec.
    - indy-node-monitor validator info includes usage information (CPU, disk space) and should be used for trending to predict when to increase resources
      
      - Clarity required on what the resources measure – e.g. overall load/disk usage on the server vs. indy-node load/disk usage.

## Future Calls

Next call:

Future:

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464400/19465473.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
