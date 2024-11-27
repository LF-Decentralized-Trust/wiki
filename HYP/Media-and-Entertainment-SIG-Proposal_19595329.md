1. [Hyperledger](index.html)
2. [LF Decentralized Trust](LF-Decentralized-Trust_19595266.html)
3. [Special Interest Groups](Special-Interest-Groups_19595400.html)
4. [SIG Process - Launch &amp; Operations](19595382.html)
5. [SIG Proposals](SIG-Proposals_19595405.html)
6. [SIG Archived Proposals](SIG-Archived-Proposals_19599815.html)

# Hyperledger : Media and Entertainment SIG Proposal

Created by David Boswell, last modified by David MacFadyen on Feb 01, 2021

## **Proposal for the Creation of a Special Interest Group (SIG) in the Fields of Media and Entertainment (ME)**

Note: This Special Interest Group will be created if there is enough interest from community members in this idea.  To express interest for creating this group, please subscribe to the [Media &amp; Entertainment SIG mailing list](https://lists.hyperledger.org/g/media-entertainment-sig) **by clicking on that link and then clicking on the 'Join This Group' button**.  We will use that mailing list to communicate with people who are interested and will announce the launch of the SIG if the the group is created.

### **1. Introduction and Work Goals**

The ME-SIG will bring together technical, academic, and industry-related expertise in order to solve long-standing problems in the creation, fair distribution, and legally appropriate attribution of media assets (film, television, e-books, audiobooks, hi-res gallery or museum images, photojournalism, games, e-sports, and so forth).

The ME-SIG will use decentralized, permissioned HL blockchains to discuss and build ​user-friendly​ apps that respond to the relative disorder of permissonless environments, where artists’ interests are significantly harder to safeguard.

Following comparative analyses of the technical challenges (and hypothetical solutions) facing filmmakers, musicians, novelists, poets, photojournalists, etc., these DLT apps/dapps will be created for content-creators and their publishers, irrespective of location or socioeconomic status. This implies a focus upon UX/UI concerns over command-line tools, all in the name of access and inclusivity.

The desirability of/need for such goals was well expressed in July 2020 by ​Ashna Gupta​: “​Imagine this: a single platform where you can search for a song and uncover a record of every single player that has touched that song from inception to delivery. Every songwriter, producer, sound engineer, and everyone in between. Imagine a transparent revenue-sharing model that pays artists their fair share of royalties right away. Imagine a world of increased trustand accountability between artists and large media corporations.” The ME-SIG will aggregate and leverage the shared skills of HL members to make such hopes a reality.

```
*
```

### **2. The Raison d’être for a TME-SIG in 2021\***

A full twenty years ago, Lev Manovich (CUNY) published an influential article, “​Database as a Genre of New Media​,” in which he argued that databases have supplanted novels as our main repositories of cultural knowledge. Within those socially accessible archives, data structures and algorithms form bidirectional supply chains of information. Users chose what to up- or download. Publishers decide what to post, stream, and take down.

Manovich’s famous study benefits from a quick comparison with the work of Canadian academic Jonathan Sterne, best known for an equally dated publication of 2006, “​The MP3 as Cultural Artifact​.” Here Sterne developed a philosophy of practice (aka praxeology) for the most popular audio format in the world, which has filled bottomless databases since the launch of Napster (1999) and iTunes (2001).

Those two studies are important for the SIG because the MP3 is, first and foremost, an exercise in reduction: much like a telephone signal, it is reduced to the smallest possible dimensions (or lowest possible fidelity) in order to move in and out of databases with maximum speed. In Sterne’s own terms, the MP3 is a small “container for containers.” It both holds and transforms its contents according to the central need for ​exchange​, not use—to the point it remains perfectly/paradoxically designed for the one crime it hopes to prohibit: piracy or endless, illegal swapping. 

An MP3’s ability to be exchanged or shared remains more important than an audiophile’s insistence upon a high-quality/hi-fi use of content. The story of a file’s lifespan is more telling than whatever story it may contain (a song, podcast, audiobook, etc). The cultural importance of an MP3 resides in what’s ​done​ with it—a potentially lawless problem that HL can solve.

The same tension between mediated control (iTunes/Spotify) and chaos (Napster/torrents) endures in the relationship between permissioned and permissionless blockchains. Indeed, in a related ​2018 study​, Jérôme Pons chronicles the benefits of many decentralized autonomous organizations (DAO) for the culture and entertainment industry, concluding that blockchains can help artist and publisher alike. And so, in the light of such promise, what’s the current state of play, especially with regard to Hyperledger and fairer, faster databases?

\*

### **3. The Recent History of Permissioned DLTs/DAOs in Media and Entertainment**

### **—Stage One (2017-2018)**

In ​2017​, ​discussions​ of media-centric DAOs tended to emphasize artists’ credit and compensation. Decentralized repositories of metadata, for example, would help to protect creators’ copyright in a $15bn industry. Sobering reference was made to some (still) ongoing court cases with legacy acts—​The Three Degrees​ and ​Carpenters​—brought against record companies for unpaid royalties.

Amid these cautionary ​tales​,​ Hyperledger’s ​vision statement​ of 2018 highlighted multiple aspects of rights attribution. The in-house HLF project name-checked most often was Dot Blockchain Media (dotBC), a music content rights registry and transaction processor across a then-purported network of more than 63M compositions. (doTB has since morphed into ​Verifi Media​ and ​Cardstack​, where permissioned blockchains are now combined with the versioning tools of GitHub to create “gitchains.”)

Boston’s ​Open Music Initiative​ ​was also referenced in early Hyperledger materials. Housed in the Berkelee College of Music, the OMI continues today to leverage HLF as a non-profit network of “leading academic institutions, music and media industry organizations, creators, technologists, entrepreneurs and policy experts.” They, like dotBC, worked towards an open-source protocol for the uniform identification of music rights holders and creators.

These efforts were then celebrated by ​Irving Wladawsky-Berger​, former VP of Technical Strategy and Innovation at IBM. Here, simultaneous with HL’s 2018 mission statement, Berklee’s spinoff ​Institute for Creative Entrepreneurship​ (ICE) was singled out for praise, along with MIT’s ​Media Lab​, ​IDEO​ ​and Context Labs​. At this time the ICE already boasted over 200 ​members​ including Sony, Universal, and Warner, together with Spotify, Pandora, Netflix, SiriusXM, YouTube, and Alibaba.

Quoting an ​article​ in Wired, Wladawsky-Berger hoped to use blockchains or decentralized databases to bridge the “serious information gap... or disconnect between the person who composed a song, the person who recorded it, and the subsequent plays.” Ideally a DAO would mean that “no-one owns the information, but everyone can access it... Keeping track of this metadata \[will mean] artists and platforms can leverage it various ways without fear of violating rights.” Hence the OMI’s ​Minimum Viable Interoperability​ APIs (MVI 1.0), syncing data associated with recordings, musical works, creators and right holders.

And so, with most frequent reference to ​Sawtooth​ (made publicly available in early 2018), HL was looking to “replace monolithic central systems with an approach based on interoperability among existing databases and distributed transactions.” Parallels were drawn with the Ethereum blockchains of Canada’s ​CoreRights​ or Consensys’ ​Ujo Music,​ who worked on smart contracts with London singer/songwriter Imogen Heap and her blockchain advocacy group ​Mycelia​.

These projects and policy-makers from the recent past help to explain the challenges and possible trajectories for a ME-SIG 2021.

\*

### **—Stage Two (2020-2021)**

In ​2021​ complaints endure over a “lack \[of] visibility, transparency and auditability” in the management of e-books, music, films/TV, e-sports, and gallery or museum holdings. Hyperledger has declared its ongoing commitment to solving “critical industry issues” and ​dispute-resolution processes​ with digital assets in telecommunication and mediated storytelling. That dedication, in turn, fosters new ME initiatives for permissioned blockchains, like tokenization or ​digital identity services.

In fact, on the subject of ​tokens​—as ​fungible and/or non-fungible​ assets—​HLF allows businesses to create their own​. FabToken on Hyperledger Fabric 2.0 enables artists, authors, and publishers to work with native cryptocurrencies and tokens. They can be transferred, exchanged or redeemed with the proper ​MSP identifiers​ (in order to process tokenization in immutable forms).

A quick and concrete comparison of two Asian examples is useful here. In ​June 2020,​ a “Blockchain Based Contracts and Rights Management System”or ​bCRMS​ transpired for Indian storytellers, again manifesting an enduring focus on file ​exchange ​over file-content ​usage.​ Creators using ​bCRMS​ can secure rights or royalty tracking while protecting IP with HLF content hashing and forensic watermarking.

DLTs in Indian entertainment can thus record and track the exchange/ownership of creative assets—automatically. Meanwhile in ​Korea,​ CJ OliveNetworks have launched a HLF blockchain digital copyrights system to fix music access histories in the exchange of advertisements, promotional videos, and other tiny narrative forms.

We should mention one more example to show how music epitomizes both the challenges and opportunities lying ahead for ME DLTs. The ​Decentralized Identity Foundation​ (wittily listing its home address as “everywhere”) operates a system of so-called “hubs” and “agents.” The former are services to help an identity owner or creator manage his/her data and interact with it; the latter (employing Hyperledger Indy) are delegated keys, exchanging digital credentials and “otherwise doing an identity owner’s bidding.” The relationship is synergistic: much “like a drummer and guitarist, they contribute in vital and complementary ways to the music of identity.” While such a ​metaphor​ may seem superficial, even inconsequential, it nonetheless speaks to the unflagging status of music as touchstone in decentralized enterprise. 

This is not a surprise, since musical storytelling was digitized and democratized much earlier than e-books, filmmaking, or gaming. Music—for both artists and publishers—is ​still ​a fragmented industry, while also offering the most familiar and/or striking metaphors of how such collaboration and/or teamwork ​should​ succeed. It is the primary battleground for fairness.

\*

### **4. Conclusion**

Since the introduction in 2001 of legal, digitized music databases (iTunes), the attribution of authors’, performers’, and publishers’ rights has been a broadly consequential problem, one worsened with the subsequent popularity of e-books, digital photojournalism, streaming film or TV, and gaming. Art forms such as cinema are authored by many people at once, just as popular songwriting emerges from complex teamwork between studio technicians, lyricists, DJs, backing vocalists, etc. In modern digital markets, these and other creators are often unfairly paid or receive a paltry income from streaming platforms.

In an increasingly networked world of Manovich’s “cultural databases,” therefore, where Sterne’s theory of file exchange over file content-use still holds sway, it is remarkable that authors, artists, and their representatives still fight for proper attribution. DLT, however, offers promising and feasible correctives.

\*

### Proposed Scope for a ME-SIG

The ME-SIG will focus on the application of Hyperledger DLTs to media-specific and entertainment use cases. Such activity will automatically foreground topics such as decentralized metadata, digital distribution, copyright protection, royalty payments, value chains, NFTs (non-fungible tokens), tokenized content, counterfeit reduction, and registered digital ownership. By logical extension, these same themes will lead to real-world scenarios or solutions for cinematic, literary, audiovisual, and photographic publishers, to name but four.

As with other SIGs, so the ME may well lead to sub-groups/sub-domains. *

Following the established activities of the Social Impact and Trade Finance SIGs, the TME group can hope to:

- Collaborate with other core Hyperledger working groups and project in the areas of architecture

           —-performance and scalability identity  
           —-smart contracts  
           —-and integration

- Build user-friendly DLT ME applications on HL, focusing on UX-UI goals over command-line tools alone, thus simplifying the workflow of HLF—for easier adoption by both artists and arts-related communities
- Research different protocols—to build standardization across different parties and projects
- Identify related reference architectures (business/integration or technical/infrastructure)
- Work with businesses and non-profit or NGO communities alike
- Share stories of civic success, failure, opportunity, and challenge
- Encourage the equal involvement of both early adopters and student newcomers, looking to examine careers beyond the academic job market.

**NB 1​**: As with all Hyperledger Working and Special Interest Groups, the ME-SIG will be open to everyone​ and maintain an inclusive environment for both technical and non-technical players. The SIG will likewise report its progress to the TSC and collaborate with other Hyperledger working groups, Linux Foundation staff, and project maintainers.

**NB 2:​** The ME-SIG is prohibited from the lobbying of (or attempted influence on) government policy making and regulatory processes. Similarly, it is not intended as a platform for the procurement of services.

\*

### **Interested Parties**

The following individuals express an interest in joining this SIG, and we hope they will become contributors over the first year:

List of interested parties with consent, including name, association, and email or URL 

*\*\*\*LIST WILL GO HERE\*\*\**

*\**

### **Proposed Chair**

The following individual(s) have volunteered to serve as the initial Chair : David MacFadyen, Professor UCLA [https://www.davidmacfadyen.com/](https://www.davidmacfadyen.com/)

*\*​ In the name of brevity, the examples in this proposal refer primarily to music, yet are equally applicable to any audiovisual narrative form, including immersive/3D storytelling, digital collectibles, generative art, tangible and virtual museum collections.*

Document generated by Confluence on Nov 26, 2024 16:46

[Atlassian](http://www.atlassian.com/)
