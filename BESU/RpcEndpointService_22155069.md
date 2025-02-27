1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Developing and Conventions](Developing-and-Conventions_22153909.html)
4. [Plugin Services](Plugin-Services_22155059.html)

# Besu : RpcEndpointService

Created by Antony Denyer on Oct 11, 2021

```
public interface RpcEndpointService
extends BesuService
```

This service allows you to add functions exposed via RPC endpoints.

This service will be available during the registration callback and must be used during the registration callback. RPC endpoints are configured prior to the start callback and all endpoints connected. No endpoint will actually be called prior to the start callback so initialization unrelated to the callback registration can also be done at that time.

## Method Summary

Modifier and TypeMethodDescription`<T> void``registerRPCEndpoint​(java.lang.String namespace, java.lang.String functionName, java.util.function.Function<PluginRpcRequest,​T> function)`

Register a function as an RPC endpoint exposed via JSON-RPC.

## Method Details

- ### [registerRPCEndpoint]()
  
  &lt;T&gt; void registerRPCEndpoint​(java.lang.String namespace, java.lang.String functionName, java.util.function.Function&lt;[PluginRpcRequest](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/rpc/PluginRpcRequest.html "interface in org.hyperledger.besu.plugin.services.rpc"),​T&gt; function) Register a function as an RPC endpoint exposed via JSON-RPC.
  
  The mechanism is a Java function that takes a list of Strings and returns any Java object, registered in a specific namespace with a function name.
  
  The resulting endpoint is the `namespace` and the `functionName` concatenated with an underscore to create the JSON-RPC method name.
  
  The function takes a [`PluginRpcRequest`](http://localhost:63342/besu/besu.plugin-api/build/docs/javadoc/org/hyperledger/besu/plugin/services/rpc/PluginRpcRequest.html "interface in org.hyperledger.besu.plugin.services.rpc") which contains a list of the inputs expressed entirely as strings. Javascript numbers are converted to strings via their toString method, and complex input objects are not supported.
  
  The output is a Java object, primitive, or array that will be inspected via [Jackson databind](https://github.com/FasterXML/jackson-databind). In general if JavaBeans naming patterns are followed those names will be reflected in the returned JSON object. If the method throws an exception the return is an error with an INTERNAL\_ERROR treatment.
  
  Type Parameters: T - specified type of return object Parameters: namespace - The namespace of the method, must be alphanumeric. functionName - The name of the function, must be alphanumeric. function - The function itself.

Document generated by Confluence on Nov 26, 2024 12:58

[Atlassian](http://www.atlassian.com/)
