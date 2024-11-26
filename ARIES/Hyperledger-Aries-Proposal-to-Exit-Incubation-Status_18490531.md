1. [Hyperledger Aries](index.html)
2. [Hyperledger Aries](Hyperledger-Aries_18481154.html)

# Hyperledger Aries : Hyperledger Aries Proposal to Exit Incubation Status

Created by Stephen Curran, last modified by Robert Mitwicki on Feb 24, 2021

This document is for the Hyperledger TSC to use in considering whether to have Hyperledger Aries exit incubation status. This document assumes the reader has some knowledge of [Hyperledger Aries](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Hyperledger+Aries+Proposal), the  concept of [Trust over IP](https://trustoverip.org) (ToIP) and the role that Hyperledger Aries plays at Layers 2 and 3 of the [ToIP stack](https://www.evernym.com/wp-content/uploads/2020/05/ToIP-stack-1024x631.jpg). Aries is not a blockchain, but rather a set of protocols and implementations that enable secure communications and the use of verifiable credentials based on Decentralized Identifiers (DIDs) and related public keys that are often stored on blockchains. Aries evolved from work in Hyperledger Indy and some (but not all) implementations depend on both Indy and Hyperledger Ursa, but those are not required for Aries.

Hyperledger Aries was formed in May, 2019 based on this [proposal](https://lf-hyperledger.atlassian.net/wiki/display/HYP/Hyperledger+Aries+Proposal). 

## Contributors Proposing to Exit Incubation:

- [Stephen Curran](https://lf-hyperledger.atlassian.net/wiki/people/557058:d676f135-ecd6-465b-b7eb-f87976bf4569?ref=confluence) – Cloud Compass Computing, Inc., ACA-Py Maintainer, Aries RFC Maintainer
- [Daniel Hardman](https://lf-hyperledger.atlassian.net/wiki/people/557058:d8f2338c-759d-4e0c-bb47-14386507f414?ref=confluence) - SICPA, Aries RFC Maintainer
- [Timo Glastra](https://lf-hyperledger.atlassian.net/wiki/people/5f64a069a1048d0069073500?ref=confluence) - Animo Solutions, Aries Framework JavaScript Maintainer, ACA-Py Contributor
- [Ian Costanzo](https://lf-hyperledger.atlassian.net/wiki/people/5a90a1b054c8ff39bc246426?ref=confluence) - Anon Solutions, Indy SDK Contributor, ACA-Py Contributor, AATH Contributor
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence) - SecureKey, Aries Framework Go Maintainer, TSC member
- [Tomislav Markovski](https://lf-hyperledger.atlassian.net/wiki/people/557058:ee5efbab-32e0-460e-ad0f-e16694c7707c?ref=confluence) - Trinsic, Aries Framework NET Contributor, Indy SDK Contributor
- [Daniel Bluhm](https://lf-hyperledger.atlassian.net/wiki/people/712020:c322d585-d6d2-4479-a990-b91fac45db1c?ref=confluence) - Indicio, Aries Static Agent - Python Maintainer, Aries Toolbox Contributor, APTS Contributor, ACA-Py Contributor
- [Steve McCown](https://lf-hyperledger.atlassian.net/wiki/people/712020:6a16994f-5370-4543-a732-609646e7e665?ref=confluence)  - Anonyome Labs, Aries Contributor, Identity Implementers WG Moderator
- [Sam Curren](https://lf-hyperledger.atlassian.net/wiki/people/557058:1ed5fd92-7e42-4cab-87b1-688e48bc02c2?ref=confluence)- Indicio, Aries Toolbox Maintainer, Aries RFC Maintainer, ACA-Py Contributor
- [Keith Smith](https://lf-hyperledger.atlassian.net/wiki/people/712020:cc600316-1f4b-43a4-b4ea-d4d2ec7a464b?ref=confluence) - IBM, Aries Protocol Test Suite Maintainer, Indy SDK contributor
- [Ajay Jadhav](https://lf-hyperledger.atlassian.net/wiki/people/557058:4c9b11a5-2616-4abe-af94-bbc11c984654?ref=confluence)- AyanWorks, Aries Framework JS Contributor
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence) - Kiva Microfunds, Aries Maintainer
- [Robert Mitwicki](https://lf-hyperledger.atlassian.net/wiki/people/712020:9176fc40-350e-4342-b616-01da76989d8d?ref=confluence)- Human Colossus Foundation, Aries Contributor

## Project Structure

There are four key types of open source elements in the Hyperledger Aries project, as outlined below.

### Aries RFCs

Aries RFCs, managed in the [aries-rfcs](https://github.com/hyperledger/aries-rfcs) repo and the primary output of the Aries Working Group, is a set of interoperable protocols that define the interaction between Aries agents, regardless of the implementer or deployer of the agents. The Aries Interoperability Profile (AIP) RFC defines how a set of Aries RFCs (each at a specific version/commit) describe an interoperability target for separate implementations. AIP 1.0 was approved in January, 2020 and has been implemented by many organizations across the world. AIP 2.0 has been proposed and the Aries Working Group is currently discussing it's final contents and structure.

### Aries Frameworks

Aries Frameworks are open source implementations of the Aries RFCs that can be used to build an Aries Agent. The frameworks implement the Aries interactions with ledger and other agents, and provide an interface to a controller that implements the business logic for a specific agent use case. For example, in a mobile verifiable credential wallet built on Aries, the controller is a User Interface to allow the user to interact with other agents. In an enterprise use case, a controller might be a legacy system containing authoritative information suitable for issuance as verifiable credentials to it's subject – e.g. a database of driver's license data to be issued to drivers.

There are three major Aries frameworks and a number of other frameworks at various levels of maturity. The major implementations are:

- [Aries Framework .NET](https://github.com/hyperledger/aries-framework-dotnet) is a .NET implementation that implements AIP 1.0 that powers both major enterprise deployments (e.g. Trinsic, estatus AG, IDRamp, etc.) and a number of mobile wallets (Trinsic, estatus, LISSI and many of others). Aries Framework .NET currently implements support for Indy ledgers and Indy's AnonCreds verifiable credential format.
- [Aries Cloud Agent Python](https://github.com/hyperledger/aries-cloudagent-python) (ACA-Py) is a Python implementation of AIP 1.0 that powers a number of major Aries enterprise deployments, including those at BC Gov, SICPA, Bosch, BMW and others. ACA-Py currently implements support for Indy ledgers and Indy's AnonCreds verifiable credential format.
- [Aries Framework Go](https://github.com/hyperledger/aries-framework-go) is a pure Go implementation of (the to be finalized) AIP 2.0. Aries Framework Go maintainers (SecureKey and others) choose a ledger-agnostic approach without support for Indy features (and hence, do not support AIP 1.0), but do support other DID methods (including Hyperledger Fabric-based TrustBloc and Sidetree DIDs) and W3C Standard JSON-LD verifiable credentials.

There are also a number of other language-based Aries open source frameworks (JavaScript, Ruby, Java). The [Aries VCX](https://github.com/hyperledger/aries-vcx) framework is a Rust implementation recently derived (by [ABSA](https://www.absa.co.za/)) from the Indy-SDK. Aries Mobile Agent Xamarin (Aries-MAX) is an open source mobile wallet that is built on Aries Framework .NET. As well, there are significant closed source implementations of Aries RFCs by IBM and Evernym.

### Aries Test Suites

There are two Aries test suites that implementers can use to test RFC conformance ([Aries Protocol Test Suite](https://github.com/hyperledger/aries-protocol-test-suite)) and another that tests both RFC conformance and interoperability ([Aries Agent Test Harness](https://github.com/hyperledger/aries-agent-test-harness)). Both are under active maintenance and usage. Aries Agent Test Harness uses GitHub Actions to execute AIP 1.0 tests against various combinations of ACA-Py and Aries Framework .NET from their main branch on a daily basis.

### Aries Shared Components

When Aries was first proposed, there was an expectation that there would be several shared components created that most/all Aries agents would embed. As the community evolved, that has not yet happened to a great degree, with one exception. The decision by groups to focus on their own framework led to a lack of focus on shared components, and a greater focus on getting the Aries RFCs right.

The recently added [Aries Askar](https://github.com/hyperledger/aries-askar), a secure storage component for Aries agents is the first shared component. It can be used to replace the "indy-wallet" storage component used in Indy-centric Aries Frameworks (e.g. Aries Framework .NET and ACA-Py). It's not clear that Aries Askar will be used by other than Aries Cloud Agent Python, and whether other Aries shared components will evolve.  And that's OK.

The lack of progress, and the late realization that they will likely not happen as planned, is one reason why it has taken so long to raise this "exit incubation" request.

## Aries Status Against Project Exit Incubation Criteria

As noted by the range of maturity in the Aries Frameworks, the rationale for exiting incubation will not be based on all the repositories in Aries. Rather, the focus is on the specific major Frameworks (.NET, Python and Go) and the success and global use of the Aries protocols. These are noted in the responses below.

### Minimum requirements

- Legal
  
  - All code has been made available under the Apache License and is free of incompatible dependencies
    
    - **Response**: All Hyperledger Aries frameworks are Apache 2.0 Licenses.
  - Project name has been checked for trademark issues
    
    - **Response**: Checking was done at proposal time, and changes made accordingly. Per [Brian Behlendorf (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/616ecf50702bd0006a5a7c6b?ref=confluence), the review completed is sufficient.
- Community support
  
  - The project must have an active and diverse set of contributing members representing various constituencies
    
    - **Response**: From the Aries Activity Dashboard, in the last 6 months, 9 different organizations made substantial contributions (by commit), with another 10% of the 1,493 commits coming from "Other" and "Unknown" organizations.
    - **Response**: The Aries WG calls continue to draw a good crowd, remain at 1.5 hours per week, with each meeting filled with discussion from start to finish.
    - **Response**: There are many, many non-contributing organizations building on Aries protocols and open source projects.
  - The project is not highly dependent on any single contributor (there are at least 3 legally independent committers and there is no single company or entity that is vital to the success of the project)
    
    - **Response**: There is a solid base and a growing number of organizations involved in Aries development.
  - Release plans are developed and executed in public by the community.
    
    - **Response**: The ongoing work in the Aries Working Group calls, in the Aries RFC, in the implemented AIP 1.0, and in the upcoming AIP 2.0 target demonstrates the release plans that have been made, executed and continue to be defined for 2021 and beyond.
- Sufficient test coverage
  
  The project must include a comprehensive unit and integration test suite and document its coverage. Additional performance and scale test capability is desirable.
  
  - **Response:** Aries Cloud Agent Python currently has (per a recent commit CI run) 2437 unit tests and coverage hovering around 99%. As well, Aries Agent Test Harness runs on demand and daily against main to run RFC protocol level test cases that cover all of AIP 1.0.
  - **Response**: The BC Gov team has a scalable infrastructure (built on Kubernetes) using multiple ACA-Py instances to issues millions of verifiable credentials in as short a time as possible. The most recent execution of that test demonstrated sustained performance of 1200/credentials per minute. The full test has not been run since new shared components (such as Aries Askar) have been available, but preliminary results suggest that the sustained performance will improve.
  - **Response**: Aries Framework Go has 89% unit test coverage (as reported by [codecov](https://codecov.io/gh/hyperledger/aries-framework-go)) and additionally has a suite of integration/bdd tests. AFG also includes tests against specification test suites (currently Verifiable Credential Data Model): [Aries Framework Go Test Reports](Aries-Framework-Go-Test-Reports_18490589.html).
- Sufficient user documentation
  
  The project must including enough documentation for anyone to test or deploy any of the modules.
  
  - **Response:** Aries Cloud Agent Python has sufficient documentation and documented demonstration scenarios that developers can have running code in a matter of minutes at the command line and API level. Demonstrations can be run using docker in the browser (using Play-With-Docker) to include ACA-Py to ACA-Py tests and tests using 3rd-party Aries mobile wallets downloaded from The App Store and Google Play.
  - **Response**: The Linux Foundation edX course "[Becoming an Aries Developer](https://www.edx.org/course/becoming-a-hyperledger-aries-developer)" provides a sound grounding in the Aries development.
  - **Response**: There are a number of example Aries apps available for demonstration from organizations like BC Gov, Trinsic, Evernym.
- Alignment
  
  - Requirements fulfillment
    
    The project must document what [requirements and use cases](https://wiki-archive.hyperledger.org/groups/requirements/requirements-wg) it addresses.
    
    - **Response**: The Aries RFCs repository, clearly documents the use case and protocols Aries addresses. As well, there are a number of resources on the Internet that describes at a full range of levels the goals of Trust over IP, Self-Sovereign Identity (SSI) and related uses of Aries Agents. The COVID-19 pandemic and the need for trust information about testing and vaccine has brought Aries use cases to the mainstream.
  - Architecture
    
    The project must document how it fits within the [Hyperledger Architecture](https://lf-hyperledger.atlassian.net/wiki/display/AWG/)
    
    - **Response**: To be determined.
  - Compatibility with other Hyperledger projects
    
    Where applicable, the project should be compatible with other active projects.
    
    - **Response**: ACA-Py, Aries Framework .NET and several other frameworks integrate closely with Hyperledger Indy and Ursa. In theory, Aries is agnostic to the ledger (other mechanism) on which is stored the necessary DIDs and cryptographic material to support verifiable credential exchange.
    - **Response**: Aries Framework Go is ledger-agnostic. Users of the framework can bring their own DID methods (and underlying ledgers) and the framework features such as Verifiable Credentials are also agnostic to the DID method (and underlying ledgers). We have also demonstrated integration with a DID method [implementation](https://github.com/trustbloc/sidetree-fabric) that uses Hyperledger Fabric as its public ledger.
  - Release numbering: the project should use the [Hyperledger standard release taxonomy](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Release+Taxonomy), once that is agreed upon.
    
    - **Response**: All major Aries frameworks use semvar versioning schemes, with a long history of appropriately numbered releases. For example, Aries Cloud Agent Python had 11 releases in calendar 2020 and has had 5 minor releases since launch. Aries Framework Go had [5 releases](https://github.com/hyperledger/aries-framework-go/releases) in calendar 2020.
    - **Response**: The achievement and demonstration of AIP 1.0 conformance by multiple implementers was (in retrospect) sufficient to be declared "1.0".
  - Project must make a release, even a “developer preview”, before graduation.
    
    - **Response**: Each Aries framework will consider this and decide on how to transition to release 1.0.0.
- Infrastructure
  
  - Gerrit or Github repo has been created
    
    - **Done**.
  - Mailing lists have been created and are archived
    
    - **Done** and active.
  - Other communication means used, such as slack channels, are set up
    
    - **Done** and extremely active.
  - Project is set up with Continuous Integration
    
    - **Response**: The major Aries frameworks all have full CI/CD and generate all necessary artifacts for application developers to build.
  - All information necessary for someone to join the community and be able to start contributing is duly documented (location of repo, list of maintainers, mailing lists addresses, slack channels if used, etc) following the Hyperledger Project standard practice ([CONTRIBUTING.md](http://CONTRIBUTING.md), MAINTAINERS.txt, etc)
    
    - **Response**: Most of the repolinter information is there for ACA-Py. Updates to come to ensure everything is there.
    - **Response**: Aries-Framework-Go is running repolinter ([rules](https://github.com/hyperledger/aries-framework-go/blob/main/.repolint.json)).
- CII Badge 
  
  A team seeking to graduate from incubation shall have started the CII Badge application and be nearly complete with incomplete badge requirements referenced in their graduation proposal. 100% of the applicable criteria for the CII Badge is a requirement for releasing a 1.0 of the project. That does not mean the project must have 100% of all criteria, just 100% of the applicable criteria. This is to allow for projects such as test harnesses, that have “N/A” answers for questions that don't offer that as an option.
  
  - **Response**: The Aries Project CII Badge can be found here: [https://bestpractices.coreinfrastructure.org/en/projects/4088](https://bestpractices.coreinfrastructure.org/en/projects/4088)
    
    - [![](https://bestpractices.coreinfrastructure.org/projects/4088/badge)](https://bestpractices.coreinfrastructure.org/projects/4088)
    - The only item missing from the criteria is the dynamic code analysis – fuzzing.

### Additional considerations

In addition to the above, requirements such as the following may be defined at the onset of the project and considered as goals to be met to exit incubation:

- Sufficient real world use
  
  The project should be used in real applications and not just in demos. Because not all real applications may be discussed publicly, in such cases statements providing as much details as possible should be made.
  
  - **Response**: Government of British Columbia's OrgBook is in production using multiple instances of ACA-Py to issue verifiable credentials to an enterprise holder (wallet).
  - **Response**: SecureKey uses aries-framework-go in several [TrustBloc](https://github.com/trustbloc/) projects as a verifiable credential agent &amp; wallet framework and for verifiable credential handling. Aries Framework Go is used within servers, within mobile (via gomobile build) and within the browser (via WASM build). SecureKey has also built DID method integration for Hyperledger Fabric, used the framework with other DID methods, and are also working towards a new ledger-agnostic DID method ([did:orb](https://trustbloc.github.io/did-method-orb/)) that we plan to integrate to aries-framework-go. We have also included components that consume Aries-Framework-Go in an interoperability plugfest (example: [w3c ccg](https://github.com/w3c-ccg/vc-http-api/tree/master/packages/plugfest-2020/vendors/trustbloc)).
  - **Response**: Evernym has implemented AIP 1.0 in its Connect.Me mobile credential wallet app (currently available for download on Android and iOS).
  - **Response**: Evernym has implemented AIP 1.0 in its Verity verifiable credentials platform product, which currently serves 400+ customers.
  - **Response**: Lumedic has begun issuing COVID-19 vaccination credentials within the Providence Healthcare Organization using AIP 1.0.
  - **Response**: The National Health Service in the UK is issuing Aries-compatible vaccinator certification credentials to healthcare and military personnel as part of their push to vaccinate the public for COVID-19.
  - **Response**: Credit unions in the US have been using the MemberPass mobile credential wallet app, implements AIP 1.0, to issue credit union membership credentials to their members since late 2020.
- Sufficient scalability
  
  The project must demonstrate sufficient scalability and document its scalability over various dimensions such as:
  
  - Maximum number of transactions per second
    
    - **Response**: Current highest transactions rate is 1200 issued verifiable credentials per minute using the AnonCreds format, however, multiple options for scaling are available.
  - Maximum number of transactions per chain
    
    - **Response**: N/A
  - Maximum size of a block
    
    - **Response**: N/A
- Minimum test code coverage expected, such as, for example:
  
  - Minimum coverage for Security &amp; cryptography
    
    - **Response**: Some Aries frameworks embed Hyperledger Ursa for cryptography. Other cryptographic components are embedded libraries. No cryptographic components are developed in Aries implementations.
    - **Response**: A great deal of the focus of the lowest level Aries protocols (DIDComm) was built based on security best practices using guidance from a number of experts in a variety of organizations.
  - Minimum coverage for other functionality
    
    - **Response**: As noted, ACA-Py has about 99% unit test coverage (per codecov) and a full integration test library at the Aries protocols level covering AIP 1.0.
  - Minimum coverage for Business logic/smart contract
    
    - **Response**: N/A

Document generated by Confluence on Nov 26, 2024 11:28

[Atlassian](http://www.atlassian.com/)
