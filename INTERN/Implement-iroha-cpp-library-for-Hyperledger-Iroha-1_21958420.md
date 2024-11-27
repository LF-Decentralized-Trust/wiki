1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)

# Hyperledger Mentorship Program : Implement iroha-cpp library for Hyperledger Iroha 1

Created by baziorek, last modified by Min Yu on Dec 19, 2022

**Project Title**Implement iroha-cpp library for Hyperledger Iroha 1.\*, refactor iroha-cli, document changes**Status**

COMPLETED

**Difficulty**

MEDIUM  

# Description

[Hyperledger Iroha](https://www.hyperledger.org/use/iroha) 1 is blockchain implemented in C++. To interact with Irohas' nodes (perform [commands](https://iroha.readthedocs.io/en/develop/develop/api/commands.html) and [queries](https://iroha.readthedocs.io/en/develop/develop/api/queries.html)) there are few client libraries - [iroha-python](https://github.com/hyperledger/iroha-python), [iroha-javascript](https://github.com/hyperledger/iroha-javascript), [iroha-java](https://github.com/hyperledger/iroha-java), [iroha-ios](https://github.com/hyperledger/iroha-ios). Despite the fact that Iroha has implemented iroha-cli in C++ there is no client library in C++. What is more iroha-cli is deprecated and not all commands are fully supported.

The internship project in short words is to refactor iroha-cli and extract from its iroha-cpp library. Using the library would require project of entire library (inspiration are rest of libraries).

Optionally the library should be compatible with C language (extern "C") to make it easy to use the library from multiple programming languages.

# Additional Information

- [Hyperledger Iroha](https://www.hyperledger.org/use/iroha) ([documentation](https://iroha.readthedocs.io/en/master/), [chat,](https://chat.hyperledger.org/channel/iroha) [wiki](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Hyperledger+Iroha), [source code](https://github.com/hyperledger/iroha))
- [Iroha-python library](https://github.com/hyperledger/iroha-python)
- [Iroha-java library](https://github.com/hyperledger/iroha-java)
- [Iroha-javascript library](https://github.com/hyperledger/iroha-javascript)
- [Iroha-ios library](https://github.com/hyperledger/iroha-ios)
- [iroha-scala (Scala SDK)](https://github.com/hyperledger/iroha-scala) (deprecated)
- [iroha-dotnet (.Net SDK)](https://github.com/hyperledger/iroha-dotnet) (deprecated)

# Learning Objectives

The mentee will be able to learn:

- architecture of Iroha (1.x),
- work in true spirit of open-source, communicating with Iroha community, joining calls,
- writing documentation,
- following [rules of open-source code](https://iroha.readthedocs.io/en/master/community/index.html#c-style-guide) of Hyperledger Iroha,
- creating automatic tests of code,
- projecting of library architecture
- making library portable across multiple systems and compilers with CMake

# Expected Outcome

- Implemented iroha-cpp library
- Refactored iroha-cli, which would use the library and support all commands and queries
- Documentation to changes above
- Examples of using the library
- Tests

# Relation to Hyperledger

[Hyperledger Iroha](https://www.hyperledger.org/use/iroha) ([documentation](https://iroha.readthedocs.io/en/master/), [chat,](https://chat.hyperledger.org/channel/iroha) [wiki](https://lf-hyperledger.atlassian.net/wiki/display/iroha/Hyperledger+Iroha)) and its client libraries (as inspiration)

# Education Level

undergraduate or graduate, but mentee should be able to **project** and implement library.

# Skills

- Reading English documentation
- C++ advanced
- git
- basic knowledge of Protobuf
- CMake
- Python (optionally)
- JSON

# Future plans

Further improvement of the stability of the tool and the library, updating its when protobuf files would change. Hopefully another member or HL Iroha community.

# Preferred Hours and Length of Internship

Full-time of part-time.

# Mentor(s) Names and Contact Info

**Grzegorz Bazior** ([AGH University of Science and Technology](https://www.agh.edu.pl/en/))  
email: bazior\[you know what]agh.edu.pl  
Telegram: @baziorek  
Discord: baziorek#9186

**Piotr Pawłowski**  
email:  ppiotru@gmail.com  
Telegram: @pawlak00

# Final report

[![](attachments/thumbnails/21958420/21967122)](attachments/21958420/21967122.pdf)[dummyfile.txt](#)

  File Modified

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl) [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true)

PDF File [IrohaPresentationAndrzejGruntowski.pdf](attachments/21958420/21967122.pdf "Download")

Nov 20, 2022 by [baziorek](/wiki/people/70121:fcfd1447-e409-47ac-bf14-f78e6031899d)

Labels

- No labels
- [Edit Labels](# "Edit Labels")

[Preview]() [$itemLabel]($itemRenderedUrl&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true) [$itemLabel]($itemRenderedUrl&isFromPageView=true&isFromPageView=true)

File [GMT20221118-113231\_Recording.transcript.vtt](attachments/21958420/21967162.vtt "Download")

Dec 05, 2022 by [Ry Jones](/wiki/people/557058:078cecfc-fb17-4d9a-8759-b5b74efa6850)

Drag and drop to upload or [browse for files]() ![](images/icons/wait.gif)

Upload file

File description
