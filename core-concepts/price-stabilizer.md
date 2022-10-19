# Price Stabilizer

The stabilizer is a module that allows the DAO to manually bring the stablecoins' price to their pegs. This is used in scenarios where there are insufficient bonders to bring the price to peg or the price is too far off due to a huge shock to the prices on either the external FX market or on the liquidity pools.

![Stabilizer performs swaps on the liquidity pool to bring price to peg](<../.gitbook/assets/Price Stabilizer.png>)

### Overview

The stabilizer has the capabilities to look up the target stablecoin price on the oracle and instruct the protocol to perform a swap on the liquidity pool to bring the price to peg.

In the case where the stablecoin is overpriced on the liquidity pool, more stablecoins will be minted to be swapped on the pool to bring prices down.

In the case where the stablecoin is underpriced on the liquidity pool, reserve assets will be swapped on the pool for the stablecoin to bring the price up. The swapped stablecoins will be burned.

### Bootstrap & Fallback Mechanism

The stabilizer will be used most aggressively during the early days of the launch when volatility is the highest and will be relaxed to allow the stabilizing bonds to take over in keeping the prices of the stablecoins to peg.

### Controls & Measure

The DAO Keeper is a whitelisted externally owned account (EOA). It does not require a multi-sig setup to allow it to quickly respond in cases where the issues need to be immediately rectified.&#x20;

The Stabilizer contract is created in a way that the DAO Keeper can only bring the price closer to the peg, cannot be used to manipulate the market in any other manner, and does not have access to other modules in the protocol.

In addition, the DAO Keeper will supply parameters to prevent excessive slippage when swaps are performed to protect against front-running transactions.
