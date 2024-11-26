1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2019 Aries Working Group Meetings](2019-Aries-Working-Group-Meetings_18511496.html)

# Hyperledger Aries : 2019-06-19 Aries Working Group Call

Created by Sam Curren, last modified on Jun 20, 2019

## Summary:

Non-repudiable Signatures, Indy Catalyst Agent as Aries Agent Codebase, HIPE → RFC Status, Static Agent Demo

## Note: This call is Recorded. Recordings posted at the bottom of the page.

## Date

19 Jun 2019

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

[Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Attendees

NameOrganizationEmailSam CurrenSovrin Foundationsam@sovrin.orgTobias LookerMattrtobias.looker@mattr.global[George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)SecureKey Technologiesgeorge.aristy@securekey.comMike RichardsonStarlings Globalemerysolutions@yahoo.co.ukLine Kofoedbloqzoneline.kofoed@bloqzone.com[Albert Solana Berengué](https://lf-hyperledger.atlassian.net/wiki/people/70121:0b2fa4b3-a9eb-4eb8-b319-d96c4647750d?ref=confluence)Validated Idalbert.solana@validatedid.com

[Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)

Sovrin Foundationdaniel.bluhm@sovrin.org

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)

Cloud Compass/BC Govswcurran@cloudcompass.ca

[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence)

Anonyome Labssmccown@anonyome.comTroy RondaSecureKey Technologiestroy.ronda@securekey.comMoushmi BanerjeeNutanix moushmi.banerjee@nutanix.com

[Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)

Lab10 Collectiverobert@lab10.coop

[Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)

Mattr Globalkyle.denhartog@mattr.global[Paul Knowles](https://lf-hyperledger.atlassian.net/wiki/people/5ee0fc649583380ab0b222ee?ref=confluence)Dativapaul.knowles@dativa.comKeith SmithIBMbksmith@us.ibm.com

[Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence)

Sovrin Foundationadan@sovrin.org[Daniel Hardman](https://lf-hyperledger.atlassian.net/wiki/people/557058:d8f2338c-759d-4e0c-bb47-14386507f414?ref=confluence)Evernymdaniel.hardman@evernym.com

## Announcements

- BC Gov is interested in collaborating with groups working on Mobile Agents that could be ready for a live implementation at the end of the summer. Contact [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence).
- Community project: Aries RFCs - [process to move HIPES](https://docs.google.com/document/d/1BKLR6lmjuwmHrYldNELijddJYi43IJByBXSMQgIHSYM/edit?usp=sharing); RFCs that have been moved [concepts](https://github.com/hyperledger/aries-rfcs/tree/master/concepts) / [features](https://github.com/hyperledger/aries-rfcs/tree/master/features) / [pull requests](https://github.com/hyperledger/aries-rfcs/pulls).
- Aries-sdk-* Repos Created: [https://github.com/hyperledger?utf8=%E2%9C%93&amp;q=aries-sdk&amp;type=&amp;language=](https://github.com/hyperledger?utf8=%E2%9C%93&q=aries-sdk&type=&language=)
- #aries-sdk on chat.hyperledger.org

## Agenda

ItemWhoNotesWelcome / Introductions

Related Meetings Review

Javascript Agent Framework - Getting Started Initial Call

Ursa

Indy Semantics

Non-repudiable signatures demo (10 min)

[Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)

Indy Catalyst Agent as new Aries Codebase (30 min)

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)

HIPE → RFC Process (20 min)

[Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)

[https://github.com/hyperledger/indy-hipe](https://github.com/hyperledger/indy-hipe)

[https://github.com/hyperledger/aries-rfcs](https://github.com/hyperledger/aries-rfcs)

Static Agent Demo (15 min)

[Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)

[https://github.com/TelegramSam/aries-staticagent-python](https://github.com/TelegramSam/aries-staticagent-python)

Open Discussion

## Next Week

- Architecture of Indy/Aries SDK Split: Evernym is putting together a proposal, but that shouldn't stop others from putting together proposals. [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)
- Aries meetings: Starting an Asia-Pacific friendly meeting and / or an America-Europe friendly meeting (off-week from Indy Working Group, or taking the place of the Indy SDK Working Group)? [Tobias Looker](https://lf-hyperledger.atlassian.net/wiki/people/712020:6b4b9e75-c537-4af4-b498-bd8e8b96dc37?ref=confluence) [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)
- Lessons learned from Indy SDK Working Group on keeping meetings focused on action: work reports and release planning [Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)

## Future Topics

## Action items

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [GMT20190619-190417\_Aries-WG-C.txt](attachments/18481388/18511657.txt "Download")

Jun 20, 2019 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [GMT20190619-190417\_Aries-WG-C.txt](attachments/18481388/18511657.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481388/18511655.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481388/18511656.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
