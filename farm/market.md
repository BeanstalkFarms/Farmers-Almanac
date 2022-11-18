# Market

Current DEXs are unable to attract liquidity without offering protocol-native emissions. The value of these emissions derives primarily from AMM trading fees. Beanstalk’s ability to attract liquidity without fee-based emissions allows it to offer DEXs without trading fees.

The Market will house various DEXs for zero fee trading. For now, there is only the Pod Market, but in the future there may be a Deposit Market, an NFT Market, an ERC-20 Market, etc.

For guides on interacting with the Market through the Beanstalk UI, go [here](../guides/market/).

## **The Pod Market**

[Pods](field.md#pods) can be bought and sold in a decentralized, trustless fashion on the Pod Market. The Pod Market creates liquidity for Pods through an on-chain order book.

Sellers can List Pods or Fill open Pod Orders placed by buyers.&#x20;

Buyers can Order Pods or Fill open Pod Listings places by sellers.

### **Pod Listings**

{% hint style="info" %}
[BIP-29](https://arweave.net/OfWylBAxD5KyGJBWrQto2EyeYpzc-MqfaroXMQ1bk5w) implements Pod Listings with Price per Pod as a function of place in the Pod Line. Beanstalk has been [upgraded](https://etherscan.io/tx/0x5e1d4c9a4e1572fd6ba7b1c0cb105a244757d5aded40f4cc8f2f6520d9c3268f), but this functionality is not yet exposed via the app.bean.money UI.
{% endhint %}

Pods from Beans Sown in a single transaction form a Plot. Anyone with a Plot can List a whole or partial Plot for sale in exchange for Beans. This is known as a Pod Listing. Pod Listings have the following inputs:

| **Pod Listing Inputs**      | **Example**                      |
| --------------------------- | -------------------------------- |
| 1. Plot                     | Place in Line: 140M, Pods: 4,000 |
| 2. Position within the Plot | 2,000 to 4,000                   |
| 3. Price per Pod            | 0.80 Beans                       |
| 4. Expiration               | 30M Pods                         |

_1. Plot_

Farmers may own multiple Plots. Plots are identified by their place in the Pod Line.

_2. Position within the Plot_

As Pods are Harvested on a First In, First Out (FIFO) basis, if less than a whole Plot is Listed, the seller must choose which Pods within the Plot to List. A seller can List any contiguous set of Pods within a Plot. If only a portion of a Plot is Listed, the seller must choose which subset of Pods within that Plot are for sale. In the example above, the last 2,000 Beans in the Plot are Listed, while the first 2,000 (i.e. Pods 0 - 2,000) remain in the seller’s possession.

_3. Price per Pod_

The sale price of each Pod, denominated in Beans.

_4. Expiration_

The number of Pods that can Harvest before the expiration of the Listing. Setting this input to 30M Pods would remove this Listing from the Pod Market once 30M Pods are Harvested after the creation of the Listing.

A Pod Listing can be Cancelled at any time until it is entirely Filled. Plots can only be Listed in a single Pod Listing at a time. Pod Listings are automatically Cancelled if the owner of the Plot transfers or re-Lists any Pods in the Plot.

A Pod Listing can be entirely or partially Filled at any time by a buyer. If the Pod Listing is partially Filled, the rest of the Pod Listing remains Listed.

### **Pod Orders**

{% hint style="info" %}
[BIP-29](https://arweave.net/OfWylBAxD5KyGJBWrQto2EyeYpzc-MqfaroXMQ1bk5w) implements Pod Orders with Price per Pod as a function of place in the Pod Line. Beanstalk has been [upgraded](https://etherscan.io/tx/0x5e1d4c9a4e1572fd6ba7b1c0cb105a244757d5aded40f4cc8f2f6520d9c3268f), but this functionality is not yet exposed via the app.bean.money UI.
{% endhint %}

A Pod Order is an offer to buy Pods at a given price, before a given place in the Pod Line. Any seller may Fill a Pod Order by selling Pods according to the terms of the Order.

Anyone with Beans can Order Pods by creating a Pod Order. A Pod Order has the following inputs:

| **Pod Order Inputs**                      | **Example** |
| ----------------------------------------- | ----------- |
| 1. Maximum number of Pods to be purchased | 4,000 Pods  |
| 2. Price per Pod                          | 0.80 Beans  |
| 3. Maximum place in the Pod Line          | 140.0M      |

_1. Maximum number of Pods to be purchased_

Because Pod Orders can be partially or entirely Filled at any time by a seller, a Pod Order defines the maximum number of Pods the buyer would like to purchase at a given price.

_2. Price per Pod_

The price to be paid for each Pod, denominated in Beans.

_3. Maximum place in the Pod Line_

A Pod Order with a maximum place in the Pod Line of 140.0M could be Filled by any Pods with a position in the Pod Line of 140.0M or earlier. In general, Pods closer to the front of the Pod Line are more valuable, as they become Harvestable for Beans sooner due to the FIFO Harvest schedule.

A Pod Order can be Cancelled at any time until it is Filled. To facilitate instant clearance, Beans are locked in a Pod Order until it is entirely Filled or Cancelled. If the Pod Order is partially Filled, the rest of the Pod Order remains Listed.
