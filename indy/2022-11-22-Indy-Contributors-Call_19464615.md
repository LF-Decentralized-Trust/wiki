1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-11-22 Indy Contributors Call

Created by Char Howland, last modified on Dec 02, 2022

## Summary

- Update on Sovrin Node pipeline
- Help getting Indy Node to past "RC" status
- Update on indy-vdr issue with Genesis File/Node mismatch issue + plus tests
- Eliminate the indy-sdk initiative

## Recording of Call: ![](plugins/servlet/confluence/placeholder/unknown-attachment)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) Neoteric Technologies Inc. &lt;wade@neoterictech.ca&gt;

[Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)Indicio &lt;lynn@indicio.tech&gt;

[Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) Indicio &lt;kim@indicio.tech&gt;

[Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH) &lt;christiancarl.bormann@de.bosch.com&gt;

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

- IIW Update
  
  - AnonCreds and their use with other ledgers and the W3C format
  - DIDComm vs OpenID for VC
  - Implemtation of predicates using BBS+
- Sovrin Node build
  
  - Working through blockers on the Indy Test Automation pipeline
- Help on the transition of indy-node from RC to final
  
  - Determining if there are commits on the main branches of indy-node and indy-plenum that should be in the 20.04 upgrade branches
  - Kim anticipates having recommendations next meeting
  - Christian tried the migration process switching to the current release candidate
    
    - Ran into some networking issues
    - Difficulty getting a timeslot that works for everyone
- Update on indy-vdr issue with Genesis File/Node mismatch issue ([indy-vdr#106](https://github.com/hyperledger/indy-vdr/issues/106))
  
  - Workaround from Lynn is updating the genesis file to ensure that you have a current snapshot of the network you're connecting to
  - Andrew is determining is there is a secure and reliable way to sync transactions from the pool without requiring full-on consensus with the network
- Using indy-node-container for the indy-vdr tests
  
  - Draft PR from Christian: [https://github.com/hyperledger/indy-vdr/pull/112](https://github.com/hyperledger/indy-vdr/pull/112)
- Deprecate the indy-sdk initiative
  
  - Adam is evaluating the best path forward for phasing out the Indy SDK
    
    - Whether to continue with having it be a Rust application or to move to using a Python applucation that uses the binaries built for Askar, Indy-VDR, etc.
    - Preparing proposal for the future of the Indy-CLI
- Questions bout deprecating the indy-sdk
  
  - The whole community is moving away from indy-sdk towards Askar, indy-vdr, and the other shared libraries
  - Discussion about the migration is happening on the indy-vdr and ACA-Py channels on discord
- Question about the implementation of observer nodes
  
  - Still just a concept, not implemented except some pieces in plenum; not known documentation
- Other Topics

## Future Calls

- Indy Roadmap
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464615/19466338.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464615/19466337.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
