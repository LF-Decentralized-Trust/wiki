1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Mobile Summit](Aries-Mobile-Summit_18494526.html)
5. [2021 Aries Mobile Summit](2021-Aries-Mobile-Summit_18494588.html)

# Hyperledger Aries : 2021-11-23 Aries Summit Session

Created by Sam Curren, last modified by Ry Jones on Apr 26, 2022

## Summary:

- Mobile Infrastructure
  
  - Mobile Verifiers
  - Device Recovery (Backup/Restore/Sync/Rotation to new keys)
  - Secure Element usage
  - SDK / Embedding Agents into existing Mobile Apps

## Note: This call was recorded and the recording and chat transcript are at the bottom of the page.

## Date

23 Nov 2021 (7AM-9AM Los Angeles)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Dial-in link

[https://zoom.us/j/93810537086](https://zoom.us/j/93810537086)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence) &lt;sam@indicio.tech&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) &lt;james.ebert@indicio.tech&gt;
- [Akiff Manji](https://lf-hyperledger.atlassian.net/wiki/people/557058:493444f6-a19a-4aa4-a9ca-24d3397297bf?ref=confluence) &lt;amanji@petridish.dev&gt;
- [Clecio Varjao](https://lf-hyperledger.atlassian.net/wiki/people/557058:f9e1bfa2-a82c-4b68-85ee-627507d593d9?ref=confluence) &lt;clecio.varjao@gov.bc.ca&gt;
- [Darrell O'Donnell](https://lf-hyperledger.atlassian.net/wiki/people/557058:63b778a3-3806-47ba-a8dd-5604ccf10f66?ref=confluence) &lt;darrell.odonnell@continuumloop.com&gt;
- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) (Cloud Compass Computing Inc.) &lt;swcurran@cloudcompass.ca&gt;
- [Sai Ranjit Tummalapalli](https://lf-hyperledger.atlassian.net/wiki/people/5f620f169109170076f8dc96?ref=confluence) &lt;sairanjit.tummalapalli@ayanworks.com&gt;
- [Jakub Koci](https://lf-hyperledger.atlassian.net/wiki/people/557058:a09deeb2-174a-4e43-9fd0-890f4d055dd5?ref=confluence) &lt;jakub.koci@gmail.com&gt;
- [Jason Leach](https://lf-hyperledger.atlassian.net/wiki/people/557058:f6688130-fee2-4c0a-a611-b8623f0d7f57?ref=confluence) (BC Gov) &lt;jason.leach@fullboar.ca&gt;

## Welcome / Introductions

## Focus

Mobile Infrastructure

## Discussion Topics

- **Mobile Verifiers**
  
  - We need them.
  - Flow
    
    - Holder displays QR, Verifier scans with mobile app and sees the result. - Common Model, assumed by those new to industry.
    - 'presenting' the QR code feels natural when 'presenting' a credential.
    - QR is best as invitation, not requiring user to know in advance what to present.
    - Verifier can also display QR.
    - Speed of transaction
      
      - User prepares to have transaction happen fast
        
        - Preselect or preauthorize set of actions
        - Can be assisted by governance / trust registry to find common targets
      - build set of 'reapprovals' after done initially.
        
        - save my authorization
  - Unique Features
    
    - Offline Verifications
      
      - Can't use shortened QR codes
      - BLE Verification useful offline
        
        - Needs framework support
      - Machine Readable Governance - cached
        
        - Cache schemas
        - Cache public keys for verifiers?
        - Pass file? (Interaction)
      - NFC - Needs investigation
    - Common Hardware
    - Framework support required
      
      - Offline aware
    - UI Supports required
    - Cache Needed
      
      - Speed of local assets
      - Mechanisms
        
        - Trust Registry Protocols - [https://wiki.trustoverip.org/display/HOME/ToIP+Trust+Registry+Protocol+Specification](https://wiki.trustoverip.org/display/HOME/ToIP+Trust+Registry+Protocol+Specification)
          
          - Webinar - [https://www.continuumloop.com/trust-registries-webinar/](https://www.continuumloop.com/trust-registries-webinar/)
        - Machine Readable Governance
        - Hard Coded
      - TTL
    - User Experience
      
      - Clear for Holder
      - Clear for Verifier
      - Clear indication of where in the flow they are. Universal progress bar?
      - Particularly for non-happy paths
        
        - Internationalization / Localization
    - Performance
    - Auditing verifications
      
      - reporting verifications back to main org
      - minimal disclosure auditing
      - knowing what is stored/passed
  - Actions Items
    
    - Framework Support
      
      - Caching
      - Transport (BLE, NFC)
    - Summary of existing state - Where are we?
      
      - BLE
        
        - [https://github.com/decentralized-identity/didcomm-bluetooth/blob/main/spec.md](https://github.com/decentralized-identity/didcomm-bluetooth/blob/main/spec.md)
      - NFC - how would it work? - Sebastian (Lissi)
      - Docs about [Machine Readable Governance](https://github.com/hyperledger/aries-rfcs/tree/main/concepts/0430-machine-readable-governance-frameworks) is currently being used.
        
        - Mike to provide overview in a few weeks, for now a [presentation](https://hackmd.io/@mikekebert/HyjBmusEF#/)
        - [Trust Registries from ToIP](https://docs.google.com/presentation/d/1skHbfJqXaX8er8iUzisNWWnFCMp7bv2ZjKmsq4GXyeA/edit#slide=id.gf81ff01b32_0_4) - Darrell provided, to link
        - How do verifiers get templates of presentation requests so they know what to ask.
    - UX of selecting which you want to verify and doing verifications
      
      - Use cases – e.g. Verifier is processing a line up going into an Event collecting Ticket+PoVaccination
      - UX for some use cases
- Device Recovery (Backup/Restore/Recovery/Rotation to new keys)
  
  - Backup / Restore Formats?
  - [https://w3c-ccg.github.io/universal-wallet-interop-spec/](https://w3c-ccg.github.io/universal-wallet-interop-spec/)
  - Data Model + app specific in the same format?
  - Keep them separate?
  - Security of backups?
    
    - huge attack vector – e.g. family member restores backup to new device and uses data
    - Is it possible to disable an old phone when a restoration is done to a new phone?
    - Assumption is that encrypted backup goes one place, the recovery key goes elsewhere and the only come together for restore
      
      - Is there more that can be done?  Other protections?
        
        - N of M recovery mechanism – e.g. [Shamir's Secret Sharing](https://en.wikipedia.org/wiki/Shamir%27s_Secret_Sharing) (coolest algorithm ever!)
      - Can this be done with self-service?  Is that safe enough?
      - Selective recovery – is that possible?
  - Some things that can't be backed up or restored
    
    - Example is a device-based keys – you can't back these up
      
      - If there is a credential somehow tied to a device key, that credential must be reissued (and that's OK)
  - How to do continuous backups (don't lose data)?
    
    - File format
      
      - File format for a full backup
        
        - Contents – connections, credentials, history
      - Will we have to do (more or less) continuous backup - full backup every time efficient enough vs. incremental?  Classic backup issues.
        
        - Treat this as an optimization for now
    - An RFC to define such a protocol to be used with a backup service – perhaps supplied by a mediator (but could be any connection).
      
      - Setup backup – location, recovery key(s) (format – e.g. passphrase? biometrics?), restoration process
      - Make backup – ongoing – data format
      - Retrieve backup for restoration
      - Restore backup using recovery key(s)
    - How can Mobile OS features help with this?
      
      - E.g. Backup/Restore of app data
- Secure Element usage
  
  - Provinces Project - diagram, markdown - decisions when making a wallet.
    
    - starting point for security framework oriented folks.
- SDK / Embedding Agents into existing Mobile Apps

## Action items

## Call Recording

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

File [GMT20211123-150030\_Recording.transcript.vtt](attachments/18494691/18516212.vtt "Download")

Apr 26, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

Text File [GMT20211123-150030\_Recording.txt](attachments/18494691/18516213.txt "Download")

Apr 26, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

[Download All](/wiki/download/all_attachments?pageId=18494691 "Download all the latest versions of attachments on this page as single zip file.")

## Attachments:

![](images/icons/bullet_blue.gif) [GMT20211123-150030\_Recording.transcript.vtt](attachments/18494691/18516212.vtt) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [GMT20211123-150030\_Recording.txt](attachments/18494691/18516213.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18494691/18516211.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18494691/18516210.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
