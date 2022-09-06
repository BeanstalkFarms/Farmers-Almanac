# How Beanstalk Works

Beanstalk does not have any collateral requirements. Beanstalk uses credit instead of collateral to create Bean price stability relative to its value peg of $1. The practicality of using DeFi is currently limited by the lack of decentralized low-volatility assets with competitive carrying costs. Borrowing rates on USD stablecoins have historically been higher than borrowing rates on USD, even when supply increases rapidly. Non-competitive carrying costs are due to collateral requirements.

Beanstalk relies on three native assets and three interconnected facilities to regularly oscillate the price of Bean across its value peg:

### **Tokens**

Beanstalk issues 3 tokens:

1. Beans — Beanstalk ERC-20 fiat stablecoins;
2. [Stalk](../farm/silo.md#the-stalk-system) — illiquid yield-generating governance tokens; and
3. [Seeds](../farm/silo.md#the-stalk-system) — illiquid tokens which yield 1/10000 Stalk each Season.

### **Primary Facilities**

#### **1. The Sun** <a href="#the-sun" id="the-sun"></a>

Beanstalk uses [the Sun](../farm/sun.md) to create a cost-efficient and protocol-native timekeeping mechanism. The Sun keeps time on the Farm in Seasons. Each Season is \~1 hour long. Beanstalk adjusts itself to return the Bean price to its value peg at the beginning of every Season.

The Sun leverages the 3CRV pool on Curve as the Beanstalk oracle price source for $1.

In practice, Beanstalk does not calculate the price of 1 Bean. Instead, at the beginning of a Season, Beanstalk calculates [deltaB](../additional-resources/glossary.md#deltab), the sum of the time and liquidity weighted average shortage or excess Beans across liquidity pools on the [Oracle Whitelist](../farm/sun.md#oracle-whitelist);

The Sun uses deltaB to determine how to change the Bean supply and [Soil](../farm/field.md#soil) supply.

#### **2. The Silo** <a href="#the-silo" id="the-silo"></a>

Beanstalk uses [the Silo](../farm/silo.md), the Beanstalk DAO, to create a robust decentralized governance mechanism. Farmers can earn yield from passive participation in Beanstalk governance by Depositing whitelisted assets in the Silo to receive Stalk and Seeds.

Stalkholders can submit and vote on [Beanstalk Improvement Proposals](broken-reference) (BIPs) and collect a portion of Bean supply increases. A diverse community of Stalkholders creates decentralization.

To encourage consistent security:

* Seeds yield Stalk every Season.
* The associated amount of Stalk and Seeds from a given Deposit must be forfeited when it is Withdrawn from the Silo.
* Deposits can be Withdrawn from the Silo at any time but are Frozen until the end of the current Season.

Deep and consistent liquidity in liquidity pools Beans trade in improves stability. Liquidity providers to liquidity pools whose LP Tokens are whitelisted can also Deposit their LP Tokens in the Silo to earn Stalk and Seeds. LP Token Deposits earn more Seeds than Bean Deposits.

Conversions within the Silo between Bean and LP Deposits serve a major role in peg maintenance.

#### **3. The Field** <a href="#the-field" id="the-field"></a>

[The Field](../farm/field.md) is Beanstalk’s decentralized credit facility. Anytime the Bean price is too low, Beanstalk uses the Field to attract lenders who can lend their Beans to Beanstalk, which are subsequently burnt in exchange for Pods, Beanstalk’s native debt asset. Pods are paid out on a First In, First Out (FIFO) basis when new Beans are minted.

Soil is the number of Beans that can be lent to Beanstalk at any given time. Any time Beanstalk is willing to issue debt, there is Soil available in the Field. Any Beans not in the Silo can be Sown (lent) to Beanstalk in exchange for Pods.

Pods have a fixed interest rate and unknown maturity date. The number of Pods that grow from 1 Sown Bean is determined by the [Temperature](../peg-maintenance/temperature.md)— the Beanstalk-native interest rate — at the time of Sowing. Pods become Harvestable (redeemable) for 1 Bean on a First In, First Out (FIFO) basis when new Beans are minted.

### **Creating Stability**

Beanstalk requires a diverse set of participants, including Silo Members (people who Deposit assets in the Silo), Sowers (people who lend Beans to Beanstalk), and arbitrageurs. Beanstalk aligns the incentives of every individual participant to maximize price stability and create a diverse, decentralized economy. Beanstalk-native financial incentives consistently increase censorship resistance, stability and liquidity over time.

At the beginning of each Season, the Sun calculates deltaB (the sum of the time and liquidity weighted average shortage or excess Beans across liquidity pools on the Oracle Whitelist), Beanstalk’s debt level, and the change in demand for Soil over the previous 2 Seasons, and dynamically adjusts the Bean supply, Soil supply and Temperature to bring the price back towards the peg.

When the price of Bean is too low (_i.e._, deltaB is negative), Beanstalk:

* Increases the Soil supply by deltaB; and
* Raises the Temperature.

By increasing the Soil supply and raising the Temperature, Beanstalk can decrease the supply of Beans and therefore bring the price of Bean back up to its peg (assuming there are willing lenders at the given Temperature). In principle, a reasonable debt level and consistent credit history attracts lenders.

When the Bean price is too high (_i.e._, deltaB is positive), Beanstalk:

* Increases the Bean supply by deltaB; and
* Lowers the Temperature.

By increasing the Bean supply and lowering the Temperature, Beanstalk can bring the price of Bean back down to its peg.

To align the interests of Stalkholders and Sowers, 1/3 of Bean supply increases are distributed to Stalkholders and 1/3 go to Pod Harvests. The other 1/3 are distributed to Active Fertilizer holders as part of Beanstalk’s recapitalization plan after the April 2022 governance exploit (see [Barn](../farm/barn.md) section).

In order to prevent inorganic growth, if the Bean price is too high and the debt level is excessively low for a Season, Beanstalk sells Beans directly on Curve to return the price to $1 (see [Flood](../peg-maintenance/flood.md) section).
