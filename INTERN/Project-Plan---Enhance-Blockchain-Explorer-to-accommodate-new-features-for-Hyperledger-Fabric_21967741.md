1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)
5. [Enhance Blockchain Explorer to accommodate new features for Hyperledger Fabric](Enhance-Blockchain-Explorer-to-accommodate-new-features-for-Hyperledger-Fabric_21959307.html)

# Hyperledger Mentorship Program : Project Plan - Enhance Blockchain Explorer to accommodate new features for Hyperledger Fabric

Created by Archana Arige, last modified by Venkata Manoj Bhargav Maddali on Aug 24, 2023

# Abstract

Blockchain Explorer is a GUI tool that allows users to view blocks, transactions, nodes, channels, chaincodes and other associated information about the blockchain network. The aim of this project is to enhance the existing application in-terms of new features and uplift the user-interface with the robust design. Blockchain explorer uses fabric-sdk to get the details from the fabric network and stores the data in the postgres database, which is later used by the explorer UI.

# Mentors and Mentees

## Mentors

Arigela Satyanarayana, Discord: Arigelas#4597  
Archana Arige, Discord: Archana#6996  
Ajin S, Discord: ajin847#0328  
Arun S M, Discord: arsulegai#7968  
Aditya Joshi, Discord: adityajoshi#9707

## Mentee

Venkata Manoj, Discord: MVB#8720

# Scope:

01. A full-fledged functional explorer application with UI that is well tested and documented w.r.t the new features implemented.
    
    1. Include information on the build and run.
    2. Cleanup the builds that are no more supported.
    3. Delete the previously deprecated Fabric releases.
02. Config driven data purge based on blockcount (or) duration.
    
    1. Partial transaction contents to be used in the search interface. The contents can be from state database, ledger (including block).
    2. Type ahead search can be enabled.
03. Research on metrics and bring up possible metric features.
    
    1. Usage: Setup alerts for anomalies. Peers have different block heights. A transaction took too long to process.
    2. Examples: Information available for the network participants which are not available within the peer/orderer metric endpoint.
    3. All the UI reported information shall be emitted as a metric. Identify screens and add line items for the mentorship.
    4. Optional: Pluggable UI for having Grafana dashboard within the Explorer.
04. Compatible with latest release version of fabric.
    
    1. Docker compose specs in the repository is up to date to support latest version of Fabric (or the previous one).
    2. Explorer to Fabric release tagging.
05. Improvise the UI Design.
    
    1. Line items from the UX mentorship.
06. User Management - Need to avoid administration key dependency in Explorer View.
    
    1. Integrating with LDAP.
    2. Decouple the admin key requirement.
    3. Revisit Authentication/Authorization. Support OAuth.
07. Optional Feature: View for generated user credentials.
    
    1. Connect to Fabric CA and fetch list of all the generated keys.
08. Role management in the Explorer.
    
    1. Identify the roles.
    2. Enable role based access mechanism.
09. Simulate/read capability for chaincode within the Explorer.
10. \[Optional] Alternate UI for transaction management, sending transaction, chaincode deployment operations.
11. Move the images from the docker hub to GHCR.
12. Write/modify the test cases to be in-compliant with the newly added features.
13. \[Optional] Look into library approach. Separate core features and design interfaces in the backend. Make it pluggable.

# Deliverables

- Data Purging based on blockcount/time
- User Access Management
- Fix the running issues
- Migrate Images from docker-hub to GHCR
- Research and implement Metrics - Network Level Observability
- Test-cases and documentation
  

# Milestones

**Eval 1:**

- Research on the best practices of purging the postgres DB data
- Implement the purging feature based on blockcount/time
- Improve Boot time for loading blocks and transactions

**Eval 2:**

- User Access Management -Integrating with LDAP
- Decouple the admin key requirement
- Revisit Authentication/Authorization. Support OAuth.

**Eval 3:**

- Fix the running issues
- Migrate Images from docker-hub to GHCR

**Eval 4:**

- Research and implement Metrics - Network Level Observability
- Test Cases and Documentation

**Eval 5:**

- Optional: Create UI screens based on wire-frames
- Integrate the UI with backend

## **Timeline**

Goal

Activity

Status

Est. Time of Completion

Milestone

Onboard &amp; Ramp-up

end of JuneOnboarding and Learning/Ramp Up

- Data Purging

end of July

Monthly Checkpoint

- 28 Jul 2023 1st quarter mentee evaluation

<!--THE END-->

- User Access Management

end of August

Monthly Checkpoint

31 Aug 2023 Midterm mentee evaluation

- Fix the running issues
- Test Cases

end of September

Monthly Checkpoint

- Network Level Observability

end of October

20 Oct 2023 3rd quarter mentee evaluation

- Improved Documentation
- Add the tutorial on deployment

end of November

Monthly Checkpoint

30 Nov 2023 final mentee evaluation

TBD

Global Meetup: Demo and Showcase

(align to The Linux Foundation's timelines)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
