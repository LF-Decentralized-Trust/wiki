1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2019 Project Updates](2019-Project-Updates_21447735.html)

# Technical Oversight Committee : 2019 Q3 Hyperledger Aries

Created by Sam Curren, last modified by Silas Davis on Aug 29, 2019

# **Projects**

##### **Language Libraries**

- Python SDK
- JS SDK
- Ruby SDK
- Go Framework
- .Net Framework

##### **Client Tools**

- Aries Cloudagent Python
- Aries Staticagent Python
- Aries Protocol TestSuite

##### **Shared Components**

- aries-sdk

# **Project Health**

Aries is a new project, but with good roots in Indy. Some things have made the transition well (RFCs, Agent code), and some things have been more complicated than anticipated (relevant portions of indy-sdk).

The community is active, and we are actively filling in missing areas.

# **Issues**

### **SDK Migration from Indy**

The launch of project Aries is an important step in encouraging interoperability among the various agent implementations. Aries is now responsible for defining the communication between agents, and will provide language frameworks that people can use to implement agents that comply with Aries standards.

Progress made:

- Hyperledger Aries as the new home for interoperable agent work.
- Previous work in the Indy project has led to quick releases of some Aries components:
- - Aries Cloud Agent - Python,
  - Aries Static Agent - Python,
  - Aries Framework - Go,
  - and the Aries Protocol Test Suite.

Further remediation planned:

- Continue standardizing agent communication protocols in the Hyperledger Aries Project.
- Move the relevant parts of the Indy SDK to become an Aries library that is shared by the Aries language frameworks.
- The remaining parts of the Indy SDK will evolve into a ledger resolver that matches the resolver API defined by Aries.

### **Maturing Support for Language Libraries**

As language libraries develop, we need to establish guides and standards so that the library interfaces  are consistent between languages.

Future work planned:

- Schedule sdk and framework review during community meetings. This will raise awareness of progress as well as development and style decisions. As inconsistencies are identified, work to find common design and resolution.
- Further work on Aries SDK to provide a more common foundation for language libraries.

### **Build Pipelines**

We have not yet build any pipelines for the Aries assets. Part of the challenge here is the wide variety of languages and platforms being served.

Future work planned:

- Choose initial projects for CI/CD pipelines.
- Develop test pipelines for initial projects.

# **Releases**

### **June 2019:**

##### **Aries Staticagent Python 0.2.0**

- Initial Release

### **July 2019:**

##### **Aries Cloudagent Python 0.2.0**

- Initial transfer of project to Hyperledger

##### **Aries Staticagent Python 0.3.0**

- Improved Routing
- Trust Contexts
- Expanded Tests

### **August 2019:**

##### **Aries Cloudagent Python 0.3.1**

- Improved command line options
- Support for Indy Transaction Author Agreements
- Credential flow improvements
- DID Based Invitations
- Multi-use Invitations

##### **Aries Staticagent Python 0.4.0**

- Switched libsodium libaries, easing installation
- Improved Module Definitions

# **Overall Activity in the Past Quarter**

**General**

- Transition related Indy HIPEs to Aries RFCs
- Established two regular community calls: one transitioned from Indy, a new alternate timezone call on a biweekly basis
- Transferred codebases from BCGov and Streetcred
- Aries SDK migration from Indy SDK
- - Significant area of focus
  - Dependant codebases are continuing with Indy SDK as a foundation, with plans to switch to Aries SDK as it matures.
- Development of Protocol Test Suite

# **Current Plans**

##### **General**

- **Credential Exchange Standards:** We will finalize the current version of the Credential Exchange Standards and begin discussion on the next versions. This will allow a fixed target for development while removing the development stress from the standards discussions.
- **Agent Tools and Testing:** The Aries Protocol Test Suite exists already, but with minimal support for the number of protocols currently in several of the adopted codebases. Expansion of these tests will facilitate interoperability between disparate projects.
- **Coordination with DIF Interop Project Efforts:** The Decentralized Identity Foundation has begun a project that involves issuing credentials between various vendors. Aries will play the role of an Enterprise Agent and issuer of credentials.
- **Other features planned:**
- - Open-source Mobile Agent
  - Desktop Agent testing and administration tools

# **Maintainer Diversity**

The weekly Aries call has been maintenance focused, and we have not needed a separate call to coordinate maintenance issues. RFC status and progress is coordinated mostly via these calls and the #aries-maintainers channel on rocketchat.

Contributed codebases have remained the focus of the contributing team with initially few contributions from others in the community. We are working to expand contributions by regularly reviewing project progress and status and inviting others to join efforts as maintainers.

# **Contributor Diversity**

In addition to the weekly call that transitioned from the Indy Agent working group, we have added a bi-weekly US Morning call in order to better serve our European contributors. This has been well attended and will continue.

# **POCs, Pilots, Projects**

Initial projects include:

- BCGov
- [Mattr](https://sovrin.org/use-case-spotlight-verifiable-credentials-from-mattr/)
- [Streetcred](https://sovrin.org/use-case-stretcred/)

# **Additional Information**

- Key channels on Rocket Chat: #aries, #aries-sdk, #aries-maintainers
- Join the Aries Mailing List: [https://lists.hyperledger.org/g/aries](https://lists.hyperledger.org/g/aries)

# Reviewed by

- Arnaud Le Hors
- Baohua Yang
- Binh Nguyen
- Christopher Ferris
- Dan Middleton
- Hart Montgomery
- Kelly Olson
- Mark Wagner
- Mic Bowman
- Nathan George
- Silas Davis

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
