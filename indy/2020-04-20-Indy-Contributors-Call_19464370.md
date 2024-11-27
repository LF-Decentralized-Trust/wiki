1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-04-20 Indy Contributors Call

Created by Richard Esplin, last modified by Stephen Curran on Apr 20, 2020

## Summary

Planned:

- Work updates:
  
  - Indy VDR
  - Indy Credx
  - Aries Credx
- Migrating from JIRA to GitHub Issues
- Migrating from Jenkins to GitHub Actions (or Azure Pipelines)
- Revocation 2.0 Discussion

## The call was recorded and available: [dummyfile.txt](#).

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- [Sergey Minaev](https://lf-hyperledger.atlassian.net/wiki/people/557058:f3eb01c9-c402-4ddf-8eb0-18eff9f16aa2?ref=confluence) (Evernym) [sergey.minaev@evernym.com](mailto:sergey.minaev@evernym.com)
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)  (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;

## Related Calls and Announcements

- Identity Implementer Working Group call ([Wiki Page](https://lf-hyperledger.atlassian.net/wiki/display/IWG/Identity+WG+Implementers+Call))
  
  - Main place to get project updates, release status, and announcements.
- IIW is next week - please [register](https://www.eventbrite.com/e/internet-identity-workshop-iiwxxx-30-2020a-tickets-79016788341) and join from your home.

## Release Status and Work Updates

- Move from Sovrin Foundation infrastructure - Wade Barnes
  
  - Move from Jenkins to GitHub actions
    
    - Sovrin Foundation Jenkins machines are going away
    - [Sovrin resource migration](https://lf-hyperledger.atlassian.net/wiki/spaces/CICD/pages/19011213/Sovrin+resource+migration)
    - #cicd discussion "Indy CI / CD Migration" (in #cicd use menu item "Discussions" to see/get to the discussion)
  - Move repo.sovrin.org → Hyperledger Artifactory for all except Sovrin Foundation specific artifacts
- Indy Node
  
  - April: no release
  - May:
    
    - Replacing Indy Crypto with Ursa (Kiva)
    - More "rich schema" objects
    - Ubuntu 20.04 (Kiva)
      
      - Need to check additional dependencies: 
        
        Error rendering macro 'jira' : null
- Indy SDK
  
  - April: no release
  - May/June:
    
    - Indy VDR into LibIndy
    - Indy Credx into LibIndy
- Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
      
      - Nearing release 1.0(?) - most work complete that was needed: Design doc, FFI, testing, CI / CD
        
        - CD not there
        - No design doc, but crate docs
      - As an Aries interface becomes standardized, will add that API layer
        
        - Do we hold off on setting the version until this is in place.  Maybe 0.8
      - GitHub actions runs unit tests and basic integration tests
      - VON Network browser moved to Indy-VDR instead of LibIndy (no wallet needed because it is stateless)
        
        - Andrew working a refactor in a PR
    - indy-credx - [https://github.com/andrewwhitehead/indy-credx](https://github.com/andrewwhitehead/indy-credx)
      
      - need to move ASAP to at least BC Gov repo - [Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)
      
      <!--THE END-->
      
      - ACA-Py branch created that can do credential exchange with indy-credx
      - Next up: adding revocation 2.0 support
      - Integrating upgraded PyO3 library
    - indy-shared-rs - [https://github.com/bcgov/indy-shared-rs](https://github.com/bcgov/indy-shared-rs)
      
      - Shared features across indy-vdr and indy-credx
      - pack/unpack on Ursa (not libsodium)
      - home for revocation support?  Or at least shared set membership proof handling?
    - aries-credx
      
      - [https://github.com/sovrin-foundation/aries-credx-framework-rs](https://github.com/sovrin-foundation/aries-credx-framework-rs)
        
        - 6 most common attribute encodings
        - Does not have anoncreds 1 attribute encoding.
      - Can make a non-revocable credential and create proofs.
        
        - Tagging will be moved to the KMS.
        - Mike will be working on revocation registry 2.0
    - Aries Secure Storage initiatives:
      
      - Mike working on documentation and architecture as an Aries RFC (KMS architecture) and Ursa RFC (API)
        
        - PR is submitted: [https://github.com/hyperledger/aries-rfcs/pull/440](https://github.com/hyperledger/aries-rfcs/pull/440)
      - Mike and Cam's work aries-kms-mayaguez - repo?  features?
        
        [https://github.com/sovrin-foundation/aries-kms-rs](https://github.com/sovrin-foundation/aries-kms-rs)
        
        - Persistence work allows plugging in any database engine.
        - Focus is using an external enclave.
        - Working on Postgres storage; will need help on lox
        - Something out the end of the week.
  - Ursa
    
    - Not covered

## Other Business

- Move to GitHub Issues from JIRA for indy-sdk, indy-node, indy-plenum
  
  - Activate issues, update README to mention history
  - Plan - Lazy Migration: Migrate current, likely to happen JIRAs to Issues as needed
    
    - NOTE: about 200 open issues on indy-sdk with a guess of about 50% to be moved
      
      - Even more open issues on plenum and node
  - Action: Stephen to get Ry to activate Github issues; update READMEs to reflect change.
- Migrate Jenkins to GitHub Actions (and perhaps Azure pipelines)
  
  - Plan started - [Sovrin resource migration](https://lf-hyperledger.atlassian.net/wiki/spaces/CICD/pages/19011213/Sovrin+resource+migration)
  - Resources:  Wade Barnes (BC Gov), Thor Wolpert (BC Gov) for first step (Indy SDK/Linux)
- Revocation 2.0
  
  - [Presentation](https://docs.google.com/presentation/d/1Ql_ClhND_q0-oXguB65lYtwKlDOUpk3JoNOGePaRgTU/edit#slide=id.p) (summary of what was presented on the Aries WG Call)
    
    - General agreement on the approach.
    - Comments from discussion:
      
      - The limiting factor will be the calculations and space needed by the prover to create the merkle tree interior nodes
      - What are the space/time trade-offs between repeating calculations per proof vs. caching the calculated tree?
      - Action: need some experimenting with the approach - compression and space/time for tree calculations
  - Please provide feedback on the proposed design (see JIRA: [Indy-2365](https://jira.hyperledger.org/browse/INDY-2365))
  - Do we need to update/release indy-node if transactions are the same but data is new?
    
    - Yes, but not much.  Mainly to verify the content of the data before writing to the ledger.

## Future Calls

Next call:

Future:

- Requirements questions:
  
  - IS-1099: anoncreds.prover\_get\_credentials\_for\_proof\_req should return per-credential timestamp
    
    - Should we allow duplicate credentials from the same issuer?

## Action items

- PR to RFC #0019 to compare pack/upack to msgpack (Sergey)
- Review the 61 cases of "unsafe" libindy calls and figure out if they are justified.

## Call Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464370/19465400.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
