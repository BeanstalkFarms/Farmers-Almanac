# Depot

The Depot facilitates complex, gas-efficient transactions within Beanstalk and across the Ethereum network.&#x20;

### Pipelines

Any protocol with a Pipeline to the Depot can be used via Beanstalk. Pipelines can be added to the Depot via Beanstalk governance.

#### Curve Pipeline

The Curve Pipeline allows anyone to call functions in any pool registered in any of the following Curve registries.

* [0xB9fC157394Af804a3578134A6585C0dc9cc990d4](https://etherscan.io/address/0xB9fC157394Af804a3578134A6585C0dc9cc990d4#readContract)
* [0x90E00ACe148ca3b23Ac1bC8C240C2a7Dd9c2d7f5](https://etherscan.io/address/0x90E00ACe148ca3b23Ac1bC8C240C2a7Dd9c2d7f5#readContract)
* [0x8F942C20D02bEfc377D41445793068908E2250D0](https://etherscan.io/address/0x8F942C20D02bEfc377D41445793068908E2250D0#readContract)

The following functions to interact with Curve pools can be called through the Curve Pipeline:

```solidity
function exchange(
    address pool, 
    address registry, 
    address fromToken, 
    address toToken, 
    uint256 amountIn, 
    uint256 minAmountOut, 
    LibTransfer.From fromMode, 
    LibTransfer.To toMode
) external payable nonReentrant;

// only in Metapools
function exchangeUnderlying(
    address pool, 
    address fromToken, 
    address toToken, 
    uint256 amountIn, 
    uint256 minAmountOut, 
    LibTransfer.From fromMode, 
    LibTransfer.To toMode
) external payable nonReentrant;

function addLiquidity(
    address pool,
    address registry,
    uint256[] memory amounts,
    uint256 minAmountOut,
    LibTransfer.From fromMode,
    LibTransfer.To toMode
) external payable nonReentrant;

function removeLiquidity(
    address pool,
    address registry,
    uint256 amountIn,
    uint256[] calldata minAmountsOut,
    LibTransfer.From fromMode,
    LibTransfer.To toMode
) external payable nonReentrant;

function removeLiquidityImbalance(
    address pool,
    address registry,
    uint256[] calldata amountsOut,
    uint256 maxAmountIn,
    LibTransfer.From fromMode,
    LibTransfer.To toMode
) external payable nonReentrant;

function removeLiquidityOneToken(
    address pool,
    address registry,
    address toToken,
    uint256 amountIn,
    uint256 minAmountOut,
    LibTransfer.From fromMode,
    LibTransfer.To toMode
) external payable nonReentrant;

```
