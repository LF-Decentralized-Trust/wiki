1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2023 Meetings and Notes](2023-Meetings-and-Notes_19466378.html)

# Hyperledger Indy : 2023-01-31 Indy Contributors Call

Created by Char Howland, last modified on Feb 08, 2023

## Summary

- Update on Sovrin Node pipeline
- DSR progress report
- Transition of indy-node from RC to final - branch comparisons
- Open Discussion

## Recording of Call: [20230131 Indy Contributors Call](https://lf-hyperledger.atlassian.net/wiki/download/attachments/19464628/20230131%20-%20Indy%20Contributors%20Call%20Recording.mp4?version=1&modificationDate=1675219255799&api=v2)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio, PBC) &lt;char@indicio.tech&gt;
- [Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@esatus.com&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence) (Indicio, PBC) &lt;lynn@indicio.tech&gt;
- [Sylvain Martel](https://lf-hyperledger.atlassian.net/wiki/people/712020:9eb55fb2-a220-4945-916a-6da7d1ed6101?ref=confluence) (Qc Gov) &lt;sylvain.martel10@mcn.gouv.qc.ca&gt;
- [Alexander Sherbakov](https://lf-hyperledger.atlassian.net/wiki/people/557058:a955b109-9f8c-405c-9f96-0903d4de8c46?ref=confluence) (DSR) &lt;alexander.sherbakov@dsr-corporation.com&gt;
- [Vladimir Shishkin](https://lf-hyperledger.atlassian.net/wiki/people/712020:cef06dc4-c20a-48e8-bb2c-64cf2765a3da?ref=confluence) (DSR) &lt;vladimir.shishkin@dsr-corporation.com&gt;

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

- Sovrin Node build
  
  - Ubuntu 20.04-compatible release candidate for Sovrin Node!
    
    - [https://github.com/sovrin-foundation/sovrin/releases/tag/v1.2.0-rc1](https://github.com/sovrin-foundation/sovrin/releases/tag/v1.2.0-rc1 "https://github.com/sovrin-foundation/sovrin/releases/tag/v1.2.0-rc1")
    - [https://sovrin.jfrog.io/ui/repos/tree/General/deb/pool/focal/rc/s/sovrin/sovrin\_1.2.0~rc1\_amd64.deb](https://sovrin.jfrog.io/ui/repos/tree/General/deb/pool/focal/rc/s/sovrin/sovrin_1.2.0~rc1_amd64.deb)
  - Testing in VON network with new package- has gone well
  - Lynn has gotten new and replaced nodes working on the Indicio tempnet
  - Refactoring Indy test automation and incorporate it into the Indy node pipeline
- Transition of indy-node from RC to final
  
  - Issue created: [https://github.com/hyperledger/indy-node/issues/1791](https://github.com/hyperledger/indy-node/issues/1791)
  - Priority raised on this issue since we have the release candidate
- DSR progress report
  
  - Update of VON network to use the recent Indy-VDK depedency instead of libindy
    
    - Done
  - New Indy CLI based on Indy VDR and Aries Askar
    
    - PR waiting for review
  - Indy test automation
    
    - Made improvements in Askar and Indy VDR
    - Good process here
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

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464628/19466417.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464628/19466415.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
