1. [Hyperledger](index.html)
2. [LF Decentralized Trust](LF-Decentralized-Trust_19595266.html)
3. [Policies and Procedures](Policies-and-Procedures_19595414.html)

# Hyperledger : Paid Tooling Policy

Created by Ry Jones, last modified by David Boswell on Oct 31, 2023

[Project and Lab Services - Hyperledger - Hyperledger Foundation](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Project+and+Lab+Services)

Hyperledger provides a number of paid developer tools and services for projects.  Below, we list all of the ones that our projects currently use.  We have divided them up by tiers, which indicate the level of support (and the timeframe of support) that projects can expect from the HLF staff.  We emphasize that just because a tool or service is not on this list does not mean projects cannot use it; it just means that they will have to (mostly) support it themselves.

Our tool list is as follows:

Recommended Tools

In order to help projects that may be looking to get started with using tooling/services, we offer the following general recommendations.  They don't necessarily work for every project, but they should be optimal for most projects.

- Technical Documentation: use markdown, GitHub pages, and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).
- Informal documentation and details (e.g. meeting notes, meeting agendas, long-term planning documentation, etc.):  use the wiki (i.e. Confluence).
- CI: use GitHub Actions.
- Artifact Storage: Use GitHub packages.
- Communication: Use Discord, unless it is blocked in your country.
- Bug tracking: Use GitHub Issues and GitHub Projects.

Long-term Available to All Projects

This describes things that we plan on using for the long term and have no plans to change.

- NPM
  
  - Why:  It's used by many projects.
- Discord
  
  - Why:  It's used by all projects, labs, members, and communities.  It also has fantastic support for people with disabilities.  We have switched our chat program twice in the history of the HLF (from Slack to Rocketchat to Discord) and Discord seems to be by far the most popular platform.  If you don't like Discord (and we know it's impossible to access in certain countries, where we have alternatives), we encourage you to communicate this with the TOC.
- Docker Hub
  
  - Why: It's used by many projects.
- Groups.io
  
  - Why:  AKA lists.hyperledger.org, it is also used by pretty much everyone.

Available to All Projects, Long-term Future in Question

These are tools or services that we have no imminent plans to change, but would like to do so if something else came along that is better.  We explain our rationale below, as well as overall recommendations for alternatives.  We understand that folks might not want to switch if they are already using one of these tools or services, but we would strongly suggest using a recommended alternative if you are looking to begin using one of these.

- Artifactory for artifact storage
  
  - Recommendation:  use GitHub packages instead.
  - Why future in question:  it's quite expensive and difficult to manage.
- ReadTheDocs pro
  
  - Recommendation:  use GitHub pages.
  - Why future in question:  it's very difficult to manage and doesn't offer enough upside compared to just using GitHub pages..
- Confluence
  
  - Recommendation:  We don't have a current recommendation; this is more of a cautionary note–see below.
  - Why future in question:  due to licensing issues, the LF as a whole may move away from Confluence which would obviously affect us.  We just wanted to warn everyone that this might be a possibility.
- MKDOCS
  
  - Background:  Hyperledger sponsors [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/), used by Besu, but available to all projects and labs.
  - Recommendation:  use "plain" markdown + Github pages.  We are aware that MKDOCS is essentially a markdown + Github pages solution with better looking output.  We don't want to explicitly discourage people from using this–if enough projects wanted to use it, we would probably be happy to support it long-term.
  - Why future in question:  not enough projects use it to justify the cost and management overhead.  This might make you more inclined to use it than some of the other things in this category, which is fine!

Legacy

We are supporting the projects that are currently using the tools but not rolling these out to new tools because there are better alternatives now.  Please don't start using these!

- JIRA
  
  - Current Situation: Almost no current projects use Jira.
  - Recommendation: Use Github issues.  We can offer help exporting Jira issues and importing them.
- Azure
  
  - Current Situation: Fabric still uses Azure, although in a very limited way.
  - Recommendation: Use Github actions (GHA); GHA is on the path to obtaining feature parity with AZP and when this happens AZP will no longer be supported.

Currently Unsupported/Unfunded

- CircleCI
  
  - Recommendation:  Use GHA instead.  It is easier to manage and, in the vast majority of cases we have come across, substantially cheaper (yes Besu maintainers, we have seen your math!).
- MacStadium
  
  - Current Situation: We have one M1 mac, used primarily by Solang and Besu Native.
  - Recommendation: If you absolutely need it, please run it on your own hardware.
- ZenHub
  
  - Recommendation: We recommend using GitHub projects instead.
  - Current Situation: This is a free tool some projects choose to use but we don't offer support for it.  You should feel free to use it if you like, but the staff will unfortunately not have the bandwidth to help with any issues.

Finally we emphasize that this list does not cover security-related tools or services.

Document generated by Confluence on Nov 26, 2024 16:46

[Atlassian](http://www.atlassian.com/)
