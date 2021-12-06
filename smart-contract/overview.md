# Overview

![Architecture of Bluejay Protocol](<../.gitbook/assets/image (8).png>)

### Overview

The protocol consists of multiple key components. The roles of the various components are described below:

#### TreasuryBondDepository

The module is used to quote the user the price of the bond as well as to allow them to purchase and redeem the bonds. Proceeds from the sale will be transferred to the `Treasury` module.

Note: The design is similar to OlympusDAO's Bond Depository except that a user may purchase multiple bonds without resetting the vesting period.

#### BondGovernor

The module is used by the DAO to specify the different parameters around the different treasury bonds. These parameters will be used by the `TreasuryBondDepository` to price its bonds.

#### Staking

The module is used to allow users to stake and lock up their BLU tokens. The staked BLU (sBLU) token is redeemable 1-1 for the BLU token. The module automatically compounds the amount of staked tokens each second. The DAO may adjust the monetary policy by setting a different staking reward here.

#### Treasury

The module is used to hold all assets, reserve tokens & liquidity tokens, on behalf of the protocol. In addition, it's the only module that can mint BLU tokens. The module allows the `StablecoinEngine` module to withdraw assets for staking in the liquidity pools. It also allows the bond depositories and staking contract to mint more BLU tokens. All BLU tokens generated are backed by the value of the assets held in the treasury.

#### StablecoinEngine

The module is used to create the various stablecoins. When a stablecoin is created, it must be backed by the reserve asset. An equal value of stablecoin and reserve assets will be staked in the `LiquidityPool` and immediately made available for anyone to buy or sell. Only the DAO can instruct the module to add or remove liquidity to a certain stablecoin's liquidity pool, depending on the proportion of the treasury to allocate to each pool. Additionally, the engine allows the `Stabilizer` module to perform a swap on the `LiquidityPool` when the price of the stablecoin is off-pegged and the `StabilizingBondDepository` is incapable of bringing it back to peg under extreme conditions.

#### StabilizingBondDepository

The module is an automatic mechanism to allow the protocol to bring the different stablecoins' prices to peg with their external oracle prices. It offers either expansionary bonds or contractionary bonds, depending on the direction of price deviation, to bonder at a discount determined by the magnitude of the price deviation. When bonds are purchased, the module either buys the stablecoin to burn it to increase the price of the stablecoin on the pool or mints more stablecoin to swap for reserve assets to decrease the price of stablecoin on the pool.

#### Oracle

The module is an interface for getting the price of an asset relative to another. It is connected to external price oracles like Chainlink for stablecoin prices. The oracle is used by the `StabilizingBondDepository` to determine the discounted price of the stabilizing bonds and the `Stabilizer` to determine how much assets the `StablecoinEngine` needs to swap on the `LiquidityPool` to bring the prices to peg as well as the direction for swap.

#### LiquidityPool

The module is a Uniswap V2 Pair contract that allows users to swap reserve assets for stablecoins or vice versa. It will be deployed from Uniswap's factory contract and will allow the stablecoins to be available on the Uniswap exchange interface.

#### DAO

The DAO is a Gnosis multi-sig wallet that is operated by several trusted members of the team.
