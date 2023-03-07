# Fees

Fees in the Bluejay Earn protocol is calculated in a simple manner.&#x20;

The protocol charges an `Origination Fee` upon the successful funding of a loan pool.&#x20;

### Fees Charged

The protocol has a tiered approach for charging fees based on the type of assets used for the loan.&#x20;

Loan pools which uses Bluejay Stablecoins (aka bluStables) do not incur any fees upon successful funding.&#x20;

Loan pools using any other assets (ie USDC, agEUR, xSGD, etc) will incur 10 basis points of fees.&#x20;

Fees are charged to the borrower when they drawdown from the loan.

Ie. A borrower who raised 1M USDC from the pool will pay 1,000 USDC to the protocol upon successful funding. The principal of the loan will hence be set to 999,000 USDC.&#x20;

### Successful Funding

A loan pool is deemed to be successfully funded when:

* The pool has raised assets greater than the minimum funding required by the borrower, and
* The borrower has drawndown on the loan before the drawdown period ends.

As such, the fees are not applied in the following scenarios:

* When a pool has met not met the minimum funding by the funding end time.
* When a pool has met the minimum funding but the borrower did not manage to drawdown in time.&#x20;

In both of such scenario, the investors will be refunded in full.&#x20;

