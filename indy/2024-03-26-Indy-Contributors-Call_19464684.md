1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2024 Meetings and Notes](2024-Meetings-and-Notes_19466709.html)

# Hyperledger Indy : 2024-03-26 Indy Contributors Call

Created by Char Howland, last modified on Mar 27, 2024

## Summary

- [Indy Besu](https://github.com/hyperledger/indy-besu) updates and discussion
- Ubuntu 22.04 upgrade
- Next Indy Summit
- Mentorship project submissions
- Any updates on upgrade or documentation contributions
- Open Discussion

## **Zoom:** [https://zoom.us/j/93198495358?pwd=TS80VklHVElJS3lEcjUzQjV0VHVtUT09](https://zoom.us/j/93198495358?pwd=TS80VklHVElJS3lEcjUzQjV0VHVtUT09)

## **Recording:** [Call Recording](https://lf-hyperledger.atlassian.net/wiki/download/attachments/19464684/video1187569130.mp4?version=1&modificationDate=1711565851957&api=v2)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio, PBC) &lt;char@indicio.tech&gt;
- [Sylvain Martel](https://lf-hyperledger.atlassian.net/wiki/people/712020:9eb55fb2-a220-4945-916a-6da7d1ed6101?ref=confluence) (Gouv Qc) &lt;sylvain.martel10@mcn.gouv.qc.ca&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio, PBC) &lt;lynn@indicio.tech&gt;
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio, PBC) &lt;kim@indicio.tech&gt;
- [Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence) (DSR Corporation) &lt;[renata.toktar@dsr-corporation.com](mailto:renata.toktar@dsr-corporation.com)&gt;

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
- Ursa
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)
- AnonCreds Specification: [https://anoncreds-wg.github.io/anoncreds-spec/](https://anoncreds-wg.github.io/anoncreds-spec/)

## Meeting Topics

- [Indy Besu](https://github.com/hyperledger/indy-besu) updates and discussion
  
  - [https://github.com/hyperledger/indy-did-method/pull/86](https://github.com/hyperledger/indy-did-method/pull/86) - sent a draft PR
  - [https://github.com/hyperledger/indy-besu/pull/38](https://github.com/hyperledger/indy-besu/pull/38) - updated error handling
- Ubuntu 22.04 upgrade
  
  - Indy-plenum work in progress
  - Work is being done here [https://github.com/reflectivedevelopment/indy-plenum/tree/feature/ubuntu22.04](https://github.com/reflectivedevelopment/indy-plenum/tree/feature/ubuntu22.04)
  - Most packages are being built via wheel2deb
  - Some packages are still being built with fpm, as not all compatible with wheel2deb
  - A package conflicts with base debian package, need to investigate further. bump\_version script behaving differently, may need to build and install dependencies first
- Next Indy Summit
  
  - April 9
  - Topic: ledger redaction (tombstoning- marking txns as nonresolvable)
  - Register: [https://zoom.us/meeting/register/tJMqdumsrDIvHt2Y-I3IHNpWeLUTyHnwYT3h#/registration](https://zoom.us/meeting/register/tJMqdumsrDIvHt2Y-I3IHNpWeLUTyHnwYT3h#/registration)
  - [Meeting page](https://docs.google.com/document/d/1Gkd-V17tAYQFI4ymtIGUjfQxBlgOYVj0WBdX1ZdWA_g/edit)
- Mentorship project submissions
  
  - TOC review until the 29th
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

- Indy-Besu
  
  - Continue discussion about open questions [https://github.com/hyperledger/indy-node/issues/1826#issuecomment-1868609236](https://github.com/hyperledger/indy-node/issues/1826#issuecomment-1868609236)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464684/19466777.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
