# Loan Lifecycle

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Overview of the loan lifecycle</p></figcaption></figure>

Loan pools are created by borrowers with specific loan terms and will transit to and from different state which defines the type of action available to both lenders and borrower. Below are the description of the different states of the loan pool:

### Before Funding Start

When the loan pool is created, and has not reached the agreed timestamp that it will start receiving funds, it will be in this state.&#x20;

In this state, both borrower and lenders do not have the ability to interact with the loan pool except to wait for the loan pool to start receiving funds.&#x20;

Note: At this point and beyond, the loan terms have already been defined by the borrower and are immutable. That means the borrower may not make any changes to the interest, loan amount, late fees, etc.

### Open for Funding

Once the time for the pool to receive funds arrives, the pool will transit into this state. This means that lenders will be able to deposit funds into the loan pool contract.&#x20;

The loan pool will be able to receive funds up to the maximum amount the borrower is willing to borrow. The loan pool will also be able to receive funds for as long as the funding period last, unless the maximum amount has been reached.&#x20;

From this point, the pool may transit into either the `Successful Funding` or `Refund` state depending on various conditions.&#x20;

### Refund

The loan pool will enter into the refund state when one of the two conditions applies:

* The minimum funds level is not reach AND the funding period has ended, or
* The borrower has failed to drawdown on the funds after the drawdown period has ended

The drawdown period is a failsafe mechanism to prevent borrowers from locking up lenders fund if the borrower fails to drawdown the loan for any reasons.&#x20;

In either of these scenarios, lenders will be able to withdraw all assets from the loan pool and the borrower will be unable to access the funds.

### Successful Funding

A pool is closed off to further injection of funds when either:

* The maximum funds has been raised, or
* The minimum funds has been raised and the funding period has ended

In this state, lenders are unable to perform any action other than waiting for the borrower to drawdown on the loan.

Borrowers will be able to drawdown the assets from the loan pool at any point after the minimum amount of funds is raised. Once the borrower initiates the drawdown process a few things will happen:

* All funds raised in the pool will be transferred to the borrower, minus any [fees](fees.md)
* Lenders will no longer be able to add more funds into the pool
* Interest calculation will start at this point, not before
* Borrowers will have to make their first repayment after one period from this point in time

### Repayment

After the drawdown has happened, the borrower will be subjected to make repayment towards the loan. When a repayment occurs, lenders will have the ability to withdraw any of the repaid balance, prorated to his share of the loan pool.

Since each loan will specify its own repayment period, the first repayment will be one period away from the drawdown date.&#x20;

For example, if a loan has 30 days repayment period and the drawdown happens on the 1st Jan 2023, the first repayment is expected to be on the 31st Jan 2023. The next repayment will be on 2nd Mar 2023, and so on.

During the repayment period, the borrower will have a grace period for each repayments where late fees are not charged. As long as the borrower repays before the determined date plus the grace period, the loan will not be in a default.&#x20;

Adding to the example above, if the loan has a 7 days grace period, the borrower has until 8th Jan 2023 to make the first repayment and 9th Mar 2023 for the second repayment.&#x20;

If the borrower is unable to make the repayment before the grace period ends, the loan is considered to be in default and the late fees is imposed.&#x20;

In the event a default happens, depending on the predetermined loan term, lenders may take further actions on the borrowers for recourse.

In the event that the borrower pays off part or all of the loans earlier than the loan term, the early repayments will be made to the principal balance. This will reduce the amount of interest borne by the borrower and the lenders will have access to their capital at an earlier time.

### Fully Repaid

Once the last repayment has been made and the principal balance has been brought to zero, the loan is considered to be fully repaid. No additional interest will be imposed on the borrower.

Lenders will be able to fully withdraw all repayments made towards his share of the loan at this point in time.
