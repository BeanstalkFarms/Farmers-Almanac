# Disclosures

**Before interacting with Beanstalk, consider reading the following Disclosures** [**prepared by the DAO**](https://app.bean.money/#/governance/0x0d9e422bafaee7f87744c09afe9c2c68af590fc76d8afd13b12b9dfc9328e794)**. This document can be found on Arweave** [**here**](https://arweave.net/g1fij0syFvuxNR83I2VKOe1auNxtjEUwevkihxoRUXg)**.**&#x20;

Interacting with Beanstalk involves many risks. Before interacting with Beanstalk, you should review the relevant documentation to make sure you understand how Beanstalk works, as well as information about the current state of Beanstalk. Beanstalk Farms has created this set of disclosures to assist in the educational process. These disclosures are not exhaustive. The [Beanstalk whitepaper](https://bean.money/docs/beanstalk.pdf), Farmers’ Almanac, [Dune dashboard](community-resources/links.md#analytics), and other Beanstalk resources, as well as participating in the Beanstalk community, can help to understand the protocol. Before participating in the protocol, everyone should do their own research, investigation and analysis.

Transparency is the cornerstone of DeFi. The Beanstalk decentralized autonomous organization (DAO) endeavors to be as transparent as possible, particularly as it pertains to communicating the risks of interacting with Beanstalk.

#### **1. BEANSTALK WAS ATTACKED ON APRIL 17, 2022 VIA ON-CHAIN GOVERNANCE. ALL \~$77M IN NON-BEAN ASSETS WERE STOLEN. PROTOCOL GOVERNANCE HAS BEEN CHANGED TO A 5-OF-9 COMMUNITY MULTISIG.** <a href="#1-governance-exploit" id="1-governance-exploit"></a>

On April 17, 2022, Beanstalk was attacked via on-chain governance resulting in a theft of all \~$77M in non-Beanstalk user assets. The attacker used a flash loan to compromise the governance mechanism and steal the assets deposited in the DAO.

Shortly after the attack, Beanstalk was Paused and on-chain governance was removed. Since the attack, governance votes have taken place on Snapshot. Beanstalk is now owned by a community-run multisig wallet (the Beanstalk Community Multisig, or BCM) responsible for executing the will of the DAO as indicated via Snapshot vote. The keys to the BCM are custodied by an anonymous group of nine Beanstalk community members and contributors. This serves as a temporary security measure until a secure and fully-decentralized governance mechanism has been developed and sufficiently audited. All contract changes under the BCM structure require the signature of 5-of-9 BCM members.

The [old Bean token](https://etherscan.io/token/0xdc59ac4fefa32293a95889dc396682858d52e5db) was replaced with a [new one](https://etherscan.io/address/0xBEA0000029AD1c77D3d5D23Ba2D8893dB9d1Efab). The obsolete token has no value according to Beanstalk.

More information:

* [Past BIPs](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/tree/master/bip)
* [Beanstalk Governance Exploit](https://bean.money/blog/beanstalk-governance-exploit)
* [BCM Process](governance/beanstalk/bcm-process.md)

#### **2. THERE IS NO MAXIMUM BEAN SUPPLY. THE BEAN SUPPLY CAN GROW INFINITELY THROUGH DEMAND-BASED MINTING AND GOVERNANCE.** <a href="#2-infinite-supply" id="2-infinite-supply"></a>

Beanstalk increases the Bean supply every Season where the liquidity and time weighted average price of 1 Bean is greater than $1 over the previous Season. Enough Beans are minted such that if all the newly minted Beans were sold, the Bean price would return to $1. Those Beans are distributed to Stalkholders, Pod holders and Active Fertilizer holders.

The Bean supply is uncapped and grows as demand for Beans increases. Beans can also be minted arbitrarily through governance (see [#7](disclosures.md#arbitrary-changes-through-governance)).

More information:

* [Pre-exploit Dune Analytics](https://dune.com/tbiq/Beanstalk)
* [Whitepaper, Section 8.10, Bean Supply](https://bean.money/docs/beanstalk.pdf)
* [Bean Supply Documentation](peg-maintenance/overview.md#bean-supply)

#### **3. BEANSTALK DID NOT HAVE A PRE-MINE, PRE-SALE, OR TEAM ALLOCATION. ALL BEANS HAVE BEEN MINTED IN ACCORDANCE WITH EITHER THE MINTING SCHEDULE OR GOVERNANCE.** <a href="#3-no-pre-mine" id="3-no-pre-mine"></a>

Beanstalk did not have a pre-mine, pre-sale or team allocation of any kind. The first 100 Beans were minted when the init() function was called to deploy Beanstalk.

Beanstalk launched without the need to raise capital. However, after an on-chain governance attack on April 17, 2022 (see [#1](disclosures.md#governance-exploit)), a fundraiser known as the Barn Raise is being used to recapitalize the non-Bean funds stolen in the exploit. The terms offered in the fundraiser are available to any Ethereum address.

More information:

* [BFP-72: The Path Forward, No Haircuts](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/blob/master/bfp/bfp-72-no-haircuts.md)
* [Whitepaper, Section 7, Barn](https://bean.money/docs/beanstalk.pdf)
* [Barn Raise Documentation](farm/barn.md)

#### **4. BEANSTALK RELIES ON THIRD PARTIES TO PROVIDE CREDIT TO RETURN THE BEAN PRICE TO ITS PEG. THERE IS NO LENDER OF LAST RESORT.** <a href="#4-credit-risk" id="4-credit-risk"></a>

Beanstalk uses a credit based model, allowing anyone to lend Beans to the protocol to participate in peg maintenance. Beanstalk burns any Beans it borrows. As a consequence, the ability of the protocol to return the price of a Bean to the peg relies on the availability of willing creditors, which is not guaranteed. The economic design of Beanstalk fails if it can no longer attract creditors.

More information:

* [Whitepaper, Section 6, Field](https://bean.money/docs/beanstalk.pdf)
* [Field Documentation](farm/field.md)

#### **5. BEANSTALK DOES NOT GUARANTEE THE BEAN PRICE. INSTEAD BEANSTALK INCENTIVIZES THE REGULAR OSCILLATION OF THE BEAN PRICE ABOVE AND BELOW ITS PEG THROUGH PROTOCOL-NATIVE INCENTIVES.** <a href="#5-oscillations" id="5-oscillations"></a>

Bean is not a collateralized stablecoin and Beanstalk offers no guarantee of the value of Bean. Beanstalk was deployed on August 6, 2021. Since then, the Bean price has crossed its dollar peg over 4,000 times. Even so, Beanstalk is still in an early stage and various parts of its economic design continue to be improved through governance.

Beanstalk tries to incentivize the regular oscillation of the Bean price above and below its peg. While the protocol’s incentives are designed to return the price of a Bean to its peg, the timing of oscillations is indeterminate. The price will almost never be exactly equal to its peg. Crossing the peg in the past is no guarantee of it happening again in the future.

More information:

* [Whitepaper, Section 8.1, Ideal Equilibrium](https://bean.money/docs/beanstalk.pdf)
* [Peg Maintenance Documentation](peg-maintenance/overview.md)

#### **6. BEANSTALK-NATIVE DEBT DOES NOT HAVE A MATURITY DATE AND THEREFORE MAY NEVER BECOME REDEEMABLE FOR BEANS.** <a href="#6-debt-maturity-risk" id="6-debt-maturity-risk"></a>

Beanstalk borrows Beans from lenders in exchange for Pods and Sprouts. Bean loans have fixed interest rates but do not have fixed maturity dates.

Pods and Sprouts are repaid when the liquidity and time weighted average price of 1 Bean is greater than $1 over the previous Season, but there is no guarantee this will continue until all Pods and Sprouts become redeemable (see [#4](disclosures.md#no-lender-of-last-resort)). Governance may also arbitrarily modify the redeemability of Beanstalk debt (see [#7](disclosures.md#arbitrary-changes-through-governance)).

More information:

* [Whitepaper, Section 11.2, Strong Credit](https://bean.money/docs/beanstalk.pdf)

#### **7. STALKHOLDERS CAN MAKE ARBITRARY CHANGES TO BEANSTALK THROUGH GOVERNANCE, IF ENACTED BY THE BEANSTALK COMMUNITY MULTISIG. THERE IS NO GUARANTEE THE CHANGES WILL BE BENEFICIAL TO BEANSTALK.** <a href="#7-governance-risk" id="7-governance-risk"></a>

Beanstalk is governed by the Beanstalk DAO—the Silo, which is comprised of Stalkholders. Stalkholders vote on Beanstalk Improvement Proposals (BIPs), which can arbitrarily change Beanstalk. Voting rights come from Stalk ownership (see [#8](disclosures.md#earlier-depositor-governance-power) for details on Stalk).

Any community member that meets a certain Stalk ownership threshold may propose a BIP. If the BIP passes, the Beanstalk Community Multisig (see [#9](disclosures.md#beanstalk-community-multisig) for details on the BCM) shall follow the results of the Snapshot, unless the Stalk distribution is compromised in a flash loan or other governance attack. Through this governance process, Stalkholders may make arbitrary changes to Beanstalk.

More information:

* [Beanstalk DAO Snapshot](https://snapshot.org/#/beanstalkdao.eth/)
* [Past BIPs](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/tree/master/bip)****

#### **8. ANYONE CAN RECEIVE STALK BY DEPOSITING WHITELISTED ASSETS IN THE SILO. EARLIER DEPOSITORS IN THE SILO HAVE PROPORTIONALLY GREATER GOVERNANCE POWER RELATIVE TO THE BEAN DENOMINATED VALUE ORIGINALLY DEPOSITED.** <a href="#8-earlier-depositor-governance-power" id="8-earlier-depositor-governance-power"></a>

Depositors earn Stalk and Seeds. Seeds yield 1/10000 new Stalk every Season. Stalkholders participate in governance and earn Bean seigniorage. Stalk ownership, and thus governance power, decentralizes over time.

As earlier Depositors in the Silo have been accruing Stalk from Seeds for more Seasons compared to later Depositors, these Depositors have greater governance power in proportion to the Bean Denominated Value (BDV) of their original Deposits.

More information:

* [Whitepaper, Section 5.1, The Stalk System](https://bean.money/docs/beanstalk.pdf)
* [Stalk System Documentation](farm/silo.md#the-stalk-system)

#### **9. THE BEANSTALK CONTRACT IS OWNED BY THE BEANSTALK COMMUNITY MULTISIG. THE MULTISIG CAN MAKE ARBITRARY CHANGES TO BEANSTALK WITH 5-OF-9 SIGNATURES FROM THE ANONYMOUS SIGNERS. THERE IS NO GUARANTEE THE MULTISIG ENACTS THE GOVERNANCE DECISIONS OF THE DAO.** <a href="#9-multisig-risk" id="9-multisig-risk"></a>

Ownership of the Beanstalk contracts is held by a 5-of-9 multisig known as the Beanstalk Community Multisig (BCM). The BCM is an extension of the Beanstalk DAO. The BCM’s role is to enact on-chain the decisions Stalkholders make via off-chain voting on Snapshot. Besides Publius (one of the members), all members of the BCM are anonymous. Publius selected the other members, who Publius believes will act in the best interest of Beanstalk. This process was approved via governance.

Off-chain governance introduces significant risks related to security and censorship. The BCM is designed to mitigate as many of those risks as possible by distributing the multisig keys across reputable community members and Beanstalk core contributors, and collectively implementing and adhering to a set of best practices. There is no guarantee the BCM enacts the governance decisions the DAO voted on via Snapshot.

More information:

* [BFP-73: Beanstalk Community Multisig](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/blob/master/bfp/bfp-73-multisig.md)
* [Multisig Powers Documentation](governance/beanstalk/bcm-process.md#multisig-powers)
* [Anonymous Multisig Signers Documentation](governance/beanstalk/bcm-process.md#anonymous-multisig-signers)
* [BCM Dashboard](governance/beanstalk/bcm-dashboard.md)

#### **10. AS GOVERNANCE POWER IS DETERMINED THROUGH STALK OWNERSHIP, SUFFICIENT CAPITAL COULD PURCHASE SIGNIFICANT GOVERNANCE POWER AND TAKE OVER BEANSTALK.** <a href="#10-stalk-governance-power" id="10-stalk-governance-power"></a>

Beanstalk is governed by Stalkholders, as described in [#7](disclosures.md#arbitrary-changes-through-governance). Stalk ownership, and thus governance power, decentralizes over time given the inflationary nature of Stalk. However, there is no maximum Stalk supply. Stalk is minted for Deposits based on the Bean Denominated Value (BDV) of the Deposit, up to any arbitrary BDV.

Stalk ownership was previously compromised via flash loan, which enabled the on-chain governance attack on April 17, 2022 (see [#1](disclosures.md#governance-exploit)). The Beanstalk Community Multisig serves as a temporary security measure until a secure and fully-decentralized governance mechanism has been developed and sufficiently audited.

More information:

* [Whitepaper, Section 5.1, The Stalk System](https://bean.money/docs/beanstalk.pdf)
* [BCM Process](governance/beanstalk/bcm-process.md)

#### **11. A VULNERABILITY IN ETHEREUM COULD RESULT IN A LOSS OF FUNDS. BEANSTALK ASSUMES THE SECURITY OF ETHEREUM.** <a href="#11-ethereum-risk" id="11-ethereum-risk"></a>

Ethereum is the largest smart contract blockchain by market capitalization, total value deposited, and dollar denominated transaction value. In general, open source networks with large amounts of value on them and long track records indicate security, but there is no guarantee. Beanstalk assumes the security of the Ethereum network.

#### **12. A VULNERABILITY IN CURVE COULD RESULT IN A LOSS OF FUNDS. BEANSTALK ASSUMES THE SECURITY OF CURVE AMMs.** <a href="#12-curve-risk" id="12-curve-risk"></a>

Bean’s sole liquidity pool (at Replant) is a BEAN:3CRV pool on the Curve AMM. Curve is among the largest Ethereum-native decentralized exchange protocols by volume. In general, open source protocols with large amounts of value on them and long track records indicate security, but there is no guarantee. Beanstalk assumes the security of Curve.

More information:

* [BFP-76: Choose Replant Liquidity Pool](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/blob/master/bfp/bfp-76-replant-pool.md)

#### **13. THE BEAN PRICE IS DERIVED FROM THE VALUE OF ASSETS IT TRADES AGAINST IN DECENTRALIZED AMMS. THERE IS NO GUARANTEE ANY OF THESE ASSETS RETAIN VALUE.** <a href="#13-non-bean-liquidity-risk" id="13-non-bean-liquidity-risk"></a>

The value of Beans is derived from the non-Bean assets trading against it in decentralized liquidity pools. Each of these assets have their own set of associated risks, unique to the asset. Beanstalk implicitly assumes risk associated with these assets.

#### **14. BECAUSE BEANS DERIVE THEIR VALUE FROM THE ASSETS THEY TRADE AGAINST, AND NOT COLLATERAL, IT IS NOT POSSIBLE FOR ALL BEAN HOLDERS TO EXIT AT A DOLLAR OF VALUE FOR EVERY BEAN.** <a href="#14-not-all-bean-holders-can-exit-at-a-dollar-of-value" id="14-not-all-bean-holders-can-exit-at-a-dollar-of-value"></a>

Beans are not redeemable for any other asset; they can only be traded for another asset that Beans are trading against. As Bean holders sell their Beans, there is less and less value trading against Beans. Thus, unlike collateralized stablecoins, it is not possible for the Bean supply to scale down to zero with every Bean holder getting a dollar of value for every Bean sold.

#### **15. BEANSTALK REQUIRES TRUSTLESS AND RELIABLE ACCESS TO A MANIPULATION-RESISTANT PRICE ORACLE FOR A DOLLAR. BEANSTALK USES THE ON-CHAIN PRICES OF OTHER STABLECOINS TO DETERMINE THE PRICE OF A DOLLAR. THERE IS RISK ASSOCIATED WITH EACH OF THESE STABLECOINS THAT CAN COMPROMISE THEIR INTEGRITY AS ACCURATE PRICE ORACLES.** <a href="#15-oracle-risk" id="15-oracle-risk"></a>

Beanstalk’s core objective is to oscillate the price of a Bean above and below its dollar peg. To do this, Beanstalk must be able to reliably measure the price of a dollar on-chain without trusting a centralized third-party to provide it. A robust, decentralized stablecoin requires a tamper-proof, manipulation resistant and decentralized price oracle.

At Replant, Beans are traded in the BEAN:3CRV pool on Curve. 3CRV consists of USDC, USDT and DAI. Beanstalk assumes the average value of each USDC, USDT and DAI in the pool is equal to $1. A disruption in the reliability or accuracy of 3CRV as an accurate measure of $1 could impact Bean minting, resulting in adverse consequences for Beanstalk.

More information:

* [Whitepaper, Section 8.2, Decentralized Price Oracle](https://bean.money/docs/beanstalk.pdf)
* [Decentralized Price Oracle Documentation](peg-maintenance/overview.md#decentralized-price-oracle)

#### **16. BEANSTALK REQUIRES THAT THE SUNRISE FUNCTION IS CALLED AT THE TOP OF EACH HOUR ON ETHEREUM. FAILURE TO SUCCESSFULLY INCENTIVIZE THE CALLING OF THE SUNRISE FUNCTION COULD HAVE AN ADVERSE AFFECT ON BEANSTALK’S ABILITY TO OSCILLATE THE BEAN PRICE ABOVE AND BELOW ITS PEG.** <a href="#16-sunrise-incentivization-risk" id="16-sunrise-incentivization-risk"></a>

Beans and/or Soil are minted upon a successful call of the sunrise() function. Beanstalk covers the cost of sunrise() by awarding the sender of an accepted sunrise() function call with newly minted Beans. The failure of Beanstalk to successfully incentivize the calling of sunrise() would effectively result in the failure of Beanstalk to influence the size of the Bean supply, and thereby the Bean price.

More information:

* [Whitepaper, Section 4, Sun](https://bean.money/docs/beanstalk.pdf)
* [Sun Documentation](farm/sun.md)

#### **17. THE BEANSTALK CONTRACTS ARE OPEN SOURCE. ANYONE CAN VIEW THE SOURCE CODE AND ATTEMPT TO FIND VULNERABILITIES.** <a href="#17-open-source-risk" id="17-open-source-risk"></a>

The Beanstalk contracts are open source and deployed on the Ethereum blockchain. There may be bugs, flaws, or other unintended consequences from using open source code to govern irreversible financial transactions on a decentralized network. These issues may lead to a loss of funds if present and discovered by malicious actors, and has in the past (see [#1](disclosures.md#governance-exploit)).

More information:

* [Beanstalk on GitHub](https://github.com/BeanstalkFarms/Beanstalk)

#### **18. BEANSTALK IS AUDITED BUT AUDITS CANNOT GUARANTEE SECURITY. IT IS ANTICIPATED THAT FUTURE CODE WILL NOT BE AUDITED BEFORE IMPLEMENTED.** <a href="#18-audit-risk" id="18-audit-risk"></a>

Security is paramount to Beanstalk's success. Prior to Replant, the majority of Beanstalk’s code was audited by Halborn and Trail of Bits. While both are reputable audit firms, there is no guarantee Beanstalk is secure. Beanstalk was audited by Omniscia prior to the attack.

In the future, it is anticipated that the DAO will vote to implement unaudited code. There is always additional risk associated with implementing unaudited code.

The Beanstalk UI hosted at [app.bean.money](https://app.bean.money/) is unaudited. There is no guarantee that interacting with Beanstalk through [app.bean.money](https://app.bean.money/) is secure. Any issues could lead to a loss of funds.

More information:

* [Beanstalk Audit Reports](protocol-resources/audits.md)
* [BIP-21, Post Audit Changes Section](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/blob/master/bip/bip-21-replant.md#post-audit-changes)

#### **19. THE APP.BEAN.MONEY FRONTEND CAN BE CENSORED AS IT IS CLOSED SOURCE AND HOSTED ON A CLOUD PROVIDER.** <a href="#19-closed-source-ui-risk" id="19-closed-source-ui-risk"></a>

The [app.bean.money](https://app.bean.money/) frontend is closed source and is hosted on Netlify, a privately held, United States based cloud provider. Netlify could censor the frontend at will, or a technical disruption could prevent access. In either scenario, Beanstalk would not be accessible from a web browser until 1) Beanstalk Farms, the decentralized development organization that manages the site, could deploy the frontend elsewhere or open source the code, or 2) other parties could develop and deploy their own frontends to interact with the Beanstalk contracts.

There have been multiple instances of Netlify getting compromised, resulting in phishing attacks. There is no guarantee that [app.bean.money](https://app.bean.money/) will not be subjected to similar attacks.

#### **20. REGULATORY INTEREST IN STABLECOINS AND DECENTRALIZED FINANCE WILL RESULT IN NEW INDUSTRY REGULATIONS. THE IMPACT OF FUTURE REGULATIONS ON BEANSTALK IS UNCERTAIN.** <a href="#20-regulatory-risk" id="20-regulatory-risk"></a>

In alignment with the ethos of DeFi, Beanstalk has been designed to be permissionless and censorship resistant, without the requirement for any trust-providing intermediary.

It is unclear what regulations, if any, governments will attempt to impose on DeFi. Therefore, it is impossible to predict how any new government regulations of DeFi will affect Beanstalk, or any of the protocols or networks Beanstalk relies on as part of its ecosystem.

#### **21. BEANSTALK IS PRIMARILY DEVELOPED BY PAID AND UNPAID CONTRIBUTORS AT BEANSTALK FARMS AND BEAN SPROUT.** <a href="#21-contributor-risk" id="21-contributor-risk"></a>

Beanstalk is not a finished protocol and requires ongoing technical, ecosystem and community development. The Beanstalk DAO is responsible for the formation and governance of two independent, symbiotic organizations with distinct mandates: Beanstalk Farms (BF) and Bean Sprout (BS). Beanstalk Farms focuses on protocol and community development and Bean Sprout is a Beanstalk accelerator program. Budgets for BF and BS have been minted via governance and have been approved quarterly by the Beanstalk DAO.

Publius, the pseudonym for the three co-founders of Beanstalk, continues to be influential within BF, BS, and the Beanstalk DAO. The identities of Publius are public. The identities of most of the remaining contributors of BF and BS are anonymous.

More information:

* [Beanstalk Farms Documentation](governance/beanstalk-farms/)
* [Bean Sprout Documentation](governance/bean-sprout/)
