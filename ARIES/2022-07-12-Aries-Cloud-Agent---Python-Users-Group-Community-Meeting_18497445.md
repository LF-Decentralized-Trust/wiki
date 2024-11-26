1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-07-12 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Patrick St-Louis on Jul 12, 2022

## Summary:

Topics:

- Upgrade the ACA-Py Python version – to what?
- BC Gov Activities planned
- Q&amp;A

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Extracted segments:
- Relevant Chat Bits:
  
  - From Warren Gallagher : Are there engineering guides for things like: storage/memory/cpu requirements for queues, caches, wallets
  - From Paul Wenzel : [https://github.com/bcgov/orgbook-configurations/tree/main/openshift/templates/agent](https://github.com/bcgov/orgbook-configurations/tree/main/openshift/templates/agent)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Philippe Bourque](https://lf-hyperledger.atlassian.net/wiki/people/712020:df573415-d7da-46a3-8bcb-fa7614ee7407?ref=confluence) (Ministère de la cybersécurité et du numérique | Gouvernement du Québec) &lt;[Philippe.Bourque@mcn.gouv.qc.ca](mailto:Philippe.Bourque@mcn.gouv.qc.ca)&gt;
- [Stéphane Harnois](https://lf-hyperledger.atlassian.net/wiki/people/62546dd59e7380006fb21f9b?ref=confluence)  (Ministère de la cybersécurité et du numérique | Gouvernement du Québec) &lt;stephane.harnois@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest.io) &lt;warren@affinitiquest.io&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;
- [Sylvain Martel](https://lf-hyperledger.atlassian.net/wiki/people/712020:9eb55fb2-a220-4945-916a-6da7d1ed6101?ref=confluence) (Gouvernement du Québec) &lt;sylvain.martel10@mcn.gouv.qc.ca&gt;
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

- Upgrading the version of Python used by ACA-Py
  
  - 3.6 is end of life'd, so this is a high priority
  - 3.7 PR, but 3.7 is less than a year from end of life
  - Other [versions lifespans](https://endoflife.date/python)
  - Why not use 3.10?
  - Discussion:
    
    - On 3.7 branch, all tests are passing, but with lots of deprecation warnings
    - 3.6 to 3.7 is likely the biggest breaking change (vs. going to 3.8, 3.9, etc.)
    - 3.11 evidently has a significant performance improvement (e.g. 25%), so being ready is important
    - Suggested approach:
      
      - 3.7 branch for now
      - Add GHAs to run all tests on all Python versions 3.7 - 3.10.
        
        - Run one version on PRs (same as today)
        - Run other versions daily on a cron
      - Add tag-based publishing of artifacts, and publish to the Hyperledger GitHub Container Repository
    - [Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence)and team to produce a HackMD doc about the plans to promote comment and community collaboration
    - Vulnerabilities associated with OS being used for the current BC Gov Images was raised – to be reviewed and possibly updated
      
      - But we really want to go to tag-based publishing per note above.
- An overview of BC Gov's priorities/focus – [presentation](https://docs.google.com/presentation/d/1Ru6qkGxv0uL3hqoJQUrRFV7EjVx1jqATXpUthEdxqYU/edit?usp=sharing)
  
  - Revocation updates – so close...
  - Completing/documenting/testing persistent queues and shared cache
    
    - Possible alternative solution to the shared cache – look at the current connection handling, where caching is being used and persist the data
  - Additional Aries Askar support for migration and shared component updates
    
    - Request about whether contributions to improve performance in high volume use cases (e.g. 400k wallets) would be generally useful
      
      - Assuming the low volume cases would not be massively impacted – yes, that would be helpful
  - [AIP 2.0 updates](https://github.com/hyperledger/aries-cloudagent-python/blob/main/SupportedRFCs.md#aip-20), especially focused on DID Exchange – did:peer and did:key – with a goal of alignment with [Aries Framework JavaScript](https://github.com/hyperledger/aries-framework-javascript) (as demonstrated by [AATH](https://aries-interop.info)).
  - OCA support as needed.
  - Aries Endorser Service.

## Next Meeting

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18497445/18516475.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
