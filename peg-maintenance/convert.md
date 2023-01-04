# Convert

Conversions within the [Silo](../farm/silo.md) between Bean and LP Deposits serve a major role in peg maintenance.

Conversions from one Deposited asset to another are permissioned by a Convert Whitelist. Conversions can be added or removed from the Convert Whitelist via [Beanstalk governance](broken-reference).&#x20;

When the Bean price is above peg (_i.e._, [deltaB](../protocol/glossary.md#deltab) is positive), Deposited Beans may be converted to Deposited BEAN:3CRV LP while retaining grown Stalk from Seeds. This conversion allows the Silo Member to add Beans to liquidity pools, which has the practical effect of selling Beans above peg. In doing so, Beanstalk incentivizes Silo Members to grow liquidity for Beans at the expense of additional Bean mints, as the Bean price is decreased back towards peg.

When the Bean price is below peg (_i.e._, deltaB is negative), Deposited BEAN:3CRV LP may be converted to Deposited Beans without forfeiting grown Stalk from Seeds or any Stalk due to LP impermanent loss. This conversion allows Silo Members to remove excess Beans from liquidity pools and increase the price back towards peg without leaving the Silo, minimizing debt issuance.

Unripe Beans are also convertible to Unripe BEAN:3CRV LP, and vice versa, in a similar fashion. See the [Unripe Assets](../farm/barn.md#unripe-assets) section of the [Barn](../farm/barn.md) page for more info.

### Convert Whitelist

In order for a Farmer to be able to Convert a Deposited asset to another, that given Conversion must be on the Convert Whitelist.

Additional Conversions may be added to the Convert Whitelist via [Beanstalk governance](broken-reference). In order for a Conversion to be added to the Convert Whitelist, Beanstalk requires:

1. The From token address;
2. The To token address;
3. Conditions under which the From token can be converted to the To token; and
4. A function to determine the number of To tokens received for Converting a given number of From tokens (see [Section 14.4 in the Whitepaper](https://bean.money/beanstalk.pdf#subsection.14.4) to see formulas).

#### Current Convert Whitelist

| From token                           | To token                     | Conditions                       |
| ------------------------------------ | ---------------------------- | -------------------------------- |
| Bean                                 | BEAN:3CRV LP                 | deltaB in the BEAN:3CRV pool > 0 |
| BEAN:3CRV LP                         | Bean                         | deltaB in the BEAN:3CRV pool < 0 |
| Unripe Bean                          | Unripe BEAN:3CRV LP          | deltaB in the BEAN:3CRV pool > 0 |
| Unripe BEAN:3CRV LP                  | Unripe Bean                  | deltaB in the BEAN:3CRV pool < 0 |
| Any token on the Deposit Whitelist\* | The same token as From token | Anytime                          |

\*Any token on the [Deposit Whitelist](../farm/silo.md#deposit-whitelist) can be Converted to the same token in order to allow Silo Members to updated the BDV of their LP tokens when their BDV increases due to impermanent loss.

#### Performance

Convert functionality was first added in [BIP-7](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/blob/master/bip/bip-07-convert.md), and generalized to support a Convert Whitelist in [BIP-21](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/blob/master/bip/bip-21-replant.md). Since BIP-7 was committed, Conversions by Silo Members have played a significant role in peg maintenance.

<figure><img src="../.gitbook/assets/Screen Shot 2022-09-12 at 10.39.44 AM.png" alt=""><figcaption><p>This screenshot of the Bean price chart is from September 12, 2022. See <a href="https://app.bean.money/">app.bean.money</a> for the latest data.</p></figcaption></figure>
