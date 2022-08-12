# Sell Pods

Pods can be exchanged in a trustless fashion on the Pod Market. Read the [Pod Market](../../farm/market.md#the-pod-market) docs first for an introduction to Pod Market mechanics, [Pod Listings](../../additional-resources/glossary.md#pod-listing) and [Pod Orders](../../additional-resources/glossary.md#pod-order).

* [List Pods](sell-pods.md#\_f0v6b16fz4gt)
* [Fill Pod Order](sell-pods.md#\_ypbvhjlyyqna)

### List Pods <a href="#list-pods" id="list-pods"></a>

1. Make sure you are on [app.bean.money](https://app.bean.money/).
2. Navigate to the “Market” page.
3. Select “Create New” then select the “List” tab.
   * The “Select Plot” dropdown shows all your Plots. Select the Plot that has the Pods you would like to List and enter the number of Pods to List.
     * By default, Listing less than an entire Plot Lists the Pods at the end of the Plot. If you would like to choose the Pods to List, select “Advanced”.
   * “Price per Pod” is how much to sell each Pod for, denominated in Beans.
   * If the Pod Line moves forward by the amount in “Expires in”, the Pod Listing will automatically expire.
4. Under “Send proceeds to”, select “Circulating Balance” or “Farm Balance”. Circulating Balance sends the proceeds to your wallet, separate from Beanstalk. [Farm Balance](../../additional-resources/glossary.md#farm-assets) keeps the proceeds stored in Beanstalk.
5. A transaction preview will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
6. Select “List”.
7. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../additional-resources/contracts.md) before signing it.
8. After the transaction has been confirmed by the network, your Pod Listing will be shown on the [My Pod Market](https://app.bean.money/#/market/account) page on the “Listings” tab, where you can check the status of your Pod Listing or cancel it.
9. When your Pod Listing is Filled, the location of your Beans will depend on the option selected in Step 7:
   * If “Circulating Balance” was selected, the Beans will be in your wallet. Your Circulating Balance is also shown on the [Balances](https://app.bean.money/#/balances) page.
   * If “Farm Balance” was selected, the Beans will be shown on the [Balances](https://app.bean.money/#/balances) page.

### Fill Pod Order <a href="#fill-pod-order" id="fill-pod-order"></a>

1. Make sure you are on [app.bean.money](https://app.bean.money/).
2. Navigate to the “Market” page.
3. Below “Overview”, switch to the Pod Order modal by selecting “Sell Now”. This view displays all the active Pod Orders, sorted by ascending [Place in Line](../../additional-resources/glossary.md#pod-line).
   * You may customize the sorting, display, or filtering of any column by selecting it.
   * The “Order” ID is a unique identifier for each Pod Order.
   * Any Pods within the Pod Line range listed under “Place in Line” are eligible to be sold to the Pod Order.
   * “Pods Requested” is the number of Pods left to be sold to the Pod Order.
4. Select a Pod Order to view details or to sell Pods to a Pod Order.
5. Under the “Fill” modal, select the Plot you would like to use to Fill the Pod Order, and enter the number of Pods you would like to sell. You may sell up to the “Pods Requested” to the Pod Order.
6. Under “Destination”, select “Circulating Balance” or “Farm Balance”. Circulating Balance sends the proceeds to your wallet, separate from Beanstalk. [Farm Balance](../../additional-resources/glossary.md#farm-assets) keeps the proceeds stored in Beanstalk.
7. A transaction preview will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
8. Select “Fill”.
9. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../additional-resources/contracts.md) before signing it.
10. After the transaction has been confirmed by the network, the location of your Beans will depend on the option selected in Step 6:
    * If “Circulating Balance” was selected, the Beans will be in your wallet. Your Circulating Balance is also shown on the [Balances](https://app.bean.money/#/balances) page.
    * If “Farm Balance” was selected, the Beans will be shown on the [Balances](https://app.bean.money/#/balances) page.
