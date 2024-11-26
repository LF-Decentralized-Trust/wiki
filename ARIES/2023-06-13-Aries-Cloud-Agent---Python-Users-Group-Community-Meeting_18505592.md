1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-06-13 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Ry Jones on Jun 13, 2023

## Summary:

Topics:

- Update and Demo of BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
- Content for 0.8.2 final (or perhaps 0.9.0 final)
- ACA-Py PRs – let's play "Can We Merge This?"!
- ACA-Py Plugins – Update on progress/plans
- Adding a new Maintainer – [Jason Sherman](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b5eb4a5-0d5d-4a7f-b2cc-b2d7597a7e8c?ref=confluence)
- Discussion Topics

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

- Full Recording: [https://youtu.be/fzlQTBK9WPQ](https://youtu.be/fzlQTBK9WPQ)
- [2023 06 13 Indy Aries Combined Call Chat.txt](attachments/18505592/18518249.txt)
- [2023 06 13 Indy Aries Combined Call Transcript.txt](attachments/18505592/18518250.txt)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov/Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio PBC) &lt;alex.walker@indicio.tech&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio PBC) &lt;colton@indicio.tech&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)
- 2023.05.15 (this Thursday): Presentation: [ZKPs – the High School Math Edition](https://lf-hyperledger.atlassian.net/wiki/display/IWG/2023-06-15%3A+Identity+Special+Interest+Group) - [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) at the Identity SIG Meeting

## Agenda

- Update on BC Gov CWU – anoncreds-rs library in ACA-Py - Indicio
  
  - [https://hackmd.io/@dbluhm/anoncreds-project-update](https://hackmd.io/@dbluhm/anoncreds-project-update)
  - MVP Revocation completed
  - Significant refactors
  - Feedback to anoncreds-rs
  - What's next?
    
    - Automated registry setup
    - Genericize revocation registry recovery?
    - Adapt original Indy anoncreds interface?
    - Test updates
    - Cleaning up
- Finalizing the 0.8.2 Release contents (or will it be 0.9.0?)
- The "Can We Merge This?" Game
  
  - [ACA-Py PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) – let's take a look!
- ACA-Py Plugins – Update on progress/plans
  
  - HackMD on Plugins:
  - Add a plugins folder in ACA-Py or a separate repo for all of the ones shared by the community
    
    - Standardize the structure and conventions in using Plugins - aries-acapy-plugins
    - Current plugins:
      
      - Traction
      - Redis/Caching
      - Kafka
      - Admin Protocol plugins
      - Moving things out of ACA-Py into plugins
        
        - Clean up the core of ACA-Py in the process
        - E.g., Mediator capabilities
    - Concern – a balance, not just everything is a plugin – important things need to be 'always there'
      
      - Example: Universal resolver plugin – not used until it moved from being a plugin to the core
- Adding a Maintainer - [Jason Sherman](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b5eb4a5-0d5d-4a7f-b2cc-b2d7597a7e8c?ref=confluence)
- Adding a Dev Container to ACA-Py to help developers get started
- Creating a scalable mediator – a community effort
  
  - Start a session next week at the Aries WG Meeting – Wednesday at 7:00 Pacific / 16:00 Central Europe – [Aries Working Group](Aries-Working-Group_18481228.html)
- Other Topics/Open Discussion

## Upcoming Meeting Topics:

- Discussion Topics:
  
  - Update on ACA-Py Container Scanning
  - Multi-architecture containers
    
    - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
    - Solution: A third container published that includes BBS+ package, but is single architecture
    - Others are Askar
- Does anyone use/see a use case for Web Sockets and Return Route beyond ACA-Py as a mobile agent mediator?

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [2023 06 13 Indy Aries Combined Call Chat.txt](attachments/18505592/18518249.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [2023 06 13 Indy Aries Combined Call Transcript.txt](attachments/18505592/18518250.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
