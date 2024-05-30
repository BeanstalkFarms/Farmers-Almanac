# Flood

Beanstalk sells newly minted Beans on the open market during long run increases in demand for Beans when [increasing the Bean supply](overview.md#bean-supply), [lowering the Maximum Temperature](temperature.md) and [lowering the Bean to Max LP Seed Ratio](bean-to-max-lp-seed-ratio.md) have not crossed the Bean price over its peg.

At the beginning of a [Season](../farm/sun.md), if it is currently raining (the previous Season P > 1), and the [Pod Rate](overview.md#debt-level) is less than 5%, it Floods at the beginning of the next Season.

At the beginning of a Season during a Flood, Beanstalk returns the Bean price to its peg in each liquidity pool on the Flood Whitelist where the Bean price is above peg by minting additional Beans and selling them directly in the pools. Proceeds from the sale are distributed to [Stalkholders](../farm/silo/#the-stalk-system) at the beginning of a Season in proportion to their Stalk ownership when the Flood began. Also, at the beginning of the first Season after the Flood began, all [Pods](../farm/field.md#pods) that were minted before it started to Flood Ripen and become Harvestable.

After the deployment of [BIP-45](https://bean.money/bip-45), Flood will occur in the whitelisted Well with the most liquidity.
