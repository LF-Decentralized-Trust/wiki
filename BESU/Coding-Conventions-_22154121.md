1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Content Refactor](Content-Refactor_22153881.html)
4. [Developing](Developing_22154116.html)

# Besu : Coding Conventions-

Created by Byron Gravenorst, last modified by Felipe Faraggi on Jan 24, 2020

# Introduction

This document contains guidelines (some stricter than others) so we can be consistent and spend more time solving the bigger and more interesting issues.

The guidelines are intended to facilitate working together not to facilitate reviews that criticize without adding value.

Some guidelines are personal opinion. The idea being we make a decision once, document it, and apply it for consistency. Again, we can then spend more time on the interesting issues and less time discussing coding conventions :-)

# General Design Philosophy

The key principles are:

- Keep It Simple
- Idiomatic Java
- YAGNI (You Ain't Gonna Need It)

## Keep It Simple

- Simple does not mean the fewest lines of code. Simple code is:
- Easy to understand
- Self-documenting and not dependent on comments to explain what it does
- Understandable even to inexperienced Java developers
- Dependent on selecting the right data structures for the task
- Usually the most performant. Without data showing another approach is faster, stick with the simple design
- Not simplistic:
  
  - Ethereum is complex and Besu must handle this complexity and operate correctly and securely
  - Besu code should align with well-established Ethereum abstractions and terminology used in Ethereum specifications
  - Aim to make the code as simple as possible but no simpler

## Idiomatic Java

Besu embraces typical Java idioms including using an Object Oriented approach to design. This includes:

- Providing alternate behaviours via polymorphism instead of having conditional logic scattered through the codebase. For example, ProtocolSpec provides a standard interface to blockchain operations and multiple implementations define the different behaviours for each Ethereum milestone.
- Encapsulating behaviour and data together in classes. For example, BytesValue encapsulates byte data and methods operating on the byte data. BytesValue.isZero() is an instance method instead of accepting a BytesValue parameter.
- ProtocolSpec is an exception and does not hold the blockchain data on which it operates. This is because that blockchain data is widely shared and not specifically owned by ProtocolSpec.
- Embracing modern Java features like Optional, Streams and lambdas when they make code simpler and clearer.
  
  - Do use Streams and map with lambdas to convert values in a list to a different form.
  - Don't pass lambdas into executors because it makes it harder to identify the threading interactions. The lambda makes the code shorter but not clearer. Instead use a separate class or extract a method.
- For good examples, refer to the APIs the JDK itself exposes.

**Note**: If you're not sure what idiomatic Java looks like, start by following the typical patterns and naming used in Besu.

## You Ain't Gonna Need It (YAGNI)

The Besu design prioritizes meeting current requirements in the simplest, clearest way over attempting to anticipate future functionality. As a result, Besu’s design:

- Is not set in stone as a big upfront design. The design is adjusted through constant refactoring as new requirements are added and understood.
- Uses abstraction only where it aids understanding of the current code. Abstraction is not used where it only supports future needs.
- Avoids over-engineering.

# Specific Design Techniques

## Creating Understandable, Self-documenting Code

To create understandable, self-documenting code:

- Use clear naming for variables, methods, and classes
- Use US spelling instead of UK. For example, synchronize instead of synchronise
- Keep methods and classes short and focused on a single responsibility. Preferable maximum lengths:
  
  - Lambdas: 1 - 3 lines
  - Methods: less than 50 lines
  - Anonymous classes: less than 50 lines
  - Inner classes: not much more than 50 lines
  - Classes: a few hundred lines
- Be thoughtfully organised in terms of method order, package structure, and module usage
- Follow well-established patterns and conventions
- Be consistent
- Make it easy to follow the control flow by clicking through in an IDE
- Make it easier to use the right way than the wrong way
- Avoid abbreviations. We are a global team and when English is a second language abbreviations reduce readability. The following abbreviations are exceptions:
  
  - tx -&gt; Transaction
  - IBFT -&gt; Istanbul Byzantine Fault Tolerant (a consensus protocol)
  - EVM -&gt; Ethereum Virtual Machine
  - P2P -&gt; Peer to Peer
  - RPC -&gt; Remote Procedure Call

## Creating Code for Constant Refactoring and Evolving Design

So the code can cope with constant refactoring and evolving design, write code that:

- Is well tested. Avoid test cases requiring detailed interactions with mocks because these are often brittle.
- Avoids duplication.
- Follows the Single Responsibility Principle where each class is responsible for one thing. It is important to scope the responsibility wisely. Responsibilities that are:
  
  - Too small lead to an explosion of classes making things hard to follow
  - Too large lead to the class becoming big and unwieldy
- Favors composition over inheritance. You can use inheritance, but prefer composition
- Uses dependency injection
  
  - Constructors should be simple, with dependencies passed in rather than built in the constructor
  - Besu does not use a dependency injection framework
- Validates method parameters for public methods using the Guava Preconditions class. Avoid validating parameters in private methods
- Generally avoids interfaces with a single implementation unless they are explicitly being used to narrow the exposed API
- Uses the most general applicable type. For example, `List` or `Collection` instead of `ArrayList`

## Additional Design Elements

- Use Optional rather than returning null when not having a value is a normal case
- Consider exception and error handling as part of the overall design. Besu avoids checked exceptions
- Give threads meaningful names. For example: `Executors.newFixedThreadPool(1, new ThreadFactoryBuilder().setNameFormat(“Ibft”).build())`

# Java

## Style Guide

Besu follows the Google code style and uses spotless to ensure consistency of formatting.

To automatically reformat the code before creating a pull request, run:

```
./gradlew spotlessApply
```

### Install Google Style Settings

The Google style settings can be installed in Intellij and Eclipse.

## Additional Java Style Guidelines

### Fields

Class-level fields are generally not separated by blank lines but can use a blank line to separate them into logical groupings.

### Final Keyword

Method parameters must be final. Class level and local fields should be final whenever possible.

### Common Methods

- Getters follow idiomatic format with `get` prefix. For example, `getBlock()` gets a block property.
- Setters follow idiomatic format with `set` prefix. For example, `setBlock(Block block)` sets a block property.
- The Setter pattern should not be used for chained builder methods.
- Methods returning a `Stream` should be prefixed with `stream`. For example `streamIdlePeers()` returns a stream of the idle peers.
- For `toString` methods use the Guava 18+ `MoreObjects.toStringHelper`
- Equals and `hashCode()` methods use the `Object.equals` and `Object.hash` methods (this is the Java 7+ template in IntelliJ. Don’t accept subclasses and don’t use getters)

### Testing

- Don't use a fixed prefix (for example, `test`). Do explain the expected behaviour not just the situation

Good: `returnTrueWhenValueIsXyz()`

Bad: `valueIsXyz()`

- Use AssertJ for assertions in preference to JUnit’s Assert class.

To help future-proof the code (avoiding libraries that may be deprecated in the near future), avoid assertions from the `org.assertj.core.api.Java6Assertions` class. Java6 in the name is a concerning signal

### 4.2.5 Miscellaneous

- When creating loggers it should be the first declaration in the class with:

`private static final Logger LOG = getLogger();`

- Ternary operators are acceptable when they make the code clearer but should never be nested
- Avoid TODO comments. Log a ticket instead
- Specify Gradle dependency versions in `versions.gradle`
- Don't use two or more blank lines in a row

# Logging

Logging is important for understanding what Besu is doing at any given time (for example, progress while synchronizing) and investigating defects. During development, add logging to aid in these cases.

## Log Messages

Make log messages:

- Not so frequent they are overwhelming in the log output
- At the appropriate level
- Detailed enough to understand what actually happened. For example:

`Insufficient validators. Expected 10 but found 4`

- As succinct as possible while still being clear.

Bad: `Insufficient validators. Expected 10 but got: [address, address, address, address, address, address]`

## Log Levels

- *Trace* - Extremely detailed view showing the execution flow. Likely only useful to developers
- *Debug* - Information that is diagnostically helpful to a wider group than just developers (for example, sysadmins)
- *Info* - Generally useful information to log (for example, service start/stop, configuration assumptions). Default logging level
- *Warn* - Anything that can potentially cause application oddities but from which Besu automatically recovers
- *Error* - Any error which is fatal to the operation, but not Besu itself (for example, missing data)
- *Fatal* - An error that forces a shutdown of Besu

Document generated by Confluence on Nov 26, 2024 13:01

[Atlassian](http://www.atlassian.com/)
