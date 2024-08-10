# Overview

Beanstalk faces the fundamental limitation that it cannot fix the Bean price at its value peg, but instead must encourage widespread participation in peg maintenance through protocol-native financial incentives. Stability is a function of how regularly the price of a Bean oscillates across its peg and the magnitude of price deviations from it.

Beanstalk has four direct peg maintenance tools available:

1. Increase the [Bean supply](overview.md#bean-supply);
2. Change the [Soil supply](overview.md#soil-supply);
3. Change the [Temperature](temperature.md);&#x20;
4. Change the [Bean to Max LP Seed Ratio](bean-to-max-lp-seed-ratio.md); and
5. Sell Beans ([Flood](flood.md)).

At the beginning of every [Season](../farm/sun.md), Beanstalk evaluates its position (i.e., price, debt level and liquidity level) and current state (i.e., direction and acceleration) with respect to ideal equilibrium, and dynamically adjusts the Bean supply, Soil supply, Temperature and Bean to Max LP Seed Ratio to move closer to ideal equilibrium.

[Conversions](convert.md) within the [Silo](../farm/silo/) between Bean and LP Deposits serve a major role in peg maintenance.

### **Ideal Equilibrium**

Beanstalk is in ideal equilibrium when the Bean price and the Beanstalk debt level are both stable at their optimal levels. In practice, this requires that four conditions are met:

1. The price of Bean is regularly oscillating around the peg;
2. The Beanstalk debt level is optimal;
3. The Beanstalk liquidity level is optimal; and
4. Demand for Soil is steady.

In order to return to ideal equilibrium, Beanstalk affects the supply of and demand for Beans in response to the Bean price, the Beanstalk debt level, the Beanstalk liquidity level and changing demand for Soil. It does so by adjusting the Bean supply, Soil supply, Temperature and Bean to Max LP Seed Ratio.

Bean supply increases primarily affect the Bean price. Soil supply impacts the Bean supply and the debt level. Temperature changes primarily affect demand for Soil. Bean to Max LP Seed Ratio changes primarily affect demand for Conversions.

In order to make the proper adjustments, Beanstalk reassesses the states of both the Bean and Soil markets at the beginning of each Season.

In practice, maintaining ideal equilibrium is impossible. Deviations from ideal equilibrium are normal and expected. As Beanstalk grows, the durations and magnitudes of deviations are expected to decrease.

### **Decentralized Price Oracle**

Beanstalk's core objective is to oscillate the price of Bean above and below its dollar peg. To do this, Beanstalk must be able to reliably measure the price of a dollar on-chain without trusting a centralized third-party to provide it. A robust, decentralized stablecoin requires a tamper-proof, manipulation-resistant and decentralized price oracle.

The [Multi Flow Pump](https://basin.exchange/multi-flow-pump.pdf) attached to whitelisted Wells is the first Ethereum-native oracle for Ethereum-native data that offers inter-block MEV manipulation resistance in a post-Merge environment. Using Multi Flow, Beanstalk can calculate an inter-block MEV manipulation resistant BEAN:ETH price.

#### P > Q

Price spikes makes Beans less attractive to borrow and price other assets against. Beanstalk should be more aggressive in returning the price to peg when the price reaches a particular threshold above $1. Currently Q is set to $1.05, a reasonable threshold while the Bean supply is small. It does not seem that there is a natural opposite to Q when P < 1.

***

In practice, Beanstalk does not calculate the price of 1 Bean. Instead, at the beginning of each Season, Beanstalk calculates the sum of the time weighted average shortages or excesses of Beans across the liquidity pools on the [Minting Whitelist](../farm/sun.md#minting-whitelist) over the previous Season (i.e., [deltaB](../protocol/glossary.md#deltab)).

### **Debt Level**

The Pod Rate represents the Beanstalk debt level relative to the Bean supply. The Pod Rate is often used as a proxy for Beanstalk’s health. If the Bean supply is 1000 and there are 2000 [Pods](../farm/field.md#pods), the Pod Rate is 200%.

Beanstalk defines a handful of Pod Rate ranges that it uses as an input to determine how to change the Temperature:

* Excessively low debt: Pod Rate < 5%
* Reasonably low debt: 5% ≤ Pod Rate < 15%
* Optimal level of debt: Pod Rate = 15%
* Reasonably high debt: 15% < Pod Rate ≤ 25%
* Excessively high debt: Pod Rate > 25%

### Liquidity Level

The Liquidity to Supply Ratio (L2SR) represents the Beanstalk liquidity level relative to the Bean supply. The L2SR is a useful indicator of Beanstalk's health.

In the context of the L2SR, liquidity is defined as the sum of the USD values of the non-Bean assets in each whitelisted liquidity pool multiplied by their respective liquidity weights. Supply is defined as the total Bean supply minus Locked Beans (defined below).

Beanstalk can be in 4 different states in relation to its L2SR:

* Excessively low liquidity: L2SR < 12%;
* Reasonably low liquidity: 12% ≤ L2SR < 40%;
* Optimal level of liquidity: L2SR = 40%
* Reasonably high liquidity: 40% < L2SR ≤ 80%; or
* Excessively high liquidity: L2SR > 80%.

#### Locked Beans

Due to the Barn Raise and the associated Beans underlying Unripe assets, the number of tradable Beans does not equal the total Bean supply. As of May 2024, \~0.224 Beans underlying each Unripe Bean, but holders can only redeem \~0.0102 Beans per Unripe Bean. Thus, \~0.2138 Beans Per Unripe are considered not tradable.

By excluding Locked Beans from the Bean supply in the L2SR calculation, Beanstalk can determine its health in terms of liquidity based on only the number of Beans that can reasonably be sold. This is preferable over factoring in Beans that cannot be sold.

### **Bean Supply**

At the beginning of each Season, Beanstalk increases the Bean supply by deltaB if there was a time weighted average shortages of Beans across the pools in the [Minting Whitelist](../farm/sun.md#minting-whitelist) over the previous Season, subject to the cap in [EBIP-2](https://arweave.net/3GyVJLO0YqhwJHWZeiykWYu4G6SsfcV0alP-1DfMygk). Essentially, Beanstalk will mint the number of Beans that need to be sold in the pools on the Minting Whitelist to return the Bean price to a dollar.

[Stalkholders](../farm/silo/#the-stalk-system), Pod holders, and [Active Fertilizer](../farm/barn.md#fertilizer) holders receive 1/3 of new Bean mints each while there are [Unfertilized Sprouts](../farm/barn.md#fertilizer) outstanding. If there is no Active Fertilizer, Stalkholders and Pod holders receive 1/2 of new Bean mints each. If there are neither Pods nor Active Fertilizer, Stalkholders receive 100% of new Bean mints.

### **Soil Supply**

When P < 1 over the previous Season (_i.e._, deltaB < 0), the Soil supply is equal to deltaB, the sum of the time weighted average excesses of Beans across the liquidity pools on the [Minting Whitelist](../farm/sun.md#minting-whitelist) over the previous Season, subject to the cap in EBIP-2.

When P ≥ 1 over the previous Season (_i.e._, deltaB ≥ 0), Beanstalk is still willing to issue debt in order to measure changing demand for [Soil](../farm/field.md#soil). The Soil supply is based on the number of Pods that Ripen and become Harvestable at the beginning of the Season, the Temperature (see [Morning](temperature.md#morning) section), and the Beanstalk debt level. A greater number of Pods Ripening increases the Soil supply. Higher Temperature and debt level decrease the Soil supply. See [Section 8.11 in the whitepaper](https://bean.money/beanstalk.pdf#subsection.8.11) for complete formulas.
