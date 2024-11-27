1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2024 Meetings and Notes](2024-Meetings-and-Notes_19466709.html)

# Hyperledger Indy : 2024-11-19 Indy Contributors Call

Created by Char Howland, last modified by Stephen Curran on Nov 19, 2024

## Summary

- Discussion about the state of Indy
  
  - Indy Quarterly Report: [https://github.com/LF-Decentralized-Trust/governance/pull/68](https://github.com/LF-Decentralized-Trust/governance/pull/68)
- Updates
  
  - [Indy Besu](https://github.com/hyperledger/indy-besu) updates and discussion
  - Trust DID Web
- Open Discussion

## **Zoom:** [https://zoom.us/j/93198495358?pwd=TS80VklHVElJS3lEcjUzQjV0VHVtUT09](https://zoom.us/j/93198495358?pwd=TS80VklHVElJS3lEcjUzQjV0VHVtUT09)

## **Recording:**

![antitrust-policy-notice.png](https://github.com/LF-Decentralized-Trust/governance/blob/845bf277e246fa2be73be260f57b645b8aa84838/tac/meeting-minutes/images/antitrust-policy-notice.png?raw=true)

![](https://raw.githubusercontent.com/LF-Decentralized-Trust/governance/717c2020287a32594adff365c898b6bfe90d630a/tac/meeting-minutes/images/all-are-welcome.png)

LF Decentralized Trust is committed to creating a safe and welcoming

community for all. For more information

please visit the [LFDT Code of Conduct](https://lf-decentralized-trust.github.io/governance/governing-documents/code-of-conduct.html).

## Welcome and Introductions

## Attendees

- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio PBC) &lt;char@indicio.tech&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) (Indicio PBC) &lt;daniel@indicio.tech&gt;
- Kim Ebert (Indicio PBC) &lt;kim@indicio.tech&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

## Related Calls and Announcements

- Sovrin Foundation is preparing for the likely ending of operations of its MainNet ledger on March 31, 2025
  

## Release Status and Work Updates

- Indy Node/plenum – PR needed to replace Ursa with the indy-blssignatures-rs implementation. Issue #
- Indy-Besu - [https://github.com/hyperledger/indy-besu](https://github.com/hyperledger/indy-besu)
- Indy-test-automation
- Indy-Node test-automation integration next step after cleaning up the dependencies issues and getting the sovrin-test-automation finished.
- Indy SDK – to be deprecated
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy Node Container - [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar, anoncreds-rs)
  
  - Small update to Indy VDR to update the dynamic network discovery URL; needs to be published
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)
- AnonCreds Specification: [https://anoncreds-wg.github.io/anoncreds-spec/](https://anoncreds-wg.github.io/anoncreds-spec/)

## Meeting Topics

- Discussion about the state of Indy
  
  - Indy Quarterly Report: [https://github.com/LF-Decentralized-Trust/governance/pull/68](https://github.com/LF-Decentralized-Trust/governance/pull/68)
  - Indicio can put resources towards PR reviews
  - Quebec Team also expressed interest in contributing resources
  - Stephen will bring to the TAC the recommendation that Indy should not be placed in a dormant state
    
    - We will engage with those who are running Indy networks but are not involved in the community to see if they would like to get involved and potentially contribute resources
- Updates
  
  - Ubuntu 22.04 upgrade
    
    - Seeking review of [https://github.com/hyperledger/indy-node/pull/1870](https://github.com/hyperledger/indy-node/pull/1870)
  - [Indy Besu](https://github.com/hyperledger/indy-besu) updates and discussion
  - Trust DID Web
- Open Discussion

Next Meeting

- Presentation on Indy Read Replica Project from Hyperledger Mentorship Program mentee Bryan Elee

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

- Indy-Besu
  
  - Continue discussion about open questions [https://github.com/hyperledger/indy-node/issues/1826#issuecomment-1868609236](https://github.com/hyperledger/indy-node/issues/1826#issuecomment-1868609236)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
