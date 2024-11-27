1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-12-06 Indy Contributors Call

Created by Stephen Curran, last modified by Char Howland on Dec 07, 2022

## Summary

- Update on Sovrin Node pipeline
- Steps in eliminating the Indy SDK
- Transition of indy-node from RC to final
- Question from Lynn: Will the did-method work be included in the 20.04 upgrade?
- Open Discussion

## Recording of Call: [20221206 Indy Contributors Call Recording](https://lf-hyperledger.atlassian.net/wiki/download/attachments/19464617/20221206%20-%20Indy%20Contributors%20Call%20Recording.mp4?version=1&modificationDate=1670350932326&api=v2)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (BC Gov/Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

[Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio, PBC) &lt;char@indicio.tech&gt;

[Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatus AG) &lt;p.schlarb@esatus.com&gt;

[Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (BC Gov / Neoteric Technologies Inc.) &lt;wade@neoterictech.ca&gt;

[Kim Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5f7247c98d88b30075da15a3?ref=confluence) (Indicio, PBC) &lt;kim@indicio.tech&gt;

## Related Calls and Announcements

- BC Gov (likely) to post funded opportunities around the migration from the Indy SDK to the Indy/Aries Shared Components (Indy VDR, Askar, etc.)
  
  - To be posted on this site: [https://marketplace.digital.gov.bc.ca/opportunities](https://marketplace.digital.gov.bc.ca/opportunities) as "Code With Us" opportunities.
  - Announcements will be made on Discord.

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
  
  - indy-test-automation consistent failing some tests.
  - call of indy-test-automation from sovrin via json encoded variable inputs (atm still hardcoded in sovrin GHA defintion, working on the parametrization and information extraction)
  - specific version problems with fpm
- Steps in eliminating the Indy SDK
  
  - Investigating different paths for the Indy CLI
  - Working on a repo using Python to recreate the Indy CLI
  - Creating a HIPE
- Transition of indy-node from RC to final
  
  - Lots of blockers getting the environment set up to, moving forward towards branch comparisons
  - VSCode Dev Containers and GitPod on the 20.04 upgrade branch
- Question from Lynn: Will the did-method work be included in the 20.04 upgrade?
  
  - Yes, the Indy DID method work is already on the 20.04 upgrade branch
  - Only outstanding item: required work on the Indy-VDR side that hasn’t been merged into the main branch yet
  - Indy VDR and Indy node 20.04 releases can be separate
    
    - However, if using Indy-VDR and the Indy DID method, need to upgrade
- Using indy-node-container for the indy-vdr tests
  
  - Draft PR from Christian: [https://github.com/hyperledger/indy-vdr/pull/112](https://github.com/hyperledger/indy-vdr/pull/112) gated by [https://github.com/hyperledger/indy-node-container/pull/121](https://github.com/hyperledger/indy-node-container/pull/121)  (ready to merge needs branch protection updates in indy-node-container)
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464617/19466351.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
