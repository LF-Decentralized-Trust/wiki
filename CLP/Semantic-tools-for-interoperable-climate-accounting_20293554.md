1. [Collaborative Learning Program](index.html)
2. [Collaborative Learning Program](Collaborative-Learning-Program_20283412.html)
3. [2023 CLP projects](2023-CLP-projects_20295338.html)

# Collaborative Learning Program : Semantic tools for interoperable climate accounting

Created by Alex Ivan Howard, last modified by Min Yu on Dec 04, 2023

**Project Title**Semantic tools for interoperable climate accounting**Status**

CANCELLED

**Primary Focus**

CODING  

# Description

Since 2021 the Standards Working Group (Standards WG) of Hyperledger's Climate Action and Accounting Special Interest Group (CA2-SIG) has been working on developing an Anthropogenic Impact Accounting Ontology (AIAO). Climate accounting is currently the primary use case for AIAO. The ontology aims to enable interoperability between the plethora of impact accounting standards and methodologies in the market, allowing further development of systems such as a global climate impact accounting ledger.

To date, the WG has formulated an ontology comprising a current total of 46 classes and 11 primary axioms with several more axioms on the secondary and tertiary level. The core concepts are explicated on the Standards WG's wiki and encoded in an OWL file. During the 2022/2023 southern hemisphere's summer break the Nova Institute sponsored and hosted a mentorship programme that recruited three second-year ICT university students from South Africa to refine the OWL file, develop a Turtle parser and set up an MVP triple store for the ontology.

The next steps towards operationalization of the ontology are aimed at developing the tools for interoperability between the AIA ontology and existing vocabularies in the field of impact accounting, starting with those from the climate accounting space. This will involve mapping the existing vocabularies and standards to the ontology, improving on the examples produced by the students; annotating existing climate impact data from selected case studies; and building a shape graph to validate annotated data.

# Additional Information

[Hyperledger Climate Action and Accounting SIG (CA2-SIG)](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Climate+Action+and+Accounting+SIG+Home)

[The core problem being addressed by the ontology](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Core+concepts+of+a+DLT-enabled+standardisation+architecture)

[The Anthropogenic Impact Accounting Ontology (AIAO)](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/An+ontology+for+anthropogenic+impact+accounting)

[The OWL implementation](http://purl.org/aiaontology)

[Gold Standard vocabulary map](http://purl.org/aiaontology/gsvocabulary)

[CDM vocabulary map](http://purl.org/aiaontology/cdmvocabulary)

[A protobuf implementation of the ontology (work in progress)](https://github.com/aartum/CA2-SIG-StandardsWG/tree/main/Schemas/protobufs)

[The triple store](https://triplydb.com/luciapauw/aia)

[The Turtle parser](https://github.com/PieterRuanCronje/TurtleParser)

# Learning Objectives

1. Develop a deeper understanding of the practical complexities of climate impact accounting, and anthropogenic impact accounting in general.
2. Develop a deeper understanding of ontologies, as used in the semantic web, and specifically the AIA ontology.
3. Gain practical knowledge of [SSSOM](https://github.com/mapping-commons/sssom), [SHACL](https://www.w3.org/TR/shacl/) and either [SPARQL](https://www.w3.org/TR/rdf-sparql-query/) or AI algorithms for semantic data processing (the latter depending on the mentee's skillset and interests).

# Expected Outcome

1. SSSOM maps that map AIAO to at least two prominent greenhouse gas accounting standards.
2. A SHACL shape graph that can be used to validate the conformation of annotated data to AIAO.
3. Tagged impact documents from at least 10 representative case studies, stored in an appropriate open source graph database. One of the case studies will be the work of our sister working group, the [Carbon Accounting and Certification WG](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Carbon+Accounting+and+Certification+WG) of CA2-SIG.
4. EITHER (a.) an AI model to annotate further documents according to AIAO, OR (b.) a SPARQL endpoint for querying annotated climate impact data. The choice between (a) an (b) will depend on the mentee's skillset and interests.

# Relation to Hyperledger

This project will directly advance the work of the [Hyperledger Climate Action and Accounting SIG (CA2-SIG)](https://lf-hyperledger.atlassian.net/wiki/display/CASIG/Climate+Action+and+Accounting+SIG+Home), especially that of the Standards WG.

# Mentee Skills

The mentee must have:

1. An interest in climate accounting.
2. A background in software development and/or data analysis.
3. Knowledge and experience of semantic web technologies are not required, but are highly recommended.

# Mentee Open Source Contribution Experience

Open source contribution experience is not required, but is highly recommended.

# Future plans

The Standards WG will continue to map further existing vocabularies to AIAO in order to contribute to greater interoperability between all impact accounting standards and methodologies. The Standards WG will furthermore produce tools and guidelines for less ambiguous, more comparable climate and other   impact accounting.

# Mentor(s) Names and Contact Info

[Christiaan J. Pauw](https://www.linkedin.com/in/christiaan-pauw-a5034533/), christiaan.pauw@nova.org.za, [Nova Institute NPC](https://www.nova.org.za/home.php).

[Alex Howard](https://www.linkedin.com/in/alexhoward1/), [alexivanhoward@gmail.com.](mailto:alexivanhoward@gmail.com.)

#### [Alfonso Govela](https://lf-hyperledger.atlassian.net/wiki/display/~alfonsogovela/), [alfonsogovela@me.com](mailto:alfonsogovela@me.com) Hyperledger Latinoamerica Regional Chapter

Document generated by Confluence on Nov 26, 2024 13:13

[Atlassian](http://www.atlassian.com/)
