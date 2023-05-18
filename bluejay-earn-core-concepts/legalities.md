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

Bluejay Earn is a decentralised credit protocol that provides a platform for borrowers and investors to interact and transact. The protocol acts as a marketplace for loan pools and enables investors to earn yield by participating in these pools. The role of the protocol is to facilitate the lending and borrowing process by connecting borrowers and investors.

However, it is important to note that the protocol is not a counterparty to the loan and thus, the protocol is not responsible for ensuring the accuracy of information presented by the borrower, and for providing legal opinion. Furthermore, the protocol does not act as a guarantor to the loan and does not provide securities to the loan. The protocol simply provides the platform as-is and does not participate directly in the deals. Investors are responsible for performing their own due diligence prior to depositing funds in any available borrower pools. The protocol acts as a facilitator, providing the tools and infrastructure to support lending and borrowing, but it is up to the investors to assess the risk and make informed decisions and the borrowers to ensure provisioning of accurate information and regulatory compliance. This decentralised structure provides a secure, efficient and more accessible alternative to traditional lending and borrowing methods.

During the beta phase of the protocol, Bluejay Earn may facilitate the onboarding of select borrowers who are not yet familiar with borrowing and lending in the DeFi space. This service is designed to help the borrowers get up to speed with the process and to ensure that they are able to participate in the loan pools effectively.&#x20;

## Flow of Funds

Investors will be depositing their funds directly into a borrower pool using stablecoins. Borrowers will interact with the protocol to withdraw funds (deployment) or to deposit funds (repayment) using stablecoins. Refer to the following diagram to understand the high-level workflow. Note that specific flow of funds documents can be found in the dataroom of each borrower pool.

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

Borrowers are responsible for specifying what kind of recourse is available to the investors under the loan terms. Since investors are holding loan pool tokens proportional to the loan provided, they may form a investors collective (or mini-DAO) to deliberate on further actions.&#x20;

This process may involve additional cost on the investors to appoint legal or non-legal representatives to seek recourse or pursue the borrower directly.

For selected pools where Bluejay acts as a facilitator, the investors collective may request for Bluejay to facilitate such proceedings. Cost involved with proceedings will still be borne by the investors' collective.

Note that this is a generalised version of the default procedure. Refer to dataroom of specific deals to see respective procedures for dealing with default.

### Limitation of Liability

The protocol shall not be liable to the investors and borrowers for any loss, damages, expenses, claims, costs (including, but not limited to legal costs), expenses arising from all circumstances. The protocol is not responsible for any loss of profits or special, exemplary, consequential or punitive damages, even if informed of the possibility of such damages.
