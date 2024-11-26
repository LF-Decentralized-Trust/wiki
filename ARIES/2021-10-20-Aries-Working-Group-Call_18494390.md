1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2021 Aries Working Group Meetings](2021-Aries-Working-Group-Meetings_18514540.html)

# Hyperledger Aries : 2021-10-20 Aries Working Group Call

Created by Sam Curren, last modified on Oct 20, 2021

## Summary:

- Work updates
- IIW Recap
- Aries Mobile Agent Mini Summit
- Aires Mediator Service
- Open Discussion (as time permits)

## Note: This call was recorded and the recording and chat transcript are at the bottom of the page.

## Date

20 Oct 2021 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

- [Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)&lt;robert.mitwicki@humancolossus.org&gt;
- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) &lt;sam@indicio.tech&gt;
- [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) &lt;iancostanzo@gmail.com&gt;
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence) &lt;smccown@anonyome.com&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) &lt;bruce\_conrad@byu.edu&gt;

## Welcome / Introductions

## Announcements

- Swiss- Discussion paper on the target vision for an e-ID: 
  
  - [https://www.bj.admin.ch/dam/bj/en/data/staat/gesetzgebung/staatliche-e-id/diskussionspapier-zielbild-e-id.pdf.download.pdf/diskussionspapier-zielbild-e-id.pdf](https://www.bj.admin.ch/dam/bj/en/data/staat/gesetzgebung/staatliche-e-id/diskussionspapier-zielbild-e-id.pdf.download.pdf/diskussionspapier-zielbild-e-id.pdf)
- GlobaliD - 'Code with me' proposal for native mobile aries frameworks. Information and reward details [here](https://docs.google.com/document/d/1v9_DhHvT5ahMEwV0eHxkVck5knN7cCde6MKlKuNxgt4/edit#heading=h.bl43zjnuoqpk)
  
- [2021-10-21 : Identity Implementers WG Call](https://lf-hyperledger.atlassian.net/wiki/spaces/IWG/pages/18252061/2021-10-21+Identity+Implementers+WG+Call) (9am MT / 3pm UTC):  Review current development topics from several SSI organizations and working groups

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
  
  - Proposed Date: 27 Oct 2021 and the next few weeks?
  - All Aries mobile app devs invited!
  - [RFC 496](https://github.com/hyperledger/aries-rfcs/blob/main/features/0496-transition-to-oob-and-did-exchange/README.md) - Transition to OOB and DID Exchange
  - HTTP Mobile exemptions
  - UX of Invitations
  - SVG Cred Display
  - Consequences of Machine Readable Governance on UX
  - Embedding Agents into existing Mobile Apps
  - Exposing errors / details to users &amp; power users (404 and 503 like errors)
    
    - Unsupported DID Method
  - Revocation implications for Mobile
  - Mobile Verifiers
  - How are we really going to do deep-links?
  - Secure Element usage
  - Device Recovery (Backup/Restore/Sync/Rotation to new keys)
- IIW Recap
  
  - What worries you?
    
    - Interop
    - Ethical uses
    - lack of UX focus
    - Understandable paradigm
  - Revocation
  - Potential non-correlation features of JSON-LD
  - DID Method Interop
  - GLIF demonstration of KERI based stack
  - PAC Privacy Authenticity Confidentiality - Sam Smith
- Potential DIDComm Users Group
  
  - Protocol Development?
- Aries Mediator Service - Ian
- how ACDC address problems of JSON-LD serialization of RDF
  
  - Robert Mitwiki
- Open Discussion

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
