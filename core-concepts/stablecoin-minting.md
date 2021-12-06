# Stablecoin Minting

Each stablecoin created by the protocol is backed by liquidity directly. This allows the protocol to be highly capital-efficient compared to models using overcollateralization only.

![The DAO manages the issuance of stablecoins](<../.gitbook/assets/image (5).png>)

### Overview

The DAO will determine which stablecoins will be provided and maintained by the protocol as well as how much liquidity to allocate to the different stablecoins by adding or removing liquidity across different pools.

During the minting process, an equal value of reserve assets and minted stablecoins will be added to the liquidity pool directly. For example, if the oracle price for SGD is 0.73 against DAI, the engine can add 100,000 SGD-T and 73,000 DAI into the liquidity pool. This immediately allows users of the stablecoin to buy and sell the stablecoin on the pool at higher volume and with lower slippage.

As the oracle price may fluctuate due to conditions on the foreign exchange (FX) market, or the price on the liquidity pool may change due to demand and supply change in the DeFi space, there are additional mechanisms to bring the price to peg.

The first mechanism is a stabilizer module, operated by the DAO, to swap assets on the pool to bring the price to peg.

The second mechanism is the stabilizing bonds. The bonds allow bonders to bring the price to peg when they purchase them.

Both mechanisms are discussed in later sections.
