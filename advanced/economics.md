# Economics

Beanstalk is designed from economic first principles to create a useful trustless fiat currency. Over time, trustlessness, stability and liquidity increase, while [carrying costs](../introduction/why-beanstalk.md#carrying-costs) decrease but remain competitive. The following principles inspire Beanstalk:&#x20;

* [Low concentration of ownership](economics.md#ownership-concentration);
* [Strong credit](economics.md#strong-credit);
* [The marginal rate of substitution](economics.md#marginal-rate-of-substitution);
* [Low friction](economics.md#low-friction);
* [Equilibrium](economics.md#equilibrium); and
* [Incentive structures determine behaviors of financially motivated actors](economics.md#incentives).

### Ownership Concentration

A design that lowers the [Gini coefficient](https://en.wikipedia.org/wiki/Gini\_coefficient) of Beans and Stalk over time is essential to censorship resistance.&#x20;

Older [Deposits](../farm/silo.md) have their [Stalk from Seeds](../farm/silo.md#the-stalk-system) diluted relative to newer Deposits every [Season](../protocol/glossary.md#season). Therefore, newly minted Beans are more widely distributed over time.&#x20;

Beanstalk does not require a pre-mine. The first 100 Beans are created when the `init` function is called to deploy Beanstalk.

### Strong Credit

Beanstalk is credit based and only fails if it can no longer attract creditors. A reasonable level of debt, strong credit history and competitive interest rate attract creditors.&#x20;

Beanstalk changes the [Temperature](../protocol/glossary.md#temperature) to return the Pod Rate to the [optimal Pod Rate](../peg-maintenance/overview.md#debt-level) while regularly crossing the Bean price over its value peg. Beanstalk acts more aggressively when [the Pod Rate is excessively high or low](../peg-maintenance/overview.md#debt-level).&#x20;

Beanstalk never defaults on debt (although in the event of Beanstalk no longer attracting creditors, the loan maturity date would become infinitely far in the future—see [Disclosures](../disclosures.md#6-debt-maturity-risk)). Beanstalk is willing to issue Pods every Season.

### Marginal Rate of Substitution

There are a wide variety of opportunities Beanstalk has to compete with for creditors. Therefore, Beanstalk does not define an optimal Temperature, but instead [adjusts it to move closer to ideal equilibrium](../peg-maintenance/temperature.md#current-and-optimal-state).

### Low Friction

Minimizing the cost of using Beans and barriers to the [Farm](broken-reference) maximizes utility for users and appeal to creditors. The [Depot](../farm/depot.md) realizes the full benefits of composability on Ethereum.&#x20;

The [FIFO](../protocol/glossary.md#fifo) Pod Harvest schedule allows smaller [Sowers](../farm/field.md) to participate in peg maintenance and decreases the benefit of large scale price manipulation. The combination of non-expiry, the FIFO Harvest schedule, transferability and a [liquid secondary market](../farm/market.md) enables Sowers to Sow Beans as efficiently as possible.&#x20;

By maximizing the efficiency of the Soil market, Beanstalk minimizes its cost to attract creditors, the durations and magnitudes of price deviations below its value peg, and excess Pod issuance.

### Equilibrium

Equilibrium is a state of equivalent marginal quantity supplied and demanded. Beanstalk affects the supply of and demand for Beans to regularly cross the equilibrium price of 1 Bean over its value peg.&#x20;

While Beanstalk can [arbitrarily increase the Bean supply](../peg-maintenance/overview.md#bean-supply) when the Bean price is above its value peg, Beanstalk cannot arbitrarily decrease the Bean supply when the Bean price is below it. Beanstalk relies on the codependence between the equilibria of Beans and Soil to work around this limitation.&#x20;

In order to Sow Beans, they must be acquired (_i.e._, marginal demand for [Soil](../farm/field.md#soil) affects marginal demand for Beans). The marginal demand for Soil and Beans are functions of the Temperature and the Bean price. By [changing the Temperature](../peg-maintenance/temperature.md), Beanstalk affects decreases in the Bean supply and changes in demand for Beans.

### Incentives

Beanstalk-native financial incentives consistently increase trustlessness, stability and liquidity over time by coordinating independently financially motivated actors (_i.e._, Stalkholders and Sowers).&#x20;

[The Stalk System](../farm/silo.md#the-stalk-system) incentivizes (1) leaving assets Deposited in the Silo continuously by creating opportunity cost to [Withdraw](../farm/silo.md#withdraw) assets from the Silo, (2) adding value to liquidity pools with Beans by [rewarding more Seeds to Deposited LP tokens](../farm/silo.md#current-deposit-whitelist) than Deposited Beans, and (3) returning the Bean price to its value peg by allowing [Conversions](../peg-maintenance/convert.md) within the Silo without forfeiting Stalk.&#x20;

Beanstalk is governed by Stalkholders. Anyone with Stalk stands to profit from future growth of Beanstalk, but are not owed anything by Beanstalk.&#x20;

When the Bean price is below $1, there is an incentive to Withdraw assets from the Silo. The combination of the Stalk System and Withdrawal Freeze reduces this incentive significantly.&#x20;

When the Bean price is above $1, there is an incentive to buy Beans to earn a portion of the upcoming Bean seigniorage. This is exacerbated when the Pod Rate is lower. The commitment to automatically return the Bean price to its value peg and distribute proceeds from the sale to current Stalkholders based on Stalk ownership when the Farm became Oversaturated ([Flood](../peg-maintenance/flood.md)) and the Withdrawal Freeze, removes this incentive entirely during Seasons where the previous Season's Pod Rate was excessively low, and reduces it significantly otherwise.

Thus, Beanstalk consistently increases trustlessness, stability and liquidity over time.
