1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings 2023](ACA-Pug-Meetings-2023_18517279.html)

# Hyperledger Aries : 2023-02-07 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Feb 07, 2023

## Summary:

Topics:

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio
- Mediator problem with messages not resent – [Issue #2111](https://github.com/hyperledger/aries-cloudagent-python/issues/2111)
- Presentation Request Revocation Intervals – lessons learned in writing the AnonCreds Specification
- ACA-Py Documentation site – the plan.
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
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io) &lt;warren@affinitiquest.io&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) (Petri Dish Development) &lt;amanji@petridish.dev&gt;
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (Fullboar Creative / Government of BC) &lt;jason.leach@fullboar.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (Quartech / Government of BC) &lt;emiliano.sune@quartech.com&gt;
- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio PBC) &lt;char@indicio.tech&gt;

## Agenda

- Update on BC Gov Code With Us – ACA-Py Indy-SDK to Askar conversion script - Indicio
  
  - Status: Just about wrapped up! [Repo transfer requested](https://github.com/hyperledger/governance/issues/70) (should we have Andrew transfer from the original fork?)
    
    - Packaging: Container image (published to HL org GHCR), PyPI package
  - Demo by [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence)
  - Repo is: [https://github.com/Indicio-tech/acapy-wallet-upgrade](https://github.com/Indicio-tech/acapy-wallet-upgrade)
  - Current branch: main
  - From [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) – AFJ issue: [https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support](https://github.com/Indicio-tech/acapy-wallet-upgrade/tree/feature/psql-support)
- Update on ACA-Py Container Scanning (brought up last meeting)
  
  - There are scanner options in Hyperledger, but not chosen.
    
    - Snyk is a possibility, Qualys was also used and both produced the same results.
  - Based on the testing, the base images were updated to bullseye, which contains no current critical vulnerability.
  - Would like to have multi-architecture release.
- Messages getting stuck when a connection is being established.
  
  - Message sent to the mediator, received, but connection not setup and message getting stuck.
  - Race condition.
  - Workaround in Bifold, but fix should be in the mediators – hence in ACA-Py/AFJ mediators.
  - On making a connection, the mediator routing and the connection are done in parallel, vs. serial.
  - Issues in ACA-Py and AFJ submitted – each need to be investigated.
  - Indicio to do more investigation
- Adding a [Documentation site](https://github.com/hyperledger/aries-cloudagent-python/issues/1951) for ACA-Py - as nice as the AFJ one - [https://aries.js.org/](https://aries.js.org/)
  
  - PR: [2079](https://github.com/hyperledger/aries-cloudagent-python/pull/2079) – tricky part is the multiple version support.
  - Proposed approach:
    
    - Use docusaurus
    - Static site generated from new repo – [https://github.com/hyperledger/aries-acapy-docs](https://github.com/hyperledger/aries-acapy-docs)
    - Landing page in new repo, version specific documentation in folders.
    - GHA manually added for each supported ACA-Py release – automate this in future via a PR created with ACA-Py tag released.
      
      - Fetch tagged branch from ACA-Py into temp folder
      - Generate a root document if not present (used to support tags created in the past) – else, use one in ACA-Py.
      - Generate the required RST documents for the ACA-Py internal documentation currently used by Read The Docs (using Python doc strings).
      - (Re-)Generate static pages for the tag into correct folder in the `docs` repo.
    - For now, periodically run the GHA for the "main" branch manually – automate this in the future to run either nightly or when an ACA-Py PR is merged.
    - Publish to "acapy.org" domain.
- Next Release?
  
  - 0.7.6 or 0.8.0 (depending on breaking changes)
  - Not a cherry-picked release – everything in main branch
  - Issues include fixing/adding revocation notification issues
- Issue [2029](https://github.com/hyperledger/aries-cloudagent-python/issues/2029): Additional security controls for webhooks for multi-tenancy
  
  - Added as a PR and then closed, to be refactored as a plugin
  - Enables key updates via an admin interface call.
- Open Discussion:
  
  - Does anyone use/see a use case for Web Sockets and Return Route beyond ACA-Py as a mobile agent mediator?

## Next Meeting

- Does anyone use/see a use case for Web Sockets and Return Route beyond ACA-Py as a mobile agent mediator?
- Understanding Presentation Request Revocation Intervals
  
  - [Presentation Slides](https://docs.google.com/presentation/d/1Y6ato1crftEMwAry2FtreAifW2Aj5mzjcw4xrb0uj2E/edit?usp=sharing)
  - Issue Created
- Status of vc-authn-oidc repository – v2.0 branch.

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18501889/18517518.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
