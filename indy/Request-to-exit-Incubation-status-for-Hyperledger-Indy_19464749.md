1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)

# Hyperledger Indy : Request to exit Incubation status for Hyperledger Indy

Created by Nathan George, last modified on Mar 27, 2019

The community developing Indy believes that it has met the requirements for graduation to an active Hyperledger project. Below are the requirements listed in the [Exit Criteria](https://lf-hyperledger.atlassian.net/wiki/spaces/TSC/pages/21430824/Project+Incubation+Exit+Criteria) document as well as our answers and responses.

- Legal
- - All code has been made available under the Apache License and is free of incompatible dependencies
  - - ✓ All Hyperledger code is available under Apache 2. (see the LICENSE file in Indy repositories)
  - Project name has been checked for trademark issues
  - - ✓ Done.
- Community support
- - The project must have an active and diverse set of contributing members representing various constituencies
  - - ✓ We have developers from the US, Canada, India, Russia, and Europe.
  - The project is not highly dependent on any single contributor (there are at least 3 legally independent committers and there is no single company or entity that is vital to the success of the project)
  - - ✓ Sovrin Foundation, Evernym, Province of British Columbia, Brigham Young University, Deutsche Telekom, Danube Tech, and more.
  - Release plans are developed and executed in public by the community.
  - - ✓
- Sufficient test coverage
- - - ✓ Maintainers to keep high test coverage in our code bases.  When \`libindy\` was last tested, it’s test case coverage was at 94%
- The project must include a comprehensive unit and integration test suite and document its coverage. Additional performance and scale test capability is desirable.
- - - ✓ Indy has comprehensive unit and integration tests on it’s projects. However, collection of test coverage is difficult considering our tech stack. Steven Gubler is actively working on a solution to start collecting these metrics programmatically using a coverage tool that is potentially compatible with our projects (kcov). While this work is being incorporated in to automated processes maintainers need to remain vigilant about keeping high test coverage in all new submissions.
- Sufficient user documentation
- - - ✓
- The project must include enough documentation for anyone to test or deploy any of the modules.
- - - ✓
- Alignment
- - The project must document what [requirements and use cases](https://wiki.hyperledger.org/groups/requirements/requirements-wg) it addresses.
  - - ✓ [Indy Use Cases](https://lf-hyperledger.atlassian.net/wiki/display/indy/Indy+Use+Cases)
  - The project must document how it fits within the [Hyperledger Architecture](https://wiki.hyperledger.org/groups/architecture/architecture-wg)
  - - ✓ [Indy's Project Page](https://lf-hyperledger.atlassian.net/wiki/display/indy/Hyperledger+Indy)
  - Where applicable, the project should be compatible with other active Hyperledger projects.
  - - ✓ Hyperledger Ursa support is underway, and integration with the new Ursa release is expected as soon as merge issues between indy-crypto and ursa 0.1.x can be resolved.
      
    - ✓ Other Hyperledger projects like Fabric and Sawtooth, while very useful projects, lack key functionalities that Indy needs. However, the Indy project is designed with compatibility in mind and is very open to integrations with other Hyperledger projects when possible.  Examples of functionality not fully supported elsewhere includes:
      
      - BFT consensus for full fault tolerance, finality is very important to knowing the correct party owns and controls an identifier and that a credential is (or was) valid at a specific point in time
      - State Proof support allows nodes to verify information contained on the ledger from a single node that contains a copy of the ledger, whether it participates in consensus or not.
        
      - Validator and Observer node tiers - the ability to service read requests from nodes that are not participating in consensus allows agents to do credentials exchange offline and is very important to read request scalability
      
      The Hyperledger Indy team believes that more code reuse and overlap between the frameworks is healthy and desirable.  We are investigating how we can share ledger code with other frameworks or reuse functionality as part of the [#indy-ledger-next](https://chat.hyperledger.org/channel/indy-ledger-next) ("Ledger 2.0") initiative that should gain more momentum August 2019.
  - The project should use the [Hyperledger standard release taxonomy](https://docs.google.com/document/d/1u9pt-bXeOXefYBB1uYE6M-D6CtmkC1lGCjmicSlZgVA), once that is agreed upon.
  - - ✓
  - Project must make a release, even a “developer preview”, before graduation.
  - - ✓ Done.
- Infrastructure
- - Gerrit or Github repo has been created
  - - ✓ [Indy-node](https://github.com/hyperledger/indy-node)
    - ✓ [Indy-sdk](https://github.com/hyperledger/indy-sdk)
    - ✓ [Indy-plenum](https://github.com/hyperledger/indy-plenum)
    - ✓ [Indy-anoncreds](https://github.com/hyperledger/indy-anoncreds)
    - ✓ [Indy-crypto](https://github.com/hyperledger/indy-crypto)
    - ✓ [Indy-agent](https://github.com/hyperledger/indy-agent)
  - Mailing lists have been created and are archived
  - - ✓ Done.
  - Other communication means used, such as slack channels, are set up
  - - ✓ Done: Hyperledger’s RocketChat instance
  - Project is set up with Continuous Integration
  - - ✓ Done.
  - All information necessary for someone to join the community and be able to start contributing is duly documented (location of repo, list of maintainers, mailing lists addresses, slack channels if used, etc) following the Hyperledger Project standard practice ([CONTRIBUTING.md](http://CONTRIBUTING.md) MAINTAINERS.txt etc)
  - - ✓
- CII Badge
- - A team seeking to graduate from incubation shall have started the CII Badge application and be nearly complete with incomplete badge requirements referenced in their graduation proposal. 100% of the applicable criteria for the CII Badge is a requirement for releasing a 1.0 of the project. That does not mean the project must have 100% of all criteria, just 100% of the applicable criteria. This is to allow for projects such as test harnesses, that have “N/A” answers for questions that don't offer that as an option.
  - - ✓

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
