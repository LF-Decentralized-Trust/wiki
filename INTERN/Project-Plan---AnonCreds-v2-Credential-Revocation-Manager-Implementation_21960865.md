1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2024 Projects](2024-Projects_21954934.html)
5. [Hyperledger AnonCreds v2 ZKP-based Credential Revocation Manager Implementation](Hyperledger-AnonCreds-v2-ZKP-based-Credential-Revocation-Manager-Implementation_21960785.html)

# Hyperledger Mentorship Program : Project Plan - AnonCreds v2 Credential Revocation Manager Implementation

Created by Stephen Curran, last modified by VictorH2208 on Jun 22, 2024

## **Abstract**

The Revocation Manager is a component of the Hyperledger AnonCreds v2 framework, aimed at improving the management of credential revocations with a focus on scalability, privacy, and security. Utilizing ALLOSAUR, an advanced cryptographic algorithm, the Revocation Manager is designed to handle high volumes of credential transactions with minimal data exchange to preserve user privacy. The system will be built using Rust for cryptographic processing and Python with FlaskAPI for the web interface. Further, the Revocation Manager is engineered to support deployment across multiple instances, facilitating robust multi-party computation (MPC) connections. This feature allows for distributed operation and data handling, reducing the load on any single system and enhancing overall service availability and fault tolerance. The deployment strategy is tailored to ensure that even in a distributed environment, data integrity and system responsiveness are maintained, making it an ideal solution for enterprises seeking scalable and secure digital credential management.

## **Mentor and Mentee**

Mentors: Mike Lodder, Stephen Curran

Timezone: US Mountain and Canadian Pacific (Vancouver)

Mentee: Victor Huang

Timezone: Canada Eastern (Toronto)

**Project repo:** 

AnonCreds Rovcation Manager Py: [https://github.com/VictorH2208/anoncreds-revocation-manger-py](https://github.com/VictorH2208/anoncreds-revocation-manger-py)

Agora ALLOSAUR RS: [https://github.com/hyperledger-labs/agora-allosaurus-rs](https://github.com/hyperledger-labs/agora-allosaurus-rs)

## **Deliverables**

- Web Service that implements an ALLOSAUR Revocation Manager.
- An API for clients to use the Revocation Manager.
- Unit and integration tests for the service.
- GitHub Actions to invoke the tests, and when triggered, release artifacts for published versions of the implementation.
- Documentation for deploying and configuring a horizontally scalable instance of the web service.

## **Milestones**

**Eval 1:**

- Create a new GitHub repository
- Define and implement an API
- Get the new implementation running using Docker and document how to run a local instance.

**Eval 2:**

- Integrate the Rust cryptography components using FFI with the Python Flask API
- Implement basic MPC and sharding functionalities
- Conduct initial testing on Docker deployment

**Eval 3:**

- Complete comprehensive integration and performance tests
- Finalize documentation with detailed sections on Docker setup, MPC integration, and API usage

**Eval 4:**

- Conduct final system evaluations in a production-like environment using Docker

## **Timeline**

WeekTask/PlanStatus**June 03 - June 23**On boarding/orientation sessions. Meet with the mentors, discuss project implementation details,  
deliverables and scope. Prepare the project plan.  
**June 24 - July 7**

Update and refine the syntax and functionality of the existing ALLOSAUR algorithm in Rust.  
Set up Docker environment for consistent development and testing across different systems.

**July 8 - July 19**

Develop the Python Flask API.  
Start the process of wrapping the Rust code with FFI for Python integration.  
Implement basic Docker setup for deploying the web service.

**July 22 - July 26**Review integration progress and Docker deployment strategy with mentors.  
1ST QUARTER MENTEE EVALUATION  
**July 27 - August 18**Continue developing the API in Python and enhance the Docker setup for scalability.  
Begin implementing MPC and sharding for mutiple manager instances.

**August 19 - September 01**

Finalize API functionalities and Rust-Python integration.  
Conduct Docker-based deployment tests to ensure the environment is stable and scalable.  
Start documentation.

**September 02 - September 06**

MIDTERM EVALUATIONS  
Perform extensive integration and performance testing

**September 08 - September 22**

Implement GitHub Actions for automated testing within Docker environments and continuous integration.  
Expand on documentation

**September 23 - October 19**

Finalize all documentation, emphasizing Docker deployment strategies

**October 14 - October 18**3RD QUARTER MENTEE EVALUATION  
**October 19 - November 10**Timeline buffer.  
Test all components, including Docker deployment and MPC functionality.  
**November 11 - November 29**

FINAL MENTEE EVALUATION

## **Explanation**

## **Methodology**

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
