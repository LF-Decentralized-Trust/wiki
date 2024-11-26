1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-01-24 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Jan 24, 2023

## Summary:

Topics:

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio
- Ledger Agnostic AnonCreds – when do we start using anoncreds-rs in ACA-Py and how?
- Experience with using ACA-Py plugins
- ACA-Py Documentation site
- Open Discussion

**Zoom Link**: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

**Call Time**: 8:00 Pacific / 17:00 Central Europe

## Recordings From the Call: [dummyfile.txt](#)

- Full Meeting:
- Topics:

```

```

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome, Introductions and Announcements

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;,Announcements
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

## Agenda

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio
  
  - Status: Refactor and review, and then on to testing - creating test cases. Wrap up next week.
  - Repo is: [https://github.com/Indicio-tech/acapy-wallet-upgrade](https://github.com/Indicio-tech/acapy-wallet-upgrade);  ACA-Py or external
  - Current branch: [https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support](https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support)
  - Question from [Kyle Robinson](https://lf-hyperledger.atlassian.net/wiki/people/60e73ed74134aa0069502ec1?ref=confluence) : How close is this conversion becoming like an export/import 
    
    - Response from [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) : There's definitely some similarities to export/import with the key difference that we're not doing a full dump/export followed by a full import. The migration script performs updates more or less in place so we don't have to worry about the size of the database being operated on
  - From [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) – AFJ issue: [https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support](https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support)
- Experiences with the use of Plugins in ACA-Py – the BC Gov Traction Team – [Jason Sherman](https://lf-hyperledger.atlassian.net/wiki/people/557058:0b5eb4a5-0d5d-4a7f-b2cc-b2d7597a7e8c?ref=confluence) 
  
  - Traction – enabling the use of multi-tenant ACA-Py for teams that want an agent within an organization
    
    - Ease of use in standing up a new interface
    - Simplifier API for issuers/verifiers
  - List of existing plugins: [https://hackmd.io/m2AZebwJRkm6sWgO64-5xQ](https://hackmd.io/m2AZebwJRkm6sWgO64-5xQ)
    
    - Action – add the Traction plugins to it
    - Action – add this as a document in the ACA-Py repo
  - [https://github.com/bcgov/traction](https://github.com/bcgov/traction)
  - [https://github.com/bcgov/traction/tree/develop/plugins](https://github.com/bcgov/traction/tree/develop/plugins)
    
    - Getting started – look at the basicmessage-storage plugin – store the basic message text
    - Need more docs on how to do it - basics plus best practices – see deployment comments below.
    - Use it for testing new capabilities before putting into core ACA-Py
    - Deployment – how do you get the plugin published, versioned and brought into images for deployment? No decisions yet?
      
      - Managing the command line parameters, and the use of yaml files for the plugins
    - Lots of logic is in ACA-Py's routes.py, which might need to be refactored – makes it harder.
    - Big win in keeping the maintenance down vs. external code. Much easier to manage.
- Ledger-Agnostic AnonCreds Interface is ACA-Py: progress
  
  - Status update
  - When should we replace indy-shared-rs with anoncreds-rs? [Issue #2044](https://github.com/hyperledger/aries-cloudagent-python/issues/2044)
- Adding a [Documentation site](https://github.com/hyperledger/aries-cloudagent-python/issues/1951) for ACA-Py - as nice as the AFJ one - [https://aries.js.org/](https://aries.js.org/)
  
  - PR: [2079](https://github.com/hyperledger/aries-cloudagent-python/pull/2079)
  - Features wanted:
    
    - a Version selector based on ACA-Py tags, so the entire site (navigation, search) is filtered to that version
      
      - Only for versions going forward – not for past versions.
    - multi-lingual support to allow for translations
  - Current PR will have the doc site within ACA-Py, but the need for multiple versions may cause us to use a separate repo for housing the generated documents.
- Question from [Pradeep Kumar Prakasam](https://lf-hyperledger.atlassian.net/wiki/people/5ffd0564dd5eb501080bf05c?ref=confluence) : About automated container scanning.
  
  - Hi. If there is time, I would like to know if Container vulnerability scanning is covered in the GitHub workflow. I can see SonarCloud Gate, but couldn't find any container scanning there. If anyone could give me more info where to look, it would be great, thanks.
    
    - Notably – would it be possible to add qualys or an equivalent for container scanning?
  - Wade Barnes created [Issue #2087](https://github.com/hyperledger/aries-cloudagent-python/issues/2087) for this, flagging [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850?ref=confluence) of Hyperledger to see what tools the Foundation has for this.

## Next Meeting

- Does anyone use/see a use case for Web Sockets and Return Route beyond ACA-Py as a mobile agent mediator?
- Issue [2029](https://github.com/hyperledger/aries-cloudagent-python/issues/2029): Additional security controls for webhooks for multi-tenancy

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18501358/18517426.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
