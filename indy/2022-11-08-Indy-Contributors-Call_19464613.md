1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-11-08 Indy Contributors Call

Created by Stephen Curran, last modified on Nov 08, 2022

## Summary

- Update on Sovrin Node pipeline
- Help needed on getting Indy Node to past "RC" status
- Update on indy-vdr issue with Genesis File/Node mismatch issue + plus tests
- Updates on the AnonCreds work that impact Indy
- Security testing outcomes, [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)
- Eliminate the indy-sdk initiative
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

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov / Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio) &lt;kim@indicio.tech&gt;

[Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH) &lt;christiancarl.bormann@de.bosch.com&gt;

[Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence)(esatus AG) &lt;p.schlarb@esatus.com&gt;

[Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)(Indicio, PBC) &lt;lynn@indicio.tech&gt;

## Related Calls and Announcements

- IIW Next Week – any sessions planned?

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

- Sovrin Node build
  
  - Indy Test Automation – focus of work. GHActions work, through some blockers – likely the big ones. Nothing more this week, but back to it next week.
- Help on the transition of indy-node from RC to final:
  
  - A review of the differences between the indy-node and indy-plenum "[main](https://github.com/hyperledger/indy-node/tree/main)" and "[ubuntu-20.04-upgrade](https://github.com/hyperledger/indy-node/tree/ubuntu-20.04-upgrade)" branches
    
    - Where there are things needed items in main, determine if they need to be added to the "[ubuntu-20.04-upgrade](https://github.com/hyperledger/indy-node/tree/ubuntu-20.04-upgrade)" branch
      
      - Development has continued on main and ubuntu-20.04-upgrade (branched from main) – what is missing from main that should be in ubuntu-20.04-upgrade branch?
    - This is the result of the "two branch" strategy for the repos, followed by a period without maintainers watching the branches.
    - Once we have the "ubuntu-20.04" branch complete, it will be become main, and we'll ignore the other branches.
  - 3rd party dependencies – such as this [https://github.com/hyperledger/indy-node/issues/1786#issuecomment-1292236274](https://github.com/hyperledger/indy-node/issues/1786#issuecomment-1292236274) needs some help
  - Other issues found by [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)
    
    - Audit ledger is supposed to create an entry every 5 minutes, but is actually creating 3 every 5 minutes (one per ledger instead of one across ledgers). Issue – not fixed.
      
      - [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)to open issue with the details when he has a chance.
      - Concern is a large audit ledger delays catch-up.
    - Issue with the timestamp recording for the domain ledger during catchup. Could cause a corruption, but unlikely. Fix has been added. Need to get to 1.13 to properly fix this.
      
      - Need to validate that this will work on existing networks.
      - More research into the real world implications
      - [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)still looking at it.
- Update on indy-vdr issue with Genesis File/Node mismatch issue ([indy-vdr#106](https://github.com/hyperledger/indy-vdr/issues/106))
  
  - indy-vdr on connecting tries to do a consensus by connecting to lots of nodes
  - Triggered on Sovrin Staging Net – genesis file has 16 nodes, indy-vdr tries to connect to at least 6
    
    - One genesis file node is active on MainNet, no longer on StagingNet – so it's response is bad.
      
      - Don't do this! On changing network, change something...perhaps remove from the genesis file, or the IP address, or the port(s)
    - If another node is slow or unresponsive, indy-vdr gives a timeout
  - Workaround is to have an accurate genesis file – e.g. for StagingNet, add an additional genesis file
  - Another app level workaround is to cache the pool state and pass that to indy-vdr (vs. the genesis file)
  - Related security testing outcomes, [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) - bottom line – no concerns identified.
    
    - Sometimes nodes out, if they were part of the ones that indy-vdr is connecting to, that's a problem. Nodes from genesis file is random.
    - indy-sdk behaves differently and it didn't happen: What's the difference? Can indy-vdr be changed to be more aligned with what indy-sdk is doing?
    - Trying to do consistency check, testing on 4 node network – what if there is just 1 one node and trying to "steal" a node.
      
      - Series of tests to "steal" a network or nodes.
      - Unable to exploit any vulnerability in trying to find if the node is valid.  Checks are necessary.
      - Recommendations for genesis file updates
    - GHA to create a PR to update the indy-networks repo when the genesis file changes, with a human to merge the PR.
- Question from Christian today – using indy-node-container for the indy-vdr tests
  
  - In [https://github.com/hyperledger/indy-vdr/tree/did-indy/ci](https://github.com/hyperledger/indy-vdr/tree/did-indy/ci) there is a indy network being started – much better to use common indy-node-container
  - [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence)– another issue to be created to propose this, get it on the backlog
- Deprecate the indy-sdk initiative:
  
  - Enable shared components in all Aries Framework – notable AFJ and Aries VCX
  - indy-vdr with did:indy support – how do we get that released?
  - indy-vdr is using Ursa, which is using a deprecated Rust module "failure" – [https://github.com/hyperledger/ursa/issues/199](https://github.com/hyperledger/ursa/issues/199); [CVE](https://rustsec.org/advisories/RUSTSEC-2020-0036) - very high score! Possibly not critical for us, but looks bad.
  - Create a migration tool to export indy-wallet contents and load into aries-askar
  - Create a "shared components" version of the Indy CLI
  - New transaction types in indy-vdr – draft PR, but needs work and testing
  - Indy Test Automation relies on the indy-sdk, needs to be moved to indy-sdk
  - Community impact on the use of the indy-sdk – a need to migrate
  - Tools on the indy-node nodes – do they use libindy?  Investigation needed – [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) / [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) to look at/create issue.
- Updates on the AnonCreds work that impact Indy
- Other Topics

## Future Calls

- GDPR and the right to be forgotten – mitigations and approaches.
- The Indy "Corporate Firewall Problem" and the idea of a Proxy Server on Nodes? [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence)
  
  - Core issue: A mobile wallet user using a Corporate WiFi may find that they can't get to an Indy ledger because all but 80/443 ports and HTTP/S protocols are blocked
  - Discussion/Options paper: [https://hackmd.io/@n5FW6jwuRfCgchBDNWR3VQ/H1kNlKpmo](https://hackmd.io/@n5FW6jwuRfCgchBDNWR3VQ/H1kNlKpmo)
  - **Question**: Is it viable to have each Indy Node also listen on port 80/443 for HTTP/S requests and arrange to have them processed?
    
    - Option: Receive on HTTP(S) and send on to local ZMQ instance as if coming from outside.
  - **Answer:** We think it is probably not viable, as mobile agents require HTTPS. As such, each Steward would have to get a IP-based SSL Certificate. Technically doable, but getting everyone through that is really not practical. The cost of the certificates and maintaining them would be ugly.
    
    - Option: Add a DIDComm agent to every node, and use DIDComm to send the messages
    - Similar to using HTTP(S), but use a DIDComm message. Since Mobile Agents would be using a mediator, the DIDComm message would flow through that, and the HTTPS issue would not matter.  This is almost easy, but... There is no encryption public key in the genesis file, so that needs to be retrieved from somewhere else...

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464613/19466292.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
