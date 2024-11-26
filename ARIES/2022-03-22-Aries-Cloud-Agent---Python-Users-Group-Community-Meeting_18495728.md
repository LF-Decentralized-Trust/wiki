1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-03-22 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Mar 22, 2022

## Summary:

Planned Topics:

- Getting to release 0.7.4 – key release notes and breaking changes?
  
  - Persistent Queues update – design change to make PQs an external plugin
- Multi-tenancy security and questions raised in issue 1632: --multitenant-admin security questions
- Endorser for multi-tenant agents
- Including seed in the Admin Interface
- Clarification on did-exchange implicit request pthid (PR 1599)

## Recording from the call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Announcements

## Deployments and Work Updates

- BC Gov Team
  
  - Aries Cloud Agent Python
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)
  - Aries-VCR/OrgBook BC Deployment
  - Issuer Kit - VCs for OIDC Issuer Service
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: [https://aries-interop.info](https://aries-interop.info)
  - [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness)
  - BPA - Business Partner Agent for B2B use of VCs
  - BC Wallet – based on Aries Framework JavaScript and Aries Bifold

## Agenda

- Update on Release 0.7.4
  
  - [PRs since Release 0.7.3](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-01-10) - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)
- Update: Adding persistent queues in ACA-Py – [Shaanjot Gill](https://lf-hyperledger.atlassian.net/wiki/people/712020:ef425cae-d196-44a6-b7e8-c21e4470d0d3?ref=confluence)
  
  - New design outlined – plugin; implementation status updated
- Multi-tenancy security and questions raised in issue [1632](https://github.com/hyperledger/aries-cloudagent-python/issues/1632): --multitenant-admin security questions 
  
  - Resolution: Approach decided; new Issue to open as "Help Wanted"; Not crucial for 0.7.4
- Endorser for multi-tenant agents – issue [1657](https://github.com/hyperledger/aries-cloudagent-python/issues/1657)
  
  - Resolution: Recommendation is to use a separate endorser instance
  - Future: create an aries-endorser-service repo
- Including the seed as a parameter in the Admin interface – issue [1640](https://github.com/hyperledger/aries-cloudagent-python/issues/1640)
  
  - Resolution: Could be added with a "--do-you-really-want-to-do-this" option to enable it. "Help Wanted" issue to be added.
- To merge or not to merge, that is the question: [1620 - Updates to Connection State](https://github.com/hyperledger/aries-cloudagent-python/pull/1620)
  
  - Summary from [Philipp.Etschel](https://lf-hyperledger.atlassian.net/wiki/people/5e3d597ae367ae0c91afb39f?ref=confluence):  I think this task started as a fix for a minor inconsistency between documentation, connection record and connection event and then mutated into a whole discussion about the deprecation of the connection protocol. So I would propose to either just fix the inconsistency, or wait until there is a decision on how to proceed. Basically there are three open questions.
    
    - 1\. how to handle the connection states
    - 2\. how to handle the deprecation
    - 3\. how to migrate stored data.
  - Resolution: Need more input from implementers – [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)(at least) to take a look)
- Clarification on did-exchange implicit request pthid ([PR 1599](https://github.com/hyperledger/aries-cloudagent-python/pull/1599))
  
  - To be discussed on the Aries WG Meeting tomorrow.

## Next Meeting

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18495728/18516058.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
