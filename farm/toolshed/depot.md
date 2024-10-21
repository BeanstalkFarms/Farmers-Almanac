# Depot

Current complex interactions with Arbitrum-native protocols are tedious, cumbersome and expensive. The Depot facilitates complex, gas-efficient interactions with other Arbitrum-native protocols in a single transaction.

Any protocol with a Pipeline to the Depot can be used via Beanstalk in a single transaction. Pipelines to the Depot can be added via [Beanstalk governance](../../governance/beanstalk/).

### Pipeline

The [Pipeline](../../ecosystem/pipeline.md) Pipeline allows anyone to perform an arbitrary series of actions in the EVM in a single transaction by using [0xb1bE000644bD25996b0d9C2F7a6D6BA3954c91B0](https://arbiscan.io/address/0xb1bE000644bD25996b0d9C2F7a6D6BA3954c91B0) as a sandbox for execution.

The following functions to interact with Pipeline can be called through the [Pipeline](../../ecosystem/pipeline.md) Pipeline.

* `pipe(...)`
* `multiPipe(...)`
* `advancedPipe(...)`
