1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-08-22 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Sean Bohan on Sep 05, 2023

## Summary:

Topics:

- Using Public DIDs (e.g., did:web DIDs) for DIDComm Connections
- Release 0.10.0 Status
- Update: Hyperledger AnonCreds Rust in ACA-Py
- Update: Qualified Peer DIDs in ACA-Py
- PRs and Other Issues
  
  - Poetry, Nightly Builds, Flake8, and more!
- Open Discussion

**Zoom Link**: [https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09](https://zoom.us/j/98856745538?pwd=VkJROWRxeW43d3hOdnJLemwrS0JKUT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call:

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
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov/Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Jason Sherman](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b5eb4a5-0d5d-4a7f-b2cc-b2d7597a7e8c?ref=confluence) (BC Gov/Quartech) &lt;jason@usingtechnolo.gy&gt;
- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence)  (Indicio PBC) &lt;char@indicio.tech&gt;

## Announcements

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Using Public DIDs (e.g., did:web DIDs) for DIDComm Connections - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) #2409
- Release 0.10.0 Status
  
  - Add 2409 – then 0.10.0-rc1
  - After testing - 0.10.0 release
- Update: Hyperledger AnonCreds Rust in ACA-Py
  
  - Breaking Change: Remove RevReg Create capabilities from Admin API – only ACA-Py will handle from now on.
  - Breaking Change: Remove Endorsement management from Admin API – only ACA-Py will handle from now on.
- Update: Qualified Peer DIDs in ACA-Py
- [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) and [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues)
  
  - Poetry
  - Flake8
  - Nightly Builds
  - More...
  - Old ones (suggested for discussion by [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)): 
    
    - [https://github.com/hyperledger/aries-cloudagent-python/issues/1042](https://github.com/hyperledger/aries-cloudagent-python/issues/1042) - https message type prefix
    - [https://github.com/hyperledger/aries-cloudagent-python/issues/1044](https://github.com/hyperledger/aries-cloudagent-python/issues/1044) - updated media types
    - Yes!  Need to decide exactly the behaviour to change.
      
      - Document what is there today.
      - Decide what will be the new behaviour – simply drop the old style or add a flag that defaults but allows the old style?  Hopefully no new flag...
      - The existing flag should continue to be accepted, I think, although we could drop it as well.
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

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
