# Understand Fert vAPY

The Beanstalk UI displays vAPY (_variable_ APY_)_ statistics for Fertilizer. APYs are called _variable_ because they are not enforced by Beanstalk in any way. Rather, the APY uses historical data about Beans earned by Fertilizer holders to estimate future returns.

The APY calculation has two parts:

1. Estimating the number of Beans that will be minted per Season using recent historical data.
2. Estimating the number of Beans that a Farmer will receive over time for holding Fertilizer. This takes some [assumptions](understand-fert-vapy.md#estimating-vapy-for-silo-deposits) about Fertilizer holder behavior.

### Fert vAPY vs Stalk vAPY

Fertilizer holder earn Bean seignorage when [deltaB](../../protocol/glossary.md#deltab) is greater than 0 over the previous Season. Estimated annual Beans earned by a Fertilizer holder is called the **Fert vAPY**.

### Estimating Sprouts Fertilized per Season

The Beanstalk UI and Subgraph use a 30-day [exponential moving average](https://en.wikipedia.org/wiki/Moving\_average#Exponential\_moving\_average) (EMA) of Beans earned by Fertilizer holders to estimate future returns. The formula uses a weighted average in which recent Seasons are weighted more heavily.

The current EMA value can be located on the Barn page by hovering over the **Fert vAPY**.

### Estimating vAPY for Fertilizer

The vAPY is determined by the estimated return of holding Fertilizer in 8760 Seasons (1 year).

The vAPY calculation makes the following assumptions:

* No more Available Fertilizer is purchased; and
* No Active Fertilizer becomes Used.

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

The 30-day exponential moving average at Season $$t$$ ($$\bar{n}^e_t$$): &#x20;

$$
\bar{n}^e_t = \beta \sum_{i=t-u}^{i \leq t}(1-\beta)^{t-i} n^e_{i}
$$

#### Fert vAPY

The formulas for the Fert vAPY ($$\text{vAPY}^{\text{Fert}}$$​) take the following variables as inputs:

* $$\bar{n}^e_t$$, the 30-day EMA of Beans earned by Fertilizer holders at Season $$t$$​;
* $$h$$, the Humidity at Season $$t$$​; and
* $$F$$, the Active Fertilizer supply.

$$\text{vAPY}^{\text{Fert}}$$​ is calculated using the estimated number of Beans owned by the Fertilizer holder a year from now (8760 Seasons from now).

First, calculate the delta Beans earned per Fertilizer ($$\text{dBPF}$$​):

$$
\text{dBPF}=\frac{\bar{n}^e_t}{F}
$$

We define $$\text{vAPY}^{\text{Fert}}$$​ as:

$$
\text{vAPY}^{\text{Fert}}=(\frac{h}{
    \frac{1 + h}{\text{BPF}} \div 8760})
$$
