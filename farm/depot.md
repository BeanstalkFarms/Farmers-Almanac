# Depot

{% embed url="https://drive.google.com/file/d/1PwIY4YZeaEZfiKfw6j3vzt5LtFrCtS0_/view?usp=share_link" %}
Publius explains the Depot
{% endembed %}

Current complex interactions with Ethereum-native protocols are tedious, cumbersome and expensive. The Depot facilitates complex, gas-efficient interactions with other Ethereum-native protocols in a single transaction.&#x20;

Any protocol with a Pipeline to the Depot can be used via Beanstalk in a single transaction. Pipelines to the Depot can be added via [Beanstalk governance](../governance/beanstalk/).

### Curve

The Curve Pipeline allows anyone to call functions in any pool registered in any of the following Curve registries.

* [0xB9fC157394Af804a3578134A6585C0dc9cc990d4](https://etherscan.io/address/0xB9fC157394Af804a3578134A6585C0dc9cc990d4#readContract)
* [0x90E00ACe148ca3b23Ac1bC8C240C2a7Dd9c2d7f5](https://etherscan.io/address/0x90E00ACe148ca3b23Ac1bC8C240C2a7Dd9c2d7f5#readContract)
* [0x8F942C20D02bEfc377D41445793068908E2250D0](https://etherscan.io/address/0x8F942C20D02bEfc377D41445793068908E2250D0#readContract)

The following functions to interact with Curve pools can be called through the Curve Pipeline:

* `exchange(...)`
* `exchange_underlying(...)`
* `add_liquidity(...)`
* `remove_liquidity(...)`
* `remove_liquidity_imbalanced(...)`
* `remove_liquidity_one_token(...)`

### Pipeline

The [Pipeline](../ecosystem/pipeline.md) Pipeline allows anyone to perform an arbitrary series of actions in the EVM in a single transaction by using [0xb1bE0000bFdcDDc92A8290202830C4Ef689dCeaa44](https://etherscan.io/address/0xb1bE0000bFdcDDc92A8290202830C4Ef689dCeaa#readContract) as a sandbox for execution.

The following functions to interact with Pipeline can be called through the [Pipeline](../ecosystem/pipeline.md) Pipeline.

* `pipe(...)`
* `multiPipe(...)`
* `advancedPipe(...)`
