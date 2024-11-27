1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Archive\_](Archive__19006062.html)

# Climate Action SIG : Governance Research for Climate Action

Created by Si Chen, last modified on Dec 06, 2021

Governance is a key question for climate projects using the blockchain, because the blockchain is fundamentally about creating collaboration networks.  Therefore, how the network is going to be governed directly affects the technical choices in building the network.  

### Stakeholders

Governance means balancing the needs of the different stakeholders so that the overall network, or "ecosystem" is healthy and vibrant.  While all stakeholders benefit from a healthy ecosystem, different stakeholders often incrementally gain at the expense of others.  Too much of a tilt towards one group of stakeholders, however, may cause the others to leave, causing the ecosystem as a whole to suffer.

In a typical climate ecosystem, such as the carbon credits market or climate investing, there are these stakeholders:

- sellers or issuers
- buyers
- intermediaries - transaction services
- gatekeepers - standards organizations, ratings agencies
- other service providers - data services, consultants

For example, issuers may want to create as many assets as inexpensively and quickly as possible, but too much "spam" flooding the network would drive out the buyers.  Some gatekeepers are needed to balance the two, but left to themselves, gatekeepers may impose too many fees or restrictions, constricting supply and causing the market to shrivel.   

Another interesting example is data services: There must be a large enough market to support them, which requires open standards and access to information to grow the market.  On the other hand, there must be some non-publicly available data that they could sell for a fee to justify their business.  

Since we're an open source project, the open source project is an additional group that needs to be considered.  What will motivate the open source developers to work on the project, or alternatively motivate the stakeholders to contribute to an open source project?  This creates, in turn, some tradeoffs:

- Should the project be cutting edge technology so that developer would be interested in working on it to learn new and valuable skills, or should it use more mature technologies to produce software that businesses would find useful and therefore pay to support?
- Should the project add more features or be minimalist?  More features attract more users and more developers, but could stifle potential commercial businesses and their investors.  They also have a bigger footprint of code, which would require more developers to maintain, or worse cause the code to be buggy and hurt adoption, users, and developers in the long run.  But at some point, minimalism makes a project pointless.
- How much should the project consult non-developers?  Without some input from real world users, the project is probably not going to be useful.  But could the project implement, and then support, their input?  Will it lead to more users and more developers that would keep the project going?

### Expertise

Because it is a complex subject with long-term consequences, climate action often involves questions of both facts and judgements. 

For example, with the [Investor Climate Disclosure](Investor-Climate-Disclosure_19008242.html), questions of verifiable facts may be "Did American Airlines disclose that Scope 1, 2, and 3 were such amounts", and questions of judgement may be "Is American Airlines on track with the Paris Agreement?" 

Similarly, with the [Completed Research: Voluntary Carbon Offsets Directory Research](19007691.html) and carbon offsets, questions of verifiable facts may be "how big are the trees in the forest?", and questions of judgement may be "did carbon credits improve the forest?"

Traditionally, questions of facts and judgements require answers from parties accredited by centralized authorities, such as doctors licensed by the Boards of Medicine and attorneys by the Bar Association.  In the absence of central authorities, however, successful decentralized networks have developed ways to answer complex questions.  A few examples are: 

- Peer reviewed academic journals – Academic journals accept contributions and send them to qualified experts in the field for review.  There is an informal yet highly developed reputation system for academics based on the number of published papers, the number of citations of those published papers, and the journal rankings of where the papers are published.    These metrics may be viewed as "tokens" of reputation, which are then used for getting more papers published, jobs and tenure at universities, and other professional advancements.
- Stackoverflow - Stackoverflow has formalized the [reputation system](https://stackoverflow.com/tour) for answering questions on its website.  Its reputation score unlocks more features on the website, and its badges are a source of personal pride.  More importantly, though, they are a proof of expertise for members when applying for jobs.  Therefore they may also be viewed as "tokens" of reputation.
- Wikipedia - Wikipedia has an elaborate system of [governance](https://en.wikipedia.org/wiki/Wikipedia:Administration) which includes editors, stewards, an arbitration committe, and administrators.  While anyone could edit a page on wikipedia, a group of volunteer editors are responsible for keeping them "accurate," while the arbitration committee resolves disputes.  Increasing levels of involvement in the Wikipedia project then leads to higher level positions with more privilege.
- Open source projects - Open source projects such as ours are generally run informally.  In most projects, there is a group of maintainers who control what goes into the project and its general direction.  Members of the community gain attention of the maintainers through their activity and could eventually become maintainers themselves through their contributions.  However, because it is easy to fork open source projects, it is also easy for members to leave the community and start on their own with the code.  Therefore, most open source projects tend to be homogeneous, rely on direct trust between the developers and the community, and don't have a formal reputation system, and many open source developers rely on Stackoverflow to build their personal reputation capital.
- Blockchain oracles - Oracles such as Chainlink are designed to provide accurate data to blockchain smart contracts.  Because they're designed to operate in a purely decentralized environment with minimal trust, they have very formal reputation and credit systems.  The [Chainlink 2.0 white paper](https://chain.link/whitepaper), for example, spells out how oracle members stake Chainlink tokens on the data they provide.  They earn rewards for supplying correct data but could lose tokens for supplying incorrect data.  An arbitrator could be called upon to decide whether the oracle member provided the correct data.
- DAO's - The difference between an oracle and a DAO is that oracles are supposed to supply verifiable facts while DAO's are for collective voting.  Compound has a sophisticated DAO for voting on its platform.  We have a [customized version of this DAO](DAO_19007052.html) as examples of how it could be used.

Economists (such as Partha Dasgupta) have observed that smaller networks (rural villages, open source projects, academic journals) tend to rely on informal reputation, whereas larger networks (international finance, DEFI blockchains, social networks) tend to rely on formal and quantitative reputation capital.  Stackoverflow has in fact used a formal reputation to connect multiple open source projects’ smaller, informal networks.  As a result, they’ve monetized the informal networks of open source projects.  Stackoverflow has in fact used a formal reputation to connect multiple open source projects’ smaller, informal networks.  As a result, they’ve monetized the informal networks of open source projects.

The oversight or steering function is a common feature of governance for many communities, from large social networks such as Instagram to small open source projects and academic journals.  The steering committee doesn't have to be   knowledgeable about particular topics, which requires specialized expertise, but should know what is general acceptable, which is something that a lot of people should understand.  For example, Instagram doesn't get involved in whether pet or vacation photos should get more likes, but it will control what types of content are allowed.  Similarly, the maintainers of an open source project may not be the most knowledgeable about each feature in the code base, but they should insist that there is proper documentation and testing for all the features that go into a project.

### Reputation Tokens

The examples above are all networks run by centralized authorities, which grant reputation for activity on their websites.  This creates two problems: The centralized authority would need to invest significant time and capital before there is enough activity to find experts.  Meanwhile the experts find their reputation or social capital tied up in another network, which could disappear or make changes that devalue the reputation they've earned. 

In a decentralized network, reputation should be earned for activity anywhere and owned by the experts.  That way the network would not need as much time and capital to start up, and the experts could control their reputation capital better.  

For example, we could allow users to submit their blog posts, twitter, reddit, stackoverflow, etc. profiles or activity streams.  Then the governing oversight committee could vote to grant them reputation tokens for staking on oracles or voting on DAO's. 

Alternatively, we could post a series of questions about the topic on public forums and grant reputation tokens to the responses.

### Use Cases

We can explore this further in use cases such as:

- [Governance Research for Climate Action](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Governance+Research+for+Carbon+Offsets+Directory) as part of the [Completed Research: Voluntary Carbon Offsets Directory Research](19007691.html)
- [Investor Climate Disclosure](Investor-Climate-Disclosure_19008242.html)

### Ideas for Speakers?

- Please share below:

### Reference

- [Blockchain for Climate Action and the Governance Challenge](https://www.climateledger.org/resources/Blockchain-for-Climate-Action-and-the-Governance-Challenge.pdf) brings up some other questions of governance for blockchain projects related to climate change.
- [Reputations Based Systems from a16z](https://future.a16z.com/reputation-based-systems/) recommends a non-fungible DAO token for reputation and a fungible value token to reward owners of DAO tokens based on their reputation.

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
