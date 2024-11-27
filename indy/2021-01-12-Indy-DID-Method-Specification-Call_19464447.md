1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy DID Method Specification](Indy-DID-Method-Specification_19465516.html)
5. [Archive: 2021 DID Indy DID Method Specification Meeting Notes](19465622.html)

# Hyperledger Indy : 2021-01-12 Indy DID Method Specification Call

Created by Stephen Curran, last modified on Jan 12, 2021

# Summary

- ATTRIBs – cardinality, transformation, assembly – specific examples
- Spec. document structure

## Recording from the call: [20210112 Indy DID Method Specification Recording](#)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

## Welcome and Introductions

## Announcements

- Indy Node and Indy Plenum CI/CD process continuing – progress being made.

## Attendees

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)
- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)

## Collaboration Channels

- Current hackmd [document](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw)
- indy-did-method on RocketChat - [https://chat.hyperledger.org/channel/indy-did-method](https://chat.hyperledger.org/channel/indy-did-method)
- [indy-did-method](https://github.com/hyperledger/indy-did-method) repo: [ReSpec](https://github.com/transmute-industries/respec-github-pages) vs. [SpecUp](https://github.com/decentralized-identity/spec-up)

## Agreed Upon:

- See HackMD Document for most of what we have discussioned
- To find networks we will require at least the first and perhaps the second of these approaches, while the rest are suggested:
  
  - Config files for one or more known networks
  - A mechanism for a ledger operator to register discovery information for other ledgers (aka "human gossip")
    
    - A DID/DIDDoc on a ledger will contain cross-registry information
    - A mechanism is needed for finding the DID(s) that contain the registrations – ideas have been put forward - a DID Name Directory (DND) is the likely approach.
    - [Document](https://docs.google.com/document/d/1qLCaUiPtFZVNVUkAcLOhkPDPFs-ealTQmmy4HvYYhXQ/edit?usp=sharing) about the DND and DNR records
  - Decentralized registries based on verifiable credentials
  - Other registry mechanisms, such as the DDNR proposal
  - The DID Method Spec will include a reference to a repo (likely) "indy-did-networks" within Hyperledger that will be a lightly managed, structured repository of folders per Indy network with at least the config file(s) for the networks. Use of the repo is voluntary, but provides a convenient way for networks to publish information about the network. Maintainers will be selected from the community and should exhibit a light hand in accepting PRs, being concerned mainly with structure of the data (not content) and that contributors are not being malicious about updating the information of other network operators. The Hyperledger governance structure may be used for disputes as appropriate. This is not a replacement for the Governance that a specific network should implement.

## Online Discussion (from RocketChat this week)

- None

## This Week's Discussion:

### Review of previous decisions

- See "Agreed Upon" topics above.

### Continuing from the last discussion on transforming NYM and ATTRIB data to get the DIDDoc

- Status of HackMD Document – updated to reflect discussions made.
- Transformations:
  
  - NYM
  - "endpoint" – historical – such ATTRIBs are on the ledger now
  - Concepts agreed to:
    
    - Only the last value of an ATTRIB type should be merged into the document; each instance should be complete
      
      - We don't have to track streams of updates
      - We are less likely to get into an invalid state
    - For "endpoint" and "serviceEndpoint" – the last of either should be used.
    - The "serviceEndpoint" and other DID Core concepts are likely to be complete sections of the JSON
      
      - This means there is less of a chance of transforming the document
      - If all the sections are complete, is it worth breaking them up vs. having a single "DIDDoc" ATTRIB and merging into it the data from the NYM transaction?
- Controller discussion
  
  - Question: Should the ability to update a DID use current Indy rules (checking the NYM owner signature and if necessary an Endorser) or should the contents of the DIDDoc be used?
  - This generated a discussion of the trade-off in the changes needed to Indy vs. the need to enable DID Core capabilities and organizational use cases (e.g. a DID controlled by multiple people in an organization).
  - Idea:
    
    - Extend the NYM to include more complex DID Controller concepts – e.g. multiple verkeys and multiple signatures required for writes, including (perhaps) N of M requirements.
    - If we did this, the more complex NYM would have to be merged into the ATTRIB(s) that make up the DIDDoc
- Idea:
  
  - Instead of having multiple ATTRIBs assembled into a DIDDoc, use a version identifier to handle the transformation of the NYM+ATTRIB to make the DIDDoc to enable backwards compatibility
- Open question: While we want to merge the NYM into the DIDDoc, do we need to have multiple ATTRIBs assembled into a DIDDoc, or just one?

## Future Discussions:

- Request for [Markus Sabadello](https://lf-hyperledger.atlassian.net/wiki/people/557058:afd8f4c8-fc7f-49a9-9e6c-10b7f5414d6d?ref=confluence) to provide guidance on aligning the "NYM as controller" concept (above) with and the DID Core specifications concept of a controller.
- ATTRIB transformations to generate a DIDDoc
- DNR and DND discussions
- Structure for Indy specific objects returned as DIDs
  
  - What is the DID?
  - What is the DIDDoc format?
  - Existing objects – backwards compatibility
    
    - DID vs. DID URL – how could that be done?

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464447/19465653.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
