1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 1](Iroha-1_21015959.html)
4. [Meeting notes](Meeting-notes_21016018.html)
5. [Meeting notes 2020](Meeting-notes-2020_21016022.html)

# Hyperledger Iroha : 2020-04-29 Status meeting notes

Created by Vadim Reutskiy on Apr 29, 2020

## Date

29 Apr 2020

## Attendees

- [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence)
- [Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence)
- [iceseer](https://lf-hyperledger.atlassian.net/wiki/people/557058:4990bcb6-a037-4038-8a49-fdcc925bfb4f?ref=confluence)
- [Evgeny Kovalev](https://lf-hyperledger.atlassian.net/wiki/people/712020:594f9075-4294-4635-bee5-2184c91eb7b6?ref=confluence)
- [Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence)
- [Sara Garifullina](https://lf-hyperledger.atlassian.net/wiki/people/5b6c115b2c9bd83c03707f95?ref=confluence)

## Discussion items

WhoNotes

[Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence)

- Yesterday discussed Burrow integration without workarounds and dirty solutions.
- Approximate implementation time - 3 days for [Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence) [Evgeny Kovalev](https://lf-hyperledger.atlassian.net/wiki/people/712020:594f9075-4294-4635-bee5-2184c91eb7b6?ref=confluence) [iceseer](https://lf-hyperledger.atlassian.net/wiki/people/557058:4990bcb6-a037-4038-8a49-fdcc925bfb4f?ref=confluence) . + tests and review.
- No updates on other tasks for now
- Will take care of the review on the next week only

 [Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence)

- Will take care of the Burrow PR decomposition into smaller logical parts after finishing with Call Engine task.
- Tomorrow will take on mockable VmCall

[Evgeny Kovalev](https://lf-hyperledger.atlassian.net/wiki/people/712020:594f9075-4294-4635-bee5-2184c91eb7b6?ref=confluence)

- CMake task for Burrow is almost done, only dependency resolution needed.
- Then will start working on the changes in Burrow interface and Go parts
- Approximate estimate for finishing Burrow-related tasks - end of the week
- Client API will be changed, hence we need to update documentation
- Andrei&gt; We will need to add a new error description.
- There is also the selection of the engine type as a new method in API.
- We will need to have a call with [Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence) to discuss errors and codes ([Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence) : there are error with code 5 for CallEngine)

[iceseer](https://lf-hyperledger.atlassian.net/wiki/people/557058:4990bcb6-a037-4038-8a49-fdcc925bfb4f?ref=confluence)

- Started a new task for Burrow integration. There are some issues in the build of the current Burrow.
- Estimation for the current task - until the beginning of the next week.

[Sara Garifullina](https://lf-hyperledger.atlassian.net/wiki/people/5b6c115b2c9bd83c03707f95?ref=confluence)

- Waiting for the Burrow documentation update
- [Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence) &gt; The internship is ready to start the selection. The deadline is May 15 - select three top candidates.
- Provided changes description to Stepan. Burrow is out of scope for now.

## Action items

Document generated by Confluence on Nov 26, 2024 15:05

[Atlassian](http://www.atlassian.com/)
