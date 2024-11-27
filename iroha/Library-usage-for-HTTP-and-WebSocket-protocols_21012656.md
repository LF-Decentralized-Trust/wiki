1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Library usage for HTTP and WebSocket protocols

Created by Egor Ivkov, last modified on Aug 24, 2020

Status

DECIDED

Stakeholders

[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) [Vadim Reutskiy](https://lf-hyperledger.atlassian.net/wiki/people/5b8d04b72786fb2bf79a7405?ref=confluence) [Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence)

OutcomeCustom web server library will be implemented with the use of the 3 suggested helper librariesDue date

24 Aug 2020

Owner

[Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) 

## Background

From the start of the development of Iroha 2, we tried to limit the number of dependencies in order to ensure higher security. With the acceptance of [Maintenance Endpoint](Maintenance-Endpoint_21012343.html) RFC, the work on the implementation of HTTP and Web Socket API has been started. Taking into account the size of the team and the time constraints it seems reasonable to use already existing libraries for both of the selected protocols (HTTP, WebSocket), and therefore add these dependencies to Iroha 2. This RFC discusses the possibility of introducing these dependencies and the selection of these libraries if they are decided to be added.

## Action items

- [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence)implement the maintenance endpoint with the selected libraries

# Problem

Should we use external libraries for the HTTP and Web Socket protocols or provide our own implementation of them? If we use external libraries, then which ones?

# Solution

## Decisions

It is suggested to use external libraries for both of these protocols. The pros and cons of this decision are shown below

ProsCons

1. Saves development time and it is important because:
   
   1. The team is rather small and with the use of libraries will be able to focus more on Iroha specific tasks
   2. The deadline for the MVP is soon
2. Both protocols are heavily standardized and libraries have to follow these standards, making their behaviour predictable and secure

<!--THE END-->

1. Addition of many external dependencies introduces potential security holes of which our team is not aware

### Requirements for Libraries

These are the high-level requirements that seem reasonable to propose for libraries that we will use:

1. Async I/O - as Iroha2 is heavily async and relies on executors for low-level thread management.
2. A relatively small number of new dependencies - as new dependencies introduce potential security risks.
3. Library rather than framework - as Iroha2 has already a rather specific structure and should not change its style to fit the framework.
4. It should be possible to upgrade HTTP connection from HTTP library with WebSocket
5. Free open license
6. HTTP 1.1 support - as Substrate offchain workers do not support HTTP 2

### Proposed Libraries

The proposed libraries are the following:

ProtocolLibrary**Description**HTTP[httparse](https://crates.io/crates/httparse)A push parser for the HTTP 1.x protocol. Avoids allocations. No copy. **Fast.**  
[route-recognizer](https://crates.io/crates/route-recognizer)Recognizes URL patterns with support for dynamic and glob segments. *Can be easily replaced with our custom solution later. Used to speed up the development process. Also doesn't have any dependencies.*Web Socket[async-tungstenite](https://crates.io/crates/async-tungstenite)Asynchronous WebSockets for [async-std](https://async.rs), [tokio](https://tokio.rs), [gio](https://gtk-rs.org) and any `std` `Future`s runtime. Based on [tungstenite](https://crates.io/crates/tungstenite) crate.

The usage of these libraries would, in general, mean that we will implement our own web server based on TCP streams, but the messages will be parsed with the help of HTTP library. When the upgrade request for web socket will be received, then the connection manager will be passed to async-tungstenite library.

## Alternatives

AlternativeDescriptionWhy not chosen[tiny\_http](https://crates.io/crates/tiny_http) as HTTP server libraryLow-level HTTP server libraryNo async support[http](https://crates.io/crates/http) as HTTP type helper libraryA general-purpose library of common HTTP types.Does not support parsing from streams or raw bytes, which is a functionality that we might spend a lot of time writing if it is not supported out of the box.[async\_h1](https://crates.io/crates/async-h1) as HTTP server libraryAsynchronous HTTP/1.1 parser.Does not support WebSocket upgrade.[hyper](https://crates.io/crates/hyper) as HTTP server libraryA **fast** and **correct** HTTP implementation for Rust. Actually the fastest HTTP server library according to [techempower](https://www.techempower.com/benchmarks/#section=data-r18&hw=ph&test=plaintext).

1. Has many dependencies and one of them is tokio which is not optional.
2. No information on whether it will work with async-std as it is built with the use of tokio.
3. Not possible to upgrade the HTTP connection with web socket.

[h2](https://crates.io/crates/h2) as HTTP server libraryA Tokio aware, HTTP/2.0 client &amp; server implementation for Rust.

1. It is not possible to use http 2.0 currently - see requirements.
2. Depends on tokio - same concerns as with hyper.

[http-service](https://crates.io/crates/http-service) as HTTP server interface libraryThe crate `http-service` provides the necessary types and traits to implement your own HTTP Server.The crate mainly provides the interface for the servers to implement the same methods, it might be good for architecture in general, but it is an additional dependency and our priority is to only add absolutely necessary ones.[tide](https://crates.io/crates/tide) as http serverA modular web framework built around async/await.

1. It is a framework, though less opinionated as others, it still imposes some limitations
2. No WebSocket protocol upgrade is supported at the [moment](https://github.com/http-rs/tide/issues/67). But this feature seems to be [under development](https://blog.yoshuawuyts.com/tide-channels/).

In general it might have been a good choice if they had finished web socket support by now.

[actix](https://crates.io/crates/actix-web) / [warp](https://crates.io/crates/warp) / [rocket](https://crates.io/crates/rocket) as web frameworkPopular web frameworks with both warp and rocket being built on the hyper library,

1. They are Web Frameworks and it is preferable to use a library.
2. They have many dependencies, where most of them are not needed for our purposes.

Custom http and web socket librariesIt is possible to implement a fully custom solution.

There are already existing solutions which correctly implement the standards and are widely used.

The team will be able to focus on our unique functionality.

## Concerns

The chosen solution might take more time to implement but at the same time, it gives us flexibility and minimal increase in dependencies.

## Assumptions

WebSocket feature is essential to us and we should support it out of the box.

## Risks

There are potential risks in adding new dependencies which might have security-related flaws.

# Additional Information

Grin developers community had a [discussion](https://github.com/mimblewimble/grin/issues/2040) on this topic which might be worth reading. Grin is a Rust implementation of [Mimblewimble blockchain format and protoco](https://github.com/mimblewimble/grin/blob/master/doc/intro.md)l.

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
