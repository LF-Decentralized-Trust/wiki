1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2019 Projects](2019-Projects_21954613.html)

# Hyperledger Mentorship Program : Hyperledger Caliper visualization

Created by feihu jiang, last modified by Raghunathan P on Jan 11, 2022

**Title**Caliper visualization**Status**

PROJECT COMPLETED

**Difficulty**

MEDIUM  

# Description

Hyperledger Caliper is a platform for facilitating the execution of user-provided workloads/benchmarks on multiple blockchain platforms in a transparent way. Caliper achieves its flexibility by relying on two configuration files during its execution.

One configuration file describes the test rounds that Caliper must execute, including: the intensity/rate and content of the workload; the deployment of processes that generate the workload; and additional monitoring settings.

The other configuration file describes the target blockchain network in detail, at least including the topology of the blockchain network (among other, platform-specific attributes). 

The aim of the project is the following:

- Create a GUI component for Caliper that makes the management of configuration files easier, specifically:
  
  - Assembling/generating configuration files through the GUI
  - Saving, loading and editing configuration files
  - Providing built-in documentation and tips for the users
- Visualize in real-time the key performance indicators observed during the execution of a benchmark

# Additional Information

Caliper documentation page: [https://hyperledger.github.io/caliper/](https://hyperledger.github.io/caliper/)

Caliper GitHub repository: [https://github.com/hyperledger/caliper](https://github.com/hyperledger/caliper)

Contribution guidelines: [https://github.com/hyperledger/caliper/blob/master/CONTRIBUTING.md](https://github.com/hyperledger/caliper/blob/master/CONTRIBUTING.md)

# Learning Objectives

- Contributing and collaborating in an open-source project
- Knowledge of how to perform a blockchain performance evaluation
- Graphical visualization techniques for performance indicators

# Expected Outcome

 A GUI component for Caliper, including: the implementation of the listed features; a developer documentation; and a user (how-to) documentation on the official documentation page (in the form of screen casts, for example).

# Relation to Hyperledger

Builds on Hyperledger Caliper, partially relying on concepts of other Hyperledger platforms (like Fabric, Sawtooth, etc.)

# Education Level

Undergraduate level or above

# Skills

- JavaScript (Node.js)
- High-level understanding of HL Fabric/Sawtooth networks (desired, but not required)
- Previous Hyperledger Caliper experience (desired, but not required)
- Fluent English or Mandarin will be preferred

# Future plans

The project outcome (the GUI component) will facilitate the adoption and easier application of Caliper in the community. As an integral part of Caliper, the GUI component will also need to follow the newly added features of Caliper, providing a continuing opportunity to work on the project.

# Preferred Hours and Length of Internship

 Full-time (40 hours a week for 12 weeks during the summer) or Part-time (20 hours a week for 24 weeks starting in summer and ending in fall)

# Mentor(s) Names and Contact Info

- Jiang Feihu, Huawei, [jiangfeihu@huawei.com](mailto:jiangfeihu@huawei.com)
- Attila Klenik, Budapest University of Technology and Economics, [klenik@mit.bme.hu](mailto:klenik@mit.bme.hu)
  

# Mentee Name and Contact Info

- Jason You [Jason You](https://lf-hyperledger.atlassian.net/wiki/people/5aede5767dd1e556227c0f43?ref=confluence) , Purdue University, jason.shengwey@gmail.com

* * *

# Mentee Updates

Last edited: Aug 29, 2019

# Project Deliverables

- **Phase 1: Starting the Caliper GUI project**
  
  - Basic Web UI design ideas;
  - Basic visualization charts for metrics;
  - Network graph visualization;
  - Consented JSON format input for Caliper visualization GUI.
- **Phase 2: Designing the initial model for the Caliper GUI**
  
  - Interactive UI with React.js;
  - Real-time visualization functionalities.
- **Phase 3: Integrating the visualization with the Caliper GUI**
  
  - Integration scripts for Caliper-core, Caliper-CLI, and Caliper GUI.
  - (TBD) Helper functions for integration with Node.js.
- **Phase 4: Refining project**
  
  - Documentation for integration and usage of Caliper GUI.
  - (TBD) Configuration files upload functionalities for framework testing with Hyperledger Caliper GUI:
  - Adding functionalities that allow users to easily test their results by dragging configuration files of different Hyperledger framework networks in to the Caliper GUI, and get visualization and reports by a few simple clicks.
- **Phase 5: Finalizing and summary**
  
  - Presentation PowerPoints for Caliper GUI project.
  - Demonstration for the functionality of Caliper GUI.

# Project Milestones

- [Jason You](https://lf-hyperledger.atlassian.net/wiki/people/5aede5767dd1e556227c0f43?ref=confluence) **Project Start \[June 3rd, 2019]** 24 Jun 2019
  
  - Deciding the visualization metrics and designing basics statics visualizations with [Plot.ly](http://Plot.ly) and D3.js.
  - Designing the basic Web UI for Caliper.
- [Jason You](https://lf-hyperledger.atlassian.net/wiki/people/5aede5767dd1e556227c0f43?ref=confluence) 1st Quarter \[June 24th, 2019] 15 Jul 2019
  
  - Using React.js to build the interactive UI.
  - Implementing the real-time visualization  functionality.

<!--THE END-->

- [Jason You](https://lf-hyperledger.atlassian.net/wiki/people/5aede5767dd1e556227c0f43?ref=confluence) 2nd Quarter \[July 15th, 2019] 05 Aug 2019
  
  - Integrating the Caliper-core or Caliper-CLI with the developed GUI and visualization functionalities.
  - Adding helper functions with Node.js.
- [Jason You](https://lf-hyperledger.atlassian.net/wiki/people/5aede5767dd1e556227c0f43?ref=confluence) 3rd Quarter \[August 5th, 2019] 26 Aug 2019
  
  - Creating and editing documentations for Caliper GUI for new users.
  - Refining the GUI and adding additional functionality to facilitate testing configuration for different Hyperledger frameworks.
- [Jason You](https://lf-hyperledger.atlassian.net/wiki/people/5aede5767dd1e556227c0f43?ref=confluence) **Final \[August 26th, 2019]** 01 Sep 2019
  
  - Preparing project presentation and GUI demonstration.

# Project Plan

[![](attachments/thumbnails/21954626/21962628)](attachments/21954626/21962628.pdf)

# Summary Report

[![](attachments/thumbnails/21954626/21963035)](attachments/21954626/21963035.pdf)

## Attachments:

![](images/icons/bullet_blue.gif) [Caliper GUI Design.pdf](attachments/21954626/21962628.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation- 2019-Caliper-Jason-You.pdf](attachments/21954626/21963035.pdf) (application/pdf)

Document generated by Confluence on Nov 26, 2024 14:59

[Atlassian](http://www.atlassian.com/)
