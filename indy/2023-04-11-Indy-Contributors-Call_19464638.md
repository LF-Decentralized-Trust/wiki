1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2023 Meetings and Notes](2023-Meetings-and-Notes_19466378.html)

# Hyperledger Indy : 2023-04-11 Indy Contributors Call

Created by Char Howland, last modified on Apr 11, 2023

## Summary

- Update on Sovrin Node pipeline
- Value of Indy
- Results of SSI tech stack survey: [Samuel Rinnetmäki](https://lf-hyperledger.atlassian.net/wiki/people/712020:b4cba51f-8e9c-44db-9269-a7d19161f716?ref=confluence)
- Indy Roadmap Discussion follow-ups: [https://hackmd.io/GeRP00i0Sj-7z4zXn2MB5g?view](https://hackmd.io/GeRP00i0Sj-7z4zXn2MB5g?view)
  
  - Scoping out top priority tasks

## Recording of Call: [Indy Contributors Call Recording](https://lf-hyperledger.atlassian.net/wiki/download/attachments/19464638/20230411%20-%20Indy%20Contributors%20Call%20Recording.mp4?version=1&modificationDate=1681257043135&api=v2)

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
- [Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio, PBC) &lt;kim@indicio.tech&gt;
- [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH) &lt;christiancarl.bormann@de.bosch.com&gt;
- [Samuel Rinnetmäki](https://lf-hyperledger.atlassian.net/wiki/people/712020:b4cba51f-8e9c-44db-9269-a7d19161f716?ref=confluence) (Findy Cooperative) &lt;samuel.rinnetmaki@findy.fi&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio, PBC) &lt;alex.walker@indicio.tech&gt;

## Related Calls and Announcements

- IIW: April 18-20

## Release Status and Work Updates

- Indy Node/plenum
- Indy-test-automation
- Indy-Node test-automation integration next step after cleaning up the dependencies issues and getting the sovrin-test-automation finished.
- Indy SDK
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy Node Container - [https://github.com/hyperledger/indy-node-container](https://github.com/hyperledger/indy-node-container)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)
- AnonCreds Specification: [https://anoncreds-wg.github.io/anoncreds-spec/](https://anoncreds-wg.github.io/anoncreds-spec/)

## Meeting Topics

- Sovrin Node build
  
  - Transition of indy-node from RC to final
- Value of Indy
- Results of Findynet's SSI tech stack survey: [Samuel Rinnetmäki](https://lf-hyperledger.atlassian.net/wiki/people/712020:b4cba51f-8e9c-44db-9269-a7d19161f716?ref=confluence) 
  
  - [Preliminary results overview (PDF)](https://findynet.sharepoint.com/:b:/s/FindyCollaboration/EcDuRB2PY3tOpYA4d1veu0YBB27DC-YqOv-i4HMKmTDtmA?e=t5h3ve), actual results will be published on Findynet's web site later (this week?)
- Indy Roadmap Discussion follow-ups: [https://hackmd.io/GeRP00i0Sj-7z4zXn2MB5g?view](https://hackmd.io/GeRP00i0Sj-7z4zXn2MB5g?view)
  
  - Scoping out top priority tasks
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464638/19466502.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
