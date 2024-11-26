1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2024](ACA-Pug-Meetings-2024_18519005.html)

# Hyperledger Aries : 2024-03-05 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Mar 05, 2024

## Summary:

Topics:

- Presentation/Demo about AnonCreds in W3C VCDM format
- Status ACA-Py 0.12.0rc1
- Status AnonCreds RS
- Status did:peer and AFJ Interop – where we are
- Upgrading an ACA-Py deployment to AnonCreds RS
- Status: ACA-Py 1.00 Checklist
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

- [Hyperledger Mentorship Program](https://lf-hyperledger.atlassian.net/wiki/display/INTERN/Hyperledger+Mentorship+Program) – now accepting project proposals through March 15, 2024 – great results last year in Hyperledger AnonCreds.
- IIW coming up April 16-18.

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io) &lt;warren@affinitiquest.io&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov / Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) &lt;BC Gov / Petri Dish Development&gt; &lt;amanji@petridish.dev&gt;

## Documentation:

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Presentation/Demo about AnonCreds in W3C VCDM format – Whats Cookin'
- Status Updates:
  
  - AnonCreds RS in ACA-Py
    
    - Endorser progress – PRs [2715](https://github.com/hyperledger/aries-cloudagent-python/pull/2715), [2720](https://github.com/hyperledger/aries-cloudagent-python/pull/2720), [2782](https://github.com/hyperledger/aries-cloudagent-python/pull/2782) all merged. Done!
    - AnonCreds RS Update process - Issue [#2808](https://github.com/hyperledger/aries-cloudagent-python/pull/2808)
      
      - Key concern – multi-tenant handling around enabling tenants to independently update when they are ready.
      - Handling is detailed in the issue.
      - Biggest change – enabling the use of Askar and Askar AnonCreds wallet types at the same time
        
        - credx and anoncreds-rs libraries both loaded.
        - All endpoints (old and new) available
  - did:peer and AFJ Interop
    
    - AATH – tests implemented for did:peer:1, 2, 4
    - PR 2748 with fixes for Credo/ACA-Py for did:peer:4
      
      - 1.0 and 1.1 support for 0023 DiD Exchange
    - Want to get Credo working for AATH – upgrade to backchannel controller for DID Exchange and OOB, restart the agent with new settings for everything
      
      - Sheldon is looking at this – starting with devcontainers so that a local environment is not needed.
      - Pick the devcontainer when you start the project – good pattern for the use of devcontainers on our repos
  - DID Rotation – [PR #2816](https://github.com/hyperledger/aries-cloudagent-python/pull/2816) – [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence)
    
    - Getting close – applying updates from feedback on the PR
    - Two more endpoints – creating the DID Peer 2, 4
    - Concern generally about DID Peer creation related to the DIDComm service – `did-communication`  vs. DIDCommMessaging  - making sure that if you use one or the other, the related data must be consistent.
      
      - ACA-Py should be using `did-communication only -- the related data should be a string -- not JSON. -- verify this.`
  - Status of DRPC – working, adjustment to the protocol to support a problem report.
- Status of ACA-Py 0.12.0rc2 - ready to go?
  
  - What PRs are needed for it?
- Status of ACA-Py 1.0.0 Release:
  
  - Checklist [Issue](https://github.com/hyperledger/aries-cloudagent-python/issues/2753), labelled [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3A1.0.0) and [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20label%3A1.0.0)
    
    - Other issues/PRs to be added?
  - Should we wait on the AnonCreds RS work?
  - LTS Considerations per [Aries RFC 0799 Long Term Support](https://github.com/hyperledger/aries-rfcs/tree/main/concepts/0799-long-term-support)
  - Other considerations?
- Other [PRs Ready for Review](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20draft%3Afalse%20) and [Issues to Discuss](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3ADiscuss)

## Upcoming Meeting Topics:

- Multi-architecture containers
  
  - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
  - Solution: A third container published that includes BBS+ package, but is single architecture
  - Others are Askar

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
