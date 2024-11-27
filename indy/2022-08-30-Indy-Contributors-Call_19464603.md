1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-08-30 Indy Contributors Call

Created by Stephen Curran, last modified on Aug 30, 2022

Zoom Link: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

## Summary

- Update on the Indy Ubuntu 20.04 Upgrade: Done?
- Update on the "mixed node" problem
- Update to DID Indy Method: Use a domain name for the "name" segment
- Q&amp;A

## Recording of Call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

[Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH) &lt;christiancarl.bormann@de.bosch.com&gt;

[Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@esatus.com&gt;

[Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio PBC) &lt;char@indicio.tech&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node
- Indy SDK
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy Node Container - [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)
- AnonCreds Specification: [https://anoncreds-wg.github.io/anoncreds-spec/](https://anoncreds-wg.github.io/anoncreds-spec/)

## Meeting Topics

- Update on the Indy Ubuntu 20.04 Upgrade – Done?
  
  - New release candidate – dev build is available, further updates are needed found from 16.04 release, needs to be tagged for RC
    
    - Add in recent updates to Indy
    - Review commit differences between main and 20.04 branches.
  - Sovrin Build – might be this week – should be copy/paste, although the pipelines take a long time to run (but 1/2 the time of the Jenkins pipelines!!!)
- Root cause and solution to the "mixed node" problem: [Indy Node issue 1769](https://github.com/hyperledger/indy-node/issues/1769)
  
  - Discussion of the short and long term handling of the issue.
  - Option 1: Just use the new "compat\_set" merging from now on.
  - Option 2: Add a config transaction with a transaction number and use "compat\_set" for earlier transactions, "sort" for ones after
  - Option 3: Versioning of transactions
  - **Option 4: Option 1  for now, and revisit after we are live**
- Using a domain name (e.g. "sovrin.org") as the name segment of a \`did:indy\` identifier, per this [GitHub Issue](https://github.com/hyperledger/indy-did-method/issues/66)
  
  - Make it optional – the challenge for some will be in retaining a long lasting domain name
  - How to keep the two versions (domain hosted, one in did-indy-networks repo) of the genesis file in sync?
    
    - Idea – GHA that compares the two files and if they differ, creates a Pull Request to update the one in GitHub repo to match the one on the domain name.
    - Pull request must be reviewed and merged by the editors according to the governance – ensures there is a human step in the process
- Action item: work on did-indy-networks
  
  - Include a static web generator so that we can publish a human friendly version of the information.
  - Include the governance guidance for the repo — who can merge and when?
- Odd pipeline behaviour – test export jobs failing – perhaps a missing/wrong token?  Fail showing because of export fail but the tests are passing.
  
  - exports being used so that debugging can occur when tests fail.
  - Could we disable for PRs, but allow for internal builds.
- Need to update the Indy read-the-docs documents
  
  - Project needed to provide updated docs
  - Would like to be on GH-Pages
  - Need to redirect from read-the-docs when the transition occurs

## Future Calls

- GDPR and the right to be forgotten – mitigations and approaches.

<!--THE END-->

- Status of Indy-SDK
  
  - Statement on the future of the Indy SDK: [PR 2329](https://github.com/hyperledger/indy-sdk/pull/2329)
  - Plans for future of Indy CLI (move to Indy VDR?)
  - Indy SDK in test for Indy Node (move to Indy VDR?)
  - Status of GitHub Actions for the Indy-SDK
- Indy bugs
  
  - Using GitHub tags "Good First Issue" and "Help Wanted"
  - [Node 1490](https://github.com/hyperledger/indy-plenum/issues/1490): problems with large catch-up
  - [Plenum 1506](https://github.com/hyperledger/indy-plenum/issues/1506): view change message consensus calculation error

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464603/19466231.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
