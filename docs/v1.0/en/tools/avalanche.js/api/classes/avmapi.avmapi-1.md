[avalanche](../README.md) › [AVMAPI](../modules/avmapi.md) › [AVMAPI](avmapi.avmapi-1.md)

# Class: AVMAPI

Class for interacting with a node endpoint that is using the AVM.

**`remarks`** This extends the [JRPCAPI](utils_types.jrpcapi.md) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1.md#addapi) function to register this interface with Avalanche.

## Hierarchy

  ↳ [JRPCAPI](utils_types.jrpcapi.md)

  ↳ **AVMAPI**

## Index

### Constructors

* [constructor](avmapi.avmapi-1.md#constructor)

### Properties

* [AVAAssetID](avmapi.avmapi-1.md#protected-avaassetid)
* [baseurl](avmapi.avmapi-1.md#protected-baseurl)
* [blockchainID](avmapi.avmapi-1.md#protected-blockchainid)
* [core](avmapi.avmapi-1.md#protected-core)
* [db](avmapi.avmapi-1.md#protected-db)
* [jrpcVersion](avmapi.avmapi-1.md#protected-jrpcversion)
* [rpcid](avmapi.avmapi-1.md#protected-rpcid)

### Methods

* [addressFromBuffer](avmapi.avmapi-1.md#addressfrombuffer)
* [buildBaseTx](avmapi.avmapi-1.md#buildbasetx)
* [buildCreateAssetTx](avmapi.avmapi-1.md#buildcreateassettx)
* [buildGenesis](avmapi.avmapi-1.md#buildgenesis)
* [buildNFTTransferTx](avmapi.avmapi-1.md#buildnfttransfertx)
* [callMethod](avmapi.avmapi-1.md#callmethod)
* [createAddress](avmapi.avmapi-1.md#createaddress)
* [createFixedCapAsset](avmapi.avmapi-1.md#createfixedcapasset)
* [createMintTx](avmapi.avmapi-1.md#createminttx)
* [createVariableCapAsset](avmapi.avmapi-1.md#createvariablecapasset)
* [exportAVA](avmapi.avmapi-1.md#exportava)
* [exportKey](avmapi.avmapi-1.md#exportkey)
* [getAVAAssetID](avmapi.avmapi-1.md#getavaassetid)
* [getAllBalances](avmapi.avmapi-1.md#getallbalances)
* [getAssetDescription](avmapi.avmapi-1.md#getassetdescription)
* [getBalance](avmapi.avmapi-1.md#getbalance)
* [getBaseURL](avmapi.avmapi-1.md#getbaseurl)
* [getBlockchainAlias](avmapi.avmapi-1.md#getblockchainalias)
* [getBlockchainID](avmapi.avmapi-1.md#getblockchainid)
* [getDB](avmapi.avmapi-1.md#getdb)
* [getRPCID](avmapi.avmapi-1.md#getrpcid)
* [getTxStatus](avmapi.avmapi-1.md#gettxstatus)
* [getUTXOs](avmapi.avmapi-1.md#getutxos)
* [importAVA](avmapi.avmapi-1.md#importava)
* [importKey](avmapi.avmapi-1.md#importkey)
* [issueTx](avmapi.avmapi-1.md#issuetx)
* [keyChain](avmapi.avmapi-1.md#keychain)
* [listAddresses](avmapi.avmapi-1.md#listaddresses)
* [parseAddress](avmapi.avmapi-1.md#parseaddress)
* [refreshBlockchainID](avmapi.avmapi-1.md#refreshblockchainid)
* [send](avmapi.avmapi-1.md#send)
* [setBaseURL](avmapi.avmapi-1.md#setbaseurl)
* [signMintTx](avmapi.avmapi-1.md#signminttx)
* [signTx](avmapi.avmapi-1.md#signtx)

## Constructors

###  constructor

\+ **new AVMAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1.md), `baseurl`: string, `blockchainID`: string): *[AVMAPI](avmapi.avmapi-1.md)*

*Overrides [JRPCAPI](utils_types.jrpcapi.md).[constructor](utils_types.jrpcapi.md#constructor)*

*Defined in [apis/avm/api.ts:822](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L822)*

This class should not be instantiated directly. Instead use the [Avalanche.addAPI](avalanche.avalanche-1.md#addapi) method.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`core` | [AvalancheCore](avalanchecore.avalanchecore-1.md) | - | A reference to the Avalanche class |
`baseurl` | string | "/ext/bc/avm" | Defaults to the string "/ext/bc/avm" as the path to blockchain's baseurl  |
`blockchainID` | string | "" | - |

**Returns:** *[AVMAPI](avmapi.avmapi-1.md)*

## Properties

### `Protected` AVAAssetID

• **AVAAssetID**: *Buffer* = undefined

*Defined in [apis/avm/api.ts:88](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L88)*

___

### `Protected` baseurl

• **baseurl**: *string*

*Inherited from [APIBase](utils_types.apibase.md).[baseurl](utils_types.apibase.md#protected-baseurl)*

*Defined in [utils/types.ts:34](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L34)*

___

### `Protected` blockchainID

• **blockchainID**: *string* = ""

*Defined in [apis/avm/api.ts:87](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L87)*

___

### `Protected` core

• **core**: *[AvalancheCore](avalanchecore.avalanchecore-1.md)*

*Inherited from [APIBase](utils_types.apibase.md).[core](utils_types.apibase.md#protected-core)*

*Defined in [utils/types.ts:33](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L33)*

___

### `Protected` db

• **db**: *StoreAPI*

*Inherited from [APIBase](utils_types.apibase.md).[db](utils_types.apibase.md#protected-db)*

*Defined in [utils/types.ts:35](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L35)*

___

### `Protected` jrpcVersion

• **jrpcVersion**: *string* = "2.0"

*Inherited from [JRPCAPI](utils_types.jrpcapi.md).[jrpcVersion](utils_types.jrpcapi.md#protected-jrpcversion)*

*Defined in [utils/types.ts:276](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L276)*

___

### `Protected` rpcid

• **rpcid**: *number* = 1

*Inherited from [JRPCAPI](utils_types.jrpcapi.md).[rpcid](utils_types.jrpcapi.md#protected-rpcid)*

*Defined in [utils/types.ts:277](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L277)*

## Methods

###  addressFromBuffer

▸ **addressFromBuffer**(`address`: Buffer): *string*

*Defined in [apis/avm/api.ts:143](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L143)*

**Parameters:**

Name | Type |
------ | ------ |
`address` | Buffer |

**Returns:** *string*

___

###  buildBaseTx

▸ **buildBaseTx**(`utxoset`: [UTXOSet](avmapi_utxos.utxoset.md), `amount`: BN, `toAddresses`: Array‹string›, `fromAddresses`: Array‹string›, `changeAddresses`: Array‹string›, `assetID`: Buffer | string, `asOf`: BN, `locktime`: BN, `threshold`: number): *Promise‹[UnsignedTx](avmapi_transactions.unsignedtx.md)›*

*Defined in [apis/avm/api.ts:598](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L598)*

Helper function which creates an unsigned transaction. For more granular control, you may create your own
[UnsignedTx](avmapi_transactions.unsignedtx.md) manually (with their corresponding [TransferableInput](avmapi_inputs.transferableinput.md)s, [TransferableOutput](avmapi_outputs.transferableoutput.md)s, and [[TransferOperation]]s).

**`remarks`** 
This helper exists because the endpoint API should be the primary point of entry for most functionality.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`utxoset` | [UTXOSet](avmapi_utxos.utxoset.md) | - | A set of UTXOs that the transaction is built on |
`amount` | BN | - | The amount of AVA to be spent in $nAVA |
`toAddresses` | Array‹string› | - | The addresses to send the funds |
`fromAddresses` | Array‹string› | - | The addresses being used to send the funds from the UTXOs provided |
`changeAddresses` | Array‹string› | - | The addresses that can spend the change remaining from the spent UTXOs |
`assetID` | Buffer &#124; string | undefined | The assetID of the value being sent |
`asOf` | BN | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/) |
`locktime` | BN | new BN(0) | Optional. The locktime field created in the resulting outputs |
`threshold` | number | 1 | Optional. The number of signatures required to spend the funds in the resultant UTXO  |

**Returns:** *Promise‹[UnsignedTx](avmapi_transactions.unsignedtx.md)›*

An unsigned transaction ([UnsignedTx](avmapi_transactions.unsignedtx.md)) which contains a [BaseTx](avmapi_transactions.basetx.md).

___

###  buildCreateAssetTx

▸ **buildCreateAssetTx**(`utxoset`: [UTXOSet](avmapi_utxos.utxoset.md), `fee`: BN, `creatorAddresses`: Array‹string› | Array‹Buffer›, `initialStates`: [InitialStates](avmapi_types.initialstates.md), `name`: string, `symbol`: string, `denomination`: number): *Promise‹[UnsignedTx](avmapi_transactions.unsignedtx.md)›*

*Defined in [apis/avm/api.ts:675](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L675)*

Creates an unsigned transaction. For more granular control, you may create your own
[UnsignedTx](avmapi_transactions.unsignedtx.md) manually (with their corresponding [TransferableInput](avmapi_inputs.transferableinput.md)s, [TransferableOutput](avmapi_outputs.transferableoutput.md)s, and [[TransferOperation]]s).

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`utxoset` | [UTXOSet](avmapi_utxos.utxoset.md) | A set of UTXOs that the transaction is built on |
`fee` | BN | The amount of AVA to be paid for fees, in $nAVA |
`creatorAddresses` | Array‹string› &#124; Array‹Buffer› | The addresses to send the fees |
`initialStates` | [InitialStates](avmapi_types.initialstates.md) | The [InitialStates](avmapi_types.initialstates.md) that represent the intial state of a created asset |
`name` | string | String for the descriptive name of the asset |
`symbol` | string | String for the ticker symbol of the asset |
`denomination` | number | Optional number for the denomination which is 10^D. D must be >= 0 and <= 32. Ex: $1 AVA = 10^9 $nAVA  |

**Returns:** *Promise‹[UnsignedTx](avmapi_transactions.unsignedtx.md)›*

An unsigned transaction ([UnsignedTx](avmapi_transactions.unsignedtx.md)) which contains a [CreateAssetTx](avmapi_transactions.createassettx.md).

___

###  buildGenesis

▸ **buildGenesis**(`genesisData`: object): *Promise‹string›*

*Defined in [apis/avm/api.ts:792](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L792)*

Given a JSON representation of this Virtual Machine’s genesis state, create the byte representation of that state.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`genesisData` | object | The blockchain's genesis data object  |

**Returns:** *Promise‹string›*

Promise of a string of bytes

___

###  buildNFTTransferTx

▸ **buildNFTTransferTx**(`utxoset`: [UTXOSet](avmapi_utxos.utxoset.md), `utxoid`: string | Array‹string›, `toAddresses`: Array‹string›, `fromAddresses`: Array‹string›, `feeAmount`: BN, `feeAddresses`: Array‹string›, `asOf`: BN, `locktime`: BN, `threshold`: number): *Promise‹[UnsignedTx](avmapi_transactions.unsignedtx.md)›*

*Defined in [apis/avm/api.ts:637](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L637)*

Helper function which creates an unsigned NFT Transfer. For more granular control, you may create your own
[UnsignedTx](avmapi_transactions.unsignedtx.md) manually (with their corresponding [TransferableInput](avmapi_inputs.transferableinput.md)s, [TransferableOutput](avmapi_outputs.transferableoutput.md)s, and [[TransferOperation]]s).

**`remarks`** 
This helper exists because the endpoint API should be the primary point of entry for most functionality.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`utxoset` | [UTXOSet](avmapi_utxos.utxoset.md) | - | A set of UTXOs that the transaction is built on |
`utxoid` | string &#124; Array‹string› | - | A base58 utxoID or an array of base58 utxoIDs for the nfts this transaction is sending |
`toAddresses` | Array‹string› | - | The addresses to send the NFT |
`fromAddresses` | Array‹string› | - | The addresses being used to send the NFT from the utxoID provided |
`feeAmount` | BN | - | The amount of fees being paid for this transaction |
`feeAddresses` | Array‹string› | - | The addresses that have the AVA funds to pay for fees of the UTXO |
`asOf` | BN | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/) |
`locktime` | BN | new BN(0) | Optional. The locktime field created in the resulting outputs |
`threshold` | number | 1 | Optional. The number of signatures required to spend the funds in the resultant UTXO  |

**Returns:** *Promise‹[UnsignedTx](avmapi_transactions.unsignedtx.md)›*

An unsigned transaction ([UnsignedTx](avmapi_transactions.unsignedtx.md)) which contains a [NFTTransferTx]].

___

###  callMethod

▸ **callMethod**(`method`: string, `params?`: Array‹object› | object, `baseurl?`: string): *Promise‹[RequestResponseData](utils_types.requestresponsedata.md)›*

*Inherited from [JRPCAPI](utils_types.jrpcapi.md).[callMethod](utils_types.jrpcapi.md#callmethod)*

*Defined in [utils/types.ts:278](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L278)*

**Parameters:**

Name | Type |
------ | ------ |
`method` | string |
`params?` | Array‹object› &#124; object |
`baseurl?` | string |

**Returns:** *Promise‹[RequestResponseData](utils_types.requestresponsedata.md)›*

___

###  createAddress

▸ **createAddress**(`username`: string, `password`: string): *Promise‹string›*

*Defined in [apis/avm/api.ts:215](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L215)*

Creates an address (and associated private keys) on a user on a blockchain.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | Name of the user to create the address under |
`password` | string | Password to unlock the user and encrypt the private key  |

**Returns:** *Promise‹string›*

Promise for a string representing the address created by the vm.

___

###  createFixedCapAsset

▸ **createFixedCapAsset**(`username`: string, `password`: string, `name`: string, `symbol`: string, `denomination`: number, `initialHolders`: Array‹object›): *Promise‹string›*

*Defined in [apis/avm/api.ts:251](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L251)*

Create a new fixed-cap, fungible asset. A quantity of it is created at initialization and there no more is ever created.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The user paying the transaction fee (in $AVA) for asset creation |
`password` | string | The password for the user paying the transaction fee (in $AVA) for asset creation |
`name` | string | The human-readable name for the asset |
`symbol` | string | Optional. The shorthand symbol for the asset. Between 0 and 4 characters |
`denomination` | number | Optional. Determines how balances of this asset are displayed by user interfaces. Default is 0 |
`initialHolders` | Array‹object› | An array of objects containing the field "address" and "amount" to establish the genesis values for the new asset  ```js Example initialHolders: [     {         "address": "X-7sik3Pr6r1FeLrvK1oWwECBS8iJ5VPuSh",         "amount": 10000     },     {         "address": "X-7sik3Pr6r1FeLrvK1oWwECBS8iJ5VPuSh",         "amount": 50000     } ] ```  |

**Returns:** *Promise‹string›*

Returns a Promise<string> containing the base 58 string representation of the ID of the newly created asset.

___

###  createMintTx

▸ **createMintTx**(`amount`: number | BN, `assetID`: Buffer | string, `to`: string, `minters`: Array‹string›): *Promise‹string›*

*Defined in [apis/avm/api.ts:321](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L321)*

Create an unsigned transaction to mint more of an asset.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`amount` | number &#124; BN | The units of the asset to mint |
`assetID` | Buffer &#124; string | The ID of the asset to mint |
`to` | string | The address to assign the units of the minted asset |
`minters` | Array‹string› | Addresses of the minters responsible for signing the transaction  |

**Returns:** *Promise‹string›*

Returns a Promise<string> containing the base 58 string representation of the unsigned transaction.

___

###  createVariableCapAsset

▸ **createVariableCapAsset**(`username`: string, `password`: string, `name`: string, `symbol`: string, `denomination`: number, `minterSets`: Array‹object›): *Promise‹string›*

*Defined in [apis/avm/api.ts:297](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L297)*

Create a new variable-cap, fungible asset. No units of the asset exist at initialization. Minters can mint units of this asset using createMintTx, signMintTx and sendMintTx.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The user paying the transaction fee (in $AVA) for asset creation |
`password` | string | The password for the user paying the transaction fee (in $AVA) for asset creation |
`name` | string | The human-readable name for the asset |
`symbol` | string | Optional. The shorthand symbol for the asset -- between 0 and 4 characters |
`denomination` | number | Optional. Determines how balances of this asset are displayed by user interfaces. Default is 0 |
`minterSets` | Array‹object› | is a list where each element specifies that threshold of the addresses in minters may together mint more of the asset by signing a minting transaction  ```js Example minterSets: [      {          "minters":[              "X-4peJsFvhdn7XjhNF4HWAQy6YaJts27s9q"          ],          "threshold": 1      },      {          "minters": [              "X-dcJ6z9duLfyQTgbjq2wBCowkvcPZHVDF",              "X-2fE6iibqfERz5wenXE6qyvinsxDvFhHZk",              "X-7ieAJbfrGQbpNZRAQEpZCC1Gs1z5gz4HU"          ],          "threshold": 2      } ] ```  |

**Returns:** *Promise‹string›*

Returns a Promise<string> containing the base 58 string representation of the ID of the newly created asset.

___

###  exportAVA

▸ **exportAVA**(`username`: string, `password`: string, `to`: string, `amount`: BN): *Promise‹string›*

*Defined in [apis/avm/api.ts:427](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L427)*

Send AVA from the X-Chain to an account on the P-Chain.

After calling this method, you must call the P-Chain’s importAVA method to complete the transfer.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The Keystore user that controls the P-Chain account specified in `to` |
`password` | string | The password of the Keystore user |
`to` | string | The account on the P-Chain to send the AVA to. Do not include P- in the address |
`amount` | BN | Amount of AVA to export as a [BN](https://github.com/indutny/bn.js/)  |

**Returns:** *Promise‹string›*

String representing the transaction id

___

###  exportKey

▸ **exportKey**(`username`: string, `password`: string, `address`: string): *Promise‹string›*

*Defined in [apis/avm/api.ts:380](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L380)*

Exports the private key for an address.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The name of the user with the private key |
`password` | string | The password used to decrypt the private key |
`address` | string | The address whose private key should be exported  |

**Returns:** *Promise‹string›*

Promise with the decrypted private key as store in the database

___

###  getAVAAssetID

▸ **getAVAAssetID**(): *Promise‹Buffer›*

*Defined in [apis/avm/api.ts:153](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L153)*

Fetches the AVA AssetID and returns it in a Promise.

**Returns:** *Promise‹Buffer›*

The the provided string representing the blockchainID

___

###  getAllBalances

▸ **getAllBalances**(`address`: string): *Promise‹Array‹object››*

*Defined in [apis/avm/api.ts:486](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L486)*

Retrieves all assets for an address on a server and their associated balances.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | string | The address to get a list of assets  |

**Returns:** *Promise‹Array‹object››*

Promise of an object mapping assetID strings with [BN](https://github.com/indutny/bn.js/) balance for the address on the blockchain.

___

###  getAssetDescription

▸ **getAssetDescription**(`assetID`: Buffer | string): *Promise‹object›*

*Defined in [apis/avm/api.ts:506](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L506)*

Retrieves an assets name and symbol.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`assetID` | Buffer &#124; string | Either a [Buffer](https://github.com/feross/buffer) or an AVA serialized string for the AssetID or its alias.  |

**Returns:** *Promise‹object›*

Returns a Promise<object> with keys "name" and "symbol".

___

###  getBalance

▸ **getBalance**(`address`: string, `assetID`: string): *Promise‹BN›*

*Defined in [apis/avm/api.ts:192](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L192)*

Gets the balance of a particular asset on a blockchain.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | string | The address to pull the asset balance from |
`assetID` | string | The assetID to pull the balance from  |

**Returns:** *Promise‹BN›*

Promise with the balance of the assetID as a [BN](https://github.com/indutny/bn.js/) on the provided address for the blockchain.

___

###  getBaseURL

▸ **getBaseURL**(): *string*

*Inherited from [APIBase](utils_types.apibase.md).[getBaseURL](utils_types.apibase.md#getbaseurl)*

*Defined in [utils/types.ts:58](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L58)*

Returns the baseurl's path.

**Returns:** *string*

___

###  getBlockchainAlias

▸ **getBlockchainAlias**(): *string*

*Defined in [apis/avm/api.ts:95](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L95)*

Gets the alias for the blockchainID if it exists, otherwise returns `undefined`.

**Returns:** *string*

The alias for the blockchainID

___

###  getBlockchainID

▸ **getBlockchainID**(): *string*

*Defined in [apis/avm/api.ts:109](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L109)*

Gets the blockchainID and returns it.

**Returns:** *string*

The blockchainID

___

###  getDB

▸ **getDB**(): *StoreAPI*

*Inherited from [APIBase](utils_types.apibase.md).[getDB](utils_types.apibase.md#getdb)*

*Defined in [utils/types.ts:65](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L65)*

Returns the baseurl's database.

**Returns:** *StoreAPI*

___

###  getRPCID

▸ **getRPCID**(): *number*

*Inherited from [JRPCAPI](utils_types.jrpcapi.md).[getRPCID](utils_types.jrpcapi.md#getrpcid)*

*Defined in [utils/types.ts:320](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L320)*

Returns the rpcid, a strictly-increasing number, starting from 1, indicating the next request ID that will be sent.

**Returns:** *number*

___

###  getTxStatus

▸ **getTxStatus**(`txid`: string): *Promise‹string›*

*Defined in [apis/avm/api.ts:533](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L533)*

Returns the status of a provided transaction ID by calling the node's `getTxStatus` method.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`txid` | string | The string representation of the transaction ID  |

**Returns:** *Promise‹string›*

Returns a Promise<string> containing the status retrieved from the node

___

###  getUTXOs

▸ **getUTXOs**(`addresses`: Array‹string› | Array‹Buffer›, `persistOpts`: [PersistanceOptions](avmapi.persistanceoptions.md)): *Promise‹[UTXOSet](avmapi_utxos.utxoset.md)›*

*Defined in [apis/avm/api.ts:552](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L552)*

Retrieves the UTXOs related to the addresses provided from the node's `getUTXOs` method.

**`remarks`** 
persistOpts is optional and must be of type [PersistanceOptions](avmapi.persistanceoptions.md)

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`addresses` | Array‹string› &#124; Array‹Buffer› | - | An array of addresses as strings or addresses as [Buffer](https://github.com/feross/buffer)s |
`persistOpts` | [PersistanceOptions](avmapi.persistanceoptions.md) | undefined | Options available to persist these UTXOs in local storage  |

**Returns:** *Promise‹[UTXOSet](avmapi_utxos.utxoset.md)›*

___

###  importAVA

▸ **importAVA**(`username`: string, `password`: string, `to`: string): *Promise‹string›*

*Defined in [apis/avm/api.ts:450](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L450)*

Finalize a transfer of AVA from the P-Chain to the X-Chain.

Before this method is called, you must call the P-Chain’s `exportAVA` method to initiate the transfer.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The Keystore user that controls the address specified in `to` |
`password` | string | The password of the Keystore user  |
`to` | string | The address the AVA is sent to. This must be the same as the to argument in the corresponding call to the P-Chain’s exportAVA, except that the prepended X- should be included in this argument |

**Returns:** *Promise‹string›*

String representing the transaction id

___

###  importKey

▸ **importKey**(`username`: string, `password`: string, `privateKey`: string): *Promise‹string›*

*Defined in [apis/avm/api.ts:404](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L404)*

Imports a private key into the node's keystore under an user and for a blockchain.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The name of the user to store the private key |
`password` | string | The password that unlocks the user |
`privateKey` | string | A string representing the private key in the vm's format  |

**Returns:** *Promise‹string›*

The address for the imported private key.

___

###  issueTx

▸ **issueTx**(`tx`: string | Buffer | [Tx](avmapi_transactions.tx.md)): *Promise‹string›*

*Defined in [apis/avm/api.ts:716](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L716)*

Calls the node's issueTx method from the API and returns the resulting transaction ID as a string.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`tx` | string &#124; Buffer &#124; [Tx](avmapi_transactions.tx.md) | A string, [Buffer](https://github.com/feross/buffer), or [Tx](avmapi_transactions.tx.md) representing a transaction  |

**Returns:** *Promise‹string›*

A Promise<string> representing the transaction ID of the posted transaction.

___

###  keyChain

▸ **keyChain**(): *[AVMKeyChain](avmapi_keychain.avmkeychain.md)*

*Defined in [apis/avm/api.ts:166](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L166)*

Gets a reference to the keychain for this class.

**Returns:** *[AVMKeyChain](avmapi_keychain.avmkeychain.md)*

The instance of [AVMKeyChain](avmapi_keychain.avmkeychain.md) for this class

___

###  listAddresses

▸ **listAddresses**(`username`: string, `password`: string): *Promise‹Array‹string››*

*Defined in [apis/avm/api.ts:469](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L469)*

Lists all the addresses under a user.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The user to list addresses |
`password` | string | The password of the user to list the addresses  |

**Returns:** *Promise‹Array‹string››*

Promise of an array of address strings in the format specified by the blockchain.

___

###  parseAddress

▸ **parseAddress**(`addr`: string): *Buffer*

*Defined in [apis/avm/api.ts:137](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L137)*

Takes an address string and returns its [Buffer](https://github.com/feross/buffer) representation if valid.

**Parameters:**

Name | Type |
------ | ------ |
`addr` | string |

**Returns:** *Buffer*

A [Buffer](https://github.com/feross/buffer) for the address if valid, undefined if not valid.

___

###  refreshBlockchainID

▸ **refreshBlockchainID**(`blockchainID`: string): *boolean*

*Defined in [apis/avm/api.ts:120](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L120)*

Refresh blockchainID, and if a blockchainID is passed in, use that.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`blockchainID` | string | undefined |

**Returns:** *boolean*

The blockchainID

___

###  send

▸ **send**(`username`: string, `password`: string, `assetID`: string | Buffer, `amount`: number | BN, `to`: string, `from`: Array‹string› | Array‹Buffer›): *Promise‹string›*

*Defined in [apis/avm/api.ts:750](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L750)*

Sends an amount of assetID to the specified address from a list of owned of addresses.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The user that owns the private keys associated with the `from` addresses |
`password` | string | The password unlocking the user |
`assetID` | string &#124; Buffer | The assetID of the asset to send |
`amount` | number &#124; BN | The amount of the asset to be sent |
`to` | string | The address of the recipient |
`from` | Array‹string› &#124; Array‹Buffer› | An array of addresses managed by the node's keystore for this blockchain which will fund this transaction  |

**Returns:** *Promise‹string›*

Promise for the string representing the transaction's ID.

___

###  setBaseURL

▸ **setBaseURL**(`baseurl`: string): *void*

*Inherited from [APIBase](utils_types.apibase.md).[setBaseURL](utils_types.apibase.md#setbaseurl)*

*Defined in [utils/types.ts:42](https://github.com/ava-labs/avalanche.js/blob/c723742/src/utils/types.ts#L42)*

Sets the path of the APIs baseurl.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`baseurl` | string | Path of the APIs baseurl - ex: "/ext/bc/avm"  |

**Returns:** *void*

___

###  signMintTx

▸ **signMintTx**(`username`: string, `password`: string, `tx`: string | Buffer, `minter`: string): *Promise‹string›*

*Defined in [apis/avm/api.ts:355](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L355)*

Sign an unsigned or partially signed mint transaction.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The user signing |
`password` | string | The password for the user signing |
`tx` | string &#124; Buffer | The output of createMintTx or signMintTx |
`minter` | string | The minter signing this transaction  |

**Returns:** *Promise‹string›*

Returns a Promise<string> containing the base 58 string representation of the unsigned transaction.

___

###  signTx

▸ **signTx**(`utx`: [UnsignedTx](avmapi_transactions.unsignedtx.md)): *[Tx](avmapi_transactions.tx.md)*

*Defined in [apis/avm/api.ts:705](https://github.com/ava-labs/avalanche.js/blob/c723742/src/apis/avm/api.ts#L705)*

Helper function which takes an unsigned transaction and signs it, returning the resulting [Tx](avmapi_transactions.tx.md).

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`utx` | [UnsignedTx](avmapi_transactions.unsignedtx.md) | The unsigned transaction of type [UnsignedTx](avmapi_transactions.unsignedtx.md)  |

**Returns:** *[Tx](avmapi_transactions.tx.md)*

A signed transaction of type [Tx](avmapi_transactions.tx.md)
