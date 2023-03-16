# FAQs on bluSGD

<details>

<summary>How is bluSGD collateralised? Any numbers we can refer to?</summary>

Each $bluSGD is backed by $DAI and $XSGD in the treasury.

You may refer to the amount of assets held in the treasury against the outstanding bluSGD supply.

As it stands on 16 Mar 2023, the protocol has the following assets against 732k of bluSGD as liabilities:

* 443,195 DAI tokens (305k via LP tokens)
* 180,110 xSGD tokens
* 497,707 bluSGD tokens (411k via LP tokens)

This effectively means that for each bluSGD in circulation, the protocol holds:

* 0.769 xSGD
* 1.89 DAI

At the market price, the collateral ratio of bluSGD token is 3.32x

</details>

<details>

<summary>How did bluSGD maintain its peg during extreme market volatility?</summary>

[The Price Stabilizer](https://docs.bluejay.finance/blustables-core-concepts/price-stabilizer) keeps bluSGD priced correctly despite the volatility of DAI token.

In addition, the team has performed defensive maneuvers to defend the price from secondary effects.

A full report on the event is available [here](https://medium.com/bluejay-finance/community-update-impact-of-usdc-svb-events-on-bluejay-233ebf49138f).

</details>

<details>

<summary>Was there any impact on bluSGD's performance during the extreme market volatility that happened during USDC crisis?</summary>

Despite high volatility in the market, bluSGD retained an excellent correlation with SGD throughout the period.

A full report on the event is available [here](https://medium.com/bluejay-finance/community-update-impact-of-usdc-svb-events-on-bluejay-233ebf49138f).

</details>

<details>

<summary>What collaterals form the treasury?</summary>

The treasury is currently comprised of DAI, xSGD, and Liquidity Pool tokens. Note, that we do not count Bluejay Finance issued tokens as part of the treasury for collateral purposes. \
Core concept of collateralization is available [here](https://docs.bluejay.finance/blustables-core-concepts/collateralization).

</details>

<details>

<summary>What happens if the treasury collaterals lose value?</summary>

Collaterals included in the treasury are selected based on their security and stability.

To guard against fluctuations in value, even large fluctuations, bluStables are overcollateralized to ensure they remain fully backed.

We also select different assets, such as DAI and xSGD to back bluSGD, to avoid correlations. This means that either assets can vary significantly in value and bluSGD holders can still be protected from their volatility.

</details>

<details>

<summary>Will bluSGD be affected by DAI or xSGD depegging?</summary>

As the protocol maintains excess collaterals in uncorrelated assets, the protocol will still be able to operate even if the value of collateral changes in a short period of time.

However, the protocol can run into the risk of being insolvent in the short term when value of assets fall below certain levels. \
The team remains committed to avoid such events by monitoring the market condition and executing our contingency plans in scenarios of extreme volatility.

</details>

<details>

<summary>Are there plans to diversify the treasury in the future?</summary>

We are committed to maintaining high quality assets in the treasury to back bluStables.

It is possible for through the DAO to discuss and execute on the addition of other collaterals in the future.

</details>

<details>

<summary>Was there any impact on Bluejay Finances reserves due to USDC crisis?</summary>

There was a negligible impact on the treasury as the team act to provide additional liquidity during the volatile period.

The details of the impact can be found [here](https://medium.com/bluejay-finance/community-update-impact-of-usdc-svb-events-on-bluejay-233ebf49138f).

</details>

<details>

<summary>Will you expand on the use cases of bluStables in the future?</summary>

We are starting to build out use cases for our bluStables. Bluejay Earn is the first iteration of that ecosystem. It allows holders of bluSGD to earn yield on their bluSGD by investing in fixed-income products.

The protocol is exploring sustainable means for users of bluStables to benefit from. Such request could be discussed and executed from the DAO.

</details>

<details>

<summary>How does bluSGD differ from SGD? How does it differ from xSGD? Why would I hold bluSGD instead of xSGD?</summary>

**bluSGD** is a digital token that is pegged to the Singapore dollar (SGD) on a 1:1 basis. It is an ERC-20 token that runs on the Ethereum blockchain, which means that it can be used in the same way as any other ERC-20 token.

**xSGD** is another stablecoin offered by Xfers Pte Ltd that is pegged to the Singapore Dollar and has facilities for fiat redemption.

While both tokens attempt to track SGD, there are differences such as:

* xSGD can be redeemed and minted directly via on/off ramps provided by the issuer while bluSGD does not have similar facilities
* bluSGD is a decentralized stablecoin that can be more resilient to the regulatory changes (ie banking crisis)
* The tracking error for both coins are different. You may read a case study of the difference in performance in both coins during the USDC crisis [here](https://medium.com/bluejay-finance/community-update-impact-of-usdc-svb-events-on-bluejay-233ebf49138f) .
* bluSGD exists in the same ecosystem as Earn and pools using bluStables enjoy a fee waiver. See the core concepts about fees [here](https://docs.bluejay.finance/bluejay-earn-core-concepts/fees).

</details>

<details>

<summary>What is the difference between bluSGD and algorithmic stablecoins like UST? Won’t we face similar depeg risk?</summary>

Unlike UST/Terra, we are a fully collateralized stablecoin, so we are not subject to the same down-spiral risk of Terra.

</details>

<details>

<summary>What kind of use cases are currently available today with bluSGD? What are the integrations available?</summary>

bluSGD users gets exclusive and fee-less access to investment opportunities offered in the Bluejay Earn marketplace.

In addition, holders can diversify exposure from existing USD assets held on chain or use it to transfer larger amount of value around.

</details>

<details>

<summary>Is bluSGD licensed by any monetary authorities?</summary>

bluSGD is not licensed by any monetary authorities as we are a fully decentralized stablecoin and do not operate any on/off ramp facilities in any jurisdiction.

</details>

<details>

<summary>What is the MAS’s view currently on stablecoins?</summary>

Here’s the suggested read about the framework on stablecoins by MAS. [https://www.moodysanalytics.com/regulatory-news/dec-12-22-mas-consults-on-framework-for-stablecoin-related-activities](https://www.moodysanalytics.com/regulatory-news/dec-12-22-mas-consults-on-framework-for-stablecoin-related-activities)

</details>

<details>

<summary>Has bluSGD reserves been invested into other protocols to earn yield?</summary>

Each $bluSGD is backed by the treasury that is currently comprised of DAI, xSGD, and Liquidity Pool tokens.

We do not reinvest assets to other protocol so that our stablecoins are backed by low-risk assets and that we can maintain the highest level of liquidity for our users.

The protocol maintains that we do not risk customer assets for short term gains, you may read about the risk of doing so [here](https://cointelegraph.com/news/euler-attack-causes-locked-tokens-losses-in-11-defi-protocols-including-balancer).

</details>

<details>

<summary>How do I obtain bluSGD today? What are the best routes of getting there?</summary>

There are two ways to swap to bluSGD: through Uniswap or the PSM module. \
The most effective route depends on the prevailing market conditions as well as the type of assets you have.\
\
As a rule of thumb, we suggest:

**If you have access to Singapore bank accounts**, we recommend you to on-ramp with xSGD and swap the asset using our xSGD ←→ bluSGD swap.

**If you already have xSGD**, we recommend you swap the asset using our xSGD ←→ bluSGD swap.

**If you already have digital assets like ETH, USDC, USDT or DAI**, we recommend you swap the assets using Uniswap. For much larger trade, you may consider using limit order exchange like CowSwap or 1Inch.

Check here for more detailed [user-guide](https://docs.bluejay.finance/user-guides/buying-and-selling-blusgd).

</details>

<details>

<summary>What is the reason for having non-USD stablecoins like bluSGD when there are already so many USD-pegged stablecoins in the market?</summary>

Real world business transacts in many currencies other than USD. Having digital representation of the different currencies allow businesses and individuals to trade in currencies they are familiar in.

One example is that a business in Philippines who is sending invoice and receiving payment in PHP will not want to send payments in USD or borrow funds in USD due to extra foreign exchange exposure. The existence of digital PHP will allow such business to have simpler business operations and can create opportunities for foreign exchange (FX) and FX derivative markets on-chain.

</details>

