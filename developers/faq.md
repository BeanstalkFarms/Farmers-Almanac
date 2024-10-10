# FAQ

#### Who calls the `gm` function? <a href="#who-calls-sunrise" id="who-calls-sunrise"></a>

In theory, anyone is able to call the `gm` function. In practice, MEV bots will front run your transaction by calling the function themselves as they can determine that they will get the Beans instead of you. As there are a number of bots playing the Sunrise game, the chances of getting a successful `gm` call from clicking the Sunrise button on the UI are essentially zero.

#### Where can I call functions directly on Beanstalk? <a href="#call-beanstalk-functions-with-louper" id="call-beanstalk-functions-with-louper"></a>

Louper allows users to directly call functions in a contract that implements EIP-2535, as Etherscan does not yet support this. The Beanstalk contract on Louper can be found [here](https://louper.dev/diamond/0xc1e088fc1323b20bcbee9bd1b9fc9546db5624c5).

#### Why do Beans only have 6 decimals? <a href="#beans-6-decimals" id="beans-6-decimals"></a>

Solidity has a limit of `2^256 - 1 ~= 1e77` for integers. Beanstalk is a complex protocol that does a lot of multiplication of big numbers which could potentially bring that upper integer limit into play, especially in the Flood functionality. Given that Bean is a stablecoin and the the value peg is $1, there is no need for an excessive amount of decimals. By reducing decimals to increase protocol security in the long run, Beanstalk is better set up for success. Note that USDC and Tether both have 6 decimals.

A lot of tokens have 18 decimals. Non-stable tokens have to be functional at any possible price at any point in the future.

Let's take the example of ETH and say that the ETH price is $4300. $0.01 is about 0.0000023 ETH. Thus, for ETH to be tradable at the cent level, it needs to have at least 7 decimals. Now fast forward 100 years and let's say (hypothetically) that ETH is worth $1,000,000,000. This would require ETH to have 11 decimals to be transacted at a cent level. Thus, it makes sense for ETH to have 18 decimals.

In terms of gas cost, there is no difference between 6 and 18 decimals.

#### How are proxy contracts used to upgrade Beanstalk? <a href="#proxy-contract-upgrades" id="proxy-contract-upgrades"></a>

Delegate calls in Solidity allow a smart contract to use functionality stored in another contract’s bytecode and apply it to its own memory.

Traditionally, an upgradeable contract is a proxy address with an implementation contract. All calls to the proxy use the logic stored in the implementation contract, but update the state of the proxy. Thus, by changing a proxy’s implementation address, one can change the functionality in a contract while maintaining the same state and address. You can read about it more on the OpenZeppelin docs [here](https://docs.openzeppelin.com/upgrades-plugins/1.x/proxies) and [here](https://docs.openzeppelin.com/learn/upgrading-smart-contracts).\
\
Beanstalk is actually a multi-facet proxy implementation called a Diamond. This implementation is defined by EIP-2535. [EIP-2535](https://eips.ethereum.org/EIPS/eip-2535) allows a single proxy to implement multiple smart contracts at the same time. You can read more about the reasoning behind EIP-2535 usage with Beanstalk [here](https://bean.money/blog/beanstalk-eip-2535).

#### What are Roots?

Roots were implemented in [BIP-0](https://bean.money/bip-0). Roots are an underlying accounting variable for Stalk in order to track how many Earned Beans a Farmer has earned. When a Farmer Deposits assets or Mows Grown Stalk, they are given Roots proportional to the Stalk they receive: `newStalk * totalRoots / totalStalk`.

When Beanstalk mints Beans, it increases `totalStalk` but not `totalRoots`, which in effect, increases `stalk / root`. When a Farmer Mows their Grown Stalk, the ratio: `farmerStalk / farmerRoots = totalStalk / totalRoots` is restored. (In this formula `farmerStalk` is equal to the Stalk they have after Mowing.)

`earnedStalk = farmerStalk - totalStalk / totalRoots * farmerRoots` (In this formula `farmerStalk` is equal to the Stalk they have before the Mow.) 1 Stalk = 1 Bean, so `earnedBeans = earnedStalk`.

#### Why build a zero fee AMM?

From an engineering perspective, building a zero fee AMM is simpler than building an AMM with fees—you can simply skip the code that implements the fee when a swap occurs.

From an economic perspective, the concept is that Silo yield is a sufficient enough incentive to attract and retain liquidity providers such that there is no need to charge a fee on swaps.

Why is having zero fees important? Given that whether `deltaB < 0` or `deltaB > 0` is a defining data point in how Beanstalk's peg maintenance operates, any fee on swaps creates a serious inefficiency in Farmers' ability to arbitrage the peg. The BEAN:3CRV pool charges a 0.04% on swaps (including Convert). This means that buying or Converting above the price of $0.9996 means you are paying more than $1 per Bean and selling or Converting below $1.0004 means you are getting less than $1 per Bean. Any Farmer who is constantly arbitraging the price within this range is losing money overtime instead of making a profit (which they should be). For reference, the BEAN:ETH pool previously had a 0.3% fee, which created an even more extreme inefficiency in peg maintenance.

In addition, Beanstalk can overtime become the primary liquidity provider for all of DeFi by providing the cheapest on-chain swaps between two non-Bean assets.

#### Why aren't Pods / Plots implemented with an ERC standard? <a href="#pods-plots-erc-721" id="pods-plots-erc-721"></a>

Plots function completely differently than both ERC-721 and ERC-1155. ERC-1155 doesn't work for Plots/Pods as Pods require ordinality for FIFO Harvesting. ERC-721 could work for Pods, but its hard to see how this would add value. ERC-721 tokens are non-divisible, so it would only allow entire Plots to be bought and sold on NFT marketplaces, which is far less efficient that the current Pod Market. Implementing Pods as ERC-721 would increase the cost of Sowing, Harvesting, Transferring, buying and selling.

#### Why doesn't Fertilizer.sol have an `initialize` function? <a href="#fertilizer-initialize" id="fertilizer-initialize"></a>

When Fertilizer was originally deployed. It was deployed as the `FertilizerPreMint.sol` contract, which has an `initialize` function that calls `__Internallize_init` [here](https://github.com/BeanstalkFarms/Beanstalk/blob/master/protocol/contracts/fertilizer/FertilizerPreMint.sol#L39.). The `initialize` function was run on deployment. When Beanstalk was Replanted, The Fertilizer proxy contract was upgraded to the `Fertilizer` contract found [here](https://github.com/BeanstalkFarms/Beanstalk/blob/master/protocol/contracts/fertilizer/Fertilizer.sol). This is the current implementation contract you see on Etherscan. There was no additional initialization needed as `__Internallize_init` was already executed. Thus, the `Fertilizer` contract has no need to have an external `initialize` function.

#### Why is the BDV of urBEAN3CRV lower than the BDV of urBEAN? <a href="#bdv-urbean3crv-urbean" id="bdv-urbean3crv-urbean"></a>

On October 25, 2022, two values could be found on the [Beanstalk Data Dashboard](https://beanstalk-dashboard.netlify.app/):

* Underlying per urBEAN3CRV: `0.219823021543684162`
* Underlying per urBEAN: `0.222227`
* Dividing the two numbers: `0.219823021543684162/0.222227 = 0.9891823`

This implies that 1 urBEAN3CRV will only ripen into 0.9891823 BEAN3CRV (i.e., not 1 BEAN3CRV) when Beanstalk is full recapitalized, assuming there are no Chops, no fees, deltaB = 0 and 1 BEAN3CRV = 1 BEAN. 1 urBEAN will ripen into 1 BEAN.

There are numerous reasons for this discrepancy, but the most significant is that `deltaB > 0` when the exploit occurred, so the BDV of LP tokens at the time was less than 1.

#### Why are Beans minted for a Fundraiser just to later burn them? <a href="#beans-minted-fundraiser-burn" id="beans-minted-fundraiser-burn"></a>

See `FundraiserFacet.sol` (now deprecated).

Fundraisers are meant to mimic an OTC swap where the buyer trades some stablecoin for a Bean and then automatically Sows the bought Beans for Pods, similar to how the credit mechanism to sustain the peg works. As defined in the whitepaper, Sowing requires a Bean to be burned in exchanged for the Pods. At the start of the Fundraiser, Beans are minted. These Beans represent (1) expected "sell pressure" for Beans as they can be sold at anytime for 1 stablecoin (normally USDC) and (2) expected Pod issuance given that the Beans will be Sown into Pods.

### Algorithm Explanations

#### [**`remainingRecapitalization`**](https://github.com/BeanstalkFarms/Beanstalk/blob/f0e29aae99ddca90085d8dfdc990cff88451d357/protocol/contracts/libraries/LibFertilizer.sol#L136) <a href="#remaining-capitalization" id="remaining-capitalization"></a>

`totalDollars` is the total dollar value required to be raised in the Barn Raise. It is equal to `dollarPerUnripeLP() * unripeLP().totalSupply()`. If no Farmer has forfeited Unripe LP, then `totalDollars` is 77 million, but given that Farmer's can `chop` their Unripe LP and forfeit the funds they have not yet been paid back, we need `totalDollars` to decrease with the total supply of Unripe LP.

**`if (s.recapitalized >= totalDollars) return 0;`** —

A safe guard in case Beanstalk ends up in a situation where too much is raised. This is also possible if someone uses the `chop` function at a penalty even after the full amount has been raised.

**`return totalDollars.sub(s.recapitalized);`** —

`s.recapitalized` is incremented every time USDC is exchanged for Fertilizer (or Unripe LP is generated through Convert), but it is equal to the dollar value that has been recapitalized. Thus, the difference between the two is the amount remaining.

#### [**`checkForMaxDeltaB`**](https://github.com/BeanstalkFarms/Beanstalk/blob/ddf3869bcdf7f7802eabe83d6abeebdfc7b8d1ab/protocol/contracts/libraries/Oracle/LibCurveOracle.sol#L152) <a href="#check-for-max-deltab" id="check-for-max-deltab"></a>

See [EBIP-2](https://bean.money/ebip-2).

It is assumed that if `|deltaB| > beanSupply / 100`, then manipulation occurred. This isn't always true, but the ramifications if `|deltaB| > beanSupply / 100` naturally are minimal as Beanstalk will simply mint fewer Beans/less Soil this Season.

Theoretically, a multi-block MEV attack could manipulate `deltaB` to be any value. Multi-block MEV can only be executed on some time cadence dependent on % ownership of Ethereal stake. Therefore, the greatest vulnerability to Beanstalk is a massive one-time Bean/Soil issuance. By adding this supply cap, the maximum effect of potential manipulation can be at most 1% of supply.
