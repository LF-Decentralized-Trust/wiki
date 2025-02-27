1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Developing and Conventions](Developing-and-Conventions_22153909.html)

# Besu : Plugin Services

Created by Antony Denyer, last modified on Oct 11, 2021

Since the deprecation of bintray and jcenter javadocs are no longer being consumed by [https://javadoc.io/doc/org.hyperledger.besu/plugin-api/latest/index.html](https://javadoc.io/doc/org.hyperledger.besu/plugin-api/latest/index.html)

This is a temporary measure until we start hosting our own javadocs

A manual snapshot was taken on 11 Oct 2021

# Package org.hyperledger.besu.plugin.services

Interface Summary

InterfaceDescriptionBesuConfiguration

Generally useful configuration provided by Besu.

BesuEvents

This service allows plugins to attach to various events during the normal operation of Besu.

BesuEvents.BlockAddedListener

The listener interface for receiving new block added events.

BesuEvents.BlockPropagatedListener

The listener interface for receiving new block propagated events.

BesuEvents.BlockReorgListener

The listener interface for receiving new block reorg events.

BesuEvents.LogListener

The listener interface for receiving log events.

BesuEvents.SyncStatusListener

The listener interface for receiving sync status events.

BesuEvents.TransactionAddedListener

The listener interface for receiving new transaction added events.

BesuEvents.TransactionDroppedListener

The listener interface for receiving transaction dropped events.

BesuService

All services that can be resolved via [`BesuContext.getService(Class)`](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/BesuContext.html#getService%28java.lang.Class%29) must implement [`BesuService`](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/BesuService.html "interface in org.hyperledger.besu.plugin.services")

MetricsSystem

An interface for creating various Metrics components.

[PermissioningService](PermissioningService_22155064.html)

This service allows plugins to decide who you should connect to and what you should send them.

PicoCLIOptions

A service that plugins can use to add CLI options and commands to the BesuCommand.

PluginVersionsProvider  
[PrivacyPluginService](PrivacyPluginService_22155066.html)

A service that plugins can use to define how private transactions should be handled.

[RpcEndpointService](RpcEndpointService_22155069.html)

This service allows you to add functions exposed via RPC endpoints.

SecurityModuleService

This service allows plugins to register a Security Module, which is abstraction of cryptographic operations that defer to specific provider (e.g.

StorageService

This service allows plugins to register as an available storage engine.

Document generated by Confluence on Nov 26, 2024 12:58

[Atlassian](http://www.atlassian.com/)
