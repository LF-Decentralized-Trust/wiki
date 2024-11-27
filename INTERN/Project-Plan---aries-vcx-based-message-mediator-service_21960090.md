1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)
5. [aries-vcx based message mediator](aries-vcx-based-message-mediator_21954879.html)

# Hyperledger Mentorship Program : Project Plan - aries-vcx based message mediator service

Created by N G, last modified on May 22, 2024

# Abstract

*Mediator service is like a drop box / post box that Aries agents can use to receive and store encrypted messages in their stead.*

*Basic flow:*

- *people can send you messages at the mediator address if you are not always available to receive messages*
- *you can pick them up later from mediator service using [pick up protocol](https://github.com/hyperledger/aries-rfcs/tree/main/features/0685-pickup-v2)*

*Mediator/ Agency are useful for scenarios like mobile phone agents which can't always receive messages. Due to reasons including:*

- *network interruption*
- *sleep /power off*
- *power conservation optimizations*
  

*There exist a agency/mediator service for Aries, but it has limitations:*

- *Written in NodeJS. A Rust based mediator service would be desirable for better integration with vcx*
- *Does not support pick up protocol (uses custom data exchange)*
  

*A new Rust based Aries mediator service would offer.*

- *High performance*
- *Horizontal scalability*
- *Simpler and more robust integration with Aries-vcx*
- *Support for newer standard protocols like Pick Up protocol.*

# Deliverables

Main Deliverables:

- Specialized high performance Aries agent (mediator to-be) that can store "forward messages" received through connection protocol.
- Pickup protocol data structs and impl inside aries-vcx
- Mediator service that can answer pick up protocol requests to authenticated peers
- CI to build and test on new commits.

Extra Deliverables:

- CI to make releases based on tags and provide binaries or docker image in Github's release section.
- (stretch goal): design/document mediator service component that can notify registered peers on inbox message available.

Project Plan

## Stage 1: HTTP Server

- Research and choose rust based web framework, suitable for project goals
- Implement simple http service with some endpoints
- Include logging library (env\_logger is popular choice)
- Include E2E test - make request against the endpoints, expect appropriate response
- CI: Lint, build, run &amp; test each commit

## Stage 2: Storage

- Understand pick-up protocol specification
- Based on the specification, design trait for retrieving messages and storing messages
- Provide mysql implementation
- Include integration tests
- CI: Include new set of tests in CI

## Stage 3: Integrate Aries-vcx

- Include aries-vcx as project dependency
- Initialize aries-vcx library (create wallet)
- Add endpoint for clients to fetch connection invitation (built using aries-vcx)

## Stage 4: Support establishing didcomm connections

- Decide if there is need to alter storage traits, or to just create new implementations, and act accordingly.
  
- Implement endpoint to fetch mediator's connection invitiation
- Support establishing didcomm connection between client and mediator using aries-vcx Connection state machine
- Create e2e test for establishing didcomm connection betwen test client and the mediator

## stage 5: Receiving and storing didcomm messages

- Enable receiving messages (mediation) on behalf of a connected client (which established connection and requested mediation - stage 4)
- Add medaitor e2e test where mediator receives and stores didcomm message

## stage 6: Add pickup protocol support

- Add pick-up protocol data model to aries-vcx messages crate
- Add pick-up protocol messages parsing to mediator
- Add mediator e2e test performing message pick-up

## stage 7: Bonus - websocket

- Implement websocket interface for pickup protocol (think can be broken down further if we start working on this)

## stage 8: Bonus - notifications

- Implement pub/sub mechanism in distributed environment to assure instant notification of connected websocket clients about a newly received message (think can be broken down further if we start working on this)

# Milestones

### **Evaluation 1 (July 11):**

- Development environment setup
- Rust learning, http framework research
- Evaluation of Stage 1

### **Evaluation 2 (August 22):**

- Evaluation of Stage 2, 3, 4

### **Evaluation 3 (October 6):**

- Evaluation of Stage 5, 6

### **Evaluation 4 (November 14):**

- Evaluation of Stage 7 / 8 or overall solution polishing&amp;refactoring

## **Timeline**

**Week**

**Activity**

**Status**

June 1 - June 30

Onboarding, research, rust learning

July 1 - July 11

Evaluation 1

Stage 1 (server)

July 11 - July 25

Stage 2 (storage)

July 26 - August 2

Stage 3 (aries-vcx as dependency)

August 3 - August 22

Evaluation 2

Stage 4 (didcomm connections)

August 23 - September 5

Stage 5 (Receiving&amp;storing didcomm messages)

September 6 - October 3

Evaluation 3

Stage 6 (Add pickup protocol)

October 4 - November 14

Evaluation 4

Refactoring / Stage 7, 8 / Other improvements / catch-ups

# Future plans

Design and document ways in which persistent connection based notification service could be integrated into mediator service project.

Benchmark the service.

Add support for did:peer:4 based did exchange.

# Participants (Mentors/Mentees)

## Mentors

NameHyperledger DiscordAffiliation*Patrik Stas**Patrik Stas#7722**Absa Group**Bogdan Mircea*

*bobozaur#5997*

*Absa Group*

*Miroslav Kovar*

*mirgee#3763**Absa Group**George Mulhearn**gmulhearn#0356*

## Mentee

NameEmailNaian G[ng.p.ref+hlfwiki@mailbox.org](mailto:ng.p.ref+hlfwiki@mailbox.org)

# Processes

Internal communication and updates:

- - Slack is used for regular communications and updates
  - Weekly Zoom meetings are scheduled to discuss the progress, blocks, questions, advice
  - Biweekly mentee-mentee meetings for knowledge sharing, active collaboration.

Mentee maintains a blog with frequent updates:

- [Aries VCX Diaries](http://envs.net/~nain/aries-vcx-diaries)

Other useful information can be found on this page

- [Learnings and Deliverables - aries-vcx based Aries Mediator Project](Learnings-and-Deliverables---aries-vcx-based-Aries-Mediator-Project_21960496.html)
- [Links: Useful research, analysis and general guide.](21960219.html)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
