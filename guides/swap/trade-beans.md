# Trade Beans

Beans can be bought and sold on the [Swap](https://app.bean.money/#/swap) page. To transfer between Farm and Circulating balances, see [Transfer Farm Balance](transfer-farm-balance.md).

1. Make sure you are on [app.bean.money](https://app.bean.money/) and [connect your wallet](../getting-started/connect-wallet.md).
2. Select “More” then “Swap” to navigate to the [Swap](https://app.bean.money/#/swap) page.
3. In the first field select the input token, or the asset you would like to sell. The dropdown menu will show each available input token and your total [Farm Balance](../../protocol-resources/glossary.md#farm-assets) and [Circulating Balance](../../protocol-resources/glossary.md#circulating-beans).
   * Farm Balance is the balance stored in Beanstalk, which can save gas fees in future transactions. See [Asset States](../../protocol-resources/asset-states.md) for more information.
   * Circulating Balance is the balance in your wallet, separate from Beanstalk.
4. In the second field, select the output token, or the asset you would like to buy.
   * Note: Swap must be used to buy or sell Beans, or to wrap or unwrap ETH. Trading between other pairs is not currently supported.
5. Enter the amount of the input token to sell, up to the amount held in your Farm or Circulating balances.
   * Note: The Beanstalk UI first spends the balance that is most gas-efficient based on the specified amount.
6. Verify the amount of the output token you will receive in the output field.
7. Under “Destination”, select “Farm Balance” or “Circulating Balance”.
8. A transaction preview will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
9. You may select a slippage tolerance by selecting the gear icon. The default slippage tolerance is 0.1%.
10. If you are trading ETH or have previously approved the token being spent, skip to Step 12. For all other tokens, select “Approve \[Token]”. This allows the Beanstalk contract to spend the token, but does not execute the trade yet.
11. Confirm the approval transaction in your wallet, and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../protocol-resources/contracts.md) before signing it.
12. Select “Swap”.
13. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../protocol-resources/contracts.md) before signing it.
14. After the transaction has been confirmed by the network, the location of your tokens will depend on the option selected in Step 7:
    * If “Farm Balance” was selected, the tokens will be shown on the [Balances](https://app.bean.money/#/balances) page.
    * If “Circulating Balance” was selected, the tokens will be in your wallet. Your Circulating Balance is also shown on the [Balances](https://app.bean.money/#/balances) page.
