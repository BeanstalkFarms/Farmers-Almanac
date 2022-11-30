# Chop Unripe Assets

[Unripe assets](../../farm/barn.md#unripe-assets) can be Chopped in exchange for the underlying. You can find more information about Chopping [here](../../farm/barn.md#chopping).

1. Make sure you are on [app.bean.money](https://app.bean.money/) and [connect your wallet](../getting-started/connect-wallet.md).
2. Select your wallet address on the top right of the page and in the dropdown menu select “Chop Unripe Assets”.
3. The “Chop Conditions” component shows the current “[Chop Penalty](../../farm/barn.md#chopping)”. Note that Chopping with a greater than 0% Chop Penalty forfeits a claim to future Ripe assets.
4. Select the asset you want to Chop using the drop down menu and enter the amount to Chop, up to the “Balance” shown below the input box.
5. Under “Destination”, select “Circulating Balance” or “Farm Balance”. Circulating Balance sends the Chopped assets to your wallet, separate from Beanstalk. [Farm Balance](../../protocol/asset-states.md) keeps the assets stored in Beanstalk which can save gas fees in future transactions. See [Asset States](../../protocol/asset-states.md) for more information.
6. A transaction preview will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
7. Select “Chop”.
8. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../protocol/contracts.md) before signing it.
9. After the transaction has been confirmed by the network, the location of your assets will depend on the option selected in Step 5:
   * If “Circulating Balance” was selected, the Chopped assets will be in your wallet. Your Circulating Balance is also shown on the [Balances](https://app.bean.money/#/balances) page.
   * If “Farm Balance” was selected, the Chopped assets will be shown on the [Balances](https://app.bean.money/#/balances) page.
