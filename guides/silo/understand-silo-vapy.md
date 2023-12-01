# Understand Silo vAPY

The Beanstalk UI displays vAPY (_variable_ APY_)_ statistics for each asset on the [Deposit Whitelist](../../farm/silo.md#deposit-whitelist). APYs are called _variable_ because they are not enforced by Beanstalk in any way. Rather, the APY uses historical data about Beans earned by Stalkholders to estimate future returns for Depositing in the Silo.

The APY calculation has two parts:

1. Estimating the number of Beans that will be minted per Season using recent historical data.
2. Estimating the number of Beans and Stalk that a Farmer will receive over time for Depositing their whitelisted assets in the Silo. This takes into account the Stalk supply and Seed supply and makes some [assumptions](understand-silo-vapy.md#estimating-vapy-for-silo-deposits) about Stalkholder behavior.

### Bean vAPY vs Stalk vAPY

Stalkholders earn Bean seignorage when [deltaB](../../protocol/glossary.md#deltab) is greater than 0 over the previous Season. Estimated annual Beans earned by a Stalkholder is called the **Bean vAPY**.

Seeds grow Stalk each Season, regardless of deltaB. Estimated annual Stalk growth for a Stalkholder is called the **Stalk vAPY**.

### Estimating Earned Beans per Season

The Beanstalk UI and Subgraph use a 30-day [exponential moving average](https://en.wikipedia.org/wiki/Moving\_average#Exponential\_moving\_average) (EMA) of Beans earned by Stalkholders to estimate future Beans earned by Stalkholders. The formula uses a weighted average in which recent Seasons are weighted more heavily.

The current EMA value can be located on the Silo page by hovering over the **Bean vAPY** values for any whitelisted asset.

### Estimating vAPY for Silo Deposits

The vAPY for Depositing a whitelisted asset in the Silo is determined by the value of 1 newly Deposited [BDV](../../protocol/glossary.md#bean-denominated-value) in 8760 Seasons (1 year).

The vAPY calculations make the following assumptions:

* No new assets are Deposited into or Withdrawn from the Silo;
* No liquidity is added or removed from liquidity pools that Beans trade in;
* There are $$\bar{n}^e$$ Beans earned by Stalkholders each Season; and
* Every Stalkholder Mows their Grown Stalk each Season.&#x20;

### Calculations

#### Exponential Moving Average (EMA)

The window of the EMA ($$u$$), i.e., the number of Seasons in 30 days:

$$
u = 24 * 30 = 720
$$

The weighting multiplier ($$\beta$$);  a constant between 0 and 1 that determines how much weight is given to the most recent data point:

$$
\beta=\frac{2}{(u+1)}
$$

The 30-day exponential moving average at Season $$t$$ ($$\bar{n}^e_t$$):

$$
\bar{n}^e_t = \beta \sum_{i=t-u+1}^{i \leq t}(1-\beta)^{t-i} n^e_{i}
$$

#### Silo vAPY

The formulas for the Silo vAPYs ($$\text{vAPY}^{x}_{\text{Bean}}$$​ and $$\text{vAPY}^{x}_{\text{Stalk}}$$​)  take the following variables as inputs:

* $$\bar{n}^e_t$$, the 30-day EMA of Beans earned by Stalkholders at Season $$t$$​;
* $$C_i$$, the total number of Seeds at Season $$i$$​;
* $$K_i$$, the total number of Stalk at Season $$i$$; and​
* $$x$$, the number of Seeds per BDV granted for Depositing this asset:
  * $$x = 3$$ for Deposited BEAN;
  * $$x= 3.25$$ for Deposited BEAN3CRV; and
  * $$x= 4.5$$ for Deposited BEANETH.

The formulas for the Silo vAPYs make estimations of the following variables:

* $$\hat{C_i}$$, the estimated total number of Seeds at Season $$i$$;​
* $$\hat{K_i}$$, the estimated total number of Stalk at Season $$i$$;
* $$\hat{b_i}$$, the estimated number of a Farmer's Deposited Beans at Season $$i$$​; and
* $$\hat{k_i}$$​, the estimated number of a Farmer's Stalk at Season $$i$$.​

$$\text{vAPY}^{x}_{\text{Bean}}$$ is calculated using the estimated number of Beans owned by the Farmer a year from now ($$\hat{b}_{t+8760}$$) by using a sequence from the current Season ($$t$$​) to Season $$t+8760$$​.

First, initialize the sequence with:

$$
\begin{aligned}
\hat{C}_{t} =& \ C_t \\
\hat{K}_{t} =& \ K_t \\
\hat{b}_{t} =& \ \frac{x}{3} \\
\hat{k}_{t} =& \ 1
\end{aligned}
$$

Then iterate through the following sequence for $$i \in\{{u | u \in \mathbb{N}, t < u \leq t+8760}\}$$​:

$$
\begin{aligned}
\hat{C_{i}} =& \ \hat{C}_{i-1} + 3\bar{n}^e_t \\
\hat{K}_{i} =& \ \hat{K}_{i-1} + \bar{n}^e_t + \frac{1}{10000}\hat{C}_{i-1} \\
\hat{b_{i}} =& \ \hat{b}_{i-1} + \bar{n}^e_t\frac{\hat{k}_{i-1}}{\hat{K}_{i-1}} \\
\hat{k}_{i} =& \ \hat{k}_{i-1} + \bar{n}^e_t\frac{\hat{k}_{i-1}}{\hat{K}_{i-1}} + \frac{3}{10000} \hat{b}_{i-1}
\end{aligned}
$$

We define $$\text{vAPY}^{x}_{\text{Bean}}$$​ for a given $$x$$​ as:

$$
\text{vAPY}^{x}_{\text{Bean}}=(\hat{b}_{t+8760}-\hat{b_t}) \times 100
$$

We define $$\text{vAPY}^{x}_{\text{Stalk}}$$​ for a given $$x$$​ as:

$$
\text{vAPY}^{x}_{\text{Stalk}}=(\hat{k}_{t+8760}-\hat{k_t}) \times 100
$$
