1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-03-07 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Mar 07, 2023

## Summary:

Topics:

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio - Last One!
- Update on BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio - First One!
- VC-Authn OIDC V2.0 – Plans and Progress
- Next release?
- Discussion Topics

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

- Full Meeting:  [dummyfile.txt](#)
- Segment on VC-Authn-OIDC by [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) and  Jason Syrotuk (BC Gov): [dummyfile.txt](#)

```

```

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;,Announcements
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BCGov/Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io)&lt;warren@affinitiquest.io&gt;

## Agenda

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio
  
  - Repo renamed:  [https://github.com/hyperledger/aries-acapy-tools](https://github.com/hyperledger/aries-acapy-tools)
- Update on BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
  
  - Phase 1 almost complete – Design document to be shared.
    
    - Some implementation started to help with the design document.
- VC-Authn OIDC V2.0 – Plans and Progress and demo - [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) and Jason Syrotuck
  
  - Demo recording: [dummyfile.txt](#)
  - Phase 1: Uplift
    
    - remove the end of life .NET Identity Server component and make other adjustments, without major changes.
    - Some tweaks done – use of Mongo DB as the backend for size and performance, put VC claims into a data structure, update the OIDC endpoints to better align with OIDC model
  - Phase 2: Improvements - add new features
    
    - Support for connected use cases
    - Handling multiple claim with identical names from different source credentials
- Next Release
  
  - 0.8.0-rc0 done
    
    - Release 0.8.0 ASAP
  - Ready for a 1.0.0-rc2 release? Timing?
    
    - TBD
    - Work has started on the last AIP 2.0 issue: the handling of DIDComm peer DIDs
      
      - See notes on [issue 2156](https://github.com/hyperledger/aries-cloudagent-python/issues/2156) about how to align with AFJs DIDComm peer DIDs
      - Design document coming, and then implementation

## Upcoming Meeting Topics:

- Discussion Topics:
  
  - Update on ACA-Py Container Scanning (brought up last meeting)
  - Multi-architecture containers
    
    - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
    - Solution: A third container published that includes BBS+ package, but is single architecture
    - Others are Askar and Indy-SDK
  - Messages getting stuck when a connection is being established.
    
    - Indicio to do more investigation
  - Adding a [Documentation site](https://github.com/hyperledger/aries-cloudagent-python/issues/1951) for ACA-Py - as nice as the AFJ one - [https://aries.js.org/](https://aries.js.org/)
- Does anyone use/see a use case for Web Sockets and Return Route beyond ACA-Py as a mobile agent mediator?
- Understanding Presentation Request Revocation Intervals
  
  - [Presentation Slides](https://docs.google.com/presentation/d/1Y6ato1crftEMwAry2FtreAifW2Aj5mzjcw4xrb0uj2E/edit?usp=sharing)
  - Issue Created

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18502757/18517721.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18502757/18517720.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
