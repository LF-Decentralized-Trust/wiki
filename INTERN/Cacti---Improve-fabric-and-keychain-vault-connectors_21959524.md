1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2023 Projects](2023-Projects_21954865.html)

# Hyperledger Mentorship Program : Cacti - Improve fabric and keychain-vault connectors

Created by Jagpreet Singh Sasan, last modified by Min Yu on Apr 27, 2023

**Project Title****Status**

UNSELECTED

**Primary Focus**

CODING DOCUMENTATION  RESEARCH

# Description

The current fabric (packages/cactus-plugin-ledger-connector-fabric) and vault(packages/cactus-plugin-keychain-vault) connectors are not cli-friendly. By cli-friendly, I refer to their use via api-server connector (packages/cactus-cmd-api-server).  
To import and initialise fabric/vault connector over api-server, one can include them as

```
    docker run \
    --rm \
    --publish 3000:3000 \
    --publish 4000:4000 \
    --env AUTHORIZATION_PROTOCOL='NONE' \
    --env AUTHORIZATION_CONFIG_JSON='{}' \
    --env GRPC_TLS_ENABLED=false \
    cas \
      ./node_modules/.bin/cactusapi \
      --plugins='[{"packageName": "@hyperledger/cactus-plugin-ledger-connector-fabric", "type": "org.hyperledger.cactus.plugin_import_type.LOCAL", "action": "org.hyperledger.cactus.plugin_import_action.INSTALL",  "options": { "connectionProfile": {}, "instanceId": "some-unique-instance-id"}}]'
```

The problem with this sort of import is that,

In case of fabric connector: The `IPluginLedgerConnectorFabricOptions`  currently expects the user to pass in a lot of information and some of the information like the `pluginRegistry`  is very difficult to pass as a JSON stringified object. Also passing a huge `connectionProfile`  as a flatten JSON string is not a good practice (sometimes the network can be huge and this could lead to a 50 liner `docker run...`  command)

In case of vault connector: The `token`  passed via `IPluginKeychainVaultOptions`  should have an option so that the plugin can pickup the token during initialisation from environment variable.

# Additional Information

For additional information, one can check out the current usage of plugins within the [api-server docs](https://github.com/hyperledger/cacti/tree/main/packages/cactus-cmd-api-server)

## Milestones

(Each milestone is set to be achieved in 2 weeks time)

- Understand the current objective to be completed for fabric and vault connector
- Update vault connector to have an optional field which enables reading of root token via environment variable
- Run the vault connector for a production grade vault deployment (vault residing over a EC2 machine or as a kubernetes pod), and identify further gaps in the connector, if any
- Fix the gaps by introducing additional optional fields in the vault connector
- Update vault test cases and the example codes using vault connector
- Update fabric connector to have pluginRegistry as an optional field (if its optional, during its initialisation while fabric connector is getting started, the pluginRegistry keychainID to be printed in plugin initialization logs)
- Run the fabric connector for a production grade fabric network (setup via Bevel) and see for further gaps, if any
- Fix the gaps by introducing additional optional fields in the fabric connector
- Update the fabric connector to have an optional field which enables the reading of connectionProfile from environment variable, same for the sshConfig variable
- Update the test cases and sample examples to have these fields if required (the above changes should be done in such a manner that it doesn't disrupt the test cases &amp; example code by a lot)
- Create a single PR to the Cacti codebase to address all the above done changes
- Create the final presentation/demo to showcase the work done

# Learning Objectives

Through this, the mentee can learn production grade best practices along with the usage and creation of Hyperledger Cacti plugins and their interaction with the api-server

# Expected Outcome

The following outcomes are expected from this:

- Modification of fabric-connector by introducing optional fields to the constructor, to facilitate the above mentioned goals in a way, it has minimal to no impact on the example usecases/testcases
- Modification of the vault-connector by introducing optional fields to the constructor, to facilitate the above mentioned goals in a way, it has minimal to no impact on the example usecases/testcases

# Relation to Hyperledger

Hyperledger Cacti

# Mentee Skills

- Expertise in JS/TS coding
- Prior knowledge/hands-on experience related to Cacti and its connectors

# Future plans

This project will enable us to rework on the Fabric connector which provides the same current functionality with minimum user inputs, taking into consideration the production grade angle of the ledger environments.

# Mentor(s) Names and Contact Info

[Peter Somogyvari](https://lf-hyperledger.atlassian.net/wiki/people/557058:cae262a4-be99-4f5e-a36e-bf20a5c795f2?ref=confluence), Accenture, Discord ID: peter\_somogyvari#3365

[Sownak Roy](https://lf-hyperledger.atlassian.net/wiki/people/5f6defc406e342007131c946?ref=confluence) , Accenture, Discord ID: Sownak#7728

[Jagpreet Singh Sasan](https://lf-hyperledger.atlassian.net/wiki/people/5d319526fe0a0d0c857abe59?ref=confluence) ,  Accenture, Discord ID: axetacular#2402

Document generated by Confluence on Nov 26, 2024 14:55

[Atlassian](http://www.atlassian.com/)
