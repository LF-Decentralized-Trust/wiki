1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2024](ACA-Pug-Meetings-2024_18519005.html)

# Hyperledger Aries : 2024-01-23 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Jan 23, 2024

## Summary:

Topics:

- Status Updates:
  
  - AnonCreds RS
  - did:peer and AFJ Interop – where we are
  - Load Generator Testing at BC Gov
  - Interop with the W3C Traceability site
  - AnonCreds in W3C Format
  - DRPC Protocol Implementation – progress
- Next Release discussion - timing, content and
- ACA-Py Roadmap for 2024
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

- Hyperledger Project Annual Reports being prepared now for Aries, AnonCreds and Indy.
- IIW coming up in April

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov / Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) (BC Gov / Petri Dish Development) &lt;amanji@petridish.dev&gt;

## Documentation:

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Status Updates:
  
  - AnonCreds RS in ACA-Py
  - AnonCreds in W3C Format
  - did:peer and AFJ Interop – where we are?
    
    - AATH – tests implemented for did:peer:1, 2, 4
    - Want to get AFJ working for AATH – upgrade to backchannel controller for DID Exchange and OOB, restart the agent with new settings for everything
  - Load Generator Testing at BC Gov using [Aries Akrida](https://github.com/hyperledger/aries-akrida)
  - Interop with the W3C Traceability site
  - New item: DRPC Support – [Aries RFC 804 PR](https://github.com/hyperledger/aries-rfcs/pull/804/files?short_path=b18d7b2#diff-b18d7b2a9c7c7719f831100c571f40ed66a1f93fa03905da6ee544fe170b4c48)
- Next Release:
  
  - Ready for RC0?
  - Current contents that would be released – [53 PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20merged%3A%3E2023-11-25)
  - What to call the release – 0.11.1, 0.12.0, 1.0.0 (rc4)?
    
    - Side note: Where we are with [AIP 2.0 support](https://github.com/hyperledger/aries-cloudagent-python/blob/main/SupportedRFCs.md#aip-20).
    - Do 0.12.0 now and if we are ready right after that, do a 1.0.0 that is essentially the same – but with some use in the wild.
      
      - Action: 0.12.0-rc0 to be created and released.
  - What is needed to be included in the release:
    
    - Too constrained DID Validation: [#2714](https://github.com/hyperledger/aries-cloudagent-python/issues/2714)/[#2610](https://github.com/hyperledger/aries-cloudagent-python/issues/2610)
    - DID Rotation: [#2639](https://github.com/hyperledger/aries-cloudagent-python/issues/2639)/[PR#2494](https://github.com/hyperledger/aries-cloudagent-python/pull/2494)
    - VC API Endpoints: [PR#2710](https://github.com/hyperledger/aries-cloudagent-python/pull/2710)
    - Others?
      
      - Update the PyDID package – issue exists
      - How the verification method is fetch for did:web (PyLD – an error) – workaround PR until it is fixed in PyLD. [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence)
      - How to indicate you have a public did:web registered – verificationMethod is needed in the options – default verificationMethod? [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence) to enter issue.
- Aries Cloud Agent Python Roadmap for 2024
  
  - Hyperledger TOC Requirement for projects to submit an [Annual Report](https://toc.hyperledger.org/governing-documents/project-annual-review.html) that includes a Roadmap for 2024
  - [Draft Aries Annual Report](https://docs.google.com/document/d/1u42q8HzZ7DwK_Nudmfa0T15yCdwUCZ2vRbeXm4U76K8/edit?usp=sharing) has been created and is being reviewed by the Aries Community
    
    - Please review, update, add to, and comment on!
  - Roadmap items applicable to ACA-Py:
    
    - Current work (above)
    - DID Rotate, leading to DIDComm v2 (and ToIP Trust Spanning Layer?)
    - did:webs (we think...) support – registrar and resolver
    - Improved Documentation/Tools/Webinars e.g.,
      
      - Scalability Report
      - ACA-Py Beyond DIDComm/AnonCreds – other protocols other VC formats
    - Release 1.0 LTS
    - Others:
      
      - Other VC types (e.g., mDL), expanded credential exchange protocols
      - More OpenID4VC support
- Other [PRs Ready for Review](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20draft%3Afalse%20) and [Issues to Discuss](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3ADiscuss)

## Upcoming Meeting Topics:

- Discussion Topics:
  
  - Update on ACA-Py Container Scanning
  - Multi-architecture containers
    
    - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
    - Solution: A third container published that includes BBS+ package, but is single architecture
    - Others are Askar
- The DSR team has started looking into supporting the "please-ack" protocol. A draft PoA will likely be ready for review on the next call, 17 Oct 2023

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
