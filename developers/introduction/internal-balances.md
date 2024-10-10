# Internal Balances

#### What are Internal Balances? <a href="#what-are-internal-balances" id="what-are-internal-balances"></a>

Beanstalk uses an Internal Balances system largely inspired by [Balancer's Vault](https://docs.balancer.fi/getting-started/faqs/the-vault#what-are-internal-user-balances). With Internal Balances, Beanstalk is able to store an any ERC-20 token on behalf of a user. Beanstalk stores that the user has that ERC-20 token in `AppStorage`. All functions within Beanstalk that either use a user's ERC-20 tokens or send ERC-20 tokens to a user can send/receive the ERC-20 tokens from the user's Internal Balance and/or External Balance (the user's wallet).

Internal Balances can significantly reduce transaction costs for using tokens that remain in Beanstalk. As more protocols utilize Internal Balances, the gas savings can compound.

{% hint style="warning" %}
In the Beanstalk ecosystem, **Internal Balances** are referred to as **Farm Balances**. Similarly, **External Balances** (balances in the user's wallet) are referred to as **Circulating Balances**. See Terminology Discrepancies.
{% endhint %}

#### Relevant Contracts <a href="#associated-contracts" id="associated-contracts"></a>

* [`LibTransfer.sol`](https://github.com/BeanstalkFarms/Beanstalk/blob/master/protocol/contracts/libraries/Token/LibTransfer.sol)
* [`LibBalance.sol`](https://github.com/BeanstalkFarms/Beanstalk/blob/master/protocol/contracts/libraries/Token/LibBalance.sol)

#### To / From

`LibTransfer` uses the following structs in order to denote the location(s) from which tokens will be used in a function.

```solidity
enum From {
    EXTERNAL,
    INTERNAL,
    EXTERNAL_INTERNAL,
    INTERNAL_TOLERANT
}
```

* `EXTERNAL`: Beanstalk will receive tokens from the user's External Balance;
* `INTERNAL`: Beanstalk will receive tokens from the user's Internal Balance;
* `EXTERNAL_INTERNAL`: Beanstalk will receive tokens from the user's Internal Balance and will receive from their External Balance if there is not enough in the Internal Balance; and
* `INTERNAL_TOLERANT`: Beanstalk will receive tokens from the user's Internal Balance and will not fail if there is not enough in their Internal Balance.

```solidity
enum To {
    EXTERNAL,
    INTERNAL
}
```

* `EXTERNAL` Beanstalk will send tokens to the user's External Balance; and
* `INTERNAL` Beanstalk will send tokens to the user's Internal Balance.

#### Transferring Internal / External Balances <a href="#transferring-internal-external-balances" id="transferring-internal-external-balances"></a>

At any time, a user can transfer, add or remove ERC-20 tokens from their Internal Balance through the `transferToken` function in the `TokenFacet`. `transferToken` is a general transfer method that allows full control of the tokens start/end location (i.e internal to internal, internal to external, external to internal, external to external).

```solidity
function transferToken(
    IERC20 token,
    address recipient,
    uint256 amount,
    LibTransfer.From fromMode,
    LibTransfer.To toMode
) external payable;
```

#### Sending Internal / External Balances <a href="#sending-internal-external-balances" id="sending-internal-external-balances"></a>

A function that sends ERC-20 tokens to users can implement Internal Balances by adding the `To` enum in `LibTransfer` to a function's signature.

Then call `sendToken` in `LibTransfer` instead of directly calling the ERC-20 function `transferFrom`.

```solidity
function sendToken(
    IERC20 token,
    uint256 amount,
    address recipient,
    To mode
) internal;
```

#### Receiving Internal / External Balances <a href="#receiving-internal-external-balances" id="receiving-internal-external-balances"></a>

A function that receives ERC-20 tokens from users can implement Internal Balances by adding the `From` enum in `LibTransfer` to a function's signature.

Then call `receiveToken` in `LibTransfer` instead of directly calling the ERC-20 function `transfer`.

```solidity
function receiveToken(
    IERC20 token,
    uint256 amount,
    address recipient,
    To mode
) internal;
```

For protocols that are building on top of Beanstalk and want to interact with Internal Balances, they can utilize the functions given in `TokenFacet`, rather than the library itself.
