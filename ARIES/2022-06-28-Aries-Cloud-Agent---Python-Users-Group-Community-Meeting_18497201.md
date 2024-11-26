1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-06-28 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Jun 28, 2022

## Summary:

Topics:

- How to handle DIDComm v2 connections in ACA-Py
- Confirming: 0.7.4 – ready to go?
- ACA-Py 1.0.0 – Ready to set a milestone?
- Q&amp;A

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Extracted segments:
- Relevant Chat Bits:

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence) (Indicio) &lt;colton@indicio.tech&gt;
- [Dave McKay](https://lf-hyperledger.atlassian.net/wiki/people/712020:24d508a3-ccfc-476f-b3c7-6b2549b19a23?ref=confluence)
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (Fullboar Creative / BC Gov.) &lt;jason.leach@fullboar.ca&gt;
- [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence)  (Technische Universität Berlin) &lt;hakan.yildiz@tu-berlin.de&gt;
- [Patrick St-Louis](https://lf-hyperledger.atlassian.net/wiki/people/712020:252ecf1c-7d3b-4f2e-805d-1b747814236e?ref=confluence) (IDLab) &lt;patrick.st-louis@idlab.org&gt;

## Announcements

## Deployments and Work Updates

- BC Gov Team
  
  - [Aries Cloud Agent Python](https://github.com/hyperledger/aries-cloudagent-python)
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)
  - [Aries-VCR](https://github.com/bcgov/aries-vcr)/OrgBook BC Deployment
  - [Issuer Kit](https://github.com/bcgov/issuer-kit) - VCs for OIDC Issuer Service
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: [https://aries-interop.info](https://aries-interop.info)
  - [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness)
  - BC Wallet – based on [Aries Framework JavaScript](https://github.com/hyperledger/aries-framework-javascript) and [Aries Bifold](https://github.com/hyperledger/aries-mobile-agent-react-native)
  - [Aries Endorser Service](https://github.com/bcgov/aries-endorser-service)
  - [Traction](https://github.com/bcgov/traction)

## Agenda

- Adding DIDComm 2.0 Connections to ACA-Py.
  
  - An update from [Hakan Yildiz](https://lf-hyperledger.atlassian.net/wiki/people/5eccf9bc7d0c250c2356b63d?ref=confluence) and his team from the discussion on [2022-04-19](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2022-04-19+Aries+Cloud+Agent+-+Python+Users+Group+Community+Meeting) about adding DIDComm V2 to ACA-Py
    
    - We will come with 3 options (and diagrams) to find a consensus. → [![](plugins/servlet/confluence/placeholder/unknown-macro)](https://docs.google.com/document/d/1piGZ-0FW9DWEFRetviV1Vjxv7DDkIFQDWUs38VGqZ-Y/edit)
- Confirming: 0.7.4 – ready to go?
  
  - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)
- ACA-Py 1.0.0 – ready to set a milestone? [Presentation](https://docs.google.com/presentation/d/1j_E9JPWjY-Yzppc92WgGajpgZLq3k5uDSItLCk8-sEs/edit?usp=sharing)
  
  - Documentation
  - Full AIP 2.0 support. What's missing: [https://github.com/hyperledger/aries-cloudagent-python/blob/main/SupportedRFCs.md#aip-20](https://github.com/hyperledger/aries-cloudagent-python/blob/main/SupportedRFCs.md#aip-20)
  - Smooth deployment, including persistent queues
  - Shared components (Askar et al.)
  - Other things that are needed:
    
    - did:indy support – handling did:indy resolution.
    - Plugin for universal resolver support.
    - DIDComm v2.0 support
    - Aggressive problem reporting (per discussion last week)
      
      - e.g. [Issue 1798 - store credential](https://github.com/hyperledger/aries-cloudagent-python/issues/1798); [Issue 1782](https://github.com/hyperledger/aries-cloudagent-python/issues/1782); even [issue 1730 - problem report for a non-protocol](https://github.com/hyperledger/aries-cloudagent-python/issues/1730)
    - More?
      
      - Python 3.7+ and associated updates?

## Next Meeting

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18497201/18516401.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
