1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-04-04 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Apr 05, 2023

## Summary:

Topics:

- Update and Demo of BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
- ACA-Py Upgrades – recent news.
- Discussion Topics

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call

Full Meeting: [dummyfile.txt](#)

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
- [Alberto Antonio Leon](https://lf-hyperledger.atlassian.net/wiki/people/6308ef06f63ba4d04a134cf5?ref=confluence) (Instnt, Inc.) &lt;alberto@instnt.org&gt;
- [Tim Bloomfield](https://lf-hyperledger.atlassian.net/wiki/people/5a70c8faa02421507dce29c3?ref=confluence) (Ontario Gov) &lt;tim.bloomfield@ontario.ca&gt;

## Announcements

- ACA-Py 0.8.0 released – [https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.8.0](https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.8.0)
- ACA-Py 0.8.1 Coming Real Soon – problems with upgrades...
- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)
- IIW Coming Soon – April 18-20, 2023
  
  - [Kyle Robinson](https://lf-hyperledger.atlassian.net/wiki/people/60e73ed74134aa0069502ec1?ref=confluence) – BC Gov EMDT
  - [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) – What's new with Indy
  - [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) – AnonCreds

## Agenda

- Update on BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
  
  - Quick Update walkthrough: [https://hackmd.io/@dbluhm/anoncreds-project-update](https://hackmd.io/@dbluhm/anoncreds-project-update)
  - Design Doc: [https://hackmd.io/@dbluhm/anoncreds-design-doc](https://hackmd.io/@dbluhm/anoncreds-design-doc)
  - Open PR: [https://github.com/hyperledger/aries-cloudagent-python/pull/2191](https://github.com/hyperledger/aries-cloudagent-python/pull/2191)
  - Additional work on Revocation: [https://github.com/Indicio-tech/aries-cloudagent-python/tree/feature/anoncreds-revocation-again](https://github.com/Indicio-tech/aries-cloudagent-python/tree/feature/anoncreds-revocation-again)
- Upgrading Upgrades – Challenges with ACA-Py upgrades found in 0.8.0, so 0.8.1 will be released Real Soon Now
  
  - Slide [Presentation](https://docs.google.com/presentation/d/1UzwWs5ljfp-OAI3Gosnwxo150Y1IphqS3GI_0tygqS8/edit?usp=sharing)
  - Here's what's happening...lots of updates in 0.8.1.
- Other Topics
  
  - Instnt:
    
    - Mediator Service repo in AWS – working 90%/stable, but with Bifold.
    - Seeing the same issues.
    - Upgrade "--from-version 0.7.5 --force-upgrade"
    - Should be automatic when going to 0.8.1 – we'll keep you posted.

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18503879/18517899.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
