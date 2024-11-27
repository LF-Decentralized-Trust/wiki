1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-02-03 Indy Contributors Call

Created by Richard Esplin, last modified on Feb 03, 2020

## Summary

- Work updates
- Discussion of current projects
- Cancelling the AMER afternoon call going forward

## Timezone: America afternoon / APAC morning

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- Name (Organization) &lt;email&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)(Evernym) &lt;richard.esplin@evernym.com&gt;

## Related Calls and Announcements

- Aries Working Group: Performance Testing LibIndy and ACA-Py
  
  - Presentation: [2020-01-22-B Aries Working Group Call](https://lf-hyperledger.atlassian.net/wiki/spaces/ARIES/pages/18484534/2020-01-22-B+Aries+Working+Group+Call+US+afternoon) (starting ~65 minutes in)
  - Follow-up Q&amp;A: [2020-01-27-A Aries Working Group Call](https://lf-hyperledger.atlassian.net/wiki/spaces/ARIES/pages/18484474/2020-01-29-A+Aries+Working+Group+Call+AMER+morning)
- Identity Implementors Working Group call
  
  - Main place to get project updates, release status, and announcements.

## Release Status and Work Updates

- Indy Node
  
  - January:
    
    - Bugfix-release for edge cases in consensus protocol
    - Additional rich schemas objects: schema object (Sovrin Foundation)
      
      - Just posted Indy HIPE
        
        [https://github.com/hyperledger/indy-hipe/pull/149](https://github.com/hyperledger/indy-hipe/pull/149)
      - Aries RFC
        
        [https://github.com/hyperledger/aries-rfcs/pull/281](https://github.com/hyperledger/aries-rfcs/pull/281)
      - PR of schema object in progress for December
      - Making progress on other RFCs for objects and one that shows how all the objects fit together.
      - Next: encoding object, then mapping object
  - Future
    
    - Replacing Indy Crypto with Ursa (Kiva)
      
      - Debian packages for Ursa-0.3.0 are uploaded to [repo.sovrin.org](http://repo.sovrin.org)
    - Ubuntu 18.04 (Kiva)
      
      - Need to check additional dependencies: 
        
        Error rendering macro 'jira' : null
    - Anoncreds 2.0 (Sovrin Foundation)
- Indy SDK
  
  - January:
    
    - Bugfixes 1.14.2
  - Future
    
    - Deprecating some docs (IS-1425: Getting Started Guides) and wrappers (IS-1423: Python and DotNet)
    - Deprecate  additional wrappers (IS-1424) and LibVCX (IS-1416)
    - GitLab migration alongside Jenkins (Foundation)?
    - Warnings from rust cargo clippy (Mike and Axel), epic: IS-1401
- Indy Catalyst
  
  - [https://github.com/bcgov/indy-catalyst](https://github.com/bcgov/indy-catalyst)
  - Migrating to Hyperledger Aries: plan is to moving to aries-verified-credential-registry
    
    - Needs more documentation
- New design for revocation / Anoncreds 2.0 (Mike)
  
  - Need a plan for changes to Indy Node
    
    - Design: [https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2](https://github.com/hyperledger/ursa-docs/tree/master/specs/anoncreds2)
    - HIPE for overall changes, then a design PR for the changes specific to the different repos.
      
      [https://github.com/hyperledger/indy-node/tree/master/design](https://github.com/hyperledger/indy-node/tree/master/design)
    - BC.gov will implement the existing revocation capability in ACA-Py for use in constrained cases, starting with extracting anoncreds from libindy into indy-aries-anoncreds
  - Comparison of Anoncreds 1.0 and 2.0: [https://docs.google.com/presentation/d/18aqk5q1sqRI\_UhOEuXWAS46-Oltsu\_HNk\_JtKfDVBGc/edit#slide=id.g790163706e\_0\_0](https://docs.google.com/presentation/d/18aqk5q1sqRI_UhOEuXWAS46-Oltsu_HNk_JtKfDVBGc/edit#slide=id.g790163706e_0_0)
- Aries Shared Libraries
  
  - indy-aries-vdr ([Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)) [https://github.com/andrewwhitehead/indy-ledger-client](https://github.com/andrewwhitehead/indy-ledger-client)
    
    - Rust API is almost completed
    - No FFI
    - HTTP proxy
  - Next is indy-aries-anoncreds with anoncreds 1 (ready to add anoncreds 2)

## Main Business

- Move afternoon call to once in four weeks?
  
  - Should just cancel, and focus on the AMER / EUR calls.
- Keith: INDY-2305: Add IP address range for outbound TCP connections from validator nodes
  
  - Changes the way nodes are represented in the Pool Ledger
  - Next step: provide guidance to Keith on where the change should be made.
  - Should probably also change the Sovrin Steward Technical Guidelines to reduce the uptime requirements (uptime should be based on the pool, not individual validator nodes)
- Andrew:
  
  - Next steps on VDR
    
    - VDR Design Doc
    - FFI
    - Unit tests
    - Functional tests
    - Integrate into existing LibIndy
    - Migrate repo to Hyperledger
      
      - First commit should point to previous history in indy-sdk
- Aries-KMS
  
  - Would like a volunteer to move the wallet crate so we have a starting point
- indy-aries-anoncreds
  
  - Mike has started. Repo for aries cred exchange framework.
    
    [https://github.com/sovrin-foundation/aries-credx-framework-rs](https://github.com/sovrin-foundation/aries-credx-framework-rs)
  - Microsoft might be taking a different approach to ZKP revocation
    
    [https://eprint.iacr.org/2019/550.pdf](https://eprint.iacr.org/2019/550.pdf)
- Aries-Shared-Util
  
  - Need a place for Rich Schemas functions
  - Lift-and-shift would be Indy specific, but refactoring for Aries could take a long time
  - Overlap with Mike's aries-core-rs?
    
    [https://github.com/sovrin-foundation/aries-core-rs](https://github.com/sovrin-foundation/aries-core-rs)
- Rich Schemas
- Mike: IS-1222 blocked by Ursa CI / CD
- Agenda for next call: work session.

## Future Calls

- Requirements questions:
  
  - IS-1099: anoncreds.prover\_get\_credentials\_for\_proof\_req should return per-credential timestamp
    
    - Should we allow duplicate credentials from the same issuer?

## Action items

- HIPE #138, Issue #144 (Ken and Brent)
  
  - Create a PR for changing status to ACCEPTED
  - Check for an Aries RFC
- PR to RFC #0019 to compare pack/upack to msgpack (Sergey)
- Richard and Sergey will close old pull requests with a descriptive comment.
- Mike wants to review the 61 cases of "unsafe" libindy calls and figure out if they are justified.

## Call Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464352/19465282.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464352/19465283.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
