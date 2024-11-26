1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2024](ACA-Pug-Meetings-2024_18519005.html)

# Hyperledger Aries : 2024-02-06 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Feb 06, 2024

## Summary:

Topics:

- Status Updates:
  
  - AnonCreds RS
  - did:peer and AFJ Interop – where we are
  - Load Generator Testing at BC Gov
  - AnonCreds in W3C Format
  - DRPC Protocol Implementation – progress
  - ACA-Py Issue #2000
- ACA-Py 1.00 Checklist and status
- The state of ACA-Py Plugins
- PRs and Issues
- Open Discussion

## **Zoom Link**: [https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09](https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09)

## **Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

- [Aries Annual Report PR](https://github.com/hyperledger/toc/pull/212) for the Hyperledger TOC has been has been created – comments are still welcome
- DSR Webinar this Thursday, Feb 8 about all things identity:
  
  - [Decentralized Identity + Interoperability: Connecting Credo (Agent Framework Javascript) with Hyperledger Besu, Cardano, Cheqd, Hyperledger AnonCreds, and OIDC4VCFuture Calls]()
- Hyperledger Mentorship Program – now accepting project proposals – great results last year in Hyperledger AnonCreds.
- IIW coming up in April

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) (BC Gov / Petri Dish Development) &lt;amanji@petridish.dev&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio PBC) &lt;kim@indicio.tech&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov / Quartech) &lt;emiliano.sune@quartech.com&gt;

## Documentation:

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Status Updates:
  
  - AnonCreds RS in ACA-Py
    
    - Endorser being worked on – Schema done and merged, CredDef, RevReg being done
  - AnonCreds in W3C Format
    
    - Credo Demo from AnonCreds Meeting – link: [https://youtu.be/tDka6a32CY0](https://youtu.be/tDka6a32CY0)
    - ACA-Py team from What's Cookin' is progressing – draft PR opened
  - did:peer and AFJ Interop
    
    - AATH – tests implemented for did:peer:1, 2, 4
    - PR 2748 with fixes for Credo/ACA-Py for did:peer:4
      
      - Before 0.5.0 there was not a framework that does did:peer:2 or 4 in a standard way.
      - Perhaps – we should do did:peer:1 emit in ACA-Py (we already do receive).
    - Want to get Credo working for AATH – upgrade to backchannel controller for DID Exchange and OOB, restart the agent with new settings for everything
      
      - Sheldon is looking at this – starting with devcontainers so that a local environment is not needed.
      - Pick the devcontainer when you start the project – good pattern for the use of devcontainers on our repos
  - Load Generator Testing at BC Gov using [Aries Akrida](https://github.com/hyperledger/aries-akrida)
    
    - Bottom line summary – 310/issuances per minute.
    - Some changes to be pushed into Akrida
  - DRPC Support – [Aries RFC 804 PR](https://github.com/hyperledger/aries-rfcs/pull/804/files?short_path=b18d7b2#diff-b18d7b2a9c7c7719f831100c571f40ed66a1f93fa03905da6ee544fe170b4c48) - work is completed, documentation has been passed and a demo being done.
  - ACA-Py [Issue 2000](https://github.com/hyperledger/aries-cloudagent-python/issues/2000) – moving webhooks – Race condition in issue-credential v1.0 leads to credential exchange switching to abandoned state
- 1.0 Release:
  
  - Checklist [Issue](https://github.com/hyperledger/aries-cloudagent-python/issues/2753), labelled [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3A1.0.0) and [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20label%3A1.0.0)
    
    - Other issues/PRs to be added?
  - LTS Considerations per [Aries RFC 0799 Long Term Support](https://github.com/hyperledger/aries-rfcs/tree/main/concepts/0799-long-term-support)
  - Other considerations?
- The state of ACA-Py Plugins – Jamie Hale
- Other [PRs Ready for Review](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20draft%3Afalse%20) and [Issues to Discuss](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3ADiscuss)

## Upcoming Meeting Topics:

- Discussion Topics:
  
  - Update on ACA-Py Container Scanning
  - Multi-architecture containers
    
    - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
    - Solution: A third container published that includes BBS+ package, but is single architecture
    - Others are Askar

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
