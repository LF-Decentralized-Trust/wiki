1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : Runtime-checked automated programming for chaincode development

Created by Imre Kocsis, last modified by Min Yu on Feb 02, 2024

**Project Title**

**Runtime-checked automated programming for chaincode development**

**Status**

COMPLETED

**Primary Focus**

  RESEARCH

# Description

Can we make ChatGPT write chaincode for us?

The answer is certainly yes, but – for now - the current caveats of “AI-conversational” programming apply: the process is iterative, and we really can’t be sure whether the result is completely right until we test it – and probably also look for execution errors at runtime.

Automated programming for other blockchain platforms is an already emerging topic, but Fabric has not been really addressed yet. This is an experimental mentorship with equal weight in research and hands-on coding, with the following goals.

1. To review existing examples and approaches of automated programming for smart contracts of other platforms (i.e., Solidity).
2. To explore the technically feasible options of automated chaincode programming for Hyperledger Fabric (incl. ChatGPT) and select one for further work.
3. To formulate a chaincode specification style which “seems to work well enough” on a set of representative examples with automated programming.
   
   (We don’t know yet what will work; One-shot or iterative? Requirement set or Behavior-Driven Development (BDD)? Conversational or formal specification? And so on.)
4. To create support for translating the specification partially or fully to runtime verification code, which can wrap the chaincode implementation.

On the last point: starting from a specification is a tried and tested way to create verifier code either manually or automatically and is much easier to do correctly than creating the implementation correctly from a specification. We plan to keep this last point “classic”: i.e., no ChatGPT here. Specification-based verification criteria are usually amenable to development time verification, too (with static analysis, model checking, etc.).

# Additional Information

Ask ChatGPT for papers which deal with using neural networks for generating Solidity code! No, really.

And ask it to write you an ERC-20 equivalent chaincode.

And ask it to introduce Fabric MSP-based ownership management.

(Try not to think of Asimov's robopsychology.)

It's not a coding wizard yet, but definitely uncanny.

Furthermore, we expect to experiment with Behavior-Driven Development; this means Gherkin/Cucumber.

Technology/approach for runtime verification ([https://en.wikipedia.org/wiki/Runtime\_verification](https://en.wikipedia.org/wiki/Runtime_verification)) will depend heavily on the results on the "constructive" side - we do not want to make a commitment on this at this point.

# Learning Objectives

- Hyperledger Fabric chaincode programming (if that's not already in the candidate's toolbox)
- Experiment planning and evaluation
- Working under guidance and collaborating using open-source tools
- Analytic thinking - and also thinking a bit outside the box

# Expected Outcome

- A representative ("towards a benchmark") set of smart contract functionality and their key variations, defined in natural language (various token contracts, cross-organizational processes, data recording, etc.)
- A set of (possibly branching) natural language conversation scripts, and a report on evaluating the capabilities and shortcomings of a selected (expected to be best-of-breed) generative approach
- A set of functionally equivalent specifications in a structured approach (we expect this to be a variant of BDD, but there are other options to try)
- A report on evaluating the capabilities and shortcomings of the structured approach on the selected (expected to be best-of-breed) generative approach, and comparison with the "conversational" approach
- At least expected: specification-compliance runtime checking code for the cases of the structured approach (determining the checked properties and a coverage goal is part of the work)
- Optimally: automatically generated checker code

# Relation to Hyperledger

Hyperledger Fabric.

# Mentee Skills

This project does not really need significant existing credentials; curiosity is the key factor. That said, basic experience in programming and knowledge of requirement-driven development approaches is needed. We prefer a candidate to have at least some experience with chaincode development and knowledge of the Hyperledger Fabric platform.

# Mentee Open Source Contribution Experience

If available, show us (preferably through GitHub) and be able to explain a nontrivial piece of chaincode you developed.

# Future plans

We expect a successful mentorship to have the potential to become a Lab project in the form of a self-hosted tool for users. At this point, due to the experimental nature of the proposed work, we are hesitant to make any further plans (e.g., about a "Fabric coding service").

# Mentor(s) Names and Contact Info

Bertalan Zoltán Péter, [bpeter@edu.bme.hu](mailto:bpeter@edu.bme.hu), PhD student, Budapest University of Technology and Economics, Dept. of Measurement and Inf. Systems, Critical Systems Research Group

Imre Kocsis, [kocsis.imre@vik.bme.hu](mailto:kocsis.imre@vik.bme.hu), assistant professor, Budapest University of Technology and Economics, Dept. of Measurement and Inf. Systems, Critical Systems Research Group

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
