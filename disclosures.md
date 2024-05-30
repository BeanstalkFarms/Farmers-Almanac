# Disclosures

**Before interacting with Beanstalk, consider reading the following disclosures** **prepared by the Beanstalk DAO. This document can be found on Arweave** [**here**](https://bean.money/disclosures)**.**

Interacting with Beanstalk involves many risks. Before interacting with Beanstalk, you should review the relevant documentation to make sure you understand how Beanstalk works, as well as information about the current state of Beanstalk. The Beanstalk DAO has created this set of disclosures to assist in the educational process. These disclosures are not exhaustive. The [Beanstalk whitepaper](https://bean.money/beanstalk.pdf), the [Farmers' Almanac](./), and other Beanstalk resources, as well as participating in the Beanstalk community, can help to understand the protocol. Before participating in the protocol, everyone should do their own research, investigation and analysis.

Transparency is the cornerstone of DeFi. The Beanstalk DAO endeavors to be as transparent as possible, particularly as it pertains to communicating the risks of interacting with Beanstalk.

#### **1. BEANSTALK WAS ATTACKED ON APRIL 17, 2022 VIA ON-CHAIN GOVERNANCE. ALL \~$77M IN NON-BEAN ASSETS WERE STOLEN. PROTOCOL GOVERNANCE HAS BEEN CHANGED TO A 5-OF-9 COMMUNITY MULTISIG.** <a href="#governance-exploit" id="governance-exploit"></a>

On April 17, 2022, Beanstalk was attacked via on-chain governance resulting in a theft of all \~$77M in non-Beanstalk user assets. The attacker used a flash loan to compromise the governance mechanism and steal the assets deposited in the DAO.

Shortly after the attack, Beanstalk was Paused and on-chain governance was removed. Since the attack, governance votes have taken place on Snapshot. Beanstalk is now owned by a community-run multisig wallet (the Beanstalk Community Multisig, or BCM) responsible for executing the will of the DAO as indicated via Snapshot vote. The keys to the BCM are custodied by a group of nine anonymous Beanstalk community members and contributors. All contract changes under the BCM structure require the signature of 5-of-9 BCM signers. This serves as a temporary security measure until either (1) a secure and fully decentralized governance mechanism has been developed and sufficiently audited, or (2) governance is removed altogether.&#x20;

The [old Bean token](https://etherscan.io/token/0xdc59ac4fefa32293a95889dc396682858d52e5db) was replaced with a [new one](https://etherscan.io/address/0xBEA0000029AD1c77D3d5D23Ba2D8893dB9d1Efab). The obsolete token has no value according to Beanstalk.

More information:

* [Past BIPs](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/tree/master/bip)
* [Beanstalk Governance Exploit](https://bean.money/blog/beanstalk-governance-exploit)
* [BCM Process](governance/beanstalk/bcm-process.md)

#### **2. THERE IS NO MAXIMUM BEAN SUPPLY. THE BEAN SUPPLY CAN GROW INFINITELY THROUGH DEMAND-BASED MINTING AND GOVERNANCE.** <a href="#infinite-supply" id="infinite-supply"></a>

Beanstalk increases the Bean supply every Season where the liquidity and time weighted average price of 1 Bean is greater than $1 over the previous Season. Enough Beans are minted such that if all the newly minted Beans were sold, the Bean price would return to $1. Those Beans are distributed to Stalkholders, Pod holders and Active Fertilizer holders.

The Bean supply is uncapped and grows as demand for Beans increases. Beans can also be minted arbitrarily through governance (see [#7](disclosures.md#governance-risk)).

More information:

* [Beanstalk Analytics Links](community/links.md#analytics)
* [Whitepaper, Section 8.10, Bean Supply](https://bean.money/beanstalk.pdf#subsection.8.10)
* [Bean Supply Documentation](peg-maintenance/overview.md#bean-supply)

#### **3. BEANSTALK DID NOT HAVE A PRE-MINE, PRE-SALE, OR TEAM ALLOCATION. ALL BEANS HAVE BEEN MINTED IN ACCORDANCE WITH EITHER THE MINTING SCHEDULE OR GOVERNANCE.** <a href="#no-pre-mine" id="no-pre-mine"></a>

Beanstalk did not have a pre-mine, pre-sale or team allocation of any kind. The first 100 Beans were minted when the `init` function was called to deploy Beanstalk.

Beanstalk launched without the need to raise capital. However, after an on-chain governance attack on April 17, 2022 (see [#1](disclosures.md#governance-exploit)), a fundraiser known as the Barn Raise is being used to recapitalize the non-Bean funds stolen in the exploit. The terms offered in the fundraiser are available to any Ethereum address.

More information:

* [BFP-72: The Path Forward, No Haircuts](https://bean.money/bfp-72)
* [Whitepaper, Section 7, Barn](https://bean.money/beanstalk.pdf#section.7)
* [Barn Raise Documentation](farm/barn.md)

#### **4. BEANSTALK RELIES ON THIRD PARTIES TO PROVIDE CREDIT TO RETURN THE BEAN PRICE TO ITS PEG. THERE IS NO LENDER OF LAST RESORT.** <a href="#credit-risk" id="credit-risk"></a>

Beanstalk uses a credit based model, allowing anyone to lend Beans to the protocol to participate in peg maintenance. Beanstalk burns any Beans it borrows. As a consequence, the ability of the protocol to return the price of a Bean to the peg relies on the availability of willing creditors, which is not guaranteed. The economic design of Beanstalk fails if it can no longer attract creditors.

More information:

* [Whitepaper, Section 6, Field](https://bean.money/beanstalk.pdf#section.6)
* [Field Documentation](farm/field.md)

#### **5. BEANSTALK DOES NOT GUARANTEE THE BEAN PRICE. INSTEAD BEANSTALK INCENTIVIZES THE REGULAR OSCILLATION OF THE BEAN PRICE ABOVE AND BELOW ITS PEG THROUGH PROTOCOL-NATIVE INCENTIVES.** <a href="#oscillations" id="oscillations"></a>

Bean is not a collateralized stablecoin and Beanstalk offers no guarantee of the value of Bean. Beanstalk was deployed on August 6, 2021, and since then, the Bean price has crossed its dollar peg thousands of times. Even so, Beanstalk is still in an early stage and various parts of its economic design continue to be improved through governance.

Beanstalk tries to incentivize the regular oscillation of the Bean price above and below its peg. While the protocol's incentives are designed to return the price of a Bean to its peg, the timing of oscillations is indeterminate. The price will almost never be exactly equal to its peg. Crossing the peg in the past is no guarantee of it happening again in the future.

More information:

* [Whitepaper, Section 8.1, Ideal Equilibrium](https://bean.money/beanstalk.pdf#subsection.8.1)
* [Peg Maintenance Documentation](farm/overview.md)

#### **6. BEANSTALK-NATIVE DEBT DOES NOT HAVE A MATURITY DATE AND THEREFORE MAY NEVER BECOME REDEEMABLE FOR BEANS.** <a href="#debt-maturity-risk" id="debt-maturity-risk"></a>

Beanstalk borrows Beans from lenders in exchange for Pods and Sprouts. Bean loans have fixed interest rates but do not have fixed maturity dates.

Pods and Sprouts are repaid when the liquidity and time weighted average price of 1 Bean is greater than $1 over the previous Season, but there is no guarantee this will continue until all Pods and Sprouts become redeemable (see [#4](disclosures.md#credit-risk)). Governance may also arbitrarily modify the redeemability of Beanstalk debt (see [#7](disclosures.md#governance-risk)).

More information:

* [Whitepaper, Section 11.2, Strong Credit](https://bean.money/beanstalk.pdf#subsection.11.2)
* [Economics Documentation](advanced/economics.md)

#### **7. STALKHOLDERS CAN MAKE ARBITRARY CHANGES TO BEANSTALK THROUGH GOVERNANCE, IF ENACTED BY THE BEANSTALK COMMUNITY MULTISIG. THERE IS NO GUARANTEE THE CHANGES WILL BE BENEFICIAL TO BEANSTALK.** <a href="#governance-risk" id="governance-risk"></a>

Beanstalk is governed by the Beanstalk DAO—the Silo, which is comprised of Stalkholders. Stalkholders vote on Beanstalk Improvement Proposals (BIPs), which can arbitrarily change Beanstalk. Voting rights come from Stalk ownership (see [#8](disclosures.md#earlier-depositor-governance-power) for details on Stalk).

Any community member that meets a certain Stalk ownership threshold may propose a BIP. If the BIP passes, the Beanstalk Community Multisig (see [#9](disclosures.md#multisig-risk) for details on the BCM) executes the will of the DAO based on the results of the vote, unless the Stalk distribution is compromised in a flash loan or other governance attack. Through this governance process, Stalkholders may make arbitrary changes to Beanstalk.

More information:

* [Beanstalk DAO Snapshot](https://snapshot.org/#/beanstalkdao.eth/)
* [Past BIPs](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/tree/master/bip)

#### **8. ANYONE CAN RECEIVE STALK BY DEPOSITING WHITELISTED ASSETS IN THE SILO. EARLIER DEPOSITORS IN THE SILO HAVE PROPORTIONALLY GREATER GOVERNANCE POWER RELATIVE TO THE BEAN DENOMINATED VALUE ORIGINALLY DEPOSITED.** <a href="#earlier-depositor-governance-power" id="earlier-depositor-governance-power"></a>

Depositors earn Stalk and Seeds. Seeds yield 1/10000 new Stalk every Season. Stalkholders participate in governance and earn Bean seigniorage. Stalk ownership, and thus governance power, decentralizes over time.

As earlier Depositors in the Silo have been accruing Stalk from Seeds for more Seasons compared to later Depositors, these Depositors have greater governance power in proportion to the Bean Denominated Value (BDV) of their original Deposits.

More information:

* [Whitepaper, Section 5.1, The Stalk System](https://bean.money/beanstalk.pdf#subsection.5.1)
* [The Stalk System Documentation](farm/silo/#the-stalk-system)

#### **9. THE BEANSTALK CONTRACT IS OWNED BY THE BEANSTALK COMMUNITY MULTISIG. THE MULTISIG CAN MAKE ARBITRARY CHANGES TO BEANSTALK WITH 5-OF-9 SIGNATURES FROM THE ANONYMOUS SIGNERS. THERE IS NO GUARANTEE THE MULTISIG ENACTS THE GOVERNANCE DECISIONS OF THE DAO.** <a href="#multisig-risk" id="multisig-risk"></a>

Ownership of the Beanstalk contracts is held by a 5-of-9 multisig known as the Beanstalk Community Multisig (BCM). The BCM is an extension of the Beanstalk DAO. The BCM's role is to enact on-chain the decisions Stalkholders make via off-chain voting on Snapshot. Besides Publius (one of the members), all members of the BCM are anonymous. Publius selects the other members, who Publius believes will act in the best interest of Beanstalk. This process was approved via governance.

Off-chain governance introduces significant risks related to security and censorship. The BCM is designed to mitigate as many of those risks as possible by distributing the multisig keys across reputable community members and Beanstalk core contributors, and collectively implementing and adhering to a set of best practices. There is no guarantee the BCM enacts the governance decisions the DAO voted on via Snapshot.

More information:

* [BFP-73: Beanstalk Community Multisig](https://bean.money/bfp-73)
* [BCM Multisig Powers Documentation](governance/beanstalk/bcm-process.md#multisig-powers)
* [Anonymous Multisig Signers Documentation](governance/beanstalk/bcm-process.md#anonymous-signers)
* [BCM Dashboard](governance/beanstalk/bcm-dashboard.md)

#### **10. MOST BEANSTALK FUNCTIONS CAN BE ARBITRARILY REMOVED BY HYPERNATIVE, A PROACTIVE THREAT PREVENTION AND REAL-TIME MONITORING PLATFORM. THERE IS NO GUARANTEE THAT FUNCTIONS ARE ONLY REMOVED WHEN APPROPRIATE.** <a href="#hypernative" id="hypernative"></a>

The Beanstalk DAO implemented Hypernative into Beanstalk, a proactive threat prevention and real-time monitoring platform. Hypernative has the ability to remove any Beanstalk function unrelated to the Ethereum Diamond and upgradability of Beanstalk.

Hypernative introduces significant risks related to security and censorship. There is no guarantee that:

* Hypernative only removes functions during high confidence pre-exploit and exploit-in-progress detections;&#x20;
* The BCM will remove Hypernative protections when necessary for the security or censorship resistance of Beanstalk; or that&#x20;
* The BCM only removes Hypernative protections when it beneficial to Beanstalk.

More information:

* [Hypernative](https://hypernative.io/)
* [BIP-46: Hypernative](https://arweave.net/2enPPzc5mkN18bXnApmCJNRkxwYc-CiCsU71XPualj4)
* [Emergency Response Procedures Documentation](governance/beanstalk/bcm-process.md#hypernative)

#### **11. AS GOVERNANCE POWER IS DETERMINED THROUGH STALK OWNERSHIP, SUFFICIENT CAPITAL COULD PURCHASE SIGNIFICANT GOVERNANCE POWER AND TAKE OVER BEANSTALK.** <a href="#stalk-governance-power" id="stalk-governance-power"></a>

Beanstalk is governed by Stalkholders, as described in [#7](disclosures.md#governance-risk). Stalk ownership, and thus governance power, decentralizes over time given the inflationary nature of Stalk. However, there is no maximum Stalk supply. Stalk is minted for Deposits based on the Bean Denominated Value (BDV) of the Deposit, up to any arbitrary BDV.

Stalk ownership was previously compromised via flash loan, which enabled the on-chain governance attack on April 17, 2022 (see [#1](disclosures.md#governance-exploit)). The Beanstalk Community Multisig serves as a temporary security measure until either (1) a secure and fully decentralized governance mechanism has been developed and sufficiently audited, or (2) governance is removed altogether.&#x20;

More information:

* [Whitepaper, Section 5.1, The Stalk System](https://bean.money/beanstalk.pdf#subsection.5.1)
* [BCM Process](governance/beanstalk/bcm-process.md)

#### **12. A VULNERABILITY IN ETHEREUM COULD RESULT IN A LOSS OF FUNDS. BEANSTALK ASSUMES THE SECURITY OF ETHEREUM.** <a href="#ethereum-risk" id="ethereum-risk"></a>

Ethereum is the largest smart contract blockchain by market capitalization, total value deposited, and dollar denominated transaction value. In general, open source networks with large amounts of value on them and long track records indicate security, but there is no guarantee. Beanstalk assumes the security of the Ethereum network.

#### **13. A VULNERABILITY IN BASIN OR ITS COMPONENTS COULD RESULT IN A LOSS OF FUNDS. BEANSTALK ASSUMES THE SECURITY OF BASIN AND ITS CORRESPONDING COMPONENTS.** <a href="#basin-risk" id="basin-risk"></a>

Beans trade in the BEAN:ETH Well on Basin. The LP token is whitelisted in the Silo and the Well is used by Beanstalk to determine how many Beans and/or Soil to mint. Basin and the corresponding components that Beanstalk uses (the Constant Product Well Function, the Well Implementation, Multi Flow, etc.) were audited by [Halborn](https://halborn.com/), [Cyfrin](https://www.cyfrin.io/) and [Code4rena](https://code4rena.com/). While all are reputable auditors, there is no guarantee that Basin or its components are secure. Beanstalk assumes the security of Basin and its corresponding components.

More information:

* [BIP-37: Basin Integration](https://bean.money/bip-37)
* [Basin Audit Reports](https://github.com/BeanstalkFarms/Beanstalk-Audits#ecosystem-audit-reports-on-arweave)
* [Basin Whitepaper](https://basin.exchange/basin.pdf)
* [Multi Flow Pump Whitepaper](https://basin.exchange/multi-flow-pump.pdf)

#### **14. A VULNERABILITY IN UNISWAP V3 COULD RESULT IN A LOSS OF FUNDS. BEANSTALK ASSUMES THE SECURITY OF UNISWAP V3.** <a href="#uniswap-v3-risk" id="uniswap-v3-risk"></a>

Beanstalk uses the ETH:USDC and ETH:USDT Uniswap V3 pools to derive the price of a dollar on-chain (see [#18](disclosures.md#oracle-risk)). Uniswap V3 is among the largest Ethereum-native decentralized exchange protocols by volume. In general, open source protocols with large amounts of value on them and long track records indicate security, but there is no guarantee. Beanstalk assumes the security of Uniswap V3.

More information:

* [BIP-37: Basin Integration](https://bean.money/bip-37)
* [Whitepaper, Section 8.2, Decentralized Price Oracle](https://bean.money/beanstalk.pdf#subsection.8.2)
* [Decentralized Price Oracle Documentation](peg-maintenance/overview.md#decentralized-price-oracle)

#### **15. A VULNERABILITY IN PIPELINE COULD RESULT IN A LOSS OF FUNDS. BEANSTALK ASSUMES THE SECURITY OF PIPELINE.** <a href="#pipeline-risk" id="pipeline-risk"></a>

Through Beanstalk, users can perform complex, gas-efficient interactions with other Ethereum-native protocols, like Pipeline. Pipeline is a sandbox contract allows anyone to perform an arbitrary series of actions in the EVM in a single transaction.

Pipeline was audited by Halborn, but there is no guarantee that Pipeline is secure. Beanstalk assumes the security of Pipeline.

More information:

* [BIP-30: Generalized Pipeline](https://bean.money/bip-30)
* [Pipeline Audit Report](https://evmpipeline.org/pipeline-audit-halborn.pdf)
* [Pipeline Whitepaper](https://evmpipeline.org/pipeline.pdf)
* [Whitepaper, Section 10, Depot](https://bean.money/beanstalk.pdf#section.10)
* [Depot Documentation](farm/depot.md)

#### **16. THE BEAN PRICE IS DERIVED FROM THE VALUE OF ASSETS IT TRADES AGAINST IN DECENTRALIZED AMMS. THERE IS NO GUARANTEE ANY OF THESE ASSETS RETAIN VALUE.** <a href="#non-bean-liquidity-risk" id="non-bean-liquidity-risk"></a>

The value of Beans is derived from the non-Bean assets trading against it in decentralized liquidity pools. Each of these assets have their own set of associated risks, unique to the asset. Beanstalk implicitly assumes risk associated with these assets.

#### **17. BECAUSE BEANS DERIVE THEIR VALUE FROM THE ASSETS THEY TRADE AGAINST, AND NOT COLLATERAL, IT IS NOT POSSIBLE FOR ALL BEAN HOLDERS TO EXIT AT A DOLLAR OF VALUE FOR EVERY BEAN.** <a href="#not-all-bean-holders-can-exit-at-a-dollar-of-value" id="not-all-bean-holders-can-exit-at-a-dollar-of-value"></a>

Beans are not redeemable for any other asset; they can only be traded for another asset that Beans are trading against. As Bean holders sell their Beans, there is less and less value trading against Beans. Thus, unlike collateralized stablecoins, it is not possible for the Bean supply to scale down to zero with every Bean holder getting a dollar of value for every Bean sold.

#### **18. BEANSTALK REQUIRES TRUSTLESS AND RELIABLE ACCESS TO A MANIPULATION RESISTANT PRICE ORACLE FOR A DOLLAR. BEANSTALK USES A CHAINLINK DATA FEED AND THE ON-CHAIN PRICES OF OTHER STABLECOINS TO DETERMINE THE PRICE OF A DOLLAR. THERE IS RISK ASSOCIATED WITH BOTH OF THESE METHODS THAT CAN COMPROMISE THEIR INTEGRITY AS ACCURATE PRICE ORACLES.** <a href="#oracle-risk" id="oracle-risk"></a>

Beanstalk's core objective is to oscillate the price of a Bean above and below its dollar peg. To do this, Beanstalk must be able to reliably measure the price of a dollar on-chain without trusting a centralized third-party to provide it. A robust, decentralized stablecoin requires a tamper-proof, manipulation resistant and decentralized price oracle.

Beanstalk measures the price of a dollar in each pool on the Minting Whitelist:

* For the BEAN:ETH Well, Beanstalk assumes the price returned by the ETH/USD Chainlink data feed is accurate if it is close enough to either the ETH:USDC Uniswap V3 pool or the ETH:USDT Uniswap V3 pool.

A disruption in the reliability of USDC, USDT, DAI or the ETH/USD Chainlink data feed could impact Bean minting, resulting in adverse consequences for Beanstalk. The Chainlink data feed is inherently centralized.

More information:

* [Whitepaper, Section 8.2, Decentralized Price Oracle](https://bean.money/beanstalk.pdf#subsection.8.2)
* [Decentralized Price Oracle Documentation](peg-maintenance/overview.md#decentralized-price-oracle)
* [ETH/USD Chainlink Data Feed](https://data.chain.link/ethereum/mainnet/crypto-usd/eth-usd)

#### **19. BEANSTALK REQUIRES THAT THE GM FUNCTION IS CALLED AT THE TOP OF EACH HOUR ON ETHEREUM. FAILURE TO SUCCESSFULLY INCENTIVIZE THE CALLING OF THE GM FUNCTION COULD HAVE AN ADVERSE AFFECT ON BEANSTALK'S ABILITY TO OSCILLATE THE BEAN PRICE ABOVE AND BELOW ITS PEG.** <a href="#sunrise-incentivization-risk" id="sunrise-incentivization-risk"></a>

Beans and/or Soil are minted upon a successful call of the `gm` function. Beanstalk covers the cost of `gm` by awarding the sender of an accepted `gm` function call with newly minted Beans. The failure of Beanstalk to successfully incentivize the calling of `gm` would effectively result in the failure of Beanstalk to influence the size of the Bean supply, and thereby the Bean price.

More information:

* [Whitepaper, Section 4, Sun](https://bean.money/beanstalk.pdf#section.4)
* [Sun Documentation](farm/sun.md)

#### **20. THE BEANSTALK CONTRACTS ARE OPEN SOURCE. ANYONE CAN VIEW THE SOURCE CODE AND ATTEMPT TO FIND VULNERABILITIES.** <a href="#open-source-risk" id="open-source-risk"></a>

The Beanstalk contracts are open source and deployed on the Ethereum blockchain. There may be bugs, flaws, or other unintended consequences from using open source code to govern irreversible financial transactions on a decentralized network. These issues may lead to a loss of funds if present and discovered by malicious actors, and has in the past (see [#1](disclosures.md#governance-exploit)).

More information:

* [Beanstalk on GitHub](https://github.com/BeanstalkFarms/Beanstalk)

#### **21. BEANSTALK IS AUDITED BUT AUDITS CANNOT GUARANTEE SECURITY. IT IS ANTICIPATED THAT FUTURE CODE WILL NOT BE AUDITED BEFORE BEING COMMITTED BY THE DAO.** <a href="#audit-risk" id="audit-risk"></a>

Security is paramount to Beanstalk's success. Prior to Replant in August 2022, the majority of Beanstalk’s code was audited by Halborn and [Trail of Bits](https://www.trailofbits.com/). Up to May 2024, the majority of new Beanstalk code since Replant was audited by Halborn, Cyfrin and Codehawks. While all are reputable audit firms, there is no guarantee Beanstalk is secure. Beanstalk was audited by [Omniscia](https://omniscia.io/) prior to the April 2022 governance exploit.

In the future, it is anticipated that the DAO will vote to commit unaudited code. There is always additional risk associated with implementing unaudited code.

Halborn has performed a pentest of the Beanstalk UI hosted at [app.bean.money,](https://app.bean.money/) but there is no guarantee that interacting with Beanstalk through the Beanstalk UI is secure. Any issues could lead to a loss of funds.

The Beanstalk SDK is unaudited. There is no guarantee that interacting with Beanstalk through the Beanstalk SDK is secure. Any issues could lead to a loss of funds.

More information:

* [Beanstalk Audits](https://github.com/BeanstalkFarms/Beanstalk-Audits)
* [Beanstalk UI Halborn Report](https://bean.money/10-19-22-beanstalk-ui-halborn-report)
* [Beanstalk SDK on GitHub](https://github.com/BeanstalkFarms/Beanstalk/tree/master/projects/sdk)

#### **22. THE APP.BEAN.MONEY FRONTEND CAN BE CENSORED AS IT IS HOSTED ON A CLOUD PROVIDER.** <a href="#closed-source-ui-risk" id="closed-source-ui-risk"></a>

The Beanstalk UI hosted at [app.bean.money](https://app.bean.money/) is hosted on Netlify, a privately held, United States based cloud provider. Netlify could censor the frontend at will, or a technical disruption could prevent access. In either scenario, Beanstalk would not be accessible from a web browser until (1) Beanstalk Farms, the decentralized development organization that manages the site, could deploy the frontend elsewhere, or (2) other parties could use the open source code to deploy their own frontends to interact with the Beanstalk contracts.

There have been multiple instances of Netlify getting compromised, resulting in phishing attacks. There is no guarantee that the Beanstalk UI will not be subjected to similar attacks.

More information:

* [Beanstalk UI on GitHub](https://github.com/BeanstalkFarms/Beanstalk/tree/master/projects/ui)
* [Beanstalk Farms Documentation](governance/beanstalk-farms/)

#### **23. THE APP.BEAN.MONEY FRONTEND DEPENDS ON THE SUBGRAPHS FOR DISPLAYING VARIOUS ON-CHAIN DATA. THERE IS NO GUARANTEE THAT SUBGRAPH DATA IS ACCURATE OR AVAILABLE.** <a href="#subgraph-data" id="subgraph-data"></a>

The Beanstalk UI hosted at [app.bean.money](https://app.bean.money/) depends on the Beanstalk and Bean Subgraphs for displaying various data. The subgraphs are primarily maintained by Beanstalk Farms.

By default the Beanstalk UI uses a version of the subgraph hosted by Beanstalk Farms, which can be censored. The subgraph that the Beanstalk UI uses can be adjusted in the settings.

More information:

* [Beanstalk Subgraph on GitHub](https://github.com/BeanstalkFarms/Beanstalk/tree/master/projects/subgraph-beanstalk)
* [BFSM Dashboard](governance/beanstalk-farms/bfsm-dashboard.md)

#### **24. REGULATORY INTEREST IN STABLECOINS AND DECENTRALIZED FINANCE WILL RESULT IN NEW INDUSTRY REGULATIONS. THE IMPACT OF FUTURE REGULATIONS ON BEANSTALK IS UNCERTAIN.** <a href="#regulatory-risk" id="regulatory-risk"></a>

In alignment with the ethos of DeFi, Beanstalk has been designed to be permissionless and censorship resistant, without the requirement for any trust-providing intermediary.

It is unclear what regulations, if any, governments will attempt to impose on DeFi. Therefore, it is impossible to predict how any new government regulations of DeFi will affect Beanstalk, or any of the protocols or networks Beanstalk relies on as part of its ecosystem.

#### **25. BEANSTALK IS NOT A FINISHED PROTOCOL AND REQUIRES ONGOING DEVELOPMENT. THERE IS NO GUARANTEE OF FURTHER DEVELOPMENT.** <a href="#regulatory-risk" id="regulatory-risk"></a>

Beanstalk is likely not at a point where it can sustain itself in perpetuity without additional development of itself and the surrounding ecosystem. High quality improvements are essential but are not guaranteed.

Publius, the pseudonym for the three co-founders of Beanstalk, continues to be influential within the Beanstalk DAO. The identities of Publius are public. The identities of most of the remaining Beanstalk contributors are anonymous.
