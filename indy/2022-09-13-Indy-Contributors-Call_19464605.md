1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-09-13 Indy Contributors Call

Created by Stephen Curran, last modified on Sep 14, 2022

Zoom Link: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

## Summary

- Vulnerabilities
- Update on the Indy Ubuntu 20.04 Upgrade: Done?
- Update on the "mixed node" problem
- Q&amp;A

## Recording of Call: [20220913 Indy Contributors Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

[Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@esatus.com&gt;

[Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)(Indicio PBC) &lt;lynn@indicio.tech&gt;

[Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)(Indicio PBC) &lt;daniel@indicio.tech&gt;

[Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH) &lt;ChristianCarl.Bormann@de.bosch.com&gt;

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

- Vulnernabities - Published
  
  - [https://github.com/hyperledger/indy-node/security/advisories/GHSA-r6v9-p59m-gj2p](https://github.com/hyperledger/indy-node/security/advisories/GHSA-r6v9-p59m-gj2p)
  - [https://github.com/hyperledger/indy-node/security/advisories/GHSA-x996-7qh9-7ff7](https://github.com/hyperledger/indy-node/security/advisories/GHSA-x996-7qh9-7ff7)
- Update on the Indy Ubuntu 20.04 Upgrade – Done?
  
  - Token-plugin nearly done. 
    
    - → found a problem with prepare script with indy-node Issue: [https://github.com/hyperledger/indy-node/issues/1778](https://github.com/hyperledger/indy-node/issues/1778)
      
      PR: [https://github.com/hyperledger/indy-node/pull/1779](https://github.com/hyperledger/indy-node/pull/1779)
  - libSovToken is nearly done as well, one outstanding Jenkins issue.
  - Sovrin package is next in line
- Root cause and solution to the "mixed node" problem: [Indy Node issue 1769](https://github.com/hyperledger/indy-node/issues/1769)
  
  - It's worse than expected,,,,
  - A flag was added to the 20.04 based branch to set default ordering to sorted ordering, this unblocks the creation of new Ubuntu 20.04 networks.
  - Next step.  Explore a new config transaction to signal point in time events.  Modeled to be generic for other such issues, complete with helpers in the code to detect and cache the txns.
    
    - Transactions handling and caching could all be generic.  Only concrete implementation(s) (plugins) needed would be for the specific transaction types, such as the ordering switchover point we need now.
  - Timing of the fixes/release:
    
    - Decision point - Do we release 1.13.x with just compatibility ordering or wait until we have a mechanism to be able to switch to sorted ordering?
      
      - The group decided we should investigate the new config transaction proposal more and discuss the releases again in 2 weeks when we know more about implementation effort.
  - Need volunteers to start looking into the proposed design.
- Action item: work on did-indy-networks
  
  - [https://github.com/hyperledger/indy-did-networks](https://github.com/hyperledger/indy-did-networks)
    
    - [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) started working on  a draft PR with documentation.
  - [https://anoncreds-wg.github.io/anoncreds-objects-methods-registry/#governance](https://anoncreds-wg.github.io/anoncreds-objects-methods-registry/#governance)
    
    - Reuse content from here for the indy-did-networks content.

## re Calls

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464605/19466244.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
