# Transfer Farm Balance

The [Swap](https://app.bean.money/#/swap) page can be used to transfer tokens between a Farmer’s [Farm Balance](../../additional-resources/glossary.md#farm-assets) and [Circulating Balance](../../additional-resources/glossary.md#circulating-beans). Farm Balance is the balance stored in Beanstalk, which can save gas fees in future transactions. Circulating Balance is the balance in your wallet, separate from Beanstalk.

1. Make sure you are on [app.bean.money](https://app.bean.money/) and [connect your wallet](../getting-started/connect-wallet.md).
2. Select “More” then “Swap” to navigate to the [Swap](https://app.bean.money/#/swap) page.
3. In the first field select the token you would like to transfer. Select the same token in the second field.
4. Enter the amount of the token to transfer, up to the amount held in your Farm or Circulating balances.
5. Under “Source” select either “Farm Balance” or “Circulating Balance”. In the second field, verify the amount and “Destination”.
   * If the “Source” was “Farm Balance”, the “Destination” will be “Circulating Balance”, and vice versa.
6. A transaction preview will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
7. If you are transferring a non-ETH token from your Circulating Balance to your Farm Balance and have not previously approved that token, select “Approve \[Token]”. This allows the Beanstalk contract to move the token, but does not execute the transfer yet. Otherwise, skip to Step 9.
8. Confirm the approval transaction in your wallet, and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../additional-resources/contracts.md) before signing it.
9. Select “Swap”.
10. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../additional-resources/contracts.md) before signing it.
11. After the transaction has been confirmed by the network, the location of your tokens will depend on the option selected in Step 5:
    * If the “Destination” is “Farm Balance”, the tokens will be shown on the [Balances](https://app.bean.money/#/balances) page.
    * If the “Destination” is “Circulating Balance”, the tokens will be in your wallet. Your Circulating Balance is also shown on the [Balances](https://app.bean.money/#/balances) page.
