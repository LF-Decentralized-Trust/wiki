1. [Hyperledger Indy](index.html)

# ![Home Page](images/icons/contenttypes/home_page_16.png) Hyperledger Indy : Hyperledger Indy

Created by Tracy Kuhrt, last modified by Sean Bohan on Nov 14, 2024

**Project**

**Status**

[GRADUATED](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Project+Lifecycle#ProjectLifecycle-incubation)

**CII Badge**

[![](https://bestpractices.coreinfrastructure.org/projects/1983/badge)](https://bestpractices.coreinfrastructure.org/en/projects/1983)

**Description**

Hyperledger Indy provides tools, libraries, and reusable components for providing digital identities rooted on blockchains or other distributed ledgers so that they are interoperable across administrative domains, applications, and any other silo. Indy is interoperable with other blockchains or can be used standalone powering the decentralization of identity.

Hyperledger Indy provides tools, libraries, and reusable components for providing digital identities rooted on blockchains or other distributed ledgers so that they are interoperable across administrative domains, applications, and any other silo. 

Indy is in active development across the following areas: 

Distributed Ledger

- [indy-node](https://github.com/hyperledger/indy-node)
- [indy-plenum](https://github.com/hyperledger/indy-plenum)

Client Tools

*Note: We are in the process of moving our Client Tools work to [Hyperledger Aries](https://lf-hyperledger.atlassian.net/wiki/display/ARIES/Hyperledger+Aries). We recommend engaging with both communities for the time being if you interested in building applications on top of an Indy network.*

- [indy-sdk](https://github.com/hyperledger/indy-sdk)
  
  - The Indy SDK has been deprecated in favor of the Indy and Aries shared libraries.  Please refer to the [Deprecation Notice](https://github.com/hyperledger/indy-sdk#warning-deprecation-notice-warning) for information on the replacement libraries.
- [indy-agent](https://github.com/hyperledger/indy-agent) (superseded by [project aries](https://lf-hyperledger.atlassian.net/wiki/spaces/ARIES/overview))

Shared Components

- [indy-hipe](https://github.com/hyperledger/indy-hipe)
- [ursa](https://github.com/hyperledger/ursa)

Key Characteristics

- Distributed ledger purpose-built for decentralized identity
- Correlation-resistant by design
- DIDs (Decentralized Identifiers) that are globally unique and resolvable (via a ledger) without requiring any centralized resolution authority
- Pairwise Identifiers create secure, 1:1 relationships between any two entities
- [Verifiable Credentials](https://w3c.github.io/vc-data-model/) in an interoperable format for exchange of digital identity attributes and relationships, currently in the standardization pipeline at the W3C
- Zero Knowledge Proofs which prove that some or all of the data in a set of Claims is true without revealing any additional information, including the identity of the Prover

Documentation

- An index of Indy documentation can be [found here](Documentation-Index_19464437.html).
- The documentation of the nitty gritty of the underpinnings of the code is located in the “docs” folder of each repo.
- **Note:** Indy Documentation is in the process of migrating to: [indy.readthedocs.io](https://indy.readthedocs.io/ "https://indy.readthedocs.io/")

Project Management

- Bugs, stories, and backlog for Indy Node (Ledger): [https://jira.Hyperledger.org/projects/INDY](https://jira.hyperledger.org/projects/INDY "https://jira.hyperledger.org/projects/INDY")
- Bugs, stories and backlog for Indy SDK: [https://jira.Hyperledger.org/projects/IS](https://jira.hyperledger.org/projects/IS "https://jira.hyperledger.org/projects/IS")
- Bugs, stories and backlog for reference Indy Agents: [https://jira.Hyperledger.org/projects/IA](https://jira.hyperledger.org/projects/IA "https://jira.hyperledger.org/projects/IA")
- A roadmap showing what the various teams are working on: [Indy Roadmap](https://wiki-archive.hyperledger.org/projects/indy/roadmap "projects:indy:roadmap")
- Production deployments of Hyperledger Indy are listed: [Indy Deployments](https://wiki-archive.hyperledger.org/projects/indy/deployments "projects:indy:deployments")
- Guidelines for reporting issues and working on issues: [How to Contribute](How-to-Contribute_19464766.html)

Repositories

- [https://github.com/Hyperledger/indy-node](https://github.com/hyperledger/indy-node "https://github.com/hyperledger/indy-node")
- [https://github.com/Hyperledger/indy-plenum](https://github.com/hyperledger/indy-plenum "https://github.com/hyperledger/indy-plenum")
- [https://github.com/Hyperledger/indy-sd](https://github.com/hyperledger/indy-sdk "https://github.com/hyperledger/indy-sdk")[k](https://github.com/Hyperledger/indy-sdk)
- [https://github.com/Hyperledger/indy-agen](https://github.com/hyperledger/indy-agent "https://github.com/hyperledger/indy-agent")[t](https://github.com/Hyperledger/indy-agent)

Communication

Mailing List

Sign up for the  [Hyperledger Indy Mailing List here](https://lists.hyperledger.org/g/indy "https://lists.hyperledger.org/g/indy")

Chat (for questions and ephemeral discussions)

Questions are welcome and best asked in Hyperledger Discord.  [Learn more about Hyperledger Discord here](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Our+chat+service), get the invite and check out one of the many Indy project channels. 

# Meetings

## Identity WG Implementors Call

This is the call to discuss how to leverage Indy within your identity solution. More information is on the page [Identity WG Implementors Call](https://lf-hyperledger.atlassian.net/wiki/spaces/IWG/pages/18251863/Identity+Implementers+WG+Call)

Indy Contributors Call

People who want to contribute to Indy should join this call. This does not replace our asynchronous collaboration, but should help us keep everyone up-to-date and moving together.

Calls happen every other week: Europe afternoon / US morning: Monday at 8AM Los Angeles, 11AM New York, 4PM London, 18H Moscow

Location: [https://zoom.us/j/244779296](https://zoom.us/j/244779296)

Discussion items: upcoming releases, current PRs, work that will generate future PRs, architecture changes that will impact downstream teams, project standards, best practices, design, etc.

Agendas: [Indy Contributors Meeting](Indy-Contributors-Meeting_19464913.html)

You can work with us between calls on the [#indy-contributors](https://chat.hyperledger.org/channel/indy-contributors) channel on Rocket Chat.

Calendars

- Add any recurring Indy events to your calendar by navigating to our [public calendar](https://lists.lfdecentralizedtrust.org/g/indy/ics/10925406/1237954293/feed.ics) and clicking on the specific events to add them to your own Google calendar.
- [Hyperledger Calendar of Public Meetings](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595324/Calendar+of+Public+Meetings)

History

- [Proposed](https://docs.google.com/document/d/1YzXz0aM8w7kSp3_ao3ue9tOFwK9paofXbtBptR1Jucg/edit?ts=5893c650) by Steve Fulling and Phil Windley, Sovrin Foundation and Nathan George and Jason Law, Evernym - [Slide Deck](https://docs.google.com/presentation/d/1AFxB6Qu_ayyepIUrUvdqjGzXz6JS6SPms5JNOiTBDas/edit?usp=sharing)
- [Approved](https://docs.google.com/document/d/1Qw4nFyclW0-RlbcSoNa8KUFqR8U8fPRu63OKuirBjDw/edit "https://docs.google.com/document/d/1Qw4nFyclW0-RlbcSoNa8KUFqR8U8fPRu63OKuirBjDw/edit") by the TSC on 2017-03-30
- [Proposed moving from Incubating to Active Status](Request-to-exit-Incubation-status-for-Hyperledger-Indy_19464749.html), [Approved](/wiki/pages/createpage.action?spaceKey=HYP&title=2019%2003%2028%20TSC%20Minutes) by the TSC on 2019-03-28
- TSC Updates: [TSC Project Updates](https://lf-hyperledger.atlassian.net/wiki/spaces/TSC/pages/21430854/TSC+Project+Updates)
- Historical updates: [TSC Project Updates pre-2019](https://lf-hyperledger.atlassian.net/wiki/display/HYP/TSC+Project+Updates)

## Recent space activity

- [![](null/aa-avatar/557058:d676f135-ecd6-465b-b7eb-f87976bf4569 "557058:d676f135-ecd6-465b-b7eb-f87976bf4569")](null/display/~557058%3Ad676f135-ecd6-465b-b7eb-f87976bf4569)
  
  - [Stephen Curran](null/display/~557058%3Ad676f135-ecd6-465b-b7eb-f87976bf4569)
  - [2024-11-19 Indy Contributors Call](2024-11-19-Indy-Contributors-Call_47087617.html "data-linked-resource-id=") contributed Nov 19, 2024
- [![](null/aa-avatar/60998bf1dafdf00068e21bae "60998bf1dafdf00068e21bae")](null/display/~60998bf1dafdf00068e21bae)
  
  - [Char Howland](null/display/~60998bf1dafdf00068e21bae)
  - [2024-12-03 Indy Contributors Call](2024-12-03-Indy-Contributors-Call_56786948.html "data-linked-resource-id=") contributed Nov 19, 2024
- [![](null/aa-avatar/634eef0301c2ff842c15f9e7 "634eef0301c2ff842c15f9e7")](null/display/~634eef0301c2ff842c15f9e7)
  
  - [Sean Bohan](null/display/~634eef0301c2ff842c15f9e7)
  - [Hyperledger Indy](index.html "Hyperledger Indy") contributed Nov 14, 2024
- [![](null/aa-avatar/557058:d676f135-ecd6-465b-b7eb-f87976bf4569 "557058:d676f135-ecd6-465b-b7eb-f87976bf4569")](null/display/~557058%3Ad676f135-ecd6-465b-b7eb-f87976bf4569)
  
  - [Stephen Curran](null/display/~557058%3Ad676f135-ecd6-465b-b7eb-f87976bf4569)
  - [2024-11-05 Indy Contributors Call](2024-11-05-Indy-Contributors-Call_45481985.html "data-linked-resource-id=") contributed Nov 05, 2024
- [![](null/aa-avatar/633ab33e140ba0bf651d1f2f "633ab33e140ba0bf651d1f2f")](null/display/~633ab33e140ba0bf651d1f2f)
  
  - [Renata Toktar](null/display/~633ab33e140ba0bf651d1f2f)
  - [2024-10-22 Indy Contributors Call](2024-10-22-Indy-Contributors-Call_35684353.html "data-linked-resource-id=") contributed Nov 05, 2024

[Show More](/wiki/plugins/recently-updated/changes.action?theme=social&pageSize=5&startIndex=5&searchToken=1&spaceKeys=indy&contentType=page%2C%20comment%2C%20blogpost&cursor=_f_NQ%3D%3D_sa_WzE3MzA4MjQyNTkwMDAsIlx0MzU2ODQzNTMgb1o1UF1BUD5nJ1peYFxcV21nb3RXIGNwIl0%3D) ![Please wait](images/icons/wait.gif)

## Space contributors

- [Stephen Curran](/wiki/display/~557058%3Ad676f135-ecd6-465b-b7eb-f87976bf4569) (7 days ago)
- [Char Howland](/wiki/display/~60998bf1dafdf00068e21bae) (7 days ago)
- [Daniel Bluhm](/wiki/display/~712020%3Ac322d585-d6d2-4479-a990-b91fac45db1c) (7 days ago)
- [Wade Barnes](/wiki/display/~70121%3A166ee094-a2f2-44b4-adee-5c3da3741ff8) (7 days ago)
- [Kim Ebert](/wiki/display/~5f7247c98d88b30075da15a3) (7 days ago)
- [...](# "2 more...")
- [Sean Bohan](/wiki/display/~634eef0301c2ff842c15f9e7) (12 days ago)
- [Renata Toktar](/wiki/display/~633ab33e140ba0bf651d1f2f) (21 days ago)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger\_Indy\_Logo\_Color.png](attachments/19464194/19464712.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Indy\_Logo\_Color.svg](attachments/19464194/19464731.svg) (image/svg+xml)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Indy.png](attachments/19464194/19466785.png) (image/png)  
![](images/icons/bullet_blue.gif) [Hyperledger\_Indy.svg](attachments/19464194/19466787.svg) (image/svg+xml)

Document generated by Confluence on Nov 26, 2024 16:49

[Atlassian](http://www.atlassian.com/)
