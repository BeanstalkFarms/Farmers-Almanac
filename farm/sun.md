# Sun

The Beanstalk peg maintenance mechanism requires a protocol-native timekeeping mechanism and regular code execution on Ethereum. The Sun keeps time on the Farm in Seasons and incentivizes cost-efficient and timely calling of the sunrise() function.

Beanstalk adjusts itself to return the Bean price to its value peg at the beginning of every Season. Each Season is \~1 hour long. The first Season began when Beanstalk was deployed on August 6, 2021.

The exact beginning of each Season may vary as Seasons do not begin until the sunrise() function has been called through an Ethereum transaction. The first transaction that successfully calls the sunrise() function after the top of each hour UTC begins a new Season. Beanstalk only accepts one sunrise() function call per Season.

Beanstalk covers the cost of calling the sunrise() function by awarding the sender of an accepted sunrise() function call with newly minted Beans. To encourage regular sunrise() function calls even during periods of congestion on Ethereum while minimizing cost, the award starts at 100 Beans and compounds 1% every additional second that elapses for 300 seconds.

Upon acceptance of the sunrise() call, the Sun:

1. Increments the Season number;
2. Calculates deltaB, the sum of the time and liquidity weighted average shortage or excess Beans in the liquidity pools on the Oracle Whitelist;
3. [Changes the Temperature](../peg-maintenance/temperature.md) if necessary and checks for [Flood](../peg-maintenance/flood.md);
4. Sets the [new Soil supply](../peg-maintenance/overview.md#soil-supply);
5. [Mints Beans](../peg-maintenance/overview.md#bean-supply) if necessary; and
6. Awards Beans to the address that successfully called the sunrise() function.

### Oracle Whitelist

The following liquidity pools are whitelisted for inclusion in the calculation of [deltaB](../additional-resources/glossary.md#deltab):

| Pool name                                      | Pool address                                                                                                          |
| ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| [BEAN:3CRV pool](https://curve.fi/factory/152) | [0xc9C32cd16Bf7eFB85Ff14e0c8603cc90F6F2eE49](https://etherscan.io/address/0xc9C32cd16Bf7eFB85Ff14e0c8603cc90F6F2eE49) |

