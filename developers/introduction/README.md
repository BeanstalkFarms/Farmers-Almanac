# Introduction

Beanstalk is a permissionless fiat stablecoin protocol built on Arbitrum.

Beanstalk forms the monetary basis of an Arbitrum-native, rent-free economy facilitated by the seigniorage of its native fiat currency, a stablecoin called Bean.

Beanstalk's primary objective is to incentivize independent market participants to regularly cross the price of 1 Bean across its value peg of $1 in a sustainable fashion. The stability of the Bean price relative to its value peg is a function of the creditworthiness of Beanstalk—Beanstalk attracts lenders when the price of a Bean is below its value peg to remove Beans from the supply and increase their price.

When the Bean price is too high, Beanstalk mints new Beans and distributes them to various ecosystem participants in a deterministic fashion. This inflation is [the positive carry](https://docs.bean.money/almanac/introduction/why-beanstalk#carrying-costs) that the Beanstalk economy is based on.

Beanstalk implements several novel mechanisms including a first-in-first-out (FIFO) [debt model](../../farm/field.md) supplemented by [an on-chain order book](../../farm/toolshed/market.md), [a time-weighted staking structure](../../farm/silo/#the-stalk-system) that increases the opportunity cost of withdrawing the longer an asset stays deposited in the DAO and [a convert mechanism](https://docs.bean.money/almanac/peg-maintenance/convert) that allows participants to perform peg maintenance while those assets are staked.

Beanstalk strives to create product market fit on both a technical and economic level. In order to service an entire ecosystem, Beanstalk needs to provide a cheap, composable and interoperable interface. However, as protocols become more sophisticated and blockspace more crowded, smart contract architecture complexity can quickly become overwhelming.

Beanstalk pioneers a path forward for devising more efficient and complex systems. Beanstalk is implemented in [Solidity v0.8.20](https://docs.soliditylang.org/en/v0.8.20/) for intended use in the [EVM](https://ethereum.org/en/developers/docs/evm/). Beanstalk leverages [EIP-2535](https://eips.ethereum.org/EIPS/eip-2535) to minimize gas costs and complexity.

Beanstalk consists of 2 main contracts:

* Beanstalk - The protocol responsible for peg maintenance implemented as an [EIP-2535](https://eips.ethereum.org/EIPS/eip-2535) multi-facet proxy.
* Bean – The stablecoin implemented as an [ERC-20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/) token.

#### Contracts

Beanstalk is deployed at [0xD1A0060ba708BC4BCD3DA6C37EFa8deDF015FB70](https://arbiscan.io/address/0xD1A0060ba708BC4BCD3DA6C37EFa8deDF015FB70).

Bean is deployed at [0xBEA0005B8599265D41256905A9B3073D397812E4](https://arbiscan.io/address/0xBEA0005B8599265D41256905A9B3073D397812E4).

All relevant contract addresses can be found on the [Contracts](../../protocol/contracts.md) page.
