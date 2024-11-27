1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Requests for Comments](Requests-for-Comments_21016001.html)

# Hyperledger Iroha : WebAssembly FFI - module linking

Created by Former user (Deleted) on May 13, 2022

## 1. Rust memory layout in WebAssembly

![WebAssembly VM](attachments/21013280/21018042.png?height=250 "WebAssembly VM")

In short, the WebAssembly memory model consists of an execution stack, linear memory, function index space and an indirect function table. However, because of security considerations, wasm programs, unlike other languages, don’t have access to its execution stack. Thus, when compiling Rust to Wasm, a separate virtual stack (as opposed to the physical execution stack of the WebAssembly VM) is maintained in the linear memory. Why? - well because linear memory is addressable.

This results in a linear memory layout as follows:

![Linear memory of Rust program](attachments/21013280/21018043.jpg?height=150 "Linear memory of Rust program")

We can see that compiling Rust to WebAssembly creates a virtual stack in linear memory starting at *\_\_stack\_pointer* which is 1048576 == 1024 * 1024 = 1MB by default. Data section is most usually small and contains static data like embedded strings and maybe globals (I’m not sure where globals reside)

## 2. FFI opaque pointer

When the initial implementation of the wasm smart contract support was finished. It was noted that the smart contract when compiled to wasm was way too large to be stored on the blockchain. There was a lot of bloat, mostly related to serializing of the data structures. To reduce the binary size it was decided to replace all the expensive (in code size) method calls with FFI calls where external methods would be exported from a 2nd module which the given smart contract would link against dynamically. Additionally, data structures involved with crossing the FFI boundary would be hidden behind opaque pointers whose internal structure would not be known to the smart contract.

    To be able to make the FFI work, the modules need to share their address space, i.e. they need to operate on a single instance of shared linear memory. In Wasm it is possible to export/import linear memory, but when this is done with Rust programs compiled to Wasm, their runtimes step over each other as they utilize the linear memory oblivious to the fact that there is another module that they are working with. This results in memory corruption. There are a few ways to make this work:

### 2.1. WebAssembly module linking proposal

Wasmtime implemented the module linking proposal only to have it [removed](https://github.com/bytecodealliance/wasmtime/issues/3941) in the 0.36 version (last version). They will be working on a new implementation through the WebAssembly component model proposal but ETA of this feature is not known to me. We could rely on the 0.35.3 version (last version to include module linking) of Wasmtime until module linking proposal is reimplemented. **Note that module linking proposal is not stabilized yet**

### 2.2. Shared linear memory with two virtual stacks

It’s possible to link two modules without them knowing about each other by modifying the stack size of one of the modules. Let’s take a look at a diagram of what memory layout would look like in this scenario:

![Linear memory shared by two Rust programs](attachments/21013280/21018044.jpg?height=143 "Linear memory shared by two Rust programs")

First let’s assume that the *\_\_stack\_pointer* is at 1MB position for the 1st module, and at 2MB position for the 2nd module. From the diagram presented it looks like *heap1* and *stack2* would step over each other which would result in corrupted memory. This would not happen if *heap1* was somehow not used in which case *stack2* would have all the space in between *\_\_heap\_base1* and *\_\_stack\_pointer2* for itself. This can be achieved in two ways. First, trivial way, would be to forbid all allocation requests for the *module1*. Second, more interesting approach, would be to replace all of the *heap1* *alloc/dealloc* requests with FFI calls to the *module2* allocator effectively having just one allocator handling all the allocation requests from both modules and operating on the *heap2* space. However, it should be mentioned that if stack overflow of the *module2* occurs then instead of hard immediate error, a memory corruption would occur (this is the reason why linker developers moved the virtual stack to the start of the linear memory growing down). If it were possible to share a mutable global *\_\_stack\_pointer* between modules we could have just one stack, which I don’t think can be done at the time of writing this doc. **Note that this approach assumes the memory layout is exactly as the aforementioned and would require defining stack sizes when building the smart contract**. The memory layout seems to be the same in other compiled languages as is for Rust with the current default stack size of 1MB for Rust and 5MB for C++.

### 2.3 Host bridge with independent memory spaces

If one finds the previous approach too hacky or to have a lot of implicit gotchas then let’s have each module have its own memory and use the host to bridge the gap in FFI calls. The reason why the 2nd module is necessary in all of the given approaches is to prevent OOM attacks. If FFI functions were defined on the host a malicious smart contract could keep allocating memory until the Iroha node crashes. Therefore, it is better to not let outside code allocate memory on the host and have a 2nd module where allocations would reside sandboxed.

FFI calls can work when memory is not shared if there is an intermediary, i.e. the host, which translates the input/output arguments into the corresponding module’s memory space. The details of the translation protocol will remain unspecified unless this approach is decided to become favored.

## 3. Comments

1. 2.1 should be the preferred solution in the long run. In the meantime 2.2 seems good enough (POC seems to work) unless there are some caveats that will surface out. If not 2.3 is also a valid approach though it seems it would be a bit more involved.
2. I didn’t write about the indirect function table because I don’t think that it’s necessary to share the table between modules. If there were function pointers (e.g. callbacks) crossing the FFI boundary then sharing the indirect function table would be a requirement. However, all we’re sharing at the moment is just the data and the functions to either construct or inspect the data and I don’t think this will change. If this is not the case then 2.2 approach will not work

## Attachments:

![](images/icons/bullet_blue.gif) [wasm\_memory\_model.png](attachments/21013280/21018042.png) (image/png)  
![](images/icons/bullet_blue.gif) [rust\_wasm\_memory\_layout.jpg](attachments/21013280/21018043.jpg) (image/jpeg)  
![](images/icons/bullet_blue.gif) [rust\_wasm\_memory\_layout2.jpg](attachments/21013280/21018044.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
