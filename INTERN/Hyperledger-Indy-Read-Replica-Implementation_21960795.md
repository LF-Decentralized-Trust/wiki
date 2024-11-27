1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2024 Projects](2024-Projects_21954934.html)

# Hyperledger Mentorship Program : Hyperledger Indy Read Replica Implementation

Created by Stephen Curran, last modified on Jun 16, 2024

**Project Title**Hyperledger Indy Read Replica Implementation**Status**

IN PROGRESS

**Primary Focus**

CODING   

**Project Plan**

[Project Plan - Indy Read Replica Implementation](Project-Plan---Indy-Read-Replica-Implementation_21960861.html)

# Description

While Hyperledger Indy has proven to be incredibly robust and more than sufficiently scalable to this point in its evolution and application, we think it would be useful to enable further scalability by adding the concept of Indy Read Replicas to the project. An Indy read replica is a copy of the ledger transactions from one or more Indy ledgers that can be used by clients that trust the replica. While not intended to be accessed by arbitrary agents, an enterprise might run a read replica on their own servers for the use of their own agents – the agents "trust" the deployment of the read replica. In turn, the use of read replicas will reduce the read load on the ledger. Each replica will stay up to date with the transactions on the ledger, and the agents using the replica need not connect directly with the ledger. For this project, we will start from one of two existing, open source Indy "ledger browser" implementations that collect transactions from the ledger and maintain them in a database. A REST API will be added that provides replica clients with an HTTP version of the existing ledger API. Once a functioning Indy read replica implementation has been developed and tested, we will look at what optimizations can be accomplished to further lower the load on the ledger. For example, a new replica has to retrieve all of the transactions on the ledger, and, in the open source ledger browsers does so by do a read for all transactions starting at 1. Is there a good approach to getting a "trusted" batch of transactions to eliminate that startup load?  To find transactions added to the ledger, the read replicas poll the ledger "anything new added?" Can that load be reduced by enabling a transaction "pub/sub" API that notifies read replicas of new transactions, perhaps even pushing them to the replicas. Lots of interesting design and implementation questions!

# Learning Objectives

- Starting from working code, evolve an Indy "ledger browser" to include and support a client agent API to handle any ledger read request.
- Investigate what existing cryptographic capabilities in Hyperledger Indy are available to increase the trust of agents in the use of the read replica – notably "state proofs" published by Hyperledger Indy
- Develop a performant, scalable web service that is easily deployed by Enterprises.
- Learn about CI/CD pipelines for running unit and integration tests, and for publishing software artifacts (libraries, containers).
- Work with experts in verifiable credentials and learn about field of digital trust.
- Understand the processes around delivering an open source web component for broad deployment.

# Expected Outcome and Deliverables

- The creation of the Hyperledger Indy Read Replica web service component.
- A release pipeline for the publication of the Indy Read Replica web service component artifacts.
- The creation of automated unit and integration tests for the web service.
- Documentation about how to run, test, use, and deploy an instance of Indy Read Replica web service.
- Opportunities to collaborate with project maintainers, and to present progress and results to the Hyperledger Indy community.

# Relation to Hyperledger and Impact on the community

This project focuses mainly on Hyperledger Indy, and to a lesser extent on Hyperledger Aries, which are the most common types of client agents that use Hyperledger Indy networks. The project's customers are enterprises that have Aries agents and that want to ensure their agents have a guaranteed service level agreement (SLA – responsiveness) in resolving ledger transactions.

# Recommended Skills

- Demonstrated proficiency with either JacaScript or Python (depending on which Indy ledger browser we will use).
- Ability and willingness to learn quickly.
- Solid understanding of blockchain technology, distributed systems, and security.
- Background in computer science, computer engineering, or equivalent
- Ability to analyze complex problems, identify areas for improvement, and propose effective solutions.
- Experience with debugging and troubleshooting complex software systems, including understanding and interpreting log files and debugging output.
- Experience with Git, GitHub Actions, Bash, Docker, and Linux.
- Experience with GitHub Actions based continuous integration/continuous deployment (CI/CD) pipelines with a focus on build and test automation.
- Advanced verbal and writing skills in English.

# Mentor(s) Names and Contact Info

Sam Curren, [sam@indicio.tech](mailto:sam@indicio.tech), Indico, PBC (Hyperledger Aries Maintainer)

Stephen Curran, [swcurran@cloudcompass.ca](mailto:swcurran@cloudcompass.ca), Cloud Compass Computing Inc. (Hyperledger Aries Maintainer)

# Additional Information

- [Hyperledger Indy Project](https://www.hyperledger.org/projects/hyperledger-indy)
- Indy Ledger Browsers (project starting point):
  
  - [IndyScan](https://github.com/Patrik-Stas/indyscan) (JavaScript, more complete) – example deployments [Sovrin](https://indyscan.io/txs/SOVRIN_MAINNET/domain), [Indicio](https://indyscan.indiciotech.io/)
  - [VON Network Browser](https://github.com/bcgov/von-network/tree/main/server) (Python, less complete) – example deployment [BCovrin Test](http://test.bcovrin.vonx.io/)
- Presentation about [Indy Read Replicas](https://docs.google.com/presentation/d/1wVUhoE0HRFV1feQWDa-1b9OnWGa0lk3LO-p21fk3mVE/edit?usp=sharing)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
