1. [Community Events](index.html)
2. [Community Events Home](Community-Events-Home_21790731.html)
3. [Workshops](Workshops_21790888.html)
4. [Hyperledger Indy Technical Deep Dive](Hyperledger-Indy-Technical-Deep-Dive_21792290.html)

# Community Events : Hyperledger Indy Technical Deep Dive - Handout

Created by Daniel Bluhm, last modified on Feb 03, 2022

## Workshop Prerequisites

Please complete the instructions found [here](https://lf-hyperledger.atlassian.net/wiki/display/events/Hyperledger+Indy+Technical+Deep+Dive+Prerequisites) in order to be prepared for the hands on portion of the workshop. If you have questions about these prerequisites, we'll do our best to provide assistance on [RocketChat in the #indy channel](https://chat.hyperledger.org/channel/indy).

## Useful Links and Additional Reading

- How to install the Indy CLI: See Appendix A of the [Indicio Selfserve Instructions](https://docs.google.com/document/d/18-8MiRRuxVHn-FFWyd8LHukPNl_WNzo-tJtXK9bmZfY)
- Go to [this link](https://github.com/Indicio-tech/indicio-network) then click appropriate directories to see examples of Genesis files, TAA, AML, and auth\_rules.
- [TAA Walkthrough](https://docs.google.com/document/d/1FWBW9KFWuyqCEetkf2z-tD1LWN7UjiBB/edit?usp=sharing&ouid=108812736870072316534&rtpof=true&sd=true) - instructions for adding a TAA to a network.
- [Indy DID Method Specification](https://hyperledger.github.io/indy-did-method/)
- [RBFT Consensus Algorithm](https://pakupaku.me/plaublin/rbft/5000a297.pdf)
- [BFT Algorithms in Hyperledger Fabric and Indy](https://medium.com/@IAMVISH/consensus-algorithms-in-hyperledger-framework-c8d40507aa70) - An excellent discussion and comparison of Consensus Algorithms in Indy and Fabric.
- [Plenum read the docs](https://hyperledger-indy.readthedocs.io/projects/plenum/en/latest/main.html)
- [Indy Node easy first tasks](https://github.com/hyperledger/indy-node/issues?q=is%3Aopen%20is%3Aissue%20label%3A%22good%20first%20issue%22)
- [Hyperledger Indy Project Enhancements](https://github.com/hyperledger/indy-hipe)

## Hands-On Guide

We will be extending the nym transaction in indy plenum to include an image field. **We are working from the 'ubuntu-20.04-upgrade' branch.**

1. To get started we will create a test that writes a nym with an image, then retrieves it from the ledger, and finally checks the returned image is correct.
   
   In **`indy_node/test/nym_txn/test_nym_additional.py`**  around line 90 add this test.
   
   1. **test\_nym\_img**
      
      ```
      def test_nym_img(looper, sdk_pool_handle, sdk_wallet_steward, endorser_did_verkey):
    # prepare txn
    did, verkey = endorser_did_verkey
    nym_request, _ = looper.loop.run_until_complete(
        prepare_nym_request(sdk_wallet_steward, None,
                            None, ENDORSER_STRING, did, verkey, False if verkey else True))
    # modify transaction to include image
    hyperledger_logo = 'https://raw.githubusercontent.com/hyperledger/indy-node/master/collateral/logos/indy-logo.png'
    txn = json.loads(nym_request)
    txn['operation']['img'] = hyperledger_logo # don't do this, avoid private data on ledgers
    request_couple = sdk_sign_and_send_prepared_request(looper, sdk_wallet_steward,
                                                        sdk_pool_handle, json.dumps(txn))
    sdk_get_and_check_replies(looper, [request_couple])
    # check image is in the nym
    rep = get_nym(looper, sdk_pool_handle, sdk_wallet_steward, did)
    assert rep[0][1]['result']['data']
    assert json.loads(rep[0][1]['result']['data'])['img'] == hyperledger_logo
      ```
   2. Inside  **`indy_node/test/nym_txn`**  directory,  **`pytest -k test_nym_img`** should result in a failing test.
2. Now that we have a failing test we can start updating nym write transaction types. In **`indy_common/types.py`**  there is a class called `ClientOperationField` around line 470. This class extends operations. Looks like Indy Node does not change the basic nym operations, we will borrow some code from Indy Plenum that defines a new operation. We will define in the next steps a new **ClientNYMOperation**. Since we are here let's add the instantiation inside **\_specific\_operations**.
   
   1. **nym operation**
      
      ```
      ...
class ClientOperationField(PClientOperationField):
    _specific_operations = {
        NYM: ClientNYMOperation(), # <----- new operation
        SCHEMA: ClientSchemaOperation(),
        ATTRIB: ClientAttribOperation(),
...
      ```
   2. Around line 72 we will copy in the `ClientNYMOperation` class from Indy Plenum with our extra `img` field.
      
      **nym operation**
      
      ```
      class ClientNYMOperation(MessageValidator):
    schema = (
        (TXN_TYPE, ConstantField(NYM)),
        (ALIAS, LimitedLengthStringField(max_length=ALIAS_FIELD_LIMIT, optional=True)),
        (VERKEY, VerkeyField(optional=True, nullable=True)),
        (TARGET_NYM, DestNymField()),
        (ROLE, RoleField(optional=True)),
        (IMG, LimitedLengthStringField(max_length=RAW_FIELD_LIMIT, optional=True)) # <----- new image field
    )
      ```
   3. We also need to update some imports. Some of which we will define in the next steps.
      
      **nym operation**
      
      ```
      ...
# include  ALIAS, VERKEY from plenum.common.constants
from plenum.common.constants import TARGET_NYM, NONCE, RAW, ENC, HASH, NAME, \
    VERSION, FORCE, ORIGIN, OPERATION_SCHEMA_IS_STRICT, OP_VER, ALIAS, VERKEY
...
# include VerkeyField, DestNymField from plenum.common.messages.fields
from plenum.common.messages.fields import ConstantField, IdentifierField, \
	...
    AnyMapField, NonEmptyStringField, DatetimeStringField, RoleField, AnyField, FieldBase, VerkeyField, DestNymField
...
from plenum.config import JSON_FIELD_LIMIT, NAME_FIELD_LIMIT, DATA_FIELD_LIMIT, \
    NONCE_FIELD_LIMIT, \
    ENC_FIELD_LIMIT, RAW_FIELD_LIMIT, SIGNATURE_TYPE_FIELD_LIMIT, ALIAS_FIELD_LIMIT
...
# include NYM, IMG from indy_common.constants
from indy_common.constants import TXN_TYPE, ATTRIB, GET_ATTR, \
	...
    RICH_SCHEMA_PRES_DEF, RS_PRES_DEF_TYPE_VALUE, NYM, IMG
      ```
3. Now that we have a test, updated operator field we need to define the '`NYM`' string constant. Inside `indy_common/constants.py` define a new `NYM` constant around line 14.
   
   1. **nym constant**
      
      ```
      # NYM
IMG = "img"
      ```
4. With the client operation for nym updated we will have transactions with our new "img" field.  We now can update the nym handler.
   
   1. inside `indy_node/server/request_handlers/domain_req_handlers/nym_handler.py` we will add a check for the `img` field, if present, store it. On line 78, add the check inside of `update_state` with supporting `NYM` import.
      
      **nym handler**
      
      ```
      ...
from indy_common.constants import IMG, NYM <--- include NYM
...
     def update_state(self, txn, prev_result, request, is_committed=False):
		...
        if IMG in txn_data: # check for IMG field
            new_data[IMG] = txn_data[IMG] # store IMG
        ...
      ```
5. Inside `indy_node/test/nym_txn` directory, `pytest -k test_nym_img` should result in a passing test.
6. Celebrate!
7. You can find this coding example [here](https://github.com/Indicio-tech/indy-node/tree/deep-dive-handout), with a [diff highlighting changes](https://github.com/hyperledger/indy-node/compare/ubuntu-20.04-upgrade...Indicio-tech:deep-dive-handout?expand=1).

Document generated by Confluence on Nov 26, 2024 16:15

[Atlassian](http://www.atlassian.com/)
