# Overview

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>Architecture of the Earn product</p></figcaption></figure>

### Overview

The Earn product consists of multiple key components. The roles of the various components are described below:

#### LoanPoolFactory

The factory is responsible for creating new loan pools and maintaining a registry of loan pools created by the factory.&#x20;

The factory creates a minimal proxy of the LoanPool and a registered CreditLineTemplate to create new pools.

#### LoanPool

The LoanPool contract is responsible for interacting with the lenders and borrower directly. Borrowers will be able to drawdown on the funds when the pool is successfully funded as well as repaying their loans. Lenders will be able to fund the pools when they are available for funding as well as withdrawing their share of repayments when the borrower has made them.

Every LoanPool will own its own credit line contract which accounts for the loan.

#### CreditLineTemplate

The CreditLineTemplate is a class of contracts that is responsible for accounting for the loan. Its main responsibility is to determine the repayment schedule against the initial principal amount and [other parameters](glossary.md). It will also account for any extra fees such as late payment fees.&#x20;

There are different implementations of the CreditLineTemplate such as the CreditLineAmortized or CreditLineBalloon

#### CreditLineAmortized

This is a flavour of the CreditLineTemplate which allows the borrower to pay back the loan with equal payments during each payment period towards both the principal and interest amount.

#### CreditLineBalloon

This is a flavour of the CreditLineTemplate which allows the borrower to pay back the loan with only interest payments until the final payment period where both the interest and principal is repaid together. Another name for this style of repayment is Bullet loan.

#### LoanPoolViewer

The viewer contract is a utility contract that frontends can use to quickly access information on the loan pool. It returns data from the loan pool, credit line, and funding asset.
