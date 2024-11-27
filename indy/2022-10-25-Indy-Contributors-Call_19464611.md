1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-10-25 Indy Contributors Call

Created by Stephen Curran, last modified on Oct 25, 2022

Zoom Link: [https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09](https://zoom.us/j/99220079317?pwd=OHk0U05ITnBkSmZ0aXlIQzFDYWg3UT09)

## Summary

- Update on the "mixed node" problem
- Update on Sovrin Node pipeline
- The Indy "Corporate Firewall Problem" and the idea of a Proxy Server on Nodes
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

[Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio) &lt;kim@indicio.tech&gt;

[Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence)(esatus AG) &lt;p.schlarb@esatus.com&gt;

[Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)(Robert Bosch Gmbh) &lt;ChristianCarl.Bormann@de.bosch.com&gt;

## Related Calls and Announcements

- DIF Interop WG is conducting a survey: [https://forms.gle/aLxj8MK2TuViyMav5](https://forms.gle/aLxj8MK2TuViyMav5)
  
  - Help shape the topics of future WG meetings!
- AnonCreds is now a top-level project

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
  
  - Still need to merge the pull requests.  They are approved, but not merged.
  - [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) and team reviewed and approved
  - [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) to merge them
- Other issues found by [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)
  
  - Audit ledger is supposed to create an entry every 5 minutes, but is actually creating 3 every 5 minutes (one per ledger instead of one across ledgers). Issue – not fixed.
  - Issue with the timestamp recording for the domain ledger during catchup. Could cause a corruption, but unlikely. Fix has been added. Need to get to 1.13 to properly fix this.
- Sovrin Node build
  
  - Dev containers for the sovrin repos
  - Pipeline is a work in progress – published version of libsovtoken was complicated – Jenkins pipeline issue.  GHA added and now run.
    
    - Discovered and fixed all pipelines because of deprecation of Node 12 in GHA.  All now updated.
  - Currently working to get the full suite of indy automation tests running, manually.  Then get the GHA implemented.
    
    - This is the hard part – not clear how long this will take.
  - After that:
    
    - GHA actions to publish the sovrin artifacts.
- indy-vdr with did:indy support – how do we get that released?
  
  - Two PRs created by [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)in indy-vdr today.
    
    - Verification key - [https://github.com/hyperledger/indy-vdr/pull/10](https://github.com/hyperledger/indy-vdr/pull/105)4
    - Structured the indy-did-methods structure – GHA needs to be run, but probably just a network issue. [https://github.com/hyperledger/indy-vdr/pull/105](https://github.com/hyperledger/indy-vdr/pull/105)
- Genesis file issue on a network
  
  - Two of four nodes in Genesis File were missing from a network. Indy-SDK works fine, but Aries Askar does not work. What is the difference in the implementations?
  - Need to get an issue created in the indy-vdr repo. 
    
    - Another scenario: 4 nodes in genesis, 2 requests made, but when 7 nodes in genesis, 3 requests made.
      
      - Is this possibly a feature, not a bug, to make sure that a genesis file attack was being prevented.  Note to check Lynn's comments in the call recording.
        
        - Idea – one node in the genesis file is contacted, but is connected to other nodes to achieve consensus.  Is that possible?
  - Wade is seeing this issue on Sovrin Staging Net.
- The Indy "Corporate Firewall Problem" and the idea of a Proxy Server on Nodes? [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence)
  
  - Core issue: A mobile wallet user using a Corporate WiFi may find that they can't get to an Indy ledger because all but 80/443 ports and HTTP/S protocols are blocked
  - Discussion/Options paper: [https://hackmd.io/@n5FW6jwuRfCgchBDNWR3VQ/H1kNlKpmo](https://hackmd.io/@n5FW6jwuRfCgchBDNWR3VQ/H1kNlKpmo)
  - **Question**: Is it viable to have each Indy Node also listen on port 80/443 for HTTP/S requests and arrange to have them processed?
    
    - Option: Receive on HTTP(S) and send on to local ZMQ instance as if coming from outside.
- Other Topics

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464611/19466279.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
