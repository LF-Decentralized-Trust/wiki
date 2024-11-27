1. [Climate Action SIG](index.html)
2. [Climate Action and Accounting SIG Home](Climate-Action-and-Accounting-SIG-Home_19005445.html)
3. [Working Groups](Working-Groups_19005701.html)
4. [Standards WG](Standards-WG_19005755.html)

# Climate Action SIG : Core concepts of a DLT-enabled standardisation architecture

Created by Christiaan Pauw, last modified by Alex Ivan Howard on Jun 02, 2022

The core concepts include an ontology (a view of what exists), an epistemology (a view of how we know things) and a semiology (a view of how things are represented). 

We work from the assumption that thinking well about these aspects in the beginning will enable us to develop software, systems and processes that will not easily become redundant. This does not mean that one must be able to foresee every detail of how things could develop in future; it is in a sense the opposite: if the basic structure is comprehensive yet flexible and can incorporate learning and development, the chances of becoming redundant in the future are low.

This means we are not just looking for a description of how things currently are; we are looking for a deeper description of what climate action and accounting are in essence. We are looking for a description of how things could be 100 years from now. We attempt to break the concept of climate action and the process of climate accounting down to their most essential structures and use that as a basis for designing representation thereof in software. 

## **Impact accounting within the context of climate action and the SDGs**

### Overview

The surroundings of a living being, i.e., the space or sphere in which it operates or functions, is generally referred to as the ***environment*** of the living being. Earth, as the home of a vast number of living beings, can be seen as consisting of a vast number of environments. Some of these environments have clear geographical boundaries, but many do not; most of these environments in fact overlap or can be viewed as sub-environments of some larger environment (e.g., a tidal pool can be viewed as an environment on its own, but it can also be viewed as part of the environment of its surrounding shoreline).

The ***state*** of an environment refers to the conditions prevalent in the environment. The more favourable the conditions are for sustaining life, the better (more valuable) the state is said to be; the less favourable the conditions are for sustaining life, the worse (less valuable) the state is said to be. Conditions are measured in terms of ***parameters***, such as the amount of CO2 in the environment’s atmosphere, or the average daytime temperature inside the environment.

What differentiates living beings from other objects in their environments is the capacity of living beings to ***wilfully*** engage in certain activities (such as moving themselves from one location to another, or consuming something); non-living beings do not have such a capacity (e.g., a rock can be moved from the top of a hill to the foot of the hill by wind or water or some other force, but it cannot move from the top of the hill to the foot of the hill by its own will). This means that when a living being is the ***wilful agent*** of an activity, the living being in question can be held ***accountable*** for the ***impact*** that the activity in question has on their environment.

To be able to hold an agent accountable in a manner that is fair and just, we need to be reasonably sure how their activities impact their environment – and this is where accounting standards come into play. The impact that the activity of an agent has on the state of their environment is measured and expressed in terms of the changes that the activity causes in the defining parameters of the environment; an ***accounting standard*** tells us how to measure these parameters, i.e. which of them we should measure, how often we should measure them and what methods we should use to measure them. Accounting standards also tell us how to determine the boundaries of the environment of interest and what the desired state thereof is. Finally, accounting standards tell us how to verify and report our measurements.

**![](attachments/19008188/19009133.png?height=400)**

*Figure 1: Environments within environments. The blue circle depicts Earth (the "global environment") as a subenvironment of the universal environment (the gray ellipsoid). The slightly transparent, green circles with dashed, brown borderlines represent the infinite number of possible environments of interest that exist within the global environment. The large green circle, populated with pictures of animals, trees and humans, depict one such possible environment of interest. The purple rectangle to the right of the diagram depicts the relationship between the (abstract) discipline of impact accounting and the real world - it intersects with reality, but can never account for reality in its fullness.*

### **The problem of plurality**

The problem is that humankind has, over the years, created different accounting standards for the same activities and agents, and the differences between them often lead to disagreements between their findings of how and to what extent a certain agent’s activities impact their environment. The solution to this problem is unfortunately not as simple as just choosing one of the standards and getting all of humankind to only use that standard henceforth – each of the standards have their strengths and weaknesses, and the arguments against a specific standard is often just as many as the arguments for that standard. The solution, instead, seems to lie in finding a structured way to compare the different standards – their requirements, their approaches, and what they take into account.

## **![](attachments/19008188/19009350.png?height=400)**

*Figure 2: Different impact claims for activities within a specific environment of interest.*

*The diagram depicts a hypothetical impact accounting case for an environment with four agents (Alice, Bob, Candice and Dennis) and six parameters of interest (represented by the geometric shapes).*

*The three green circles at the top of the diagram depict the environment of interest at three different points in time. The first green circle depicts the environment right before Alice, Bob, Candice and Dennis started with their activities. The second green circle depicts the environment of interest for the period during which the activities were conducted. The third green circle depicts the environment of interest right after the activities had been conducted. The first green circle thus represents the start of the accounting period, while the third green circle represents the end of the accounting period. The blue arrows depict relationships between entities in the environment: R1 highlights the relationships between agents and activities (agents engage in activities; activities do not occur by themselves); R2 highlights the relationships between activities and the parameters of the environment in which they are conducted (activities always impact their environment, and we measure that impact via parameters); R3 highlights the relationships between the parameters of the environment - parameters are usually interrelated, and because of this relation, an activity may have an indirect impact on many more parameters than just the ones that it impacts directly. See Figure 3 below for more on relations.*

*The four purple rectangles represent impact claims submitted by the four agents who engaged in activities in the environment of interest during the period of interest (i.e., during the accounting period). The geometric shapes in the claims represent their correlative parameters in the environment. The geometric shapes on the left side of each claim represent the state of their parameters before the activity in question occurred; the geometric shapes on the right side of each claim represent the state of their parameters after the activity in question occurred. The changes in the colours of the parameters from before the activity to after the activity represent the calculated impact (calculated according to the standard chosen by each of the claimants) that the activity in question had on the parameters. A colour change from green to orange or red indicates a negative impact on the parameter in question; a colour change from red to orange or green indicates a positive impact on the parameter in question. In this hypothetical scenario, Alice submitted an impact claim for her activity of travelling by car, and she took three different parameters (the diamond, trapesium and pentagon parameters) and all three types of relationships into account; Bob engaged in building activities and also took three parameters (the hexagon, triangle and pentagon parameters) into account for his impact claim, but only considered relationships of type R1; Candice travelled by aeroplane, and considered two parameters (the square and the hexagon parameters) and relation types R1 and R2 for her impact claim; Dennis, like Alice, submitted an impact claim for travelling by car, but he considered two other parameters than Alice for his claim, and also only took relations of type R1 and R2 into account. Thus, although Alice and Dennis engaged in the same activity during the same accounting period and in the same environment, their impact claims look very different - because they used two different standards to report their claims against. This represents the problem posed by a plurality of impact accounting standards.*

![](attachments/19008188/19008825.png?height=400)

*Figure 3: Different types of relations in an impact accounting scenario. Credit: Alfonso Govela ([Alfonso Govela](https://lf-hyperledger.atlassian.net/wiki/people/712020:8cbeb593-dd1b-4b43-a966-913564f1575a?ref=confluence)).*

*R1 represents the relationship that exists between an activity and an agent. An agent wilfully engages in an activity. Unlike events, activities do not happen "by themselves" - they are initiated and conducted by wilful agents. Because of this, agents can be held accountable for the impact that their activities have.*

*R2 represents the relationship between an activity and an environment. An activity always has some impact, whether beneficial or detrimental, on the environment(s) in which they are conducted. The impact occurs via the inputs and outputs of the activity, i.e., by taking something from the environment and transforming or displacing it.*

*R3 represents the relationships between different entities/parameters in the environment. Environments are usually complex systems with many interdependencies between their constituents, e.g., an impact on component X will likely have an impact on component Y, which is likely to have an impact on component Z in turn.*

*R4 represents the relationship between two states of the same environment. This is the relationship that lies at the heart of impact accounting (represented by the rectangle and the bottom of the diagram). Impact accounting is concerned with why and how this state change occurred, i.e., who did what that led to this change in state. Agents submit claims about, and corresponding proofs for, their contributions to these state changes.*

## **Generic formulation of impact accounting**

**Premise: An agent engages in an activity that impacts an environment.**

An **agent** deliberately engages in an **activity**.

The activity impacts one or more **environments** that are considered valuable. 

The impact of the activity is measured in terms of the changes that occurred in the **state(s)** of the environment(s) because of the activity.

Accounting is the presentation, verification and aggregation of **claims** about agents, the outcomes of their activities and the nature and magnitude of the **impact** that they had/ve on environments.

**Standards** prescribe the content and structure of such claims and allow third parties to assess the veracity of thereof.

## **The process of impact accounting**

**Someone or something gathers data**

- Observes a phenomenon using some instrument.

**Someone or something presents data as a claim**

- A claim concerns at least one property of an agent or activity or one paramater of a state and is accompanied by metadata (e.g., about the instrument, agent and sampling frame).
- A claim is made up of representations of the key aspects and dimensions of agents, activities and states as well as representations about the claim itselff.
- Some claims are proofs. A proof contains all the information needed to evaluate its veracity. Claims are often constructed from other claims.

**Someone or something evaluates the claim**

## Attachments:

![](images/icons/bullet_blue.gif) [image2022-2-1\_17-54-24.png](attachments/19008188/19008825.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-2-1\_17-56-40.png](attachments/19008188/19008826.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-4-12\_13-36-58.png](attachments/19008188/19009128.png) (image/png)  
![](images/icons/bullet_blue.gif) [OntologyRelations-1.png](attachments/19008188/19009129.png) (image/png)  
![](images/icons/bullet_blue.gif) [OntologyRelations-2.png](attachments/19008188/19009130.png) (image/png)  
![](images/icons/bullet_blue.gif) [OntologyRelations-3.png](attachments/19008188/19009131.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-4-12\_13-43-15.png](attachments/19008188/19009132.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-4-12\_13-43-52.png](attachments/19008188/19009133.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-4-12\_13-44-17.png](attachments/19008188/19009134.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-4-12\_13-44-39.png](attachments/19008188/19009135.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-4-12\_13-46-26.png](attachments/19008188/19009136.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-4-12\_13-47-52.png](attachments/19008188/19009138.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-6-2\_18-58-53.png](attachments/19008188/19009350.png) (image/png)

Document generated by Confluence on Nov 26, 2024 13:09

[Atlassian](http://www.atlassian.com/)
