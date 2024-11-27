1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)

# Hyperledger Mentorship Program : Visual Studio Code support for Hyperledger Caliper artifacts

Created by Attila Klenik, last modified by Min Yu on Dec 19, 2022

**Project Title**Visual Studio Code support for Hyperledger Caliper artifacts**Status**

COMPLETED

**Difficulty**

 MEDIUM   

# Description

Performance benchmarking distributed systems (such as DLTs) is a challenging task, comprising of **multiple aspects**, such as scalable workload generation, representative workload definitions, and comprehensive data analysis.

Hyperledger Caliper is a general-purpose benchmarking tool with the goal of mitigating the aforementioned aspects of performance benchmarking:

1. It provides a flexible architecture to allow scalable workload generation.
2. It collects and reports results based on detailed client-observable execution traces.
3. It allows the implementation/plug-in of custom workload behaviors to meet the diverse criteria of a wide range of business scenarios.

The flexible support of the aforementioned performance benchmarking aspects inherently makes the setup and configuration of a Caliper-based project **cumbersome and error-prone**:

- The user must provide information about the system under test (SUT) in the form of a network configuration file.
- The user must also specify the flow of the benchmark run in the form of a benchmark configuration file.
- The runtime behavior of Caliper components can be influenced in detail through a configuration file.
- As with most programming-related projects, a Caliper-based project should employ best practices to make its structure flexible and maintainable.

The goal of the mentorship project is to deliver a Visual Studio Code extension that can help users perform the aforementioned tasks in an assisted and possibly automated manner.

The exact steps of the project are detailed in the Expected Outcome section.

# Additional Information

- Caliper GitHub repository: [https://github.com/hyperledger/caliper](https://github.com/hyperledger/caliper)
- Caliper example benchmarks GitHub repository: [https://github.com/hyperledger/caliper-benchmarks](https://github.com/hyperledger/caliper-benchmarks)
- Caliper documentation page: [https://hyperledger.github.io/caliper/](https://hyperledger.github.io/caliper/)
  
  - Architecture documentation: [https://hyperledger.github.io/caliper/vNext/architecture/](https://hyperledger.github.io/caliper/vNext/architecture/)
  - Benchmark configuration documentation: [https://hyperledger.github.io/caliper/vNext/bench-config/](https://hyperledger.github.io/caliper/vNext/bench-config/)
  - Workload module documentation: [https://hyperledger.github.io/caliper/vNext/workload-module/](https://hyperledger.github.io/caliper/vNext/workload-module/)
- Caliper Discord channels (registration needed for login)
  
  - General: [https://discord.com/channels/905194001349627914/941417677778473031](https://discord.com/channels/905194001349627914/941417677778473031)
  - Contributors: [https://discord.com/channels/905194001349627914/941417722946924554](https://discord.com/channels/905194001349627914/941417722946924554)

# Learning Objectives

- Mastering the open-source workflow
  
  - Managing issues, pull requests, development branches, and repository content
- Being part of an open community, navigating and utilizing different forums
- Working in a team
- Covering a wide spectrum of software development skills
  
  - Conducting unsupervised research for state-of-the-art solutions
  - Writing detailed, consistent specifications
  - Designing/implementing functionally rich, testable, maintainable software components
  - Testing methodologies for rigorous testing
  - Documentation and presentation skills
    
    - Developer documentation
    - User documentation
    - To-the-point, coherent presentation

# Expected Outcome

The mentee must complete the following tasks by the end of the internship:

1. Create a schema for the benchmark configuration file of Caliper.
2. Create a schema for the Fabric network configuration file of Caliper.
3. Create a schema for the Ethereum/Besu configuration file of Caliper.
4. Create a schema for the runtime configuration file of Caliper.
5. Implement code generators for various Caliper artifact skeletons (general project, workload module, connector, etc.).
6. Thoroughly test the implemented artifacts
7. Create a Visual Studio Code extension that integrates the implemented functionalities into Visual Studio Code.
8. Provide developer and user documentation for the implemented artifacts.

# Relation to Hyperledger

Hyperledger Caliper: specification and implementation of an "extend-only" feature (meaning no blocking dependency on parallel implementation efforts).

# Education Level

At least an ongoing B.Sc. study in software engineering is required.

# Skills

Required skills:

- Basic understanding of version control and git
- Experience with JavaScript programming (in Node.JS context)
- Intermediate verbal and writing skills in English
- High-level understanding of Hyperledger Caliper components

Nice-to-have skills (the mentee can learn these during the internship):

- Advanced git usage (upstream repositories, branching, rebasing, etc)
- Familiarity with Visual Studio Code and its extension mechanism
- Experience in unit testing and JS-related unit testing frameworks
- Writing documentation in markdown
- Capability for unsupervised learning and research

# Future plans

The project is an important stepping stone towards lowering the entry barrier for performance benchmarking DLTs using Caliper.

The project is intended as the basis and proof-of-concept for a Visual Studio Code extension package to help users set up Caliper-based performance benchmarks.

# Preferred Hours and Length of Internship

Full-time (40 hours a week for 12 weeks during the summer)

# Mentor(s) Names and Contact Info

[Attila Klenik](https://lf-hyperledger.atlassian.net/wiki/people/712020:4b6a8d7d-e65a-471e-a60d-e945d09147e2?ref=confluence)

Budapest University of Technology and Economics, Critical Systems Research Group

Email: [attila.klenik@vik.bme.hu](mailto:attila.klenik@vik.bme.hu)  
GitHub handle: aklenik  
Discord handle: klenik#9902

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
