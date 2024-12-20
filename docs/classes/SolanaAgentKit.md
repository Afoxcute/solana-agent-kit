[**solana-agent-kit v1.2.0**](../README.md)

***

[solana-agent-kit](../README.md) / SolanaAgentKit

# Class: SolanaAgentKit

Main class for interacting with Solana blockchain
Provides a unified interface for token operations, NFT management, and trading

 SolanaAgentKit

## Constructors

### new SolanaAgentKit()

> **new SolanaAgentKit**(`private_key`, `rpc_url`, `openai_api_key`): [`SolanaAgentKit`](SolanaAgentKit.md)

#### Parameters

##### private\_key

`string`

##### rpc\_url

`string` = `"https://api.mainnet-beta.solana.com"`

##### openai\_api\_key

`string`

#### Returns

[`SolanaAgentKit`](SolanaAgentKit.md)

#### Defined in

[agent/index.ts:48](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L48)

## Methods

### requestFaucetFunds()

> **requestFaucetFunds**(): `Promise`\<`string`\>

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:60](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L60)

***

### deployToken()

> **deployToken**(`name`, `uri`, `symbol`, `decimals`, `initialSupply`?): `Promise`\<\{ `mint`: `PublicKey`; \}\>

#### Parameters

##### name

`string`

##### uri

`string`

##### symbol

`string`

##### decimals

`number` = `DEFAULT_OPTIONS.TOKEN_DECIMALS`

##### initialSupply?

`number`

#### Returns

`Promise`\<\{ `mint`: `PublicKey`; \}\>

#### Defined in

[agent/index.ts:64](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L64)

***

### deployCollection()

> **deployCollection**(`options`): `Promise`\<[`CollectionDeployment`](../interfaces/CollectionDeployment.md)\>

#### Parameters

##### options

[`CollectionOptions`](../interfaces/CollectionOptions.md)

#### Returns

`Promise`\<[`CollectionDeployment`](../interfaces/CollectionDeployment.md)\>

#### Defined in

[agent/index.ts:74](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L74)

***

### getBalance()

> **getBalance**(`token_address`?): `Promise`\<`null` \| `number`\>

#### Parameters

##### token\_address?

`PublicKey`

#### Returns

`Promise`\<`null` \| `number`\>

#### Defined in

[agent/index.ts:78](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L78)

***

### mintNFT()

> **mintNFT**(`collectionMint`, `metadata`, `recipient`?): `Promise`\<[`MintCollectionNFTResponse`](../interfaces/MintCollectionNFTResponse.md)\>

#### Parameters

##### collectionMint

`PublicKey`

##### metadata

###### name

`string`

###### uri

`string`

###### sellerFeeBasisPoints

`number`

###### creators

`object`[]

##### recipient?

`PublicKey`

#### Returns

`Promise`\<[`MintCollectionNFTResponse`](../interfaces/MintCollectionNFTResponse.md)\>

#### Defined in

[agent/index.ts:82](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L82)

***

### transfer()

> **transfer**(`to`, `amount`, `mint`?): `Promise`\<`string`\>

#### Parameters

##### to

`PublicKey`

##### amount

`number`

##### mint?

`PublicKey`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:90](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L90)

***

### registerDomain()

> **registerDomain**(`name`, `spaceKB`?): `Promise`\<`string`\>

#### Parameters

##### name

`string`

##### spaceKB?

`number`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:94](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L94)

***

### resolveSolDomain()

> **resolveSolDomain**(`domain`): `Promise`\<`PublicKey`\>

#### Parameters

##### domain

`string`

#### Returns

`Promise`\<`PublicKey`\>

#### Defined in

[agent/index.ts:98](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L98)

***

### getPrimaryDomain()

> **getPrimaryDomain**(`account`): `Promise`\<`string`\>

#### Parameters

##### account

`PublicKey`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:102](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L102)

***

### trade()

> **trade**(`outputMint`, `inputAmount`, `inputMint`?, `slippageBps`?): `Promise`\<`string`\>

#### Parameters

##### outputMint

`PublicKey`

##### inputAmount

`number`

##### inputMint?

`PublicKey`

##### slippageBps?

`number` = `DEFAULT_OPTIONS.SLIPPAGE_BPS`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:106](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L106)

***

### lendAssets()

> **lendAssets**(`amount`): `Promise`\<`string`\>

#### Parameters

##### amount

`number`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:115](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L115)

***

### getTPS()

> **getTPS**(): `Promise`\<`number`\>

#### Returns

`Promise`\<`number`\>

#### Defined in

[agent/index.ts:119](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L119)

***

### getTokenDataByAddress()

> **getTokenDataByAddress**(`mint`): `Promise`\<`undefined` \| [`JupiterTokenData`](../interfaces/JupiterTokenData.md)\>

#### Parameters

##### mint

`string`

#### Returns

`Promise`\<`undefined` \| [`JupiterTokenData`](../interfaces/JupiterTokenData.md)\>

#### Defined in

[agent/index.ts:123](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L123)

***

### getTokenDataByTicker()

> **getTokenDataByTicker**(`ticker`): `Promise`\<`undefined` \| [`JupiterTokenData`](../interfaces/JupiterTokenData.md)\>

#### Parameters

##### ticker

`string`

#### Returns

`Promise`\<`undefined` \| [`JupiterTokenData`](../interfaces/JupiterTokenData.md)\>

#### Defined in

[agent/index.ts:127](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L127)

***

### launchPumpFunToken()

> **launchPumpFunToken**(`tokenName`, `tokenTicker`, `description`, `imageUrl`, `options`?): `Promise`\<\{ `signature`: `string`; `mint`: `string`; `metadataUri`: `any`; \}\>

#### Parameters

##### tokenName

`string`

##### tokenTicker

`string`

##### description

`string`

##### imageUrl

`string`

##### options?

[`PumpFunTokenOptions`](../interfaces/PumpFunTokenOptions.md)

#### Returns

`Promise`\<\{ `signature`: `string`; `mint`: `string`; `metadataUri`: `any`; \}\>

#### Defined in

[agent/index.ts:131](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L131)

***

### stake()

> **stake**(`amount`): `Promise`\<`string`\>

#### Parameters

##### amount

`number`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:148](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L148)

***

### sendCompressedAirdrop()

> **sendCompressedAirdrop**(`mintAddress`, `amount`, `decimals`, `recipients`, `priorityFeeInLamports`, `shouldLog`): `Promise`\<`string`[]\>

#### Parameters

##### mintAddress

`string`

##### amount

`number`

##### decimals

`number`

##### recipients

`string`[]

##### priorityFeeInLamports

`number`

##### shouldLog

`boolean`

#### Returns

`Promise`\<`string`[]\>

#### Defined in

[agent/index.ts:152](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L152)

***

### createOrcaSingleSidedWhirlpool()

> **createOrcaSingleSidedWhirlpool**(`depositTokenAmount`, `depositTokenMint`, `otherTokenMint`, `initialPrice`, `maxPrice`, `feeTier`): `Promise`\<`string`\>

#### Parameters

##### depositTokenAmount

`BN`

##### depositTokenMint

`PublicKey`

##### otherTokenMint

`PublicKey`

##### initialPrice

`Decimal`

##### maxPrice

`Decimal`

##### feeTier

`0.01` | `0.02` | `0.04` | `0.05` | `0.16` | `0.3` | `0.65` | `1` | `2`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:171](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L171)

***

### raydiumCreateAmmV4()

> **raydiumCreateAmmV4**(`marketId`, `baseAmount`, `quoteAmount`, `startTime`): `Promise`\<`string`\>

#### Parameters

##### marketId

`PublicKey`

##### baseAmount

`BN`

##### quoteAmount

`BN`

##### startTime

`BN`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:190](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L190)

***

### raydiumCreateClmm()

> **raydiumCreateClmm**(`mint1`, `mint2`, `configId`, `initialPrice`, `startTime`): `Promise`\<`string`\>

#### Parameters

##### mint1

`PublicKey`

##### mint2

`PublicKey`

##### configId

`PublicKey`

##### initialPrice

`Decimal`

##### startTime

`BN`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:209](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L209)

***

### raydiumCreateCpmm()

> **raydiumCreateCpmm**(`mint1`, `mint2`, `configId`, `mintAAmount`, `mintBAmount`, `startTime`): `Promise`\<`string`\>

#### Parameters

##### mint1

`PublicKey`

##### mint2

`PublicKey`

##### configId

`PublicKey`

##### mintAAmount

`BN`

##### mintBAmount

`BN`

##### startTime

`BN`

#### Returns

`Promise`\<`string`\>

#### Defined in

[agent/index.ts:231](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L231)

***

### openbookCreateMarket()

> **openbookCreateMarket**(`baseMint`, `quoteMint`, `lotSize`, `tickSize`): `Promise`\<`string`[]\>

#### Parameters

##### baseMint

`PublicKey`

##### quoteMint

`PublicKey`

##### lotSize

`number` = `1`

##### tickSize

`number` = `0.01`

#### Returns

`Promise`\<`string`[]\>

#### Defined in

[agent/index.ts:257](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L257)

## Properties

### connection

> **connection**: `Connection`

Solana RPC connection

#### Defined in

[agent/index.ts:43](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L43)

***

### wallet

> **wallet**: `Keypair`

Wallet keypair for signing transactions

#### Defined in

[agent/index.ts:44](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L44)

***

### wallet\_address

> **wallet\_address**: `PublicKey`

Public key of the wallet

#### Defined in

[agent/index.ts:45](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L45)

***

### openai\_api\_key

> **openai\_api\_key**: `string`

#### Defined in

[agent/index.ts:46](https://github.com/thearyanag/solana-agent-kit/blob/c88d8d8c341dc6e1d1c45e94402cf4241851da80/src/agent/index.ts#L46)