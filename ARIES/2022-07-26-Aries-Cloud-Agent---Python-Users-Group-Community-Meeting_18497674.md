1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-07-26 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified by Philippe Foucault on Jul 27, 2022

## Summary:

Topics:

- Recent Merges / Priorities
- Discussion: Getting to Ledger Agnostic DIDs and AnonCreds Objects
- Q&amp;A

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Extracted segments: Discussion on DIDs, DID Methods, AnonCreds Objects and Ledger Agnostic ACA-Py starts at 9:49 of the recording.
- Relevant Chat Bits:
  
  - 08:22:51 From Victor Martinez (SICPA) : [https://docs.godiddy.com/en/advanced/didcomm-interface](https://docs.godiddy.com/en/advanced/didcomm-interface)
  - 08:25:42 From Timo Glastra : We recently added a generic did resolver to AFJ. There is a spec from the identity foundation for a generic did registrar interface: [https://identity.foundation/did-registration/](https://identity.foundation/did-registration/)
  - 08:27:27 From Victor Martinez (SICPA) : [https://github.com/sicpa-dlab/aries-cloudagent-python/tree/feature/did-registrar](https://github.com/sicpa-dlab/aries-cloudagent-python/tree/feature/did-registrar)
  - 08:40:30 From Timo Glastra : Cheqd identifier example: did:cheqd:mainnet:6h7fjuw37gbf9ioty633bnd7thf65hs1/resources/f09c9296-6b39-4057-afff-dc2116fe746d
  - 08:42:39 From Timo Glastra : The appraoch we're taking for AFJ is creating a generic AnonCredsResourceService. You pass it an id and it resolves to the AnonCreds objects. The ID should be unique enough to determine the specific resource + define the resource provider (e.g. indy, cheqd, but could also be https).
  - 08:43:32 From Timo Glastra : Someone made a fabric integration in AFJ that swapped out the Indy ledger service for a fabric ledger service, and it kinda worked with the indy sdk out of the box
  - 08:45:13 From Timo Glastra : You can define it as a cred def / schema in your did document by adding a service:
  - 08:45:19 From Timo Glastra :
    
    - ```
      {
"id": "did:cheqd:mainnet:zF7rhDBfUt9d1gJPjx7s1JXfUY7oVWkY#non-fungible-image",
"type": "LinkedDomains"
"serviceEndpoint": "https://gateway.ipfs.io/ipfs/bafybeihetj2ng3d74k7t754atv2s5dk76pcqtvxls6dntef3xa6rax25xe",
}
      ```

```

```

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)(Indicio) &lt;sam@indicio.tech&gt;
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (Fullboar Creative / BC Gov) &lt;jason.leach@fullboar.ca&gt;
- [Sylvain Martel](https://lf-hyperledger.atlassian.net/wiki/people/712020:9eb55fb2-a220-4945-916a-6da7d1ed6101?ref=confluence) (Qc) &lt;sylvain.martel0@mcn.gouv.qc.ca&gt;
- [Char Howland](https://lf-hyperledger.atlassian.net/wiki/people/60998bf1dafdf00068e21bae?ref=confluence) (Indicio) &lt;char@indicio.tech&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;

## Announcements

## Deployments and Work Updates

- BC Gov Team
  
  - [Aries Cloud Agent Python](https://github.com/hyperledger/aries-cloudagent-python)
  - Aries Shared Components – [indy-vdr](https://github.com/hyperledger/indy-vdr), [indy-shared-rs](https://github.com/hyperledger/indy-shared-rs) and [aries-askar](https://github.com/hyperledger/aries-askar)
  - [Aries-VCR](https://github.com/bcgov/aries-vcr)/OrgBook BC Deployment
  - [Issuer Kit](https://github.com/bcgov/issuer-kit) - VCs for OIDC Issuer Service
  - [Aries Agent Test Harness](https://github.com/bcgov/aries-agent-test-harness) work - Results page: [https://aries-interop.info](https://aries-interop.info)
  - [Aries Mobile Test Harness](https://github.com/hyperledger/aries-mobile-test-harness)
  - BC Wallet – based on [Aries Framework JavaScript](https://github.com/hyperledger/aries-framework-javascript) and [Aries Bifold](https://github.com/hyperledger/aries-mobile-agent-react-native)
  - [Aries Endorser Service](https://github.com/bcgov/aries-endorser-service)
  - [Traction](https://github.com/bcgov/traction)

## Agenda

- Updates on merges and current PRs – priorities
  
  - Merges [Since 0.7.4](https://github.com/hyperledger/aries-cloudagent-python/pulls?q=is%3Apr%20is%3Amerged%20sort%3Aupdated%20merged%3A%3E2022-06-30)
  - [Open PRs](https://github.com/hyperledger/aries-cloudagent-python/pulls)
- Discussion: How to enable object (DID and AnonCreds) resolution to improve ledger agnostic Aries protocols, and in particular, ledger-agnostic AnonCreds
  
  - Topics:
    
    - DID Resolution:
      
      - State of DID Resolution in ACA-Py – local and external resolvers, regex to define if and how to resolve a DID.
        
        - External resolvers – http and didcomm interfaces available
      - Work happening now on did:peer to make it fit the interface
      - Working happening at SICPA on a DID Registrar based on the DIF Spec - Issue to be added to discuss/track
        
        - EBSI plugin being created (Ethereum based, DIDs only)
        - Plugins needed for did:sov, did:indy, did:peer, did:key ![(question)](images/icons/emoticons/help_16.png) and folks may be interested in adding more
      - Inconsistency in returned DIDDoc – suggests the need for a method in ACA-Py to "smooth out" the handling of DIDDocs - Issue to be added to request
    - AnonCreds Objects Handling
      
      - Currently tied to Indy – a "baseLedger" class with instances for Indy-SDK (indy-wallet storage only) and Indy VDR (indy-wallet or askar storage).
        
        - Handles writing as well, with Endorser handling.
      - Likely need to abstract to a similar, pluggable resolution and writing mechanisms - Issue(s) to be created.
        
        - Given an identifier in an AnonCreds object/context – resolve it.
        - Write AnonCreds objects using plugins to various target VDRs.
      - AFJ starting to talking about an AnonCredsResourceService

## Next Meeting

## Future Topics

## Action items

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18497674/18516532.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
