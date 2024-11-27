1. [Hyperledger Iroha](index.html)
2. [Hyperledger Iroha](Hyperledger-Iroha_20873224.html)
3. [Iroha 2](Iroha-2_21012047.html)
4. [Architecture Decision Records Log](Architecture-Decision-Records-Log_21016003.html)

# Hyperledger Iroha : Genesis Block and Network Setup

Created by Egor Ivkov, last modified on Aug 16, 2021

Status

DECIDED

Stakeholders

 [武宮誠](https://lf-hyperledger.atlassian.net/wiki/people/557058:12c320e6-5d17-404f-b20e-bfa5721ae960?ref=confluence) [Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence) [Nikita Puzankov](https://lf-hyperledger.atlassian.net/wiki/people/5df113768998970e5b434e0a?ref=confluence)

Outcome

Due date

25 Sep 2020

Owner

[Egor Ivkov](https://lf-hyperledger.atlassian.net/wiki/people/5dd9631c1cf3c20ef5ff9f0f?ref=confluence)

# Background

Below there is a part of code with initial configuration of the World State View, which each peer executes on startup. Initially there was a plan to move this logic into the **genesis block** functionality and transform it into several Iroha Special Instruction.

After some initial work on this task it appears that this part could not be moved to genesis block and in general there should not be any genesis block based logic in core Iroha.

```
		let domain_name = "global".to_string();
       	let mut asset_definitions = BTreeMap::new();
        let asset_definition_id = permission::permission_asset_definition_id();
        asset_definitions.insert(
            asset_definition_id.clone(),
            AssetDefinition::new(asset_definition_id.clone()),
        );
        let account_id = AccountId::new("root", &domain_name);
        let asset_id = AssetId {
            definition_id: asset_definition_id,
            account_id: account_id.clone(),
        };
        let asset = Asset::with_permission(asset_id.clone(), Permission::Anything);
        let mut account = Account::with_signatory(
            &account_id.name,
            &account_id.domain_name,
            config.public_key.clone(),
        );
        account.assets.insert(asset_id, asset);
        let mut accounts = BTreeMap::new();
        accounts.insert(account_id, account);
        let domain = Domain {
            name: domain_name.clone(),
            accounts,
            asset_definitions,
        };
        let mut domains = BTreeMap::new();
        domains.insert(domain_name, domain);
        let world_state_view = Arc::new(RwLock::new(WorldStateView::new(Peer::with_domains(
            PeerId::new(&config.torii_configuration.torii_url, &config.public_key),
            &config.sumeragi_configuration.trusted_peers,
            domains,
        ))));
```

# Problem

## Root account

The data model of Iroha is build around domains, accounts, assets and corresponding permissions. Based on this model it is essential that at the point of peers network initialization system should have a sudo/root user with \`DoAnything\` permission**.** 

Only "root" user can create accounts with lesser privileges, domains of different types and different assets.

Right now this type of user is created by direct manipulation of the World State View when the peer is started as you can see in the code listing. And consequently it is impossible to create this user by Iroha Special Instructions, as we need some account that this Iroha Special Instructions would relate to with \`DoAnything\` permission. Genesis block can't solve this problem without modification of basic Iroha mechanisms Permissions + Instructions.

## Permission Representation

Currently permissions are represented as assets in the predefined **permissions** domain. They are then given to different accounts. Consequently the logic of permission domain initialization also can not be moved to ISI in genesis block.

# Solution

The solution which I propose to this question is not to define any genesis block related logic in Iroha. The World State View will be initialized with the "root" user on peer startup and then depending on the type of blockchain application that is built on top of Iroha, the app will proceed with its own initialization transactions:

1. For **public blockchains** it would be reasonable to execute a transaction for the root user to remove itself after all initial setup is done.
2. For **private blockchains** the user may remain for some system administration related work.

If this solution is accepted we should proceed to remove the initial Kura code related to the genesis block issue.

# Decisions

- Every Iroha Peer starts with "root@global" Account with \`DoAnything\` permission

# Alternatives

Provide instructions or instruction mode that can be executed only at genesis - an equivalent of DoAnything permission but without root. May prove to be a lot of work, with a rather small outcome.

# Concerns

We should be careful to design the solution so that it can be used in both public and private blockchains. It is addressed in the **Solution** section.

# Assumptions

Assumption is made that we do not want to change much the current data model of domains, accounts, assets and permissions.

# Risks

We do not want to change the data model much, as some other projects already depend on it.

# Additional Information

Every other setup related work apart from root account initialization and permissions domain initialization can be done by ordinary transactions submitted by clients and therefore does not require genesis block related functionality.

# Final Decision

It was decided to disable permission checks specifically for genesis block validation.

Document generated by Confluence on Nov 26, 2024 15:06

[Atlassian](http://www.atlassian.com/)
