# Collateralization

Bluejay Finance uses liquidity to back the stablecoins, allowing stablecoins to be directly swappable for reserve assets on decentralized exchanges. Combining that with the stabilizing bonds, the protocol allows for stablecoins issued to be backed with both liquidity and collaterals.

### How demand of stablecoins in circulation affects treasury's reserves&#x20;

To understand how the stablecoins are collateralized, one needs to understand that there will be Bluejay's stablecoins in circulation, outside of the DAO. Some examples of such stablecoins:

* Stablecoins held in stakeholders' externally-owned accounts
* Stablecoins held in by other protocols' treasuries or reserves
* Stablecoins on liquidity pools and are not owned by the DAO treasury

Having more of these stablecoins in circulation, and not owned by the DAO through its liquidity ownership, means that there are fewer of these stablecoins in the liquidity pool, hence putting upward price pressures on the stablecoins on the pools.&#x20;

> The higher demand for stablecoins makes them more expensive.

Since the protocol will automatically issue the stabilizing bonds, specifically the expansionary bond, bonders can post more reserve assets for the protocol to mint more stablecoins to be swapped on the liquidity pool, bringing the price down to peg. The effect of this is that:

* Reserve assets (ie DAI) is added to the Treasury
* Stablecoin Engine mints more stablecoin
* Stablecoin Engine swaps stablecoin for reserve assets on liquidity pool to be kept in Treasury
* Price of the stablecoin falls when there are more stablecoin in reserve and fewer reserve assets in reserve&#x20;

> Expansionary (stabilzing) bonds increases reserve assets in Treasury and releases more stablecoins into circulation while keeping prices to peg

In this case, the stablecoins in circulation are technically backed by the reserve assets held in the Treasury when expansionary bonds are retroactively sold when there is increased demand for the stablecoin.&#x20;

When there is less demand for stablecoin, the contractionary bonds will be sold. In that scenario:

* Stablecoin Engine buys back the stablecoin on the liquidity pool
* Stablecoin Engine burns the stablecoin received and removes it from circulation
* Price of the stablecoin rises when there are fewer stablecoin in reserve and more reserve assets in reserve

> Contractionary (stabilizing) bonds sells reserve assets in Treausry and removes stablecoins from circulation to keep price to peg&#x20;

### Understanding collateralization

![Initial states](<../.gitbook/assets/image (7).png>)

In the early days of the protocol, the protocol will be over-collateralized. That means that the value of the DAI held in the treasury will be more than or equal to the aggregate value of all the stablecoin in external circulation. In the diagram above, the DAI in the treasury backs the SGD-T in external circulation.

The stablecoins held by the protocol, through the liquidity tokens, are backed 1-1 with the reserve assets it is paired up with.&#x20;

Since the protocol can be used to issue other assets, the reserve asset can be used to create new stablecoins and their liquidity pool. That means there will be more than one type of liquidity token held by the treasury.&#x20;

![](<../.gitbook/assets/image (2).png>)

Once the protocol has reached a certain scale and stability, where it is possible to forecast the number of stablecoins in circulation, it is possible for the protocol to transit into a fractional reserve model. This means that the reserve assets held in the treasury have a lower value than the aggregate value of all the stablecoins in circulation. Moving into a fractional reserve model means that the protocol becomes more capital efficient (ie 1 USD of assets can be used to back >1 USD of stablecoins), but also increase the risk of the protocol to remain solvent and retain the peg of the issued stablecoins.

### Collateralization ratio as a governance-controlled parameter

The ideal collateralization ratio and allocation of treasury into the different stablecoins will be parameters controlled by the DAO through voting. This means that the community will have to be comfortable and agree to the risk level of the protocol.&#x20;



