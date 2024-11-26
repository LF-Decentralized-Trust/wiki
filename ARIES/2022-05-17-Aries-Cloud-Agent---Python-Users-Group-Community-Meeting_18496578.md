1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-05-17 Aries Cloud Agent - Python Users Group Community Meeting

Created by Ian Costanzo, last modified on May 17, 2022

## Summary:

Planned Topics:

- Getting to release 0.7.4
- Discuss outstanding PRs
- Persistent Queues
- Q&amp;A

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Extracted segments:
- Chat: 
  
  - Me to Everyone (8:04 AM)
    
    [https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2022-05-17+Aries+Cloud+Agent+-+Python+Users+Group+Community+Meeting](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2022-05-17+Aries+Cloud+Agent+-+Python+Users+Group+Community+Meeting)
    
    Daniel Bluhm to Everyone (8:07 AM)
    
    We'll be testing out rc2 in the various repos Indicio participates in ASAP
    
    Matteo Marangoni to Everyone (8:27 AM)
    
    [https://github.com/sicpa-dlab/aries-acapy-plugin-kafka-events](https://github.com/sicpa-dlab/aries-acapy-plugin-kafka-events)
    
    Kim Ebert to Everyone (8:43 AM)
    
    We are creating a PR around the document loader to fix some interaction problems that we've had with redis and asyncio. [https://github.com/hyperledger/aries-cloudagent-python/compare/main...Indicio-tech:fix/document-loader-thread](https://github.com/hyperledger/aries-cloudagent-python/compare/main...Indicio-tech:fix/document-loader-thread)
    
    Thomas Diesler to Everyone (8:51 AM)
    
    How about a notion of plugin profiles? In that way you could have a profile for V1 protocols and another for V2. Custom profiles could streamline the process for specific customers.
    
    Thomas Diesler to Everyone (9:00 AM)
    
    Is there a tentative ETA for 0.7.4?
    
    Lovely, thanks
    
    Bruno Hivert to Everyone (9:01 AM)
    
    Thanks !

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) (Anon Solutions Inc.) &lt;IanCostanzo@gmail.com&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Bruno Hivert](https://lf-hyperledger.atlassian.net/wiki/people/712020:0ef3e380-8e1e-45be-82e1-708b65f236da?ref=confluence)([https://idlab.org)](https://idlab.org%29) &lt;bruno.hivert@idlab.org&gt;

## Announcements

## Deployments and Work Updates

- BC Gov Team
  
  - [Aries Cloud Agent Python](https://github.com/hyperledger/aries-cloudagent-python)
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)
  - [Aries-VCR](https://github.com/bcgov/aries-vcr)/OrgBook BC Deployment
  - [Issuer Kit](https://github.com/bcgov/issuer-kit) - VCs for OIDC Issuer Service
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: [https://aries-interop.info](https://aries-interop.info)
  - [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness)
  - BC Wallet – based on Aries Framework JavaScript and Aries Bifold
  - [Aries Endorser Service](https://github.com/bcgov/aries-endorser-service)
  - [Traction](https://github.com/bcgov/traction)
  - BPA - Business Partner Agent for B2B use of VCs

## Agenda

- Getting to release 0.7.4 – what is needed after RC2
  
  - [PRs since Release 0.7.4-RC2](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-05-11) - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)
- outstanding PR discussion
  
  - [https://github.com/hyperledger/aries-cloudagent-python/pull/1734](https://github.com/hyperledger/aries-cloudagent-python/pull/1734) - add a parameter to the revocation API to specify the notification version (required parameter), allows support for both V1 and V2 protocols, and eventually should use
  - and [https://github.com/hyperledger/aries-cloudagent-python/pull/1737](https://github.com/hyperledger/aries-cloudagent-python/pull/1737) - PR can be accepted as is; not necessary for revocation notification (see above comment)
  - Kim Ebert will be introducing a PR to fix an issue with async (see link in chat)
  - Include PR 1710 in 0.7.4 (connectionless) - "breaking change", but only breaks if you start to use the connectionless feature
- persistent queues/plug-ins ([Shaanjot Gill](https://lf-hyperledger.atlassian.net/wiki/people/712020:ef425cae-d196-44a6-b7e8-c21e4470d0d3?ref=confluence) and SICPA [Victor Martinez](https://lf-hyperledger.atlassian.net/wiki/people/557058:73fff461-39df-4cc9-85d1-7b8a65773bee?ref=confluence) )
  
  - See [https://github.com/bcgov/aries-acapy-plugin-redis-events](https://github.com/bcgov/aries-acapy-plugin-redis-events)
  - and [https://github.com/sicpa-dlab/aries-acapy-plugin-kafka-events](https://github.com/sicpa-dlab/aries-acapy-plugin-kafka-events)
- questions
  
  - There was some discussion around support for plug-in profiles (support for standard aca-py configurations)

## Next Meeting

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18496578/18516292.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
