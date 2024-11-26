1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2021 Aries Working Group Meetings](2021-Aries-Working-Group-Meetings_18514540.html)

# Hyperledger Aries : 2021-11-03 Aries Working Group Call

Created by Sam Curren, last modified by Robert Mitwicki on Nov 03, 2021

## Summary:

- Aries Mobile Agent Summit

## Note: This call was recorded and the recording and chat transcript are at the bottom of the page.

## Date

03 Nov 2021 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Dial-in link

[https://zoom.us/my/hyperledger.community.3?pwd=UE90WHhEaHRqOGEyMkV3cldKa2d2dz09](https://zoom.us/my/hyperledger.community.3?pwd=UE90WHhEaHRqOGEyMkV3cldKa2d2dz09)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) &lt;sam@indicio.tech&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) &lt;smccown@anonyome.com&gt;
- [Rolson Quadras](https://lf-hyperledger.atlassian.net/wiki/people/622101eec88f1000682f2f68?ref=confluence)&lt;rolson.quadras@securekey.com&gt;
- [Sudesh Shetty](https://lf-hyperledger.atlassian.net/wiki/people/62334edb867a4e0070970909?ref=confluence)&lt;sudesh.shetty@securekey.com&gt;
- [Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)&lt;robert.mitwicki@humancolossus.org&gt;

## Welcome / Introductions

## Announcements

- Swiss- Discussion paper on the target vision for an e-ID: 
  
  - [https://www.bj.admin.ch/dam/bj/en/data/staat/gesetzgebung/staatliche-e-id/diskussionspapier-zielbild-e-id.pdf.download.pdf/diskussionspapier-zielbild-e-id.pdf](https://www.bj.admin.ch/dam/bj/en/data/staat/gesetzgebung/staatliche-e-id/diskussionspapier-zielbild-e-id.pdf.download.pdf/diskussionspapier-zielbild-e-id.pdf)
- [2021-11-04 : Identity Implementers WG Call](https://lf-hyperledger.atlassian.net/wiki/spaces/IWG/pages/18252063/2021-11-04+Identity+Implementers+WG+Call) (9am MT / 3pm UTC):  Steve McCown will present methods for automatically generating language wrappers for Rust libraries.

Release Status and Work Updates

- Aries Protocol Test Suite
- Aries Agent Test Harness
- Aries Shared:
- Aries-CloudAgent-Python
  
  - 0.7.2 Release being prepared for this week
  - Test cases being run for BBS+ and PE with a few issues found.
- Aries-Framework-Go (Troy) #aries-go
- Aries Mobile Agent React Native
- Aries-CloudAgent-Pico
- Aries-SDK-Ruby (Jack)
- Aries-Framework-DotNet (Tomislav)
- Aries-Toolbox
- Aries-SDK-Java
- Aries-Framework-JavaScript
  
  - New [aries-framework-javascript-ext](https://github.com/hyperledger/aries-framework-javascript-ext) repository for extensions
    
    - New package @aries-framework/rest as a rest wrapper around AFJ
  - Work going on for automatic multi indy ledger support
- Rich Schemas and W3C Verifiable Credentials (Brent &amp; Ken)
- Aries-MobileAgent-Xamarin (Aries MAX)
- Ursa

## Notes:

## Discussion Topics

- Aries Mobile Agent Summit
- Prioritize topics: 
  
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
- Future sessions - schedule, format, and topics
  
  - 2 hour meetings weekly
  - task forces - publish agendas, focused on different issues
  - group agenda topics
    
    - protocol format
    - mobile infrastructure
      
      - backup
      - secure elements
    - ux topics
      
      - display creds
      - standardized experiences
  - leverage wiki on topics, discussions on github?
- Tasks
  
  - Select regular 2 hour meeting block (sam)
  - wiki / etc infrastructure (sam)

## Other Business

## Future Topics

- Next Meeting
- Daniel Hardman - n-wise protocols (not next week, perhaps 2 weeks)
- ux - wallet interactions with machine readable governance files, what UI do we want, and how do we support that? (stephen curran, pending topic)
- Other:
  
  - Where should we document interoperability results (AIP 1.0)? A page in this wiki space?
  - Hubs vs Agents
    
    - [https://www.hyperledger.org/blog/2019/07/23/rhythm-and-melody-how-hubs-and-agents-rock-together](https://www.hyperledger.org/blog/2019/07/23/rhythm-and-melody-how-hubs-and-agents-rock-together)
  - Status and future of wallet query language
  - DID Resolution W3C and Sam's concerns: [https://github.com/hyperledger/aries-rfcs/issues/130](https://github.com/hyperledger/aries-rfcs/issues/130)
  - Connectionless
  - KERI - deep dive / transaction family / Notary groups /

## Action items

- [Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)  Bring on the next call information about how ACDC address problems of JSON-LD serialization of RDF

## Call Recording

  File Modified

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
