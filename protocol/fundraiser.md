# Fundraiser

Fundraisers allow Beanstalk to issue Pods in exchange for dollar-pegged assets other than Beans and independent of the [Soil minting schedule](../peg-maintenance/overview.md#soil-supply) in order to raise funds to facilitate payments in other currencies (e.g., to cover the cost of an audit). Doing so in a way that does not directly affect Beanstalk’s normal peg maintenance model is ideal. Fundraisers are created via [Beanstalk governance](../governance/beanstalk/).

Each Fundraiser requires (1) a token address of the token to raise, (2) the number of tokens to raise, and (3) the wallet address to send the tokens to upon completion of the Fundraiser.

The selected dollar-pegged asset can be exchanged for 1 Bean’s worth of [Pods](../farm/field.md#pods) each, based on the [Temperature](../farm/field.md#temperature) at the time of the contribution to the Fundraiser. Tokens raised via a Fundraiser cannot be distributed until the entire Fundraiser is complete.

Past BIPs that created Fundraisers:

* [BIP-4: Trail of Bits Audit](https://arweave.net/Msk8Mbz7CPDN8vmQmMI8dtqCr4ydTZ8jN1jpPFqQ9lM)
* [BIP-5: Omniscia Audit](https://arweave.net/EGXO6x0ko5mAaT45G22Sq4Gfh5qMi9KgM1zzRlQedLA)
* [BIP-10: Omniscia Retainer](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/blob/master/bip/bip-10-omniscia-retainer.md)
