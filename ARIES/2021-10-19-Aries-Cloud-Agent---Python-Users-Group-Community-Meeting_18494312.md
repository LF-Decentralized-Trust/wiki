1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2021](ACA-Pug-Meetings-Archive-2021_18514526.html)

# Hyperledger Aries : 2021-10-19 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Ian Costanzo on Oct 19, 2021

## Summary:

Planned Topics:

- Review of PRs for 0.7.2 Final -- anything to be added?
- Creating Aries Mediator Service repo (aries-mediator-service) - dependent on ACA-Py?
- Creating Indy Endorser Server repo (indy-endorser-service)
- ACA-Py support for Indy Multi-Ledger
- AMA (as time permits)

## Recording from the call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- Ian Costanzo (BC Gov/contractor) &lt;iancostanzo@gmail.com&gt;
- [Dave McKay](https://lf-hyperledger.atlassian.net/wiki/people/712020:24d508a3-ccfc-476f-b3c7-6b2549b19a23?ref=confluence) [dave@nothernblock.io](mailto:dave@nothernblock.io)
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) &lt;[james.ebert@indicio.tech](mailto:james.ebert@indicio.tech)&gt;an
- Bruno Hivert ([https://idlab.org)](https://idlab.org%29) [bruno.hivert@idlab.org](mailto:bruno.hivert@idlab.org)
- Burak Can Kus (DataGateway Japan) &lt;[burak.can.kus@datagateway.co.jp](mailto:burak.can.kus@datagateway.co.jp)&gt;
- Tõnu Samuel (NSA)
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) (Animo Solutions) &lt;timo@animo.id&gt;

## Announcements

## Deployments and Work Updates

- BC Gov Team
  
  - Aries-VCR/OrgBook BC Deployment
    
    - In progress: a multi-tenant OrgBook Issuer
  - Issuer Kit - VCs for OIDC Issuer Service
  - Verification Tutorial – multi-purpose verifier aimed at the general population receiving their first verifiable credential
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: https://aries-interop.info
  - BPA - Business Partner Agent for B2B use of VCs
  - AIP 2.0
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)

## Agenda

- Ready to tag 0.7.2?
  
  - [PRs merged since 0.7.2RC0](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aclosed%20is%3Amerged%20updated%3A%3E%3D2021-10-05)
  - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) – which are needed before 0.7.2? Perhaps [1446](https://github.com/hyperledger/aries-cloudagent-python/pull/1446), [1433](https://github.com/hyperledger/aries-cloudagent-python/pull/1433), [1430](https://github.com/hyperledger/aries-cloudagent-python/pull/1430)
- Discussion and plan: Creating a new "aries-mediator-service" repo [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence)
  
  - Background: Proposal on Aries channel: [https://chat.hyperledger.org/channel/aries?msg=AoJWWBfs6z3KYyzK3](https://chat.hyperledger.org/channel/aries?msg=AoJWWBfs6z3KYyzK3)
  - Follow up – best plan seems to be to use ACA-Py as a dependency, as is done here: [https://github.com/Indicio-tech/infra-mediator](https://github.com/Indicio-tech/infra-mediator)
  - What needs to be done in ACA-Py to make this work. Hint: persistent queues.
- Discussion and plan: Creating a new "indy-endorser-service" repo - [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence)
  
  - Background – same as above, but for Indy transaction endorsing
- Status of ACA-Py Indy Multi-ledger support - [Shaanjot Gill](https://lf-hyperledger.atlassian.net/wiki/people/712020:ef425cae-d196-44a6-b7e8-c21e4470d0d3?ref=confluence)
- Questions – AMA

## Next Meeting

## Future Topics

- Double Signature with eIDAS?
  
  - Background: [https://www.slideshare.net/FIDOAlliance/introduction-to-fido-and-eidas-services](https://www.slideshare.net/FIDOAlliance/introduction-to-fido-and-eidas-services)
  - SICPA - For the eSSIF program, with json-ld credential we are adding double signature, the normal + eIDAS
    
    - [Mateo](https://lf-hyperledger.atlassian.net/wiki/people/557058:46dd489d-ef95-4225-b625-9e0bf11b4704?ref=confluence)
  - Double signature in ACA-Py with pluggable mechanism, and implementation for eIDAS
- Performance with Shared Components enabled (Aries Askar et al.)

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18494312/18515627.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18494312/18515615.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
