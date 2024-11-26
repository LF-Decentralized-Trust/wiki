1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q3 Hyperledger Cactus

Created by 竹内琢磨, last modified by artem on Oct 20, 2022

# Project Health

We had a comprehensive security audit of Cactus v1.0.0 codes performed by a third-party company. The next release to fix the points from the review will be released soon in the next quarter.  
The merge of pull-requests on the main branch had been stopped due to some unstable behavior of CI script since June, but we will make a counter measure to this problem soon.  
Hyperledger-labs Weaver maintainers are welcomed to Cactus maintainers, and we are working on merge/collaboration with them.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? **Yes**
   
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? **Yes**
   
3. Has your project implemented these inclusive language changes listed below to your repo? You can optionally [use the DCI Lint tool](https://github.com/petermetz/gh-action-dci-lint#usage) to make this a recurring action on your repo. **Yes, we use DCI-Lint as part of our CI**
   
   1. master → main
   2. slave → replicas
   3. blacklist → denylist
   4. whitelist → allowlist
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? **Yes**
   

# Questions/Issues for the TSC

None at the moment.

# Releases

**v1.0.0** =&gt; [https://github.com/hyperledger/cactus/releases/tag/v1.0.0](https://github.com/hyperledger/cactus/releases/tag/v1.0.0)

# Overall Activity in the Past Quarter

1. We were hard at work to make our Weaver merge/collaboration and made a branch for this collaboration work. On this branch, we welcomed two Weaver maintainers as the maintainers of this branch. After the merge, they will officially become maintainers on Cactus.
2. We aim to bring as much Hyperledger interoperability work efforts together as possible to make the total output greater than the individual sums (code reuse enablement, shared testing infrastructure expertise, benchmarks, release management, etc.)
3. The plan is to leverage our mono-repo project structure in order to make the above plans as painless/as low overhead as possible since we want to actively prevent bogging down everybody involved with administrative changes/refactorings/breaking changes required in the name of collaboration
4. We continue to put effort into academic research (namely a research group within Hyperledger; several Hyperledger Summer Internships with a research component have been proposed and accepted).

# Current Plans

1. Currently there are some unstable behaviors of our CI scripts and our pull-requests are stopped to be merged, but we already made a counter measure and the problem will be fixed soon. =&gt; [https://github.com/hyperledger/cactus/pull/2096](https://github.com/hyperledger/cactus/pull/2096)
2. After the above problem are fixed, we plan to finish the security audit of the 1.0.0 release and issue patch releases as necessary based on the findings (1.0.1, 1.0.2 etc.)

# Maintainer Diversity

As is required, you can find our current maintainer list here:  [https://github.com/hyperledger/cactus/blob/main/MAINTAINERS.md](https://github.com/hyperledger/cactus/blob/main/MAINTAINERS.md).

Our existing maintainers are:

- Jonathan Hamilton (Accenture)
- Jagpreet Singh Sasan (Accenture)
- Peter Somogyvari (Accenture)
- Izuru Sato (Fujitsu)
- Takuma Takeuchi (Fujitsu)
- Sandeep Nishad (IBM) * NEW LAST QUARTER
- Venkatraman Ramakrishna (IBM) * NEW LAST QUARTER

Note that Sandeep and Venkatraman from Weaver project are currently working as the maintainers only on the branch to merge with Weaver.  After the merge, we plan on adding them as Cactus maintainers.

# Contributor Diversity

[https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard](https://lfanalytics.io/projects/hyperledger%2Fcactus/dashboard)

Our contributor strength has increased in this quarter compared to the previous quarter, which is great news!

# Additional Information

N/A

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

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
