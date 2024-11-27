1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [The Giving Chain](The-Giving-Chain_21957087.html)
6. [Project Plan Giving Chain](Project-Plan-Giving-Chain_21964753.html)
7. [Technical Track](Technical-Track_21957774.html)

# Hyperledger Mentorship Program : Project Requirements for Incubation Status

Created by Bobbi Muscara, last modified on Aug 05, 2021

[Skip to end of metadata](https://lf-hyperledger.atlassian.net/wiki/display/CA/New+Project+Checklist#page-metadata-end)

- Created by [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/display/~tkuhrt/), last modified by [David Boswell](https://lf-hyperledger.atlassian.net/wiki/display/~davidwboswell/) on [May 14, 2021](https://wiki.hyperledger.org/pages/diffpagesbyversion.action?pageId=2392331&selectedPageVersions=25&selectedPageVersions=26 "Show changes")

[Go to start of metadata](https://lf-hyperledger.atlassian.net/wiki/display/CA/New+Project+Checklist#page-metadata-start)

- Set up appointment with Marketing team to devise Name and Logo
- Set up chat channel named #{project-name} (see [Create a Chat Channel](https://lf-hyperledger.atlassian.net/wiki/display/CA/Create+a+Chat+Channel))
- Set up mailing list named `{project-name}@lists.hyperledger.org` (see [Create a Mailing List](https://lf-hyperledger.atlassian.net/wiki/display/CA/Create+a+Mailing+List) and [Add Moderator and/or Owner to Mailing List](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=20548258))
- Set up Wiki space using project space (To be created in the meantime use the [Sample Project Page](https://wiki.hyperledger.org/pages/createpage.action?spaceKey=CA&title=Sample%20Project%20Page&linkCreation=true&fromPageId=2392331) as the home page in a blank space). Name the space `projectname` all lower case.
  
  - Label the page with `project-home` so that it shows up on the main page and project page automatically
  - Configure the sidebar on the space and remove the "Pages", "Blog", and "Space Shortcuts" sections by clicking on the \`-\` sign next to them until they appear as a \`+\` sign. Then save the changes.
  - Edit the [Set Space Permissions for Anon to read only](https://lf-hyperledger.atlassian.net/wiki/display/CA/Set+Space+Permissions+for+Anon+to+read+only) (and only view rights) to anonymous users.
- Add the Wiki space to the "Projects" menu (see [Modify Top-Level Menu](https://lf-hyperledger.atlassian.net/wiki/display/CA/Modify+Top-Level+Menu))
- Work with the project maintainers to determine how source control will be handled and what repositories are needed
- Set up Github repositories
  
  - Should have settings file; [here's an example](https://github.com/hyperledger/fabric/blob/main/.github/settings.yml)
  - Must comply with [common repo structure](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure) (You have two quarters to comply, but it's easier to do up front)
    
    - Please note the repolinter section is in flux right now
- Make sure DCO is turned on
- Make sure Maintainers sign off on NEVER TURNING OFF DCO
- License Scan
- DCO Scan
- Is a security audit needed?
- Create an event on the [TSC calendar](https://lists.hyperledger.org/g/tsc/calendar) for the first quarterly update (see [example](https://lists.hyperledger.org/g/tsc/addevent?eventid=352412&repeatid=0&calstart=2018-12-06)). We normally skip at least one quarter before requiring them to do their first update. That gives them time to get things up and running
- Create an event on the new working group's calendar to remind the subscribers that their TSC update is due (see [example](https://lists.hyperledger.org/g/explorer/addevent?eventid=352423&repeatid=0&calstart=2018-12-06))
- Create a recurring event on the project's calendar for public calls
- Work with the marketing team to develop a project-specific webpage (see [example](https://docs.google.com/document/d/1T3GcfzLXY1PNi6sgXpPDufWlpqGzIFHjg4ejdoVnVbE/edit))
- Work with the creative services team to create a project-specific logo (file Jira ticket similar to this [example](https://jira.linuxfoundation.org/browse/LP-4327), minimum two weeks in advance)
- Work with [pr@hyperledger.org](mailto:pr@hyperledger.org) to create a blog post (minimum two weeks in advance)
- Work with [marketing@hyperledger.org](mailto:marketing@hyperledger.org) on web assets:
  
  - Banner for homepage and greenhouse graphic tagline (if applicable)
  - Short description for Hyperledger projects landing page /projects
  - Extended description for dedicated project page
  - All currently available getting started resource pointers for the project page, i.e., Wiki, Github, WG, Chat, mailing list, video playlists
- Add project maintainers to the [maintainers list](https://lists.hyperledger.org/g/maintainers) and send an introduction message welcoming them to the list
- Send out [welcome email](https://docs.google.com/document/d/1VKLiow7dnWzDC2ePv4b2lYG_WssGetMZX3Temv3PkxA/edit) to the maintainers and invite them to an onboarding call and to the new maintainer orientation call
- Two months after welcome email is sent follow up with maintainers if they have not yet scheduled an onboarding call to see how things are going and if they need help
- Add to [FAQ page](https://lf-hyperledger.atlassian.net/wiki/display/HYP/FAQ)
- Add to [Video Checklist](https://lf-hyperledger.atlassian.net/wiki/display/VID/Videos)

# Overview of Proposal

Hyperledger would benefit from a common repo structure which presents the same elements consistently. This includes:

- README
- SECURITY
- CODEOWNERS
- CODE\_OF\_CONDUCT
- CONTRIBUTING
- LICENSE
- MAINTAINERS
- NOTICES

# Formal Proposal(s)

Adopt [repolinter](https://github.com/todogroup/repolinter) with a policy as in [Fabric PR#630](https://github.com/hyperledger/fabric/pull/630). Each repo will add the same repolint.json file and the CA team (or preferably CI) will periodically run a check to ensure projects are in compliance. Additionally, we should establish a template repository that has LICENSE, NOTICE, CoC and Security default files.

$ npx repolinter ../hyperledger/fabric  
npx: installed 60 in 3.726s  
Target directory: /Users/cbf/dev/hyperledger/fabric  
Ruleset: repolint.json  
Linguist Axiom: Linguist not found in path, only running language-independent rules  
Target directory: /Users/cbf/dev/hyperledger/fabric  
✔ notice-file-exists: found (NOTICE)  
✔ license-file-exists: found (LICENSE)  
✔ readme-file-exists: found ([README.md](http://readme.md/))  
✔ contributing-file-exists: found ([CONTRIBUTING.md](http://contributing.md/))  
✔ code-of-conduct-file-exists: found ([CODE\_OF\_CONDUCT.md](http://code_of_conduct.md/))  
✔ changelog-file-exists: found ([CHANGELOG.md](http://changelog.md/))  
✔ security-file-exists: found ([SECURITY.md](http://security.md/))  
⚠ support-file-exists: not found: ({docs/,.github/,}SUPPORT\*)  
✔ readme-references-license: File [README.md](http://readme.md/) contains license  
✔ binaries-not-present: Excluded file type doesn't exist (\*\*/\*.exe,\*\*/\*.dll,!node\_modules/\*\*)  
✔ test-directory-exists: found (test-pyramid.png)  
✔ integrates-with-ci: found (.github/workflows/trigger.yml)  
⚠ code-of-conduct-file-contains-email: File [CODE\_OF\_CONDUCT.md](http://code_of_conduct.md/) doesn't contain email address  
⚠ github-issue-template-exists: not found: (ISSUE\_TEMPLATE\*, .github/ISSUE\_TEMPLATE\*)  
✔ github-pull-request-template-exists: found (.github/[PULL\_REQUEST\_TEMPLATE.md](http://pull_request_template.md/))  
✔ license-detectable-by-licensee: Licensee identified the license for project: Apache-2.0

[Skip to end of metadata](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Incubation+entry+considerations#page-metadata-end)

- Created by [Ry Jones](https://lf-hyperledger.atlassian.net/wiki/display/~ryjones/), last modified by [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/display/~tkuhrt/) [yesterday at 8:06 PM](https://wiki.hyperledger.org/pages/diffpagesbyversion.action?pageId=54657887&selectedPageVersions=26&selectedPageVersions=27 "Show changes")

[Go to start of metadata](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Incubation+entry+considerations#page-metadata-start)

This document provides information to help people who are considering bringing their projects to Hyperledger for incubation. Specifically, it will outline items that the TSC will take into consideration when evaluating the project, as well as, some best practices that have been followed by other projects prior to the project proposal being submitted to the TSC. Our hope is that this document will smooth the entry process for new projects being proposed. The [project proposal process](https://tsc.hyperledger.org/project-lifecycle.html#proposal) and the [template for project proposals](https://hyperledger.github.io/hyperledger-hip/) are outlined outside of this document. The goal of incubation within Hyperledger is to provide a space for projects that have high potential to grow in the community. Ideas should start in [Hyperledger Labs](https://labs.hyperledger.org/).

# Considerations

When considering projects that are proposed for incubation to Hyperledger, the TSC will consider the following items: codebase, maintainers, sponsors, legal, and overlap with existing projects.

## Codebase

- Code should exist as open source software in some form. Previous accepted projects have come up through labs (e.g., Cactus, Ursa); while others previously had stand alone governance prior to joining (e.g., Besu).
- DCO sign off should exists in the code repository. If not 100% ready, the code must be capable of becoming compliant upon entry (i.e. squash commit).

## Maintainers

- The project should have multiple maintainers. These maintainers need not be from different companies; however, having maintainers from different companies is seen as a positive sign. Proposals with only one maintainer have been rejected by prior TSCs.
- The project should have demonstrable examples of POC/production uses publicly available.
- The project should have the backing of more than one organization/individuals (i.e., the project proposers should be able to demonstrate significant, long term contribution in codebase).

## Sponsors

- Sponsors are advocates for the project. There should be more than one sponsor, and they should be from different organizations. They may or may not be committing resources to the project.

## Legal

- Trademark concerns – project names should not be trademarked by a contributing company or if it is, then the trademark will need to be handed over to Hyperledger. Project names must be approved by the Hyperledger marketing committee
- Projects do not require a name prior to being submitted.
- Codebase should be Apache 2 licensable, without encumbrances
  
  - Non-Apache 2 licensed code is possible, but requires Governing board approval (Section 12 subsection d of the [Hyperledger Charter](https://www.hyperledger.org/about/charter))
  - Special examination should be given to copyleft and non-licensed code.
  - Required patent licensing issues have prevented projects from entering incubation.
  - GPL licensing issues have prevented projects from entering incubation.
- If code does not already have copyright, the code should be modified to include copyright as per [Copyright and License Policy](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Copyright+and+License+Policy) prior to being brought into Hyperledger.

## Overlap with Existing Projects

- The TSC has mentioned that they are not interested in bringing in additional distributed ledger projects. There should be a distinct advantage for a new distributed ledger project. This will be similar for other type of projects. In general, if a project is similar to an existing project, there should be a distinct advantage that the project brings over and beyond the existing project and that this cannot be contributed directly to the existing project.
- New projects should bring something to the table that current projects do not.

# Best Practices

The following best practices have been identified by previous proposals.

- Discuss the new project proposal within the community prior to submitting to the TSC for consideration. You might do this through existing chat channels, mailing lists, or direct communication with members of the community.
- Make sure that any links provided in the proposal are publicly available.

Document generated by Confluence on Nov 26, 2024 14:58

[Atlassian](http://www.atlassian.com/)
