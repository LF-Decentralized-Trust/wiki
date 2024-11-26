1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Archived](Archived_21447696.html)
4. [Task Forces](Task-Forces_21452525.html)

# Technical Oversight Committee : Incubation entry considerations

Created by Ry Jones, last modified by Tracy Kuhrt on Aug 05, 2021

Created [PR against the hyperledger/tsc repo](https://github.com/hyperledger/tsc/pull/13)

This document provides information to help people who are considering bringing their projects to Hyperledger for incubation. Specifically, it will outline items that the TSC will take into consideration when evaluating the project, as well as, some best practices that have been followed by other projects prior to the project proposal being submitted to the TSC. Our hope is that this document will smooth the entry process for new projects being proposed. The [project proposal process](https://tsc.hyperledger.org/project-lifecycle.html#proposal) and the [template for project proposals](https://hyperledger.github.io/hyperledger-hip/) are outlined outside of this document. The goal of incubation within Hyperledger is to provide a space for projects that have high potential to grow in the community. Ideas should start in [Hyperledger Labs](https://labs.hyperledger.org/).

# Considerations

When considering projects that are proposed for incubation to Hyperledger, the TSC will consider the following items: codebase, maintainers, community, sponsors, legal, and overlap with existing projects. The below items are not hard and fast rules for projects being accepted. The considerations are a guide to project proposers. If you meet most of the considerations, you are most likely to be accepted. If you do not meet any of the considerations, you are most likely to not be accepted.

## Codebase

- Code should exist as open source software in some form. Previous accepted projects have come up through labs (e.g., Cactus, Ursa); while others previously had stand alone governance prior to joining (e.g., Besu).
- DCO sign off should exists in the code repository. If not 100% ready, the code must be capable of becoming compliant upon entry (i.e. squash commit).

## Maintainers

- The project should have multiple maintainers. These maintainers need not be from different companies; however, having maintainers from different companies is seen as a positive sign. Proposals with only one maintainer have been rejected by prior TSCs.
- The project should have demonstrable examples of POC/production uses publicly available.
- The project should have the backing of more than one organization/individuals (i.e., the project proposers should be able to demonstrate significant, long term contribution in codebase).

## Community

- TSC more likely to accept projects that have contributors familiar with open source practices. Participating in existing projects or starting in Hyperledger Labs is a great place to grow this experience.

## Sponsors

- Sponsors are advocates for the project. There should be more than one sponsor, and they should be from different organizations. They may or may not be committing resources to the project.

## Legal

- Trademark concerns – project names should not be trademarked by a contributing company or if it is, then the trademark will need to be handed over to Hyperledger. Project names must be approved by the Hyperledger marketing committee
- Projects do not require a name prior to being submitted.
- Codebase should be Apache 2 licensable, without encumbrances
  
  - Non-Apache 2 licensed code is possible, but requires Governing board approval (Section 12 subsection d of the [Hyperledger Charter](https://www.hyperledger.org/about/charter))
  - Special examination should be given to copyleft and non-licensed code.
  - Required patent licensing issues have prevented projects from entering incubation.
  - GPL licensing issues have prevented projects from entering incubation.
- If code does not already have copyright, the code should be modified to include copyright as per [Copyright and License Policy](Copyright-and-License-Policy_21430874.html) prior to being brought into Hyperledger.

## Overlap with Existing Projects

- The TSC has mentioned that they are not interested in bringing in additional distributed ledger projects. There should be a distinct advantage for a new distributed ledger project. This will be similar for other type of projects. In general, if a project is similar to an existing project, there should be a distinct advantage that the project brings over and beyond the existing project and that this cannot be contributed directly to the existing project.
- New projects should bring something to the table that current projects do not.

# Best Practices

The following best practices have been identified by previous proposals.

- Discuss the new project proposal within the community prior to submitting to the TSC for consideration. You might do this through existing chat channels, mailing lists, or direct communication with members of the community.
- Make sure that any links provided in the proposal are publicly available.
- If you need an introduction into the Hyperledger Community, the [Learnings Material Development Working Group](https://lf-hyperledger.atlassian.net/wiki/spaces/LMDWG) will provide a good introduction.

* * *

Information below this line is the original discussion. 

This is a list of considerations TSC members apply to inbound project contributions.

(Arun) **Goal:** Provide space under Hyperledger for a project that has high potential to grow in the community. The project shall be conceptually implemented and in use. Otherwise Hyperledger Labs is the place to grow up before incubation under the Hyperledger. *Ideas should start in Hyperledger Labs.*

- (Hart):  I'm fine with projects not necessarily be conceptually implemented (in full, anyway) and in use, as long as there is a community in place that convinces me that this will happen in the not too distant future.  If we have these guidelines, we also have to define "conceptually implemented" and "in use."  Does "in use" count production use cases, PoCs, running in the background on my backup work Linux box, or what exactly?  What does "conceptually implemented" mean?

# Codebase

- (Danno) Code should exist as open source software in some form
  
  - Some projects come up from labs (e.g., Cactus, Ursa)
  - Some projects have stand alone governance prior to joining (Besu ... others?)
- DCO sign off exists in the code repository 
  
  - If not 100% ready, the code is capable of becoming compliant upon entry (i.e. squash commit)
- (Arun) Answer the checklist (TODO: come up with a checklist) for a new project's proposal in terms of license/copyright, DCO requirements, file structure/repo requirement (should comply to this requirement within 6 months of incubation), CI/CD requirement, release process (will be incubation exit criteria).

# Maintainers

- (Danno) The project should have multiple maintainers
  
  - These maintainers need not be from different companies
    
    - However, having maintainers from different companies is seen as a positive sign (Hart)
  - Proposals with only one maintainer have been rejected by prior TSCs.
- (Arun) Come up with a plan to promote contributors into maintainers. Get this plan published as part of project proposal.
- (Arun) The project either has demonstrable examples of POC/production uses publicly available or has backing of more than one organization/individuals (should be able to demonstrate significant contribution in codebase, should also be able to demonstrate that this engagement is long term ~ex: 3 months long or at least 35% of the codebase contributions).

# Sponsors

- Sponsors are advocates for the project. There should be more than one sponsor, and they should be from different organizations. They may or may not be committing resources to the project.
  
  - Shall we move this definition to [https://hyperledger.github.io/hyperledger-hip/](https://hyperledger.github.io/hyperledger-hip/)?

# Legal

- (Tracy) Trademark concerns – project names should not be trademarked by a contributing company or if it is, then the trademark will need to be handed over to Hyperledger.
  
  - (Hart) Haven't we often formally named projects after approval?  I think we should just require marketing approval for a name.  This should solve the trademarking issue, as well as a number of other things (technical people pick bad names if left to their own devices!).
- (Danno) Codebase should be Apache 2 licensable, without encumbrances
  
  - Non-Apache 2 licensed code is possible, but requires Governing board approval (Section 12 subsection d of the [Hyperledger Charter](https://www.hyperledger.org/about/charter))
  - Special examination should be given to copyleft and non-licensed code.
  - Required patent licensing issues have prevented projects from entering incubation.
  - GPL licensing issues have prevented projects from entering incubation.
  - (Hart):  isn't this required explicitly?  I think this is non-negotiable.  We can also move this under legal.
- If code does not already have copyright, the code should be modified to include copyright as per [Copyright and License Policy](Copyright-and-License-Policy_21430874.html) prior to being brought into Hyperledger

# Overlap with Existing Projects

- (Tracy) The TSC has mentioned that they are not interested in bringing in additional distributed ledger projects. There should be a distinct advantage for a new distributed ledger project. This will be similar for other type of projects. In general, if a project is similar to an existing project, there should be a distinct advantage that the project brings over and beyond the existing project and that this cannot be contributed directly to the existing project.
  
  - (Hart) I think it should be the case that a new project should bring something to the table that current projects don't.  But I think this language might be a little too strong.
- (Tracy) Based on the [HIP template](https://hyperledger.github.io/hyperledger-hip/), dependent project's maintainers must sign off on the proposal before it is considered by the TSC.
  
  - (Danno) What is a dependent project? What is the difference between a dependent project and one used as a library vs. an optional integration?  What if multiple projects are integrated, can one block admission?
- (Arun) [https://hyperledger.github.io/hyperledger-hip/](https://hyperledger.github.io/hyperledger-hip/) lists that a new project proposal must be floated in mailing list such as TSC's before submitting a HIP.

# Charter

- (Arun) The project at the time of proposal must meet Hyperledger's charter as defined and amended on time to time. (Leaving it out on purpose, this is expected and implicit).
- (Arun) TSC may decide to go through in depth and understand the project, ask for special sessions. There is no fixed timeline as to when TSC makes a decision. Project proposal can bring the topic back to TSC if there are no action items pending and all questions are answered with documents to demonstrate the completion.
  
  - (Hart) This seems like rules for the TSC rather than guidelines for the project.  Can we rephrase this so it tells the submitters what to expect rather than sets rules for the TSC?
  - (Arun) Right, makes sense.

# Proposal Process

- (Arun) Follow the guidelines listed at [https://hyperledger.github.io/hyperledger-hip/](https://hyperledger.github.io/hyperledger-hip/)
- (Arun) Update checklist items for tools/website/writing blogs/marketing etc. (TODO: come up with a checklist). This becomes important as the community and number of projects grow. The requirement here is that project team follows up on completing the checklist after it is approved. Checklist can be found at [New Project Checklist - Community Architects - Hyperledger Confluence](https://lf-hyperledger.atlassian.net/wiki/display/CA/New+Project+Checklist).

# Recommendations

- (Arun) Make relevant documentations, design discussions available in public. Keep them in review before bringing for discussion in TSC meeting.
  
  - (Hart) I think this is a big one.  We shouldn't even consider proposals where these things are not yet public, and should tell submitters to come back when they are.
- (Arun) Publish the project's scope in advance. Call for public review comments on project's scope.
  
  - Optionally, make use of Hyperledger channels to invite more participation. Make use of Hyperledger mailing lists to invite and call for participation.
  - There can be special consideration, for example projects that are incubated from labs have been in the public domain, Hyperledger community is familiar with them.

Document generated by Confluence on Nov 26, 2024 11:23

[Atlassian](http://www.atlassian.com/)
