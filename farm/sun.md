# Sun

The Beanstalk peg maintenance mechanism requires a protocol-native timekeeping mechanism and regular code execution on Arbitrum. The Sun keeps time on the Farm in Seasons and incentivizes cost-efficient and timely calling of the `gm` function.

Beanstalk adjusts itself to return the Bean price to its value peg at the beginning of every Season. Each Season is \~1 hour long. The first Season began when Beanstalk was deployed on August 6, 2021 (initially on Ethereum).

The exact beginning of each Season may vary as Seasons do not begin until the `gm` function has been called through an Arbitrum transaction. The first transaction that successfully calls the `gm` function after the top of each hour UTC begins a new Season. Beanstalk only accepts one `gm` function call per Season.

Beanstalk covers the cost of calling the `gm` function by awarding the sender of an accepted `gm` function call with newly minted Beans. To encourage regular `gm` function calls even during periods of congestion on Arbitrum while minimizing cost, the award for successfully calling the `gm` function starts at 1 Bean and compounds 1.0201% every additional 2 seconds for 300 seconds.

Upon acceptance of the `gm` call, the Sun:

1. Increments the Season number;
2. Calculates deltaB, the sum of the time-weighted average shortages or excesses Beans across liquidity pools on the [Minting Whitelist](../protocol/glossary.md#minting-whitelist);
3. [Changes the Maximum Temperature](../peg-maintenance/temperature.md) if necessary and checks for [Flood](../peg-maintenance/flood.md);
4. Changes the [Crop Ratio](../peg-maintenance/crop-ratio.md) (and updates the Gauge Points of each whitelisted asset);
5. Sets the initial[ Soil supply](../peg-maintenance/overview.md#soil-supply);
6. [Mints Beans](../peg-maintenance/overview.md#bean-supply) if necessary; and
7. Awards Beans to the address that successfully called the `gm` function.

### Minting Whitelist

To be included in the calculation of [deltaB](../protocol/glossary.md#deltab), a liquidity pool must be on the Minting Whitelist.

Additional liquidity pools may be added to the Minting Whitelist via [Beanstalk governance](../governance/beanstalk/). In order for a liquidity pool to be added to the Minting Whitelist, Beanstalk requires:

1. The pool address; and
2. A function to calculate the liquidity and time weighted average shortage or excess of Beans in the pool.

#### Current Minting Whitelist

| Name             | Address                                                                                                              |
| ---------------- | -------------------------------------------------------------------------------------------------------------------- |
| BEAN:WETH Well   | [0xBeA00Aa8130aCaD047E137ec68693C005f8736Ce](https://arbiscan.io/address/0xBeA00Aa8130aCaD047E137ec68693C005f8736Ce) |
| BEAN:wstETH Well | [0xBEa00BbE8b5da39a3F57824a1a13Ec2a8848D74F](https://arbiscan.io/address/0xBEa00BbE8b5da39a3F57824a1a13Ec2a8848D74F) |
| BEAN:weETH Well  | [0xBeA00Cc9F93E9a8aC0DFdfF2D64Ba38eb9C2e48c](https://arbiscan.io/address/0xBeA00Cc9F93E9a8aC0DFdfF2D64Ba38eb9C2e48c) |
| BEAN:WBTC Well   | [0xBea00DDe4b34ACDcB1a30442bD2B39CA8Be1b09c](https://arbiscan.io/address/0xBea00DDe4b34ACDcB1a30442bD2B39CA8Be1b09c) |
| BEAN:USDC Well   | [0xBea00ee04D8289aEd04f92EA122a96dC76A91bd7](https://arbiscan.io/address/0xBea00ee04D8289aEd04f92EA122a96dC76A91bd7) |
| BEAN:USDT Well   | [0xbEA00fF437ca7E8354B174339643B4d1814bED33](https://arbiscan.io/address/0xbEA00fF437ca7E8354B174339643B4d1814bED33) |
