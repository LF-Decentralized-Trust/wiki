1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Developing and Conventions](Developing-and-Conventions_22153909.html)
4. [Plugin Services](Plugin-Services_22155059.html)

# Besu : PrivacyPluginService

Created by Antony Denyer on Oct 11, 2021

```
public interface PrivacyPluginService
extends BesuService
```

A service that plugins can use to define how private transactions should be handled.

You must register a [`PrivacyPluginPayloadProvider`](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivacyPluginPayloadProvider.html "interface in org.hyperledger.besu.plugin.services.privacy") when using this plugin and can optionally register a [`PrivateMarkerTransactionFactory`](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivateMarkerTransactionFactory.html "interface in org.hyperledger.besu.plugin.services.privacy") and a [`PrivacyGroupGenesisProvider`](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivacyGroupGenesisProvider.html "interface in org.hyperledger.besu.plugin.services.privacy")

## Method Summar

Modifier and TypeMethodDescription`PrivacyPluginPayloadProvider``getPayloadProvider()`  
`PrivacyGroupAuthProvider``getPrivacyGroupAuthProvider()`  
`PrivacyGroupGenesisProvider``getPrivacyGroupGenesisProvider()`  
`PrivateMarkerTransactionFactory``getPrivateMarkerTransactionFactory()`  
`void``setPayloadProvider​(PrivacyPluginPayloadProvider privacyPluginPayloadProvider)`

Register a provider to use when handling privacy marker transactions.

`void``setPrivacyGroupAuthProvider​(PrivacyGroupAuthProvider privacyGroupAuthProvider)`

Register a provider to use when auth requests for a multi-tenant environment.

`void``setPrivacyGroupGenesisProvider​(PrivacyGroupGenesisProvider privacyGroupAuthProvider)`

Register a provider for initialising private state genesis

`void``setPrivateMarkerTransactionFactory​(PrivateMarkerTransactionFactory privateMarkerTransactionFactory)`

Register a factory to specify your own method for signing and serializing privacy marker transactions.

## Method Details

- ### [setPayloadProvider]()
  
  void setPayloadProvider​([PrivacyPluginPayloadProvider](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivacyPluginPayloadProvider.html "interface in org.hyperledger.besu.plugin.services.privacy") privacyPluginPayloadProvider)
  
  Register a provider to use when handling privacy marker transactions.
  
  Parameters: privacyPluginPayloadProvider - the provider to use for the privacy marker payload
- ### [getPayloadProvider]()
  
  [PrivacyPluginPayloadProvider](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivacyPluginPayloadProvider.html "interface in org.hyperledger.besu.plugin.services.privacy") getPayloadProvider()
- ### [setPrivateMarkerTransactionFactory]()
  
  void setPrivateMarkerTransactionFactory​([PrivateMarkerTransactionFactory](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivateMarkerTransactionFactory.html "interface in org.hyperledger.besu.plugin.services.privacy") privateMarkerTransactionFactory)
  
  Register a factory to specify your own method for signing and serializing privacy marker transactions.
  
  Parameters: privateMarkerTransactionFactory - the factory to use to build the privacy marker transaction
- ### [getPrivateMarkerTransactionFactory]()
  
  [PrivateMarkerTransactionFactory](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivateMarkerTransactionFactory.html "interface in org.hyperledger.besu.plugin.services.privacy") getPrivateMarkerTransactionFactory()
- ### [setPrivacyGroupAuthProvider]()
  
  void setPrivacyGroupAuthProvider​([PrivacyGroupAuthProvider](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivacyGroupAuthProvider.html "interface in org.hyperledger.besu.plugin.services.privacy") privacyGroupAuthProvider)
  
  Register a provider to use when auth requests for a multi-tenant environment. If you are not using a multi-tenant environment you always return true.
  
  Parameters: privacyGroupAuthProvider - the provider to use to determine authz
- ### [getPrivacyGroupAuthProvider]()
  
  [PrivacyGroupAuthProvider](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivacyGroupAuthProvider.html "interface in org.hyperledger.besu.plugin.services.privacy") getPrivacyGroupAuthProvider()
- ### [setPrivacyGroupGenesisProvider]()
  
  void setPrivacyGroupGenesisProvider​([PrivacyGroupGenesisProvider](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivacyGroupGenesisProvider.html "interface in org.hyperledger.besu.plugin.services.privacy") privacyGroupAuthProvider)
  
  Register a provider for initialising private state genesis
  
  Parameters: privacyGroupAuthProvider - the provider for the initial private state
- ### [getPrivacyGroupGenesisProvider]()
  
  [PrivacyGroupGenesisProvider](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/privacy/PrivacyGroupGenesisProvider.html "interface in org.hyperledger.besu.plugin.services.privacy") getPrivacyGroupGenesisProvider()

Document generated by Confluence on Nov 26, 2024 12:58

[Atlassian](http://www.atlassian.com/)
