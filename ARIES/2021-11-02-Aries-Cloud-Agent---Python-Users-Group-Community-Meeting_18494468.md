1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2021](ACA-Pug-Meetings-Archive-2021_18514526.html)

# Hyperledger Aries : 2021-11-02 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Nov 02, 2021

## Summary:

Planned Topics:

- Review of PRs for 0.7.2 Final -- anything to be added?
- Review of AIP 2.0 – what's missing?
- Ontario's Proxy Controller design
- AMA (as time permits)

## Recording from the call: [dummyfile.txt](#)

## Chat from the call: [20211102 ACA-Pug Community Call Chat.txt](attachments/18494468/18515663.txt)

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
  
  - Aries-VCR/OrgBook BC Deployment
    
    - In progress: a multi-tenant OrgBook Issuer
  - Issuer Kit - VCs for OIDC Issuer Service
  - Verification Tutorial – multi-purpose verifier aimed at the general population receiving their first verifiable credential
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: https://aries-interop.info
  - BPA - Business Partner Agent for B2B use of VCs
  - AIP 2.0
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)
  - Wallet – based on Aries Framework JavaScript and Aries Bifold

## Agenda

- Ready to tag 0.7.2?
  
  - [PRs merged since 0.7.2RC0](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Aclosed%20is%3Amerged%20updated%3A%3E%3D2021-10-05)
    
    - New: DIDComm V2 envelope support via Askar (AIP 2.0)
    - Startup/shutdown handling
    - Endorser updates
    - Fix: credential Admin API updates for Askar mode
    - Bug fixes
  - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls) – which are needed before 0.7.2?
    
    - Yes: 1430 – W3C Fixes for selective disclosure
    - Yes: Endorser auto-connect and 3 fixes.
    - Maybe: Multiple Indy Ledger?
    - Maybe: AIP-2 base64url consistency?
  - To Do: Read The Docs update.
- AIP 2.0 – What's Missing?
  
  - [ACA-Py Feature Overview](https://hackmd.io/OJ2oqI8-SY2MyhjOHg7pNA) – joint effort by Animo Solutions and Northern Block
  - To be implemented:
    
    - [Revocation Notification](https://github.com/hyperledger/aries-rfcs/tree/b3a3942ef052039e73cd23d847f42947f8287da2/features/0183-revocation-notification) – [PR](https://github.com/hyperledger/aries-cloudagent-python/pull/1464) from [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)
      
      - See discussion on the PR
    - [Discover Feature 2.0](https://github.com/hyperledger/aries-rfcs/tree/b3a3942ef052039e73cd23d847f42947f8287da2/features/0557-discover-features-v2) – [Issue](https://github.com/hyperledger/aries-cloudagent-python/issues/1466) assigned to [Shaanjot Gill](https://lf-hyperledger.atlassian.net/wiki/people/712020:ef425cae-d196-44a6-b7e8-c21e4470d0d3?ref=confluence)
      
      - Is there sufficient support for [Goal Codes](https://github.com/hyperledger/aries-rfcs/tree/b3a3942ef052039e73cd23d847f42947f8287da2/concepts/0519-goal-codes)?
    - [Please Ack](https://github.com/hyperledger/aries-rfcs/tree/main/features/0317-please-ack)
      
      - How does the controller indicate a request to add a `~please_ack`? Need a cross-cutting way.
      - Response when message is received – in the core handling.
      - Response when message is handled – harder, as it needs to be per protocol.
      - Any issues with the `~thread` decorator handling, e.g. message count?  Or will that just work?
    - [Static Peer DIDs](https://github.com/hyperledger/aries-rfcs/tree/b3a3942ef052039e73cd23d847f42947f8287da2/features/0627-static-peer-dids)
- Ontario's Proxy Controller Design - [Dave McKay](https://lf-hyperledger.atlassian.net/wiki/people/712020:24d508a3-ccfc-476f-b3c7-6b2549b19a23?ref=confluence) - [Presentation](https://docs.google.com/presentation/d/1sYb40dSvsuw7QbcN9fu-e0mZqBg6nnXgkwQc2m8gmK0/edit?usp=sharing)
- Questions – AMA

## Next Meeting

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [20211102 ACA-Pug Community Call Chat.txt](attachments/18494468/18515663.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18494468/18515662.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
