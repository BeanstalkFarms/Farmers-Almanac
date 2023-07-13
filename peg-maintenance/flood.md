# Flood

Beanstalk sells newly minted Beans on Curve during long run increases in demand for Beans when [increasing the Bean supply](overview.md#bean-supply) and [lowering the Maximum Temperature](temperature.md) have not crossed the Bean price over its peg.

At the beginning of a [Season](../farm/sun.md), if it is currently raining (the previous Season P > 1), and the [Pod Rate](overview.md#debt-level) is less than 5%, there is a Flood.

At the beginning of a Season during a Flood, Beanstalk returns the Bean price to its peg by minting additional Beans and selling them directly on Curve. Proceeds from the sale in the form of 3CRV are distributed to [Stalkholders](../farm/silo.md#the-stalk-system) at the beginning of a Season in proportion to their Stalk ownership when the Flood began. Also, at the beginning of the first Season after the Flood began, all [Pods](../farm/field.md#pods) that were minted before it started to Flood Ripen and become Harvestable.
