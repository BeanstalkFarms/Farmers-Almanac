# Contracts

### Contracts

| Contract                                                                                     | Address                                                                                                               |
| -------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Beanstalk                                                                                    | [0xC1E088fC1323b20BCBee9bd1B9fC9546db5624C5](https://etherscan.io/address/0xC1E088fC1323b20BCBee9bd1B9fC9546db5624C5) |
| Bean ERC-20 token                                                                            | [0xBEA0000029AD1c77D3d5D23Ba2D8893dB9d1Efab](https://etherscan.io/address/0xBEA0000029AD1c77D3d5D23Ba2D8893dB9d1Efab) |
| BEAN:3CRV LP token ([Curve pool](https://curve.fi/#/ethereum/pools/factory-v2-152/deposit/)) | [0xc9C32cd16Bf7eFB85Ff14e0c8603cc90F6F2eE49](https://etherscan.io/address/0xc9C32cd16Bf7eFB85Ff14e0c8603cc90F6F2eE49) |
| Unripe Bean ERC-20 token                                                                     | [0x1BEA0050E63e05FBb5D8BA2f10cf5800B6224449](https://etherscan.io/address/0x1BEA0050E63e05FBb5D8BA2f10cf5800B6224449) |
| Unripe BEAN:3CRV LP ERC-20 token                                                             | [0x1BEA3CcD22F4EBd3d37d731BA31Eeca95713716D](https://etherscan.io/address/0x1BEA3CcD22F4EBd3d37d731BA31Eeca95713716D) |
| Fertilizer ERC-1155 token                                                                    | [0x402c84de2ce49af88f5e2ef3710ff89bfed36cb6](https://etherscan.io/address/0x402c84de2ce49af88f5e2ef3710ff89bfed36cb6) |
| Fertilizer Admin                                                                             | [0xfECB01359263C12Aa9eD838F878A596F0064aa6e](https://etherscan.io/address/0xfECB01359263C12Aa9eD838F878A596F0064aa6e) |
| Fertilizer Implementation                                                                    | [0x39cdAf9Dc6057Fd7Ae81Aaed64D7A062aAf452fD](https://etherscan.io/address/0x39cdAf9Dc6057Fd7Ae81Aaed64D7A062aAf452fD) |

### Diamond

Beanstalk is a [ERC-2535 Diamond](https://bean.money/blog/beanstalk-eip-2535). The following are the different facets Beanstalk uses. You can explore the facets on [Louper](https://louper.dev/diamond/0xC1E088fC1323b20BCBee9bd1B9fC9546db5624C5?network=mainnet), an interface for inspecting Ethereum Diamonds.

| Contract                        | Address                                                                                                                                                                                                                                                                                     |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sun** > SeasonFacet           | [0x0cEFF1129091A0ffa97cC58d4D160F9676866a24](https://etherscan.io/address/0x0cEFF1129091A0ffa97cC58d4D160F9676866a24)                                                                                                                                                                       |
| **Silo** > SiloFacet            | <ul><li><a href="https://etherscan.io/address/0xf73db3fb33c7070db0f0ae4a76872251dca15e97">0xf73db3fb33c7070db0f0ae4a76872251dca15e97</a></li><li><a href="https://etherscan.io/address/0xeD7bE52F59B4aA0c36b046E5c1F14Df62aaE79D6">0xeD7bE52F59B4aA0c36b046E5c1F14Df62aaE79D6</a></li></ul> |
| **Silo** > BDVFacet             | [0xc17ED2e41242063DB6b939f5601bA01374b9D44a](https://etherscan.io/address/0xc17ED2e41242063DB6b939f5601bA01374b9D44a)                                                                                                                                                                       |
| **Silo** > WhitelistFacet       | [0xAeA0e6e011106968ADc7943579C829E49EFddaD0](https://etherscan.io/address/0xAeA0e6e011106968ADc7943579C829E49EFddaD0)                                                                                                                                                                       |
| **Silo** > ConvertFacet         | [0xc2e90acba1dc5ec1b852592390f479012eb304c2](https://etherscan.io/address/0xc2e90acba1dc5ec1b852592390f479012eb304c2)                                                                                                                                                                       |
| **Field** > FieldFacet          | [0x79801F5cB2592Dd2173482198385e62870a0eAe2](https://etherscan.io/address/0x79801F5cB2592Dd2173482198385e62870a0eAe2)                                                                                                                                                                       |
| **Field** > FundraiserFacet     | [0x538C76976eF45b8cA5c12662a86034434bFC7a8E](https://etherscan.io/address/0x538C76976eF45b8cA5c12662a86034434bFC7a8E)                                                                                                                                                                       |
| **Barn** > FertilizerFacet      | [0xFC7Ed192a24FaB3093c8747c3DDBe6Cacd335B6C](https://etherscan.io/address/0xFC7Ed192a24FaB3093c8747c3DDBe6Cacd335B6C)                                                                                                                                                                       |
| **Barn** > UnripeFacet          | [0x261b3ae660504537fbfe15b6c1c664976344eb0a](https://etherscan.io/address/0x261b3ae660504537fbfe15b6c1c664976344eb0a)                                                                                                                                                                       |
| **Market** > MarketplaceFacet   | [0x0c9f436fbef08914c1c68fe04bd573de6e327776](https://etherscan.io/address/0x0c9f436fbef08914c1c68fe04bd573de6e327776)                                                                                                                                                                       |
| **Farm** > FarmFacet            | [0x855D37a6C3868Aa4e8F2e1a80965D08B3f10d292](https://etherscan.io/address/0x855D37a6C3868Aa4e8F2e1a80965D08B3f10d292)                                                                                                                                                                       |
| **Farm** > DepotFacet           | [0xD812fDfB45BC4D05884Eb270f7DdFaac71D60F78](https://etherscan.io/address/0xD812fDfB45BC4D05884Eb270f7DdFaac71D60F78)                                                                                                                                                                       |
| **Farm** > TokenFacet           | <ul><li><a href="https://etherscan.io/address/0x8d00ef08775872374a327355fe0fdbdece1106cf">0x8d00ef08775872374a327355fe0fdbdece1106cf</a></li><li><a href="https://etherscan.io/address/0x50eb0085c31dfa8cf86ca16def77520e762ead4a">0x50eb0085c31dfa8cf86ca16def77520e762ead4a</a></li></ul> |
| **Farm** > TokenSupportFacet    | [0x5e15667Bf3EEeE15889F7A2D1BB423490afCb527](https://etherscan.io/address/0x5e15667Bf3EEeE15889F7A2D1BB423490afCb527#code)                                                                                                                                                                  |
| **Farm** > CurveFacet           | [0xd231498144c5b53b65b782343CDFB366472c7bf7](https://etherscan.io/address/0xd231498144c5b53b65b782343CDFB366472c7bf7)                                                                                                                                                                       |
| **Diamond** > DiamondCutFacet   | [0xDFeFF7592915bea8D040499E961E332BD453C249](https://etherscan.io/address/0xDFeFF7592915bea8D040499E961E332BD453C249)                                                                                                                                                                       |
| **Diamond** > DiamondLoupeFacet | [0xB51D5C699B749E0382e257244610039dDB272Da0](https://etherscan.io/address/0xB51D5C699B749E0382e257244610039dDB272Da0)                                                                                                                                                                       |
| **Diamond** > OwnershipFacet    | [0x5D45283Ff53aabDb93693095039b489Af8b18Cf7](https://etherscan.io/address/0x5D45283Ff53aabDb93693095039b489Af8b18Cf7)                                                                                                                                                                       |
| **Diamond** > PauseFacet        | [0xeab4398f62194948cB25F45fEE4C46Fae2e91229](https://etherscan.io/address/0xeab4398f62194948cB25F45fEE4C46Fae2e91229)                                                                                                                                                                       |

### Multisigs

| Contract                                                                                    | Address                                                                                                                                 |
| ------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| [Beanstalk Community Multisig (BCM)](../governance/beanstalk/bcm-dashboard.md)              | [0xa9bA2C40b263843C04d344727b954A545c81D043](https://app.safe.global/eth:0xa9bA2C40b263843C04d344727b954A545c81D043/transactions/queue) |
| [Beanstalk Farms Multisig (BFM)](../governance/beanstalk-farms/bfm-dashboard.md)            | [0x21DE18B6A8f78eDe6D16C50A167f6B222DC08DF7](https://app.safe.global/eth:0x21DE18B6A8f78eDe6D16C50A167f6B222DC08DF7/transactions/queue) |
| [Bean Sprout Multisig (BSM)](../governance/bean-sprout/bsm-dashboard.md)                    | [0xb7ab3f0667eFF5e2299d39C23Aa0C956e8982235](https://app.safe.global/eth:0xb7ab3f0667eFF5e2299d39C23Aa0C956e8982235/transactions/queue) |
| [Beanstalk Farms Subgraph Multisig (BFSM)](../governance/beanstalk-farms/bfsm-dashboard.md) | [0xe1c3aEf912eCBF766155100038994c3FE880dB02](https://app.safe.global/eth:0xe1c3aEf912eCBF766155100038994c3FE880dB02/transactions/queue) |

### Ecosystem

| Contract                                                             | Address                                                                                                               |
| -------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| [Root Token](https://roottoken.org/) (Mainnet)                       | [0x77700005bea4de0a78b956517f099260c2ca9a26](https://etherscan.io/token/0x77700005bea4de0a78b956517f099260c2ca9a26)   |
| [Root Token](https://roottoken.org/) (Arbitrum)                      | [0x40A9a378204b005bD3496f8eeFCce9136071B40f](https://arbiscan.io/token/0x40a9a378204b005bd3496f8eefcce9136071b40f)    |
| [Pipeline](https://evmpipeline.org/)                                 | [0xb1bE0000bFdcDDc92A8290202830C4Ef689dCeaa](https://etherscan.io/address/0xb1bE0000bFdcDDc92A8290202830C4Ef689dCeaa) |
| [Depot](https://evmpipeline.org/)                                    | [0xDEb0f000082fD56C10f449d4f8497682494da84D](https://etherscan.io/address/0xDEb0f000082fD56C10f449d4f8497682494da84D) |
| [BeaNFT Genesis](https://opensea.io/collection/beanft-genesis)       | [0xa755A670Aaf1FeCeF2bea56115E65e03F7722A79](https://etherscan.io/address/0xa755A670Aaf1FeCeF2bea56115E65e03F7722A79) |
| [BeaNFT Winter](https://opensea.io/collection/beanft-winter)         | [0x459895483556dad32526efa461f75e33e458d9e9](https://etherscan.io/address/0x459895483556dad32526efa461f75e33e458d9e9) |
| [BeaNFT Barn Raise](https://opensea.io/collection/beanft-barn-raise) | [0xa969bb19b1d35582ded7ea869cecd60a3bd5d1e8](https://etherscan.io/address/0xa969bb19b1d35582ded7ea869cecd60a3bd5d1e8) |

### Misc. <a href="#misc" id="misc"></a>

| Contract                | Description                                                                           | Address                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Bean Price Contract     | Helper contract for getting the Bean price                                            | [0xF2C2b7eabcB353bF6f2128a7f8e1e32Eeb112530](https://etherscan.io/address/0xF2C2b7eabcB353bF6f2128a7f8e1e32Eeb112530) |
| InitMint Contract       | Used for minting Beans as part of BIPs                                                | [0x077495925c17230E5e8951443d547ECdbB4925Bb](https://etherscan.io/address/0x077495925c17230E5e8951443d547ECdbB4925Bb) |
| Ethical Return Contract | Deployed per [BOP-2](https://arweave.net/aOAzXi2IzO5Ts1OrXYVrAjXbBavbKg07k7k56gIXtl4) | [0xf96681781cd426d25dd3ee45fe77ba5763ae24e4](https://etherscan.io/address/0xf96681781cd426d25dd3ee45fe77ba5763ae24e4) |

### Pre-Exploit Contracts

{% hint style="danger" %}
The addresses below refer to the exploited Bean token (0xDC59). Do not buy these tokens. A new Bean token was issued at Replant—you can find it at the top of this page.
{% endhint %}

| Contract                                                                                                 | Address                                                                                                               |
| -------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| [Bean ERC-20 Token](https://etherscan.io/address/0xDC59ac4FeFa32293A95889Dc396682858d52e5Db)             | [0xDC59ac4FeFa32293A95889Dc396682858d52e5Db](https://etherscan.io/address/0xDC59ac4FeFa32293A95889Dc396682858d52e5Db) |
| [BEAN:ETH Uniswap V2 Pair](https://v2.info.uniswap.org/token/0xdc59ac4fefa32293a95889dc396682858d52e5db) | [0x87898263B6C5BABe34b4ec53F22d98430b91e371](https://etherscan.io/address/0x87898263B6C5BABe34b4ec53F22d98430b91e371) |
| [BEAN:3CRV Metapool](https://curve.fi/#/ethereum/pools/factory-v2-81/deposit/)                           | [0x3a70DfA7d2262988064A2D051dd47521E43c9BdD](https://etherscan.io/address/0x3a70DfA7d2262988064A2D051dd47521E43c9BdD) |
| [BEAN:LUSD Plain Pool](https://curve.fi/#/ethereum/pools/factory-v2-103/deposit/)                        | [0xD652c40fBb3f06d6B58Cb9aa9CFF063eE63d465D](https://etherscan.io/address/0xD652c40fBb3f06d6B58Cb9aa9CFF063eE63d465D) |
