1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-05-02 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on May 02, 2023

## Summary:

Topics:

- Update and Demo of BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
- Lessons Learned: Converting an ACA-Py Deployment to use Aries Askar
- Discussion Topics

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call: [dummyfile.txt](#)

Full Meeting: 

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
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio PBC) &lt;alex.walker@indicio.tech&gt;
- [Alberto Antonio Leon](https://lf-hyperledger.atlassian.net/wiki/people/6308ef06f63ba4d04a134cf5?ref=confluence) (Instnt, Inc) &lt;alberto@instnt.org&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;

## Announcements

- ACA-Py 0.8.1 released – [https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.8.](https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.8.0)1
- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Update on BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
  
  - Quick Update walkthrough (updated May 2): [https://hackmd.io/@dbluhm/anoncreds-project-update](https://hackmd.io/@dbluhm/anoncreds-project-update)
  - Design Doc: [https://hackmd.io/@dbluhm/anoncreds-design-doc](https://hackmd.io/@dbluhm/anoncreds-design-doc)
  - Open PR: [https://github.com/hyperledger/aries-cloudagent-python/pull/2191](https://github.com/hyperledger/aries-cloudagent-python/pull/2191)
  - Additional work on Revocation: [https://github.com/Indicio-tech/aries-cloudagent-python/tree/feature/anoncreds-revocation-again](https://github.com/Indicio-tech/aries-cloudagent-python/tree/feature/anoncreds-revocation-again)
- Lessons Learned: Upgrading an ACA-Py Deployment from Indy SDK to Aries Askar - [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
- Subtle web hook change noted in controllers ([ACA-Py Issue 2217](https://github.com/hyperledger/aries-cloudagent-python/issues/2217)) as a result of change in [ACA-Py PR 2099](https://github.com/hyperledger/aries-cloudagent-python/pull/2099)
  
  - Is there a way to keep the goodness of 2099 without upsetting the state machine handling in controllers?
  - Or do we document the issue?
- Ursa End of Life impacts on Aries:
  
  - CL Signatures being moved from Ursa to AnonCreds, only dependencies are in anoncreds-rs and indy-shared-rs
  - BLS Signatures being moved from Ursa to Indy, along with a Python wrapper. Dependencies are in Indy.
  - BBS Signatures being moved from Ursa to Aries, with Wrapper updates needed in a repository in Mattr Global. Dependencies in Aries (ACA-Py).
  - All continue to work with the existing Ursa code, but moving them out of Ursa will place them more closely with where they are being used.
- Other Topics:

## Upcoming Meeting Topics:

- Discussion Topics:
  
  - Update on ACA-Py Container Scanning (brought up last meeting)
  - Multi-architecture containers
    
    - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
    - Solution: A third container published that includes BBS+ package, but is single architecture
    - Others are Askar and Indy-SDK
  - Messages getting stuck when a connection is being established.
  - Adding a [Documentation site](https://github.com/hyperledger/aries-cloudagent-python/issues/1951) for ACA-Py - as nice as the AFJ one - [https://aries.js.org/](https://aries.js.org/)
- Does anyone use/see a use case for Web Sockets and Return Route beyond ACA-Py as a mobile agent mediator?
- Understanding Presentation Request Revocation Intervals
  
  - [Presentation Slides](https://docs.google.com/presentation/d/1Y6ato1crftEMwAry2FtreAifW2Aj5mzjcw4xrb0uj2E/edit?usp=sharing)
  - Issue Created

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18504577/18518033.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
