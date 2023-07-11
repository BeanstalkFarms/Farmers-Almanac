# Withdraw from the Silo

The associated amount of Stalk, Seeds, and Stalk from Seeds from a given Deposit must be forfeited when the Deposit is Withdrawn from the Silo. You can find more information about Withdrawals [here](../../farm/silo.md#withdraw).

1. Make sure you are on [app.bean.money](https://app.bean.money/) and [connect your wallet](../getting-started/connect-wallet.md).
2. Navigate to the “Silo” page.
3. At the bottom of the page, there is a table showing the various assets on the [Deposit Whitelist](../../farm/silo.md#deposit-whitelist).
4. Select the asset you want to Withdraw. You must already have a Deposit of this asset in order to Withdraw.
5. Select the “Withdraw” tab and enter the amount of the Deposited asset you would like to Withdraw. You may Withdraw any amount up to your “Deposited Balance” shown below the input box.
6. Under “Destination”, select “Circulating Balance” or “Farm Balance”. Selecting Circulating Balance returns Withdrawn assets to your wallet. Selecting Farm Balance keeps the asset stored in Beanstalk which can save gas fees in future transactions. See [Asset States](../../protocol/asset-states.md) for more information.
7. LP Tokens have a “Claim as” option that allows you to receive the asset in a different form. For example, BEAN:3CRV LP may be Withdrawn as BEAN:3CRV, Bean or 3CRV. If the option selected is different from the Withdrawn asset, the transaction will convert the Withdrawn asset.
   * If the transaction involves trading between assets, you may select a slippage tolerance by selecting the gear icon. The default slippage tolerance is 0.1%.
8. A transaction preview showing the [decrease in Stalk and Seeds](../../farm/silo.md#the-stalk-system) will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
9. Select “Withdraw”.
10. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should [verify](../../protocol/contracts.md) that the transaction is interacting with the correct contract before signing it.
11. After the transaction has been confirmed by the network, the location of your assets will depend on the option selected in Step 6:
    * If “Circulating Balance” was selected, the assets will be in your wallet. Your Circulating Balance is also shown on the [Balances](https://app.bean.money/#/balances) page.
    * If “Farm Balance” was selected, the assets will be shown on the [Balances](https://app.bean.money/#/balances) page.
