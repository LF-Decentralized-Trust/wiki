1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q3 Hyperledger Ursa

Created by Stephen Curran, last modified by Bobbi Muscara on Nov 30, 2022

Project Health

The project health continues to be shaky, albeit with a few signs that could improve the outlook. On the negative front, no new maintainers or contributors have been add this quarter and [Camilo Parra](https://lf-hyperledger.atlassian.net/wiki/people/5ade0ac99fcb1f22f34ccae2?ref=confluence) has officially stepped away from the project because his job no longer involves Hyperledger projects. Work continues on the security vulnerability mentioned in the last report. The vulnerability remains confidential and has not been publicly released as a github CVE.

On a more positive note, a [code review and assessment of Ursa](https://www.idlab.org/en/hyperledger-ursa-code-review/) was completed this past quarter and published by the [Digital Identity Lab of Canada](https://www.idlab.org/en/) (IDLab). While there were some issues identified, they were relatively minor – a positive result. The full report is available [here](https://www.idlab.org/wp-content/uploads/2022/05/URSA-IDLab-Code-Review.pdf). Thanks to the IDLab and the contributors in the creation of the report, several Canadian public sector entities and [Interac](https://www.interac.ca/en/) (Canada’s interbank network).

An expected outcome from the (very) recent approval of the Hyperledger AnonCreds project is an increase in focus on and (hopefully) activity in Ursa. The purpose of the AnonCreds project is to expand the awareness of AnonCreds, its capabilities and applicability beyond Indy. With that awareness, we expect an increase in use of the verifiable credential format and as such, the underlying open source code, including the code within Ursa.

As noted in the previous report, we hope to continue our recruitment of new maintainers and contributors to further along operation Oso (code refactoring).

At the Ursa meetings, conversation is focused on a roadmap for the projects.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Yes
   
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? Yes
   
3. Has your project implemented these inclusive language changes listed below to your repo? No
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? No
   

# Questions/Issues for the TSC

There are no issues at this time.

# Releases

No releases have been made this quarter but we hope to get some out soon for URSA-base after the pull request is reviewed and merged. Again this is a lower priority than the current security vulnerability.

# Overall Activity in the Past Quarter

There was very little activity this past quarter as this [Ursa Activity Dashboard](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard;subTab=technical?time=%7B%22from%22%3A%222022-07-01T07%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222022-09-30T23%3A59%3A59.999Z%22%7D) shows. 

# Current Plans

As it was mentioned before we hope to have the high risk vulnerability fixed and released. All the planning and coordination for these efforts have been completed. The next task is to finish and review the code and that should be done in the next few months. After this is completed the next step is to finish another section of the Ursa refactoring. This will probably be the ursa-signatures part of the refactoring. This will greatly help out Indy and others who depend heavily on Ursa for it's cryptographic key tools.

# Maintainer Diversity

- Mike Lodder (Independent)
- Brent Zundel (Evernym Inc.)
- Dan Anderson (Intel)
- Dan Middleton (Intel)

# Contributor Diversity

[https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22:%22now-90d%22,%22type%22:%22datemath%22,%22to%22:%22now%22%7D](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Fursa/dashboard?time=%7B%22from%22%3A%22now-90d%22%2C%22type%22%3A%22datemath%22%2C%22to%22%3A%22now%22%7D).  

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
