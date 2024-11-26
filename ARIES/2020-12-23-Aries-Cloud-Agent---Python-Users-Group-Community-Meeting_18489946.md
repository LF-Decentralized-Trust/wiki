1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2020](ACA-Pug-Meetings-Archive-2020_18513017.html)

# Hyperledger Aries : 2020-12-23 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Christos Patsonakis on Jan 06, 2021

## Summary:

Planned Topics:

- Recent Merges – Mediator, Multi-Tenancy, DID Exchange, Shared Components
- ACA-Py Integration Testing
- ACA-Py Custodial Wallets Use Case

## Recording from the call: [2020-12-23 ACA-Pug Community Meeting Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- Name (Organization) &lt;email&gt;
- Stephen Curran (Cloud Compass Computing Inc./BC Gov) &lt;swcurran@cloudcompass.ca&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio) &lt;daniel@indicio.tech&gt;
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;
- Christos Patsonakis (CERTH) &lt;cpatsonakis@iti.gr&gt;

## Announcements

- BBS+ [Code With Us](https://digital.gov.bc.ca/marketplace/opportunities/code-with-us/3f9f0e86-b8bf-47ee-9f3d-5b272f9ec845)
- ACA-Py Release 0.6.0 coming soon
  
  - Breaking changes
    
    - DID Exchange support with common connection records
    - Support for Aries shared component

## Deployments and Work Updates

- BC Gov Team
  
  - Aries-VCR/OrgBook BC Deployment - will be starting on an OrgBook Issuer
  - Issuer Kit - VCs for OIDC Issuer Service - [Safe Entry BC PoC](https://vonx.io/safeentry) - VCs for Physical Access Points
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work
    
    - GitHub Actions - now running daily for ACA-Py and .Net
    - Results visualization tool – Allure to see the results/click-through
  - Breaking up the Indy SDK
    
    - indy-vdr progress - now embedded in von-network and tails server
    - indy-shared-rs
    - aries-askar - storage
  - BBS+ to achieve W3C Standard VCs with ZKP and Selective Disclosure

## Agenda

- Recent [issues](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20sort%3Aupdated-desc) - [help wanted](https://github.com/hyperledger/aries-cloudagent-python/issues?q=is%3Aissue%20is%3Aopen%20sort%3Aupdated-desc%20label%3A%22help%20wanted%22%20)
- Recently [merged PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aclosed%20sort%3Aupdated-desc) and Status updates:
  
  - Multitenancy - [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) [Victor Martinez](https://lf-hyperledger.atlassian.net/wiki/people/557058:73fff461-39df-4cc9-85d1-7b8a65773bee?ref=confluence) 
    
    - Ready and working with relay functionality - code routes the message to the relevant wallet, Alice/Faber Demo – see code for examples
      
      - Managed wallets – base wallet handles the keys of the sub-wallets
      - In progress: Unmanaged wallets – keys are elsewhere – e.g. in a custodial use case - thin wallet
    - Next: test, **docs**, demos and integrating with mediator support
  - Mediator - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)  [Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence)
    
    - Coordinate mediation work
    - Integrated that with connections – enabled construction of the peer DID to use the mediator
    - In progress – Admin API for using the mediator/managing
    - Next: Docs, demos, DID Exchange support
- ACA-Py AMA with the core maintainers
  
  - Custodial Wallets Use Case
    
    - Attack surfaces and GDPR compliance
    - Separation of keys and wallet/data
      
      - Unmanaged wallets are the multi-tenancy approach
      - Example – Biometric on the user side, keys on cloud HSM, separate from the wallets - need to figure out how/when to bring the data/keys together
        
        - Goal - pluggable method to get the key to the wallet.
- Integration Testing - Timo
  
  - Unit tests are there, but that's not enough.  Though we have 99% coverage.
  - Idea is to add a Behave framework to ACA-Py to enable integration tests for feature (vs. interop testing).
    
    - Need to be conscious of Aries Agent Test Harness
- Current active work:
  
  - Web hooks re-organization
  - Persistent queues
  - Indy / Aries Shared components
- Other Discussion

## Next Meeting

- ACA-Py Roadmap – what's next?

## Future Topics

- Documentation needs
- FAQ materials

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18489946/18514521.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
