1. [Hyperledger Indy](index.html)
2. [Hyperledger Indy](Hyperledger-Indy_19464194.html)
3. [Meeting Agendas and Notes](Meeting-Agendas-and-Notes_19464715.html)
4. [Indy SDK Working Group Agendas](Indy-SDK-Working-Group-Agendas_19464232.html)

# Hyperledger Indy : 2019-05-22 Indy SDK Working Group Agenda

Created by Richard Esplin, last modified on May 22, 2019

## Summary:

- Planned releases for May and June.
- Other work updates
- Discussed problem with iOS, BitCode, and Rust.
- Discussed evolution of Indy SDK to include an Aries SDK, including repositories, chat channels, and meetings.

## Remember:

- [Linux Foundation Anti-Trust Policy](2019-05-22-Indy-SDK-Working-Group-Agenda_19464277.html)
- [Code of Conduct](https://lf-hyperledger.atlassian.net/wiki/spaces/events/pages/21791172/Diversity+and+Code+of+Conduct)

## Attendees:

- Richard Esplin
- Stephen Curran
- Steve McCown
- Sergey Minaev
- Mike Lodder
- Sam Curren
- Arjan Van Eersel
- Thomas Shelton
- Doug Wightman

## Release Status:

- May: Indy SDK 1.9.0
  
  - Transaction Author Agreement API (Evernym)
  - Ursa (Foundation)
  - Wallet Entities Deletion (BC.gov)
    
    [https://github.com/hyperledger/indy-sdk/pull/1588](https://github.com/hyperledger/indy-sdk/pull/1588)
  - Cached credentials / offline proofs (Evernym)
  - GitLab migration alongside Jenkins (Foundation)?
    
    - Linux should be ready, maybe Windows.
    - Need a plan for mobile devices.
    - Could run it right after the release.
- June: Indy SDK 1.9.1
  
  - Bugfixes
  - GitLab migration to replace Jenkins (Foundation)
  - Flexible Credential Attribute Tagging (BC.gov)

# Work Updates:

- Language specific libraries:
  
  - List
    
    - indy-sdk-python: Sam Curren (telegramsam)
    - indy-sdk-ruby: John Callahan (johncallahan)
    - indy-sdk-go: Arjan Van Eersel (arjanvaneersel)
    - indy-sdk-ios: Norm (nsivraj) is willing, but someone else will understand IOS development better (especially with Swift).
    - indy-sdk-java: Thomas Shelton (twshelton)
    - indy-sdk-android: Mike Lodder (mikelodder7) is willing, but someone else with more interest could take it over
    - indy-sdk-dotnet: Tomislav Markovski (tmarkovski)
    - indy-sdk-javascript: Joe Genereux (thedolie)
  - Nathan says that the repos are in progress.
  - Should they be aries repos?
- GitLab migration
  
  - Will migrate indy-sdk after migrating LibSovToken.
  - 1\) publish the proposal to community, discuss it
    
    2) implement CI and run it in parallel with current version as optional
    
    3) implement CD and target file publishing to the temporary location
    
    4) swap GL CI and Jenkins: make GL required, Jenkins optional
    
    5) disable Jenkins CD, target GL to actual artifacts location
    
    6) disable Jenkins CI
- SDK 2.0 architecture (Sergey)
  
  - Need to resolve how libvcx relates to language specific libraries
  - [https://github.com/hyperledger/indy-sdk/pull/1546](https://github.com/hyperledger/indy-sdk/pull/1546)
  - Will re-visit the proposed design in June
- HIPEs (Sergey)
  
  - Credentials Exchange HIPE
  - Payment decorator
- Warnings from rust cargo clippy (Mike)
  
  - Initial evaluation completed
  - Started fixing common errors
    
    - Using types instead of passing lots of parameters
  - Some of the suggestions break compilation
- Rust support for iOS bitcode
  
  - Error rendering macro 'jira' : null
  - Probably will be an ongoing issue as Rust and XCode / iOS upgrade LLVM versions, as the teams slip out of sync
  - Working on rebuilding the Rust compiler
- New design for revocation: (Mike)
  
  - Working on the paper. Draft of paper is available if people want to review it.
  - Actively building prototypes.
  - Ledger changes will be required, so it will take months to have a usable implementation on the Sovrin network.

# Other Open PRs:

- Plans for older pull requests: either need to finish them or reject them.

# Other Business:

- Issue with 'bitcode' being disabled in the IOS wrapper for Indy SDK. This makes the library incompatible with our commercial app that needs bitcode enabled. Does anyone know how to enable it or who to talk to about iOS issues? Bitcode needs to be enabled to submit to the App Store. IS-1261
- Emerging use case at BC.gov will require revocation; shooting for end of summer. (Access to audio: detailed discussion recorded in the last the Agent call)
- Indy SDK and Aries SDK
  
  - Prioritize in the short term creating Aries language specific libraries with a stable API for application developers, postpone splitting Indy and Aries under-the-hood.
  - Will require coordination among the maintainers of language specific libraries to allow consistency.
    
    - #aries-sdk will help with coordination
    - Git repo for aries-sdk in the short term will also help, even if it isn't used in the short term
  - Should each one have a channel on [chat.hyperledger.org?](http://chat.hyperledger.org)
    
    - Should create the channels as the library matures enough to require contributor coordination and work with users
    - #aries-sdk-go, etc
- Proposal:
  
  - Git Repos 
    
    - aries-sdk: Sergey Minaev (jovfer), Artem Ivanov (Artemkaaas), Sam Curren (telegramsam)
    - aries-sdk-python: Sam Curren (telegramsam), Andrew Whitehead (cywolf)
    - aries-sdk-ruby: John Callahan (johncallahan)
    - aries-sdk-go: Arjan Van Eersel (arjanvaneersel)
    - aries-sdk-ios: Norm Jarvis (nsivraj), Steve McCown (smccown)
    - aries-sdk-java: Thomas Shelton (twshelton), Sergey Minaev (jovfer)
    - aries-sdk-android: Mike Lodder (mikelodder7), Norm Jarvis (nsivraj)
    - aries-sdk-dotnet: Tomislav Markovski (tmarkovski)
    - aries-sdk-javascript: Joe Genereux (thedolie)
  - Chat channels:
    
    - #aries-sdk
    - We'll wait on the others. Revisit in August.
  - Meetings:
    
    - For now, we'll keep mixing Indy SDK and Aries SDK conversations.

Document generated by Confluence on Nov 26, 2024 16:50

[Atlassian](http://www.atlassian.com/)
