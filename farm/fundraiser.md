# Fundraiser

Fundraisers allow Beanstalk to issue Pods in exchange for dollar-pegged assets other than Beans and independent of the [Soil minting schedule](../peg-maintenance/overview.md#soil-supply) in order to raise funds to facilitate payments in other currencies (e.g., to cover the cost of an audit). Doing so in a way that does not directly affect Beanstalk’s normal peg maintenance model is ideal. Fundraisers are created via [Beanstalk governance](../governance/beanstalk/).

Each Fundraiser requires (1) a token address of the token to raise, (2) the number of tokens to raise, and (3) the wallet address to send the tokens to upon completion of the Fundraiser.

The selected dollar-pegged asset can be exchanged for 1 Bean’s worth of [Pods](field.md#pods) each, based on the [Temperature](field.md#temperature) at the time of the contribution to the Fundraiser. Tokens raised via a Fundraiser cannot be distributed until the entire Fundraiser is complete.

Past BIPs that created Fundraisers:

* [BIP-4: Trail of Bits Audit](https://github.com/BeanstalkFarms/Beanstalk/blob/master/bips/bip-4.md)
* [BIP-5: Omniscia Audit](https://github.com/BeanstalkFarms/Beanstalk/blob/master/bips/bip-5.md)
* [BIP-10: Omniscia Retainer](https://github.com/BeanstalkFarms/Beanstalk/blob/master/bips/bip-10.md)
