1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-02-21 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Feb 21, 2023

## Summary:

Topics:

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio
- Plugins - documentation and an overview
- Key Updates needed in ACA-Py
- Open Discussion

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call: [dummyfile.txt](#)

- Full Meeting:
- Topics:

```

```

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

- AnonCreds v2.0 Working Group – [Meetings](/wiki/pages/createpage.action?spaceKey=ANONCREDS&title=Meetings%3A%20AnonCreds%20v2.0%20Working%20Group)
- OWF Presentation on Aries

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;,Announcements
- [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) (Anon Solutions) &lt;iancostanzo@gmail.com&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio) &lt;alex.walker@indicio.tech&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio) &lt;daniel@indicio.tech&gt;
- [Victor Martinez](https://lf-hyperledger.atlassian.net/wiki/people/557058:73fff461-39df-4cc9-85d1-7b8a65773bee?ref=confluence) (SICPA) &lt;victor.martinez@sicpa.com&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov / Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio PBC) &lt;char@indicio.tech&gt;

## Agenda

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio
  
  - Work is done!
  - Repo is now in Hyperledger: [https://github.com/hyperledger/aries-acapy-wallet-upgrade](https://github.com/hyperledger/aries-acapy-wallet-upgrade)
  - One issue that is dependent on an Askar update: [https://github.com/hyperledger/aries-acapy-wallet-upgrade/issues/7](https://github.com/hyperledger/aries-acapy-wallet-upgrade/issues/7)
  - Working on a Docker issue in the GitHub Action. Docker image publishing is fixed.
- Plugins discussion – Ian Costanzo
  
  - [https://docs.google.com/presentation/d/1DoBsDGUEGtodteX57-O8S0TD22XrQFwL8unsals-MaY/edit?usp=sharing](https://docs.google.com/presentation/d/1DoBsDGUEGtodteX57-O8S0TD22XrQFwL8unsals-MaY/edit?usp=sharing)
  - Recommended: An "app store" repo of community developed, accepted ACA-Py Plugins, plus a directory of all ACA-Py Plugins, within or outside of the community plugins repo
  - Suggestions given on the last page of potential plugins pulled from the core – mediator, endorser considered to be high on the list, also, DID Methods, VC formats and AnonCreds methods.
  - The Event Bus is a useful component for triggering activation of plugins, but care must be taken to not use it for cross-instance communication. Rely on queuing for that.
  - Extend AATH to support the use of plugins for tests.
  - Potential issue – plugins dependent on plugins could create the need for a package manager-type functionality.
    
    - For now, developers must manage plugins by updating both the Python `requirements` and the plugins references in the config params/YAML.
- Didn't get to these issues – run through these next meeting.
  
  - Updates from previous meetings:
    
    - Update on ACA-Py Container Scanning (brought up last meeting)
    - Multi-architecture containers
      
      - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
      - Solution: A third container published that includes BBS+ package, but is single architecture
      - Others are Askar and Indy-SDK
    - Messages getting stuck when a connection is being established.
      
      - Indicio to do more investigation
    - Adding a [Documentation site](https://github.com/hyperledger/aries-cloudagent-python/issues/1951) for ACA-Py - as nice as the AFJ one - [https://aries.js.org/](https://aries.js.org/)
    - Next Release – completed – 0.8.0-rc0
      
      - Ready for final 0.8.0 release?
      - Ready for a 1.0.0-rc2 release?
- Important updates to be made to ACA-Py
  
  - Presentation: [ACA-Py Focus on Adoption](https://docs.google.com/presentation/d/1E-8JjAdfC5rROVUyyA6OMXqQqli1m1QQskZQ9PqBUZo/edit?usp=sharing)
    
    - DID Handling – all DIDs
      
      - And AnonCreds objects on any ledger/VDR
    - AIP 2.0 completion, including AATH tests
    - Cleanup tasks
    - Multi-tenant: Instance features made adjustable by tenants
    - Refactoring – especially with plugins
    - OCA Support
    - Building on the AFJ OpenID4VCs capabilities – what they are, how to use them.
- Open Discussion

## Upcoming Meeting Topics:

- Does anyone use/see a use case for Web Sockets and Return Route beyond ACA-Py as a mobile agent mediator?
- Understanding Presentation Request Revocation Intervals
  
  - [Presentation Slides](https://docs.google.com/presentation/d/1Y6ato1crftEMwAry2FtreAifW2Aj5mzjcw4xrb0uj2E/edit?usp=sharing)
  - Issue Created
- Status of vc-authn-oidc repository – v2.0 branch.

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18502451/18517644.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
