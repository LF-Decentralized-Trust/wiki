1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)
5. [2019 Meeting Notes](2019-Meeting-Notes_19464916.html)

# Hyperledger Indy : 2019-06-03 Indy Maintainers Call

Created by Nathan George, last modified on Jun 03, 2019

## Summary

First time doing notes on the wiki

## Date

03 Jun 2019

## [Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

## Attendees

NameOrganizationEmail[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)Cloud Compass/BC Govswcurran@cloudcompass.caNathan GeorgeSovrin Foundationnathan@sovrin.orgMichael LodderSovrin Foundationmike@sovrin.orgThomas SheltonIndependenttwshelton@hrtoolbox.comSam CurrenSovrin Foundationsam@sovrin.orgRichard EsplinEvernymrichard.esplin@evernym.comCam ParraKivacamilop@kiva.org

## Announcements

## Agenda

WhoNotesSummary of Prior callEverybody  
What is the schedule for creating Aries repos and moving contentDaniel and Sam  
Reception of Aries project and timeline for Indy migrationSam

Cred Def 2.0, Revocation Registry 2.0

Mike

Dependency preventing Ubuntu 18.04?  Bounty?

HIPEs, Aries-RFCs, Ursa-RFCs, Sovrin SIPs, docs folders

(How do we manage the multiple locations)

## Notes

- Indy-SDK-lang repositories created as Aries-SDK-lang repos:
  
  - aries-sdk-python: Sam Curren (telegramsam), Andrew Whitehead (cywolf)
  - aries-sdk-ruby: John Callahan (johncallahan)
  - aries-sdk-go: Arjan Van Eersel (arjanvaneersel)
  - aries-sdk-ios (Objective-C and Swift): Steve McCown (smccown)
  - aries-sdk-android: Mike Lodder (mikelodder7)
  - aries-sdk-dotnet: Tomislav Markovski (tmarkovski), Thomas Shelton (twshelton)
  - Needed:
    
    - aries-sdk-java: maintainer(s)
    - aries-sdk-android: co-maintainer
    - aries-sdk-ios: co-maintainer
    - aries-sdk-javascript (Node and client side JS): Joe Genereux (thedolie)? Kyle's friend?
- Also: aries-sdk: Sergey Minaev (jovfer), Artem Ivanov (Artemkaaas), Sam Curren (telegramsam)
- Reception of Aries project
  
  - Generally positive.
  - Concerns from DIF crew about Aries being in Hyperledger.
    
    - Want as large a contributor community as possible
    - But don't want to slow down forward progress with governance questions
    - Create an Aries DIDComm working group might help DIF participants?
      
      - Probably won't help.
- Timeline for Indy migration to Aries.
  
  - Future of LibVCX? Will be discussed in the Indy SDK WG on Wednesday.
  - Indy SDK vs Aries SDK? Will be discussed in the Indy SDK WG on Wednesday.
  - Indy Agent Test Framework becomes Aries DIDComm Test Framework
    
    - DIDComm or DIDComms ? Will decide in the Aries call.
- Cred Def and Revocation Registry 2.0
  
  - Does the Issuer decide how an attribute is encoded to a cryptographic value?
    
    - Anoncreds 1.0: If it is a number, take it. If not, sign the SHA256.
    - Anoncreds 2.0: Needs to work with Schema 2.0 (attribute mapping to the cryptographic integer that gets signed)
    - Allowing every Issuer to do something different reduces the reusability of the schema.
      
      - But issuers might have different standards for things.
      - But an issuer can always create a new schema.
  - How quickly can we deprecate the current approach in favor of the new approach?
    
    - Need a detailed architectural review before making a decision.
- Documentation:
  
  - Need a SIP for Transaction Author Agreement explaining policy needs.
  - Need better documentation for Indy Node.
    
    - Evernym video:

## Next Week

- Documentation: (a conversation for the US / Europe group, already had it with US / Asia)
  
  - Where to document changes? HIPEs/Repo Docs/Jira Tickets
  - PR's should link back to Jira tickets

## Action items

## Call Recording

## Attachments:

![](images/icons/bullet_blue.gif) [GMT20190508-190433\_Indy-Agent.txt](attachments/19464281/19464919.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464281/19464917.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/19464281/19464918.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
