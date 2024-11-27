1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy DID Method Specification](Indy-DID-Method-Specification_19465516.html)
5. [Archive: 2020 DID Indy DID Method Specification Meeting Notes](19465518.html)

# Hyperledger Indy : 2020-12-15 Indy DID Method Specification Call

Created by Stephen Curran, last modified on Dec 15, 2020

# Summary

- Unresolved question about Indy Network Discovery
- Demo - resolving with version-id and version-time
- NYMs/ATTRIBs and DIDs/DIDDocs

## Recording from the call: [20201215 Indy DID Method Specification Call](#)

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

## Collaboration Channels

- Current hackmd [document](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw)
- indy-did-method on RocketChat - [https://chat.hyperledger.org/channel/indy-did-method](https://chat.hyperledger.org/channel/indy-did-method)
- [indy-did-method](https://github.com/hyperledger/indy-did-method) repo
  
  - [ReSpec](https://github.com/transmute-industries/respec-github-pages) vs. [SpecUp](https://github.com/decentralized-identity/spec-up)

## Agreed Upon:

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
    - A mechanism is needed for finding the DID(s) that contain the registrations – ideas have been put forward - a DID Name Directory (DND) is the likely approach.
  - Decentralized registries based on verifiable credentials
  - Other registry mechanisms, such as the DDNR proposal
- **UPDATED**: did:indy will support version-id using seqNo and version-time by returning the object active as of the specified time according to the ledger time tracking
  
  - Code will likely be needed to be added to did-indy to support that
- **NEW**: For backwards compatibility, NYMs with no ATTRIBs and NYMs with Endpoint ATTRIBs, both of which are common on the Sovrin ledger today, will continue to be returned as DIDDocs, regardless of how we redefine a "DIDDoc" ATTRIB.
  
  - Currently, such a transformation is done by the Universal Resolver and it returns a certain format.
  - In future, the transformation for those use cases will be formalized in the DID Method and will be along the lines of the "did:key" approach (aligned of course with the DID Spec), where a number of uses for the DID key is defined vs. the current publication of just the key itself.
- **NEW**: The DID Method Spec will include a requirement that a DIDDoc will be returned as a transformation of ledger data regardless of how it is stored on the ledger.  There will always be a need to transform the the ledger data (if only because the DID Core Spec will evolve). To be determined where and how that transformation will occur.
- **NEW**: The DID Method Spec will include a reference to a repo (likely) "indy-did-networks" within Hyperledger that will be a lightly managed, structured repository of folders per Indy network with at least the config file(s) for the networks. Use of the repo is voluntary, but provides a convenient way for networks to publish information about the network. Maintainers will be selected from the community and should exhibit a light hand in accepting PRs, being concerned mainly with structure of the data (not content) and that contributors are not being malicious about updating the information of other network operators. The Hyperledger governance structure may be used for disputes as appropriate. This is not a replacement for the Governance that a specific network should implement.

## Online Discussion (from RocketChat this week)

- None

## This Week's Discussion:

### Unresolved question from the network Discovery process:

- Should we document in the DID Indy Method Spec. the centralized publishing of ledger config files?
  
  - All the publishing of ledger config files in a known place – e.g. github – and under the control of an entity such as Hyperledger or DIF
    
    - This is centralized control because the maintainers accept the PRs that update the data
  - **Decision**: Do we want to propose a location to publish config files? **DECISION: YES**
  - If yes, **Decision**: Where? **DECISION**: A Hyperledger repo – see new entry in the "[Agreed Upon](#id-2020-12-15IndyDIDMethodSpecificationCall-agreed_upon_)" section above.

### Demo - resolving with version-id and version-time

### From Dec. 1 Meeting about NYMs / ATTRIBs and DIDs / DIDDocs

Updates from this week are in bold. Strikethrough added where appropriate to previous text.

- DIDs / DIDDocs and NYMs / ATTRIBs - Discussion summary from last week:
  
  - **Answer**: No one likes the "don't change" Indy limitation – we'll have to change Indy to ensure consistency.
  - **Answer**: No on likes the possibility of inconsistent results from non-transactional (in the database sense) updates to separate ledger objects.
    
    - **DISCUSSION: Agreed that there WILL be a transformation of a NYM+ATTRIB, [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)to facilitate discussion next meeting about how to combine those two to produce a DIDDoc. We had general agreement that the ATTRIB will NOT contain the "complete" DIDDoc as originally proposed in the hackmd.io document.**
  - Desire is to have the NYM controller information in the DIDDoc either by the ledger verifying it is there or by injecting it during the writing or resolution.
    
    - Questions:
      
      - Should this be automatic (injected into the DIDDoc) or a MUST for the DID writer?
      - If automatic should it be on writing or resolution?
        
        - How would that impact signatures on transactions?
      - If the DIDDoc has in it multiple signature requirements, does Indy enforce that? How would that merge with Indy permission rules (e.g. endorser+author to write object)
    - **ANSWER**:
      
      - **Transformation will (likely – details to be discussed next meeting) be done to combine in some canonical way the NYM and ATTRIB data into a DIDDoc**
      - **It will be on resolution. Data will be written as today via NYM and ATTRIB transactions that can be read and verified ("source of truth") as needed from the ledger. DID resolution to transform the NYM and ATTRIB data will be an additional step.**
  - Need to make sure that an ATTRIB-less NYM continues to resolve to a DIDDoc – can't lose that.
    
    - Question: Should an ATTRIB-less NYM return a DIDDoc conforming to (or aligning with) the did:key specification?
    - **ANSWER**: **Decisions made that current ATTRIB-less NYMs and "endpoint ATTRIB"+NYM will return canonicalized DIDDocs via transformation, and that transformation will likely be structured in the style of "did:key", but up to date with the DID Core Spec.**
  - Question: Should a DIDDoc be assembled from just the ATTRIB, from the NYM+latest(ATTRIB) (could be a specific ATTRIB version) or from the NYM+set(ATTRIBs)?
    
    - **ANSWER: Assembled from NYM+ATTRIB (TBD – one ATTRIB or a collection of ATTRIBs?)**
  - Question: Does any assembly of the DIDDoc occur by the ledger, or does the ledger return the pieces to an external resolver that assembles the DIDDoc?
    
    - **ANSWER: Still pending... to be discussed further.**

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464433/19465619.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
