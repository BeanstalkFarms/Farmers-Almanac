# Sun

The Beanstalk peg maintenance mechanism requires a protocol-native timekeeping mechanism and regular code execution on Ethereum. The Sun keeps time on the Farm in Seasons and incentivizes cost-efficient and timely calling of the `gm` function.

Beanstalk adjusts itself to return the Bean price to its value peg at the beginning of every Season. Each Season is \~1 hour long. The first Season began when Beanstalk was deployed on August 6, 2021.

The exact beginning of each Season may vary as Seasons do not begin until the `gm` function has been called through an Ethereum transaction. The first transaction that successfully calls the `gm` function after the top of each hour UTC begins a new Season. Beanstalk only accepts one `gm` function call per Season.

Beanstalk covers the cost of calling the `gm` function by awarding the sender of an accepted `gm` function call with newly minted Beans. To encourage regular `gm` function calls even during periods of congestion on Ethereum while minimizing cost, the award is based on an approximation of the cost to call the `gm` function in Beans in the current block and compounds 1% every additional second that elapses for 300 seconds (see [Section 4 of the whitepaper](https://bean.money/beanstalk.pdf#section.4) for complete formulas).

Upon acceptance of the `gm` call, the Sun:

1. Increments the Season number;
2. Calculates deltaB, the sum of the time and liquidity weighted average shortage or excess Beans across liquidity pools on the [Oracle Whitelist](sun.md#oracle-whitelist);
3. [Changes the Maximum Temperature](../peg-maintenance/temperature.md) if necessary and checks for [Flood](../peg-maintenance/flood.md);
4. Sets the initial[ Soil supply](../peg-maintenance/overview.md#soil-supply);
5. [Mints Beans](../peg-maintenance/overview.md#bean-supply) if necessary; and
6. Awards Beans to the address that successfully called the `gm` function.

### Oracle Whitelist

To be included in the calculation of [deltaB](../protocol/glossary.md#deltab), a liquidity pool must be on the Oracle Whitelist.

Additional liquidity pools may be added to the Oracle Whitelist via [Beanstalk governance](broken-reference/). In order for a liquidity pool to be added to the Oracle Whitelist, Beanstalk requires:

1. The pool address; and
2. A function to calculate the liquidity and time weighted average shortage or excess of Beans in the pool (see [Section 14.6 of the whitepaper](https://bean.money/beanstalk.pdf#subsection.14.6) for complete formulas).

#### Current Oracle Whitelist

| Name                                           | Address                                                                                                               |
| ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| [BEAN:3CRV pool](https://curve.fi/factory/152) | [0xc9C32cd16Bf7eFB85Ff14e0c8603cc90F6F2eE49](https://etherscan.io/address/0xc9C32cd16Bf7eFB85Ff14e0c8603cc90F6F2eE49) |
