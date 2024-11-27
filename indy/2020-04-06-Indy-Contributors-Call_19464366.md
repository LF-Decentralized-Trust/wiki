1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-04-06 Indy Contributors Call

Created by Richard Esplin, last modified on Apr 06, 2020

## Summary

- Work updates:
  
  - Indy VDR
  - Indy Credx / Aries Credx
- The future of this meeting

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- Name (Organization) &lt;email&gt;
- Richard Esplin (Evernym) &lt;richard.esplin@evernym.com&gt;
- Stephen Curran (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- Kumaravel N (Ford) &lt;nkumara2@ford.com&gt;

## Related Calls and Announcements

- Identity Implementors Working Group call
  
  - Main place to get project updates, release status, and announcements.
- Results from [call to discuss techniques for supporting an Indy Network](19464360.html)

## Release Status and Work Updates

- Move from Sovrin Foundation infrastructure
  
  - Move from Jenkins to GitHub actions
    
    - Jenkins machines are going away
    - [Sovrin resource migration](https://lf-hyperledger.atlassian.net/wiki/spaces/CICD/pages/19011213/Sovrin+resource+migration)
    - #cicd discussion "Indy CI / CD Migration" (in #cicd use menu item "Discussions" to see/get to the discussion)
  - repo.sovrin.org → Hyperledger Artifactory
- Indy Node
  
  - April: no release
  - May:
    
    - Replacing Indy Crypto with Ursa (Kiva)
    - More "rich schema" objects
    - Ubuntu 20.04 (Kiva)
      
      - Need to check additional dependencies: 
        
        Error rendering macro 'jira' : null
- Indy SDK
  
  - March: 
    
    - 1.15.0:
      
      - LibVCX improvements to reject proof and connection redirect
      - Bug fixes
  - April: no release
  - May:
    
    - Indy VDR into LibIndy
    - Indy Credx into LibIndy
- Aries Verifiable Credentials Registry (VCR)
  
  - [https://github.com/bcgov/aries-vcr](https://github.com/bcgov/aries-vcr)
  - Working on transitioning to Hyperledger - rename, required files, documentation
  - Being deployed at Government of Canada
- Anoncreds 2.0
  
  - Mike: Creating a development plan in the Indy section of the wiki
  - Mike: Aries-Credx
  - Andrew: indy-credx
- Aries Shared Libraries
  
  - Aries Shared:
    
    - indy-vdr (Andrew Whitehead)  [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr)
      
      - Remaining work: Design doc, FFI, testing, CI / CD
      - As an Aries interface becomes standardized, will add that API layer
      - Split out an Indy-Util to contain common components between Indy-VDR and Indy-Credx
        
        - Need to check that duplicate copies of the util library doesn't cause trouble.
      - GitHub actions runs unit tests and basic integration tests
      - VON Network browser moved to Indy-VDR instead of LibIndy (no wallet needed because it is stateless)
      - Andrew working a large refactor in a PR
      - Put rich shemas behind a feature flag?
    - indy-credx / aries-credx
      
      - [https://github.com/sovrin-foundation/aries-credx-framework-rs](https://github.com/sovrin-foundation/aries-credx-framework-rs)
        
        - 6 most common attribute encodings
        - Does not yet have anoncreds 1 attribute encoding.
      - [https://github.com/andrewwhitehead/indy-credx](https://github.com/andrewwhitehead/indy-credx)
        
        - Can make a non-revocable credential and create proofs.
        - Tagging will be moved to the KMS.
        - Mike will be working on revocation registry 2.0
      - Integrating upgraded PyO3 library
      - Create an Indy-Util for API types and other utility functions?
    - Aries-Util
      
      - Pack / Unpack
      - Not started yet
    - Aries-KMS
      
      - Mike working on documentation and architecture as an Aries RFC (KMS architecture) and Ursa RFC (API)
        
        - PR is submitted: [https://github.com/hyperledger/aries-rfcs/pull/440](https://github.com/hyperledger/aries-rfcs/pull/440)
      - Mike and Cam's aries-core-rs → aries-kms-mayaguez
        
        [https://github.com/sovrin-foundation/aries-kms-rs](https://github.com/sovrin-foundation/aries-kms-rs)
        
        - Persistence work allows plugging in any database engine.
        - Focus is using an external enclave.
      - Indy wallet crate might move to start another aries-kms implementation → aries-kms-vostok
    - Aries-Storage
      
      - Non-KMS entities
- Ursa 0.3.2
  
  - To replace libsodium, need to have a replacement for the anoncrypt / authcrypt sealed box for pack / unpack.
    
    - Can be done in Ursa with two steps, but might add as a single function call.

## Other Business

- Future of this meeting (and Indy collaboration generally)
  
  - We recognize as a community that each of us needs to adapt to current global events: improving the upstream open source libraries is likely to be slower.
    
    - Note from Aries calls: no apology is needed if people take longer to respond to things.
    - Evernym focused on a COVID19 response project through end of May
      
      - Richard's role changed, so we need a change in host for this meeting
        
        - Stephen Curran will host
    - More async collaboration

## Future Calls

Next call:

Future:

- Requirements questions:
  
  - IS-1099: anoncreds.prover\_get\_credentials\_for\_proof\_req should return per-credential timestamp
    
    - Should we allow duplicate credentials from the same issuer?

## Action items

- HIPE #138, Issue #144 (Ken and Brent)
  
  - Create a PR for changing status to ACCEPTED
  - Check for an Aries RFC
- PR to RFC #0019 to compare pack/upack to msgpack (Sergey)
- Richard and Sergey will close old pull requests with a descriptive comment.
- Review the 61 cases of "unsafe" libindy calls and figure out if they are justified.

## Call Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464366/19464372.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464366/19464374.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
