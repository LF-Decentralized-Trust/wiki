1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy DID Method Specification](Indy-DID-Method-Specification_19465516.html)
5. [Archive: 2020 DID Indy DID Method Specification Meeting Notes](19465518.html)

# Hyperledger Indy : 2020-11-10 Indy DID Method Specification Call

Created by Stephen Curran, last modified on Nov 10, 2020

# Summary

- Update from DID F2F last week – resolutions?
- Continued: About the &lt;network&gt; element of the DID

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming community for all. For more information please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

## Recording from the call: [20201110 did indy Method Specification Call Recording](#)

## Welcome and Introductions

## Announcements

- TBD

## Collaboration Channels

- Current hackmd [document](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw)
- indy-did-method on RocketChat - [https://chat.hyperledger.org/channel/indy-did-method](https://chat.hyperledger.org/channel/indy-did-method)
- [indy-did-method](https://github.com/hyperledger/indy-did-method) repo
  
  - [ReSpec](https://github.com/transmute-industries/respec-github-pages) vs. [SpecUp](https://github.com/decentralized-identity/spec-up)

## Discussion

- Update from the recent W3C DID Core Face to Face sessions - [Brent Zundel](https://lf-hyperledger.atlassian.net/wiki/people/557058:bf590372-a52e-4c12-b1da-0c07b8b0a512?ref=confluence)
  
  - \`type\` will not be included in the spec, which impacts how we will store non-DID ledger objects (e.g. schema, etc.) as DIDs
  - JSON, JSON-LD and CBOR will all be supported in the spec., although DID Methods have the option of supporting some representations
    
    - This impacts the \`type\` issue in that we can solve the issue in just, say JSON-LD, and cover it in the other representations.
- ```
  The <network> element of the DID – did:indy:<network>:<id>
  ```
  
  - Proposals to start the meeting: 
    
    - Hash (did:indy:543F4:&lt;id&gt;) – unrecognizable, verifiable with the ledger, short, non-discoverable/requires a registry
    - Domain Name (did:indy:example.com:&lt;id&gt;) – recognizable, discoverable, not tied to the ledger, dependent on DNS
    - Arbitrary Name (did:indy:Sovrin:&lt;id&gt;) - recognizable, non-discoverable/requires a registry, not tied to the ledger
    - Hash plus an alias based on the domain name (this is what TrustBloc does)
    - Combination of arbitrary name and hash e.g. did:indy:sovrin:543F4:&lt;id&gt;
  
  ApproachDiscoverabilityDecentralized
  
  Naming(Limited)
  
  VerifiabilityHuman FriendlyConcisenessDependenciesHash of Domain Genesis FileNoYesYesNoYesRegistry or ConfigDomain NameYesYesNoYesNoDNSArbitrary NameNoNo
  
  (collision risk)NoYesMaybeRegistry or ConfigHash and Domain Name
  
  Alias, as in TrustBlocYes and NoYesYesYes and NoYes and NoDNS and ConfigArbitrary Name + HashNoYesYesYesNoRegistry or Config
  
- Online discussion after last week's meeting – about the value of the hash for verifiability and the risk of spoofing.
  
  - Purpose of the hash is not so much for verifiability as for decentralized naming – no risk of squatting on the same name as there would be with an arbitrary name.
  - Added the "Decentralized Naming" to the table above.

<!--THE END-->

- The in-call discussion about the proposals:
  
  - Eliminated the DNS-based one as not desirable because of dependency on DNS

<!--THE END-->

- - Eliminated the hash and DNS-based alias because of the complexity in using the two names for the identifier in signing scenarios, and the use of DNS.
  - Eliminated the hash only approach because of the lack of benefit of doing the hash vs. the downsides
    
    - The verifiability in using the hash is lost by using just 5 characters, but using a sufficient number makes the identifier too long
      
      - Micha generated a new Sovrin genesis file with a matching hash by varying only the alias name of one of the nodes in 30 minutes
      - Since we assume there will be in the low thousands of networks at the outside, the decentralization inherent in using the hash is not crucial
  - Eliminated the hash + arbitrary name because the hash is not providing additional value.
  - Leaving "Arbitrary Name" as the selected solution.

<!--THE END-->

- Next questions:
  
  - Third level names for subsidiary ledgers – e.g. Sovrin Staging and Sovrin Builder net?
  - How to find the nodes of the network once the ledger is known?  Config files, registries, gossiped names, etc.

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464414/19465542.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
