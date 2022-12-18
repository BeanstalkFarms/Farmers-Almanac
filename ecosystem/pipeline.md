# Pipeline

Pipeline is a sandbox contract that can execute an arbitrary number of actions within the EVM from an EOA in a single transaction.

Pipeline enables the execution an arbitrary composition of valid actions within the EVM in a single transaction using Ether. Depot is a wrapper for Pipeline that supports (1) loading Ether and non-Ether assets into Pipeline, (2) using them and (3) unloading them from Pipeline, in a single transaction. Clipboard defines an Advanced Function Call (AFC) architecture that allows subsequent function calls to use the `returnData` of previous ones in a configurable fashion. The combination of Pipeline, Depot and Clipboard allows EVM users to perform arbitrary valid actions, through arbitrarily many protocols, in a single transaction.

### Links

Website: [https://evmpipeline.org](https://evmpipeline.org/)

Whitepaper: [https://evmpipeline.org/pipeline.pdf](https://evmpipeline.org/pipeline.pdf)

GitHub: [https://github.com/BeanstalkFarms/evmpipeline](https://github.com/BeanstalkFarms/evmpipeline)

Halborn Audit Report: [https://bean.money/11-15-22-pipeline-halborn-report](https://bean.money/11-15-22-pipeline-halborn-report)
