1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2022 Projects](2022-Projects_21954800.html)

# Hyperledger Mentorship Program : Chia Connector for Hyperledger Cactus

Created by Peter Somogyvari, last modified by Min Yu on Jun 07, 2022

**Project Title**Chia Connector for Hyperledger Cactus**Status**

IN PROGRESS

**Difficulty**

HIGH

# Description

Develop a Cactus Chia connector plugin + test infrastructure (container images, container manager class, etc.) from scratch.  
Include end to end test cases powered by Jest and the said testing infrastructure that prove that the connector is working as intended with a locally simulated Chia network.

You will be creating a new package in the Cactus monorepo from scratch under the `packages/cactus-plugin-ledger-connector-chia/` path.

All the information presented here can also be found at the GitHub issue tracker of Hyperledger Cactus, filed under issue #1634 =&gt; [github.com/hyperledger/cactus/issues/1634](http://github.com/hyperledger/cactus/issues/1634)

# Additional Information

### Links, Tips, Useful Information

> Most important tip: You should study the code of other - already working - connector plugins to see how they implement web services for example. A lot of the code is just boilerplate around the actual logic that translates Cactus API requests into RPC calls to the Chia ledger.

1 .There is a Typescript library facilitating RPC calls to Chia chains: [https://www.npmjs.com/package/chia-js](https://www.npmjs.com/package/chia-js) The latter should be used for the internal workings of the connector class to keep things simple (e.g. do not go down the rabbit hole of trying to use bindings from another language via IPC or other complex workarounds).  
2\. Start with the connector plugin package's implementation by simply copy pasting one of the existing connectors and then find &amp; replace the ledger name within that folder accordingly ($COPIED\_LEDGER\_NAME =&gt; `chia`)  
3\. Double check that in `packages/cactus-plugin-ledger-connector-chia/package.json` the dependency versions to other Cactus packages are up to date and that the name of the package itself is also up to date.

# Learning Objectives

1. Learn how an open-source project works in general
   
   1. How pull request reviews are done
   2. Acquire basic git know-how about managing branches, rebasing onto the upstream's main branch
   3. Responding to reviews/questions/change requests from maintainers and/or other community members
2. Learn to present the work/results that's been accomplished
3. Become proficient in NodeJS/Typescript
4. Understand how large scale open source projects are managed (monorepo, automated CI+testing infrastructure)
5. Learn how the Chia Network DLT works both conceptually and in practice.
6. Learn about the Hyperledger Cactus plugin architecture

# Expected Outcome

### Acceptance Criteria

1. Chia All-In-One image is created (`tools/docker/chia-all-in-one/Dockerfile`) which also has a [README.md](http://README.md) next to it explaining the building and running of the image and it's containers (`tools/docker/chia-all-in-one/README.md`)
   
   1.1 Container health checks must be be operational and reliable for the image meaning that the `HEALTHCHECK` keyword needs to be used within the `Dockerfile` to define when the container has finished launching (e.g. it must only pass once the ledger is up and running, ready to accept transactions)
2. The AIO image mentioned above is published to the official GitHub Container Registry under the fully qualified image tag of `ghcr.io/hyperledger/cactus-chia-all-in-one:2022-MM-DD-$GIT_SHORT_HASH` for example `ghcr.io/hyperledger/cactus-chia-all-in-one:2021-01-08-7a055c3` (do not use the exact example tag of course)
3. A `packages/cactus-test-tooling/src/main/typescript/chia/chia-test-ledger.ts` code file is added with a `ChiaTestLedger` class in it that is responsible for providing a `start()` method that takes care of launching
4. A `packages/cactus-plugin-ledger-connector-chia/src/main/typescript/plugin-ledger-connector-chia.ts` file is added with a `PluginLedgerConnectorChia` class in it. This class uses the `chia-js` npm package under the hood to implement the connector's usual methods.
5. The functionality of the connector is covered by the end to end tests mentioned earlier. The tests must be using the AIO image to simulate a production Chia ledger with reasonable accuracy.
6. Web services are implemented so that the connector's functionality can be exposed via the network when the plugin is loaded into the Cactus API server.
7. Tests are also covering (e.g. using) the generated API client class (for which you'll need to define the necessary request and response types and endpoints in a file at `packages/cactus-plugin-ledger-connector-chia/src/main/json/openapi.json` file.

# Relation to Hyperledger

Hyperledger Cactus

# Education Level

Any computer science/self taught programming background is great regardless of the highest level of achieved education.

# Skills

1. Git
2. Docker / containerization
3. NodeJS
4. Typescript
5. HTTP/REST/ExpressJS
6. Swagger/OpenAPI Specification
7. VSCode
8. GitHub
9. Computer Science 101

# Future plans

The Chia connector plugin could be used in a number of projects that end up leveraging Cactus itself.

# Preferred Hours and Length of Internship

No preference. With the right attitude and willingness to learn &amp; problem solve, the intern should be able to get it done regardless of the intensity of the work being carried out.

# Mentor(s) Names and Contact Info

Name: **Peter Somogyvari**

Company affiliation: **Accenture**

Chat ID (Discord): **peter\_somogyvari#3365**

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
