1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2024 Meetings and Notes](2024-Meetings-and-Notes_19466709.html)

# Hyperledger Indy : 2024-10-08 Indy Contributors Call

Created by Char Howland, last modified by Stephen Curran on Oct 08, 2024

## Summary

- Indy Read Replica progress from mentee Bryan Elee
- Updates
  
  - Ubuntu 22.04 upgrade
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
- [Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence) (DSR Corporation) &lt;[renata.toktar@dsr-corporation.com](mailto:renata.toktar@dsr-corporation.com)&gt;

## Related Calls and Announcements

## Release Status and Work Updates

- Indy Node/plenum – PR needed to replace Ursa with the indy-blssignatures-rs implementation. Issue #
- Indy-Besu - [https://github.com/hyperledger/indy-besu](https://github.com/hyperledger/indy-besu)
- Indy-test-automation
- Indy-Node test-automation integration next step after cleaning up the dependencies issues and getting the sovrin-test-automation finished.
- Indy SDK – to be deprecated
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy Node Container - [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar, anoncreds-rs)
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)
- AnonCreds Specification: [https://anoncreds-wg.github.io/anoncreds-spec/](https://anoncreds-wg.github.io/anoncreds-spec/)

## Meeting Topics

- Indy Read Replica progress from mentee Bryan Elee
  
  - [https://github.com/rxbryan/indyread](https://github.com/rxbryan/indyread)
  - [https://github.com/rxbryan/indyread/blob/main/docs/API.md](https://github.com/rxbryan/indyread/blob/main/docs/API.md)
- Updates
  
  - Ubuntu 22.04 upgrade
    
    - Seeking review of [https://github.com/hyperledger/indy-node/pull/1870](https://github.com/hyperledger/indy-node/pull/1870)
  - [Indy Besu](https://github.com/hyperledger/indy-besu) updates and discussion
    
    - Fixed a bug with Schema and Cred Def identifiers - namespace definition - [https://github.com/hyperledger/indy-besu/pull/102](https://github.com/hyperledger/indy-besu/pull/102)
    - [Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence) shared ideas about comparing Indy-Besu and EBSI
  - Trust DID Web
    
    - Changes the log entries from array to named object - more flexible and self-describing
    - New information site - [https://didtdw.org/latest/](https://didtdw.org/latest/)
  - We were not selected for Ledger Redaction: NGI-Sargasso 
    
    - action items: define next steps for investment
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

- Indy-Besu
  
  - Continue discussion about open questions [https://github.com/hyperledger/indy-node/issues/1826#issuecomment-1868609236](https://github.com/hyperledger/indy-node/issues/1826#issuecomment-1868609236)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
