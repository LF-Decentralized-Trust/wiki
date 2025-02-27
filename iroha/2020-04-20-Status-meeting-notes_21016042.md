1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 1](Iroha-1_21015959.html)
4. [Meeting notes](Meeting-notes_21016018.html)
5. [Meeting notes 2020](Meeting-notes-2020_21016022.html)

# Hyperledger Iroha : 2020-04-20 Status meeting notes

Created by Sara Garifullina, last modified by Vadim Reutskiy on May 06, 2020

## Date

20 Apr 2020

## Attendees

- [Sara Garifullina](https://lf-hyperledger.atlassian.net/wiki/people/5b6c115b2c9bd83c03707f95?ref=confluence)
- [Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence)
- [Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence)
- [Evgeny Kovalev](https://lf-hyperledger.atlassian.net/wiki/people/712020:594f9075-4294-4635-bee5-2184c91eb7b6?ref=confluence)
- [iceseer](https://lf-hyperledger.atlassian.net/wiki/people/557058:4990bcb6-a037-4038-8a49-fdcc925bfb4f?ref=confluence)
- [Kamill Gusmanov](https://lf-hyperledger.atlassian.net/wiki/people/557058:63da6633-c7e7-46ec-af27-94ba8825efea?ref=confluence)

## Goals

- Discuss how things are going, keeping the release in mind.

## Discussion items

WhoNotes

[Sara Garifullina](https://lf-hyperledger.atlassian.net/wiki/people/5b6c115b2c9bd83c03707f95?ref=confluence)

- Prepared report for HL about Iroha release. The team needs to review it.
  
  Single blocker — burrow integration.
  
  Will work on the Release Notes and documentation to have those in time for Release

 [Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence)

- Worked on multi-hash cryptography - 1 question, need to advise from Andrei. The task appears to be bigger than expected but on review already.
- There is an issue with MST.
- Everything is ok with Utimaco. Will finish till the end of the week

[Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence)

- On Saturday had a call with Eugene, discussed Burrow storage and client request on committed transactions with Burrow call command inside. Changes are not yet made but plan to finish today - add some handles to storage and use them in Go wrapper.
- After that – reviews.
- Talked to DevOps about the release docker build - fixed the binaries.
- Other tasks should be done till the end of the week

[Evgeny Kovalev](https://lf-hyperledger.atlassian.net/wiki/people/712020:594f9075-4294-4635-bee5-2184c91eb7b6?ref=confluence)

- Call with Andrei about Burrow went very productively, waiting for Andrei’s interfaces to finish the documentation.
- While those interfaces are not ready – will work on CMake task.
- About IR-697 - very little from Eugene (change event sync implementation), most of it is on Andrei. So it will be just an addition to Andrei’s work
  
  Error rendering macro 'jira' : null

[iceseer](https://lf-hyperledger.atlassian.net/wiki/people/557058:4990bcb6-a037-4038-8a49-fdcc925bfb4f?ref=confluence)

- Productive weekend – fixed CLI by adding everything lacking.
- Found how to reproduce a phantom transaction bug: 
  
  Error rendering macro 'jira' : null
  
  . It produces 2 transactions with the same hash in storage - GRPC seems to complete the package by sending it again when there is a high load. Interesting thing: often a batch fully freezes and its transactions double in another batch - added logging to show all the blocks in storage. Close to understanding what is wrong
- Found something wrong with MST\_OFF flag - allows creating pending MSTs (it seems to be by design?).
- Another issue found. Will need to research it: 
  
  Error rendering macro 'jira' : null

[Kamill Gusmanov](https://lf-hyperledger.atlassian.net/wiki/people/557058:63da6633-c7e7-46ec-af27-94ba8825efea?ref=confluence)

- Java library. Will finish till Wednesday and cover with tests.

Bonus round: 

[Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence) and [Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence)

Decided to ditch this task for now: 

Error rendering macro 'jira' : null

because 

Error rendering macro 'jira' : null

needs to be finished. Will do it by dividing it into 2 parts: 1 to be merged into master and another – into a release branch. 

## Action items

Document generated by Confluence on Nov 26, 2024 15:05

[Atlassian](http://www.atlassian.com/)
