1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-03-21 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Mar 21, 2023

## Summary:

Topics:

- Update on BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
- ACA-Py Plugins Reimagined
  
- ACA-Py Releases
- ACA-Py Kubernetes Throttling
- Discussion Topics

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call

Full Meeting: [dummyfile.txt](#)

Segment on Plugins by [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) : [dummyfile.txt](#)

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
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;
- [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) (Anon Solutions) &lt;iancostanzo@gmail.com&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov / Quartech) &lt;emiliano.sune@quartech.com&gt;

## Announcements

- ACA-Py 0.8.0 released – [https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.8.0](https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.8.0)
- IIW Coming Soon – April 18-20, 2023

## Agenda

- Update on BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
  
  - Design doc published/accepted
  - Split resolver/registrar
  - Work on all the objects
  - Python Wrapper – updates – this seems to be extra than expected
- Plugins - a new approach, from [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) – based on this HackMd.io document: [https://hackmd.io/BnrTas1gQ3aC\_-qP7G-Rcg?view](https://hackmd.io/BnrTas1gQ3aC_-qP7G-Rcg?view)
  
  - Next step – call to action on making the changes, timing, impacts on ACA-Py itself, and on breaking changes for existing plugins
- Next Release
  
  - 0.8.0 done
  - Ready for a 1.0.0-rc2 release? Timing? Today? No – leave it for now.
    
    - Work has started on the last AIP 2.0 issue: the handling of DIDComm peer DIDs
      
      - See notes on [issue 2156](https://github.com/hyperledger/aries-cloudagent-python/issues/2156) about how to align with AFJs DIDComm peer DIDs
      - Design document coming, and then implementation
- Concern about ACA-Py throttling on Kubernetes platforms – Issue [2157](https://github.com/hyperledger/aries-cloudagent-python/issues/2157)
  
  - Question: Is there anything inherently different about ACA-Py from other "typical" Python apps that makes it worse on Kubernetes?
  - Is the use of threading and the operation of the GIL ([Global Interpreter Lock](https://realpython.com/python-gil/)) a problem?
- Other Topics

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18503377/18517810.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18503377/18517809.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18503377/18517808.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
