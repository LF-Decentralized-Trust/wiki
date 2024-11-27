1. [CI/CD](index.html)

# CI/CD : Sovrin resource migration

Created by Ry Jones, last modified by Stephen Curran on Apr 07, 2020

## Proposed Approach:

- Decide on approach to take around resource heavy parts of the process:
  
  - Can we use an external ledger to eliminate the need for spinning up a ledger for Indy SDK tests?
  - Can we use version controlled docker images with pre-loaded dependencies to reduce build times?
  - What platforms will we prioritize?
    
    - Notably, we'll do one first (Linux, likely), and then likely MacOS, followed by Windows. The community will decide what to do (or not do) after that.
  - Can we eliminate some of the artifacts - e.g. indy-crypto?
- Convert from Jenkins to either (TBD) GHA or AZP. **Decision**: Per [Brett Logan (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/712020:70fd36cb-f719-40fc-993c-9c3f644b7f10?ref=confluence)it's super easy to switch between the two (just key names are different) and admin overhead is less with GHA.
  
  - This is the big effort - lots of detail and tasking to be done.
    
    - Given the scope of the indy-sdk CI/CD scripts - does anyone know the ballpark effort of this?  Best approach to sharing (or not) the work?
  - Iteratively complete the tasks
- Evaluate the best platform (GHA or AZP or similar) for different pipelines to use long term based on the pipeline requirements.
- Tune the scripts to the selected platform

### Tentative Plan for indy-sdk migration:

- Migrate CI Linux
- Evaluate/possibly refactor ledger interactions (depends on effort of changes per test case)
- Evaluate/possible refactor docker images approach
- Migrate CD Linux
- Migrate Linux artifact publishing
- Migrate MacOS CI
- Migrate MacOS CD
- Migrate Windows CI
- Migrate Windows CD

Ideally, one person does the first four steps, supported through questions to others, and with reviews with a group at the end of each step. After that, we can expand out the work to more people, and we can apply the same approach to the other repos.

## Hyperledger Paid For Resources

- [Artifactory](https://hyperledger.jfrog.io/hyperledger/webapp/#/home)
  
  - [Fabric's migration announcement from Nexus to Artifactory](https://lists.hyperledger.org/g/fabric/message/7604)
  - Supports maven, etc
  - Mostly used for CI
- [Bintray](https://bintray.com/hyperledger-org)
  
  - Has CDN

## Migration Scope: ([from this list](https://lf-hyperledger.atlassian.net/wiki/display/~ryjones/CI+usage#space-menu-link-content))

### Jenkins:

- [indy-sdk](https://github.com/hyperledger/indy-sdk) - [CI Script](https://github.com/hyperledger/indy-sdk/blob/master/Jenkinsfile.ci) * [CD Script](https://github.com/hyperledger/indy-sdk/blob/master/Jenkinsfile.cd)
  
  - Most active and slowest build/test process at 5 hours per PR.
- [indy-node](https://github.com/hyperledger/indy-node) - [CI Script](https://github.com/hyperledger/indy-node/blob/master/Jenkinsfile.ci) * [CD Script](https://github.com/hyperledger/indy-node/blob/master/Jenkinsfile.cd)
- [indy-plenum](https://github.com/hyperledger/indy-plenum) - [CI Script](https://github.com/hyperledger/indy-plenum/blob/master/Jenkinsfile.ci) * [CD Script](https://github.com/hyperledger/indy-plenum/blob/master/Jenkinsfile.cd)
- [indy-crypto](https://github.com/hyperledger/indy-crypto) - [CI Script](https://github.com/hyperledger/indy-crypto/blob/master/Jenkinsfile.ci) * [CD Script](https://github.com/hyperledger/indy-crypto/blob/master/Jenkinsfile.cd)
  
  - **Question**: Ursa is on AZP, so one would think this would be relatively easy to switch?
  - **Question**: On the other hand, can we just eliminate the repo in favour of ursa?

### Nexus:

- rpm publishing

### Debian Publishing - [repo.sovrin.org](http://repo.sovrin.org)

- [repo.sovrin.org](http://repo.sovrin.org/) provides debian packages that are used by the Sovrin Stewards to install Indy Node and a Maven interface for developers.  The former use will need to shift to whatever Steward organization forms as a fallout of the Sovrin Foundation transition. The latter us can be transitioned to Hyperledger resources, with a transition notification to the developer community.

<!--THE END-->

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) Let the MainNet transition team (headed by Riley Hughes) that this is an issue that will need to be addressed by that group.

## Requirements (from this [presentation slide](https://docs.google.com/presentation/d/1SM_2m99KJv6s2ybN9fZKPmwh6gKsmP0okVLe-dy10IY/edit#slide=id.g7e4232c7ca_0_6) from Evernym)

- Linux, Windows, macOS platforms support.
- Triggering builds from GitHub PRs sent from fork.
- Ability to run our integration tests with IndyPool created as docker network on the same machine (maybe there are another solution-related ways)
- Hardware acceleration for Android’s routines (nice to have).
- Ability to passing artifacts through CI/CD jobs/steps (to avoid rebuilding artifacts).
- Run jobs in parallel.
- Ease of scale (ability to insert new runner machine).

## Background Information

### CI/CD Platform Evaluation:

- This [sprint demo reviews Evernym's evaluation](https://www.youtube.com/watch?v=EEHpINC7nqQ&t=398s) of options for CI / CD (tracked in this [JIRA issue](https://jira.hyperledger.org/browse/IS-1496) - login required) where we recommended GitHub Actions based on [this presentation summary](https://docs.google.com/presentation/d/1SM_2m99KJv6s2ybN9fZKPmwh6gKsmP0okVLe-dy10IY/edit#slide=id.p). Discussed on [this Indy Contributors](https://lf-hyperledger.atlassian.net/wiki/display/indy/2020-03-09+Indy+Contributors+Call) call (with a failed recording).
  
  - **Recommendation was GitHub Actions** (and Azure Pipelines where necessary/useful).
  - Additional recommendation from that was to drop the number of supported platforms, particularly in the mobile area.
- Anticipated impacts of moving to GitHub Actions:
  
  - The approach to running a pool for testing will need to be very different from that taken by Jenkins, so the scripts will have to be reworked.
  - Indy SDK currently supports a broad range of environments (Ubuntu, RedHat, Windows, OSX, iOS, Android), but we agreed that we can reduce the number of environments and people who miss those artifacts can contribute those build resources.
  - The testing pipeline takes a long time because there are a lot of tests–was **3.5 hours per PR** with full AWS set of machines, now at **5 hours** with reduced AWS machines, and GitHub Actions is **likely to be slower**.
  - This document covers [findings about using GitHub actions](https://docs.google.com/document/d/1Ts_xLTAtm6blySLVBJmNT-UuxYMzwV4ABtH8agJtnKc/edit) with some useful links as we begin implementations, with expected positives and only technical negative related to managing a docker repo.
- [Feel free to test here](https://github.com/hyperledger-cicd)

### Hyperledger Fabric Experience - from [Brett Logan (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/712020:70fd36cb-f719-40fc-993c-9c3f644b7f10?ref=confluence)

[Hyperledger Fabric Experience - Azure Pipelines vs GitHub Actions](Hyperledger-Fabric-Experience---Azure-Pipelines-vs-GitHub-Actions_19011230.html)

## Lower priority:

Travis:

- aries-framework-dotnet

Circle-CI:

- aries-cloudagent-python
- aries-rfcs
- indy-hipe

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
