# Oracle

The oracle plays a role to provide a standardized price feed for the protocol.

### Overview

The protocol needs to know the correct exchange rate for the stablecoins to the reserve assets to correctly quote the target stablecoin price on the different liquidity pools.

To do that, we make use of oracle providers such as [Chainlink](https://chain.link/) or [Band Protocol](https://bandprotocol.com/) to provide a reliable price feed to the protocol. Since the quotes are usually for the currency pairs (ie SGD/USD), it needs to be further adjusted for the difference between the reserve asset value and the USD currency (ie DAI/USD).

The oracle also provides a safe way for the protocol to access and store the [Time-Weighted Average Price (TWAP)](https://docs.uniswap.org/contracts/v2/concepts/core-concepts/oracles) of the liquidity pool to protect the transaction from any flash loan or market manipulation attacks.

### Dependent Modules

The oracle will be used by the Price Stabilizer module as well as the Stabilizing Bond Depository module.
