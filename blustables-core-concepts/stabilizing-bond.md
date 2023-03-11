# Stabilizing Bond

### Overview

Stabilizing bonds are bonds that help to correct the liquidity pool's price to bring them to peg. It's a mechanism for the protocol to incentivize bonders to help correct the stablecoin prices automatically. Two forms of stabilizing bonds are available for each liquidity pool, expansionary bonds, and contractionary bonds, and are offered during different market conditions automatically

The bonds allow the protocol to acquire reserve assets (like DAI) to either mint and sell more stablecoins or to buy back stablecoins from the market. The type of bond offered depends on the direction of the price deviation and the discount offered depends on the magnitude of price deviation. The protocol also defines a small tolerance level where neither bonds are sold because the price deviation of the stablecoin is inconsequential.

![Dynamic pricing and sale of stabilizing bonds](<../.gitbook/assets/Stabilizing Bonds (1).png>)

### Expansionary Bonds

Expansionary bonds are offered when the price of the stablecoin in the liquidity pool is higher than that on the oracle. This usually indicates an expansion in the usage of the particular stablecoin outside the protocol, which increases the price of the stablecoin on the liquidity pool when they are overbought. In such cases, the assets obtained from the bond sale will be used to mint more stablecoin to be sold on the liquidity pool, effectively lowering the price of the stablecoins.

![Expansionary bond sales decrease the price of stablecoins on liquidity pool](<../.gitbook/assets/Expansionary Bonds.png>)

In the example above, you can see that SGD-T is more expensive than the oracle price which is 0.73. In this case, the protocol quotes a bond for DAI to back and mint 1000 SGD-T to be swapped on the pool for 752 DAI. This has the effect of bringing the spot price closer to the oracle price, from 0.76 to 0.745.

### Contractionary Bonds

Contractionary bonds are offered when the price of the stablecoin in the liquidity pool is lower than that on the oracle. This usually indicates a contraction in the usage of the particular stablecoin outside the protocol, which decreases the price of the stablecoin on the liquidity pool when they are oversold. In such cases, the assets obtained from the bond sale will be used to swap for the stablecoins to be burnt, effectively increasing the price of the stablecoins.

![Contractionary bond sales increase the price of stablecoins on liquidity pool](<../.gitbook/assets/Contractionary Bonds.png>)

\
In the example above, you can see that SGD-T is less expensive than the oracle price which is 0.73. In this case, the protocol quotes a bond for 1000 DAI to be swapped on the pool for 1408 SGD-T. This has the effect of bringing the spot price closer to the oracle price, from 0.7 to 0.72.

### Bond Price Calculation

The bond discount is calculated by the following formula:

$$
discount = min(maxDiscount, controlVariable*priceDeviation^2)
$$

This allows more disproportionally more discounts to be applied during times where there is a greater deviation between the oracle price and the liquidity pool price.

### Security Concerns

To prevent the gaming discounts on the bond, the bond will be using the time-weighted average price (TWAP) of the liquidity pool to protect itself against flash loan attacks.

In addition, there will be a limit on the amount of bond purchasable which is a function of the maximum amount of assets required in the swap to get the liquidity pool to be priced correctly, as well as a cap on the maximum discount available to the bonder.
