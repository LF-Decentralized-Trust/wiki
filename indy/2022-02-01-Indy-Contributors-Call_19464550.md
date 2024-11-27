1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2022 Meetings and Notes](2022-Meetings-and-Notes_19465927.html)

# Hyperledger Indy : 2022-02-01 Indy Contributors Call

Created by Stephen Curran, last modified on Feb 01, 2022

## Summary

- Status of indy-node CI/CD and the Ubuntu upgrade
- did:indy PRs
- Discussion Topic: did:indy resolution of non-DIDs – schema, etc.

## Recording of Call: [dummyfile.txt](#)

## Chat from Call:

- 08:10:56 From Daniel Bluhm : Link to the agenda: [https://lf-hyperledger.atlassian.net/wiki/display/indy/2022-02-01+Indy+Contributors+Call](https://lf-hyperledger.atlassian.net/wiki/display/indy/2022-02-01+Indy+Contributors+Call)
- 08:17:57 From Lynn Bendixsen : I think it might be because of key rootation...
- 08:21:55 From Markus Sabadello : "The meaning of colons in the method-specific-id is entirely method-specific. Colons might be used by DID methods for establishing hierarchically partitioned namespaces, for identifying specific instances or parts of the verifiable data registry, or for other purposes. Implementers are advised to avoid assuming any meanings or behaviors associated with a colon that are generically applicable to all DID methods. "
- 08:23:45 From Christian Bormann : [https://github.com/hyperledger/indy-did-method/issues/30](https://github.com/hyperledger/indy-did-method/issues/30)
- 08:24:49 From Paul Bastian : I like it
- 08:35:26 From Paul Bastian : I'm thinking if it makes sense to squash anoncreds/v1/&lt;object\_type&gt; to a single path like anoncredsv1\_NYM if you would evolve only certain objects to next generation
- 08:47:31 From Richard Esplin : Referencing a schema on another ledger seems like a bad practice and should be discouraged.
- 08:48:30 From Mirko Mollik - TrustCerts : I think ist really cool since you can treat it as the hosted one on [Schema.org](http://Schema.org)
- 08:49:17 From Richard Esplin : Until the schema changes unexpectedly. Sam Smith pointed out how it changes the attack surface of the solution.
- 08:49:34 From Sam Curren (TelegramSam) : we can require imutability?
- 08:49:54 From Richard Esplin : Then what is the value of it being somewhere else instead of working with a copy on your ledger?
- 08:50:11 From Mirko Mollik - TrustCerts : Correct, you depend on another ressource
- 08:50:23 From Richard Esplin : The approach of BBS+ to bundle the schema with the cred is the right solution.
- 08:50:51 From Mirko Mollik - TrustCerts : but if it is the trusted network of the Government, it can be treated as the Standard. E.g. for University Degrees.
- 08:51:08 From Sam Curren (TelegramSam) : it means it's the same object, and can be referred to by governance frameworks etc.
- 08:52:38 From Mirko Mollik - TrustCerts : Even when you make your Schema not immutable, you can reverence it with a Version time and a hash. We did this with JSON-LD schemas, addressing them with DIDs and a Version time and hash
- 08:53:21 From Sam Curren (TelegramSam) : Mirko it does require trust that it will consistently resolve.
- 08:57:34 From Dominic : I think weekly would be good
- 08:58:05 From Daniel Bluhm : Agreed, judging from how long it took to discuss issues today

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@[cloudcompass.ca](http://cloudcompass.ca)&gt;
- [Philipp Schlarb](https://lf-hyperledger.atlassian.net/wiki/people/712020:746f867b-3462-4658-8241-e74712f0cf6a?ref=confluence) (esatusAG) &lt;p.schlarb@[esatus.com](http://esatus.com)&gt;
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)(Indicio PBC) &lt;daniel@indicio.tech&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence)(Indicio PBC) &lt;colton@indicio.tech&gt;
- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)  (Bundesdruckerei) &lt;paul.bastian@bdr.de&gt;
- [Lynn Gray Bendixsen](https://lf-hyperledger.atlassian.net/wiki/people/618ec0fbe1b3e0006978ab61?ref=confluence)(Indicio PBC) &lt;lynn@indicio.tech&gt;
- [Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence) (Indicio PBC) &lt;adam@indicio.tech&gt;
- [Christian Bormann](https://lf-hyperledger.atlassian.net/wiki/people/712020:402bd53a-7b29-43cf-927d-955c323c7ed7?ref=confluence) (Robert Bosch GmbH) &lt;ChristianCarl.Bormann@de.bosch.com&gt;
- [Michael Schäfer](https://lf-hyperledger.atlassian.net/wiki/people/5fad776881b28800781eba81?ref=confluence) (Robert Bosch GmbH) &lt;Michael.Schaefer6@de.bosch.com&gt;
- [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence) (Neoteric Technologies Inc.) &lt;[wade@neoterictech.ca](mailto:wade@neoterictech.ca)&gt;
- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio PBC) &lt;char@indicio.tech&gt;

## Related Calls and Announcements

- Upcoming Indicio course on Indy Node development - this Thursday
  
  - URGENT: Finding "good first issues" on the Indy Node and Indy Plenum repos - please take a look!!
- AnonCreds standardization work has begun. Next meeting is by invite and then we'll have a charter and next steps.

## Release Status and Work Updates

- Indy Node
  
  - GitHub actions led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - Ubuntu 20.04 upgrade led by [Robin Klemens](https://lf-hyperledger.atlassian.net/wiki/people/5b068694a595df5d0a165a66?ref=confluence)
  - Sovrin Updates [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - New branching model led by [Wade Barnes](https://lf-hyperledger.atlassian.net/wiki/people/70121:166ee094-a2f2-44b4-adee-5c3da3741ff8?ref=confluence)
  - [indy-node-container](https://github.com/IDunion/indy-node-container/tree/main/controller) Crisitan Kubis ( [https://github.com/tsurai](https://github.com/tsurai) ), has created a Node Controller Container ([docs](https://github.com/IDunion/indy-node-container/tree/main/controller)), allows containerized indy nodes to participate in pool restart and upgrade
- Indy SDK
  
  - GitHub actions led by [Patrik Stas](https://lf-hyperledger.atlassian.net/wiki/people/557058:fb121afb-e6f9-4acf-beb7-91d5f2d988b7?ref=confluence)
- Indy Monitoring - [https://github.com/hyperledger/indy-node-monitor](https://github.com/hyperledger/indy-node-monitor)
- Indy/Aries Shared Libraries - Hyperledger (indy-vdr, indy-shared-rs, aries-askar)
- Ursa
- Hyperledger [Contribution Campaign](https://lf-hyperledger.atlassian.net/wiki/spaces/DR/pages/17170443/Contribution+Campaigns) ( [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) )
- Indy DID Method – [https://hyperledger.github.io/indy-did-method/](https://hyperledger.github.io/indy-did-method/)

## Meeting Topics

- Update on CI/CD Update and Ubuntu Upgrade: [Status Document](https://docs.google.com/document/d/1oBZSm-Ot8cu0Qcod3nhAzI3veEHIy4kJLBVnpO_nbiM/edit?usp=sharing)
  
  - Indy-Plenum Status: 
    
    - Done, 16.04, 20.04, Jenkins and GHA
  - Indy-Node Status:
    
    - Done, 16.04, 20.04, Jenkins and GHA
    - One 20.04 running in the IDUnion network of 16.04 nodes
    - Preparing and executing the automated release process.
  - indy-test-automation Status:
    
    - Circular dependency broken.
  - Developer tools
    
    - indy-node-container (move to Hyperledger in progress) and GitPod tools available (node and plenum)
    - On plenum – error with building the dev containers about Indy SDK version – need to get the metadata version correct ([https://github.com/hyperledger/indy-sdk/issues/2473](https://github.com/hyperledger/indy-sdk/issues/2473))
  - Indy-SDK build progress
    
    - Unblocked – builds are going and PRs are being reviewed (and rebasing PRs).
- ["did:indy" DID Method](https://hyperledger.github.io/indy-did-method/)
  
  - Pull Requests:
    
    - New method for self-certifying NYMs - [#27](https://github.com/hyperledger/indy-did-method/pull/27) - updated per discussion last meeting
      
      - Change to use SHA-256, but use the full public key as input
      - Decision: Go ahead and merge.
    - Proposal - change the separator for the sub-network from ":" to "." - [#31](https://github.com/hyperledger/indy-did-method/pull/31) 
      
      - Decision: No based on Markus's input in the comments: 
        
        - "The meaning of colons in the method-specific-id is entirely method-specific. Colons might be used by DID methods for establishing hierarchically partitioned namespaces, for identifying specific instances or parts of the verifiable data registry, or for other purposes. Implementers are advised to avoid assuming any meanings or behaviors associated with a colon that are generically applicable to all DID methods. "
    - Fix Typos - [#24](https://github.com/hyperledger/indy-did-method/pull/24) – Decision: go ahead and merge.
    - Newly Merged: Add the new Indy DID method to the W3C registry: [https://github.com/w3c/did-spec-registries](https://github.com/w3c/did-spec-registries) - [#393](https://github.com/w3c/did-spec-registries/pull/393)
  - Discussion topic - referencing non-DIDs via DID Indy and other DID Methods
    
    - Restricting the &lt;namespace&gt; part of the DID to lower case [#30](https://github.com/hyperledger/indy-did-method/issues/30) – yes!! Christian Bormann to PR
    - Issue raised to adjust the method: [#32](https://github.com/hyperledger/indy-did-method/pull/32) – agreed to use the revised approach – [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)to PR
      
      - Simple Issue: Change format from `<did>/<object-type>/<object-type-identifier>`, to `<did>/anoncreds/v1/<object-type>/<object-type-identifier>`
    - Related issues (raised in comment):
      
      - Is this the best approach from a DID Resolution perspective? – Response: this is good.
      - What object would we expect to get back from such a DID resolution? Presumably an object of the desired type, but should it be a DIDDoc with the object embedded?
        
        - Easy for did:indy, but for the broader use of AnonCreds, will this work with other DID Methods?
          
          - Response – good ahead for did:indy and as a part of the AnonCreds work, determine what else can be done.
      - Would other common DID Methods be able to support this? E.g. What other DID Methods are important for AnonCreds and could they support this approach?
        
        - Response – Leave this issue for the AnonCreds discussions.
  - Not Discussed:
    
    - Referencing (or not) the network of the DID in NYMs and in DIDDocContent put on the ledger - Issue [#33](https://github.com/hyperledger/indy-did-method/issues/23)
    - Verification of the self-certification of a DID - Issue [#23](https://github.com/hyperledger/indy-did-method/issues/23)
    - Issue: If Indy SDK is not updated, how do we run the Indy Node/Plenum tests?
      
      - Ideas are brewing on this...

## Future Calls

- Ideas for "Good First Task" for the Indicio class coming up in two weeks
- Issues that could impact indy-node on 20.04
  
  - indy-sdk: needs an upgrade to OpenSSL 1.1 to properly support Ubuntu 18.04/20.04.  For indy-node, just using indy-sdk as is.
  - Multiple libsodium versions could impact consensus – intermittent issue on a mixed network.
- **Plans for a new Indy-SDK release?**
  
  - A few people from the community have asked.
  - The most recent request has been for a release to include this feature; [https://github.com/hyperledger/indy-sdk/pull/2400](https://github.com/hyperledger/indy-sdk/pull/2400)

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
- Hyperledger campaign to recruit additional developers.

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464550/19465967.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
