# Convert

Conversions within the [Silo](../farm/silo.md) between Bean and LP Deposits serve a major role in peg maintenance.

Conversions from one Deposited asset to another are permissioned by a Convert Whitelist. Conversions can be added or removed from the Convert Whitelist via [Beanstalk governance](broken-reference).&#x20;

When the Bean price is above peg (_i.e._, [deltaB](../additional-resources/glossary.md#deltab) is positive), Deposited Beans may be converted to Deposited BEAN:3CRV LP while retaining grown Stalk from Seeds. This conversion allows the Silo Member to add Beans to liquidity pools, which has the effect of selling Beans above peg. In doing so, Beanstalk incentivizes Silo Members to grow liquidity for Beans at the expense of additional Bean mints, as the Bean price is arbitraged back towards peg.

When the Bean price is below peg (_i.e._, deltaB is negative), Deposited BEAN:3CRV LP may be converted to Deposited Beans while retaining grown Stalk from Seeds and without forfeiting any Stalk due to LP impermanent loss. This conversion allows Silo Members to remove excess Beans from liquidity pools and arbitrage the price back towards peg without leaving the Silo, minimizing debt issuance.

Unripe Beans are also convertible to Unripe BEAN:3CRV LP and vice versa in a similar fashion. See the [Unripe Assets](../farm/barn.md#unripe-assets) section of the [Barn](../farm/barn.md) page for more info.

In order for a given Conversion to be added to the Convert Whitelist, Beanstalk requires:

1. The From token address;
2. The To token address;
3. Conditions under which the From token can be Converted to the To token; and
4. A function to determine the number of To tokens received for Converting a given number of From tokens (see [Section 14.4 in the whitepaper](https://bean.money/docs/beanstalk.pdf) to see formulas).

#### Current Convert Whitelist <a href="#convert-whitelist" id="convert-whitelist"></a>

| From token          | To token            | Conditions                       |
| ------------------- | ------------------- | -------------------------------- |
| Bean                | BEAN:3CRV LP        | deltaB in the BEAN:3CRV pool > 0 |
| BEAN:3CRV LP        | Bean                | deltaB in the BEAN:3CRV pool < 0 |
| Unripe Bean         | Unripe BEAN:3CRV LP | deltaB in the BEAN:3CRV pool > 0 |
| Unripe BEAN:3CRV LP | Unripe Bean         | deltaB in the BEAN:3CRV pool < 0 |
