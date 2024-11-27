1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy DID Method Specification](Indy-DID-Method-Specification_19465516.html)
5. [Archive: 2020 DID Indy DID Method Specification Meeting Notes](19465518.html)

# Hyperledger Indy : 2020-12-08 Indy DID Method Specification Call

Created by Stephen Curran, last modified on Dec 08, 2020

# Summary

- Review: Discovery of networks
  
  - Given a DID, how to find it's network via gossiped ledger data

## Recording from the call: [20201208 Indy DID Method Call Recording](#)

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
- [Dan Gisolfi](https://lf-hyperledger.atlassian.net/wiki/people/5efde33024882a0bb5fed1ae?ref=confluence)
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
- did:indy will support version-id using txnID and version-time by returning the object active as of that time
  
  - Code will be needed to be added to did-indy to support that

## Online Discussion (from RocketChat this week)

## This Week's Discussion:

This week we talked about using "namespace DIDs" to discovery other networks starting from one you know. Specifically, we discussed Drummond's proposal in this [document](https://docs.google.com/document/d/1qLCaUiPtFZVNVUkAcLOhkPDPFs-ealTQmmy4HvYYhXQ/edit?usp=sharing).  Here is how we revised the questions we had previously – knocking out a number of contenders and focusing on how we can achieve cross registration of networks. 

Read the full [document](https://docs.google.com/document/d/1qLCaUiPtFZVNVUkAcLOhkPDPFs-ealTQmmy4HvYYhXQ/edit?usp=sharing), but here is a TL;DR version:

- Registration:
  
  - Network A and B are set up
  - Network B Authorities (people) ask Network A Authorities to cross register Network B
  - Network A Authorities do some due diligence on Network B, agrees and updates their "DID Network Directory" config ledger record to include information from Network B
  - Ideally – Network A Authorities also asks Network B Authorities to do the same to establish transitive trust.
- Lazy Discovery:
  
  - Alice's agent knows about Indy Network A
  - In processing a document (e.g. a DIDDoc or a VC) discovers a DID reference to Indy Network B
  - Alice's agent resolves on Network A the DID: "did:indy:a:dnr:did:indy:b", getting back a DIDDoc with configuration information about Network B (assuming Network A knows about B)
  - Alice connects to Network B resolves the DID on Network B
- Proactive Discovery:
  
  - Acme's agent knows about Indy Network A and wants to find all the networks that Network A has registered.
  - Acme's agent resolves the DID "did:indy:a:dnd" and gets back a DIDDoc with a list of the cross registered networks published by Network A
  - Acme's agent goes through the list and resolves the "dnr" DID for each network (see Alice example above).
  - Acme's agent may do the same operations recursively across all the newly discovered networks until all connected networks have been found.
- Specs and Standards:
  
  - The idea of resolving "dnd" and "dnr" DIDs and the data model of the "dnd" DIDDoc can be a standard across all DID networks.
  - The data model for the "dnr" DIDDocs is specific to the DID Method of the registered network. For example, for an Indy network, the contents will (likely) be a "pool genesis file"

Unresolved question from two weeks ago:

- Should we do centralized publishing of ledger config files?
  
  - All the publishing of ledger config files in a known place – e.g. github – and under the control of an entity such as Hyperledger or DIF
    
    - This is centralized control because the maintainers accept the PRs that update the data
  - **Decision**: Do we want to propose a location to publish config files?
  - If yes, **Decision**: Where?

## From Dec. 1 Meeting about NYMs / ATTRIBs and DIDs / DIDDocs

- DIDs / DIDDocs and NYMs / ATTRIBs - Discussion summary from last week:
  
  - No one likes the "don't change" Indy limitation – we'll have to change Indy to ensure consistency.
  - No on likes the possibility of inconsistent results from non-transactional (in the database sense) updates to separate ledger objects.
  - Desire is to have the NYM controller information in the DIDDoc either by the ledger verifying it is there or by injecting it during the writing or resolution.
    
    - **Questions**:
      
      - Should this be automatic (injected into the DIDDoc) or a MUST for the DID writer?
      - If automatic should it be on writing or resolution?
        
        - How would that impact signatures on transactions?
      - If the DIDDoc has in it multiple signature requirements, does Indy enforce that? How would that merge with Indy permission rules (e.g. endorser+author to write object)
  - Need to make sure that an ATTRIB-less NYM continues to resolve to a DIDDoc – can't lose that.
    
    - **Decision**: Should an ATTRIB-less NYM return a DIDDoc conforming to (or aligning with) the did:key specification?
  - **Decision**: Should a DIDDoc be assembled from just the ATTRIB, from the NYM+latest(ATTRIB) (could be a specific ATTRIB version) or from the NYM+set(ATTRIBs)?
    
    - General feeling is not just the ATTRIB – can't separate out the NYM controller information 
      
      - My feeling is that assembling for a set of DIDDocs makes resolution more complex than necessary. For example, this requires rules about how to replace sections when merging ATTRIBs. Doable, but requires complexity that I think is unnecessary.
  - **Decision**: Does any assembly of the DIDDoc occur by the ledger, or does the ledger return the pieces to an external resolver that assembles the DIDDoc?

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464426/19465598.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
