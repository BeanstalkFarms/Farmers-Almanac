# Buy Pods

Pods can be exchanged in a trustless fashion on the Pod Market. Read the [Pod Market](../../farm/market.md#the-pod-market) docs first for an introduction to Pod Market mechanics, [Pod Listings](../../additional-resources/glossary.md#pod-listing) and [Pod Orders](../../additional-resources/glossary.md#pod-order).

* [Fill Pod Listing](buy-pods.md#\_h7wv7iarhbgk)
* [Order Pods](buy-pods.md#\_714q89jrln2n)

### Fill Pod Listing <a href="#_h7wv7iarhbgk" id="_h7wv7iarhbgk"></a>

1. Make sure you are on [app.bean.money](https://app.bean.money/)
2. Navigate to the “Market” page.
3. Open Pod Listings appear below the “Buy Now” tab. This view displays all the Pod Listings, sorted by ascending [Place in Line](../../additional-resources/glossary.md#pod-line).
   * You may customize the sorting, display, or filtering of any column by selecting it.
   * The “Listing” # is a unique identifier for each Pod Listing.
   * The “Place in Line” is the position in the Pod Line when the Pods in the Pod Listing will start to become Harvestable.
   * The “Price per Pod” is the number of Beans requested per Pod.
   * The “Amount” is the number of Pods left to be purchased from the Pod Listing.
   * If the Pod Line moves forward by the amount in the “Expires in” field, the Pod Listing will automatically expire.
4. Select a Pod Listing to view details and to buy Pods from a Pod Listing.
5. Under the “Fill” component, select the token you would like to use to buy Pods, and enter the amount you would like to buy. You may buy up to the “Amount” of Pods available from the Pod Listing.
6. A transaction preview will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
7. You may select a slippage tolerance by selecting the gear icon. The default slippage tolerance is 0.1%.
8. If you are buying Pods with ETH, skip to Step 10. For all other assets, select “Approve \[Token]”. This allows the Beanstalk contract to spend the asset, but does not buy Pods yet.
9. Confirm the approval transaction in your wallet, and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../additional-resources/contracts.md) before signing it.
10. Select “Fill”.
11. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../additional-resources/contracts.md) before signing it.
12. After the transaction has been confirmed by the network, your Pods will appear in the “Pod Balance” table at the bottom of the “Field” page.

### Order Pods <a href="#_714q89jrln2n" id="_714q89jrln2n"></a>

1. Make sure you are on [app.bean.money](https://app.bean.money/).
2. Navigate to the “Market” page.
3. Select “Create New”. “Order” is selected by default, allowing you to create a Pod Order.
   * “Max Place in Line” is the maximum [Place in Line](../../additional-resources/glossary.md#pod-line) at which you are willing to buy Pods at the specified price. Any Pods at a lower Place in Line than the maximum Place in Line will be eligible to Fill the Pod Order.
   * “Price per Pod” is how much you will pay for each Pod, denominated in Beans.
   * “Order using” specifies the amount and the asset to be used to buy Pods. This amount will be locked in the Pod Order to allow for instant settlement. Pod Orders may be partially filled.
4. A transaction preview will appear below the inputs. Select the “Transaction Details” dropdown to review each step of the transaction.
5. You may select a slippage tolerance by selecting the gear icon. The default slippage tolerance is 0.1%.
6. If you are buying Pods with ETH, skip to Step 8. For all other assets, select “Approve \[Token]”. This allows the Beanstalk contract to spend the asset, but does not create the Pod Order yet.
7. Confirm the approval transaction in your wallet, and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../additional-resources/contracts.md) before signing it.
8. Select “Order”.
9. Confirm the transaction in your wallet and your hardware wallet, if applicable. You should verify that the transaction is interacting with the [correct contract](../../additional-resources/contracts.md) before signing it.
10. After the transaction has been confirmed by the network, your Pod Order will be shown on the [My Pod Market](https://app.bean.money/#/market/account) page under the “Orders” tab, where you can check the status of your Pod Order or Cancel it.
