1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-06-27 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Ry Jones on Jun 27, 2023

## Summary:

Topics:

- ACA-Py Release 0.8.2-rc1
- Embedding AnonCreds Rust in ACA-Py – progress and plan.
- Updating Aries Mediator Service given the open sourcing of Indicio's SocketDock
- In progress - did:peer 2 and 3 support in ACA-Py
- Crazy idea: ACA-Py Startup Parameters Editor
- ACA-Py PRs – let's play "Can We Merge This?"!
- Open Discussion

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

- [https://youtu.be/hDpEJDH46Uc](https://youtu.be/hDpEJDH46Uc)
- [2023 06 27 Indy Aries Combined Call chat.txt](attachments/18505862/18518338.txt)
- [2023 06 27 Indy Aries Combined Call transcript.txt](attachments/18505862/18518339.txt)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Alberto Antonio Leon](https://lf-hyperledger.atlassian.net/wiki/people/6308ef06f63ba4d04a134cf5?ref=confluence) (Instnt, Inc) &lt;alberto@instnt.org&gt;
- [Charles Lanahan](https://lf-hyperledger.atlassian.net/wiki/people/712020:50e56df1-41cf-415b-a802-ae0b89b9c75b?ref=confluence) &lt;charles.lanahan@gmail.com&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- ACA-Py Release 0.8.2-rc1
- Embedding AnonCreds Rust in ACA-Py – progress and plan - [Presentation](https://docs.google.com/presentation/d/1GjB3tp068nTt1ISjjJoxc_v7L4zxYeyk-W6pdyxeJ-g/edit?usp=sharing)
  
  - [PR 2276](https://github.com/hyperledger/aries-cloudagent-python/pull/2276) merged to hyperledger:anoncreds-rs
  - Project board for remaining items: [https://github.com/orgs/hyperledger/projects/26](https://github.com/orgs/hyperledger/projects/26)
- Updating Aries Mediator Service given the open sourcing of Indicio's SocketDock
  
  - Side issue: Eliminating ngrok by using ACA-Py as a mediator client.
- In progress - did:peer 2 and 3 support in ACA-Py
- Crazy idea: ACA-Py Startup Parameters Editor
  
  - Address one of the more painful parts of ACA-Py – getting your startup parameters right.
  - Suggestion: 
    
    - Use something like [survey.js](https://surveyjs.io/) to generate/customize a tool to edit the settings.  Hand update.
    - Code to initialize, load and save settings, put into/out of format for the survey.js component.
    - GHA Tool to monitor changes to startup parameters
      
      - Create file with `--help`  output, script diffs current output with checked in file
      - GHA runs on each merge, creates an issue when new output differs
- ACA-Py PRs – let's play "Can We Merge This?"!
- Open Discussion

## Upcoming Meeting Topics:

- Discussion Topics:
  
  - Update on ACA-Py Container Scanning
  - Multi-architecture containers
    
    - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
    - Solution: A third container published that includes BBS+ package, but is single architecture
    - Others are Askar

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [2023 06 27 Indy Aries Combined Call chat.txt](attachments/18505862/18518338.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [2023 06 27 Indy Aries Combined Call transcript.txt](attachments/18505862/18518339.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
