1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Working Groups](Working-Groups_19005701.html)
4. [Standards WG](Standards-WG_19005755.html)

# Climate Action SIG : An ontology for anthropogenic impact accounting

Created by Alex Ivan Howard, last modified on Nov 26, 2024

**Overview**

This ontology is a tool for aggregating and consolidating impact accounting data across different standards and vocabularies. The ontology is intended to be generic enough to be used for anthropogenic impact accounting in almost any discipline and context, including climate action impact accounting.

### **Structure**

The ontology currently comprises 54 classes and 12 primary axioms.

### Premise

An agent engages in an activity that impacts a **thing**.

### Classes

- thing
  
  - agent
  - attribute
  - claim
    
    - identity claim
    - impact claim
    - measurement
    - state claim
    - report
    - attestation
  - control
    
    - classification system
    - calculation formula
    - identification system
    - indicator
    - measurement system
      
      - spatial measurement system
      - temporal measurement system
    - objective
    - parameter
      
      - inputs and outputs
      - spatial parameter
        
        - area
        - line
        - volume
        
        <!--THE END-->
        
        - location
        - position
      - temporal parameter
        
        - duration
        - instant
        - period
    - role
      
      - calibrator
      - claimant
      - operator
      - owner
      - verifier
        
        - auditor
    - spatial reference system
    - temporal reference system
  - environment
  - event
    
    - activity
      
      - calculating
      - claiming
        
        - reporting
      - measuring
      - monitoring
      - representing
      - validating
      - verifying
        
        - auditing
    - state change
  - evidence/substantiation
  - instrument
  - medium
  - process
    
    - project
  - state
  - substantiation

### Axioms

#### Primary

01. An agent engages in an activity.
02. An activity impacts an environment.
03. An environment is defined by (interrelated) parameters.
04. A state is the value of a parameter P at time position t.
05. An activity is performed with an instrument.
06. An activity has at least one thing as input.
07. An activity has at least one thing as output.
08. A claim is a statement about a (some specific) thing.
09. A claim is expressed in a claim medium.
10. An agent enacts a role.
11. An event impacts a state.
12. A control limits or directs a thing.
13. A claim can be substantiated by another thing.

#### Secondary

(Listed in OWL file.)

#### Tertiary

(Listed in OWL file.)

![](https://documents.lucid.app/documents/7c52fe9a-1292-45a4-9da5-ee47267d3eb7/pages/0_0?a=4098&x=7&y=-7385&w=978&h=969&store=1&accept=image%2F%2A&auth=LCA%20bec9b96435d970b2ff642a6a90a5c1274d326b0617bef06715dd499192fb9cd8-ts%3D1729099303)

### Definitions

**Class**

**Definition**

**Synonyms**

**Notes**

**Last edited on**

**thing**

**"Anything perceivable or conceivable."** ("object" - ISO 9000:2015(E))

"An entity is a physical, digital, conceptual, or other kind of thing with some fixed aspects; entities may be real or imaginary." ([https://www.w3.org/ns/prov#Entity](https://www.w3.org/ns/prov#Entity))

object, entity, item

"Every individual in the OWL world is a member of the class owl:Thing. Thus each user-defined class is implicitly a subclass of owl:Thing."\[[1](https://www.w3.org/TR/owl-guide/)]

thing:**agent**

**A thing that bears some form of accountability for the occurrence of another thing.**

A thing that bears some form of responsibility for an activity or for the existence of another thing, and which can be held accountable for it.

"An agent is something that bears some form of responsibility for an activity taking place, for the existence of an entity, or for another agent's activity." ([http://www.w3.org/ns/prov#Agent](http://www.w3.org/ns/prov#Agent))

"\[A] person or thing that takes an active role or produces a specified effect." (OED, Google)

"\[The] doer of an action, typically expressed as the subject of an active verb or in a by phrase with a passive verb." (OED, Google)

"occurrence" = happening or existing.

'organization' as defined in ISO's Annex SL Appendix 2 is treated in this ontology as an agent consisting of multiple other agents.

Think further about delegation.

foaf has: The **foaf:Agent** class is the class of agents; things that do stuff. A well known sub-class is foaf:Person, representing people. Other kinds of agents include foaf:Organization and foaf:Group.

2024/10/16

thing:**attribute(n)**

**A quality or feature of a thing that can be used, whether independently or in conjunction with other attributes, to identify it.**

"\[A] quality or feature regarded as a characteristic or inherent part of someone or something." (OED, Google)

An attribute is something that is expected to remain constant *for the duration of the impact accounting exercise*. It is typically *not* related to scope or extent.

"\[A] distinctive attribute or aspect of something." ("feature" ~ OED, Google)

"\[A] feature or quality belonging typically to a person, place, or thing and serving to identify them." ("characteristic" ~ OED, Google)

"\[A] distinctive attribute or characteristic possessed by someone or something." ("quality" ~ OED, Google)

"\[A] particular part or feature of something." ("aspect" ~ OED, Google)

"\[A]n attribute, quality, or characteristic of something." ("property" ~ OED, Google)

thing:attribute:**class**

The ... of a thing according to some classification system.

#AH: Not necessary for first version of AIAO.

'class' is an **individual** of class 'attribute', not a subclass thereof.

2024/10/15

thing:**claim(n)**

**A statement made by an agent about a thing.**

"\[A]n assertion that something is true." (OED, Google)

[assertion](https://www.w3.org/2003/glossary/keyword/All/assertion.html?keywords=assertion)

2024/10/15 

thing:evidence/substantiation:claim:**attestation**

**A formal statement made by an agent in which they claim to have witnessed or been presented with sufficient evidence to consider a specific claim made by another agent as truthful or accurate.**

"\[A] declaration that something exists or is the case." (OED, Google)

attest(v): "\[P]rovide or serve as clear evidence of." (OED, Google)

attest(v): "\[D]eclare that something exists or is the case." (OED, Google)

attest(v): "\[W]itness or certify formally." (OED, Google)

"A claim that is validated by formal statement of authority "

"The act of witnessing " ... "subscribing as a witness"

Attestation, evidence or proof of something.

the action of being a witness to or formally certifying something.

Cambridge: a formal statement that you make and officially say is true

Example: A Carbon Credits Issuance Certificate produced by Cercarbono.

2024/10/15

thing:claim:**audit(n)**

The result of an auditing process.

#AH: An audit, as a noun, is rather a specific procedure. An audit produces a report.

2024/10/15

thing:claim:**identity\_claim**

**A statement made by an agent about their identity, with reference to some identification system.**

2024/10/15

thing:claim:**impact\_claim**

**A statement about the causal relation between a thing, usually an activity, and a state change.**

A statement about the relation between an activity and a state change, typically following an impact accounting methodology (thing:control).

2024/10/15

thing:claim:measurement**state\_claim**

**A statement about the condition of a thing at a specific point in time, expressed in terms of one or more indicator-value pairs.**

The value of an indicator at a specific time instant.

The value of a parameter at a specific time instant.

"\[T]he particular condition that someone or something is in at a specific time." (OED, Google)

The condition of a thing at a specific point in time, expressed as some aggregate of the values of one or more parameters at that point in time.

Can be be based on measurement or calculation.

Re 'state' vs 'status:

[https://english.stackexchange.com/questions/12958/status-vs-state](https://english.stackexchange.com/questions/12958/status-vs-state)

'state' usually refers to a condition that can fluctuate along a spectrum, while 'status' usually refers to a condition that can only progress (move in one direction only) along a linear, usually discrete, scale.

2024/11/17

thing:claim:**report(n)**

**A statement, made according to some specification, about a thing.**  

A specification for a report is a thing:control

2024/10/15

thing:**control(n)**

**A thing that limits or directs another thing.**

A means of limiting or directing a thing.

"\[A] means of limiting or regulating something." (OED, Google)

"\[T]he restriction of an activity, tendency, or phenomenon." (OED, Google)

limit, regulation, constraint, guide(n),

directive, specification,

requirement,

constraint

An impact accounting standard is a control that comprises both procedures and object specifications.

"standard": {

1. "\[A] level of quality or attainment." (OED, Google)
2. "\[A] required or agreed level of quality or attainment." (OED, Google)
3. "\[S]omething used as a measure, norm, or model in comparative evaluations." (OED, Google)
4. "\[P]rinciples of conduct informed by notions of honour and decency." (OED, Google)

}

requirement: {

1. "\[A] thing that is needed or wanted." (OED, Google)
2. "\[A] thing that is compulsory; a necessary condition." (OED, Google)
3. "\[N]eed or expectation that is stated, generally implied or obligatory." (ISO Annex SL Appendix 2)

}

constraint: {

1. "\[A] limitation or restriction." (OED, Google)
2. "\[S]omething that controls what you do by keeping you within particular limits." ([Cambridge](https://dictionary.cambridge.org/dictionary/english/constraint))
3. "\[A] constraining condition, agency, or force." ([Merriam-Webster](https://www.merriam-webster.com/dictionary/constraint))
4. "\[A] restrictive condition." ([Collins](https://www.collinsdictionary.com/dictionary/english/constraint))

}

A procedure guides an activity.

procedure: {

1. "\[A]n established or official way of doing something." (OED, Google)
2. "\[A] series of actions conducted in a certain order or manner." (OED, Google)
3. "\[S]pecified way to carry out an activity or process." (ISO 9000:2015(E))

}

"methodology": {

1. "\[A] system of methods used in a particular area of study or activity." (OED, Google)

}

Methodology vs. procedure: {

1. Option 1: "methodology" is a synonym for "procedure".
2. Option 2: A methodology is a subclass of a procedure; hence narrower as a procedure.
3. Option 3: A methodology is a thing:control that simply contains a procedure.

}

An object specification is a control.

"\[D]ocument stating requirements." ("specification", ISO 9000:2015(E))

"A plan is an entity that represents a set of actions or steps intended by one or more agents to achieve some goals." ([http://www.w3.org/ns/prov#Plan](http://www.w3.org/ns/prov#Plan))

A condition limits an activity with reference to a state.

"Condition" in the sense of "if x then..." are expressed by using thing:state inside thing:control. Definitions for "condition": {

1. "\[A] situation that must exist before something else is possible or permitted." (OED, Google)
2. "\[A]n arrangement that must exist before something else can happen." ([Cambridge](https://dictionary.cambridge.org/dictionary/english/condition))
3. "\[A] premise upon which the fulfillment of an agreement depends." ([Merriam-Webster](https://www.merriam-webster.com/dictionary/condition))
4. "\[A] provision making the effect of a legal instrument contingent upon an uncertain event." ([Merriam-Webster](https://www.merriam-webster.com/dictionary/condition))
5. "\[S]omething essential to the appearance or occurrence of something else." ([Merriam-Webster](https://www.merriam-webster.com/dictionary/condition))
6. "\[A] restricting or modifying factor." ([Merriam-Webster](https://www.merriam-webster.com/dictionary/condition))

}

2024/10/15

thing:control:**classification\_system**

**A system for organising things into groups according to their attributes.**

2024/10/15

thing:control:**data\_format**

A defined structure and encoding system for the processing, storage, or presentation of data.

#AH: I don't think we need this in version 1 of AIAO. A format is not a control per se; a control can specify what the format of something should be, but that control is not a format - it is a specification for a format. "format" falls, to my mind, in the same category as "colour" - it's not a control but an attribute or property that can be controlled.

**Format:** encoding system [text, images, audio, sensor data,)

2024/10/15

thing:control:**calculation\_formula**

**A control that guides a mathematical calculation.**

"\[A] method or procedure for achieving something." (OED, Google)

"\[A] mathematical relationship or rule expressed in symbols." (OED, Google)

2024/10/15

thing:control:**identification\_system**

**A system for distinguishing individual things from one another.**

2024/10/15

thing:control:**indicator**

**A thing that indicates the state or level of another thing.**

A convention for expressing the state of a thing. 

A thing in terms of which the state of a (another) thing can be measured.

A concept that allows (guides/limits) the expression of a state of a thing.

A calculated interpretation of measured parameters that indicates the state or level of an OWL::thing.

"\[A] thing that indicates the state or level of something." (OED, Google)

"Something that shows what a situation is like" (Cambridge Dictionary)

Indicator: A proxy for the state of a property that is difficult to or cannot be measured directly.

2024/10/15

thing:control:indicator:**reputation**

"\[T]he beliefs or opinions that are generally held about someone or something." (OED, Google)

"\[A] widespread belief that someone or something has a particular characteristic." (OED, Google)

#AH: Not necessary for first version of AIAO.

2024/10/15

thing:control:**measurement\_system**

**A system for expressing and comparing quantities.**

A system for expressing states related to quantity, scale or rank.

A measurement system allows the expression of the state of a parameter.

datum

system of measurement

I.e., a system for answering the question of "How much?"

A measurement system standardises units for measuring and comparing quantities.

A spatial reference system sets standards for determining and comparing locations. A spatial reference system defines points of reference and standardises methods for describing the location of things relative to those points of reference.

Example 1: What Three Words is a spatial reference system, not a measurement system.

Example 2: The statements "300 miles south of the equator" and "482 kilometers south of the equator" make use of the same spatial reference system, but different measurement systems.

2024/10/15

thing:control:measurement\_system:**spatial\_measurement\_system**

**A system for expressing and comparing spatial quantities.**

E.g., "meter" or "yard".

thing:control:measurement\_system:**temporal\_measurement\_system**

**A system for expressing and comparing temporal quantities.**

E.g., "solar day" or "moon day"

thing:control:**objective**

**A desired state to be effected by an activity.**

"\[R]esult to be achieved." (ISO Annex SL Appendix 2)

goal

Is an attribute of thing:event:activity and thing:process:project?

2024/10/16

thing:control:**parameter**

**A limit or boundary wich defines the scope or extent of a thing.**

A limit or boundary wich defines the scope or extent of an environment, event, or process.

A quality or feature forming one of a set that defines a thing or sets the conditions of its existence or operation.

"\[A] limit or boundary which defines the scope of a particular process or activity." (OED, Google)

"\[A] numerical or other measurable factor forming one of a set that defines a system or sets the conditions of its operation." (OED, Google)

"\[A] numerical characteristic of a population, as distinct from a statistic of a sample." (OED, Google)

"\[A] standard unit used to express the size, amount, or degree of something." ("measure" ~ OED, Google)

Whether a thing is an attribute, an indicator or a parameter depends on its purpose during the impact accounting exercise and whether its value will remain constant or not during the impact accounting exercise.

If the value of an indicator or a parameter will remain fixed during impact accounting exercise and can consequently be used to distinguish the bearer thereof from other individuals with different values for that indicator or parameter, the indicator or parameter acts as an attribute and should be treated as such. 

If the value of a parameter can vary during the impact accounting exercise, but its variability is neither caused by the activity under study, nor affects the impact of the activity under study, then the parameter should simply be treated as a parameter.

If the value of a parameter can vary during the impact accounting exercise, and its variability is caused by the activity, then the parameter should rather be considered an indicator.

2024/10/15

thing:control:parameter:**spatial\_parameter**

**A parameter wich defines the spatial scope or spatial extent of an environment, an event, or a process.**

2024/10/15

thing:control:parameter:spatial\_parameter:**extent**

The amount of space that a thing occupies.

"\[T]he size or scale of something." (OED, Google)

"\[T]he degree or limit of something; how great or severe something is." (Cambridge Dictionary)

"\[T]he amount of space or surface that something occupies or the distance over which it extends." (Merriam-Webster)

"\[T]he range over which something extends." (Merriam-Webster)

"\[T]he space, amount, or degree to which a thing extends; size; length; breadth." (Collins)

Multiple sets of coordinates.

"extent" is embedded in the very definition of "parameter".

2024/11/14

thing:control:parameter:spatial\_parameter:extent:**area**

**The amount of space that a thing occupies across two spatial dimensions, expressed according to a spatial measurement system.**

region

This is an **individual** of the class 'spatial parameter', not a subclass of class 'spatial parameter'.

thing:control:parameter:spatial\_parameter:extent:**line**

**The amount of space that a thing occupies in a single spatial dimension, expressed according to a spatial measurement system.**

This is an **individual** of the class 'spatial parameter', not a subclass of class 'spatial parameter'.

Length, widht and height is each an example.

2024/10/15

thing:control:parameter:spatial\_parameter:extent:**volume**

**The amount of space that a thing occupies across three spatial dimensions, expressed according to a spatial measurement system.**

This is an **individual** of the class 'spatial parameter', not a subclass of class 'spatial parameter'.

thing:control:parameter:spatial\_parameter:**location**

**The point in space at which a thing occurs, expressed according to a spatial reference system.**

Location, or space, can - like time and periods - be either definite or fuzzy.

This is an **individual** of the class 'spatial parameter', not a subclass of class 'spatial parameter'.

Is this not rather an attribute or an indicator?

thing:control:parameter:spatial\_parameter:**position**

**The relation between the spatial locations of different parts of a thing.**

The locations of the parts of a thing relative to each other.

The arrangement of a thing in space.

"\[A] particular way in which someone or something is placed or arranged." (OED, Google)

"\[A] certain arrangement of bodily parts." (Merriam-Webster)

"\[T]he way in which something is arranged." (Cambridge Dictionary)

"\[T]he way in which someone is lying, sitting, or standing." (Cambridge Dictionary)

This is an **individual** of the class 'spatial parameter', not a subclass of class 'spatial parameter'.

Is this not rather an attribute or an indicator?

thing:control:parameter:**temporal\_parameter**

**A parameter wich defines the temporal scope or temporal extent of an environment, an event, or a process.**

2024/10/15

thing:control:parameter:temporal\_parameter:**duration**

**The amount of time that a thing occupies, expressed according to a temporal measurement system.**

"\[T]he time during which something continues." (OED, Google)

"Duration of a temporal extent expressed as a decimal number scaled by a temporal unit." (owl-time)

This is an **individual** of the class 'spatial parameter', not a subclass of class 'spatial parameter'.

thing:control:parameter:temporal\_parameter:**instant**

**The point in time at which a thing occurs, expressed according to a temporal reference system.**

"\[A] precise moment of time." ("instant" - OED, Google)

"\[A]n exact point in time." ("moment" - OED, Google)

"A temporal entity with zero extent or duration." (owl-time) It could have location, though, because "...properties ...provide alternative ways to describe the temporal position of an :Instant." (owl-time)

moment

This is an **individual** of the class 'spatial parameter', not a subclass of class 'spatial parameter'.

2024/10/16

thing:control:parameter:temporal\_parameter:**period**

**An extent of time between two (thing:parameter:temporal\_parameter:)instants.**

An extent of time of which the start and end is each marked by a specific (thing:parameter:temporal\_parameter:)instance

An extent of time defined by a specific starting instant and a specific ending instant.

"A temporal entity with non-zero extent or duration, i.e. for which the value of the beginning and end are different." ("proper interval", owl-time)

a length or portion of time

A portion of time defined by a specific starting point in time and a specific ending point in time.

interval stretch term span phase session bout run

Some periods in time may be "fuzzy" - exact y:m:d h:m:s may be unknown, but we can attribute a starting or ending point with a certain level of confidence. I.e., they can be definite or fuzzy.

This is an **individual** of the class 'spatial parameter', not a subclass of class 'spatial parameter'.

thing:control:parameter:temporal\_parameter:**time\_position**

"A temporal position described using either a (nominal) value from an ordinal reference system, or a (numeric) value in a temporal coordinate system." ("time position", owl-time)

"A position on a time-line" ("temporal position", owl-time)

E.g., "travel through space and time"

#AH: We distinguish between 'position' and 'location' when we talk about space, so we should probably not conflate the two terms when we talk about time. The Time Ontology's definitions of "time position" and "temporal position" each conflates "position" and "location", in my opinion.

2024/10/16

thing:control:**role**

**A control that specifies the scope of and/or requirements for an agent's relation to an event.**

A predefined set of requirements, responsibilities and/or actions for an agent with regard to a specific activity.

The function assumed or part enacted by an agent in a particular situation, and which might be subjected to a thing:control.

"\[T]he function assumed or part played by a person or thing in a particular situation." (OED, Google)

"\[A] role is particular behaviour which a material entity may exhibit."

[CHEBI:50906](https://www.ebi.ac.uk/chebi/chebiOntology.do?chebiId=CHEBI%3A50906)

"A role is the function of an entity or agent with respect to an activity, in the context of a usage, generation, invalidation, association, start, and end." ([http://www.w3.org/ns/prov#Role](http://www.w3.org/ns/prov#Role))

Roles are context-specific.  
A role restricts the set of activities that an agent can perform in the context within which they enact the role.  
Roles are sometimes mutually exclusive.  
Some roles require the enacting agent to have met certain requirements to be allowed to enact the role in that context.

Cf. 4E cognition: embodied, embedded, enactive, extended.

Define 'responsibility'?

Add 'requirement' to the definition? Define 'requirement'?

Is this not an **individual** of class 'control' rather than a subclass thereof?

2024/10/15

thing:control:role:**calibrator**

**A predefined set of requirements, responsibilities and/or actions for an agent who calibrates an instrument.**

2024/10/15

thing:control:role:**claimant**

**A predefined set of requirements, responsibilities and/or actions for an agent who makes a claim.**

"\[A] person making a claim, especially in a lawsuit or for a state benefit." (OED, Google)

2024/10/15

thing:control:role:**operator**

**A predefined set of requirements, responsibilities and/or actions** **for an agent who operates a specific thing (e.g., an instrument).**

"\[A] person who operates equipment or a machine." (OED, Google)

"\[A] person or company that runs a business." (OED, Google)

A project operator is an agent who operates a project, with the project considered to be an instrument.

2024/10/15

thing:control:role:**owner**

**A predefined set of requirements, responsibilities and/or actions for an agent who owns a specific thing.**

"\[A] person who owns something." (OED, Google)

A project owner is an agent who owns a project, with the project considered to be an instrument.

2024/10/15

thing:control:role:**project\_developer**

A predefined set of responsibilities and actions for an agent who defines and prepares the conditions for an activity or a set of activities.

"\[A] person or thing that develops something." (OED, Google)

#AH: Do we need this? In an impact accounting scenario the project developer is really just a service provider to the owner of the project in question. It is ultimately the owner of the project who will be held accountable for the impact of the project, not the project developer, so do we really need to single the role of "project developer" out?

2024/10/15

thing:control:role:**verifier**

**A predefined set of requirements, responsibilities and/or actions for an agent who verifies a claim.**

"\[S]omeone who vouches for another or for the correctness of a statement." (["verifier"](https://www.vocabulary.com/dictionary/verifier))

2024/10/15

thing:control:role:verifier:**auditor**

**A predefined set of requirements, responsibilities and/or actions for an agent who conducts an audit.**

"\[A] person who conducts an audit." (OED, Google)

"\[P]erson who conducts an audit." (ISO 9000:2015(E))

2024/10/15

thing:control:**spatial\_reference\_system**

**A system for expressing and comparing spatial locations.**

A system for expressing states related to spatial location.

I.e., a system for answering the question of "Where?"

A measurement system standardises units for measuring and comparing quantities.

A spatial reference system sets standards for determining and comparing locations. A spatial reference system defines points of reference and standardises methods for describing the location of things relative to those points of reference.

Example 1: What Three Words is a spatial reference system, not a measurement system.

Example 2: The statements "300 miles south of the equator" and "482 kilometers south of the equator" make use of the same spatial reference system, but different measurement systems.

Location can be either an attribute or a state, depending on the context.

2024/10/15

thing:control:spatial\_reference\_system:**geocentric\_datum**

TODO.

#AH: I don't think we need to go this deep in version 1 of AIAO.

2024/10/15

thing:control:spatial\_reference\_system:**geodetic\_datum**

TODO.

#AH: I don't think we need to go this deep in version 1 of AIAO.

2024/10/15

thing:control:**temporal\_reference\_system**

**A system for expressing and comparing temporal locations.**

A system for expressing states related to temporal location.

I.e., a system for answering the question of "When?"

E.g., the Gregorian Calendar or Greenwich Time.

2024/10/16

thing:**environment**

**The surroundings and conditions in which a thing occurs.**

"\[T]he surroundings or conditions in which a person, animal, or plant lives or operates." (OED, Google)

"\[T]he setting or conditions in which a particular activity is carried on. (OED, Google)

"\[A] specified sphere of activity or knowledge." ("domain" - OED, Google)

domain (?)

(A x-scape is a coded aggregate interpretation of an environment.)

2024/10/15

thing:**event**

**A thing that occurs over a period of time** and which impacts another thing**.**

A thing that happens or takes place and which impacts an environment. An event is differentiated from an activity by the absence of explicit human intention.

"Nature has events, humans act"

"\[A] thing that happens or takes place,..." (OED, Google)

"\[A] single occurrence of a process, e.g. the ionization of one atom." (OED, Google)

"A transition in the world" ([http://www.w3.org/ns/prov#InstantaneousEvent](http://www.w3.org/ns/prov#InstantaneousEvent)).

Occurs over a period of time and has a duration.

Has a spatial dimension.

"Events include generation, usage, or invalidation of entities, as well as starting or ending of activities...

An... event... happens in the world and marks a change in the world, in its activities and in its entities. The term 'event' is commonly used in process algebra with a similar meaning. Events represent communications or interactions; they are assumed to be atomic and instantaneous." ([http://www.w3.org/ns/prov#InstantaneousEvent](http://www.w3.org/ns/prov#InstantaneousEvent))

thing:event:**activity**

**An event that is orchestrated by an agent.**

A thing that an agent does and which impacts an environment.

"\[A] thing that a person or group does or has done." (OED, Google)

"Smallest identified object of work in a project." (ISO 9000:2015(E))

"An activity is something that occurs over a period of time and acts upon or with entities; it may include consuming, processing, transforming, modifying, relocating, using, or generating entities." ([http://www.w3.org/ns/prov#Activity](http://www.w3.org/ns/prov#Activity))

action, act

"orchestrate": "\[P]lan or coordinate the elements of (a situation) to produce a desired effect..." (OED, Google)

**The only activities we are concerned with defining are the ones in which humans are in some accountable way involved in the execution thereof. If the activity cannot be used in the sentence "An agent engages in (a/an) &lt;the activity&gt;", then we are not concerned with defining it.**

2024/10/15

thing:event:activity:**calculating**

**The activity of deriving the value of a parameter or indicator from one or more other values, according to some mathematical calculation formula.** (Cf. thing:event:activity:measuring.)

The activity of deriving the value of a parameter from other parameters' values by combining them according to some mathematical thing:control:formula.

E.g., Sarah performed a calculation to determine the amount of water she needed.

2024/10/15

thing:event:activity:**evidence**

The act/ivity of being or presenting evidence in support of a claim.

"\[B]e or show evidence of." (OED, Google)

#AH: The only activities we are concerned with defining are the ones in which humans are in some accountable way involved in the execution thereof. If the activity cannot be used in the sentence, "An agent does/performs a/an &lt;the activity&gt;", then we are not concerned with defining it.

2024/10/14

thing:event:activity:**claiming**

**The activity of making a statement about a thing.**

"\[S]tate or assert that something is the case..." (OED, Google)

"\[A]ssert that one has gained or achieved (something)." (OED, Google)

assert

W3C [Glossary](https://www.w3.org/2003/glossary/subglossary/rdf-mt.rdf/): (n.) **Assertion** (i) Any expression which is claimed to be true. (ii) The act of claiming something to be true.

[https://www.w3.org/TR/vc-data-model/#claims](https://www.w3.org/TR/vc-data-model/#claims) is practically identical: "A [claim](https://www.w3.org/TR/vc-data-model/#dfn-claims) is a statement about a [subject](https://www.w3.org/TR/vc-data-model/#dfn-subjects). A [subject](https://www.w3.org/TR/vc-data-model/#dfn-subjects) is a thing about which [claims](https://www.w3.org/TR/vc-data-model/#dfn-claims) can be made."

2024/10/16

thing:event:activity:claiming:**reporting**

**The activity of making a statement about a thing according to a specification.**

2024/10/14

thing:event:activity:**measuring**

**The activity of determining the value of a parameter or indicator through observation (as opposed to calculation).** (Cf. thing:event:activity:**calculating**.)

The activity of determining a state through direct observation (as opposed to calculation), typically by using a calibrated measurement instrument.

"\[A]scertain the size, amount, or degree of (something) by using an instrument or device marked in standard units." (OED, Google)

"\[A]ssess the importance, effect, or value of (something)." (OED, Google)

"\[D]etermining the status of a system, a process, a product, a service, or an activity." ("monitoring" - ISO 9000:2015(E))

"...by using an instrument or device marked in standard units." - the involvement of standardised units of measure is captured in the definition of *state.*

2024/10/14

thing:event:activity:**monitoring**

**The activity of repeatedly determining a state over a period of time.**

"\[O]bserve and check the progress or quality of (something) over a period of time; keep under systematic review." (OED, Google)

"\[M]aintain regular surveillance over." (OED, Google)

It is a series of measurements.

2024/10/14

thing:event:activity:**representing**

**The activity of acting on behalf of another thing, usually - but not necessarily - in a different medium and/or different environment (or context) than that in which the represented thing occurs.**

The act of registering a claim unto a claim\_medium by means of an instrument. #AH: This is rather the definition of making a representation of something.

TODO: Define representation, as in a non-living thing (such as a photograph) that "represents" (passively) another thing.

2024/10/15

thing:event:activity:**validating**

**The activity of ascertaining that the form, structure or type of some thing satisfies a specification.**

Where 'specification' = a thing:control.

2024/10/15

thing:event:activity:**verifying**

**The activity of ascertaining that the content of a claim satisfies a particular specification for accuracy, truthfulness or demonstrability.**

The activity of ascertaining that some claim is true, accurate, or justified.

"\[M]ake sure or demonstrate that (something) is true, accurate, or justified." (OED, Google)

"\[C]onfirm\[], through the provision of objective evidence, that specified requirements have been fulfilled." ("verification" - ISO 9000:2015(E))

"\[T]o establish the truth, accuracy, or reality of." ([Merriam-Webster](https://www.merriam-webster.com/dictionary/verify))

ISO 9000 defines 'verification' and 'validation' indistinguishably.

2024/10/15

thing:event:activity:verifying:**auditing**

**The activity, performed by an auditor, of following a formal procedure to verify a claim.**

To perform a systematic, independent, objective and documented evaluation of a claim and its supporting evidence to determine the extent to which it complies with specific criteria. \[control]

"\[C]onduct a systematic review of." (OED, Google)

Conduct a systematic review or assessment of something.

"systematic, independent and documented process for obtaining objective evidence and evaluating it objectively to determine the extent to which the audit criteria are fulfilled" ("audit" - ISO 9000:2015(E))

Note: We can possibly broaden it in a later version to include validation.

2024/10/15

thing:event:**state\_change**

There's the event of the activity, and then there's the event of the state change caused by the activity on some environment.

It only becomes an *impact* once it is explicitly associated with an agent or an activity as its cause.

thing:**evidence/substantiation**

**A thing presented in support of the truthfulness of a claim.**

"\[T]he available body of facts or information indicating whether a belief or proposition is true or valid."

"\[I]nformation drawn from personal testimony, a document, or a material object, used to establish facts in a legal investigation or admissible as testimony in a law court."

"\[S]igns or indications of something."

Evidence can be physical (e.g., the presence of some material) or in the form of sworn statements (affidavits, witness accounts) by other agents.

A thing is never a substantiation in itself, as e.g., an agent or an activity or an instrument is a thing in itself. When a thing is presented as a substantiation to a claim, the connection between that thing and the claim is best expressed as a relationship.

2024/10/14

thing:**instrument**

**A thing used to perform an activity, but which does not undergo a significant state change due to the activity.**

(as opposed to consumables that do undergo significant state changes due to the activity)

A thing used to perform an activity. 

A thing used during the performance of an activity, and which neither forms part of the consumable inputs to the activity, nor forms part of the intended output of the activity.

A thing used during the performance of an activity, but which is not consumed by the activity. 

Input: Material in the environment of an activity that undergoes one or more significant and deliberate state changes due to the activity.

"\[A] tool or implement, especially one for precision work." (OED, Google)

"\[A] means of pursuing an aim." (OED, Google)

"\[A] measuring device used to gauge the level, position, speed, etc. of something,..." (OED, Google)

"\[A] thing made or adapted for a particular purpose, especially a piece of mechanical or electronic equipment." ("device" - OED, Google)

"\[A] plan, method, or trick with a particular aim." ("device" - OED, Google)

"\[A] device or implement, especially one held in the hand, used to carry out a particular function." ("tool" - OED, Google)

"\[A] thing used to help perform a job." ("tool" - OED, Google)

device (?)

tool (?)

Conscious decision taken not to distinguish further between measurement instruments, production instruments, communication instruments, etc., because most instruments today serve a variety of functions - e.g., a specific instrument can be used both for production and measurement.

thing:**medium**

**A thing that is altered, either temporarily or permanently, to transport another thing through space and/or time.**

"\[A]n agency or means of doing something." (OED, Google)

2024/10/16

thing:medium:**claim\_medium**

A means of representation though a control:data\_format

Media can be digital or physical

#AH: Is it necessary to include this in AIAO version 1?

A medium is a thing that can be altered, either temporarily or permanently, to serve as a vehicle of communication.

2024/10/15

thing:medium:**attestation\_medium**

A means of representation though a control:data\_format

Media can be digital or physical

#AH: Is it necessary to include this in AIAO version 1?

2024/10/15

thing:**process(n)**

**A series of interrelated and/or interacting events.**

A series of interrelated or interacting events or activities.

"\[A] series of actions or steps taken in order to achieve a particular end." (OED, Google)

"\[A] natural series of changes." (OED, Google)

"\[A] systematic series of mechanized or chemical operations that are performed in order to produce something." (OED, Google)

"\[S]et of interrelated or interacting activities that uses or transforms inputs to deliver a(n) (intended) result." (ISO Annex SL Appendix 2; ISO 9000:2015(E))

2024/10/16

thing:process:**natural\_process**

**A series of interrelated or interacting events.**

A series of interrelated or interacting natural events without a primary human cause. 

2024/10/15

thing:process:**project**

**A set of coordinated activities, undertaken to achieve an overarching objective, and subject to specific controls.**

A unique process, consisting of a set of coordinated activities, undertaken to achieve an objective under specific controls.

"\[A]n individual or collaborative enterprise that is carefully planned to achieve a particular aim." (OED, Google)

"\[A] proposed or planned undertaking." (OED, Google)

"\[U]nique process, consisting of a set of coordinated and controlled activities with start and finish dates, undertaken to achieve an objective conforming to specific requirements, including the constraints of time, cost and resources." (ISO 9000:2015(E))

### Other

The table below contains terms that were considered for inclusion in the ontology, but for which the decision was made that they were mere synonyms of other classes already included, or they were "terms of convenience" that did not identify specific classes in themselves.

**Term**

**Definition**

**Synonyms**

**Notes**

resource

FINAL: A stock or supply of money, materials, staff, and other assets that an agent can use to perform an activity. 

"\[A] stock or supply of money, materials, staff, and other assets that can be drawn on by a person or organization in order to function effectively." (OED, Google)

"\[A] source of help or information." (OED, Google)

"\[A]vailable assets." (OED, Google)

A term that can be applied to a thing when it becomes an input or instrument to an activity or process. It is not a class in itself.

input

"\[W]hat is put in, taken in, or operated on by any process or system." (OED, Google)

Is an attribute of thing:event:activity and thing:process.

A term use to describe the relation of some owl:thing to some owl:activity. It is not a class in itself.

output

"\[R]esult of a process." (ISO 9000:2015(E))

result

Is an attribute of thing:event:activity and thing:process.

A term use to describe the relation of some owl:thing to some owl:activity. It is not a class in itself.

## **Application of the ontology**

TODO: this table is a work in progress and still needs A LOT of work.

**Ontology (What are the 'things' that the accounting system should know about? What are the defining properties or characteristics of each 'thing'?)**

**Epistemology (How will the accounting system get information about these things and their attributes?)**

**Semiology (How will each of the things be represented in the accounting system?)**

**Agents**

- unique identifier (identity)
- type (individual or group; if group, what type of group, e.g. organisation, company or movement; auditor)
  
  - Develop or source a schema describing a minimum set of properties by agents type

An agent asserts their identity though digital signatures

Agents provide proofs of their properties through verified credentials 

Other parties can verify agent properties and make claims about their methods and results

Digital signature

Verified credentials 

Validation claim by third party

**Role**

See: [http://purl.obolibrary.org/obo/CHEBI\_50906](http://purl.obolibrary.org/obo/CHEBI_50906)

Definition "A role is particular behaviour which a material entity may exhibit."^^xsd:string

**Activities**

- activity class (e.g. IPCC categories)
- activity description including objective(s)
- location
- start time
- end time (possibly)
- agent
- input(s) (e.g. materials and energy; consumables and non-consumables)
- process(es): a process links inputs to products and waste
- output(s) product + waste
- objective (experience, create, reduce, destroy, avoid, verify) (optional / not required in all instances)

\* An audit is a special type of activity where the input is a claim and the output is an evaluation of that claim.

Ex ante: An agent asserts their intentions to act in a Projet Design Document (PDD) 

Ex post: An agent describe their actions in a Projet Design Document (PDD) 

The activity and its results and impacts are documented by the agent at intervals in a monitoring report (MR)

- unique identifier

Consider a token for an activity that contains all the essential elements in column 1. Such a token must have a time limit and proof of life requirements (e.g. minimum process data feed to confirm it is ongoing)

[NACE activity codes](https://nacev2.com/en)

IPCC

[NAICS](https://www.census.gov/naics/)

[ISIC](https://ilostat.ilo.org/resources/concepts-and-definitions/classification-economic-activities/)

**Environments**

- location and temporal extent (either objective or referential)
- definition (in terms of parameters of interest)

**States**

- metrics referring to parameters
- type (actual \[measured] or baseline \[counterfactual])

\*State as in environmental state (not political state)

Parameters/indicators for states

Parameters/indicators delivered by agents via PDDs and MRs

- unique identifier
- impact claim per state

**Parameters**

- name
- definition
- unit of measure
- rationale
- calculation
- credibility

(Emission factors are parameters, for example.)

- unique identifier

**Standards**

- name
- author(s)
- applicability - type of agent, type of activity, state
- requirements (e.g. reporting requirements, calculation requirements)
- version
- method(s)
- precision
- accuracy / std error
- emission factors (defaults)

<!--THE END-->

- unique identifier

**Claims**

- agent
- activity
- "before" state for every every environment and aspect of the state under consideration
- "after" state for every every environment and aspect of the state under consideration
- causal connection between activity and the resultant state (e.g. scope 1 (primary/secondary), scope 2 or scope 3)
- standard followed

### Epistemology

We know about things through direct participation in them or through representations. 

For things we experience directly we do not need any further assurance that they are true. 

## **OWL file**

[https://github.com/aartum/CA2-SIG-StandardsWG/tree/main/Schemas/OWL](https://github.com/aartum/CA2-SIG-StandardsWG/tree/main/Schemas/OWL)

## **Implementations examples**

1. Protobuf
   
   1. [UML diagram](https://lucid.app/lucidchart/bece8e81-0dfa-44c1-bad6-f1cb85bdb847/edit?viewport_loc=-1492%2C1169%2C3741%2C1447%2C0_0&invitationId=inv_0e2f3ff7-c085-45fd-9ea9-7837e32140d6) (hosted on Lucidchart; login required)
   2. [Protos](https://github.com/aartum/CA2-SIG-StandardsWG/tree/main/Schemas/protobufs)
2. Hedera Guardian

## **Vocabulary maps**

CDM - AIAO: [https://purl.archive.org/purl/aiaontology/cdmvocabulary](https://purl.archive.org/purl/aiaontology/cdmvocabulary)

Gold Standard - AIAO: [https://purl.archive.org/purl/aiaontology/gsvocabulary](https://purl.archive.org/purl/aiaontology/gsvocabulary)

VCS - AIAO: [https://purl.archive.org/purl/aiaontology/vcsvocabulary](https://purl.archive.org/purl/aiaontology/vcsvocabulary)

## **Other resources**

[https://purl.archive.org/purl/aiaontology](https://purl.archive.org/purl/aiaontology)

[https://lucid.app/lucidchart/bece8e81-0dfa-44c1-bad6-f1cb85bdb847/edit?viewport\_loc=-2589%2C184%2C5120%2C2276%2C0\_0&amp;invitationId=inv\_0e2f3ff7-c085-45fd-9ea9-7837e32140d6](https://lucid.app/lucidchart/bece8e81-0dfa-44c1-bad6-f1cb85bdb847/edit?viewport_loc=-2589%2C184%2C5120%2C2276%2C0_0&invitationId=inv_0e2f3ff7-c085-45fd-9ea9-7837e32140d6)

## Attachments:

![](images/icons/bullet_blue.gif) [Ontology-KnowledgeGraph.png](attachments/19009364/19009367.png) (image/png)  
![](images/icons/bullet_blue.gif) [CA2-SAG\_StandardsWGontology-KGv1.png](attachments/19009364/19009594.png) (image/png)  
![](images/icons/bullet_blue.gif) [AIA\_Knowledge\_Graph.png](attachments/19009364/19010069.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
