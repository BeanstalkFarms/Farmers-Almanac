# Understand My Balances

* [Overview](understand-my-balances.md#overview)
* [Total Deposited Value](understand-my-balances.md#total-deposited-value)
* [Quick Rinse / Quick Harvest](understand-my-balances.md#quick-rinse-quick-harvest)
* [Rewards](understand-my-balances.md#rewards)
* [Farm Balance / Circulating Balance](understand-my-balances.md#farm-balance-circulating-balance)

### Overview

The [Balances](https://app.bean.money/#/balances) page is a dashboard for all Beanstalk-related holdings by wallet address.

After [connecting a wallet](../getting-started/connect-wallet.md) on [app.bean.money](https://app.bean.money/), navigate to the "Balances" page.

The top of the Balances page displays your Stalk, Seeds, Pods and Sprouts:

* [Stalk](../../protocol/glossary.md#stalk) - Your total Stalk balance. Stalk is the governance token of the Beanstalk DAO. Stalk entitles holders to passive interest in the form of a share of future Bean mints, and the right to propose and vote on [BIPs](../../protocol/glossary.md#beanstalk-improvement-proposal). Your Stalk is forfeited when you Withdraw your Deposited assets from the Silo.
* [Seeds](../../protocol/glossary.md#seeds) - Your total Seed balance. Each Seed yields 1/10000 [Grown Stalk](../../protocol/glossary.md#grown-stalk) each Season. Grown Stalk must be [Mown](../../protocol/glossary.md#mow) to add it to your Stalk balance. Your Seeds are forfeited when you Withdraw your Deposited assets from the Silo.
* [Pods](../../protocol/glossary.md#pods) - Your total Pod Balance. Pods become [Harvestable](../../protocol/glossary.md#harvestable-pods) on a [FIFO](../../protocol/glossary.md#fifo) basis. For more information on your place in the [Pod Line](../../protocol/glossary.md#pod-line), head over to the [Field page](https://app.bean.money/#/field).
* [Sprouts](../../protocol/glossary.md#sprouts) - Your total Sprout balance. The number of Beans left to be earned from your [Fertilizer](../../protocol/glossary.md#fertilizer). Sprouts become [Rinsable](../../protocol/glossary.md#rinsable-sprouts) on a [pari passu](../../protocol/glossary.md#pari-passu) basis. For more information on your Sprouts, head over to the [Barn page](https://app.bean.money/#/barn).

### Total Deposited Value

Shows the current USD denominated value of your Silo Deposits and a chart of historical value. As Silo Deposits generate [Earned Beans](../../protocol/glossary.md#earned-beans), [Planting](../../protocol/glossary.md#plant) them will increase "Total Deposited Value".

* For pre-exploit Farmers, the value of [Unripe Assets](../../protocol/glossary.md#unripe-assets) is calculated after the [Chop Penalty](../../protocol/glossary.md#chop-penalty).

The module below provides information on Deposits categorized by asset. This module can be switched between USD and [BDV](../../protocol/glossary.md#bean-denominated-value) by selecting your wallet address, "Settings", and choosing a "Fiat display" option.

* The "Amount Deposited" is your amount of Beans or LP Deposited. Note that one unit of LP is not expected to be equal to one Bean due to BDV differences.
* The "Value Deposited" is the value of your Deposits in USD or BDV. Unripe Assets are calculated after the Chop Penalty.
* The "Stalk" is the amount of Stalk associated with each Deposited asset. Stalk will increase as Grown Stalk is Mown and with [Earned Stalk](../../protocol/glossary.md#earned-stalk).
  * Pre-exploit Farmers receive [Revitalized Stalk](../../protocol/glossary.md#revitalized-stalk). Revitalized Stalk are minted as the percentage of [Fertilizer](../../protocol/glossary.md#fertilizer) sold increases. Revitalized Stalk does not contribute to Stalk ownership until [Enrooted](../../protocol/glossary.md#enroot).
* The "Seeds" is the amount of Seeds associated with each Deposited asset. Seeds will increase as [Plantable Seeds](../../protocol/glossary.md#plantable-seeds) are [Planted](../../protocol/glossary.md#plant).
  * Pre-exploit Farmers receive [Revitalized Seeds](../../protocol/glossary.md#revitalized-seeds). Revitalized Seeds are minted as the percentage of Fertilizer sold increases. Revitalized Seeds do not generate Stalk until Enrooted.

### Quick Rinse / Quick Harvest

These modules appear if you have [Rinsable Sprouts](../../protocol/glossary.md#rinsable-sprouts) or [Harvestable Pods](../../protocol/glossary.md#harvestable-pods).

* Under “Destination”, select “Circulating Balance” or “Farm Balance”. [Circulating Balance](../../protocol/glossary.md#circulating-beans) sends the Rinsed or Harvested Beans to your wallet, separate from Beanstalk. [Farm Balance](../../protocol/asset-states.md) keeps the asset stored in Beanstalk which can save gas fees in future transactions. See [Asset States](../../protocol/asset-states.md) for more information.
* Select “Rinse” or "Harvest".
* Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../protocol/contracts.md) before signing it.
* After the transaction has been confirmed by the network, the location of your assets will depend on the "Destination" selected.&#x20;
  * You can confirm the location in the ["Farm Balance" and "Circulating Balance" modules](understand-my-balances.md#farm-balance-circulating-balance).

### Rewards

This module displays and allows claiming of [Silo Rewards](../../farm/silo.md#silo-rewards).

* Earned Beans are the number of Beans earned since your last Plant. Upon Plant, Earned Beans are Deposited in the current Season.
* Earned Stalk is the Stalk associated with Earned Beans. Earned Stalk automatically contribute to Stalk ownership and do not require any action to claim them.
* Plantable Seeds are Seeds earned in conjunction with Earned Beans. Plantable Seeds must be Planted in order to grow Stalk.
* Grown Stalk are Stalk earned from Seeds. Grown Stalk does not contribute to Stalk ownership until it is Mown. Grown Stalk is Mown at the beginning of any Silo interaction.
* Revitalized Stalk are Stalk that have vested for pre-exploit Silo Members. Revitalized Stalk are minted as the percentage of Fertilizer sold increases. Revitalized Stalk does not contribute to Stalk ownership until Enrooted.
* Revitalized Seeds are Seeds that have vested for pre-exploit Silo Members. Revitalized Seeds are minted as the percentage of Fertilizer sold increases. Revitalized Seeds do not generate Stalk until Enrooted.

See the [Claim Silo Rewards guide](../silo/claim-rewards.md) for detailed instructions.

### Farm Balance / Circulating Balance

Farm Balances are assets stored in Beanstalk. [Farm assets](../../protocol/glossary.md#farm-assets) can be used in transactions on the Farm. Circulating balances are Beanstalk assets in your wallet.

See [Asset States](../../protocol/asset-states.md) for more info on the different states Beanstalk assets can be in.

These modules display your current Farm and Circulating balances for all tokens that can be used within the Beanstalk UI.

