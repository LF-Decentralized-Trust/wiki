1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2024](ACA-Pug-Meetings-2024_18519005.html)

# Hyperledger Aries : 2024-03-19 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Mar 20, 2024

## Summary:

Topics:

- Status Update AnonCreds RS
- Status Update did:peer and AFJ Interop – where we are
- Status Update Upgrading an ACA-Py deployment to AnonCreds RS
- Status Update ACA-Py 1.00 Checklist
- Status ACA-Py 0.12.0
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

- IIW coming up April 16-18.

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov/Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

## Documentation:

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)

## Agenda

- Status Updates:
  
  - AnonCreds RS in ACA-Py
    
    - PRs for AnonCreds+CredX concurrently – after the 0.12.0 release
    - Upgrade script – PR in draft – still being worked.
  - did:peer and AFJ Interop
    
    - Connection reuse for did:peer:2/4
    - Credo/ACA-Py defined need to support 1.0 and 1.1 of DID Exchange.  Need to get the implementation done.
    - Respond in kind being done as well.
    - In the extraordinarily capable hands of [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)
  - DID Rotation – [PR #2816](https://github.com/hyperledger/aries-cloudagent-python/pull/2816) – [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) Merged.
  - Status of DRPC – Merged.
- Status of ACA-Py 0.12.0
  
  - Additional PRs to go into the release? Yes – list: 
    
    - VC-API Endpoint – need to re-add VerificationMethod
    - VC-API question:
      
      - Old: Verkey to sign and issuer as input
      - New: Issuer provided, resolve key to sign
      - Propose: Additional way, create a DID, publish it twice (Indy, did:web), choose the one to be used for signing – either resolves to the same public key.
        
        - Current way – use the same seed for two DIDs.
        - DID Alias?  "alsoKnownAs" – need additional metadata to use the alsoKnownAs as searchable metadata
        - post 0.12.0
  - Additional concepts? No
- Status of ACA-Py 1.0.0 Release:
  
  - Checklist [Issue](https://github.com/hyperledger/aries-cloudagent-python/issues/2753), labelled [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3A1.0.0) and [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20label%3A1.0.0)
    
    - Other issues/PRs to be added?
  - Should we wait on the AnonCreds RS work?
  - LTS Considerations per [Aries RFC 0799 Long Term Support](https://github.com/hyperledger/aries-rfcs/tree/main/concepts/0799-long-term-support)
  - Other considerations?
- ACA-Py Traceability Traction Test Suite Controller – being deployed
  
  - JSON-LD credentials with did:web, interact with other implementations – ed25519 signature
  - POST requests to exchange – with OAUTH2 tokens, including an implementation of StatusList2021
  - Specific to supply chains use cases and traceability vocab defined at W3C.
  - Compatibility with the VC-API
  - Potential to add ACA-Py/Traction Controller to the [https://canivc.com/](https://canivc.com/) interoperability test suite.
  - Repo available to use with docker, now adding k8s helm charts being added and an ongoing interop testing.
    
    - Same priniciples as AATH – all implementations can talk to one another.
- Hyperledger Mentorships – Indy (Read Replicas) and AnonCreds (Revocation Manager implementation)
- Other [PRs Ready for Review](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20draft%3Afalse%20) and [Issues to Discuss](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3ADiscuss)
  
  - Multi-instance ACA-Py by default.
    
    - Redis or kafka plugin for message queuing
    - Redis for cache handling.
    - Biggest issue was in connection establishment – caching disabled for that now – biggest risk eliminated
      
      - Makes local only viable – DID Rotation is exception.
      - Need for a "cluster-wide event bus" – e.g, redis event bus to notify events.
        
        - Currently using the database for polling for events that may happen on other instances.
        - Revocation is a primary user of this.
    - Trade-off – need to have a third-party dependencies.
    - Need this for Mediator based on ACA-Py using SocketDock.

## Upcoming Meeting Topics:

- Multi-architecture containers
  
  - Issue with BBS+ package – doesn't support ARM containers – need an update to their CI
  - Solution: A third container published that includes BBS+ package, but is single architecture
  - Others are Askar

## Future Topics

## Action items

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
