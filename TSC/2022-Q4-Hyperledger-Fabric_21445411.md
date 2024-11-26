1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2022 Project Updates](2022-Project-Updates_21443095.html)

# Technical Oversight Committee : 2022 Q4 Hyperledger Fabric

Created by David Enyeart, last modified by Danno Ferrin on Nov 04, 2022

Project Health

Hyperledger Fabric is fairly mature and stable with a Long-term support (LTS) release and incremental new features being added in minor releases. There is less churn and fewer commits than in years past, with continued focus on quality and support. New features get proposed, approved, and implemented based on a community RFC process. Mailing list activity is down a bit compared to prior years. PRs and mailing list questions are generally turned around quickly.

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? YES
2. [Have you implemented the Common Repository Structure in all your repos](https://tsc.hyperledger.org/repository-structure.html)? YES
3. Has your project implemented these inclusive language changes listed below to your repo? YES
   
   1. master → main
   2. slave → replicas
   3. blacklist → denylist
   4. whitelist → allowlist
4. Have you added an [Inclusive Language Statement](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Inclusive+Language+Example) to your project's documentation and/or Wiki pages? YES
   

# Questions/Issues for the TSC

None.

# Releases

v2.2 is the current LTS releases with patch releases approximately quarterly.

Releases past quarter:

- Fabric v2.2.8 - August 8, 2022
- Fabric v2.4.6 - August 8, 2022

Fabric CA

- v1.5.5 - July 8, 2022

Upcoming releases:

- Fabric v2.5.0 - Expected to be next LTS release

# Overall Activity in the Past Quarter

The project delivered fixes to the Fabric v2.2 and v2.4 releases, as well as Fabric CA v1.5 release.

Work is underway to implement the Purge Private Data History feature, targeted for v2.5 later this year.

New RFCs under consideration:

- [BFT Ordering service](https://github.com/hyperledger/fabric-rfcs/pull/52) (RFC 3 of 3)
- [New capability for updated Identity Mixer](https://github.com/hyperledger/fabric-rfcs/pull/53)

Related projects

- [Fabric-operator Hyperledger lab](https://github.com/hyperledger-labs/fabric-operator) - IBM continued pushing features from IBM Blockchain Platform to the open source operator.
- [Fabric workshop from Global Forum](https://github.com/hyperledgendary/full-stack-asset-transfer-guide) **-** Developed a new workshop demonstrates good practices for app development with gateway SDKs, chaincode-as-a-service for chaincode debug, and deployment using fabric-operator.

# Current Plans

The project is working on a v2.5.0 release in the release-2.5 branch, with a feature to Purge the history of private data. The feature may help organizations meet GDPR requirements with the ability to delete private data while preserving a hash of the data on the blockchain. The v2.5 release is expected around end of 2022 and is expected to become the next long-term support release. 

Fabric v3.0 release development has started, primarily around refactoring the ordering service for the upcoming BFT consensus integration. In the v3.0 release we are considering deprecation and removal of some features that have historically made deployment difficult, such as docker-in-docker chaincode building.

The project is investigating creation of ARM based binaries and docker images, due to the M1 mac (ARM-based) gaining traction in the developer community.

The project has started to shift CI from Azure Pipelines to Github Actions across the various Fabric repositories.

More details can be found in the project [ZenHub board](https://app.zenhub.com/workspaces/fabric-57c43689b6f3d8060d082cf1/board), this board provides a current priority view of the Github issues across the various Fabric repositories.

# Maintainer Diversity

6 of 8 maintainers from IBM.

# Contributor Diversity

Year to year comparison, by commit:

- Q3 2021 - 411 commits. 64% from IBM.
- Q3 2022 - 305 commits. 73% from IBM.

Year to year comparison, by contributor:

- Q3 2021 - 68 contributors. 37% from IBM.
- Q3 2022 - 45 contributors. 36% from IBM.

# Additional Information

[Insight Dashboards for Q3](https://insights.lfx.linuxfoundation.org/projects/hyperledger%2Ffabric/dashboard;subTab=technical?time=%7B%22from%22%3A%222021-07-01T04%3A00%3A00.000Z%22%2C%22type%22%3A%22absolute%22%2C%22to%22%3A%222021-10-01T04%3A00%3A00.000Z%22%7D&filter=%23%2Fdashboard%2FGit%3Fembed%3Dtrue%26_g%3D%28filters%3A%21%28%29%2CrefreshInterval%3A%28pause%3A%21t%2Cvalue%3A0%29%2Ctime%3A%28from%3A%272021-07-01T04%3A00%3A00.000Z%27%2Cto%3A%272021-10-01T04%3A00%3A00.000Z%27%29%29%26_a%3D%28description%3A%27Git%2520Overview%2520panel%27%2Cfilters%3A%21%28%28%27%24state%27%3A%28store%3AappState%29%2Cmeta%3A%28alias%3A%27Empty%2520Commits%27%2Cdisabled%3A%21f%2Cindex%3Agit%2Ckey%3Afiles%2Cnegate%3A%21t%2Cparams%3A%28query%3A%270%27%29%2Ctype%3Aphrase%29%2Cquery%3A%28match%3A%28files%3A%28query%3A%270%27%2Ctype%3Aphrase%29%29%29%29%2C%28%27%24state%27%3A%28store%3AappState%29%2Cmeta%3A%28alias%3ABots%2Cdisabled%3A%21f%2Cindex%3Agit%2Ckey%3Aauthor_bot%2Cnegate%3A%21t%2Cparams%3A%28query%3A%21t%29%2Ctype%3Aphrase%29%2Cquery%3A%28match%3A%28author_bot%3A%28query%3A%21t%2Ctype%3Aphrase%29%29%29%29%2C%28%27%24state%27%3A%28store%3AappState%29%2Cmeta%3A%28alias%3A%27Is%2520Commit%27%2Cdisabled%3A%21f%2Cindex%3Agit%2Ckey%3Atype%2Cnegate%3A%21f%2Cparams%3A%28query%3Acommit%29%2Ctype%3Aphrase%29%2Cquery%3A%28match_phrase%3A%28type%3Acommit%29%29%29%2C%28%27%24state%27%3A%28store%3AappState%29%2Cmeta%3A%28alias%3A%21n%2Cdisabled%3A%21f%2Cindex%3Agit%2Ckey%3Aauthor_org_name%2Cnegate%3A%21f%2Cparams%3A%28query%3A%27International%2520Business%2520Machines%2520Corporation%27%29%2Ctype%3Aphrase%29%2Cquery%3A%28match_phrase%3A%28author_org_name%3A%27International%2520Business%2520Machines%2520Corporation%27%29%29%29%29%2CfullScreenMode%3A%21f%2Coptions%3A%28darkTheme%3A%21f%2CuseMargins%3A%21t%29%2Cpanels%3A%21%28%28embeddableConfig%3A%28title%3A%27Commits%2520Percentage%2520By%2520Organization%27%29%2CgridData%3A%28h%3A13%2Ci%3A%271%27%2Cw%3A13%2Cx%3A22%2Cy%3A0%29%2Cid%3Agit_commits_organizations%2CpanelIndex%3A%271%27%2Ctitle%3A%27Commits%2520Percentage%2520By%2520Organization%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3AFilter%29%2CgridData%3A%28h%3A16%2Ci%3A%27788f235e-6d11-451b-ba12-50e7b8765e0f%27%2Cw%3A13%2Cx%3A0%2Cy%3A0%29%2Cid%3A%27985c11c0-a449-11ea-bb19-4b3cb1a7236f%27%2CpanelIndex%3A%27788f235e-6d11-451b-ba12-50e7b8765e0f%27%2Ctitle%3AFilter%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3ASummary%29%2CgridData%3A%28h%3A11%2Ci%3Ad65f6177-a704-4194-861d-019efd71a00f%2Cw%3A9%2Cx%3A13%2Cy%3A0%29%2Cid%3A%2713de3220-1aaf-11eb-b81d-a32b9537df14%27%2CpanelIndex%3Ad65f6177-a704-4194-861d-019efd71a00f%2Ctitle%3ASummary%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27Lines%2520Changed%2520Percentage%2520By%2520Organization%27%29%2CgridData%3A%28h%3A13%2Ci%3Aa8bec484-b99e-4cdc-96f2-722907cf4d00%2Cw%3A13%2Cx%3A35%2Cy%3A0%29%2Cid%3Ae70ac370-b6f0-11ea-83d0-e156a256d6e6%2CpanelIndex%3Aa8bec484-b99e-4cdc-96f2-722907cf4d00%2Ctitle%3A%27Lines%2520Changed%2520Percentage%2520By%2520Organization%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27About%2520Summary%27%29%2CgridData%3A%28h%3A5%2Ci%3A%270ba87e3a-a35b-4a3a-95bc-7572c0ecb90e%27%2Cw%3A9%2Cx%3A13%2Cy%3A11%29%2Cid%3A%2791b28510-ae4e-11eb-b42d-29bb7e46b0a1%27%2CpanelIndex%3A%270ba87e3a-a35b-4a3a-95bc-7572c0ecb90e%27%2Ctitle%3A%27About%2520Summary%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27About%2520Commits%2520Percentage%2520By%2520Organization%27%29%2CgridData%3A%28h%3A3%2Ci%3A%276680773a-5280-430b-9c7d-d03bca19518e%27%2Cw%3A13%2Cx%3A22%2Cy%3A13%29%2Cid%3A%279fdfe060-ae53-11eb-b42d-29bb7e46b0a1%27%2CpanelIndex%3A%276680773a-5280-430b-9c7d-d03bca19518e%27%2Ctitle%3A%27About%2520Commits%2520Percentage%2520By%2520Organization%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27About%2520Lines%2520Changed%2520Percentage%2520By%2520Organization%27%29%2CgridData%3A%28h%3A3%2Ci%3Ab7cbfd88-6612-4a08-bd6c-c5430265494d%2Cw%3A13%2Cx%3A35%2Cy%3A13%29%2Cid%3A%27193917b0-ae54-11eb-b42d-29bb7e46b0a1%27%2CpanelIndex%3Ab7cbfd88-6612-4a08-bd6c-c5430265494d%2Ctitle%3A%27About%2520Lines%2520Changed%2520Percentage%2520By%2520Organization%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27Active%2520Contributors%2520and%2520Organizations%27%29%2CgridData%3A%28h%3A13%2Ci%3Abdcfb437-9e3d-4418-94ce-5fa4a6362b78%2Cw%3A23%2Cx%3A0%2Cy%3A16%29%2Cid%3A%279d649f50-a0ee-11eb-9005-3930817a030d%27%2CpanelIndex%3Abdcfb437-9e3d-4418-94ce-5fa4a6362b78%2Ctitle%3A%27Active%2520Contributors%2520and%2520Organizations%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3ACommits%29%2CgridData%3A%28h%3A13%2Ci%3A%279167a0f4-2452-434f-b63a-2f4800b7fd30%27%2Cw%3A25%2Cx%3A23%2Cy%3A16%29%2Cid%3A%27572c48c0-a0ef-11eb-9005-3930817a030d%27%2CpanelIndex%3A%279167a0f4-2452-434f-b63a-2f4800b7fd30%27%2Ctitle%3ACommits%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27About%2520Active%2520Contributors%2520and%2520Organizations%27%29%2CgridData%3A%28h%3A3%2Ci%3A%27223e1016-00a3-430d-841f-9f42b8032606%27%2Cw%3A23%2Cx%3A0%2Cy%3A29%29%2Cid%3A%27905a6060-ae54-11eb-b42d-29bb7e46b0a1%27%2CpanelIndex%3A%27223e1016-00a3-430d-841f-9f42b8032606%27%2Ctitle%3A%27About%2520Active%2520Contributors%2520and%2520Organizations%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27About%2520Commits%27%29%2CgridData%3A%28h%3A3%2Ci%3Adab778dc-7ac0-48fb-a178-f6333fabc1dd%2Cw%3A25%2Cx%3A23%2Cy%3A29%29%2Cid%3Aef34e880-ae54-11eb-b42d-29bb7e46b0a1%2CpanelIndex%3Adab778dc-7ac0-48fb-a178-f6333fabc1dd%2Ctitle%3A%27About%2520Commits%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27Commits%2520By%2520Organization%27%29%2CgridData%3A%28h%3A13%2Ci%3A%273278fa75-0a7b-492b-9b8a-b866b45b3dc1%27%2Cw%3A23%2Cx%3A0%2Cy%3A32%29%2Cid%3Ae2bb7d40-a0f2-11eb-94e8-4323c8335d1a%2CpanelIndex%3A%273278fa75-0a7b-492b-9b8a-b866b45b3dc1%27%2Ctitle%3A%27Commits%2520By%2520Organization%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27Lines%2520Of%2520Code%2520Changed%2520By%2520Organization%27%29%2CgridData%3A%28h%3A13%2Ci%3A%2756561788-a72f-45b6-942d-b5b01a209d45%27%2Cw%3A25%2Cx%3A23%2Cy%3A32%29%2Cid%3Aa78a02c0-a0fa-11eb-94e8-4323c8335d1a%2CpanelIndex%3A%2756561788-a72f-45b6-942d-b5b01a209d45%27%2Ctitle%3A%27Lines%2520Of%2520Code%2520Changed%2520By%2520Organization%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27About%2520Commits%2520By%2520Organization%27%29%2CgridData%3A%28h%3A3%2Ci%3A%279b8b0c22-36c1-4d8f-86dd-841dfef2c6b1%27%2Cw%3A23%2Cx%3A0%2Cy%3A45%29%2Cid%3A%278e421240-ae55-11eb-b42d-29bb7e46b0a1%27%2CpanelIndex%3A%279b8b0c22-36c1-4d8f-86dd-841dfef2c6b1%27%2Ctitle%3A%27About%2520Commits%2520By%2520Organization%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27About%2520Lines%2520Of%2520Code%2520Changed%2520By%2520Organization%27%29%2CgridData%3A%28h%3A3%2Ci%3A%271c5972b7-e4c0-4fb8-a042-cd6cc9f1fd94%27%2Cw%3A25%2Cx%3A23%2Cy%3A45%29%2Cid%3A%2751418140-ae56-11eb-b42d-29bb7e46b0a1%27%2CpanelIndex%3A%271c5972b7-e4c0-4fb8-a042-cd6cc9f1fd94%27%2Ctitle%3A%27About%2520Lines%2520Of%2520Code%2520Changed%2520By%2520Organization%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27Commits%2520by%2520Time%2520Zone%27%29%2CgridData%3A%28h%3A14%2Ci%3A%27632c77ff-eb61-40aa-b101-11e75f9f28f7%27%2Cw%3A23%2Cx%3A0%2Cy%3A48%29%2Cid%3A%277f4bed90-a0fb-11eb-94e8-4323c8335d1a%27%2CpanelIndex%3A%27632c77ff-eb61-40aa-b101-11e75f9f28f7%27%2Ctitle%3A%27Commits%2520by%2520Time%2520Zone%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27Time%2520To%2520Commit%2520%28Hrs%29%27%29%2CgridData%3A%28h%3A14%2Ci%3A%274abc0674-24a1-459f-8310-d92c9f58e41e%27%2Cw%3A25%2Cx%3A23%2Cy%3A48%29%2Cid%3Aab467ee0-5756-11eb-bbd0-c758192c580e%2CpanelIndex%3A%274abc0674-24a1-459f-8310-d92c9f58e41e%27%2Ctitle%3A%27Time%2520To%2520Commit%2520%28Hrs%29%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27About%2520Time%2520To%2520Commit%2520%28Hrs%29%27%29%2CgridData%3A%28h%3A5%2Ci%3A%27261503ca-d4cd-4990-a215-f630fdbb3037%27%2Cw%3A25%2Cx%3A23%2Cy%3A62%29%2Cid%3Ab5fe1aa0-ae5e-11eb-b42d-29bb7e46b0a1%2CpanelIndex%3A%27261503ca-d4cd-4990-a215-f630fdbb3037%27%2Ctitle%3A%27About%2520Time%2520To%2520Commit%2520%28Hrs%29%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27About%2520Commits%2520by%2520Time%2520Zone%27%29%2CgridData%3A%28h%3A5%2Ci%3A%27129f247f-b4aa-464c-9112-c4a982f20f21%27%2Cw%3A23%2Cx%3A0%2Cy%3A62%29%2Cid%3A%2787e893d0-ae5d-11eb-b42d-29bb7e46b0a1%27%2CpanelIndex%3A%27129f247f-b4aa-464c-9112-c4a982f20f21%27%2Ctitle%3A%27About%2520Commits%2520by%2520Time%2520Zone%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3ASubmitters%29%2CgridData%3A%28h%3A19%2Ci%3A%278cdb35b3-6f32-416f-956b-50f7b221e73e%27%2Cw%3A21%2Cx%3A0%2Cy%3A67%29%2Cid%3A%2731f04bd0-1ab0-11eb-b81d-a32b9537df14%27%2CpanelIndex%3A%278cdb35b3-6f32-416f-956b-50f7b221e73e%27%2Ctitle%3ASubmitters%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3AOrganizations%29%2CgridData%3A%28h%3A19%2Ci%3Ad4d3ea5e-fedf-4818-bfe4-e6de2ab43a3c%2Cw%3A27%2Cx%3A21%2Cy%3A67%29%2Cid%3Aca6b1b90-1ab2-11eb-bbd0-c758192c580e%2CpanelIndex%3Ad4d3ea5e-fedf-4818-bfe4-e6de2ab43a3c%2Ctitle%3AOrganizations%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3ARepositories%29%2CgridData%3A%28h%3A19%2Ci%3Aa476e04a-1dde-4bdc-98b6-8c6d16c30b46%2Cw%3A29%2Cx%3A0%2Cy%3A86%29%2Cid%3Ade3203e0-1ab3-11eb-bbd0-c758192c580e%2CpanelIndex%3Aa476e04a-1dde-4bdc-98b6-8c6d16c30b46%2Ctitle%3ARepositories%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3AProjects%29%2CgridData%3A%28h%3A19%2Ci%3A%27077e496f-d414-4840-a3b0-3bc9da32ddcc%27%2Cw%3A19%2Cx%3A29%2Cy%3A86%29%2Cid%3A%2770e5e750-1ab5-11eb-b81d-a32b9537df14%27%2CpanelIndex%3A%27077e496f-d414-4840-a3b0-3bc9da32ddcc%27%2Ctitle%3AProjects%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%2C%28embeddableConfig%3A%28title%3A%27Organization%2520Commits%27%29%2CgridData%3A%28h%3A18%2Ci%3Ac73b96e3-a6ec-4b4a-aa9f-7bd4b158c968%2Cw%3A48%2Cx%3A0%2Cy%3A105%29%2Cid%3A%273c6f01b0-f21e-11ea-ada8-692b75e53835%27%2CpanelIndex%3Ac73b96e3-a6ec-4b4a-aa9f-7bd4b158c968%2Ctitle%3A%27Organization%2520Commits%27%2Ctype%3Avisualization%2Cversion%3A%277.6.2%27%29%29%2Cquery%3A%28language%3Alucene%2Cquery%3A%27%2A%27%29%2CtimeRestore%3A%21f%2Ctitle%3AGit%2CviewMode%3Aview%29)

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
