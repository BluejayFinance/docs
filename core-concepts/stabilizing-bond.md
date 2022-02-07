# Stabilizing Bond

Stabilizing bonds are bonds that help to correct the liquidity pool's price to bring them to peg. It's a mechanism for the protocol to incentivize bonders to help correct the stablecoin prices automatically. Two forms of stabilizing bonds are available for each liquidity pool, expansionary bonds, and contractionary bonds.

![Dynamic pricing and sale of stabilizing bonds](<../.gitbook/assets/Stabilizing Bonds (1).png>)

### Overview

Expansionary bonds are bonds sold when the price of the stablecoin on the liquidity pool is higher than that on the oracle. The bond has the effect of putting downward price pressure on the stablecoin in the liquidity pool.

Contractionary bonds are bonds sold when the price of the stablecoin on the liquidity pool is lower than that on the oracle. The bond has the effect of putting upward price pressure on the stablecoin in the liquidity pool.

Both types of bonds have discounts proportional to the price difference between the liquidity pool's price and the oracle's price.

### Bond Price Calculation

The bond discount is calculated by the following formula:

$$
discount = min(maxDiscount, controlVariable*priceDeviation^2)
$$

This allows more disproportionally more discounts to be applied during times where there is a greater deviation between the oracle price and the liquidity pool price.

### Security Concerns

To prevent the gaming discounts on the bond, the bond will be using the time-weighted average price (TWAP) of the liquidity pool to protect itself against flash loan attacks.

In addition, there will be a limit on the amount of bond purchasable which is a function of the maximum amount of assets required in the swap to get the liquidity pool to be priced correctly, as well as a cap on the maximum discount available to the bonder.
