1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [How-to articles](How-to-articles_22154631.html)

# Besu : Decouple a class with Dagger - DRAFT

Created by Justin Florentine, last modified on Aug 02, 2023

Incredibly raw notes follow:

- Coupling. What it is and why it's a problem in Besu.
  
  - [https://en.wikipedia.org/wiki/Coupling\_(computer\_programming)](https://en.wikipedia.org/wiki/Coupling_%28computer_programming%29)
  - [https://www.infoworld.com/article/3632143/how-coupling-impacts-software-quality.html](https://www.infoworld.com/article/3632143/how-coupling-impacts-software-quality.html)
- Examples found in the code.
  
  - Adding metrics somewhere. - [https://github.com/hyperledger/besu/pull/5315/files](https://github.com/hyperledger/besu/pull/5315/files)
    
    - A MetricsSystem requires user configuration, which is done when BesuCommand sets up the BesuControllerBuilder.  You can see in that PR, in order to provide a MetricsSystem to the class being instrumented, 10 other classes had to be modified to just pass the dependency on to where it was to be used (BonsaiWorldStateKeyValueStorage.java).
  - Adding caching somewhere.
    
    - Introducing caching somewhere can either be easy, or a nightmare. If the cache requires user configurable or user tunable parameters, we end up with the later. In this PR [https://github.com/hyperledger/besu/pull/2821/files](https://github.com/hyperledger/besu/pull/2821/files) , you see that because the cache was user-tunable via the -`Xevm-jumpdest-cache-weight-kb`  param, we now have a similar problem as above with the MetricsSystem, however this one is much worse (20+ intermediate classes) because the distance between the user-supplied configuration and where it is used is greater.
  - CachedMerkleTrie loader.
- Inversion of Control fixes this - [https://www.educative.io/answers/what-is-inversion-of-control](https://www.educative.io/answers/what-is-inversion-of-control)
  
  - Dagger is a compile time implementation of dependency injection to provide inversion of control. [https://medium.com/@amitkma/understanding-inversion-of-control-ioc-principle-163b1dc97454](https://medium.com/@amitkma/understanding-inversion-of-control-ioc-principle-163b1dc97454)
- Knock-on effects. What else does decoupling lead to, other than less coupling?
  
  - Isolatable interfaces. Interfaces into re-usable implementations emerge, allowing easier swapping of components.
  - Mocking and Testing. More subcomponents, allows developers to re-use mocked out object graphs for their tests, so they don't need to wire it all up and mock it all out every time.
  - Composability. Coarser grained functionality can emerge built on top of stabilized sub-components. Should increase re-use and reduce test coverage required.

Terminology To Use:

- Module - From Dagger. A class that knows how to provide an implementation of some reusable function that other parts of the code may need. Usually singleton scoped, but not required to be.
- Component - From Dagger.  A composition of multiple modules, what implements the "service locator" pattern.
- Plugin - From Besu. see the existing plugin framework.

Enough Theory, on to Practice.

- BonsaiWorldStateProvider depends on 3 classes which BesuComponent knows how to provide. We can hide this dependency via BesuComponent, if we can solve the circular dependency running through clique.
- Instead of using BesuComponent and unnecessarily expanding the dependency graph, create a subcomponent with just the things BonsaiWorldState cares about.  This should live in the gradle module that will use it, which already should have the appropriate compile dependencies. This way the modules and components for the code being reused is in the same place as the implementations.
  
  - Yes, this means Dagger as a concern will spread quite widely across the codebase.
  - You will likely need to create 2 modules to produce the subcomponent; one to produce it for the subsystem that implements it, and a higher level one which can create the subcomponent using configurations parsed at runtime.
    
    - So for instance there will be a BonsaiComponent which combines things the BonsaiSubsystem needs, each their own module, like CachedMerkleTrieLoader, MetricsSystem, PluginContext etc.
    - Then, there may be a "naive" module (BonsaiModule) that can produce that component which lives alongside the implementations, to be used for unit/integration tests local to that subsystem.
    - The second module is probably a BesuBonsaiModule that creates the subcomponent, using provided configuration from the Besu application runtime. This likely would be an extension of the naive one, so classes that use it to locate services need not be aware of the Besu variant, since the source of the configuration is an implementation detail.

Discussion Points

- Tipping point
  
  - Aren't we just trading lots of little dependencies for one big one that contains them all?
  - Yes, for now. At some point, a class and all its dependencies may be provided by dagger. Every time that mini-graph is completed, now Dagger can provide it in total to clients.
    
    - Example and diagram needed, this is vague, hard to parse, and super important.
- FAQs
  
  - How do i know what should and shouldn't be provided by a module?
    
    - If you don't mind coupling the things together, then go for it. Use your judgement on the semantics.
  - How do other things already being provided by Dagger get into my module so I can use them when constructing my thing?
    
    - Parameter types, and @Named when you need a particular one.
  - where should I find the canonical list of modules / is there a canonical list.
    
    - Sorta. If you start with Besu.java, you'll see DaggerBesuComponent.create() which is our bootstrap of the object graph for all things that Dagger knows about. The convention dagger uses is to create an implementation of your component with Dagger as a prefix. From there, look at BesuComponent and you'll see a list of modules which it is capable of using to construct and provide objects.
  - how to plumb just ‘part’ of the object constructor when only some of the paramters are dagger provided
    
    - Overload the existing public constructor, removing all parameters which are provided by dagger. Add a parameter of type BesuComponent, and call on that to get the parameters which can be provided, and pass them into the "legacy" constructor. Don't remove the old one, we'll need it later once Dagger can provide all the dependencies, then Dagger can provide that class itself, and no longer needs to have the BesuComponent passed in.

<!--THE END-->

- Page:
  
  [Decouple a class with Dagger - DRAFT](/wiki/spaces/BESU/pages/22156326/Decouple+a+class+with+Dagger+-+DRAFT)

Document generated by Confluence on Nov 26, 2024 13:01

[Atlassian](http://www.atlassian.com/)
