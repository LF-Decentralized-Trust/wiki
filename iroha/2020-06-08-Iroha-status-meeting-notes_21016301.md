1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 1](Iroha-1_21015959.html)
4. [Meeting notes](Meeting-notes_21016018.html)
5. [Meeting notes 2020](Meeting-notes-2020_21016022.html)

# Hyperledger Iroha : 2020-06-08 Iroha status meeting notes

Created by Vadim Reutskiy on Jun 09, 2020

## Date

08 Jun 2020

## Attendees

- [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence)

## Goals

## Discussion items

WhoNotes

[Andrei Lebedev](https://lf-hyperledger.atlassian.net/wiki/people/557058:c02f1b3d-42e6-4519-ba84-2d0476dccbc9?ref=confluence)

- There is an issue now, that we have no limit in the Iroha domain names. Alexander has faced that problem.
- Also, there is no indexing for the transaction creator
- There is still wrong information about error code in the Burrow documentation, will talk with Sara about it.

 [Михаил Болдырев](https://lf-hyperledger.atlassian.net/wiki/people/557058:584193b8-9303-4b5a-8cb3-8153294c8cc2?ref=confluence)

- Fixed tests in Burrow integration and restarted the CI process
- Stepan having issues with using Ursa from the client-side. He has failed with his approach by using a 3rd party library. Standard library signed transactions are not working.
- We need to fix the PR by Kamill into the Python library.
- Finished the migration scripts and made simple tests.
- Will take care of the Python client library

[Sara Garifullina](https://lf-hyperledger.atlassian.net/wiki/people/5b6c115b2c9bd83c03707f95?ref=confluence)

- I will take care for the Burrow docs
- Will fix the release notes for 1.2rc version

## Action items

Document generated by Confluence on Nov 26, 2024 15:05

[Atlassian](http://www.atlassian.com/)
