1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-09-09 Indy Contributors Call

Created by Richard Esplin, last modified on Sep 11, 2019

## Summary

- Move PostgreSQL wallet storage out of experimental state when the wallet is moved to Aries
- Start cross-organization PR reviews after PBFT View Change is shipped, as an experiment
- We want to move quickly with the Indy / Aries split and avoid long term maintenance of Indy SDK if possible.
- Incomplete request format refactor
- Trade-offs of new pack/unpack versus msgpack

## Timezone: US morning and Europe afternoon

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- Name (organization) &lt;email&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass/BC Gov) &lt;swcurran@cloudcompass.ca&gt;
- [Ken Ebert](https://lf-hyperledger.atlassian.net/wiki/people/70121:2cc4df0e-16de-40dc-ba52-09649099759a?ref=confluence) (Sovrin Foundation) &lt;ken@sovrin.org&gt;
- [Arjan van Eersel](https://lf-hyperledger.atlassian.net/wiki/people/712020:23c27cf6-adfa-4521-a2cd-1badf30806b5?ref=confluence) (Sonemas) &lt;arjan@sonemas.com&gt;
- [Sam Smith](https://lf-hyperledger.atlassian.net/wiki/people/70121:d328bb58-9406-4363-8440-41dfb6b21ee8?ref=confluence) (ProSapien &lt;sam@samuelsmith.org&gt;
- [Alexander Sherbakov](https://lf-hyperledger.atlassian.net/wiki/people/557058:a955b109-9f8c-405c-9f96-0903d4de8c46?ref=confluence) (Evernym) &lt;alexander.shcherbakov@evernym.com&gt;
- [Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence) (Sovrin Foundation) &lt;adam@sovrin.org&gt;

Announcements

- Hyperledger Maintainers Conference: Minneapolis in October.
- Bootcamp Russia: [Event Location](https://lf-hyperledger.atlassian.net/wiki/spaces/RU/pages/22315033/Event+Location)
- IIW

## Summary of Prior Call

## Release Status

- Indy Node
  
  - August: 1.9.2
    
    - Bug fix release
    - Important bug fix for ledger corruption INDY-2211
      
      - Recovery complicated by [https://sovrin.atlassian.net/browse/SN-7](https://sovrin.atlassian.net/browse/SN-7)
  - September: 1.10.0
    
    - PBFT view change
    - Indy Node and Indy Plenum support for Ubuntu 18.04
- Indy SDK
  
  - August: 1.11.1
    
    - Finish Authors vs Endorsers
    - Finish proof of possession of payment address
    - Platform Updates: Ubuntu 18.04
  - September: 1.12.0
    
    - Fully qualified DIDs
      
      - Dependent on DIDDoc support? (Daniel's document and David Huseby's work)
    - Platform Updates: MacOS, CentOS
  - Future
    
    - GitLab migration alongside Jenkins (Foundation)?
    - Aries / Indy split
    - Anoncreds 2.0 (Sovrin Foundation, BC.gov?)
- Ursa
  
  - Working on release of 0.2.0 (September / October)
    
    - ZKP  / ZKLang improvements
    - Debian packages
    - Refactor internal plumbing for anoncreds 2.0, shouldn't impact external interfaces
    - Refactor multi-signature BLS in addition to aggregated signature
- Aries
  
  - Lots of progress on language libraries, frameworks, and agents.
- Indy Catalyst
  
  - Production deployment testing: volume loads.
  - Won't go live in production at BC.gov until October.
  - Not yet migrated to Hyperledger. Needs more documentation.

## Work Updates

- Documentation improvements: Michael B and Stephen C
  
  - Need to review and prune out-of-date documentation (Alice / Faber treatment of pairwise DIDs is a key pain point)
  - Michael is working on Indy Agent walkthrough using C#
  - Finishing work on ReadTheDocs (2 more weeks?)
  - Cloud Compass is building the Linux Foundation EdX courses for Indy and Aries
- SDK 2.0 architecture / Indy-Aries split (Sergey)
  
  - Anxious to start moving, and iterating.
- GitLab migration (Mike and Steve G)
  
  - Demos in the Identity Implementers WG calls
  - Issues with Jenkins machines because Rust builds run out of memory—workaround increased build time but is a temporary solution
- Advanced Schemas and W3C creds (Ken)
  
  - Can successfully write and retrieve the Context object from the node code. Will track through all layers up to Aries.
    
    - [https://github.com/ken-ebert/indy-node/commits/master](https://github.com/ken-ebert/indy-node/commits/master)
  - 5 additional objects need to be added.
  - Working on the HIPE for the new Schema object.
- Warnings from rust cargo clippy (Mike and Axel)
  
  - IS-1270 through IS-1274
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Would be useful to have a comparison in performance between Anoncreds 1.0 and Anoncreds 2.0
  - First draft is latex document in Ursa repo. Will be published as PDF and HTML.
    
    - [https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2](https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2)
  - Need a plan for changes to Indy Node
    
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)
- Getting Ursa artifacts published that can be used by Indy Node and Indy SDK (Mike and Cam)

## Other Business

- PostgreSQL leaving experimental status ([see previous discussion](2019-08-26-Indy-Maintainers-Call_19464297.html))
  
  - Would like to update existing issues first.
  - Ian will be going on vacation.
  - Kiva is interested in helping.
  - Want to see this happen this year, but maybe wait for the Aries Wallet repo? (Kiva prefers to do it in Aries.)
- Maintainership requirements for Indy Node and Indy SDK
  
  - Don't worry about new maintainers for Indy SDK now, wait for Aries decisions.
  - Need for cross organizational review.
    
    - Should define the process, including how we handle exceptions (emergency fixes shouldn't be blocked, but would require notification)
    - After PBFT view change (middle of October).
    - Ken and Cam can do the reviews of Evernym work.
    - For now, Alex will continue reviewing everything.
    - Alex should train other reviewers on how to do good reviews.
- How long should we maintain Indy SDK after we start work on Aries core libraries?
  
  - Will need to understand the Aries plan first.
- Partially completed refactoring of the Request format: INDY-1375 and IS-567
  
  - Completed the new format for transactions, and designed the new format for requests, but didn't implement it.
  - [https://github.com/hyperledger/indy-node/blob/master/docs/source/requests-new.md](https://github.com/hyperledger/indy-node/blob/master/docs/source/requests-new.md)
- New pack / unpack requires disclosure of recipient
  
  - Cannot hide the receiver of the message like we could with msg\_pack
  - Allows having multiple recipients of the same message
  - Should list the drawback in the Aries-RFC? Is there an alternative way that preserves the capability to selectively disclose the recipient?
    
    - [https://github.com/hyperledger/aries-rfcs/tree/master/features/0019-encryption-envelope](https://github.com/hyperledger/aries-rfcs/tree/master/features/0019-encryption-envelope)
  - From [Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)
    
    msg\_pack presents problems when dealing with an agent that maintains more than one relationship. For example, if I receive a message, I don't know which key in my agent I should be using to decrypt the message. We can get sender anonymity or receiver anonymity, but I don't believe it's possible to get both and still determine who the message is for.
  - Pack/unpack only exposes the Verkey of the recipients. It does not do forward secrecy.

## Future Calls

- Define pull request review process for Indy Node.
  
  - Should define the process, including how we handle exceptions (emergency fixes shouldn't be blocked, but would require notification)
  - What is important in a good review?
- Fully Qualified DID support in Indy SDK
- fuzzing libindy [https://github.com/AxelNennker/indy-sdk/tree/fuzzing/](https://github.com/AxelNennker/indy-sdk/tree/fuzzing/)
  
  \`cargo +nightly fuzz run fuzz\_target\_1 -- -only\_ascii=1\`
  
  Worried about unsafe code in libindy
  
  \`\`\`
  
  ignisvulpis@namenlos:~/development/hyperledger/indy-sdk/libindy$ find src -name \\\*\\.rs -exec fgrep unsafe {} \\; | wc -l
  
  61
  
  \`\`\`
- Ursa and AMCL:  Discussed in the Ursa call (August 21), but no decision yet.
- Architecture questions for Indy SDK:
  
  ![](plugins/servlet/confluence/placeholder/unknown-macro)
- How to handle old pull requests that failed DCO Checks? Close?
- How to handle pull requests for IOS / Swift wrappers? Close and encourage the move to Aries?
- How to handle pull requests for LibVCX? Deprecate?
- Close PR [https://github.com/hyperledger/indy-sdk/pull/1048](https://github.com/hyperledger/indy-sdk/pull/1048) as something that will be replaced by the advanced schema work?
- HIPE pull requests: [https://github.com/hyperledger/indy-hipe/pulls](https://github.com/hyperledger/indy-hipe/pulls)

## Action items

- HIPE #138, Issue #144 (Ken and Brent)
  
  - Create a PR for changing status to ACCEPTED
  - Check for an Aries RFC

## Call Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464301/19465091.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
