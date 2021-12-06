# Overview

### Summary

* Bluejay is a platform to issue multiple capital-efficient stablecoins, each backed by liquidity owned by the protocol.
* Prices of the stablecoins are pegged to external oracles through a bonding mechanism.
* Bluejay relies on two groups of stakeholders: stakers and bonders.

### Key Problems

Most stablecoin solutions are centered around USD and not designed for other currencies. This means that users do not have a choice of having exposure to currencies other than USD in the DeFi space.

By having stablecoins of different currencies around the world on the blockchain, we lower the barrier for businesses and individuals in these countries to transact without currency exchange risk. This helps to widen the product offerings of existing DeFi companies that provide crypto invoicing (ie [Request](https://request.network/en/)), streaming payments (ie [Sablier](https://sablier.finance)), etc.

Full-reserve stablecoins that are fiat-backed are not scalable in either volume, liquidity, or product types as they are often encumbered by regulators, custodian services, and other service providers.

Existing solutions using overcollateralization are also facing pressure by the community to deploy the collaterals as working capital, thereby resulting in increased risk exposure to the protocol itself.

#### Bluejay's Approach

Bluejay Finance allows stablecoins to be provided, with deep liquidity backing directly from a DAO through protocol-owned liquidity.

Some key elements of our designs:

* Bonding mechanism to fund stablecoin minting
* Protocol-owned liquidity to back stablecoins
* Stabilizer bonds for bringing stablecoins to peg

The DAO will be using a bonding mechanism, popularised by OlympusDAO, to allow users to own a stake of the DAO and bring additional funds into the DAO’s treasury. Users will be able to exchange collaterals (ie DAI) or liquidity provider tokens for the stablecoins for its native governance token.

The DAO’s treasury will comprise mostly liquidity provider tokens, which represent an equal proportion of stablecoin and collaterals staked on a decentralized exchange. This eliminates the need for excessive collaterals to be kept to back the stablecoins as they are backed by liquidity directly. The design also creates predictable liquidity for the stablecoins supplied as there is no reliance on external liquidity providers.

In addition to those bonds, the DAO also issues different stabilizing bonds, depending on whether the stablecoin is overpriced or underpriced in relation to real-world pricing. These bonds allow users to buy the governance token at a discount relative to the deviation between the prices and its proceeds will be used to swap assets on the liquidity pool to bring the on-chain price to peg.

Finally, the DAO is governed by its native governance token, the BLU token.

### Stakeholder

The protocol depends on two groups of stakeholders, the stakers and bonders.

**Stakers** helps to stabilize the protocol by locking up supplies of the BLU token while expanding the supply of the BLU, while the protocol is growing. Stakers rewards are ultimately tied to the overall growth of the protocol - profit is made when the protocol growth exceeds token supply growth. As Bluejay expands into more currencies around the world, the protocol's growth will be accelerated by its network effect.

**Bonders** help to grow the protocol by introducing more reserves and liquidity into the treasury through treasury bonds and peg the stablecoin prices through the stability bonds. Bonders are rewarded in the short term through direct discounts on the BLU's price.
