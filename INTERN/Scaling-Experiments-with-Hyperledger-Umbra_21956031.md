1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2020 Projects](2020-Projects_21963347.html)

# Hyperledger Mentorship Program : Scaling Experiments with Hyperledger Umbra

Created by David Huseby, last modified by Min Yu on Dec 01, 2020

**Title**Scaling Experiments with Hyperledger Umbra**Status**

COMPLETED

**Difficulty**

MEDIUM

# Description

For the past two years, the Hyperledger Umbra lab has been worked on by mentees to develop the capability of running the unmodified Hyperledger Fabric docker images under a simulated network environment for the purposes of doing experiments on running Fabric networks in a controlled way. At the end of last summer, Hyperledger Umbra achieved the initial goal of running Fabric networks under simulation. Hyperledger Umbra is useful for doing network-level security fuzzing as well as network scaling experiments and this mentorship is focused on designing and executing scaling experiments.

Hyperledger Fabric networks are designed to scale up fairly easily, however nobody has actually tried scaling Hyperledger Fabric to many hundreds and thousands of nodes and done analysis on how it affects the characteristics of the distributed system such as time to reach consensus, time to run an election for block creation, etc. The mentee chosen for this project will work with their mentor to design a plan for setting up, executing, gathering and analyzing data, and reporting the results of scaling experiments run at different scales.

# Additional Information

Hyperledger Umbra operates on and with Docker images published by the Hyperledger Fabric project. To be successful this project will require working knowledge of Docker and also of Amazon Web Services and Kubernetes as the scaling experiments will be run on AWS using Kubernetes.

# Learning Objectives

- First and foremost the mentee will learn how to be a positive collaborator and contributor in an active open source project.
- Learn how to work within the Hyperledger open source ecosystem and culture.
- Apply computer science skills to understand the algorithms being used and to propose effective experiments to measure how performance varies with the scale of the network.
- Gain a better understanding of distributed network applications and how to study them.

# Expected Outcome

- A report on the wiki detailing the setup, design and objective of each experiment.
- A report on the results with analysis of the results.
- Maybe bug reports for both Hyperledger Ursa and/or Hyperledger Fabric.

# Relation to Hyperledger

This project is directly related to Hyperledger Umbra as it will be used to run the experiments and indirectly related to Hyperledger Fabric as it will be experimented upon.

# Education Level

The ideal mentee is a university student or a developer with one or two years of experience with a solid background in Computer Science, especially distributed systems and related algorithms.

# Skills

- Experience with Docker is a must.
- Python programming experience.
- Experience with Amazon Web Services and Kubernetes.
- Computer Science background in distributed systems and algorithms.

# Future plans

These experiments will feed into our education plans for creating Computer Science courses focused on distributed ledger technology. Hyperledger Umbra will likely also have its feature set enhanced as a result of the feedback from using it for these experiments.

# Preferred Hours and Length of Internship

This project can be done by a full-time or part-time mentee.

# Mentor(s) Names and Contact Info

David Huseby, dhuseby@linuxfoundation.org, "dhuseby" on chat.hyperledger.org

# Mentee

[Raphael Vicente Rosa](https://lf-hyperledger.atlassian.net/wiki/people/70121:ec78d2c6-ed67-4e95-82f0-508dc3b3f49d?ref=confluence)

# Project Results

The main project outcomes are seen in the [merge pull request in hyperledger-labs/umbra](https://github.com/hyperledger-labs/umbra/commit/20f2294ba85edc3fecf144d3181c66c94579a8d1) :

- Adds umbra-agent, umbra-monitor, umbra-cli components to umbra
- Adds Vagrantfile to umbra (options to virtualbox and qemu/kvm)
- Comprehensive Makefile to install and run umbra
- umbra-cli component automates all the experiments (easy to code/run examples)
- Adds scaling functionalities to umbra - environments realize the abstraction of multiple machines
- Updates fuzzing functionalities to run together with scaling functionalities
- Adds support to Iroha and examples

# Final Report

[![](attachments/thumbnails/21956031/21964148)](attachments/21956031/21964148.pdf)

# Lightening Talk Recording

![](plugins/servlet/confluence/placeholder/unknown-attachment)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Mentee 2020 - Scaling Experiments with Hyperledger Umbra.pptx.pdf](attachments/21956031/21964148.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/21956031/21964225.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 14:59

[Atlassian](http://www.atlassian.com/)
