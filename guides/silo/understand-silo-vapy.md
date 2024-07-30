# Understand Silo vAPY

The Beanstalk UI displays vAPY (_variable_ APY_)_ statistics for each asset on the [Deposit Whitelist](../../farm/silo/#deposit-whitelist). APYs are called _variable_ because they are not enforced by Beanstalk in any way. Rather, the APY uses historical data about Beans earned by Stalkholders to estimate future returns for Depositing in the Silo.

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
* There are 30-day EMA of Beans earned by Stalkholders each Season (which assumes that the Bean to Max LP Seed Ratio will approach its max value if there are any Seasons where Stalkholders earned Beans in the last 30 days); and
* Every Stalkholder Mows their Grown Stalk and Plants their Plantable Seeds each Season.&#x20;

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

#### Strategy

The Beanstalk UI shows the vAPYs for a Deposit with the average amount of Grown Stalk\* based on a simulation of the Farmer's increase in Bean and Stalk positions compounded over the next year.

The complete formulas for the vAPYs can be read in the code [here](https://github.com/BeanstalkFarms/Beanstalk-API/blob/main/src/utils/apy/gauge.js).

\*The [APYs on DeFiLlama](https://defillama.com/yields?token=BEAN) are based on a new Deposit with no Grown Stalk.
