# Bean to Max LP Seed Ratio

Beanstalk is a credit-based stablecoin protocol. The main goal of Beanstalk is to regularly oscillate the Bean price across $1, indefinitely. Beanstalk's primary peg maintenance mechanism, and theoretical basis for existence, is the [Field](../farm/field.md) (_i.e._, the Beanstalk credit facility). The ability for Beanstalk to borrow Beans from the open market at a reasonable interest rate is essential for long term peg maintenance.

However, with the successful addition of Conversions within the Silo in December 2021, a second peg maintenance mechanism was discovered. The ability to add and remove Beans from liquidity pools to decrease and increase the Bean price, respectively, changes the Bean price without any outflows or inflows from the system. Currently, Converts are limited in that Depositors can only Convert between Beans and LP tokens, and vice versa (_i.e._, not across LP tokens). Furthermore, the incentives for Converting in a given direction with respect to peg (in particular, Seed allocations to the various assets whitelisted for Deposit) are not adjusted autonomously in response to Beanstalk's state.

With the introduction of the Seed Gauge System, now Beanstalk also measures its liquidity level (in practice, the Liquidity to Supply Ratio, or L2SR).

***

In order to adjust the Bean to Max LP Seed Ratio, in practice Beanstalk adjusts a scalar (the Bean to Max LP Seed Scalar) between 0 and 1, where 0 results in the minimum Bean to Max LP Ratio and 1 results in the maximum Bean to Max LP Ratio. Therefore, the peg maintenance mechanism can adjust the Bean to Max LP Ratio independently of the minimum and maximum values (set to 50% and 100%, respectively).

At the beginning of each [Season](../farm/sun.md), Beanstalk changes the Bean to Max LP Seed Scalar depending on its position ([price](overview.md#decentralized-price-oracle), [debt level](overview.md#debt-level) and [liquidity level](overview.md#liquidity-level)) with respect to its [ideal equilibrium](overview.md#ideal-equilibrium).

Considering the current state and the liquidity level, Beanstalk adjusts the Bean to Max LP Seed Scalar to move toward the optimal state:

### Excessively Low L2SR

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

No matter the L2SR, when P > Q, Beanstalk should maximally incentivize Converting to LP Deposits by aggressively decreasing the Bean to Max LP Ratio. By decreasing the scalar by 0.5 each Season, the Bean to Max LP Ratio returns to the minimum value within 2 Seasons.

When L2SR is excessively low, in all cases, Beanstalk should be similarly aggressive in incentivizing Conversions to LP Deposits by quickly reaching the minimum Bean to Max LP Ratio.

### Reasonably Low L2SR

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

When the L2SR is reasonably low and Pod Rate is low, Beanstalk should be similarly aggressive in reaching the minimum Bean to Max LP Ratio given that, at the margin, Beanstalk would rather take on debt than lose liquidity. When the L2SR is reasonably low and Pod Rate is high, Beanstalk should gradually increase the Bean to Max LP Ratio when P > 1 (to incentivize Conversions above peg) and gradually decrease it when P < 1 (to incentivize Conversions below peg). By changing the scalar by 0.01 each Season, the Bean to Max LP Ratio can change from the maximum to the minimum value (or vice versa) within 100 Seasons.

### Reasonably High L2SR

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

When L2SR is reasonably high and P < 1, Beanstalk should similarly gradually increase the Bean to Max LP Ratio to incentivize Converting from LP Deposits to Bean Deposits, and vice versa when P > 1.

### Excessively High L2SR

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

When L2SR is excessively high, Beanstalk should be more willing to accept a loss of liquidity rather than an increase in debt level at the margin. Therefore, it should adjust the Bean to Max LP Scalar just as it does when L2SR is reasonably high, except it can be slightly more aggressive when P < 1 and the Pod Rate is high. By increasing the Bean to Max LP Scalar by 0.02, the Bean to Max LP Ratio can change from the minimum to the maximum value within 50 Seasons.
