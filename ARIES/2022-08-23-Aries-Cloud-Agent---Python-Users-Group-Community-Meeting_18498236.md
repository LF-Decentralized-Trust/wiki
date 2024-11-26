1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-08-23 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Aug 23, 2022

## Summary:

Topics:

- Recent Merges / v1.0.0-rc0 Breaking/Not-Breaking
- Upcoming Process: Roadmap Creation
- Aries Interop-a-athon
- Q&amp;A

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Extracted segments:
- Relevant Chat Bits: 
  
  - 08:24:38 From Daniel Bluhm : As an aside, SICPA is still planning to donate the Kafka Queue plugin to HL. Just been stalled a bit with holidays and competing priorities :)
  - 08:25:45 From Kim Ebert : [https://github.com/Indicio-tech/aries-acapy-cache-redis](https://github.com/Indicio-tech/aries-acapy-cache-redis) Colton did most of the work here.
  - 08:26:14 From Paul Wenzel : I am also very curious to run load tests with the Redis caches. Just let me know how to configure AcaPy once it is ready
  - 08:31:21 From Daniel Bluhm : In fairness, even while being really sensitive, I have found the analysis from sonarcloud helpful :)
  - 08:34:59 From Colton Wolkins : Maybe if it didn't include merges, I'd see the same thing. I'm surprised that it doesn't exclude the merges from main like the GitHub merge view does. Looks like I'll have to learn how to properly do rebases and figure out how to handle rebase conflicts (with GPG signing each commit)

```

```

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (InfinitiQuest.io) &lt;warren@affinitiquest.io&gt;
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
  - BC Wallet – based on [Aries Framework JavaScript](https://github.com/hyperledger/aries-framework-javascript) and [Aries Bifold](https://github.com/hyperledger/aries-mobile-agent-react-native)
  - [Aries Endorser Service](https://github.com/bcgov/aries-endorser-service)
  - [Traction](https://github.com/bcgov/traction)

## Agenda

- Updates on merges and current PRs – priorities
  
  - Merges [Since 0.7.4](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-06-30)
  - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)
  - Status of reaching full AIP 2.0
- SonarCloud activation:
  
  - Doing an "Update from Main" vs. a rebase causes extra files to be referenced in the PR, and adds to the code scanned by SonarCloud – suggestion is to use rebase.
  - Please pay attention to the feedback, but we will not gate PR merges on SonarCloud feedback – at least not yet.
  - Please add comments to your PR about why you are not addressing SonarCloud feedback so that we can understand how it is being used, and if we configure it better for the repository.
- Upcoming Process: Creating an AnonCreds Roadmap
- ACA-Py Aries Interop-a-thon Planning
  
  - Planned rooms:
    
    - [Bruno Hivert](https://lf-hyperledger.atlassian.net/wiki/people/712020:0ef3e380-8e1e-45be-82e1-708b65f236da?ref=confluence)  idLabs – using AATH with mobile agents
    - [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) BC Gov – using AATH between framework agents — running, debug, fixing tests, adding tests
    - [Sheldon Regular](https://lf-hyperledger.atlassian.net/wiki/people/557058:03ca5fa1-a9b1-4962-8ade-a10467940771?ref=confluence) BC Gov – using the Aries Mobile Test Harness for automated testing of mobile agents

## Next Meeting

## Future Topics

- Proposal for topic (Indicio): Pickup Protocol Plugin + Persistence of mediated messages
  
  - [https://github.com/indicio-tech/acapy-plugin-pickup](https://github.com/indicio-tech/acapy-plugin-pickup)
  - Persistence Feature Branch: [https://github.com/indicio-tech/acapy-plugin-pickup/tree/feature/persistence](https://github.com/indicio-tech/acapy-plugin-pickup/tree/feature/persistence)

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18498236/18516663.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
