# Flood

Beanstalk sells newly minted Beans on Curve during long run increases in demand for Beans when [increasing the Bean supply](overview.md#bean-supply) and [lowering the Temperature](temperature.md) have not crossed the Bean price over its peg.

At the beginning of a [Season](../farm/sun.md), if it is currently raining (the previous Season P > 1), and the [Pod Rate](overview.md#debt-level) is less than 5%, the Farm is Oversaturated. If it is Oversaturated for 4 consecutive Seasons or more, each Season in which it continues to be Oversaturated, it Floods.

At the beginning of a Season where it Floods, Beanstalk returns the Bean price to its peg by minting additional Beans and selling them directly on Curve. Proceeds from the sale in the form of 3CRV are distributed to [Stalkholders](../farm/silo.md#the-stalk-system) at the beginning of a Season in proportion to their Stalk ownership when the Farm started to be Oversaturated. Also, at the beginning of the Flood, all [Pods](../farm/field.md#pods) that were minted before it started to be Oversaturated Ripen and become Harvestable.
