1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : One-stop-shop Hyperledger Fabric performance analysis with Hyperledger Caliper

Created by Attila Klenik, last modified by Min Yu on Dec 18, 2023

**Project Title**One-stop-shop Hyperledger Fabric performance analysis with Hyperledger Caliper**Status**

COMPLETED

**Primary Focus**

CODING DOCUMENTATION   

# Description

Performance evaluation of DLTs is a complex process stemming from the inherent complexity of distributed systems. One way to mitigate such complexity is the separation of concerns: use task-oriented solutions for different aspects of the process:

- The System Under Test (SUT) is deployed in a representative operating environment.
- A dedicated, purpose-specific load generator tool submits representative requests to the SUT.
- The SUT is closely monitored during the load generation process, and the measured data is typically stored for post-mortem analysis.
- A detailed analysis is performed on the measured data using dedicated data analysis techniques. A summarizing report is the typical final output of the process, containing insights about the SUT.

Even though the above concerns should be separated, it becomes cumbersome to provide a one-click ("cloud-like") experience for running a performance analysis, mainly because the last step does not build on common solutions and contains ad-hoc/in-house solutions.

Hyperledger Caliper provides capabilities to integrate lightweight components that can retrieve aggregated results from external components and incorporate them into the generated report (e.g., the [Prometheus monitor](https://hyperledger.github.io/caliper/v0.5.0/caliper-monitors/#prometheus-monitor)).

The goal of the project is to provide a single entry/exit point to the performance analysis (once the SUT and its monitoring are configured) by:

- Providing an open, well-designed, and thoroughly documented side-car service for the detailed performance analysis of distributed Fabric transaction traces.
- And integrating it into the Caliper load generation and response measurement process as part of the final report.

The project will heavily build on the PSWG's Performance Sandbox, aiming to "standardize" its flow and methodologies independently of the applied technologies.

# Additional Information

- A systematic performance analysis approach for Hyperledger Fabric:
  
  - [Adding Semantics to Measurements: Ontology-Guided, Systematic Performance Analysis](https://cyber.bibl.u-szeged.hu/index.php/actcybern/article/view/4278) (highly recommended, lighter reading)
  - [Measurement-based performance evaluation of distributed ledger technologies](https://repozitorium.omikk.bme.hu/bitstream/handle/10890/18724/ertekezes.pdf?sequence=2&isAllowed=y) (more general, advanced material)
- Related PSWG activities:
  
  - [Hyperledger Blockchain Performance Metrics White Paper](https://www.hyperledger.org/learn/publications/blockchain-performance-metrics)
  - [PSWG Performance Sandbox: HL Fabric deployment and monitoring](https://github.com/hyperledger-labs/PerformanceSandBox)
- Hyperledger Caliper, the scalable and extendable workload generator of Hyperledger: [https://www.hyperledger.org/use/caliper](https://www.hyperledger.org/use/caliper)
- Hyperledger Fabric, a modular and scalable distributed ledger implementation of Hyperledger: [https://www.hyperledger.org/use/fabric](https://www.hyperledger.org/use/fabric)

# Learning Objectives

- Mastering the open-source workflow
  
  - Managing issues, pull requests, development branches, and repository content
- Being part of an open community, navigating and utilizing different forums
- Working in a team
- Covering a broad spectrum of software development skills
  
  - Designing/implementing functionally rich, testable, maintainable software components
  - Introduction to service-oriented software engineering approaches
  - Introduction to performance data analysis
  - Documentation and presentation skills
    
    - Developer documentation
    - User documentation
    - To-the-point, coherent presentation

# Expected Outcome

1. Detailed, technology-agnostic documentation about the observability of Hyperledger Fabric, integrated with its (semi-)formal consensus model.
2. A transaction/event-level monitoring solution (preferably building on the existing Performance Sandbox capabilities) for tunneling distributed traces into a single processing component.
3. A self-contained, side-car service that systematically aggregates, validates, and analyses the incoming distributed traces and exposes the results in a simple format.
4. An enhanced "Monitoring &amp; Reporting" pipeline in Hyperledger Caliper that facilitates the integration of custom monitors and reporters.
5. A custom Caliper monitor integration that pulls the results of the side-car service and a custom Caliper reporter integration that displays the detailed performance results in a self-contained format.

# Relation to Hyperledger

- Hyperledger Fabric: the project aims to provide a canonical methodology for conducting such a performance analysis of the platform.
- Hyperledger Caliper: the project aims to extend Caliper with the capability of easily integrating external monitoring/measurement data, thus keeping the concerns separated (Caliper is primarily a workload generator).
- PSWG: the project is the first step toward a unified performance analysis approach for Hyperledger DLT solutions, specializing (along a common methodology) the previous PSWG whitepaper for each platform.

# Mentee Skills

## Education Level

At least an ongoing M.Sc. study (or strong design skills) in software engineering is recommended.

## Technical Skills

Required skills:

- Basic understanding of version control and git
- Experience with JS (Node.JS)
- Basic data analysis skills (e.g., pandas in python)
- Intermediate verbal and writing skills in English
- A firm understanding of the Hyperledger Fabric consensus

Nice-to-have skills (the mentee can learn these during the internship):

- Advanced git usage (upstream repositories, branching, rebasing, etc)
- Familiarity with Visual Studio Code or similar IDE
- Experience in service-oriented system design
- Experience with monitoring and log processing solutions
- Writing documentation in markdown
- Capability for unsupervised learning

# Mentee Open Source Contribution Experience

Show us a code base (preferably on GitHub) you created/had a major role in creating and which you are proud of. If that's not applicable, our plan is to assign some programming tasks during the selection interview for such candidates.

# Future plans

- Enhancing the Caliper monitoring and reporting capabilities is a significant step in the proper modularization of Caliper, paving the road for further optimization of the code base.
- The side-car service can provide kernel functionalities for higher-level, smarter analysis methods for the rigorous (and automated) performance analysis of Fabric solutions.
- The experience gathered during the project will be integrated into PSWG-related activities, e.g., the performance sandbox and designing future whitepapers.

# Mentor(s) Names and Contact Info

[Attila Klenik](https://lf-hyperledger.atlassian.net/wiki/people/712020:4b6a8d7d-e65a-471e-a60d-e945d09147e2?ref=confluence), research fellow, [attila.klenik@vik.bme.hu](mailto:attila.klenik@vik.bme.hu), Budapest University of Technology and Economics, Dept. of Measurement and Inf. Systems, Critical Systems Research Group (ftsrg)

[Javaid, Haris](https://lf-hyperledger.atlassian.net/wiki/people/712020:a6724b50-b282-40cf-abea-83ac81af6589?ref=confluence), Senior Staff Researcher, [haris.javaid@amd.com](mailto:haris.javaid@amd.com), AMD Singapore.

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
