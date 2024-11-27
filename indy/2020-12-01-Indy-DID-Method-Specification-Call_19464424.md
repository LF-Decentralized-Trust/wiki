1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy DID Method Specification](Indy-DID-Method-Specification_19465516.html)
5. [Archive: 2020 DID Indy DID Method Specification Meeting Notes](19465518.html)

# Hyperledger Indy : 2020-12-01 Indy DID Method Specification Call

Created by Stephen Curran, last modified on Dec 01, 2020

# Summary

- Review: Discovery of networks
  
  - Given a DID, how to find it's network via gossiped ledger data
- Handling DIDs / DIDDocs using NYMs / ATTRIBs

## Recording from the call: [20201201 Indy DID Method Speciation Call Recording](#)

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
- [Markus Sabadello](https://lf-hyperledger.atlassian.net/wiki/people/557058:afd8f4c8-fc7f-49a9-9e6c-10b7f5414d6d?ref=confluence)
- [Dan Gisolfi](https://lf-hyperledger.atlassian.net/wiki/people/5efde33024882a0bb5fed1ae?ref=confluence)
- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)
- @Kamlesh Nagware
- [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence)

## Collaboration Channels

- Current hackmd [document](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw)
- indy-did-method on RocketChat - [https://chat.hyperledger.org/channel/indy-did-method](https://chat.hyperledger.org/channel/indy-did-method)
- [indy-did-method](https://github.com/hyperledger/indy-did-method) repo
  
  - [ReSpec](https://github.com/transmute-industries/respec-github-pages) vs. [SpecUp](https://github.com/decentralized-identity/spec-up)

## Previous Discussions:

- The specific will be specific that all DIDs MUST be self-certifying – e.g. derived from the initial public key used in the NYM
- We'll use ":" for subsidiary ledgers, and we'll include placeholder support for KERI, leading to 4 cases:
  
  - Ledger with no subsidiary name, example: `did:indy:sovrin:12345`
  - KERI identifier on a ledger with no subsidiary name, example: `did:indy:sovrin:keri:12345`
  - Ledger with subsidiary name, example: `did:indy:sovrin:staging:keri:12345`
  - KERI identifier on a ledger with a subsidiary name, example: `did:indy:sovrin:staging:keri:12345`
- To find networks we will require at least the first and perhaps the second of these approaches, while the rest are suggested:
  
  - Config files for one or more known networks
  - A mechanism for a ledger operator to register discovery information for other ledgers (aka "human gossip")
    
    - A DID/DIDDoc on a ledger will contain cross-registry information
    - A mechanism is needed for finding the DID(s) that contain the registrations – ideas have been put forward
  - Decentralized registries based on verifiable credentials
  - Other registry mechanisms, such as the DDNR proposal
- did:indy will support version-id using txnID and version-time by returning the object active as of that time
  
  - Code will be needed to be added to did-indy to support that

## Online Discussion (from RocketChat this week)

- Not on Rocketchat, but there was a note that no change to the DID Spec would be needed for resolving "did:indy:&lt;namespace&gt;" to return metadata about the ledger.
- A further suggestion could be made to find metadata about a ledger by resolving "did:indy:&lt;namespace&gt;:did:indy:&lt;cross-reg namespace&gt;" to return cross-register information
  
  - That DID would be resolved on the "did:indy:&lt;namespace&gt;" by using the namespace specific identifier "did:indy:&lt;cross-reg namespace&gt;"
  - TBD who that did is handled by the ledger to find the DIDDoc.
- Drummond to lead documenting this process in a new section of the HackMD.io doc

## Discussion:

- Review of last week:
  
  - See discussion below and highlight/make decisions
- This week: DIDs / DIDDocs and NYMs / ATTRIBs
  
  - Proposal from Paul Bastian – in hackmd.io document – "Alternative Version" section
  - Proposal from [Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)in the [HackMd.io](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw) document – [presentation](https://docs.google.com/presentation/d/1QkVHWiA8MMw3CyqacC4L_lePVEVLzEf-U13lw_TIRQ8/edit?usp=sharing)
  - Discussion summary:
    
    - No one likes the "don't change" Indy limitation – we'll have to change Indy to ensure consistency.
      
      - No on likes the possibility of inconsistent results from non-transactional (in the database sense) updates to separate ledger objects.
    - Desire is to have the NYM controller information in the DIDDoc either by the ledger verifying it is there or by injecting it during the writing or resolution.
      
      - This is for adherence to the DID Spec and for security – to make clear in the DIDDoc the controller rules.
      - If the DIDDoc has in it multiple signature requirements, does Indy enforce that? How would that merge with Indy permission rules (e.g. endorser+author to write object)
    - Need to make sure that an ATTRIB-less NYM continues to resolve to a DIDDoc – can't lose that.
      
      - Suggestion made that an ATTRIB-less NYM return a DIDDoc conforming to (or aligning with) the did:key specification.
    - Debate: Should a DIDDoc be assembled from just the ATTRIB, from the NYM+latest(ATTRIB) (could be a specific ATTRIB version) or from the NYM+set(ATTRIBs)?
      
      - General feeling is not just the ATTRIB – can't separate out the NYM controller information
      - My feeling is that assembling for a set of DIDDocs makes resolution more complex than necessary. For example, this requires rules about how to replace sections when merging ATTRIBs. Doable, but requires complexity that I think is unnecessary.
    - Debate: Does any assembly of the DIDDoc occur by the ledger, or does the ledger return the pieces to an external resolver that assembles the DIDDoc?

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

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464424/19465587.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
