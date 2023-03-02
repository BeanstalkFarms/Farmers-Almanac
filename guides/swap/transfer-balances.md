# Transfer Balances

The [Swap](https://app.bean.money/#/swap) page can be used to transfer tokens between a Farmer’s [Farm Balance](../../protocol/glossary.md#farm-assets) and [Circulating Balance](../../protocol/glossary.md#circulating-beans) and between wallets.

1. Make sure you are on [app.bean.money](https://app.bean.money/) and [connect your wallet](../getting-started/connect-wallet.md).
2. Select “More” then “Swap” to navigate to the [Swap](https://app.bean.money/#/swap) page. Select the "Transfer" tab.
3. In the first field select the token you would like to transfer and its location:
   * "Circulating Balance" is the balance in your wallet, separate from Beanstalk.
   * "Farm Balance" is the balance stored in Beanstalk, which can save gas fees in future transactions.
   * "Combined Balance" is the sum of Circulating Balance and Farm Balance. Note Combined Balance cannot be used when transferring to yourself.
5. Enter the amount of the token to transfer, up to the amount held in your Farm, Circulating or Combined balances.
6. Under “Transfer to”, enter the address to transfer the tokens to, or select "Me" to move your Farm Balance to Circulating Balance or vice versa.
7. Under "Destination Balance" select either "Circulating Balance" or "Farm Balance".
   * If "Transfer to" is set to "Me", if the source of the token was “Farm Balance”, the “Destination” will be “Circulating Balance”, and vice versa.
8. A transaction preview will appear below the inputs. Select the “Transfer Details” dropdown to review each step of the transaction.
9. If you are transferring a non-ETH token from your Circulating Balance and have not previously approved that token, select “Approve \[Token]”. This allows the Beanstalk contract to move the token, but does not execute the transfer yet. Otherwise, skip to Step 10.
10. Confirm the approval transaction in your wallet, and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../protocol/contracts.md) before signing it.
11. Select “Transfer”.
12. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../protocol/contracts.md) before signing it.
13. After the transaction has been confirmed by the network, the location of your tokens will depend on the option selected in Step 5:
    * If the “Destination” is “Farm Balance”, the tokens will be shown on the [Balances](https://app.bean.money/#/balances) page.
    * If the “Destination” is “Circulating Balance”, the tokens will be in the destination wallet. The Circulating Balance is also shown on the [Balances](https://app.bean.money/#/balances) page.
