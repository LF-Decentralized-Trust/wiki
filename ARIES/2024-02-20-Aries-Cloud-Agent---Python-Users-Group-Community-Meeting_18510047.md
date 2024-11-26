1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2024](ACA-Pug-Meetings-2024_18519005.html)

# Hyperledger Aries : 2024-02-20 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Feb 20, 2024

## Summary:

Topics:

- Status ACA-Py 0.12.0rc1
- Status AnonCreds RS
- Status did:peer and AFJ Interop – where we are
- Status Load Generator Testing at BC Gov
- Status AnonCreds in W3C Format
- Upgrading an ACA-Py deployment to AnonCreds RS
- Status: ACA-Py 1.00 Checklist
- Brainstorming: ACA-Py based Hyperledger Mentorships, and call for Mentors
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

- [Aries Annual Report PR](https://github.com/hyperledger/toc/pull/212) for the Hyperledger TOC has been has been created – comments are still welcome.
- The report will be discussed at the Hyperledger TOC meeting this Thursday, Feb. 22 at 7:00 Pacific / 16:00 Central Europe – [Meeting Notice](https://lists.hyperledger.org/g/toc/viewevent?repeatid=52670&eventid=2216994&calstart=2024-02-22). Everyone from the project is invited to attend.
- Hyperledger Mentorship Program – now accepting project proposals – great results last year in Hyperledger AnonCreds.
- IIW coming up April 16-18.

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence)  (BC Gov/Quartech) &lt;emiliano.sune@quartech.com&gt;
- And 16 others...

## Documentation:

- ACA-Py documentation: [https://aca-py.org](https://aca-py.org/main/)
  
  - Being updated such that the site will be generated from the ACA-Py repo directly, rather than from aries-acapy-docs.

## Agenda

- Status Updates:
  
  - AnonCreds RS in ACA-Py
    
    - Endorser progress – PRs [2715](https://github.com/hyperledger/aries-cloudagent-python/pull/2715), [2720](https://github.com/hyperledger/aries-cloudagent-python/pull/2720), [2782](https://github.com/hyperledger/aries-cloudagent-python/pull/2782) all merged. Left?
      
      - Getting multitenancy going is next. Issue [#2767](https://github.com/hyperledger/aries-cloudagent-python/issues/2767) (needed), [#2792](https://github.com/hyperledger/aries-cloudagent-python/issues/2792) (problem with what we have)
    - Next – last? part of the AnonCreds update: Implementing a AnonCreds Methods Registry – with documentation on how to implement it.
      
      - Need an example, and an implementation.
  - AnonCreds in W3C Format
    
    - ACA-Py team from What's Cookin' is progressing – draft PR opened
  - did:peer and AFJ Interop
    
    - AATH – tests implemented for did:peer:1, 2, 4
    - PR 2748 with fixes for Credo/ACA-Py for did:peer:4
      
      - Before 0.5.0 there was not a framework that does did:peer:2 or 4 in a standard way.
      - Perhaps – we should do did:peer:1 emit in ACA-Py (we already do receive).
    - Want to get Credo working for AATH – upgrade to backchannel controller for DID Exchange and OOB, restart the agent with new settings for everything
      
      - Sheldon is looking at this – starting with devcontainers so that a local environment is not needed.
      - Pick the devcontainer when you start the project – good pattern for the use of devcontainers on our repos
    - DID Rotation – [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) is going to be working on this starting today.
  - Load Generator Testing at BC Gov using [Aries Akrida](https://github.com/hyperledger/aries-akrida)
    
    - Bottom line summary – 310/issuances per minute.
    - Some changes to be pushed into Akrida
- AnonCreds RS Update process:
  
  - Upgrade process – Issues: Single wallet: #[2776](https://github.com/hyperledger/aries-cloudagent-python/issues/2776), multitenacy wallets: #[2785](https://github.com/hyperledger/aries-cloudagent-python/issues/2785)
  - Data to be upgraded:
    
    - Issues [#2384](https://github.com/hyperledger/aries-cloudagent-python/issues/2384), [#2385](https://github.com/hyperledger/aries-cloudagent-python/issues/2385) are about revocation objects
    - Issue [#2386](https://github.com/hyperledger/aries-cloudagent-python/issues/2386) is about schemas and creddefs
    - Issue [#2389](https://github.com/hyperledger/aries-cloudagent-python/issues/2389) is about private keys related to AnonCreds objects.
    - Much less data than needed to be updated in the Indy SDK to Askar upgrade.
  - Proposal: Upgrade script to migrate from Askar to Askar-AnonCreds, similar to the Indy SDK to Askar script in [aries-acapy-tools](https://github.com/hyperledger/aries-acapy-tools).
    
    - Core approach: Stop instance, run update script, start instance.
      
      - But...what about multitenancy?
    - Side Issue: Can we extend the definition of what is in the ACA-Py plugins repository to cover the upgrade scripts currently in "[aries-acapy-tools](https://github.com/hyperledger/aries-acapy-tools)"?
      
      - Removes the need for an extra repo, and puts all of the "extras" for ACA-Py into a single place.
      - We could rename the repo, or just add information that "extends" the meaning of "plugins" to include other stuff.
      - Could also do that for examples in [aries-acapy-controllers](https://github.com/hyperledger/aries-acapy-controllers)?
    - Concerns with "in-flight" credential exchanges – do we support those?
    - Upgrades will not include going from one database type to another (e.g., sqlite to postgres).
    - See issues below about multi-tenant upgrades. I think we have to see if we can avoid a "database update" vs. a "tenant updating records per tenant".
  - Upgrading the controllers in sync with updating the wallet:
    
    - Should the execution of the upgrade block the use of the old endpoints?
      
      - Pretty much has to or one is in a mess – records in the wallet that are old school and new.
      - What do we use to do this?
        
        - Data in the wallet that is checked on startup, and that blocks the endpoints?
        - Or do we use a startup parameter for the same purpose?
        - Can we dynamically remove the endpoints from the Swagger to cut down on the open-api size?
    - Multi-tenancy – can we run the upgrade on a per tenant basis vs. all tenants?  E.g., make the script operate at the tenant level vs. the database level?
      
      - In scenarios like Traction, where each tenant might use a different controller, doing an "all at once" upgrade is extremely difficult, bordering on impossible.
      - **Question**: are we changing the database structure (I don't think so...) vs. just changing the JSON content of records?
    - Upgrade has to be run with the Agent paused – e.g. no controller operations, since we need to upgrade the data before using the new endpoints.
      
      - How do we do that with multiple tenants. We don't want to force all of the tenants to upgrade at once.
      - Idea: Implement a "pause" mechanism that holds all processing of a deployment of ACA-Py instances while the upgrade is in process.
        
        - Careful: Has to be based on data in the wallet that has to be checked continuously, just in case an upgrade might happen.
        - Idea: Start-up parameter that when set tells the instance not to proceed until a wallet value set to a preset value.
          
          - Upgrade all ACA-Py instances to new version, with parameter set. All are sleeping, waiting for magic value.
          - Run update script that updates all records, set magic value.
          - ACA-Py instances see the magic value and proceed.
          - Subsequently, remove the startup parameter, or leave it and on startup, things proceed.
  - Need documentation for the API endpoint updates – what is the minimum update needed to convert from old to new?
- Status of ACA-Py 0.12.0rc1 - done.
- Status of ACA-Py 1.0.0 Release:
  
  - Checklist [Issue](https://github.com/hyperledger/aries-cloudagent-python/issues/2753), labelled [Issues](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20label%3A1.0.0) and [PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aopen%20label%3A1.0.0)
    
    - Other issues/PRs to be added?
  - Should we wait on the AnonCreds RS work?
  - LTS Considerations per [Aries RFC 0799 Long Term Support](https://github.com/hyperledger/aries-rfcs/tree/main/concepts/0799-long-term-support)
  - Other considerations?
- Brainstorming: ACA-Py based Hyperledger Mentorships, and call for Mentors. **Ideas**:
  
  - Full pass over all the documentation and demos to make sure it is all up to date.
  - Investigating, designing and adding mDL support into ACA-Py.
  - Integrate ACA-Py and Aries SocketDock to make a hyper-scaling mediator.
  - Enabling tracing support in ACA-Py.
  - AnonCreds ideas:
    
    - Formalize the AnonCreds v2 programming interface, accounting for the existing AnonCreds v1 interface, but fully embracing AnonCreds v2.
    - Post-Quantum PS Signatures in AnonCreds v2.
    - AnonCreds v2 Cryptography Documentation.
    - Productizing ZKP-based scalable revocation using ALLOSAUR.
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
