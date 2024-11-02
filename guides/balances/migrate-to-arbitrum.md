# Migrate to Arbitrum

[BIP-50](https://arweave.net/sl\_UxJFZbThaTxOMgH8ewLo7cwODJh54s9HtbU8MOl0) migrated Beanstalk from Ethereum mainnet to Arbitrum One.

Many users were automatically migrated, however, given that Beanstalk does not have control of Beans outside of the Beanstalk contract, Circulating Beans need to be manually migrated to Arbitrum.&#x20;

Beanstalk assets in smart contract accounts could not be automatically migrated given that Beanstalk cannot assume an owner of a smart contract is able to gain ownership of the same address on Arbitrum.

If you need to manually migrate to Arbitrum:

1. Make sure you are on [app.bean.money](https://app.bean.money/) and [connect your wallet](../getting-started/connect-wallet.md).
2. Enter the wallet address on Arbitrum One to receive your Beanstalk assets.
3. Select "Delegate Beanstalk Balances".
4. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should [verify](../../protocol/contracts.md) that the transaction is interacting with the correct contract before signing it.

For contract migrations only:

5. Connect the Arbitrum One wallet entered in step #2.
6. Select "Claim Beanstalk Balances".
7. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should [verify](../../protocol/contracts.md) that the transaction is interacting with the correct contract before signing it.

\


\
