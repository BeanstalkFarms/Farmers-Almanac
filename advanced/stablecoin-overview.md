# Stablecoin Overview

### What is a Stablecoin?

A stablecoin is a fungible asset intended to maintain low price volatility relative to an arbitrary value peg. Oftentimes, stablecoins are pegged to the price of an off-chain currency.

A currency’s utility is a function of:

* Trustlessness;
* Carrying costs;
* Low volatility; and
* Liquidity.

Low volatility is essential to the utility of a currency. Without looking at the theoretical reasons for why this is the case, the market has clearly demonstrated its value. Since its inception with the creation of Tether – a historically very [low volatility asset](https://coinmarketcap.com/currencies/tether/) – in 2014, the stablecoin industry has grown from a fringe backwater to a [$150B market cap](https://www.statista.com/statistics/1255835/stablecoin-market-capitalization/) decentralized finance (“DeFi”) behemoth.

The history of money tells a story of markets seeking out the least volatile assets to use as currency. The relatively brief history of DeFi tells the same story.

### What is the Problem with Current Implementations of Stablecoins?

While the market has demonstrated clear demand for low volatility blockchain-native assets, the vast majority of current implementations suffer from a variety of risks and drawbacks, primarily with regard to a lack of trustlessness, negative carrying costs and thin liquidity. In other words, the only utility that has been created by current stablecoin implementations is low volatility. The absence of a decentralized currency with competitive carrying costs and deep liquidity is the main issue – in addition to high blockchain transaction costs – holding businesses producing real economic activity back from adopting decentralized financial primitives.

Businesses built exclusively on decentralized primitives have struggled to compete with businesses built on centralized financial systems like fiat USD because DeFi lacks a trustless and liquid currency with sufficiently low price volatility and competitive carrying costs.

For example, historically, [borrowing rates on USD stablecoins](https://app.aave.com/markets/) have significantly exceeded [borrowing rates on fiat USD](https://www.newyorkfed.org/markets/reference-rates/effr). Until network-native borrowing rates are comparable to or lower than off-chain borrowing rates, DeFi will continue to struggle to attract meaningful economic activity away from TradFi.

### Stablecoin Features

Current implementations of stablecoins can be conceptualized along the following three axes: value source, convertibility and network nativity.

#### 1. Value Source: Exogenous value vs. Endogenous value <a href="#value-source" id="value-source"></a>

Stablecoin value can come from exogenous assets or endogenous value creation.

A stablecoin with _exogenous value_ is one whose value is derived from another asset or basket of assets which are held by the issuer as collateral. Reliance on exogenous value generates opportunity costs associated with collateral requirements, which creates non-competitive carrying costs.

A stablecoin with _endogenous value_ is one whose value is derived from demand for the currency. Endogenous value has the potential to facilitate the creation of trustless currency with low price volatility, competitive carrying costs and deep liquidity.

#### 2. Convertibility: Convertible vs. Non-convertible <a href="#convertibility" id="convertibility"></a>

Convertibility is the option to exchange an asset for its underlying collateral.

A _convertible_ stablecoin protocol is one that facilitates convertibility between its stablecoin and its underlying collateral. Arbitrage opportunities created by convertibility ensure that the stablecoin price is rarely above or below the value of the underlying collateral, once frictions around convertibility are accounted for. Convertibility comes at the expense of low liquidity and non-competitive carrying costs because of the opportunity cost associated with locking up collateral to facilitate it.

A _non-convertible_ stablecoin protocol is one that does not facilitate convertibility between its stablecoin and any form of underlying collateral. It is impossible to keep a stablecoin price equal to its value peg at all times without low-friction convertibility. Non-convertible stablecoin protocols without collateral requirements have the potential to create endogenous value that facilitates trustlessness, competitive carrying costs and deep liquidity at the expense of volatility.

#### 3. Network Nativity: Network-native vs. Non-network native <a href="#network-nativity" id="network-nativity"></a>

Network nativity refers to the source of a stablecoin’s value with regard to its network.

A _network-native_ stablecoin is one that derives its value exclusively from the network to which it is native. Network-nativity eliminates most points of centralization from a stablecoin’s value chain.

A _non-network-native_ stablecoin is one that does not exclusively derive its value from the network to which it is native. Non-network-nativity requires a custodian that facilitates a bridge to the network, which can introduce significant costs, complexities and points of centralization.
