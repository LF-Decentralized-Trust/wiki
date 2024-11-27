1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy DID Method Specification](Indy-DID-Method-Specification_19465516.html)
5. [Archive: 2020 DID Indy DID Method Specification Meeting Notes](19465518.html)

# Hyperledger Indy : 2020-11-17 Indy DID Method Specification Call

Created by Stephen Curran, last modified on Nov 17, 2020

# Summary

- Next steps on the &lt;network&gt; element of the DID
  
  - Third (or more) level names
  - How to find the nodes of the ledger given a DID with a &lt;network&gt;
  - Ramifications of finding previous versions of a DID by version-id or version-time

## Recording from the call: [20201117 Indy DID Method Spec Call Recording](#)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming community for all. For more information please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

## Welcome and Introductions

## Announcements

- TBD

## Attendees

- [Paul](https://lf-hyperledger.atlassian.net/wiki/people/6096f0170b80a600693aeaf3?ref=confluence)
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)

## Collaboration Channels

- Current hackmd [document](https://hackmd.io/@icZC4epNSnqBbYE0hJYseA/S1eUS2BQw)
- indy-did-method on RocketChat - [https://chat.hyperledger.org/channel/indy-did-method](https://chat.hyperledger.org/channel/indy-did-method)
- [indy-did-method](https://github.com/hyperledger/indy-did-method) repo
  
  - [ReSpec](https://github.com/transmute-industries/respec-github-pages) vs. [SpecUp](https://github.com/decentralized-identity/spec-up)

## Previous Discussion:

- ```
  The <network> element of the DID – did:indy:<network>:<id> will be an arbitrary string (see meeting notes from last meeting).
  ```
  
  ApproachDiscoverabilityDecentralized
  
  Naming(Limited)
  
  VerifiabilityHuman FriendlyConcisenessDependenciesHash of Domain Genesis FileNoYesYesNoYesRegistry or ConfigDomain NameYesYesNoYesNoDNSArbitrary NameNoNo
  
  (collision risk)NoYesMaybeRegistry or ConfigHash and Domain Name
  
  Alias, as in TrustBlocYes and NoYesYesYes and NoYes and NoDNS and ConfigArbitrary Name + HashNoYesYesYesNoRegistry or Config

<!--THE END-->

- The in-call discussion about the proposals:
  
  - Eliminated the DNS-based one as not desirable because of dependency on DNS
  - Eliminated the hash and DNS-based alias because of the complexity in using the two names for the identifier in signing scenarios, and the use of DNS.
  - Eliminated the hash only approach because of the lack of benefit of doing the hash vs. the downsides
    
    - The verifiability in using the hash is lost by using just 5 characters, but using a sufficient number makes the identifier too long
      
      - Micha generated a new Sovrin genesis file with a matching hash by varying only the alias name of one of the nodes in 30 minutes
      - Since we assume there will be in the low thousands of networks at the outside, the decentralization inherent in using the hash is not crucial
  - Eliminated the hash + arbitrary name because the hash is not providing additional value.
  - Leaving "Arbitrary Name" as the selected solution.

## Online Discussion (from RocketChat this week)

- Why we propose to go with the arbitrary name (summarized by Paul Bastian)
  
  - 1\. motivation to pick namespace collisions are not high,
  - 2\. chances for namespace collisions are not to be expected due to the expected numbers,
  - 3\. we should forbid selfdeclared DID ids and only allow selfcertyfing, generated DID ids that form a cryptographic barrier in case of an attacker collision,
  - 4\. hash solution does not solve the this either,
  - 5\. nobody wants DNS
- Why it's a bad idea ([Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence))
  
  - 1 if an attacker squats on a name space then that won’t remain true. That’s premised on the assumption that all actors are benevolent within the space.
  - 2 again has nothing to do with honest actors. They’ll easily work out how to avoid name space collision through implicit governance of the Indy sub namespace. It’s malicious actors who will cause the problems.
  - 3 agree but this doesn’t have anything to do with network identification and resolution
  - 4 if a cryptographic hash is used and not overly truncated it would. This is what pre-image resistance is about
  - 5 Then it would be wise of us to not create a human friendly network identifier because DNS has the architectural constraints on it due to their namespace also opting to use human friendly identifiers and being globally unique.
  - From the sounds of it though, people are convinced this is what they want so that’s the direction the method will go. I’m just trying to do my due diligence by calling out the tradeoffs that I’m seeing that don’t seem like they’re being considered from the discussions I’m seeing. If people are aware and still willing to accept the tradeoffs that’s fine because I raised the concern at least.

## Discussion:

- Action: Add to the spec that only self-certifying DIDs will be permitted, and must be enforced – not enforced on Indy today.
- Third level names for subsidiary ledgers – e.g. Sovrin Staging and Sovrin Builder net?
  
  - We should use ":", but that creates lots of colons. So example is did:indy:sovrin:staging:&lt;namespace-specific-id&gt;
    
    - We SHOULD NOT allow subnamespaces other than by the top namespace "owner"
    - Perhaps other rules?
  - [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence) mentioned in chat that "." is a valid character per the DID Spec. What about that?
    
    - ```
      did                = "did:" method-name ":" method-specific-id
method-name        = 1*method-char
method-char        = %x61-7A / DIGIT
method-specific-id = *( *idchar ":" ) 1*idchar
idchar             = ALPHA / DIGIT / "." / "-" / "_"
      ```
  - KERI: &lt;namespace-specific-id&gt; MAY have a "keri:" prefix for a future way of hosting a KERI identifier, example: did:indy:sovrin:staging:keri:&lt;keri\_id&gt;
- How to find the nodes of the network once the ledger is known?  Perhaps this sequence, but how do we want to represent that in the DID Method Spec.  Tentative idea – formally include at least the first, consider adding the second as well, and include informative text on the potential ways to go in the future.
  
  1. Config files,
  2. "human" gossiped names stored on the ledger - Daniel to produce a deck to explore the idea from nothing to networks
     
     1. Key pair - DID for the Indy DID Method for your network - "networks" - resolve the DID and you get the cross-registered list
        
        1. Extend to have the Trustee or Stewards DIDs be the ones to use for the "networks" elements of DIDDocs
        2. Must have a single hardcoded config file or way to resolve one DID (could use the universal resolver)
  3. decentralized registries
     
     1. Use of verifiable credentials - how can we use this to build this?
  4. protocol for cross-registration – how do you do this?
- How to find previous versions of DIDs and what are the implementation ramifications of that?
  
  - &lt;did&gt;?version-id=&lt;txnid&gt;
  - &lt;did&gt;?version-time=&lt;timestamp&gt;

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464418/19465552.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
