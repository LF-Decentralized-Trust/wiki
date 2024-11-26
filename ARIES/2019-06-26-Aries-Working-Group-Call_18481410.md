1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2019 Aries Working Group Meetings](2019-Aries-Working-Group-Meetings_18511496.html)

# Hyperledger Aries : 2019-06-26 Aries Working Group Call

Created by Sam Curren, last modified by Richard Esplin on Jun 27, 2019

## Summary:

Aries Meeting Schedule / Format: will start a second call for Aries conversation that is during European business hours.

Aries / Indy SDK Split Plan: lots of discussion that will have to be continued.

## Note: This call is Recorded. Recordings posted at the bottom of the page.

## Date

26 Jun 2019

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

[Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Attendees

NameOrganizationEmail

[Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)

Sovrin Foundationdaniel.bluhm@sovrin.org

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)

Cloud Compass Computing/BC Govswcurran@cloudcompass.ca[Paul Knowles](https://lf-hyperledger.atlassian.net/wiki/people/5ee0fc649583380ab0b222ee?ref=confluence)Dativapaul.knowles@dativa.com

[Tobias Looker](https://lf-hyperledger.atlassian.net/wiki/people/712020:6b4b9e75-c537-4af4-b498-bd8e8b96dc37?ref=confluence)

Mattrtobias.looker@mattr.globalMike RichardsonStarlings Globalemerysolutions@yahoo.co.uk

[George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)

SecureKey Technologiesgeorge.aristy@securekey.com[Albert Solana Berengué](https://lf-hyperledger.atlassian.net/wiki/people/70121:0b2fa4b3-a9eb-4eb8-b319-d96c4647750d?ref=confluence)Validated Idalbert.solana@validatedid.com

[Ken Ebert](https://lf-hyperledger.atlassian.net/wiki/people/70121:2cc4df0e-16de-40dc-ba52-09649099759a?ref=confluence) 

Sovrin Foundationken@sovrin.org[Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)Sovrin Foundationnathan@sovrin.org

[Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)

Evernymrichard.esplin@evernym.com

[Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence)

Sovrin Foundationadam@sovrin.org[Thomas Shelton](https://lf-hyperledger.atlassian.net/wiki/people/70121:391f7846-5243-44e4-8a48-c68f027ba2dc?ref=confluence)Independenttwshelton@hrtoolbox.com[Tomislav Markovski](https://lf-hyperledger.atlassian.net/wiki/people/557058:ee5efbab-32e0-460e-ad0f-e16694c7707c?ref=confluence)Streetcredtomislav@streetcred.idBecky Christmanfreelancerebeccachristman@gmail.com[Drummond Reed](https://lf-hyperledger.atlassian.net/wiki/people/70121:f3a4c542-f887-49b3-aac9-7374b4da8e1d?ref=confluence)Evernym[drummond.reed@evernym.com](mailto:drummond.reed@evernym.com)

[Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)

Mattrkyle.denhartog@mattr.globalMoushmi BanerjeeNutanixmoushmi.banerjee@nutanix.com[Audrius R](https://lf-hyperledger.atlassian.net/wiki/people/557058:91e2e94f-24f3-45b6-a3e4-28703955486a?ref=confluence)123c Consultingaudrius@123c.eu[Nader Helmy](https://lf-hyperledger.atlassian.net/wiki/people/5a8b44640e6608334b4676eb?ref=confluence)Danube Technader.helmy@danubetech.comLine Kofoedbloqzoneline.kofoed@bloqzone.comBruno Pontes  
brunospontes@hotmail.comPatrik StasAbsapatrik.stas@absa.co.zaTroy RondaSecureKey Technologies[troy.ronda@securekey.com](mailto:troy.ronda@securekey.com)

## Announcements

- BC Gov is interested in collaborating with groups working on Mobile Agents that could be ready for a live implementation at the end of the summer. Contact [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence).
- BC Gov is posting a "[Code With Us](https://www.bcdevexchange.org/opportunities/cwu/opp-create-a-red-hat-keycloak-identity-provider--idp--capable-of-processing-verifiable-credentials-using-decentralized-identity-technology-created-by-bc-gov-to-authorize-access-to-a-bc-government-digital-service-)" (bounty) opportunity for a developer/team to build an Aries-based Identity Provider (IdP) for an IAM solution (Red Hat's Keycloak). Contact [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence).
- Community project: Aries RFCs - [process to move HIPES](https://docs.google.com/document/d/1BKLR6lmjuwmHrYldNELijddJYi43IJByBXSMQgIHSYM/edit?usp=sharing); RFCs that have been moved [concepts](https://github.com/hyperledger/aries-rfcs/tree/master/concepts) / [features](https://github.com/hyperledger/aries-rfcs/tree/master/features) / [pull requests](https://github.com/hyperledger/aries-rfcs/pulls).
- Aries-sdk-* Repos Created: [https://github.com/hyperledger?utf8=%E2%9C%93&amp;q=aries-sdk&amp;type=&amp;language=](https://github.com/hyperledger?utf8=%E2%9C%93&q=aries-sdk&type=&language=)
- Repo [aries-cloudagent-python](https://github.com/bcgov/aries-cloudagent-python) (aca-py) will be transferred from BCGov to Hyperledger this coming Monday (give or take).
- [aries-staticagent-python on PyPI](https://pypi.org/project/aries-staticagent/) (demoed during last week's call).
- #aries-sdk on chat.hyperledger.org

## Agenda

ItemWhoNotesWelcome / Introductions

[Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence)

[Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) will make sure the call is recorded in Sam's absenceRelated Meetings Review

Ursa - anoncreds 1.0 discussion

Indy Semantics - Schema 2.0 HIPE, Aries Semantics WG? Hold off for the summer.

Brief announcement about Agents and Hubs paper

[Daniel Hardman](https://lf-hyperledger.atlassian.net/wiki/people/557058:d8f2338c-759d-4e0c-bb47-14386507f414?ref=confluence)

See [https://docs.google.com/document/d/1shacUcB9KcdKPmt2yAZkdOKsnsgDBXBewkOomlp7V2c/edit](https://docs.google.com/document/d/1shacUcB9KcdKPmt2yAZkdOKsnsgDBXBewkOomlp7V2c/edit)Aries Meeting Schedule / Format

[Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence) [Tobias Looker](https://lf-hyperledger.atlassian.net/wiki/people/712020:6b4b9e75-c537-4af4-b498-bd8e8b96dc37?ref=confluence)

Starting an Asia-Pacific friendly meeting and / or an America-Europe friendly meeting (off-week from Indy Working Group, or taking the place of the Indy SDK Working Group)?Architecture of Indy / Aries SDK Split

[Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)

IS-1285

Open Discussion

## Next Week

- [Daniel Hardman](https://lf-hyperledger.atlassian.net/wiki/people/557058:d8f2338c-759d-4e0c-bb47-14386507f414?ref=confluence)  - Converting the DIDcomm protocols to use the did:peer method.

## Future Topics

## Action items

- Count of people willing to attend Aries call at 7AM Pacific on Thursday

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [GMT20190626-190131\_Aries-WG-C.txt](attachments/18481410/18511691.txt "Download")

Jul 01, 2019 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [GMT20190626-190131\_Aries-WG-C.txt](attachments/18481410/18511691.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481410/18511689.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481410/18511690.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
