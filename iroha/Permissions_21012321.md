1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Permissions

Created by Nikita Puzankov, last modified by Egor Ivkov on Nov 27, 2020

Status

ACCEPTED

Stakeholders

[武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence)

Outcome

Error rendering macro 'jira' : null

Due date

04 Dec 2020

Owner

[Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence)

## Background

Iroha Special Instructions and Iroha Queries processing requires a permissions based security model.

Whitepaper and Iroha v1 documentation were researched.

## Problem

[The White Paper](https://github.com/hyperledger/iroha/blob/iroha2-dev/docs/source/iroha_2_whitepaper.md#211-data-permissions) requires protection of data from unauthorized read and write access.

[Iroha 1 documentation](https://iroha.readthedocs.io/en/master/concepts_architecture/glossary.html#permission) gives a Permission's definition:

> A named rule that gives the privilege to perform a command. Permission **cannot** be granted to an account directly, instead, account has roles, which are collections of permissions. Although, there is an exception, see Grantable Permission.

and Grant-able Permission:

> Only grantable permission is given to an account directly. An account that holds grantable permission is allowed to perform some particular action on behalf of another account. For example, if account a@domain1 gives the account b@domain2 a permission that it can transfer assets — then b@domain2 can transfer assets of a@domain1 to anyone.

As you can see permissions were a first-level entities in Iroha 1 and had a strict hardcoded verification logic. Iroha1 was mainly planned to be used as a private blockchain and this system would work there. Yet Iroha2 is planned to be used in both private and public blockchains and therefore needs some degree of customization on how permissions are checked to implement some more complex cases.

## Solution

As the Iroha project progresses towards being able to be used in different types of blockchains. It would be good to give more powers to developers. Therefore this RFC introduces a minimal Permission framework, which let's the developers of each blockchain have the power to set up their permission checks accordingly. Of course there will be an out of box implementations provided which can be used for simple blockchains, for more complex logic the developers will be able to define their completely own Permission checks implementation that would suit their needs.

### TL;DR

- Introduce Permission Checker trait
- Make Iroha generic over \`PermissionChecker\` and \`Permission\` types
- Implement out of box \`IrohaPermissionChecker\` with minimal checks and the ability to tweak it through the \`IrohaPermissionCheckerBuilder\`

### Code Example

```rust

trait PermissionChecker<Permission> {
    pub fn check_permissions(instruction: ISI, authority: Id) -> Result<(), String>
}

Register<Permission, Account>: ISI

#[derive(Encode, Decode, Serialize, Deserialize)]
struct Account<Permission> {
    permissions: Vec<Permission>,
    account_data: 
    // .. other fields
}

struct Iroha<Permission, PC: PermissionChecker<Permission>> {
    pub checker: PC,
    // .. other fields
}

Iroha<Iroha1Permission, Iroha1PermissionChecker>

enum Iroha1Permission {

}
```

### Pros

1. Customizable permissions check logic
2. Customizable permission type
3. Permission check logic is written in pure rust - which is a turing complete and convenient language while ISIs are not yet there.
4. Faster than WASM
5. Does not introduce additional complexity as WASM does.

### Cons

1. Can be customized only at compile time, can not be stored in genesis

## Alternatives

1. Use Iroha 1 approach with roles and grantable permissions and do hardcoded permissions checks inside instructions
   
   1. **Pros**:
      
      1. Tested in already running blockchains like Bakong and Byacco
   2. **Cons**:
      
      1. Hardcoded permission model - not possible to suit to different types of blockchains
2. Use Iroha Special Instructions as scripting for checking permissions + Assets mechanisms to store. With two options: implement permission checks as triggers, or simply another part of validation pipeline.
   
   1. **Pros:**
      
      1. Customizable permissions check logic
      2. Can be changed at runtime and stored in file
   2. **Cons:**
      
      1. ISIs and Queries are not mature enough to write complex logic that might be needed for permission checks
      2. Triggers design is not finalized and they are not implemented.
3. Use WASM permission check functions
   
   1. **Pros:**
      
      1. Customizable permissions check logic
      2. Can be changed at runtime and stored in file
      3. Can be written in any language that can be compiled to WASM
   2. **Cons:**
      
      1. WASM execution is in general slower
      2. Types through all the codebase will need to be adapted to be compatible with WASM
      3. More research about the WASM libraries and execution is needed

## Additional Information

- This solution impacts the Genesis Block design
- This makes Iroha closer to a framework

## Attachments:

![](images/icons/bullet_blue.gif) [dummyfile.txt](attachments/21012321/21017047.txt) (text/plain)

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
