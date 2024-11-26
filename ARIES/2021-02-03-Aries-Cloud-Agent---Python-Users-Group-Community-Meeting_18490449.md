1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2021](ACA-Pug-Meetings-Archive-2021_18514526.html)

# Hyperledger Aries : 2021-02-03 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Feb 03, 2021

## Summary:

Planned Topics:

- Preparation for the 0.6.0 release
- W3C Verifiable Credentials in ACA-Py with ZKP and Selective Disclosure

## Recording from the call: [20210203 ACA-Pug Meeting Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- Name (Organization) &lt;email&gt;
- Christos Patsonakis (CERTH) &lt;cpatsonakis@iti.gr&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;

## Announcements

- Primary branch of repo has been renamed to main – update your forks accordingly
- ACA-Py Release 0.6.0 coming soon (see below) – likely this week

## Deployments and Work Updates

- BC Gov Team
  
  - Aries-VCR/OrgBook BC Deployment - starting on an multi-tenant OrgBook Issuer
  - Issuer Kit - VCs for OIDC Issuer Service - [Safe Entry BC PoC](https://vonx.io/safeentry) - VCs for Physical Access Points
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work
    
    - DID Exchange Test Cases; deprecating 0160 Connections usage
    - Backchannel for Aries Framework Go
  - Breaking up the Indy SDK
    
    - indy-vdr
    - indy-shared-rs – contribution to Hyperledger
    - aries-askar - storage – contribution to Hyperledger
  - BBS+ support to achieve W3C Standard VCs with ZKP and Selective Disclosure

## Agenda

- Recent [issues](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20sort%3Aupdated-desc) - [help wanted](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20sort%3Aupdated-desc%20label%3A%22help%20wanted%22%20)
- Release 0.6.0 – It's BIG
  
  - Breaking Changes - [https://hackmd.io/pWCJ4fnoR\_aTPIoBiNBV\_g](https://hackmd.io/pWCJ4fnoR_aTPIoBiNBV_g)
    
    - Controllers: New API endpoints, tightened up revocation handling to RFC 441
    - Startup: Removal of auto-creating wallet in "start" mode and the handling of recreating a wallet in "provision" mode
    - Plugin Writers:
      
      - use of "Profile" vs. "RequestContext" and overall handling of contexts (no longer assume single context)
      - retrieving the "AdminRequestContext" as changed
      - "ProfileSession" needed to inject a the "BaseStorage" or "BaseWallet" interfaces and the "inject" method is no longer async
  - Additions since 0.5.6 (2020.10.19) – [120 merged PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20closed%3A%3E2020-10-19) ago.
    
    - Issue Credential V2 (RFC 0453) – Draft
    - Mediator – with docs
    - Multi-tenancy – with docs
    - OOB – complete, unit tests almost there
    - DID Exchange and common connection record
    - Flexible web hooks – with demo for multi-tenancy use case
    - Indy Best Practices for Proof Request/Proof (RFC 441)
    - Underlying changes to support Indy/Aries Shared Library deployments
    - Unit tests updates (still ~99% coverage)
    - Alice/Faber Demo updates to include all new features
  - Current work, but not included
    
    - Persistent Queue - [plan for completion of first cut](https://github.com/hyperledger/aries-cloudagent-python/issues/927)
    - Sign Transaction Protocol
    - Shared Components (branch exists, but won't be in main or 0.6.0)
- W3C Verifiable Credential project: [https://hackmd.io/@animo/acapy-bbs-2](https://hackmd.io/@animo/acapy-bbs-2)
- Repolinter - [Hyperledger requirement](https://github.com/hyperledger/aries-cloudagent-python/issues/935)
- Other Discussion
  
  - SICPA/Indicio DID Resolver - [Outline of plans](https://hackmd.io/@dbluhm/uniresolver-acapy), [feature/did-resolver branch](https://github.com/rd-dlab/aries-cloudagent-python/tree/feature/did-resolver), [GitHub project](https://github.com/rd-dlab/aries-cloudagent-python/projects/1)
- Indy DID Method meetings and links: [Indy DID Method Specification](https://lf-hyperledger.atlassian.net/wiki/spaces/indy/pages/19465516/Indy+DID+Method+Specification)

## Next Meeting

- Requests?

## Future Topics

- Documentation needs
- FAQ materials

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18490449/18514721.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
