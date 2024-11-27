1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy DID Method Specification](Indy-DID-Method-Specification_19465516.html)
5. [Archive: 2020 DID Indy DID Method Specification Meeting Notes](19465518.html)

# Hyperledger Indy : 2020-11-24 Indy DID Method Specification Call

Created by Stephen Curran, last modified by Markus Sabadello on Dec 01, 2020

# Summary

- Discovery of networks
  
  - Given a DID, how to find it's network via gossiped ledger data
- Versioning

## Recording from the call: [20201124 Indy DID Method Specification Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Announcements

- TBD

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)
- [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence)  (Laniakea Health) &lt;alex@[laniakeahealth.com](http://laniakeahealth.com)&gt;
- [Markus Sabadello](https://lf-hyperledger.atlassian.net/wiki/people/557058:afd8f4c8-fc7f-49a9-9e6c-10b7f5414d6d?ref=confluence)

## Collaboration Channels

- Current hackmd [document](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw)
- indy-did-method on RocketChat - [https://chat.hyperledger.org/channel/indy-did-method](https://chat.hyperledger.org/channel/indy-did-method)
- [indy-did-method](https://github.com/hyperledger/indy-did-method) repo
  
  - [ReSpec](https://github.com/transmute-industries/respec-github-pages) vs. [SpecUp](https://github.com/decentralized-identity/spec-up)

## Previous Discussion:

- The specific will be specific that all DIDs MUST be self-certifying – e.g. derived from the initial public key used in the NYM
- We'll use ":" for subsidiary ledgers, and we'll include placeholder support for KERI, leading to 4 cases:
  
  - Ledger with no subsidiary name, example: `did:indy:sovrin:12345`
  - KERI identifier on a ledger with no subsidiary name, example: `did:indy:sovrin:keri:12345`
  - Ledger with subsidiary name, example: `did:indy:sovrin:staging:keri:12345`
  - KERI identifier on a ledger with a subsidiary name, example: `did:indy:sovrin:staging:keri:12345`
- To find networks we will require at least the first and perhaps the second of these approaches, while the rest are suggested:
  
  - Config files for one or more known networks
  - A mechanism for a ledger operator to register discovery information for other ledgers (aka "human gossip")
  - Decentralized registries based on verifiable credentials
  - Other registry mechanisms, such as the DDNR proposal
    
    ```
    
    ```

## Online Discussion (from RocketChat this week)

- 
  

## Discussion:

- Discussion led by [Daniel Hardman](https://lf-hyperledger.atlassian.net/wiki/people/557058:d8f2338c-759d-4e0c-bb47-14386507f414?ref=confluence) about how to implement the gossiping mechanism via "networks" ledger DIDs -
  
  - Daniel Hardman [presentation](https://j.mp/36Zi7ij)
  - DID Namespace DID: [https://github.com/WebOfTrustInfo/rwot8-barcelona/blob/master/topics-and-advance-readings/did-namespace-records.md](https://github.com/WebOfTrustInfo/rwot8-barcelona/blob/master/topics-and-advance-readings/did-namespace-records.md)
- How to find config files in a centralized place?
  
  - ToIP, DIF, OrgBook for networks
  - Folder where the spec is – indy-did-method repo
- How to find previous versions of DIDs and what are the implementation ramifications of that?
  
  - &lt;did&gt;?version-id=&lt;txnid&gt;
    
    - Return the txnid as part of DID resolution so it can be included in URIs
  - &lt;did&gt;?version-time=&lt;timestamp&gt;
    
    - Indy does do timestamping - coarse:
      
      - tracked as part of consensus to (a) within 5 minutes (b) batch time greater than the last one
      - leader node picks, but vetted by other nodes, understanding that the leader node's time could drift.
    - How to do time based querying?
      
      - Probably not indexed
      - Could do binary search querying of the txnids
    - Code needs to be written to do this.

## Summary - Cross-Registering Networks on a Ledger

- Start with a config file for one or more networks
  
  - The config file will contain at least the pool transactions for the ledger – could contain more; see below
- On the ledger will be one or more DIDs that have associated "Network Metadata" information that includes (and might be limited to) information about cross-registered networks.
  
  - Proposed options for finding the "Network Metadata DID(s)" with the network listings:
    
    - A "network metadata" DID embedded in the config file.
      
      - Proposed that writing to the DID would be controlled, such as by a Trustee or some other config rules.
    - Could be found via resolving "known DIDs" so that knowledge of the "special" DID is not needed:
      
      - DIDs of each Trustee on the network (requires search by role)
      - DIDs of each Steward on the network (requires search by role)
      - A DID with a new "Network Metadata" role (requires search by role)
        
        - Same as putting the DID in the config file, but this enables finding it by role.
      - Resolving the "namespace DID" (e.g. DID with no ledger specific identifier). Requires change to DID Core Spec.
  - **Decision**: DID in Config File, Trustee DID, Steward DID, New Role DID, Namespace DID
    
    - **Impact**: What code needs to be written?
    - **Impact**: If trustee or steward DIDs – what processing rules should be applied?
- **Decision**: Does the network metadata go into an ATTRIB, or does it go into the DIDDoc associated with the DID?
- Data associated with the "Network Metadata" DID(s):
  
  - For cross-registered networks, an array:
    
    - Namespace
    - Pool Transactions file contents or
    - Location of Pool Transactions file
  - Metadata about the ledger
    
    - Link to Governance Framework information
    - Other?
  - **Decision**: What categories of data should go into a DID holding Network Metadata?
  - **Decision**: What is the exact format of the data?
- Centralized publishing of ledger config files
  
  - All the publishing of ledger config files in a known place – e.g. github – and under the control of an entity such as Hyperledger or DIF
    
    - This is centralized control because the maintainers accept the PRs that update the data
  - **Decision**: Do we want to propose a location to publish config files?
  - If yes, **Decision**: Where?

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464420/19465569.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
