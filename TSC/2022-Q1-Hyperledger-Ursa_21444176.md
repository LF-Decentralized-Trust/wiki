1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q1 Hyperledger Ursa

Created by Cam Parra, last modified by Peter Somogyvari on May 03, 2022

Project Health

After many changes with contributors and leaders the project is undergoing a revival and restructuring. The meetings are now being planned and directed by Cam Parra. This was done since Hart Montgomery changed his role to CTO at HyperLedger and could no longer perform those duties. The project has lost a lot of momentum with losing one of it's main contributors. The good news is that a plan to refactor the code base named Operation Oso has been agreed upon and started. This work item sets to simplify and make it easier to contribute to the project and make the components of the library more reusable. This work has been proposed and has started but it's moving slowly.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? YES
   
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? YES
   
3. Has your project implemented these inclusive language changes listed below to your repo? No but in the works
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? No
   

# Questions/Issues for the TSC

 We aren't as connected to all the projects as we would like. So we would be really grateful if the TSC members could help us gather feedback about Ursa. We would appreciate this feedback and especially know how we can help integrate Ursa into their projects.

# Releases

No releases have been made this quarter but we hope to get some out soon for URSA-base which is the first part of the refactoring being done in Project Oso

# Overall Activity in the Past Quarter

As mentioned before the activity in this project has slowed down due to many changes in the contributors and leaders. We are currently working to fix that by attracting new contributors. This is being done by making the meetings more new comer friendly and leaving time for others to participate by asking questions. We believe that this will help us get input and code from people who would normally be too afraid to do so because of the intensity of the project. We continue to see the maintainers show up in the meetings and show interest in the group. They contribute not just to the calls but are very activate on the past pull requests.

We have currently one outstanding pull request which is to add a zero knowledge language to URSA. That still has work to be done as it does not meet standards of the code base but is being worked on by the maintainers to merge it.

# Current Plans

Operation OSO is the current plan that has been agreed upon by the active maintainers. Like mentioned above this refactoring is being done so that the project can be more reusable and simpler. The first step to do this will be the refactoring of the key components (not cryptographic keys) of URSA and group them into their own package. This will setup the code base to continue the refactoring in the other components of URSA such as signatures and Zero knowledge proofs. Also this is not just a separation and simplification of code. This will break up the components into their own Rust crates. This will allow users to pick and choose what part of URSA they need and want to implement. This will be a game changer for IOT and those needing to run cryptographic primitives on restricted systems.

For recruitment and participation on the project we will be taking steps to become more accessible and transparent with the work. The meeting will be more new comer friendly as mentioned above and allow for others to voice their concerns as well as propose solutions to whatever need they may have. We also plan on bringing in more contributors and implementer from different HL projects so that they can offer their insight on how URSA is being used and how it can change.

# Maintainer Diversity

- Mike Lodder (Independent)
- Brent Zundel (Evernym Inc.)
- Dan Anderson (Intel)
- Cam Parra (Kiva)
- Dan Middleton (Intel)

# Contributor Diversity

Here is the link from LF analytics:  [https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22:%22now-90d%22,%22type%22:%22datemath%22,%22to%22:%22now%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22%3A%22now-90d%22%2C%22type%22%3A%22datemath%22%2C%22to%22%3A%22now%22%7D).  

# Additional Information

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [artem](https://lf-hyperledger.atlassian.net/wiki/people/557058:5196a62e-7a77-4c97-8180-ae5a5992fb63?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Jim Zhang](https://lf-hyperledger.atlassian.net/wiki/people/712020:e39af0bd-79c1-49e2-887c-a74cef87f822?ref=confluence)
- [kamlesh nagware](https://lf-hyperledger.atlassian.net/wiki/people/557058:8e1fc425-f938-4b39-ad13-9cd8b0ddde52?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

# Submission date

![](plugins/servlet/confluence/placeholder/unknown-macro)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
