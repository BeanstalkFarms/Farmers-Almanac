# Understand My Balances

The [Balances](https://app.bean.money/#/balances) page is a dashboard for all Beanstalk-related holdings by wallet address.

After [connecting a wallet](../getting-started/connect-wallet.md) on [app.bean.money](https://app.bean.money/), navigate to the "Balances" page.

The top of the Balances page displays your total Beanstalk-related balance denominated in US dollars. The total balance is the sum of:

* Deposited Balances - Assets that are [Deposited](../../protocol-resources/glossary.md#deposit) in the [Silo](../../farm/silo.md).
* Withdrawn Balances - Assets being [Withdrawn](../../protocol-resources/glossary.md#withdraw) from the Silo. At the end of the current [Season](../../protocol-resources/glossary.md#season), Withdrawn assets become [Claimable](../../protocol-resources/glossary.md#claimable-assets).
* Claimable Balances - Assets that can be Claimed after a Withdrawal.
* Farm Balances - Assets stored in Beanstalk. [Farm assets](../../protocol-resources/glossary.md#farm-assets) can be used in transactions on the Farm.
* Circulating Balances - Beanstalk assets in your wallet.

See [Asset States](../../protocol-resources/asset-states.md) for more info on the different states Beanstalk assets can be in.

Note that Unripe Bean and Unripe BEAN:3CRV LP balances are based on the amount received as if they were [Chopped](../../protocol-resources/glossary.md#chop) for [Ripe assets](../../protocol-resources/glossary.md#ripe-assets), after accounting for the [Chop Penalty](../../protocol-resources/glossary.md#chop-penalty).

These holdings listed on the Balances page are not included in the USD balance calculation:

* [Stalk](../../protocol-resources/glossary.md#stalk) - Your total Stalk balance. Stalk is the governance token of the Beanstalk DAO. Stalk entitles holders to passive interest in the form of a share of future Bean mints, and the right to propose and vote on [BIPs](../../protocol-resources/glossary.md#beanstalk-improvement-proposal). Your Stalk is forfeited when you Withdraw your Deposited assets from the Silo.
* [Seeds](../../protocol-resources/glossary.md#seeds) - Your total Seed balance. Each Seed yields 1/10000 [Grown Stalk](../../protocol-resources/glossary.md#grown-stalk) each Season. Grown Stalk must be [Mown](../../protocol-resources/glossary.md#mow) to add it to your Stalk balance. Your Seeds are forfeited when you Withdraw your Deposited assets from the Silo.
* [Pods](../../protocol-resources/glossary.md#pods) - Your total Pod Balance. Pods become [Harvestable](../../protocol-resources/glossary.md#harvestable-pods) on a [FIFO](../../protocol-resources/glossary.md#fifo) basis. For more information on your place in the [Pod Line](../../protocol-resources/glossary.md#pod-line), head over to the [Field page](https://app.bean.money/#/field).
* [Sprouts](../../protocol-resources/glossary.md#sprouts) - Your total Sprout balance. The number of Beans left to be earned from your [Fertilizer](../../protocol-resources/glossary.md#fertilizer). Sprouts become [Rinsable](../../protocol-resources/glossary.md#rinsable-sprouts) on a pari passu basis. For more information on your Sprouts, head over to the [Barn page](https://app.bean.money/#/barn).
