# Protocol Comparison

For DeFi users familiar with other protocols like OlympusDAO, MakerDAO, etc, this section provides a section to help you quickly understand what are some of the similarities and differences between Bluejay Finance and some of the more familiar protocols.&#x20;

### vs OlympusDAO

Bluejay Finance's protocol-owned liquidity (POL) is inspired by the success of [OlympusDAO](https://www.olympusdao.finance), allowing for a more predictable supply of liquidity for our stablecoins users. In addition, Bluejay makes use of existing bonding mechanics from Olympus for the treasury bond where the bonds are priced as a function of the debt ratio and a control variable. However, Bluejay introduces significant changes to how the treasury is used by deploying them as operational capital for a stablecoin issuer.

**Similarities**

* Bonding mechanism (only Bluejay's Treasury Bonds)
* Protocol-owned liquidity
* DAO controlled treasury

**Differences**

* Simplified smart contracts for bonding
* Treasury deployed for stablecoin issuing
* Per-second compounding for staked assets (vs per-epoch on OlympusDAO)
* Stabilizing bonds for pegging stablecoin prices
* Protocol revenue generated from protocol growth and stablecoins' utility

### vs MakerDAO

Bluejay Finance's governance model is inspired by the dual-token model of [MakerDAO](https://makerdao.com) where the stablecoin issued is pegged to a value and the governance token act as an asset for value accrual and governance. Unlike MakerDAO, Bluejay does not impose rent on stablecoins, in the form of a stability fee, but instead collects revenue from swaps on the liquidity pools. In addition, Bluejay simplifies the process of creating stable assets for stakeholders, by managing the risk at the protocol level as opposed to having users manage individual debt positions.&#x20;

**Similarities**

* [Dual-token](https://www.linkedin.com/pulse/ep-53-basic-primer-token-design-dai-makerdao-og-stablecoin-tan/) mechanism
* Value accrual on governance token
* Governance token to recapitalize issued stablecoins as last-resort

**Differences**

* Multi-stablecoin model
* Liquidity backed stablecoins (vs collaterals backed stablecoin on MakerDAO)
* Value generated from utility (vs [rent](https://makerdao.world/en/learn/vaults/stability-fees/) on MakerDAO)
* Protocol managed positions (vs user-managed position on MakerDAO)

### vs Angle Protocol

Bluejay Finance's multi-stablecoin model is inspired by [Angle Protocol](https://www.angle.money). Both protocols aim to present different approaches to creating stablecoin issuance platforms that are capital-efficient. The main difference is the way we approach liquidity (protocol-owned or user-owned) and risk (internalizing within the protocol or externalizing to hedging agents)/

**Similarities**

* Multi-stablecoin model
* Capital-efficient model that avoids excessive overcollateralization

**Differences**

* Protocol-owned liquidity
* Internalizing exchange risk (vs selling to [hedging agents](https://docs.angle.money/concepts/hedging-agents) on Angle)

### vs Frax Finance

Bluejay Finance's capital-efficient model is inspired by [Frax Finance](https://frax.finance). Both protocols optimize the use of capital while balancing capitalization risk. The main difference is that Frax was designed as a fractional reserve model while Bluejay has a more dynamic range for the collateralization ratio.

**Similarities**

* Fractional reserve model

**Differences**

* Multi-stablecoin model
* Stabilizing bonds to bring prices to peg (vs [minting & redeeming](https://docs.frax.finance/minting-and-redeeming) on Frax)
* Protocol-owned liquidity & price stabilizer
