1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)
3. [Meetings](Meetings_18481222.html)
4. [Aries Working Group](Aries-Working-Group_18481228.html)
5. [2019 Aries Working Group Meetings](2019-Aries-Working-Group-Meetings_18511496.html)

# Hyperledger Aries : 2019-06-05 Aries Working Group Call

Created by Sam Curren, last modified on Jun 06, 2019

## Summary:

Mobile Links, Protocols, Service Decorator, Connect Protocol (DID Exchange Protocol), Renaming Wallet, LOX

## Note: This call is Recorded. Recordings posted at the bottom of the page.

## Date

05 Jun 2019

## Anti-Trust Policy:

Linux Foundation meetings involve participation by industry competitors, and it is the intention of the Linux Foundation to conduct all of its activities in accordance with applicable antitrust and competition laws. It is therefore extremely important that attendees adhere to meeting agendas, and be aware of, and not participate in any activities that are prohibited under applicable US state, federal or foreign antitrust and competition laws.

Examples of types of actions that are prohibited at Linux Foundation meetings and in connection with Linux Foundation activities are described in the Linux Foundation Antitrust Policy available at [http://www.linuxfoundation.org/antitrust-policy](http://www.linuxfoundation.org/antitrust-policy). If you have questions about these matters, please contact your company counsel, or if you are a member of the Linux Foundation, feel free to contact Andrew Updegrove of the firm of Gesmer Updegrove LLP, which provides legal counsel to the Linux Foundation.

[Hyperledger Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595281/Hyperledger+Code+of+Conduct)

## Attendees

NameOrganizationEmailSam CurrenSovrin Foundationsam@sovrin.orgTroy RondaSecureKey Technologiestroy.ronda@securekey.com[Daniel Hardman](https://lf-hyperledger.atlassian.net/wiki/people/557058:d8f2338c-759d-4e0c-bb47-14386507f414?ref=confluence)Evernymdaniel.hardman@evernym.com[Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)Sovrin Foundationnathan@sovrin.org[Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence)Anonyome Labssmccown@anonyome.comAlexi FalquierSpaceman IDalexis@spaceman.id

[Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)

Mattrindy@kyledenhartog.comTobias LookerMattrtobias.looker@mattr.global

[Adam Burdett](https://lf-hyperledger.atlassian.net/wiki/people/557058:089ba491-66a4-4ec7-a78b-6be560fa21ca?ref=confluence)

Sovrin Foundationadam@sovrin.org[George Aristy](https://lf-hyperledger.atlassian.net/wiki/people/712020:a54e9044-6519-4da3-84ed-b85f302c0029?ref=confluence)SecureKey Technologiesgeorge.aristy@securekey.com

[Ken Ebert](https://lf-hyperledger.atlassian.net/wiki/people/70121:2cc4df0e-16de-40dc-ba52-09649099759a?ref=confluence)

Sovrin Foundationsken@sovrin.org[Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)Lab10 Collectiverobert@lab10.coop[Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence)Sovrin Foundationdaniel.bluhm@sovrin.org

[Richard Esplin](https://lf-hyperledger.atlassian.net/wiki/people/712020:8b35bfaa-715c-4137-8dbd-c4fdab87b671?ref=confluence)

Evernymrichard.esplin@evernym.comAlex Blombloqzonealexander.blom@bloqzone.com[Oliver Terbu](https://lf-hyperledger.atlassian.net/wiki/people/557058:1b0b89c4-350c-41f9-9260-1ef40f38fec7?ref=confluence)uPortoliver.terbu@consensys.net[Mike Lodder](https://lf-hyperledger.atlassian.net/wiki/people/557058:23b28066-a30e-4a6b-9b86-34dae49fd7f0?ref=confluence)Sovrin Foundationmike@sovrin.orgMoushmi BanerjeeNutanixmoushimi.banerjee@nutanix.com[Audrius R](https://lf-hyperledger.atlassian.net/wiki/people/557058:91e2e94f-24f3-45b6-a3e4-28703955486a?ref=confluence)123c Consultingaudrius@123c.eu

## Announcements

- BC Gov is interested in collaborating with groups working on Mobile Agents that could be ready for a live implementation at the end of the summer. Contact [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence).
- Community project: Aries RFCs - [process to move HIPES](https://docs.google.com/document/d/1BKLR6lmjuwmHrYldNELijddJYi43IJByBXSMQgIHSYM/edit?usp=sharing); RFCs that have been moved [concepts](https://github.com/hyperledger/aries-rfcs/tree/master/concepts) / [features](https://github.com/hyperledger/aries-rfcs/tree/master/features) / [pull requests](https://github.com/hyperledger/aries-rfcs/pulls).
- Aries-sdk-* Repos Created: [https://github.com/hyperledger?utf8=%E2%9C%93&amp;q=aries-sdk&amp;type=&amp;language=](https://github.com/hyperledger?utf8=%E2%9C%93&q=aries-sdk&type=&language=)
- #aries-sdk on chat.hyperledger.org

## Agenda

ItemWhoNotesWelcome / Introductions

Techniques for creating unified Mobile Agent links (15 min)

[Tomislav Markovski](https://lf-hyperledger.atlassian.net/wiki/people/557058:ee5efbab-32e0-460e-ad0f-e16694c7707c?ref=confluence)

Protocols (15 min)

[Daniel Hardman](https://lf-hyperledger.atlassian.net/wiki/people/557058:d8f2338c-759d-4e0c-bb47-14386507f414?ref=confluence)

[http://bit.ly/31eooTc](http://bit.ly/31eooTc)Service Decorator (10 min)Sam Curren[https://github.com/hyperledger/aries-rfcs/tree/master/features/0056-service-decorator](https://github.com/hyperledger/aries-rfcs/tree/master/features/0056-service-decorator)Connect Protocol (10 min)Sam Curren[https://github.com/hyperledger/aries-rfcs/pull/23](https://github.com/hyperledger/aries-rfcs/pull/23)Wallet Name Discussion (5 min)Sam Curren[https://docs.google.com/document/d/1gfIz5TT0cNp2kxGMLFXr19x1uoZsruUe\_0glHst2fZ8/edit#heading=h.dj01ko326kf8](https://docs.google.com/document/d/1gfIz5TT0cNp2kxGMLFXr19x1uoZsruUe_0glHst2fZ8/edit#heading=h.dj01ko326kf8)Lox Layer (15 min)

[Mike Lodder](https://lf-hyperledger.atlassian.net/wiki/people/557058:23b28066-a30e-4a6b-9b86-34dae49fd7f0?ref=confluence)

[https://github.com/hyperledger/aries-rfcs/tree/master/features/0042-lox](https://github.com/hyperledger/aries-rfcs/tree/master/features/0042-lox)--- meeting ended here ---

Non-repudiable signatures demo (10 min)[Kyle Den Hartog](https://lf-hyperledger.atlassian.net/wiki/people/712020:9e8190c6-0788-48e1-a99a-ed6d18b5d34d?ref=confluence)

Open Discussion

## Next Week

## Future Topics

- How to accommodate collaboration in Asia-Pacific timezones
- Architecture of Aries / Indy (split between libaries and libindy)

## Action items

## Call Recording

  File Modified

Labels

- [recording](/wiki/label/ARIES/recording)
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

Text File [GMT20190605-190222\_Aries-WG-C.txt](attachments/18481334/18511609.txt "Download")

Jun 06, 2019 by [Sam Curren](/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2)

## Attachments:

![](images/icons/bullet_blue.gif) [GMT20190605-190222\_Aries-WG-C.txt](attachments/18481334/18511609.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481334/18511607.txt) (text/plain)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/18481334/18511608.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 11:30

[Atlassian](http://www.atlassian.com/)
