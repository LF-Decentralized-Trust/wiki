1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-05-30 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Jun 09, 2023

## Summary:

Topics:

- Update and Demo of BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
- ACA-Py PRs – let's play "Can We Merge This?"!
- Converting from unqualified peer DIDs to did:peer:3
- Discussion Topics

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

- Full Recording: [https://youtu.be/IX2\_v2q1PDE](https://youtu.be/IX2_v2q1PDE)
- Peer DID 3 Presentation: [https://youtu.be/IX2\_v2q1PDE?t=1959](https://youtu.be/IX2_v2q1PDE?t=1959)
- [2023 05 30 ACA PUG Chat](attachments/18505311/18518153.txt)
- [2023 05 30 ACA PUG Transcript](attachments/18505311/18518153.txt)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio PBC) &lt;alex.walker@indicio.tech&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Alberto Antonio Leon](https://lf-hyperledger.atlassian.net/wiki/people/6308ef06f63ba4d04a134cf5?ref=confluence) (Instnt, Inc) &lt;alberto@instnt.org&gt;
- @Wanja Mascarenhas (Northern Block) &lt;wanja.mascarenhas@northernblock.io&gt;
- [Charles Lanahan](https://lf-hyperledger.atlassian.net/wiki/people/712020:50e56df1-41cf-415b-a802-ae0b89b9c75b?ref=confluence) &lt;charles.lanahan@gmail.com&gt;
- [Artem Ivanov](https://lf-hyperledger.atlassian.net/wiki/people/557058:490facf1-26c6-4490-955a-53ac8ac201a5?ref=confluence) DSR &lt;artem.ivanov@dsr-corporation.com&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)
- AnonCreds Workshop – Tomorrow - May 31, 2023: [https://www.hyperledger.org/event/hyperledger-anoncreds-workshop-using-zkp-verifiable-credentials-everywhere](https://www.hyperledger.org/event/hyperledger-anoncreds-workshop-using-zkp-verifiable-credentials-everywhere)

## Agenda

- Update on BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
  
  - [https://hackmd.io/@dbluhm/anoncreds-project-update](https://hackmd.io/@dbluhm/anoncreds-project-update)
- ACA-Py and Redis/Mediator – latest news
  
  - DON'T USE "info" LOGGING IN PRODUCTION!
- The "Can We Merge This?" Game
  
  - [ACA-Py PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) – let's take a look!
- peer:3 Upgrading unqualified DIDs to peer:DID:2/3 DIDs ([Recording](https://wiki.hyperledger.org/%5Brecording%5D%28https:/youtu.be/IX2_v2q1PDE?t=1959%29), [Presentation](https://docs.google.com/presentation/d/1jRwD1pRg1i7CGO3mCB6MBW7cRvoOHn-CskPvKQTKwCQ/edit?usp=sharing))
- Other Topics:

## Upcoming Meeting Topics:

- Discussion Topics:
  
  - Update on ACA-Py Container Scannin
  - Multi-architecture containers
    
    - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
    - Solution: A third container published that includes BBS+ package, but is single architecture
    - Others are Askar
- Does anyone use/see a use case for Web Sockets and Return Route beyond ACA-Py as a mobile agent mediator?

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [2023 05 30 ACA PUG.vtt](attachments/18505311/18518154.vtt) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [2023 05 30 ACA PUG.txt](attachments/18505311/18518153.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
