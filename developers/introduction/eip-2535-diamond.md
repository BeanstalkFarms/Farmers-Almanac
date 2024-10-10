# EIP-2535 Diamond

The Beanstalk contract is a Diamond – a multi-facet proxy defined in [EIP-2535](https://eips.ethereum.org/EIPS/eip-2535) that can implement functionality from numerous different Facet contracts.

All the Facets share a common storage through the [`AppStorage`](https://dev.to/mudgen/appstorage-pattern-for-state-variables-in-solidity-3lki) pattern. Functionality is shared between Facets through internal Libraries.

Understanding EIP-2535 really helps to understand Beanstalk. This page serves as a resource hub for EIP-2535.

**What is a Diamond?**

* [EIP-2535](https://eips.ethereum.org/EIPS/eip-2535)
* [Understanding Diamonds on Ethereum](https://dev.to/mudgen/understanding-diamonds-on-ethereum-1fb)
* [How Diamond Upgrades Work](https://dev.to/mudgen/how-diamond-upgrades-work-417j)

**Implementation Tips for Diamonds (which Beanstalk uses)**

* [AppStorage Pattern for State Variables in Solidity](https://dev.to/mudgen/appstorage-pattern-for-state-variables-in-solidity-3lki)
* [How to Share Functions Between Facets of a Diamond](https://dev.to/mudgen/how-to-share-functions-between-facets-of-a-diamond-1njb)
* [Accessing State Variables in Libraries](https://dev.to/mudgen/solidity-libraries-can-t-have-state-variables-oh-yes-they-can-3ke9)

**Why use a Diamond?**

* [Ethereum's Maximum Contract Size Limit is Solved with the Diamond Standard](https://dev.to/mudgen/ethereum-s-maximum-contract-size-limit-is-solved-with-the-diamond-standard-2189)
* [🌱 Beanstalk 🤝 EIP-2535 💎](https://publius.money/blog/2021-09-24-beanstalk-eip-2535)
* [Ethereum Diamonds Solve These Problems](https://dev.to/mudgen/ethereum-diamonds-solve-these-problems-3fmp)

**More Information on Diamonds**

* [Beanstalk on Louper, The Ethereum Diamond Inspector](https://louper.dev/diamond/0xc1e088fc1323b20bcbee9bd1b9fc9546db5624c5)
* [EIP-2535 Diamonds Discord](https://discord.gg/kQewPw2)
* [Nick Mudge <> Publius Podcast](https://www.youtube.com/watch?v=3-RUl12lPnI)
