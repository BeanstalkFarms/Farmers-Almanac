# Flood

Beanstalk sells newly minted Beans on the open market during long run increases in demand for Beans when [increasing the Bean supply](overview.md#bean-supply), [lowering the Maximum Temperature](temperature.md) and [lowering the Crop Ratio](crop-ratio.md) have not crossed the Bean price over its peg.

At the beginning of a [Season](../farm/sun.md), if it is currently Raining (the previous Season P > 1), and the [Pod Rate](overview.md#debt-level) is less than 5%, it Floods at the beginning of the next Season.

At the beginning of a Season during a Flood, Beanstalk Beanstalk mints additional Beans and sells them directly in pools on the Flood Whitelist with the highest shortage of Beans at the end of the previous Season. Liquidity pools can be added to and removed from the Flood Whitelist via [Beanstalk governance](../governance/beanstalk/). Proceeds from the sale are distributed to Stalkholders at the beginning of Season in proportion to their Stalk holdings when it began to Rain. At the beginning of each Season in which it Floods, up to 0.1% of the Bean supply worth of Pods that grew from Beans Sown before it began to Rain Ripen and become Harvestable.

#### Current Flood Whitelist

| Name             | Address                                                                                                              |
| ---------------- | -------------------------------------------------------------------------------------------------------------------- |
| BEAN:WETH Well   | [0xBeA00Aa8130aCaD047E137ec68693C005f8736Ce](https://arbiscan.io/address/0xBeA00Aa8130aCaD047E137ec68693C005f8736Ce) |
| BEAN:wstETH Well | [0xBEa00BbE8b5da39a3F57824a1a13Ec2a8848D74F](https://arbiscan.io/address/0xBEa00BbE8b5da39a3F57824a1a13Ec2a8848D74F) |
| BEAN:weETH Well  | [0xBeA00Cc9F93E9a8aC0DFdfF2D64Ba38eb9C2e48c](https://arbiscan.io/address/0xBeA00Cc9F93E9a8aC0DFdfF2D64Ba38eb9C2e48c) |
| BEAN:WBTC Well   | [0xBea00DDe4b34ACDcB1a30442bD2B39CA8Be1b09c](https://arbiscan.io/address/0xBea00DDe4b34ACDcB1a30442bD2B39CA8Be1b09c) |
| BEAN:USDC Well   | [0xBea00ee04D8289aEd04f92EA122a96dC76A91bd7](https://arbiscan.io/address/0xBea00ee04D8289aEd04f92EA122a96dC76A91bd7) |
| BEAN:USDT Well   | [0xbEA00fF437ca7E8354B174339643B4d1814bED33](https://arbiscan.io/address/0xbEA00fF437ca7E8354B174339643B4d1814bED33) |
