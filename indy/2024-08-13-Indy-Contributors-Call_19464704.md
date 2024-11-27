1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2024 Meetings and Notes](2024-Meetings-and-Notes_19466709.html)

# Hyperledger Indy : 2024-08-13 Indy Contributors Call

Created by Char Howland, last modified by Renata Toktar on Aug 13, 2024

## Summary

- Indy Project Charter
- Updates
  
  - Ubuntu 22.04 upgrade
  - [Indy Besu](https://github.com/hyperledger/indy-besu) updates and discussion
  - Indy Mentorship Project (Read Replicas)
- Open Discussion

## **Zoom:** [https://zoom.us/j/93198495358?pwd=TS80VklHVElJS3lEcjUzQjV0VHVtUT09](https://zoom.us/j/93198495358?pwd=TS80VklHVElJS3lEcjUzQjV0VHVtUT09)

## **Recording:**

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

Kim Ebert &lt;kim@indicio.tech&gt;

[Renata Toktar](https://lf-hyperledger.atlassian.net/wiki/people/633ab33e140ba0bf651d1f2f?ref=confluence) (DSR Corporation) &lt;[renata.toktar@dsr-corporation.com](mailto:renata.toktar@dsr-corporation.com)&gt;

## Related Calls and Announcements

- Hyperledger Mentorship Project - acceptance complete

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

- Indy Project Charter:
  
  - Stems from the recent "intent to form" [announcement](https://www.linuxfoundation.org/press/linux-foundation-announces-intent-to-form-lf-decentralized-trust) from the Linux Foundation and Hyperledger Foundation about LF Decentralized Trust.
  - Proposed Charter: [https://docs.google.com/document/d/1rFPDlH5VYS9sVqcGRbWfOoxwhVTZQ7jaX9b8R6fhtsw/edit](https://docs.google.com/document/d/1rFPDlH5VYS9sVqcGRbWfOoxwhVTZQ7jaX9b8R6fhtsw/edit)
  - Plan:
    
    - Create an "indy" repo, similar to this [Aries repo](https://github.com/hyperledger/aries).
    - Put into it a "[TSC.md](http://TSC.md)" file that lists the Indy TSC members (currently on the Indy Admin Team list) and processes – same as this [TSC.md in Aries](https://github.com/hyperledger/aries/pull/22/files?short_path=a30a225#diff-a30a2252bbf738b901d35399ea54d5f4dffbbf6bf9e2619de7c3fe53b14c7262).
    - Put into it a "[MAINTAINERS.md](http://MAINTAINERS.md)" that points to the Hyperledger "[access-control.yaml](https://github.com/hyperledger/governance/blob/main/access-control.yaml)" file and processes of Maintainers – same as this [MAINTAINERS.md in Aries](https://github.com/hyperledger/aries/pull/23/files?short_path=39da3bd#diff-39da3bd6270d44ea37b6ed50bd42eeb9d93ac5e1639645871a69cbe08cbe29de).
    - Put a "[MAINTAINERS.md](http://MAINTAINERS.md)" ([like this one](https://github.com/hyperledger/aries-mediator-service/pull/167/files?short_path=39da3bd#diff-39da3bd6270d44ea37b6ed50bd42eeb9d93ac5e1639645871a69cbe08cbe29de)) file in all Indy repos that points to the "[access-control.yaml](https://github.com/hyperledger/governance/blob/main/access-control.yaml)" file and to the `indy` repo [MAINTAINERS.md](http://MAINTAINERS.md)
    - Update the charter to match roughly what is in the [Aries Charter](https://docs.google.com/document/d/1F6RbR7xDaBt5CDJhqLJzR4c1pDJtyPGshp9fy6eVtSM/edit?usp=drive_link)
- Ubuntu 22.04 upgrade
  
  - Seeking review of [https://github.com/hyperledger/indy-node/pull/1870](https://github.com/hyperledger/indy-node/pull/1870)
- [Indy Besu](https://github.com/hyperledger/indy-besu) updates and discussion
  
  - Revocation is in progress.  CPQD has implemented some code for revocation / API and design, based on revocation list.
    
    - [https://github.com/hyperledger/indy-besu/pull/76](https://github.com/hyperledger/indy-besu/pull/76)
  - Hyperledger Meetup planned for the end of September – "Indy on Besu" – looking for contributors to lead the meetup re: Indy / Besu -- Both / Either.
- Updates
  
  - Indy Mentorship Project (Read Replicas)
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
