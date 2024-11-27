1. [Community Architects](index.html)
2. [Community Architects Team](Community-Architects-Team_20545564.html)
3. [Works in Progress](Works-in-Progress_20561000.html)

# Community Architects : Hyperledger Glossary for marketing

Created by Ry Jones, last modified by Silona Bonewald on Mar 22, 2019

- **What is a project?**
  
  - **A project is a top-level DLT or component that has been ratified by the TSC.**
  - **Projects should ship**
  - **The bar for new projects is high.**
    
    - **Burrow**
    - **Fabric**
    - **Indy**
    - **Iroha**
    - **Sawtooth**
    - **GRID (should be a sub-project of Sawtooth, or a lab)**
  - What are the benefits?
  - What kind of Support does it get?
- What is a sub-project?
  
  - What are the benefits?
  - What kind of Support does it get?
  - What is the relationship to the Project?
- **What is a tool?**
  
  - **A tool is a project that works with one or more of the DLT projects, as ratified by the TSC.**
  - **Tools should ship**
  - **The bar for new tools is lower than projects, but still high**
    
    - **Caliper**
    - **Cello (should be a sub-project of Fabric)**
    - **Composer (should be sub-project of Fabric, or a lab)**
    - **Explorer (probably a sub-project of Fabric)**
    - **Quilt (should be a lab)**
    - **URSA**
- **Proposed Current State of the World**
  
  - **Projects**
    
    - **Burrow**
      
      - Burrow is a top-level DLT designed to bring support for the Ethereum smart contract standard to permissioned blockchains.
      - Burrow is interroperable with Sawtooth and has planned interop with Fabric.
    - **Fabric**
      
      - **Cello**
        
        - Cello is a tool for provisioning DLT networks. Currently it can only provisions Fabric networks.
        - Cello plans to support provisioning other DLT networks by supporting Kubernetes.
      - **Composer**
        
        - Composer is a tool for designing business logic and translating it into DLT smart contracts.
      - **Explorer**
    - **Indy**
      
      - **Ursa**
    - **Iroha**
    - **Sawtooth**
      
      - **Grid**
  - **Labs**
    
    - **Quilt**
- What is a Library?
- What is a framework?
- What is a Platform?
- How a sub-project can graduate into top-level project?
  
  - Demonstrate interop across multiple existing top-level projects.
- Different Levels of interop for each?
  
  - Platform have a ready SDK
  - Full support for API across multiple platforms
  - Information exchange level VS asset exchange level
  - Different levels?
    
    - Level 1 – show roadmap and/or prototype code for talking to multiple DLT platforms (not necessarily Hyperledger)
    - Level 2 – demonstrate working code.
    - Level 3 – active tracking of API changes with automatic detection via routine CI/CD compatibility testing.
  - Different types of interop
    
    - Interfacing with one only one DLT at a time, but capable of talking to multiple DLTs.
      
      - Example: Explorer should be able to talk to all DLTs but it's purpose is to talk to one at a time.
      - Example: Caliper should be able to measure perf of multiple DLTs (not exclusive to HL) but it's purpose is to talk to one at a time.
    - Interfacing across multiple DTLs at the same time.
      
      - Example: Quilt needs to talk to multiple DLTs at the same time to lock an asset in one DLT and create it in another at the same time.
- What are the interop requirements for Tools and Libraries?
- Can we reward platforms for being interop with other platforms?
- **What is a SIG?**
  
  - **A SIG is a group of people that want to discuss a particular area where blockchains may be useful.**
  - **They may produce white papers, use cases, or code.**
  - **SIGs may or may not ship**
  - **SIGs consist of SMEs for the vertical of the SIG**
  - **SIGs are governed by ECO**
    
    - **Healthcare**
    - **Public Sector**
    - **Social Impact**
    - **Telecom**
    - **Trade Finance**
- **What is a WG?**
  
  - **A WG is focused on guiding development in specific areas**
  - **A WG may or may not ship**
  - **A WG develops guidelines and frames the expertise of the SMEs more broadly so they can work in a wider scope than an individual project**
    
    - **Architecture**
    - **Identity**
    - **Learning Materials**
    - **Perf &amp; Scale**
    - **Smart Contracts**
    - **TWGC is probably a sig? It's somewhere between a WG and a SIG. It is a Technical group because of the great firewall issues and translation issues.**
- **What is a lab?**
  
  - **Labs were created to provide a low-impact to LF staff incubation ground for code to be tried out and try to build momentum.**
  - **The lab must find a sponsor on the TSC or among lab stewards.**
  - **Labs start with code first.**
  - **The roles and responsibilities of stewards is unclear.**
    
  - **The goal is to allow projects to graduate from a lab to a project or tool without a lot of handholding by LF staff.**
  - **Labs are not really expected to ship anything**
  - **No blog posts about labs, no PR, etc. The bar is low.**
- **What is SEMVER?**
  
  - **[SEMVER](https://semver.org/), Semantic Versioning, is how all projects and tools are supposed to be versioned.**
- **What is FMR?**
  
  - **FMR, First Major Release, is tied to a gate for having SEMVER 1.0.0**
- **Who governs FMR?**
  
  - **FMR is a gate governed by the TSC.**
- **Who cares?**
  
  - **It is expected that projects and tools that pass FMR will have some level of support as they move forward.**
- Community Maturity
- Vendor Diversity
- What is Incubation, active, inactive?
  
  - If this is a measure of community maturity, how do we described the attributes of the community maturity such that being "immature" doesn't harm the marketing of the project.
  - The "Status" seems to be too prominent in our marketing and too visible in our wiki.
    
    - What we want outsiders to see is our technical readiness and the opportunities that exist for getting involved.
    - What we want insiders to see is the maturity metrics of the communities associated with each project.
- CII badge
- Policy on Websites, twitter etc.

Document generated by Confluence on Nov 26, 2024 13:04

[Atlassian](http://www.atlassian.com/)
