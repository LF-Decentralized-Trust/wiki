1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-10-11 Indy Contributors Call

Created by Stephen Curran, last modified on Oct 11, 2022

Zoom Link: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

## Summary

- Update on the "mixed node" problem
- Update on Sovrin Node pipeline
- AnonCreds outside of Indy
- Q&amp;A

## Recording of Call: [dummyfile.txt](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

[Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@esatus.com&gt;

[Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH) &lt;christiancarl.bormann@de.bosch.com&gt;

[Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio) &lt;[lynn@indicio.tech](mailto:lynn@indicio.tech)&gt;

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio) &lt;daniel@indicio.tech&gt;

[Gary de Beer](https://lf-hyperledger.atlassian.net/wiki/people/5a2233575ba27e1b07ea2896?ref=confluence) (One37) &lt;gary.debeer@one37id.com&gt;

[Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio PBC) &lt;char@indicio.tech&gt;

## Related Calls and Announcements

- DIF Interop WG is conducting a survey: [https://forms.gle/aLxj8MK2TuViyMav5](https://forms.gle/aLxj8MK2TuViyMav5)
  
  - Help shape the topics of future WG meetings!

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

- Root cause and solution to the "mixed node" problem: [Indy Node issue 1769](https://github.com/hyperledger/indy-node/issues/1769)
  
  - Demonstration done of the nodes
  - Question for Wade – can we get a release of indy-plenum, indy-node in the next two days.  "Yes!!!!!"
  - Work completed.
  - Need a way to test the network migration (16.04 to 20.04) on test networks affected by the ordering issue
- New bug found by [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) in Indy-Node (or perhaps Plenum)
  
  - View change to a node that has not caught up.
  - Creates problem.
- Another issue found by [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)
  
  - Audit ledger is supposed to create an entry every 5 minutes, but is actually creating 3 every 5 minutes (one per ledger instead of one across ledgers).
- Discussed [https://github.com/hyperledger/indy-node/pull/1783](https://github.com/hyperledger/indy-node/pull/1783)
- Sovrin Node build
  
  - Dependencies confusion between deb and python packages for installing sovrins
  - Hacky solution has been implemented that works, but...
  - Indy-Node Version mismatch between deb and pypi packages → [https://github.com/hyperledger/indy-node/issues/1781](https://github.com/hyperledger/indy-node/issues/1781)
- CANdy Prod is now in production in Canada – For Government Issuers – Wade leading the charge on that, but others in Canada participated and contributed.
  
  - Configs: [https://github.com/CQEN-QDCE/Candy](https://github.com/CQEN-QDCE/Candy)
  - Governance: [https://github.com/bcgov/bc-vcpedia/wiki/(Layer-1)-CANdy-Utility-Provisional-Governance-Framework](https://github.com/bcgov/bc-vcpedia/wiki/%28Layer-1%29-CANdy-Utility-Provisional-Governance-Framework)
  - Genesis Files: [https://github.com/ICCS-ISAC/dtrust-reconu](https://github.com/ICCS-ISAC/dtrust-reconu) / [https://github.com/ICCS-ISAC/dtrust-reconu/tree/main/CANdy/prod](https://github.com/ICCS-ISAC/dtrust-reconu/tree/main/CANdy/prod)
  - Ledger Browser: [https://candyscan.idlab.org/home/CANDY\_PROD](https://candyscan.idlab.org/home/CANDY_PROD)
- indy-vdr – how do we get that released?
  
  - [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)to work with Andrew Whitehead to get indy-vdr released with the associated flag update.
  - Also to check on the did:indy work within indy-vdr – it is not part of main. [https://github.com/hyperledger/indy-vdr/tree/did-indy](https://github.com/hyperledger/indy-vdr/tree/did-indy)
- AnonCreds:
  
  - [Proposal for Hyperledger AnonCreds to be a top level project is here](http://2021).  Please review, comment and if you support this, and your name to the sponsor list.
  - AnonCreds on ledgers other than Indy – now up to 6 independent implementations.  Working in the spec. group on making that easier.
  - AnonCreds in W3C VC Data Model standard.  Seems to be not very difficult to do.  Working on a proposal to share for putting an AnonCreds VC into W3C format (and reverse) and the same for an AnonCreds presentation into W3C VC (or VP) Data Model format.

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464609/19466269.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
