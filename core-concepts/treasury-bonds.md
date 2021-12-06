# Treasury Bonds

Treasury bonds are a mechanism for the protocol to obtain reserve assets and liquidity tokens for its operations.

![Token flow for Bond Sale](<../.gitbook/assets/image (3).png>)

### Overview

Bonders can buy BLU bonds from the TreasuryBondDepository with reserve assets like `DAI` or with liquidity tokens like `BLU/DAI LP` or `SGD-T/DAI LP`. The treasury quotes the user the bond price that is a function of the debt ratio of the bond depository as well as a control variable. Users will be able to determine if the quoted bond price is a fair market discount, compared to the price of BLU on the open market.

If the user chooses to purchase the bond, the user will exchange the assets for the bond. The bond will be vested linearly over the vesting period and the bonder may choose to redeem the vested BLU at any point in time, the full amount will be available when the bond matures at the end of the vesting period.

When the bond is purchased, the DAO also receives a fee from the sale of the bond.

#### Bond Parameters

The parameters of the bond are determined by the current monetary policy found in the Bond Governor contract that can be set only by the DAO.

These parameters include:

* Bond control variable
* Total debt ceiling
* Minimum bond price
* Minimum bond size
* Maximum bond size
* Fees

#### Bond Price Calculation

The bond price is determined by the following equation:

$$
price = 1+controlVariable*debtRatio
$$

The bond price is proportional to the debt ratio of the bond depository. This means that when more bonds are sold over the last period, the higher the price of the bond.

In addition, the control variable is set by the DAO to allow the bond price to fluctuate across different ranges as well as to set the relative proportion of assets to accept into the treasury.

As you may observe, the price is independent of external market price, this allows the market's demand for the bond to determine the price.
