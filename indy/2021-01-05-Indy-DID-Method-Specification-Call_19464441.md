1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy DID Method Specification](Indy-DID-Method-Specification_19465516.html)
5. [Archive: 2021 DID Indy DID Method Specification Meeting Notes](19465622.html)

# Hyperledger Indy : 2021-01-05 Indy DID Method Specification Call

Created by Stephen Curran, last modified by Paul on Jan 12, 2021

# Summary

- Review of decisions to date
- Discussion (led by [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)) about transforming NYM and ATTRIB data into a DIDDoc
  
  - What goes into the ATTRIB and how does it manifest in the DIDDoc?

## Recording from the call: [20210105 Indy DID Method Specification Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Announcements

- BC Gov Open Source Bounty ($60k CDN) to add W3C Standard Verifiable Credentials with ZKP and Selective Disclosure to ACA-Py. Applications accepted through Friday [here](https://digital.gov.bc.ca/marketplace/opportunities/code-with-us/3f9f0e86-b8bf-47ee-9f3d-5b272f9ec845).

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
- [Dan Gisolfi](https://lf-hyperledger.atlassian.net/wiki/people/5efde33024882a0bb5fed1ae?ref=confluence)
- [Markus Sabadello](https://lf-hyperledger.atlassian.net/wiki/people/557058:afd8f4c8-fc7f-49a9-9e6c-10b7f5414d6d?ref=confluence)
- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)

## Collaboration Channels

- Current hackmd [document](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw)
- indy-did-method on RocketChat - [https://chat.hyperledger.org/channel/indy-did-method](https://chat.hyperledger.org/channel/indy-did-method)
- [indy-did-method](https://github.com/hyperledger/indy-did-method) repo: [ReSpec](https://github.com/transmute-industries/respec-github-pages) vs. [SpecUp](https://github.com/decentralized-identity/spec-up)

## Agreed Upon:

- The specific will be specific that all DIDs MUST be self-certifying – e.g. derived from the initial public key used in the NYM
- We'll use ":" for subsidiary ledgers, and we'll include placeholder support for KERI, leading to 4 cases:
  
  - Ledger with no subsidiary name, example: `did:indy:sovrin:12345`
  - KERI identifier on a ledger with no subsidiary name, example: `did:indy:sovrin:keri:12345`
  - Ledger with subsidiary name, example: `did:indy:sovrin:staging:12345`
  - KERI identifier on a ledger with a subsidiary name, example: `did:indy:sovrin:staging:keri:12345`
- To find networks we will require at least the first and perhaps the second of these approaches, while the rest are suggested:
  
  - Config files for one or more known networks
  - A mechanism for a ledger operator to register discovery information for other ledgers (aka "human gossip")
    
    - A DID/DIDDoc on a ledger will contain cross-registry information
    - A mechanism is needed for finding the DID(s) that contain the registrations – ideas have been put forward - a DID Name Directory (DND) is the likely approach.
    - [Document](https://docs.google.com/document/d/1qLCaUiPtFZVNVUkAcLOhkPDPFs-ealTQmmy4HvYYhXQ/edit?usp=sharing) about the DND and DNR records
  - Decentralized registries based on verifiable credentials
  - Other registry mechanisms, such as the DDNR proposal
- did:indy will support version-id using seqNo and version-time by returning the object active as of the specified time according to the ledger time tracking
  
  - Code will likely be needed to be added to did-indy to support that
- For backwards compatibility, NYMs with no ATTRIBs and NYMs with Endpoint ATTRIBs, both of which are common on the Sovrin ledger today, will continue to be returned as DIDDocs, regardless of how we redefine a "DIDDoc" ATTRIB.
  
  - Currently, such a transformation is done by the Universal Resolver and it returns a certain format.
  - In future, the transformation for those use cases will be formalized in the DID Method and will be along the lines of the "did:key" approach (aligned of course with the DID Spec), where a number of uses for the DID key is defined vs. the current publication of just the key itself.
- The DID Method Spec will include a requirement that a DIDDoc will be returned as a transformation of ledger data regardless of how it is stored on the ledger.  There will always be a need to transform the the ledger data (if only because the DID Core Spec will evolve). To be determined where and how that transformation will occur.
- The DID Method Spec will include a reference to a repo (likely) "indy-did-networks" within Hyperledger that will be a lightly managed, structured repository of folders per Indy network with at least the config file(s) for the networks. Use of the repo is voluntary, but provides a convenient way for networks to publish information about the network. Maintainers will be selected from the community and should exhibit a light hand in accepting PRs, being concerned mainly with structure of the data (not content) and that contributors are not being malicious about updating the information of other network operators. The Hyperledger governance structure may be used for disputes as appropriate. This is not a replacement for the Governance that a specific network should implement.

## Online Discussion (from RocketChat this week)

- None

## This Week's Discussion:

### Review of previous decisions

- See "Agreed Upon" topics above.

### Continuing from the last discussion on transforming NYM and ATTRIB data to get the DIDDoc

- Last meeting we talked about the easy cases:
  
  - NYM and no ATTRIB
  - NYM and ATTRIB only with an "endpoint" URL.
- What about more interesting cases? [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)to facilitate the discussion.
  
  - See notes at the end of the HackMD Document
  - Do we do validation checking on the known ATTRIB raw types? yes - where possible
  - Where does the DIDDoc construction occur? Must happen on the ledger.

## Future Discussions:

- DNR and DND discussions
- DIDDocs:
  
  - What is the structure of the DIDDoc template - core and extensions?
- Structure for Indy specific objects returned as DIDs
  
  - What is the DID?
  - What is the DIDDoc format?
  - Existing objects – backwards compatibility
    
    - DID vs. DID URL – how could that be done?

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464441/19465646.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
