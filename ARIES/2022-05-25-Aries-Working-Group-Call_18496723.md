1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2022 Aries Working Group Meetings](2022-Aries-Working-Group-Meetings_18515842.html)

# Hyperledger Aries : 2022-05-25 Aries Working Group Call

Created by Sam Curren, last modified by Ry Jones on Dec 05, 2022

## Summary:

- Machine Readable Governance Update
- AIP v2 Update

## Date

25 May 2022 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Mike Ebert](https://lf-hyperledger.atlassian.net/wiki/people/5ea322540d58350c2b066eeb?ref=confluence)(Indicio) &lt;mike@indicio.tech&gt;
- [Philippe Foucault](https://lf-hyperledger.atlassian.net/wiki/people/62150c66c345490071971b9f?ref=confluence) (Gouvernement du Québec) &lt;philippe.foucault@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca/)&gt;
- [Rodolfo Miranda](https://lf-hyperledger.atlassian.net/wiki/people/557058:a5a62b78-cc75-4d00-80c0-df455129302a?ref=confluence) (rootsid.com)&lt;rodolfo.miranda@gmail.com&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (rootsid.com)&lt;lance.byrd@rootsid.com&gt;
- [Sylvain Martel](https://lf-hyperledger.atlassian.net/wiki/people/712020:9eb55fb2-a220-4945-916a-6da7d1ed6101?ref=confluence)(Gouvernement du Québec) &lt;sylvain.martel10@mcn.gouv.qc.ca&gt;
- [Marco](https://lf-hyperledger.atlassian.net/wiki/people/557058:970af937-5953-455b-9fed-ac996daa73dd?ref=confluence) (Gouvernement du Québec) &lt;marc-olivier.deschenes-rompre@[mcn.gouv.qc.ca](http://mcn.gouv.qc.ca)&gt;
- [Regis Eloi](https://lf-hyperledger.atlassian.net/wiki/people/712020:1f85fa5f-ff75-4f77-9f7b-b6eb5244e07f?ref=confluence) (IDLab) &lt;[regis.eloi@idlab.org](mailto:regis.eloi@idlab.org)&gt;

## Welcome / Introductions

## Announcements

- DIDComm WG Voting to approve V2 on Monday!
- Cardea Interopathon June 16 (includes basic protocol testing–connection using connections v.1 and OOB invitations, issuance, presentations, basic message, question and answer)

Release Status and Work Updates

- Aries Agent Test Harness ([https://aries-interop.info](https://aries-interop.info))
- Aries Shared Components - Indy SDK replacements
  
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs,)
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr,)
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
    
    - 0.2.5 release - performance/load work and testing – specific load errors reduced (down to 0.05% error rate), performance up 11%
- Frameworks:
  
  - Aries-CloudAgent-Python ([https://github.com/hyperledger/aries-cloudagent-python,](https://github.com/hyperledger/aries-cloudagent-python,) Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html))
  - Aries-Framework-JavaScript ([https://github.com/hyperledger/aries-framework-javascript,](https://github.com/hyperledger/aries-framework-javascript,) Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html))
    
    - Working on 0.3.0 release
      
      - Issue Credential / Present Proof v2
      - Merged: OOB / DIDExchange - merged last Friday
      - Merged: Holder revocation with revocation notifications support
    - PR open to support lower versions of a protocol
    - Nearing completion for JSON-LD and BBS+ credential support
    - Started working on writing a wrapper for Indy VDR for React Native – Almost ready now
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html)) 
    
    - Working on support for DIDComm v2, Credential Manifest, OOB v2 and v3 credential protocols (for DIDComm v2)
    - [RFC 700](https://github.com/hyperledger/aries-rfcs/pull/700) to enable web wallets
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-service-mediator](https://github.com/hyperledger/aries-mediator-service) repo added – a DIDComm Mediator in a Box
- Aries-Toolbox
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Notes:

## Discussion Topics

- Machine-readable governance using governance framework files update - Mike
  
  - Response at IIW
  - Work item at the DIF Claims and Credentials Working Group
  - Major parts
    
    - Meta data
    - Schema list
    - Trusted participants
    - Roles and permissions
    - Actions (which allow for workflows)
      
      - Protocols
      - Decisions
      - APIs
    - Utilize DIF presentation definitions (presentation exchange)
    - Looking to add DIF credential manifests
  - Releasing basic implementation in Cardea
  - Should investigate OCA schema (make sure the file is more human-readable). See: [https://github.com/hyperledger/aries-mobile-agent-react-native/issues/164](https://github.com/hyperledger/aries-mobile-agent-react-native/issues/164)
  - Should interface with TOIP
    
    - Who are the trusted issuers?
    - Who are the authorized verifiers?
    - What schemas are we using? (and how are they defined?)
    - Important note: It's not strictly centralized
    - TOIP has no problem incorporating existing work for defining schemas and other useful information specified by other parties
- Status update for AIP v2 - Let's cover this again later, esp. when the AIP v2 leaders (Sam Curren or Steven Curran or Timo) are here to discuss
  
  - What progress has everybody made?
  - What items are being difficult?
  - Which optional targets have folks worked on?
- Pickup Protocol
  
  - [PR 737](https://github.com/hyperledger/aries-rfcs/pull/737) - Add support for \`message\_id\` in notification - no objections or changes were voiced during today's meeting.

## Other Business

## Future Topics

- decorator for redirection after proofs. - existing?
- Standardized attribute names for AnonCreds - alignment with VC data model. (Paul Bastian)
  
  - terms and conditions (as link)
  - machine-readable governance?

## Action items

## Call Recording

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

File [GMT20220525-140437\_Recording.transcript.vtt](attachments/18496723/18517122.vtt "Download")

Dec 05, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

Text File [GMT20220525-140437\_Recording.txt](attachments/18496723/18517123.txt "Download")

Dec 05, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
