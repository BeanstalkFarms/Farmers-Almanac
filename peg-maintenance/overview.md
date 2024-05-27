# Overview

{% hint style="info" %}
This page has not yet been updated to account for [BIP-45: Seed Gauge System](https://github.com/BeanstalkFarms/Beanstalk/pull/722).
{% endhint %}

Beanstalk faces the fundamental limitation that it cannot fix the Bean price at its value peg, but instead must encourage widespread participation in peg maintenance through protocol-native financial incentives. Stability is a function of how regularly the price of a Bean oscillates across its peg and the magnitude of price deviations from it.

Beanstalk has four direct peg maintenance tools available:

1. Increase the [Bean supply](overview.md#bean-supply);
2. Change the [Soil supply](overview.md#soil-supply);
3. Change the [Temperature](temperature.md); and
4. Sell Beans ([Flood](flood.md)).

At the beginning of every [Season](../farm/sun.md), Beanstalk evaluates its position (i.e., price and debt level) and current state (i.e., direction and acceleration) with respect to ideal equilibrium, and dynamically adjusts the Bean supply, Soil supply and Temperature to move closer to ideal equilibrium.

[Conversions](convert.md) within the [Silo](../farm/silo.md) between Bean and LP Deposits serve a major role in peg maintenance.

### **Ideal Equilibrium**

Beanstalk is in ideal equilibrium when the Bean price and the Beanstalk debt level are both stable at their optimal levels. In practice, this requires that three conditions are met:

1. The price of Bean is regularly oscillating around the peg;
2. The Beanstalk debt level is optimal; and
3. Demand for Soil is steady.

In order to return to ideal equilibrium, Beanstalk affects the supply of and demand for Beans in response to the Bean price, the Beanstalk debt level and changing demand for Soil. It does so by adjusting the Bean supply, Soil supply and Temperature.

Bean supply increases primarily affect the Bean price. Soil supply impacts the Bean supply and the debt level. Temperature changes primarily affect demand for Soil.

In order to make the proper adjustments, Beanstalk reassesses the states of both the Bean and Soil markets at the beginning of each Season.

In practice, maintaining ideal equilibrium is impossible. Deviations from ideal equilibrium are normal and expected. As Beanstalk grows, the durations and magnitudes of deviations are expected to decrease.

### **Decentralized Price Oracle**

Beanstalk's core objective is to oscillate the price of Bean above and below its dollar peg. To do this, Beanstalk must be able to reliably measure the price of a dollar on-chain without trusting a centralized third-party to provide it. A robust, decentralized stablecoin requires a tamper-proof, manipulation-resistant and decentralized price oracle.

#### BEAN:ETH Well

Ether is the most decentralized, censorship resistant and liquid asset on the Ethereum network. Beanstalk leverages the [ETH/USD Chainlink data feed](https://data.chain.link/ethereum/mainnet/crypto-usd/eth-usd) and the ETH:USDC and ETH:USDT Uniswap V3 pools for calculating deltaB in the BEAN:ETH Well. Wells are the liquidity pools of [Basin](https://basin.exchange/), a composable EVM-native DEX protocol.

The [Multi Flow Pump](https://basin.exchange/multi-flow-pump.pdf) attached to the BEAN:ETH Well is the first Ethereum-native oracle for Ethereum-native data that offers inter-block MEV manipulation resistance in a post-Merge environment. Using Multi Flow, Beanstalk can calculate an inter-block MEV manipulation resistant BEAN:ETH price.

Uniswap V3 pools are not inter-block MEV manipulation resistant but are on-chain and permissionless. Chainlink data feeds are inter-block MEV manipulation resistant because they are off-chain and permissioned. The ETH/USD data feed is the only Chainlink feed secured by staking. By comparing the ETH/USD Chainlink data feed with the ETH:USDC or ETH:USDT Uniswap V3 pools, Beanstalk can calculate an inter-block MEV manipulation resistant ETH:USD price at the cost of some centralization.

***

In practice, Beanstalk does not calculate the price of 1 Bean. Instead, at the beginning of each Season, Beanstalk calculates the sum of the liquidity and time weighted average shortage or excess of Beans across the liquidity pools on the [Minting Whitelist](../farm/sun.md#minting-whitelist) over the previous Season (i.e., [deltaB](../protocol/glossary.md#deltab)).

### **Debt Level**

The Pod Rate represents the Beanstalk debt level relative to the Bean supply. The Pod Rate is often used as a proxy for Beanstalk’s health. If the Bean supply is 1000 and there are 2000 [Pods](../farm/field.md#pods), the Pod Rate is 200%.

Beanstalk defines a handful of Pod Rate ranges that it uses as an input to determine how to change the Temperature:

* Excessively low debt: Pod Rate < 5%
* Reasonably low debt: 5% ≤ Pod Rate < 15%
* Optimal level of debt: Pod Rate = 15%
* Reasonably high debt: 15% < Pod Rate ≤ 25%
* Excessively high debt: Pod Rate > 25%

### **Bean Supply**

At the beginning of each Season, Beanstalk increases the Bean supply by deltaB if there was a liquidity and time weighted average shortage of Beans across the pools in the [Minting Whitelist](../farm/sun.md#minting-whitelist) over the previous Season, subject to the cap in [EBIP-2](https://arweave.net/3GyVJLO0YqhwJHWZeiykWYu4G6SsfcV0alP-1DfMygk). Essentially, Beanstalk will mint the number of Beans that need to be sold in the pools on the Minting Whitelist to return the Bean price to a dollar.

[Stalkholders](../farm/silo.md#the-stalk-system), Pod holders, and [Active Fertilizer](../farm/barn.md#fertilizer) holders receive 1/3 of new Bean mints each while there are [Unfertilized Sprouts](../farm/barn.md#fertilizer) outstanding. If there is no Active Fertilizer, Stalkholders and Pod holders receive 1/2 of new Bean mints each. If there are neither Pods nor Active Fertilizer, Stalkholders receive 100% of new Bean mints.

### **Soil Supply**

When P < 1 over the previous Season (_i.e._, deltaB < 0), the Soil supply is equal to deltaB, the sum of the liquidity and time weighted average excess of Beans across the liquidity pools on the [Minting Whitelist](../farm/sun.md#minting-whitelist) over the previous Season, subject to the cap in EBIP-2.

When P ≥ 1 over the previous Season (_i.e._, deltaB ≥ 0), Beanstalk is still willing to issue debt in order to measure changing demand for [Soil](../farm/field.md#soil). The Soil supply is based on the number of Pods that Ripen and become Harvestable at the beginning of the Season, the Temperature (see [Morning](temperature.md#morning) section), and the Beanstalk debt level. A greater number of Pods Ripening increases the Soil supply. Higher Temperature and debt level decrease the Soil supply. See [Section 8.11 in the whitepaper](https://bean.money/beanstalk.pdf#subsection.8.11) for complete formulas.
