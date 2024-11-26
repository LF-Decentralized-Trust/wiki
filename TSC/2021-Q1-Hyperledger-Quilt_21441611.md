1. [Technical Oversight Committee](index.html)
2. [Technical Oversight Committee Home](Technical-Oversight-Committee-Home_21430274.html)
3. [Hyperledger Projects](Hyperledger-Projects_21447704.html)
4. [TSC Project Updates](TSC-Project-Updates_21430854.html)
5. [2021 Project Updates](2021-Project-Updates_21452543.html)

# Technical Oversight Committee : 2021 Q1 Hyperledger Quilt

Created by David Fuelling, last modified by Danno Ferrin on May 05, 2021

Project Health

Project health is unchanged from the previous quarter (I would mark it as **neutral-to-unhealthy**). Contributors have dropped to just one (me, David Fuelling, the primary maintainer) due to changing priorities at the companies that have historically funded development of Interledger and Quilt. Contributions to the project over Q1 were also *neutral*: there were only two commits to the project, although one introduced substantial new functionality in the form of [ILP-Pay](https://github.com/hyperledger/quilt/pull/479) (a port of the [JS client application](https://github.com/interledgerjs/interledgerjs/tree/master/packages/pay) of the same name) allowing for more robust micro-payment sending using the [STREAM](https://github.com/interledger/rfcs/blob/master/0029-stream/0029-stream.md) protocol.

That said, my own ability to contribute to Quilt will likely be reduced during Q2 and Q3, so while no major bugs have been identified in Quilt, adding new features is not currently a high priority because there are no external customers or developers seeking to deploy Quilt or the Java ILP Connector, at the moment. Until this changes, I will likely focus my priorities elsewhere.

On the bright side, however, there are a number of developer-grant programs spinning-up that will focus on Interledger (e.g., Coil/Mozilla's [Grant for the Web](https://www.grantfortheweb.org/)) and crypto in-general, so it will be interesting to see how developer and/or corporate interest in Interledger evolves over 2021. If this increases, it's likely that I will have more cycles to contribute, and also likely others who have historically contribute to the project would also have cycles to contribute to Quilt.

That said, if project health continues in this direction, we should consider moving Quilt into a dormant/maintenance state potentially, or become more comfortable with few contributions (at least over the short term 1 or 2 quarters)

# Required Information

1. [Have you switched from master to main in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Projects+have+two+quarters+to+comply+with+common+repo+structure?focusedCommentId=21452776)? Not yet, but there is an issue filed to perform this change (see [here](https://github.com/hyperledger/quilt/issues/481)).
2. [Have you implemented repolinter.json in all your repos](https://lf-hyperledger.atlassian.net/wiki/display/TSC/Common+Repo+structure)? Not fully, but see this [issue](https://github.com/hyperledger/quilt/issues/435) that is half-complete.

# Questions/Issues for the TSC

What happens to a project when it goes through a "lull" in contributions, such as what Quilt is experiencing now? There was some discussion awhile back by the TSC around "project states", but I haven't been tracking the TSC closely enough to know the current state of these discussions, or current HL process. Any pointers would be helpful.

# Releases

No new releases. [Most recent release was August, 2020](https://github.com/hyperledger/quilt/releases/tag/v1.3.1).

# Overall Activity in the Past Quarter

Outside of the primary contributor, there is no developer activity (e.g., no new issues filed in Q1, no external participants via email or community call).

# Current Plans

See the "Project Health" section above. Quilt development will likely be paused for some months.

# Maintainer Diversity

No new maintainers. David Fuelling is the primary maintainer, though technically [these people](https://github.com/hyperledger/quilt/blob/master/pom.xml#L62) are the core maintainer group and can address bugs. However, nobody has new functionality planned.

# Contributor Diversity

Contributor diversity is low, and unchanged.

# Additional Information

None at this time.

# Reviewed By

- [Angelo de Caro](https://lf-hyperledger.atlassian.net/wiki/people/70121:d6b0f0e4-825f-4f16-88e1-4d14e95f2f10?ref=confluence)
- [Arnaud J LE HORS](https://lf-hyperledger.atlassian.net/wiki/people/70121:0e75e3b8-500a-4067-9f7e-ed46e91bcb9d?ref=confluence)
- [Arun .S.M.](https://lf-hyperledger.atlassian.net/wiki/people/621a0e5097d313006ba7386a?ref=confluence)
- [Baohua Yang](https://lf-hyperledger.atlassian.net/wiki/people/557058:17d87dbf-05fe-4c1b-84cf-fd69f7fcbb20?ref=confluence)
- [Bobbi Muscara](https://lf-hyperledger.atlassian.net/wiki/people/5c4cb1b7d8bbb7445c0a457e?ref=confluence)
- [Danno Ferrin](https://lf-hyperledger.atlassian.net/wiki/people/5b7f2d80c4e4892a5b789551?ref=confluence)
- [David Enyeart](https://lf-hyperledger.atlassian.net/wiki/people/712020:30d7e775-8a5d-4896-8950-8da2af027639?ref=confluence)
- [Gari Singh](https://lf-hyperledger.atlassian.net/wiki/people/557058:51429e31-90f4-4684-b7cd-9a4fe15ff188?ref=confluence)
- [Grace Hartley (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/5c3e0cd1ff324728a1db2448?ref=confluence)
- [Hart Montgomery](https://lf-hyperledger.atlassian.net/wiki/people/712020:86f447c0-86dc-43b3-ac03-6a31923bbb84?ref=confluence)
- [María Teresa nieto](https://lf-hyperledger.atlassian.net/wiki/people/5d36fa46af1d920bc99755b6?ref=confluence)
- [Mark Wagner (Deactivated)](https://lf-hyperledger.atlassian.net/wiki/people/70121:81b88945-c9ef-40fe-9224-207bdb280922?ref=confluence)
- [Nathan George](https://lf-hyperledger.atlassian.net/wiki/people/712020:3e7556ab-cdb8-47f5-8b68-12a3378021fd?ref=confluence)
- [Tracy Kuhrt](https://lf-hyperledger.atlassian.net/wiki/people/712020:eb6ae9c3-aa8e-40ba-9dab-a6969b1ac52e?ref=confluence)
- [Troy Ronda](https://lf-hyperledger.atlassian.net/wiki/people/557058:c854f35a-2b58-4be3-9003-ca2a67495580?ref=confluence)

Document generated by Confluence on Nov 26, 2024 11:22

[Atlassian](http://www.atlassian.com/)
