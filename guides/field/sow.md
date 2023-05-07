# Sow Beans

When there is [Soil](../../farm/field.md#soil) in [the Field](../../farm/field.md), Farmers can lend their Beans to Beanstalk for an interest rate known as the [Temperature](../../peg-maintenance/temperature.md).

1. Make sure you are on [app.bean.money](https://app.bean.money/) and [connect your wallet](../getting-started/connect-wallet.md).
2. Navigate to the “Field” page.
3. The Available Soil and Temperature are displayed in the “Field Conditions” component. The Soil supply is set by the Beanstalk peg maintenance mechanism. See [Soil Supply](../../peg-maintenance/overview.md#soil-supply) for additional information.
   * During the first five minutes of each Season, the Temperature ramps from 1% to 100% of the maximum Temperature in a Dutch auction known as the Morning Auction.
5. In the “Sow” tab, there is a dropdown menu to select the token you would like to use to buy and Sow Beans.
6. Enter the amount of the selected token you want to use to buy and Sow Beans.
   * The Soil available when preparing to buy and Sow Beans may not still be available at the time the transaction is confirmed by the network. If a transaction is submitted to Sow a greater amount of Soil than is available, the remaining Soil will be Sown, and all remaining Beans from the transaction will be sent to your [Farm Balance](../../protocol/asset-states.md).
   * If you are Sowing during the Morning Auction, the number of Pods to be received will increase in real time on the UI with the increasing Temperature. The actual amount of Pods you receive depends upon Soil availability and the Temperature at the time your transaction is confirmed.
7. A transaction preview will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
8. You may select a slippage tolerance by selecting the gear icon. The default slippage tolerance is 0.1%.
9. If you are buying and Sowing Beans with ETH or have previously approved the asset being spent, skip to Step 10. For all other assets, select “Approve \[Token]”. This allows the Beanstalk contract to spend the asset, but does not use it to buy and Sow Beans yet.
10. Confirm the approval transaction in your wallet, and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../protocol/contracts.md) before signing it.
11. Select “Sow”.
12. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../protocol/contracts.md) before signing it.
13. After the transaction has been confirmed by the network, your Pods will appear in the “Pod Balance” table at the bottom of the “Field” page.
