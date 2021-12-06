# Bonding

Bonding is a process to allow Bluejay to acquire its own liquidity and reserve assets (ie DAI) and bring stablecoins to the peg by selling BLU at a discount. There are two main types of bonds on Bluejay, treasury bonds, and stabilizing bonds. For both types of bonds, the user exchanges either a reserve asset (ie DAI) or a liquidity token (ie BLU/DAI LP) in exchange for a BLU bond.

### BLU bond

When bonders purchase a bond from the protocol, they will be quoted the term of the bond such as the discounted BLU price, the vesting period, and the amount of BLU claimable when the bond matures. The bond will vest linearly over the vesting period, allowing the bonder to claim any vested BLU as it matures, and the full amount when the entire period is up.

### Treasury Bonds

The objective of these bonds is to allow the protocol to acquire its own liquidity which in turn will be used productively for minting and backing stablecoins. This creates a predictable supply of liquidity for Bluejay stablecoins' users and in turn generates revenue for the protocol through the collection of swap fees.

To do so, the protocol quotes bonds for reserve assets like `DAI` or liquidity tokens like `SGD-T/DAI LP`, in exchange for discounted BLU vested over a period of time. These assets will be transferred to the treasury directly to be used as operating capital for the stablecoins.

### Stabilizing Bonds

![Dynamic pricing of stabilizing bonds](<../.gitbook/assets/image (7) (1).png>)

The objective of stabilizing bonds is to bring the various stablecoins' prices to their peg. There will be two types of stabilizing bonds, expansionary and contractionary bonds, and are offered during different market conditions automatically. The bonds allow the protocol to acquire reserve assets (like DAI) to either mint and sell more stablecoins or to buy back stablecoins from the market. The type of bond offered depends on the direction of the price deviation and the discount offered depends on the magnitude of price deviation. The protocol also defines a small tolerance level where neither bonds are sold because the price deviation of the stablecoin is inconsequential.

**Expansionary bonds** are offered when the price of the stablecoin in the liquidity pool is higher than that on the oracle. This usually indicates an expansion in the usage of the particular stablecoin outside the protocol, which increases the price of the stablecoin on the liquidity pool when they are overbought. In such cases, the assets obtained from the bond sale will be used to mint more stablecoin to be sold on the liquidity pool, effectively lowering the price of the stablecoins.

![Expansionary bond sales decrease the price of stablecoins on liquidity pool](<../.gitbook/assets/image (1).png>)

In the example above, you can see that SGD-T is more expensive than the oracle price which is 0.73. In this case, the protocol quotes a bond for DAI to back and mint 1000 SGD-T to be swapped on the pool for 752 DAI. This has the effect of bringing the spot price closer to the oracle price, from 0.76 to 0.745.

**Contractionary** bonds are offered when the price of the stablecoin in the liquidity pool is lower than that on the oracle. This usually indicates a contraction in the usage of the particular stablecoin outside the protocol, which decreases the price of the stablecoin on the liquidity pool when they are oversold. In such cases, the assets obtained from the bond sale will be used to swap for the stablecoins to be burnt, effectively increasing the price of the stablecoins.

![Contractionary bond sales increase the price of stablecoins on liquidity pool](<../.gitbook/assets/image (4).png>)

In the example above, you can see that SGD-T is less expensive than the oracle price which is 0.73. In this case, the protocol quotes a bond for 1000 DAI to be swapped on the pool for 1408 SGD-T. This has the effect of bringing the spot price closer to the oracle price, from 0.7 to 0.72.

### Choosing your bonds

The different bonds will be quoted on the protocol website along with the APY. As a protocol user, you will only need to pick the bond which presents the highest APY for you. Whether the bond is a treasury bond or a stabilizing bond does not affect the way you interact with it, you simply swap your reserve assets (or LP token) for discounted BLU.
