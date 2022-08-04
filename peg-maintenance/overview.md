# Overview

Beanstalk faces the fundamental limitation that it cannot fix the Bean price at its value peg, but instead must encourage widespread participation in peg maintenance through protocol-native financial incentives. Stability is a function of how regularly the price of a Bean oscillates across its peg and the magnitude of price deviations from it.

Beanstalk has four peg maintenance tools available:

1. Increase the [Bean supply](overview.md#bean-supply);
2. Change the [Soil supply](overview.md#soil-supply);
3. Change the [Temperature](temperature.md); and
4. Sell Beans ([Flood](flood.md)).

At the beginning of every [Season](../farm/sun.md), Beanstalk evaluates its position (i.e., price and debt level) and current state (i.e., direction and acceleration) with respect to ideal equilibrium, and dynamically adjusts the Bean supply, Soil supply and Temperature to move closer to ideal equilibrium.

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

Beanstalk’s core objective is to oscillate the price of Bean above and below its dollar peg. To do this, Beanstalk must be able to reliably measure the price of a dollar on-chain without trusting a centralized third-party to provide it. A robust, decentralized stablecoin requires a tamper-proof, manipulation-resistant and decentralized price oracle.

Beanstalk leverages the 3CRV pool on Curve as its price oracle. Curve is an Ethereum-native decentralized exchange protocol specializing in efficient stablecoin trading. Curve offers continuous trading in any direction by maintaining a liquidity pool of currencies for a 0.04% trading fee.

Owners of the currencies in a liquidity pool on Curve can add liquidity to the pool in exchange for liquidity pool tokens (LP tokens) unique to that liquidity pool. LP token owners receive a portion of trading fees. Price slippage increases when the size of a trade is large relative to the size of the liquidity pool. Pools with greater liquidity serve as more robust price sources.

3CRV is one of the most liquid stablecoin pools in DeFi, consisting of USDC, USDT and DAI. The centralized organizations that control USDC and USDT cannot blacklist 3CRV without destroying the value proposition of their own stablecoins. DAI is a network-native exogenous value convertible stablecoin that is primarily backed by centralized stablecoins.

In practice, Beanstalk does not calculate the price of 1 Bean. Instead, at the beginning of each Season, Beanstalk calculates the sum of the liquidity and time weighted average shortage or excess of Beans across the liquidity pools on the [Oracle Whitelist](../farm/sun.md#oracle-whitelist) over the previous Season (i.e., [deltaB](../additional-resources/glossary.md#deltab)).

### **Debt Level**

The Pod Rate represents the Beanstalk debt level relative to the Bean supply. The Pod Rate is often used as a proxy for Beanstalk’s health. If the Bean supply is 1000 and there are 2000 [Pods](../farm/field.md#pods), the Pod Rate is 200%.

Beanstalk defines a handful of Pod Rate ranges that it uses as an input to determine how to change the Temperature:

* Excessively low debt: Pod Rate < 5%
* Reasonably low debt: 5% ≤ Pod Rate < 15%
* Optimal level of debt: Pod Rate = 15%
* Reasonably high debt: 15% < Pod Rate ≤ 25%
* Excessively high debt: Pod Rate > 25%

### **Bean Supply**

At the beginning of each Season, Beanstalk increases the Bean supply by deltaB if there was a liquidity and time weighted average shortage of Beans across the pools in the [Oracle Whitelist](../farm/sun.md#oracle-whitelist) over the previous Season. Essentially, Beanstalk will mint the number of Beans that need to be sold in the pools on the Oracle Whitelist to return the Bean price to a dollar.

[Stalkholders](../farm/silo.md#the-stalk-system), Pod holders, and [Active Fertilizer](../farm/barn.md#fertilizer) holders receive 1/3 of new Bean mints each while there are [Unfertilized Sprouts](../farm/barn.md#fertilizer) outstanding. If there is no Active Fertilizer, Stalkholders and Pod holders receive 1/2 of new Bean mints each. If there are neither Pods nor Active Fertilizer, Stalkholders receive 100% of new Bean mints.

### **Soil Supply**

At the beginning of each Season, Beanstalk sets the Soil supply.

When P < 1 over the previous Season (_i.e._, deltaB < 0), the Soil supply is equal to deltaB, the sum of the liquidity and time weighted average excess of Beans across the liquidity pools on the [Oracle Whitelist](../farm/sun.md#oracle-whitelist) over the previous Season.

When P ≥ 1 over the previous Season (_i.e._, deltaB ≥ 0), Beanstalk is still willing to issue debt in order to measure changing demand for [Soil](../farm/field.md#soil). The Soil supply is based on the number of Pods that Ripen and become Harvestable at the beginning of the Season, the Temperature, and the Beanstalk debt level. A greater number of Pods Ripening increases the Soil supply. Higher Temperature and debt level decrease the Soil supply. See [Section 8.11 in the whitepaper](https://bean.money/docs/beanstalk.pdf) for complete formulas.
