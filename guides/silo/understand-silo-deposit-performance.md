# Understand Silo Deposit Performance

The [Silo](https://app.bean.money/#/silo) page is a dashboard for monitoring the balances and performance of your [Silo Deposits](../../protocol-resources/glossary.md#deposit).

After [connecting a wallet](../getting-started/connect-wallet.md) on [app.bean.money](https://app.bean.money/), navigate to the "Silo" page.

The first module provides an overview of your Silo Deposits and their performance over time.

* The "Deposits" tab shows your current USD denominated "Value Deposited" and a chart of historical value. As Silo Deposits generate [Earned Beans](../../protocol-resources/glossary.md#earned-beans), [Planting](../../protocol-resources/glossary.md#plant) them will increase "Value Deposited".
  * For pre-exploit Farmers, the value of [Unripe Assets](../../protocol-resources/glossary.md#unripe-assets) is calculated after the [Chop Penalty](../../protocol-resources/glossary.md#chop-penalty).
* The "Stalk" tab shows your total "Stalk Balance" and a chart of historical Stalk balances, "Stalk Ownership" and "Stalk Grown per Day".
  * [Stalk](../../protocol-resources/glossary.md#stalk) is the governance token of the [Beanstalk DAO](../../governance/beanstalk/) received by Depositing assets on the [Deposit Whitelist](../../farm/silo.md#deposit-whitelist) and from [Seeds](../../protocol-resources/glossary.md#seeds). Your "Stalk Balance" will grow as your Seeds yield more Stalk.
  * Stalk entitles holders to passive interest in the form of a share of future [Bean mints](../../peg-maintenance/overview.md#bean-supply), and the right to propose and vote in [governance](../../governance/proposals.md). Your Stalk is forfeited when you [Withdraw](../../protocol-resources/glossary.md#withdraw) your Deposited assets from the Silo.
  * "Stalk Ownership" is your current ownership of Beanstalk displayed as a percentage. Ownership is determined by your proportional ownership of the total Stalk supply.
  * "Stalk Grown per Day" is the amount of Stalk grown each day from Seeds. Seeds yield 1/10,000 Stalk each [Season](../../protocol-resources/glossary.md#season).
* The "Seeds" tab shows your "Seeds Balance" and a chart of historical Seed balances.
  * Seeds are received by Depositing assets on the Deposit Whitelist and yield 1/10,000 Stalk each Season.

The second module provides an overview of your [Silo Rewards](../../protocol-resources/glossary.md#silo-rewards). Read how to [Claim Silo Rewards](claim-rewards.md).

* Earned Beans are the number of Beans earned since your last Plant. Upon Plant, Earned Beans are Deposited in the current Season.
* Earned Stalk is the Stalk associated with Earned Beans. Earned Stalk automatically contribute to Stalk ownership and do not require any action to claim them.
* [Plantable Seeds](../../protocol-resources/glossary.md#plantable-seeds) are Seeds earned in conjunction with Earned Beans. Plantable Seeds must be Planted in order to grow Stalk.
* [Grown Stalk](../../protocol-resources/glossary.md#grown-stalk) are Stalk earned from Seeds. Grown Stalk does not contribute to Stalk ownership until it is [Mown](../../protocol-resources/glossary.md#mow). Grown Stalk is Mown at the beginning of any Silo interaction.
* [Revitalized Stalk](../../protocol-resources/glossary.md#revitalized-stalk) are Stalk that have vested for pre-exploit Silo Members. Revitalized Stalk are minted as the percentage of [Fertilizer](../../protocol-resources/glossary.md#fertilizer) sold increases. Revitalized Stalk does not contribute to Stalk ownership until [Enrooted](../../protocol-resources/glossary.md#enroot).
* [Revitalized Seeds](../../protocol-resources/glossary.md#revitalized-seeds) are Seeds that have vested for pre-exploit Silo Members. Revitalized Seeds are minted as the percentage of Fertilizer sold increases. Revitalized Seeds do not generate Stalk until Enrooted.

The third module provides information on Deposits categorized by asset. This module can be switched between USD and BDV by selecting your wallet address, "Settings", and choosing a "Fiat display" option.

* The "Rewards" column shows the number of Stalk and Seeds per Bean denominated value (BDV) Deposited. Hover over the column to see the BDV of each asset.
* See [Understand vAPY](understand-vapy.md) for details on the Variable APY calculation.
* "TVD" is the Total Value Deposited from all Depositors.  Unripe Assets are scaled by the USD value of the underlying Beans or LP as recapitalized through the [Barn](../../farm/barn.md).
* The "Amount Deposited" is your amount of Beans or LP Deposited. Note that one unit of LP is not expected to be equal to one Bean. See the current BDV under the "Rewards" column.
* The "Value Deposited" is the value of your Deposits in USD or BDV. Unripe Assets are calculated after the Chop Penalty.
