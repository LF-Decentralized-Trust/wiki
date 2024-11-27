1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)
5. [Implement iroha-cpp library for Hyperledger Iroha 1](Implement-iroha-cpp-library-for-Hyperledger-Iroha-1_21958420.html)

# Hyperledger Mentorship Program : Project Plan - Implement iroha-cpp library for Hyperledger Iroha 1

Created by nullpointerexception, last modified on Nov 28, 2022

## **Abstract**

[Hyperledger Iroha](https://www.hyperledger.org/use/iroha) 1 is blockchain implemented in C++. To interact with Irohas' nodes (perform [commands](https://iroha.readthedocs.io/en/develop/develop/api/commands.html) and [queries](https://iroha.readthedocs.io/en/develop/develop/api/queries.html)) there are few client libraries - [iroha-python](https://github.com/hyperledger/iroha-python), [iroha-javascript](https://github.com/hyperledger/iroha-javascript), [iroha-java](https://github.com/hyperledger/iroha-java), [iroha-ios](https://github.com/hyperledger/iroha-ios). Despite the fact that Iroha has implemented iroha-cli in C++ there is no client library in C++.

The project is about implementing the iroha-cpp library.

Optionally the library should be compatible with C language (extern "C") to make it easy to use the library from multiple programming languages.

## **Mentors**

Name

Time zone

Discord ID

Telegram ID

Email ID

Grzegorz BaziorCESTbaziorek#9186@baziorek[bazior@agh.edu.pl](mailto:bazior@agh.edu.pl)Piotr PawłowskiCEST  
@pawlak00[ppiotru@gmail.com](mailto:ppiotru@gmail.com)

## **Mentee**

Name

Time zone

Discord ID

Telegram ID

Email ID

Andrzej GruntowskiCESTByte#5828  
[andrzejggru@gmail.com](mailto:andrzejggru@gmail.com)

Communication channel:  Discord + Telegram + Email + Github

**Project repo: TBD**

## **Deliverables**

- Approved library design and flow

## **Merged PR's**

- [https://github.com/hyperledger/iroha/pull/2660](https://github.com/hyperledger/iroha/pull/2660)

## **Final Project Presentation:**

- It was presented during Iroha-BI-Weekly community meeting on 18th November 2022 ([link](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=21013325)):
  

![](plugins/servlet/confluence/placeholder/unknown-attachment)

[![](attachments/thumbnails/21958861/21967113)](attachments/21958861/21967113.pdf)

## **Milestones**

**Eval 1:**

- Configured environment to handle development library inside Hyperledger Iroha's main repository
- Prepared final design of external library

**Eval 2:**

- Completed external Iroha library in C++

**Eval 3:**

- Completed well defined documentation

**Eval 4:**

- \*Clean up, refactoring and debugging Iroha-lib
- Present final results

## **Timeline**

Dates

Tasks/Plan

Status

**June 1 - June 14**

Getting familiar with Iroha documentation and starting example database.

Building and running Iroha from code.

Mentee intro with the mentor. Introduction to the concepts of Hyperledger Iroha 1.

Build and run Hyperledger Iroha node (Irohad) and Iroha-cli from source.

Send sample commands and queries via Iroha-cli with succeed.

Done**June 15 - June 28**

Send sample command and queries via Iroha-Python and Iroha-Java library.

Reading Iroha code. Getting familiar with iroha transactions, queries and statuses.

Done

**June 29 - July 12**

Design interface of Iroha-cpp library.Done**July 13 - July 26**Start implementing iroha-cpp library. Introduce working draft/concept of the interface. Resolving current issues.Done**July 27 - Aug 9**

Refactor current implementation. Possible contact with the iroha developers on monthly meetings in order to verify current progress,

design and approach of the implementation. Create a separate directory/module for iroha-cpp client library in iroha main repository.

Independence from iroha transaction/query/status implementation. Implement own methods in order to handle auto-generated protobufs.

Done**Aug 10 - Aug 23**Implement grpc client in order to send a transaction/query/status to the iroha server. Create a separate repository (iroha-cpp). Create first PR to review.Done**Aug 24 - Sept 6**

Working on newly created draft pull request. Improvements/refactoring/testing.

[https://github.com/hyperledger/iroha/pull/2660](https://github.com/hyperledger/iroha/pull/2660)

Added atomic to Batch Transactions.  
Provided more detailed samples of usage.  
Refactored Grpc Client class.  
Removed grpc handlers.  
Extracted status code, status name and error code based on transaction hash.

Done**Sept 7 - Sept 20**Response to all comments from PR. Contact with Iroha Hyperledger developers/architect. Possible additional training(s) related to the project (on Udemy platform).Done**Sept 21 - Oct 4**Update the description. Add more samples. Reply and modify all comments from draft pull request.  
Rebase commits on top of current develop. Resolve all conflicts with develop branch.  
Squash all 56 commits into 1.  
Mark Pull Request as a Ready for review.Done**Oct 5 - Oct 18**Resolve/reply to all comments during the review. Pull Request successfully merged and closed.Done**Oct 19 - Nov 1**Prepare more detailed README file with functionalities of the library. New PR with readme file created. Attend to biweekly Iroha meetings to be up to date with the latest changes and updates.Done**Nov 2 - Nov 12**

New PR with some improvements -&gt; [https://github.com/hyperledger/iroha/pull/2935](https://github.com/hyperledger/iroha/pull/2935) → Approved &amp; Merged.

Final evaluation. Presentation of project final results to Iroha Team on bi-weekly meeting ([link](https://lf-hyperledger.atlassian.net/wiki/pages/viewpage.action?pageId=21013325)) and presentation of project.

Done

## **Methodology**

**TBD**

**Project results**

- Merge Requests:
  
  - [https://github.com/hyperledger/iroha/pull/2660](https://github.com/hyperledger/iroha/pull/2660)
  - [https://github.com/hyperledger/iroha/pull/2935](https://github.com/hyperledger/iroha/pull/2935)

**Presentation**

[IrohaPresentationAndrzejGruntowski.pdf](attachments/21958861/21967113.pdf)

## Attachments:

![](images/icons/bullet_blue.gif) [Hyperledger Mentee Project Presentation-Iroha-lib-AndrzejGruntowski.pptx](attachments/21958861/21967105.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)  
![](images/icons/bullet_blue.gif) [IrohaPresentationAndrzejGruntowski.pdf](attachments/21958861/21967113.pdf) (application/pdf)  
![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/21958861/21967120.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
