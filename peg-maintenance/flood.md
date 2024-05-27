# Flood

Beanstalk sells newly minted Beans on the open market during long run increases in demand for Beans when [increasing the Bean supply](overview.md#bean-supply) and [lowering the Maximum Temperature](temperature.md) have not crossed the Bean price over its peg.

At the beginning of a [Season](../farm/sun.md), if it is currently raining (the previous Season P > 1), and the [Pod Rate](overview.md#debt-level) is less than 5%, it Floods at the beginning of the next Season.

At the beginning of a Season during a Flood, Beanstalk returns the Bean price to its peg in each liquidity pool on the Flood Whitelist where the Bean price is above peg by minting additional Beans and selling them directly in the pools. Proceeds from the sale are distributed to [Stalkholders](../farm/silo.md#the-stalk-system) at the beginning of a Season in proportion to their Stalk ownership when the Flood began. Also, at the beginning of the first Season after the Flood began, all [Pods](../farm/field.md#pods) that were minted before it started to Flood Ripen and become Harvestable.

### Flood Whitelist

To be included in a Flood sale, a liquidity pool must be on the Flood Whitelist and the Bean price must be above peg in the pool.&#x20;

Additional liquidity pools may be added to the Flood Whitelist via [Beanstalk governance](../governance/beanstalk/). In order for a liquidity pool to be added to the Flood Whitelist, Beanstalk requires:

1. The pool address; and
2. A function to calculate the shortage of Beans in the pool at the end of the previous Season (see [Section 14.7 of the whitepaper](https://bean.money/beanstalk.pdf#subsection.14.7) for complete formulas).

#### Current Flood Whitelist

| Name                                                                                       | Address                                                                                                               |
| ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| [BEAN:ETH Well](https://basin.exchange/#/wells/0xbea0e11282e2bb5893bece110cf199501e872bad) | [0xBEA0e11282e2bB5893bEcE110cF199501e872bAd](https://etherscan.io/address/0xBEA0e11282e2bB5893bEcE110cF199501e872bAd) |
