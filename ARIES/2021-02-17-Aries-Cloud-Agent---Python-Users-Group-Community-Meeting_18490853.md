1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2021](ACA-Pug-Meetings-Archive-2021_18514526.html)

# Hyperledger Aries : 2021-02-17 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Feb 18, 2021

## Summary:

Planned Topics:

- Status of Persistent Queues Work
- Status of Signed Transactions / Endorser Protocol
- Update on W3C Standard Verifiable Credentials with ZKP and Selective Disclosure in ACA-Py
- Release Status

## Recording from the call: [20210217 ACA-Pug Community Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- Name (Organization) &lt;email&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- Christos Patsonakis (CERTH) &lt;cpatsonakis@iti.gr&gt;

## Announcements

- [ACA-Py 0.6.0-RC0 tagged](https://github.com/hyperledger/aries-cloudagent-python/releases/tag/0.6.0-rc0) and [image](https://hub.docker.com/r/bcgovimages/aries-cloudagent/tags?page=1&ordering=last_updated) created
- Hyperledger Aries exiting Incubation

## Deployments and Work Updates

- BC Gov Team
  
  - Aries-VCR/OrgBook BC Deployment - starting on an multi-tenant OrgBook Issuer
  - Issuer Kit - VCs for OIDC Issuer Service - [Safe Entry BC PoC](https://vonx.io/safeentry) - VCs for Physical Access Points
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work
    
    - DID Exchange Test Cases; deprecating 0160 Connections usage
    - Backchannel for Aries Framework Go
    - Reporting pages - status and link to daily run Allure reports
  - Breaking up the Indy SDK
    
    - [indy-vdr](https://github.com/hyperledger/indy-vdr)
    - [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) – contribution to Hyperledger
    - [aries-askar](https://github.com/hyperledger/aries-askar) - storage – contribution to Hyperledger
  - BBS+ support to achieve W3C Standard VCs with ZKP and Selective Disclosure

## Agenda

- Recent [issues](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20sort%3Aupdated-desc) - [help wanted](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20sort%3Aupdated-desc%20label%3A%22help%20wanted%22%20)
- Persistent Queues status update[Christopher Adams](https://lf-hyperledger.atlassian.net/wiki/people/70121:3d516a61-192d-4596-9e38-36cb1750f39e?ref=confluence)
- Signed Transactions status update [harsh.multani@ayanworks.com](mailto:harsh.multani@ayanworks.com) (AyanWorks)
- Update on W3C Verifiable Credential project: [https://hackmd.io/@animo/acapy-bbs-2](https://hackmd.io/@animo/acapy-bbs-2) [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence)
- Other topics:
  
  - Repolinter - [Hyperledger requirement](https://github.com/hyperledger/aries-cloudagent-python/issues/935) - run once and corrections made; need to make it a standard check
  - SICPA/Indicio DID Resolver - [Outline of plans](https://hackmd.io/@dbluhm/uniresolver-acapy), [feature/did-resolver branch](https://github.com/rd-dlab/aries-cloudagent-python/tree/feature/did-resolver), [GitHub project](https://github.com/rd-dlab/aries-cloudagent-python/projects/1)
  - Indy DID Method meetings and links: [Indy DID Method Specification](https://lf-hyperledger.atlassian.net/wiki/spaces/indy/pages/19465516/Indy+DID+Method+Specification)

## Next Meeting

- Requests?

## Future Topics

- Documentation needs
- FAQ materials

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18490853/18514825.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
