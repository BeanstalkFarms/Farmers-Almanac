# Claim Assets

After Withdrawing Deposited Assets, they become Withdrawn assets until the end of the Season of Withdrawal. At the beginning of the next Season, they become [Claimable](../../protocol-resources/glossary.md#claimable-assets). These assets must be Claimed in order to use them.

1. Make sure you are on [app.bean.money](https://app.bean.money/) and [connect your wallet](../getting-started/connect-wallet.md).
2. Navigate to the “Silo” page.
3. At the bottom of the page, there is a table showing the various assets on the [Deposit Whitelist](../../farm/silo.md#deposit-whitelist).
4. Select the asset you Withdrew and would like to Claim.
5. Select the “Claim” tab. The “Claimable Balance” will be shown. You will receive this amount of the asset after Claiming.
6. Under “Destination”, select “Circulating Balance” or “Farm Balance”. Selecting Circulating Balance returns Claimed assets to your wallet. Selecting Farm Balance keeps the asset stored in Beanstalk which can save gas fees in future transactions. See [Asset States](../../protocol-resources/asset-states.md) for more information.
7. LP Tokens have a “Claim as” option that allows you to receive the asset in a different form. For example, BEAN:3CRV LP may be Claimed as BEAN:3CRV, Bean or 3CRV. If the option selected is different from the Claimable asset, the transaction will convert the Claimable asset.
   * If the transaction involves trading between assets, you may select a slippage tolerance by selecting the gear icon. The default slippage tolerance is 0.1%.
8. A transaction preview will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
9. Select “Claim”.
10. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../protocol-resources/contracts.md) before signing it.
11. After the transaction has been confirmed by the network, the location of your assets will depend on the option selected in Step 6:
    * If “Circulating Balance” was selected, the assets will be in your wallet. Your Circulating Balance is also shown on the [Balances](https://app.bean.money/#/balances) page.
    * If “Farm Balance” was selected, the assets will be shown on the [Balances](https://app.bean.money/#/balances) page.
