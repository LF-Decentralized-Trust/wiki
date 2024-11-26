1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Archived](Archived_21447696.html)

# Technical Oversight Committee : Project Incubation Exit Criteria

Created by Tracy Kuhrt, last modified on Feb 13, 2023

[**The current version of this document is hosted elsewhere.**](https://toc.hyperledger.org/governing-documents/project-incubation-exit.html)

**Hyperledger Governing Process document - do not modify without first getting approval of the [TSC](/wiki/pages/createpage.action?spaceKey=HYP&title=Technical%20Steering%20Committee)**

Accepted by the Technical Steering Committee on 2016/12/01.

## Introduction

The Hyperledger Project has defined a [lifecycle](https://lf-hyperledger.atlassian.net/wiki/spaces/HYP/pages/19595327/Project+Lifecycle) for its projects but this definition does not specify in any detail what it takes for a project to be able to transition from the *Incubation* phase to the *Active* phase.

This document is meant to fill this gap by defining a set of criteria to be considered before moving a project from *Incubation* to *Active*.

It is important to note that *Active* in this case refers to the project itself rather than its product and it is therefore more about the maturity of process than the maturity of the product or General Availability (GA).

For this reason this document defines two sets of exit criteria. The first one is made of requirements expected to be met by all projects before moving to *Active*. The second set lists examples of additional requirements typically defined at the onset of the project as goals to be met to exit incubation. There are expected to be documented in the [Proposal for a Hyperledger Improvement Project (HIP)](https://hyperledger.github.io/hyperledger-hip/). Because not all projects have the same goals, the importance of each criteria and the exact definition of this second set of criteria may vary from one project to another. Ultimately the TSC is responsible for determining whether a project deserves to move to *Active* or not and this decision does not need to be solely based on these exit criteria. The purpose of these exit criteria is to help the TSC in its decision process by informing its members of key aspects of the project.

## Minimum requirements

- Legal
  
  - All code has been made available under the Apache License and is free of incompatible dependencies
  - Project name has been checked for trademark issues
- Community support
  
  - The project must have an active and diverse set of contributing members representing various constituencies
  - The project is not highly dependent on any single contributor (there are at least 3 legally independent committers and there is no single company or entity that is vital to the success of the project)
  - Release plans are developed and executed in public by the community.
- Sufficient test coverage
  
  The project must include a comprehensive unit and integration test suite and document its coverage. Additional performance and scale test capability is desirable.
- Sufficient user documentation
  
  The project must including enough documentation for anyone to test or deploy any of the modules.
- Alignment
  
  - Requirements fulfillment
    
    The project must document what [requirements and use cases](https://wiki-archive.hyperledger.org/groups/requirements/requirements-wg) it addresses.
  - Architecture
    
    The project must document how it fits within the [Hyperledger Architecture](https://lf-hyperledger.atlassian.net/wiki/spaces/AWG)
  - Compatibility with other Hyperledger projects
    
    Where applicable, the project should be compatible with other active projects.
  - Release numbering: the project should use the [Hyperledger standard release taxonomy](Release-Taxonomy_21430846.html), once that is agreed upon.
  - Project must make a release, even a “developer preview”, before graduation.
- Infrastructure
  
  - Gerrit or Github repo has been created
  - Mailing lists have been created and are archived
  - Other communication means used, such as slack channels, are set up
  - Project is set up with Continuous Integration
  - All information necessary for someone to join the community and be able to start contributing is duly documented (location of repo, list of maintainers, mailing lists addresses, slack channels if used, etc) following the Hyperledger Project standard practice (CONTRIBUTING.md, MAINTAINERS.txt, etc)
- CII Badge 
  
  A team seeking to graduate from incubation shall have started the CII Badge application and be nearly complete with incomplete badge requirements referenced in their graduation proposal. 100% of the applicable criteria for the CII Badge is a requirement for releasing a 1.0 of the project. That does not mean the project must have 100% of all criteria, just 100% of the applicable criteria. This is to allow for projects such as test harnesses, that have “N/A” answers for questions that don't offer that as an option.

## Additional considerations

In addition to the above, requirements such as the following may be defined at the onset of the project and considered as goals to be met to exit incubation:

- Sufficient real world use
  
  The project should be used in real applications and not just in demos. Because not all real applications may be discussed publicly, in such cases statements providing as much details as possible should be made.
- Sufficient scalability
  
  The project must demonstrate sufficient scalability and document its scalability over various dimensions such as:
  
  - Maximum number of transactions per second
  - Maximum number of transactions per chain
  - Maximum size of a block
- Minimum test code coverage expected, such as, for example:
  
  - Minimum coverage for Security &amp; cryptography
  - Minimum coverage for other functionality
  - Minimum coverage for Business logic/smart contract

## Acknowledgements

The above borrows from the [ASF’s Minimum Graduation Requirements](http://incubator.apache.org/incubation/Incubation_Policy.html#Graduating+from+the+Incubator).

Document generated by Confluence on Nov 26, 2024 11:24

[Atlassian](http://www.atlassian.com/)
