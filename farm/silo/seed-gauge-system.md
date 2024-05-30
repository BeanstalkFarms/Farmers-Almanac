# Seed Gauge System

Seeds generate opportunity cost for Withdrawing assets that have been Deposited for longer and marginal benefit for holding particular assets in the Silo in the form of Grown Stalk.

There are 3 new primary tools that Beanstalk has at its disposal as a result of implementing the Seed Gauge System:

1. The Target Seasons to Catchup, which determines the target number of Seasons for a new Deposit with an average number of Seeds to catch up to the average Grown Stalk per BDV of existing Deposits at the time of Deposit;
2. Bean vs LP Seed distribution, or more specifically, the [Bean to Max LP Seed Ratio](../../peg-maintenance/bean-to-max-lp-seed-ratio.md), which determines the relative benefits of holding Bean exposure vs exposure to at least 1 particular LP token in the Silo over time; and
3. LP vs LP Seed distribution, which determines relative benefits of holding a given non-Bean asset in the Silo over time.

### Grown Stalk Inflation Rate

The Grown Stalk per BDV for a Deposit can be thought of as the age of that Deposit—the longer the Deposit has been in the Silo, the higher its Grown Stalk is relative to its BDV. Thus, the average Grown Stalk per BDV is a measure for how old Deposits are across the entire Silo relative to the total BDV in the Silo.

The Seed Gauge System enables Beanstalk to target an amount of Grown Stalk per BDV that should be issued each Season. In particular, Beanstalk sets the target number of Seasons for a new Deposit with an average number of Seeds to catch up to the average Grown Stalk per BDV of existing Deposits at the time of Deposit, or in other words, the Target Seasons to Catchup. The Target Seasons to Catchup is currently set to 4320 Seasons, or \~6 months.

### **Gauge Points**

Gauge Points determine how the Grown Stalk issued in a Season should be distributed between whitelisted LP tokens. Only whitelisted LP tokens have Gauge Points.&#x20;

Every Season, Beanstalk calculates the new amount of Gauge Points an LP token should have by calling each whitelisted LP token's Gauge Point function. Currently all whitelisted LP tokens use the same Gauge Point function that increments or decrements the Gauge Points based on whether the current Deposited BDV is lower or higher than optimal.

### **Bean to Max LP Seed Ratio**

Gauge Points per BDV is the amount of Gauge Points allocated to a whitelisted LP token divided by the total BDV of that LP token Deposited in the Silo. The whitelisted LP token with the largest Gauge Points per BDV is used to determine the distribution of Grown Stalk to Beans in the Silo in order to ensure that at least 1 LP token always receives at least as much Grown Stalk as Deposited Beans (_i.e._, the "Max LP" in "Bean to Max LP Seed Ratio"). Ensuring that 1 whitelisted LP token (_i.e._, the LP token with the highest Gauge Points per BDV) is always allocated at least as many Seeds as Beans ensures that Beanstalk never incentivizes holding Beans over providing liquidity.

The Bean to Max LP Seed Scalar ($$L$$) is a scalar between 0 and 1 that is adjusted by the peg maintenance mechanism. The Bean to Max LP Seed Ratio has a minimum ($$Y$$) and maximum value ($$Z$$). Currently, $$Y$$ and $$Z$$ are set to 1:2 (_i.e._, 50%) and 1:1 (_i.e._, 100%), respectively.&#x20;

$$
Bean To Max LP Seed Ratio = Y + L(Z - Y)
$$

At $$L = 0$$, the Bean to Max LP Seed Ratio is at its minimum value (_i.e._, at 1:2, 1 Bean Deposited in the Silo receives half the amount of Grown Stalk as 1 BDV of the Max LP token), and at $$L = 1$$, the Bean to Max LP Seed Ratio is at its maximum value (_i.e._, at 1:1, 1 Bean Deposited in the Silo receives the same amount of Grown Stalk as 1 BDV of the the Max LP token).
