1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2020 Meeting Notes](2020-Meeting-Notes_19465228.html)

# Hyperledger Indy : 2020-02-10 Indy Contributors Call

Created by Richard Esplin, last modified on Feb 10, 2020

## Summary

Work updates and collaboration

- Indy Node using Ursa
- Indy-VDR
- Anoncreds
- Rich Schemas

Will schedule additional meetings for a Rich Schemas discussion and a discussion to help others support Indy networks.

## We intend to record this call.

## Remember the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Introductions

## Attendees

- Name (Organization) &lt;email&gt;
- [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) (Evernym) &lt;richard.esplin@evernym.com&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass/BC Gov) &lt;swcurran@cloudcompass.ca&gt;
- [Alexander Sherbakov](https://lf-hyperledger.atlassian.net/wiki/people/557058:a955b109-9f8c-405c-9f96-0903d4de8c46?ref=confluence) (Evernym) &lt;alexander.shcherbakov@evernym.com&gt;
- [Camilo Parra](https://lf-hyperledger.atlassian.net/wiki/people/5ade0ac99fcb1f22f34ccae2?ref=confluence) (KIVA) &lt;camilop@kiva.org&gt;
- [Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence) (Sovrin) &lt;adam@sovrin.com&gt;
- [Kumaravel N](https://lf-hyperledger.atlassian.net/wiki/people/70121:1d7790e2-8efd-409a-bf1e-ff3f8c520669?ref=confluence) (Ford)&lt;nkumara2@ford.com&gt;

## Related Calls and Announcements

- Going forward, we will not be holding the AMER afternoon / APAC morning call
- Identity Implementors Working Group call
  
  - Main place to get project updates, release status, and announcements.

## Release Status and Work Updates

- Indy Node
  
  - February:
    
    - Replacing Indy Crypto with Ursa (Kiva)
    - More "rich schema" objects
    - Tool for detecting ZMQ network problems
    - Troubleshooting guide
  - Future
    
    - Ubuntu 18.04 (Kiva)
      
      - Need to check additional dependencies: 
        
        Error rendering macro 'jira' : null
- Indy SDK
  
  - February:
    
    - Bug fixes
- Indy Catalyst
  
  - [https://github.com/bcgov/indy-catalyst](https://github.com/bcgov/indy-catalyst)
  - Migrating to Hyperledger Aries: plan is to moving to aries-verified-credential-registry
    
    - Needs more documentation
- Anoncreds 2.0 (Mike)
  
  - Implementing in an Aries Shared Library
- Aries Shared Libraries
  
  - indy-vdr ([Andrew Whitehead](https://lf-hyperledger.atlassian.net/wiki/people/557058:03322b63-53ed-4272-9c4a-a256b19c7098?ref=confluence)) [https://github.com/andrewwhitehead/indy-ledger-client](https://github.com/andrewwhitehead/indy-ledger-client)
    
    - HTTP REST client that can be used to proxy ZMQ traffic
    - Next steps:
      
      - VDR Design Doc
      - FFI
      - Unit tests
      - Functional tests
      - Migrate repo to Hyperledger
        
        - First commit should point to previous history in indy-sdk
      - Integrate into existing LibIndy
        
        - Apply recent bug fixes to the new VDRI
    - As an Aries interface becomes standardized, a new repo will be created for the indy-aries-vdri
      
      - Or a single aries-vdri with modules for each interoperable ledger
  - indy-aries-anoncreds / indy-creds → indy-credx
    
    - Mike has started. Repo for Aries cred exchange framework.
      
      [https://github.com/sovrin-foundation/aries-credx-framework-rs](https://github.com/sovrin-foundation/aries-credx-framework-rs)
    - As an Aries interface becomes standardized, a new repo would be created for the indy-aries-credx?
    - Goal is to make the current anocreds a separate component, then work on anoncreds 2
    - Microsoft might be taking a different approach to ZKP revocation
      
      [https://eprint.iacr.org/2019/550.pdf](https://eprint.iacr.org/2019/550.pdf)
  - Aries-Shared-Util
    
    - Pack / Unpack
      
      - Lift-and-shift would be Indy specific, but refactoring for Aries-KMS could take a long time
    - Need a place for Rich Schemas functions → many will go to Aries Credx
  - Aries-KMS
  - - Mike and Cam's aries-core-rs → aries-kms-(placeholder)
      
      [https://github.com/sovrin-foundation/aries-core-rs](https://github.com/sovrin-foundation/aries-core-rs)
      
      - Evolution from lox
      - Will include a default storage that is not a different implementation from the plugins
      - Hopes for a protype in February
    - Move the Indy wallet crate as a starting point → aries-kms-taiga
- Ursa 0.3.2
  
  - Releasing this week?
  - Implements key exchange, so LibSodium hopefully is no longer required

## Main Business

- Special calls:
  
  - Conflicts: US February 17, Russia February 24, HL Global Forum March 2, Russian March 9
  - Rich Schemas:
    
    - Tuesday February 11 at 8 Mountain or Wednesday February 12 at 9 Mountain?
  - On troubleshooting Indy
    
    - Tuesday February 25 at 8 Mountain or Wednesday February 26 at 9 Mountain?
- Collaborate on Rich Schemas
  
  - New Indy HIPE: [https://github.com/hyperledger/indy-hipe/pull/153](https://github.com/hyperledger/indy-hipe/pull/153)
  - Aries RFC is next
  - Concerned about interacting with schema objects as DID Docs
- IS-1222 blocked by Ursa CI / CD
- INDY-2305: Add IP address range for outbound TCP connections from validator nodes

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
- Mike wants to review the 61 cases of "unsafe" libindy calls and figure out if they are justified.

## Call Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464354/19465309.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464354/19465310.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
