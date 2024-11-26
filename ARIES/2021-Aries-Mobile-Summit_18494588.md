1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Mobile Summit](Aries-Mobile-Summit_18494526.html)

# Hyperledger Aries : 2021 Aries Mobile Summit

Created by Sam Curren, last modified on Jan 10, 2022

The Mobile Summit is a series of weekly workshops organized to address issues specific to mobile agents and wallets.

## Meetings

[2021-11-16 Aries Summit Session](2021-11-16-Aries-Summit-Session_18494660.html) - QR/Invitations 

[2021-11-23 Aries Summit Session](2021-11-23-Aries-Summit-Session_18494691.html) - Mobile Infrastructure 

[2021-11-30 Aries Summit Session](2021-11-30-Aries-Summit-Session_18494777.html) - Credential UX Part 1

[2021-12-07 Aries Summit Session](2021-12-07-Aries-Summit-Session_18494869.html) - Credential UX Part 2

[2021-12-14 Aries Summit Session](2021-12-14-Aries-Summit-Session_18494953.html) - General UX / Summit Wrap-up

## Outcome &amp; Work Items

[RFC 496](https://github.com/hyperledger/aries-rfcs/blob/main/features/0496-transition-to-oob-and-did-exchange/README.md) - Transition to OOB and DID Exchange From [2021-11-16 Session](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2021-11-16+Aries+Summit+Session)

- **To do**: Chase wallet vendors, share findings, and update RFC [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)

How are we really going to do deep-links? From [2021-11-16 Session](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2021-11-16+Aries+Summit+Session)

- Options: Custom, associated domains, community managed domain
- **To Do**: Writeup of proposed option: [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) [Clecio Varjao](https://lf-hyperledger.atlassian.net/wiki/people/557058:f9e1bfa2-a82c-4b68-85ee-627507d593d9?ref=confluence) [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)

Handling HTTP on mobile, since mobile OS's require an exemption to use HTTP. DIDComm over HTTPS results in double encryption. From [2021-11-16 Session](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2021-11-16+Aries+Summit+Session)

- **To Do**: PR to [RFC 0025 Transports](https://github.com/hyperledger/aries-rfcs/tree/main/features/0025-didcomm-transports) to make HTTPS a SHOULD since the UX to request an exemption is a Bad Thing [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence)

Auto-approval of presentation requests. From [2021-12-07 Session](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2021-12-07+Aries+Summit+Session)

- Can be risky, e.g. auto-presenting could lead to interaction-less login
- One aspect: bulk approval (present series of proofs with one user action to approve)
- Another aspect: policy approval (conditions by which an approval or other user action can be automated)
  
  - Care needed on: anti-patterns, security vs. convenience, following SSI principles, fiduciary responsibility when agents work on behalf of users
- **To Do:**
  
  - Needs bulk presentation request (Present Proof) (mostly done)
  - Needs policy to recommend bulk actions
  - Policy approval is complex and needs more investigation

Machine-Readable Governance and UX. From [2021-12-07 Session](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/2021-12-07+Aries+Summit+Session)

- Introduces new types of user interactions
- Has many types of governance: root of trust, identifying participants, etc.
- Mike is working on test applications of Machine Readable Governance

Credential UX

- Theming can be facilitated using overlay bundles and SVG
- Review Horatio's work on SVG credential display: [https://github.com/hyperledger/aries-rfcs/pull/694/files?short\_path=c91c22b#diff-c91c22b4e711690c9d2dc4c3830300ba7a1e7fa0af70e100922f13aa43c87a6e](https://github.com/hyperledger/aries-rfcs/pull/694/files?short_path=c91c22b#diff-c91c22b4e711690c9d2dc4c3830300ba7a1e7fa0af70e100922f13aa43c87a6e)
- Horatio and Sebastien to work on Bifold and Lissi for compatible display
- **To Do**: [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) to work on an overlay layer type
- risk: may give organizations too much control on the look and feel of a credential

UX of Invitations

- Development of Machine Readable Governance
- Development of language around trust
- **To Do**: Need Proposed Initial Attempt as an Aries RFC - [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)

Mobile Verifiers

- Inversion of QR scanning flow where verifier scans holder's QR code
- Other mechanisms other than QR Code (e.g.: BLE)
- **Todo**: Summary of existing state for BLE
- **Todo**: Summary of existing state for NFC
- Todo: Document use cases and UX flows

Device Backup/Recovery

- Define interop format for backup
  
  - Not everything can be backed up. Some credentials may only be usable in the device/wallet it was issued to
- Define a backup service protocol

Error Handling and Reporting

- We don't currently have enough published community knowledge to organize the conversation very well.
- Errors need to be communicated at both a technical level and a human level
- Context for errors is important - don't imply that background errors relate to a different foreground operation.
- **ToDo**: Need a focused convention of agent developers to share the errors they handle and how, with a goal of capturing community knowledge and best practices.

### Original Topics List

- Mobile Infrastructure (2)
  
  - Mobile Verifiers
  - Device Recovery (Backup/Restore/Sync/Rotation to new keys)
  - Secure Element usage
  - SDK / Embedding Agents into existing Mobile Apps
- Credential UX (3)
  
  - SVG Cred Display
  - Auto-approval of presentation requests (e.g.: trusted verifier, trusted preset, etc ...)
  - Credential Theming (e.g. Icon, Colors, Description)
  - Revocation implications for Mobile
  - Consequences of Machine Readable Governance on UX
- Other User Experience (UX) (4)
  
  - UX of Invitations
  - Exposing errors / details to users &amp; power users (404 and 503 like errors)
    
    - Unsupported DID Method
  - Glossary - naming conventions - how to hide technicalities in front of user
- QR / Invitations (1)
  
  - How are we really going to do deep-links?
  - [RFC 496](https://github.com/hyperledger/aries-rfcs/blob/main/features/0496-transition-to-oob-and-did-exchange/README.md) - Transition to OOB and DID Exchange
  - [RFC 700](https://github.com/hyperledger/aries-rfcs/pull/700) - sending out-of-band as query parameters and enable redirect back.
  - HTTP Mobile exemptions
- Security
  
  - DID method specific
  - Immutability of schema and JSON-LD security issues
  - Biometrics/PIN unlock (overlap with UX)
- Protocols
  
  - DIF Credential Manifest attachment (followup from Issue Credential v2 json-ld attachment in AIPv2).
  - DIDComm v2 (and related)
    
    - DIDComm v2
    - WACI

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
