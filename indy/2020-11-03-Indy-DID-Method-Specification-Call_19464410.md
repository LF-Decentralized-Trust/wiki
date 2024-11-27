1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy DID Method Specification](Indy-DID-Method-Specification_19465516.html)
5. [Archive: 2020 DID Indy DID Method Specification Meeting Notes](19465518.html)

# Hyperledger Indy : 2020-11-03 Indy DID Method Specification Call

Created by Stephen Curran, last modified by Paul on Nov 17, 2020

# Summary

- Recap of IIW Discussion
- Collaboration Tools
- About the &lt;network&gt; element of the DID

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming community for all. For more information please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

## Recording from the call: [20201103 Indy DID Method Call Recording](#)

## Welcome and Introductions

## Announcements

- Status of relevant, unresolved issues in the DID Core Spec
  
  - A \`type\` attribute

## Discussion

- Recap of discussion at IIW
- Collaboration Tools:
  
  - Current hackmd [document](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw)
  - indy-did-method on RocketChat - [https://chat.hyperledger.org/channel/indy-did-method](https://chat.hyperledger.org/channel/indy-did-method)
  - [indy-did-method](https://github.com/hyperledger/indy-did-method) repo
    
    - [ReSpec](https://github.com/transmute-industries/respec-github-pages) vs. [SpecUp](https://github.com/decentralized-identity/spec-up)
- ```
  About the <network> element of the DID – did:indy:<network>:<id>
  ```
  
  - - What is the goal of the structure of the network?
      
      - Hash (543F4) – unrecognizable, verifiable with the ledger, short, non-discoverable/requires a registry
      - Domain Name (example.com) – recognizable, discoverable, not tied to the ledger, dependent on DNS
      - Arbitrary Name (SovrinStaging) - recognizable, non-discoverable/requires a registry, not tied to the ledger
      - Combination of hash and domain name (this is what TrustBloc does)
      - Combination of arbitrary name and hash &lt;arbname&gt;:&lt;hash&gt;  e.g. did:indy:sovrin:&lt;hash&gt;:&lt;id&gt;
  
  ApproachDiscoverabilityDecentralized
  
  Control(Limited)
  
  VerifiabilityHuman FriendlyConcisenessDependenciesHash of Domain Genesis FileNoYesYesNoYesRegistry or ConfigDomain NameYesYesNoYesNoDNSArbitrary NameNoYesNoYesNoRegistry or ConfigHash and Domain Name
  
  Alias, as in TrustBlocYes and NoYesYesYes and NoYes and NoDNS and ConfigArbitrary Name + HashNoYesYesYesNoRegistry or Config
  
  - - What is the easiest way for agents to use this?
      
      - DNS is a hard sell per [Dan Gisolfi](https://lf-hyperledger.atlassian.net/wiki/people/5efde33024882a0bb5fed1ae?ref=confluence)
      - A registry implies centralization - e.g. GitHub, DIF, ToIP
      - Today it will be just a manual list of name - config files
      - Does readability matter?   Who sees a DID?
        
        - Should be no one.  "If anyone sees a DID, we've failed at our job" - quote from RWoT

Discussion ended here.  The following was not discussed in detail

- First 5 characters of a hash – of what?
  
  - Genesis File
    
    - What Genesis File?  [Domain](https://github.com/sovrin-foundation/sovrin/blob/master/sovrin/domain_transactions_live_genesis) (does not change - first n transactions on the ledger), [Pool](https://github.com/sovrin-foundation/sovrin/blob/master/sovrin/pool_transactions_live_genesis) (does change - inevitable as it contains IP:port of nodes)
      
      - Proposal: Use the Domain Genesis File hash
      - Pool file is required to contact nodes of the network.
      - If Domain, what to do if there is a fork?
        
        - Proposal: Domain Genesis file contains the first n records after the fork, as the sequence number is the same
- Should an "alias" be allowed as TrustBloc uses?
  
  - From Troy Ronda: A quick update on our did:trustbloc handling of multiple networks. With the ability to specify a canonical DID in the DID document, we are adding the ability to have both discoverable domains in the DID - e.g., did:trustbloc:domain:suffix and also to have a stable consortium genesis identifier - e.g., did:trustbloc:&lt;consortium genesis hash&gt;:suffix. The canonical DID would become the &lt;consortium genesis hash&gt; version such that the resolution of discoverable domain DIDs would point to this canonical DID in the resolution result.
  - TrustBloc alias example:
    
    - did:trustbloc:testnet.trustbloc.dev:s3did12345
    - [https://testnet.trustbloc.dev/.well-known/did-trustbloc/org1.sandbox.trustbloc.dev.json](https://testnet.trustbloc.dev/.well-known/did-trustbloc/org1.sandbox.trustbloc.dev.json)
      
      - Configuration file – equivalent to the Indy Pool Genesis File
  - So Indy might use: 
    
    - &lt;domain&gt; alias is :example.com, [https://example.com/.well\_known/did-indy](https://example.com/.well_known/indy)/ ??
      
      - Perhaps a folder with current ledger pool genesis file (to find the ledger) and ledger domain genesis file (to find/check the hash)
- If the DID to be resolved is NOT using an alias, how is the Pool Genesis File found?
  
  - Known by all that need to know it?
  - Registry? GitHub?

#### Attendees: [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) [Alexander Jonsson](https://lf-hyperledger.atlassian.net/wiki/people/557058:e785bcce-e136-4074-8df6-ea773557fcb0?ref=confluence) [Kumaravel N](https://lf-hyperledger.atlassian.net/wiki/people/70121:1d7790e2-8efd-409a-bf1e-ff3f8c520669?ref=confluence) [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464410/19465531.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
