---
description: >-
  Prior to using Bluejay Earn, you are strongly recommended to seek advice from
  your own legal and tax counsel in your jurisdiction to ensure full compliance
  in your jurisdiction.
---

# Legalities

In this section we will be covering important legal and regulatory aspects for you to get started with the protocol:

1. The role of the protocol
2. Flow of funds
3. Legal structure
4. Dealing with borrower defaults
5. Risk disclosure

## The role of the protocol

Bluejay Earn is a decentralised credit protocol that provides a platform for borrowers and lenders to interact and transact. The protocol acts as a marketplace for loan pools and enables lenders to earn yield by participating in these pools. The role of the protocol is to facilitate the lending and borrowing process by connecting borrowers and lenders.

However, it is important to note that the protocol is not a counterparty to the loan and thus, the protocol is not responsible for ensuring the accuracy of information presented by the borrower, and for providing legal opinion. Furthermore, the protocol does not act as a guarantor to the loan and does not provide securities to the loan. The protocol simply provides the platform as-is and does not participate directly in the deals. \Lenders are responsible for performing their own due diligence prior to depositing funds in any available borrower pools. The protocol acts as a facilitator, providing the tools and infrastructure to support lending and borrowing, but it is up to the lenders to assess the risk and make informed decisions and the borrowers to ensure provisioning of accurate information and regulatory compliance. This decentralised structure provides a secure, efficient and more accessible alternative to traditional lending and borrowing methods.

During the beta phase of the protocol, Bluejay Earn may facilitate the onboarding of select borrowers who are not yet familiar with borrowing and lending in the DeFi space. This service is designed to help the borrowers get up to speed with the process and to ensure that they are able to participate in the loan pools effectively.&#x20;

## Flow of Funds

Lenders will be depositing their funds directly into a borrower pool using bluSGD stablecoins. Borrowers will interact with the protocol to withdraw funds (deployment) or to deposit funds (repayment) using bluSGD stablecoins. Refer to the following diagram to understand the high-level workflow. Note that specific flow of funds documents can be found in the dataroom of each borrower pool.

<figure><img src="https://lh3.googleusercontent.com/uZM0ftdPvym8LD1vrQAzD3x2EsDkptI8tHTHqFjE87wWyZOVUw65VosoYBmgxKHShO_F_q9Lj1kyHcclIQTjPUSlH6SqSO_TJefRDLgYThxAoF_hrJSO3xDIvIwvnGcIN8OlRUA-r2g-zGAbZXFHMVQ" alt=""><figcaption></figcaption></figure>

### Off-ramp into Fiat

When the loan pool is fully funded, borrowers can access the funds by withdrawing from the pool. In order to off-ramp the funds into fiat, borrowers can use our [Peg Stability Module](https://docs.bluejay.finance/faq/mainnet-user-guides/peg-stability-module-psm) to swap bluSGD into xSGD and use [StraitsX’s business account](https://www.straitsx.com/business-account) to off ramp into fiat SGD.

For borrowers who prefer to withdraw their funds in USD, they may also convert bluSGD to USDC using Uniswap (underlying route: bluSGD <> DAI <> USDC) and use any preferred exchange or even [StraitsX](https://www.straitsx.com/blog-post/product-usdc-usd-transfers-are-now-supported) to withdraw funds in USD.

### On-ramp from Fiat

In order to on-ramp from fiat into bluSGD to repay for loans, borrowers can follow the process in reverse. They can use either StraitsX or any exchange of choice to convert SGD/USD fiat into xSGD. They would then be able to convert xSGD into bluSGD using our Peg Stability Module and proceed with their repayment.

## Legal Structure

This section explores a few structures which borrowers can use to structure their deal to raise debt capital from Bluejay Earn. We will be using a Fintech marketplace proposing a borrower pool as an example (applicable only to verified borrowers):

<figure><img src="https://lh4.googleusercontent.com/dULfbsMv1Bag0hvcK7qFv6oWyDk0_QnkKwvgrOCaOFKQI4Qg8TIWyZyJh3v6BzpiQ33ALetHdG5ZAIZNNgoG66Pk0y7P7G_HtqoWLIlXRUt86ZpbnZy0kcfqhw8b2-LDcRUWgYbdnhwB_Jf8o42pMFY" alt=""><figcaption></figcaption></figure>

Special Purpose Vehicle (“SPV”): this is used as an intermediary to facilitate fund withdrawals and repayment on behalf of the borrower (FinTech in this example).

## Dealing with Borrower Defaults

When the borrower fails to pay beyond the grace period, the loan will start to incur a late fee which is added on top of the initial interest rate.

Borrowers are responsible for specifying what kind of recourse is available to the lenders under the loan terms. Since lenders are holding loan pool tokens proportional to the loan provided, they may form a lenders collective (or mini-DAO) to deliberate on further actions.&#x20;

This process may involve additional cost on the lenders to appoint legal or non-legal representatives to seek recourse or pursue the borrower directly.

For selected pools where Bluejay acts as a facilitator, the lenders collective may request for Bluejay to facilitate such proceedings. Cost involved with proceedings will still be borne by the lenders collective.

Note that this is a generalised version of the default procedure. Refer to dataroom of specific deals to see respective procedures for dealing with default.

### Limitation of Liability

The protocol shall not be liable to the lenders and borrowers for any loss, damages, expenses, claims, costs (including, but not limited to legal costs), expenses arising from all circumstances. The protocol is not responsible for any loss of profits or special, exemplary, consequential or punitive damages, even if informed of the possibility of such damages.

## Risk Disclosure

Bluejay Earn is in its beta stage, which means that the Bluejay Earn App, and all related software, including blockchain software and smart-contracts, are experimental. The platform is provided on an “as is” and “as available” basis, without warranty of any kind.

Investing in alternative investment opportunities is a high risk endeavour. Lenders are strongly encouraged to carefully evaluate opportunities available to them. It is necessary before lenders make any decision, they should understand the following:

100% loss of invested capital: investment in any amount in any opportunity does not guarantee returns. The lender may lose their principal partially or in full. Lending is a risky affair and lenders may not be able to recover, on a timely basis or at all, the full principal and/or the return accrued there on.

Past performance and forecasts: Borrowers may have presented certain forward-looking information based on past performance and certain assumptions which may be relevant for current macroeconomic scenarios. However, past performance is not a reliable indicator of future performance. Lenders should not rely on any past performance as a guarantee of future performance. Forecasts may also not be a reliable indicator of future performance.

Incomplete information: Information and data presented by the borrowers may not be complete and accurate. There may be some information related to the borrower or its underlying collateral which may not be shared due to confidentiality which otherwise may have material adverse impact. The protocol, as a platform, is not obligated to ensure accuracy and completeness of the information.

Smart contract risk: The smart contracts being used are unaudited during the beta stage and are of highly experimental nature. You should not interact with the protocol unless you fully understand how it works, and the consequences of transactions carried out with the use of the protocol.

Stablecoin risk: Cryptocurrencies are volatile, risky, and experimental in nature. Even when dealing with stablecoins, you are encouraged to understand how the stability mechanism of the stablecoin in use works. While stablecoins tend to be less volatile, they still carry risk&#x20;

\
