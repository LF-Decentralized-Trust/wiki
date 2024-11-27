1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2023 Meetings and Notes](2023-Meetings-and-Notes_19466378.html)

# Hyperledger Indy : 2023-11-21 Indy Contributors Call

Created by Char Howland, last modified on Nov 22, 2023

## Summary

- Absa / Patrik Stas: Review of DSR's Besu POC
- PR review: [Initial version of readme, code of conduct, contributing information](https://github.com/hyperledger/indy-did-networks/pull/2)
- - Associated issue: [Discussion about network identifiers](https://github.com/hyperledger/indy-did-networks/issues/3)
- [Validator prep PR review](https://github.com/hyperledger/indy-node/pull/1825)
- Co-creation projects at IDLab: [https://www.idlab.org/en/projects/public-review/](https://www.idlab.org/en/projects/public-review/ "https://www.idlab.org/en/projects/public-review/")
- Read replicas
- Any updates on upgrade or documentation contributions
- Open Discussion

## **Zoom:** [https://zoom.us/j/93198495358?pwd=TS80VklHVElJS3lEcjUzQjV0VHVtUT09](https://zoom.us/j/93198495358?pwd=TS80VklHVElJS3lEcjUzQjV0VHVtUT09)

## **Recording:** [11212023 Recording](https://lf-hyperledger.atlassian.net/wiki/download/attachments/19464668/11212023%20Indy%20Contributors%20WG%20Recording.mp4?version=4&modificationDate=1700676597062&api=v2)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio, PBC) &lt;char@indicio.tech&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Emiliano Suñé](https://lf-hyperledger.atlassian.net/wiki/people/60f1a8944257a90070da4a78?ref=confluence) (BC Gov / Quartech) &lt;emiliano.sune@quartech.com&gt;
- [Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence) (DSR Corporation) &lt;[renata.toktar@dsr-corporation.com](mailto:renata.toktar@dsr-corporation.com)&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node/plenum – PR needed to replace Ursa with the indy-blssignatures-rs implementation. Issue #
- Indy-test-automation
- Indy-Node test-automation integration next step after cleaning up the dependencies issues and getting the sovrin-test-automation finished.
- Indy SDK – to be deprecated
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy Node Container - [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar, anoncreds-rs)
- Ursa
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)
- AnonCreds Specification: [https://anoncreds-wg.github.io/anoncreds-spec/](https://anoncreds-wg.github.io/anoncreds-spec/)

## Meeting Topics

- Absa / Patrik Stas: Review of DSR's Besu POC
  
  - `did:ethr`  +  custom `anoncreds registry`  POC: [https://github.com/gmulhearn/anoncreds-on-ethereum](https://github.com/gmulhearn/anoncreds-on-ethereum)
- PR review: [Initial version of readme, code of conduct, contributing information](https://github.com/hyperledger/indy-did-networks/pull/2)
  
  - Associated issue: [Discussion about network identifiers](https://github.com/hyperledger/indy-did-networks/issues/3)
- [Validator prep PR review](https://github.com/hyperledger/indy-node/pull/1825)
- Co-creation projects at IDLab: [https://www.idlab.org/en/projects/public-review/](https://www.idlab.org/en/projects/public-review/ "https://www.idlab.org/en/projects/public-review/")
- Read replicas
- Any updates on upgrade or documentation contributions
- Open Discussion

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

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464668/19466679.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464668/19466676.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
