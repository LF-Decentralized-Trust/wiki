1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)
5. [Optimising the pipelines using Github Actions for Caliper and Caliper-Benchmarks](Optimising-the-pipelines-using-Github-Actions-for-Caliper-and-Caliper-Benchmarks_21958404.html)

# Hyperledger Mentorship Program : Project Plan - Optimising the pipelines using GitHub Actions for Caliper and Caliper-Benchmarks

Created by Rinish Sam, last modified by d\_kelsey on Oct 25, 2022

## Abstract

The goal of this project is to optimise how Caliper and Caliper-Benchmarks verify PRs and publish artifacts using Github Actions and to improve how testing is done to ensure that the artifacts to be published actually work as expected.

* * *

## Mentor and Mentee

  Mentor

[d\_kelsey](https://lf-hyperledger.atlassian.net/wiki/people/5e3292559029c30ca0bc9620?ref=confluence)

(Discord: NorfolkAndChance #6513)

Mentee

[Rinish Sam](https://lf-hyperledger.atlassian.net/wiki/people/6001d62991bb2e010840450c?ref=confluence)

(Discord: CaptainIRS#2752)

* * *

## Communication Channel

Discord + Email + GitHub

* * *

## Plan

#### Initial Objectives

- Follow Caliper tutorial and document the experience
- Follow Caliper-benchmarks and document the experience
- Document the Azure pipelines used in Caliper
- Port UnitTests Stage to GitHub Actions
- Raise GitHub issues describing remaining work

Caliper Github will be used to define and track the work for this project (And will include shadow issues for the Caliper benchmarks repo). The epics will track the overall project and themes. There are 3 themes. 

- Migrate (Migrate Caliper build to github actions)
- Optimize (Optimize the builds for caliper and caliper-benchmarks)
- Enhance (enhance the builds with new features for caliper and caliper-benchmarks)

  Migrate

- Port to GitHub Actions for
  
  - Unit Tests (PR [caliper#1364](https://github.com/hyperledger/caliper/pull/1364))
  - Integration Tests (PR [caliper#1376](https://github.com/hyperledger/caliper/pull/1376))
- Disable Azure Pipelines for (PR [caliper#1382](https://github.com/hyperledger/caliper/pull/1382)) 
  
  - Unit Tests
  - Integration Tests
- Publish to GitHub Actions (PR [caliper#1384](https://github.com/hyperledger/caliper/pull/1384)) 
  
  - Stable release
  - Unstable release

Optimize

- Caliper
  
  - PR Verification
    
    - Investigate possibility of testing only what has changed (PR [caliper#1421](https://github.com/hyperledger/caliper/pull/1421))
    - Investigate options for caching node modules across workflows ([Approaches for caching node\_modules.docx](attachments/21958940/21967009.docx))
    - Implement caching for node modules (PR [caliper#1406](https://github.com/hyperledger/caliper/pull/1406))
    - Investigate options for caching docker images (see [comment](https://github.com/hyperledger/caliper/issues/1373#issuecomment-1200117974))
    - Implement caching of docker images (draft PR [caliper#1419](https://github.com/hyperledger/caliper/pull/1419))
    - Setup GitHub actions for docs in the gh-pages branch (PR [caliper#1424](https://github.com/hyperledger/caliper/pull/1424))
  - On merge
    
    - Investigate whether Unit Tests should be run on merge (see [comment](https://github.com/hyperledger/caliper/issues/1380#issuecomment-1206332412))
- Caliper Benchmarks
  
  - Investigate whether whole benchmark suite has to be run for all changes (PR [caliper-benchmarks#226](https://github.com/hyperledger/caliper-benchmarks/pull/226))
  - Investigate caching of docker images (see [comment](https://github.com/hyperledger/caliper/issues/1373#issuecomment-1200117974))
  - Investigate caching of caliper install (PR [caliper-benchmarks#225](https://github.com/hyperledger/caliper-benchmarks/pull/225))

Enhance

(Stretch

Goal)

- Migrate the repository to npm workspaces (PR [caliper#1394](https://github.com/hyperledger/caliper/pull/1394))
- Migrate Fabric integration tests to test-network (PRs [caliper#1410](https://github.com/hyperledger/caliper/pull/1410) and [caliper#1414](https://github.com/hyperledger/caliper/pull/1414))
- Remove channel and chaincode operations from Fabric v1 connector (PR [caliper#1411](https://github.com/hyperledger/caliper/pull/1411))
- Test docker images as part of a PR pipeline
- Include node.js dependency checker as part of a PR pipeline
- Investigate publishing to local npm and testing IN PROGRESS
- Investigate replacing current publish process with a more GitHub centric approach
- Publish to ghcr.io
- Refine release process
  
  - Implement automatic version bump
  - Document the process of creating a stable release
- Improve integration tests
  
  - Investigate a better way to setup Fabric during workflows (possibly leverage services in GitHub actions)
  - Investigate ways to cover more of Caliper's capability
  - Cleanup the 3 Fabric packages
- Re-enable Java in Caliper Benchmarks
- Add license checking in caliper-benchmarks
- Other miscellaneous enhancements
  
  - Update dependencies and deliver package-lock.json files IN PROGRESS
  - Create and publish Code Coverage reports (PR [caliper#1428](https://github.com/hyperledger/caliper/pull/1428))
  - Add GitHub actions for security scanning
    
    - CodeQL
    - npm audit
    - Dependabot
  - Investigate nightly builds
  - Discord notifications of build failure using webhooks
  - eslint improvements across all of Caliper

* * *

## Current PRs

## Epic Issues

## Ongoing Issues

# (WIP)

## Attachments:

![](images/icons/bullet_blue.gif) [Approaches for caching node\_modules.docx](attachments/21958940/21967009.docx) (application/vnd.openxmlformats-officedocument.wordprocessingml.document)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
