1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2023 Aries Working Group Meetings](2023-Aries-Working-Group-Meetings_18517292.html)

# Hyperledger Aries : 2023-03-15 Aries Working Group Call

Created by Sam Curren, last modified on Mar 15, 2023

## Summary:

- Peer DID Updates
- OCA Next Steps
- IssueCredential 2.1 issues
- PR/Issue Review

## Date

15 Mar 2023 (7AM Los Angeles, 10AM New York, 3PM London, 4PM CET, 18H Moscow)

![](https://wiki.hyperledger.org/download/attachments/29034696/Antitrustnotice.png?version=1&modificationDate=1581695654000&api=v2)

Hyperledger is committed to creating a safe and welcoming

community for all. For more information

please visit the [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Code+of+Conduct).

![](https://wiki.hyperledger.org/download/attachments/2392771/welcome.png?version=2&modificationDate=1572450107000&api=v2)

## Attendees

- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)(Indicio) &lt;sam@indicio.tech&gt;
- [Alexandra Walker](https://lf-hyperledger.atlassian.net/wiki/people/62e8177de50f2f2a39544bf5?ref=confluence) (Indicio) &lt;alex.walker@indicio.tech&gt;
- [bruce\_conrad@byu.edu](https://lf-hyperledger.atlassian.net/wiki/people/5a305bc720cc34374b243891?ref=confluence) (Pico Labs) &lt;bruce\_conrad@byu.edu&gt;
- [Lance Byrd](https://lf-hyperledger.atlassian.net/wiki/people/6346b13f754fb6b373b9af19?ref=confluence) (RootsID) &lt;lance.byrd@rootsid.com&gt;
- [James Ebert](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b65ef69-a9c7-4f13-8ac7-eca3c34f5f97?ref=confluence) (Indicio) &lt;james.ebert@indicio.tech&gt;
- [Warren Gallagher](https://lf-hyperledger.atlassian.net/wiki/people/557058:98b910cc-1131-4987-bc79-b6c4681c64ab?ref=confluence) (AffinitiQuest) &lt;warren@affinitiquest.io&gt;

## Welcome / Introductions

## Announcements

- IIW
- IIW DIDComm v2 Connectathon

Release Status and Work Updates

- Aries Agent Test Harness ([https://aries-interop.info](https://aries-interop.info))
- Aries Shared Components - Indy SDK replacements
  
  - Shared Rust Library/CredX (AnonCreds) [https://github.com/hyperledger/indy-shared-rs](https://github.com/hyperledger/indy-shared-rs,)
  - Indy Verifiable Date Registry - Ledger Interface [https://github.com/hyperledger/indy-vdr](https://github.com/hyperledger/indy-vdr,)
  - Aries Askar secure storage - [https://github.com/bcgov/aries-askar](https://github.com/bcgov/aries-askar)
  - AnonCreds Rust - https://github.com/hyperledger/anoncreds-rs
- Frameworks:
  
  - Aries-CloudAgent-Python ([https://github.com/hyperledger/aries-cloudagent-python,](https://github.com/hyperledger/aries-cloudagent-python,) Meetings: [ACA-Pug Meetings](ACA-Pug-Meetings_18484272.html))
  - Aries-Framework-JavaScript ([https://github.com/hyperledger/aries-framework-javascript,](https://github.com/hyperledger/aries-framework-javascript,) Meetings: [Framework JS Meetings](Framework-JS-Meetings_18482467.html))
    
    - Version 0.3.2 released - [https://www.youtube.com/watch?v=PGgUPPwa63g](https://www.youtube.com/watch?v=PGgUPPwa63g)
    - PR from SICPA for DIDComm v2 on AFJ need help:
      
      - [https://github.com/hyperledger/aries-framework-javascript/issues/1038](https://github.com/hyperledger/aries-framework-javascript/issues/1038)
      - [https://github.com/hyperledger/aries-framework-javascript/pull/1096](https://github.com/hyperledger/aries-framework-javascript/pull/1096)
  - Aries-Framework-Go (Troy) #aries-go ([https://github.com/hyperledger/aries-framework-go,](https://github.com/hyperledger/aries-framework-go,) Meetings: [aries-framework-go](aries-framework-go_18481606.html))
  - Aries VCX ([https://github.com/hyperledger/aries-vcx)](https://github.com/hyperledger/aries-vcx%29)
  - Aries-Framework-DotNet ([https://github.com/hyperledger/aries-framework-dotnet](https://github.com/hyperledger/aries-framework-dotnet))
  - Picos as Aries agents ([https://github.com/Picolab/aries-cloudagent-pico](https://github.com/Picolab/aries-cloudagent-pico))
    
    - Phil Windley has students working on a DIDComm v2 version of ACA-Pico
- Mobile:
  
  - Aries Mobile Agent React Native, aka Aries Bifold ([https://github.com/hyperledger/aries-mobile-agent-react-native,](https://github.com/hyperledger/aries-mobile-agent-react-native,) Meetings: [Aries Bifold User Group Meetings](Aries-Bifold-User-Group-Meetings_18490725.html))
    
    - Bifold Summit Happening now – [Bifold Summit 2023](Bifold-Summit-2023_18500878.html)
    - BCGov has realeased an Aries Bifold version, rebranded w/ BC blue/theme/etc (BC wallet)
  - Aries-MobileAgent-Xamarin aka Aries MAX ([https://github.com/hyperledger/aries-mobileagent-xamarin](https://github.com/hyperledger/aries-mobileagent-xamarin))
- [aries-mediator-service](https://github.com/hyperledger/aries-mediator-service) – a DIDComm Mediator in a Box
  
  - working on Pickup support
- [aries-endorser-server](https://github.com/bcgov/aries-endorser-service) – an Indy Endorser in a Box (in development)
- [Aries-Toolbox](https://github.com/hyperledger/aries-toolbox)
- Aries-SDK-Java
- Ursa ([https://www.hyperledger.org/use/hyperledger-ursa](https://www.hyperledger.org/use/hyperledger-ursa), [https://github.com/hyperledger/ursa](https://github.com/hyperledger/ursa))

## Discussion Topics

- Peer DID Continued Discussion
  
  - [https://hackmd.io/\_Kkl9ClTRBu8W4UmZVGdUQ?view#Base-DID-method-support](https://hackmd.io/_Kkl9ClTRBu8W4UmZVGdUQ?view#Base-DID-method-support)
  - Review of general sentiment
  - did:kerilite update? - Rodolfo
  - define shorter 'synonym' for did:peer:2 dids that can be computed by both sides, used interchangeably after initial exchange.
    
    - did:peer:3 (really, 2.1, or 2 with synonym)
- Issue Credential Protocol Short Circuit
  
  - Daniel to make issue.
  - Issue: [https://github.com/hyperledger/aries-rfcs/issues/774](https://github.com/hyperledger/aries-rfcs/issues/774)
  - Next Steps: 
    
    - Survey of existing impls? Do they care if the proceeding messages happen?
    - New version - based on didcomm v1 or v2?
    - IssueCredential 4.0
      
      - contains DIDComm v2 compatible attachments (from IssueCredential 3.0)
      - also .1 and .2 features from IssueCredential v2.x
      - consider other protocol updates as well.
    - Diagram source link: [https://github.com/hyperledger/aries-rfcs/blob/main/features/0036-issue-credential/credential-issuance.html](https://github.com/hyperledger/aries-rfcs/blob/main/features/0036-issue-credential/credential-issuance.html) (instructions in .md text for 0036)
    - PR Needed
- [PR 775](https://github.com/hyperledger/aries-rfcs/pull/755) - OCA
  
  - Three things without consensus
    
    - 1 - pushback on the image slice
      
      - unhappy with ux compared to first option
    - 2 - need command line interface that converts source oca to an oca bundle
      
      - have a utility that converts the xls file
      - json file merged in for the arise specific stuff
      - SAID (from keri) that are embedded in the resulting file that do not meet spec.
      - May be able to ignore the SAID problem.
      - to fully follow OCA spec we need to fill that gap.
      - that's the goal of the command line utility
    - 3 - how does the issuer/schema publisher publish the bundle? (Discovery)
      
      - Tails file like server?
        
        - Cred Def points to tails file
        - OCA bundle doesn't have that.
      - Schema / Cred Def can't point to it directly.
      - Supplement
        
        - As link
        - As inline attachment
        - Works like a one-shot link
        - Malicious issuer could make link unique per issuer to monitor access
        - requires presentation supplement to make it available to verifier
        - possibly workable but not ideal
      - OCA bundle (similar to cred def) that could be used
        
        - network (indy/chekd/etc) publish oca bundle alongside cred def
        - automation to include when cred def / schema retrieved
      - Use the repository (could be Github) strategy that can be accessed by convention 
        
        - locate in repo by issuerid and schemaid
        - Could have a common OCA repository used for lookup
        - could tolerate multiple repositories
        - governance rules matter for each repository
          
          - acceptance / rejection policy
          - github allows process
          - github privately owned
        - stopgap solution, easy to create but not awesome in the long term
      - links from governance files
        
        - needs some sharing from Indicio to aid understanding
  - Next Steps:
    
    - Merge? Update?
- Issue Credential v2.1 Learning
  
  - Why is this hard?
  - no post-mortem yet
  - fixes could be had in the proposed 4.0
  - parallel message delivery in a protocol is hard?
  - Will revisit after BCGov postmortem
- [Issue 773](https://github.com/hyperledger/aries-rfcs/issues/773) - Mime type inconsistency

## Other Business

## Future Topics

- Thomas - [Nessus DIDComm 0.23.2 First Release](https://github.com/tdiesler/nessus-didcomm/releases/tag/0.23.2)
  
  - Wallet abstraction for AcaPy + Nessus native
  - Camel Http Endpoint for Nessus agent
  - Support for RFC0434 Out-of-Band Invitation V1 &amp; V2
  - Support for RFC0023 Did Exchange V1
  - Support for RFC0048 Trust Ping V1 &amp; V2
  - Support for RFC0095 Basic Message V1 &amp; V2
  - CLI to work with supported protocols and model

<!--THE END-->

- Issue Credential v2.1 learning
- State-of-union of Aries projects
- decorator for redirection after proofs. - existing?

## Action items

## Call Recording

  File Modified

Document generated by Confluence on Nov 26, 2024 11:29

[Atlassian](http://www.atlassian.com/)
