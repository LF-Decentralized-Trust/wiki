1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Aries Frameworks and User Groups](Aries-Frameworks-and-User-Groups_18481290.html)
4. [ACA-Pug - Aries Cloud Agent-Python User Group](ACA-Pug---Aries-Cloud-Agent-Python-User-Group_18484248.html)
5. [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html)
6. [ACA-Pug Meetings Archive 2022](ACA-Pug-Meetings-Archive-2022_18515844.html)

# Hyperledger Aries : 2022-08-09 Aries Cloud Agent - Python Users Group Community Meeting

Created by Stephen Curran, last modified on Aug 10, 2022

## Summary:

Topics:

- Recent Merges / Priorities
- Enabling OCA in ACA-Py
- Update on Ledger Agnostic AnonCreds in Aries / ACA-Py
- Q&amp;A

## Recordings from the call:

- Full Meeting: [dummyfile.txt](#)
- Extracted segments:
- Relevant Chat Bits: 
  
  - 08:17:43 From Timo Glastra : [https://github.com/hyperledger/aries-cloudagent-python/pull/1725#issuecomment-1097159274](https://github.com/hyperledger/aries-cloudagent-python/pull/1725#issuecomment-1097159274)
  - 08:38:15 From Kim Ebert : why wouldn't we send the OCA Bundle (or a pointer to it) with the credential at issuance or sharing
  - 08:39:11 From Daniel Bluhm : Would there be any indication on a ledger of the existence of the bundle on the resource server associated with a schema?
  - 08:42:43 From Daniel Bluhm : I'm assuming we'd need to do things like hashlinks to help ensure data resovled is data we intended to resolve
  - 08:46:13 From John Nathaniel Jr. : Must have a signature and a DID agreed.

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
- @ Kim Ebert &lt;kim@indicio.tech&gt;
- [Frostyfrog](https://lf-hyperledger.atlassian.net/wiki/people/557058:65c4fa44-5241-41cc-8835-455239d51ed7?ref=confluence)&lt;colton@indicio.tech&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence)(RootsID) &lt;lance.byrd@rootsid.com&gt;

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
  - Status of reaching full AIP 2.0
- Presentation and discussion on enabling OCA for Aries in general and in ACA-Py specifically
  
  - MRGs and OCA – how to link them
- Update on last week's discussion and ledger agnostic AnonCreds in Aries/ACA-Py:
  
  - How to enable object (DID and AnonCreds) resolution to improve ledger agnostic Aries protocols, and in particular, ledger-agnostic AnonCreds
    
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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18497970/18516594.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:26

[Atlassian](http://www.atlassian.com/)
