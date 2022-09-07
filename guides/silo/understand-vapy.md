# Understand vAPY

The Beanstalk UI displays vAPY (_variable_ APY_)_ statistics for each asset on the [Deposit Whitelist](../../farm/silo.md#deposit-whitelist). APYs are called _variable_ because they are not enforced by Beanstalk in any way. Rather, the APY uses historical data about Beans earned by Stalkholders to estimate future returns for Depositing in the Silo.

The APY calculation has two parts:

1. Estimating the number of Beans that will be minted per Season using recent historical data.
2. Estimating the number of Beans and Stalk that a Farmer will receive for Depositing in the Silo. This takes into account the Stalk supply and Seed supply and makes some [assumptions](understand-vapy.md#estimating-vapy-for-silo-deposits) about Stalkholder behavior.

### Bean vAPY vs Stalk vAPY

Stalkholders earn Bean seignorage when [deltaB](../../additional-resources/glossary.md#deltab) is greater than 0 over the previous Season. Estimated annual Beans earned by a Stalkholder is called the **Bean vAPY**.

Seeds grow Stalk each Season, regardless of deltaB. Estimated annual Stalk growth for a given Stalkholder is called the **Stalk vAPY**.

### Estimating Earned Beans per Season

Beanstalk uses a 14-day [exponential moving average](https://en.wikipedia.org/wiki/Moving\_average#Exponential\_moving\_average) (EMA) of Beans earned by Stalkholders to estimate future Beans earned by Stalkholders. The formula uses a weighted average in which recent Seasons are weighted more heavily.

The current EMA value can be located on the Silo page by hovering over the **Bean vAPY**.

### Estimating vAPY for Silo Deposits

The vAPY for Depositing a whitelisted asset in the Silo is determined by the value of 1 newly Deposited [BDV](../../additional-resources/glossary.md#bean-denominated-value) in 8760 Seasons (1 year).

The vAPY calculations make the following assumptions:

* No new assets are Deposited into or Withdrawn from the Silo;
* No liquidity is added or removed from liquidity pools that Beans trade in;
* There are $$\bar{n}^e$$ Beans earned by Stalkholders each Season; and
* Every Stalkholder Mows their Grown Stalk each Season.&#x20;

### Calculations

#### Exponential Moving Average (EMA)

$$
\beta=\frac{2}{(u+1)}
$$

$$
u=14*7=210
$$

$$
\bar{n}^e_t = \beta \sum_{i=0}^{i \leq t}(1-\beta)^{t-i} n^e_{i}
$$

#### APY: Silo Deposits

The formulas for ($$APY^{Silo}_x$$) take the following additional variables as inputs:

* ($$C_i$$), the total number of Seeds at Season $$i$$​
* ($$K_i$$), the total number of Stalk at Season $$i$$​
* ($$x$$), the number of Seeds per BDV granted for Depositing this asset
  * ($$x = 2$$) for Deposited BEAN;
  * ($$x= 4$$) for Deposited BEAN:3CRV, etc.

The formulas for ($$APY^{Silo}_x$$) make estimations of the following variables:

* ($$\hat{K_i}$$), the estimated total number of Stalk at Season $$i$$​
* ($$\hat{C_i}$$​), the estimated total number of Seeds at Season $$i$$​
* ($$\hat{k_i}$$​), the estimated number of a Depositor's Stalk at Season $$i$$​
* ($$\hat{b_i}$$), the estimated number of a Depositor's Deposited Beans at Season $$i$$​.

($$APY^{Silo}_x$$​) is calculated from the estimated number of Beans owned in a year ($$\hat{b_{t+8760}}$$) by using a sequence from the current Season ($$t$$​) to ($$t+8760$$​).

First, initialize the sequence with:

$$
\begin{aligned}
\hat{C}_{t} =& \ C_t \\
\hat{K}_{t} =& \ K_t \\
\hat{b}_{t} =& \ \frac{x}{2} \\
\hat{k}_{t} =& \ 1
\end{aligned}
$$

Then iterate through the following sequence for $$i \in\{{u | u \in \mathbb{N}, t < u \leq t+8760}\}$$​:

$$
\begin{aligned}
\hat{C_{i}} =& \ \hat{C}_{i-1} + 2\bar{n}^e \\
\hat{K}_{i} =& \ \hat{K}_{i-1} + \bar{n}^e + \frac{1}{10000}\hat{C}_{i-1} \\
\hat{b_{i}} =& \ \hat{b}_{i-1} + \bar{n}^e\frac{\hat{k}_{i-1}}{\hat{K}_{i-1}} \\
\hat{k}_{i} =& \ \hat{k}_{i-1} + \bar{n}^e\frac{\hat{k}_{i-1}}{\hat{K}_{i-1}} + \frac{1}{5000} \hat{b}_{i-1}
\end{aligned}
$$

We then define ($$APY^{Silo}_x$$​) for a given ($$x$$​) as:

$$
APY^{Silo}_x=\frac{\hat{b}_{t-8760}-\hat{b_t}}{100}
$$
