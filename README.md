# Regulated Transaction QA Portfolio

## Overview

This repository is a professional QA portfolio focused on regulated transaction testing across iGaming, Banking and FinTech environments.

The portfolio demonstrates how financial transactions, balances, payments, payouts, reversals, histories, audit trails, API responses and database records can be tested for accuracy, consistency and traceability.

The goal of this repository is to show practical QA thinking in systems where financial correctness, compliance evidence and defect traceability are critical.

## Portfolio Focus

This portfolio focuses on three regulated domains:

| Domain | Testing Focus |
|---|---|
| iGaming | Player balances, wagers, payouts, game history, platform records, back office records and certification evidence |
| Banking | Account balances, debit transactions, credit transactions, EFT payments, reversals and statements |
| FinTech | Payment flows, transaction status, API validation, SQL validation, reconciliation and audit trails |

## Why This Portfolio Exists

Many QA portfolios focus only on basic login tests, UI validation or simple automation scripts.

This portfolio is different.

It focuses on regulated systems where a small transaction error can create financial, compliance, audit or customer trust risks.

The case studies in this repository show how I approach testing when the system must prove that every transaction is accurate, traceable and consistent across multiple sources.

## Core QA Areas Covered

| QA Area | Description |
|---|---|
| Functional Testing | Verifying that system features work according to requirements |
| Financial Logic Validation | Checking balance calculations, debits, credits, payouts, fees and reversals |
| Transaction Reconciliation | Comparing records across UI, history, statements, admin portals, APIs and databases |
| Compliance Testing | Validating systems from a regulated environment perspective |
| Regression Testing | Ensuring new builds do not break previously approved functionality |
| API Testing | Validating responses, statuses, payloads and transaction data |
| SQL Validation | Checking backend records against expected values |
| Defect Reporting | Creating clear, reproducible and risk based defects |
| Test Documentation | Producing structured test cases, test summaries and evidence |
| Risk Based Testing | Prioritising tests based on business, financial and compliance impact |

## Repository Structure

```text
regulated-transaction-qa-portfolio/
│
├── README.md
│
├── iGaming-Case-Studies/
│   ├── Case-Study-1-Game-Transaction-and-Balance-Validation/
│   ├── Case-Study-2-Regression-Testing-for-Certified-Game-Builds/
│   └── Case-Study-3-Multi-Jurisdictional-Compliance-Validation/
│
├── Banking-Case-Studies/
│   ├── Case-Study-1-Bank-Account-Balance-Validation/
│   ├── Case-Study-2-EFT-Payment-Testing-and-Transaction-Reconciliation/
│   └── Case-Study-3-Failed-Payment-Reversal-and-Recovery-Testing/
│
├── SQL-Validation/
│   ├── igaming-transaction-validation.sql
│   ├── banking-balance-validation.sql
│   ├── eft-payment-reconciliation.sql
│   └── failed-payment-reversal-validation.sql
│
├── API-Testing/
│   ├── account-balance-api-tests.md
│   ├── eft-payment-api-tests.md
│   └── transaction-status-api-tests.md
│
├── Defect-Reports/
│   ├── igaming-defect-examples.md
│   ├── banking-defect-examples.md
│   └── fintech-defect-examples.md
│
└── Test-Documentation/
    ├── test-case-samples.md
    ├── reconciliation-tables.md
    └── test-summary-report-samples.md
Case Studies
iGaming Case Studies
Case Study 1: Game Transaction and Balance Validation

This case study validates player balances, wagers, payouts and game round transactions.

It demonstrates how to confirm that financial values are correct across:

Source	Purpose
Game Interface	Player facing balance and result
Game History	Player transaction record
Platform History	Operator platform record
Back Office	Internal transaction record
Database	Backend source of truth

Key validation areas include:

Area	Validation
Opening Balance	Confirms balance before the game round
Wager Deduction	Confirms stake is deducted correctly
Win Amount	Confirms payout is calculated correctly
Closing Balance	Confirms final balance is accurate
Transaction Record	Confirms round ID and transaction ID are traceable
Reconciliation	Confirms all sources show the same values
Case Study 2: Regression Testing for Certified Game Builds

This case study validates a new iGaming build against a previously certified version.

It demonstrates how to check that approved game behaviour, paytable values, rules, help screens, artwork and transaction behaviour remain aligned after a build update.

Key validation areas include:

Area	Validation
Certified Baseline	Compare new build against approved version
Paytable Values	Confirm payout values remain unchanged
Help Screen Rules	Confirm game rules remain complete and accurate
Artwork	Confirm only approved visual changes are present
Wager Limits	Confirm limits remain correct
Game History	Confirm transaction records still work correctly
Defect Retesting	Confirm previous defects remain resolved
Case Study 3: Multi Jurisdictional Compliance Validation

This case study validates an iGaming product against jurisdiction specific requirements.

It demonstrates how market rules can affect test scope, configuration, wager limits, game history, responsible gaming controls and certification readiness.

Key validation areas include:

Area	Validation
Jurisdiction Configuration	Confirms correct market setup
Wager Rules	Confirms limits are enforced
Game Rules	Confirms player facing rules are accessible
Responsible Gaming	Confirms required messages or controls appear
Game History	Confirms required transaction details are displayed
Backend Records	Confirms transaction traceability
Evidence	Confirms results support certification review
Banking Case Studies
Case Study 1: Bank Account Balance Validation

This case study validates customer account balances after debit and credit transactions.

It demonstrates how to confirm that account balances are updated correctly after payments, fees and incoming credits.

Key validation areas include:

Area	Validation
Opening Balance	Confirms starting account balance
Debit Transaction	Confirms money is deducted correctly
Transaction Fee	Confirms fee is applied correctly
Credit Transaction	Confirms incoming money is added correctly
Closing Balance	Confirms final balance is accurate
Statement	Confirms transaction appears correctly
API Response	Confirms API balance matches UI
Database	Confirms backend balance matches expected result
Case Study 2: EFT Payment Testing and Transaction Reconciliation

This case study validates an EFT payment from sender to recipient.

It demonstrates how to test that the sender is debited, the recipient is credited, the transaction fee is applied, the payment reference is created and all records match.

Key validation areas include:

Area	Validation
Sender Balance	Confirms sender balance decreases correctly
Recipient Balance	Confirms recipient balance increases correctly
Transaction Fee	Confirms fee is deducted from sender
Payment Reference	Confirms unique reference is created
Transaction Status	Confirms payment status is accurate
Sender History	Confirms debit appears correctly
Recipient History	Confirms credit appears correctly
Reconciliation	Confirms all records match
Case Study 3: Failed Payment Reversal and Recovery Testing

This case study validates what happens when a payment fails after debit or reservation.

It demonstrates how to test reversal logic, customer balance restoration, failed statuses, duplicate reversal prevention and audit trail accuracy.

Key validation areas include:

Area	Validation
Payment Failure	Confirms failure is processed correctly
Temporary Debit	Confirms deducted amount is tracked
Reversal	Confirms money is restored
Final Balance	Confirms balance returns to expected value
Transaction Status	Confirms status is Failed or Reversed
Duplicate Reversal	Confirms reversal is not processed twice
Audit Trail	Confirms full transaction journey is traceable
Sample Test Calculation Logic
iGaming Balance Calculation
Closing Balance = Opening Balance minus Wager Amount plus Win Amount

Example:

R1 000.00 minus R10.00 plus R50.00 = R1 040.00
Banking Debit Calculation
Closing Balance = Opening Balance minus Debit Amount minus Transaction Fee

Example:

R5 000.00 minus R750.00 minus R5.00 = R4 245.00
EFT Sender Balance Calculation
Sender Closing Balance = Sender Opening Balance minus Payment Amount minus Transaction Fee

Example:

R10 000.00 minus R1 500.00 minus R8.00 = R8 492.00
EFT Recipient Balance Calculation
Recipient Closing Balance = Recipient Opening Balance plus Payment Amount

Example:

R2 500.00 plus R1 500.00 = R4 000.00
Failed Payment Reversal Calculation
Final Balance = Temporary Balance plus Payment Amount plus Transaction Fee

Example:

R4 743.00 plus R1 250.00 plus R7.00 = R6 000.00
Sample SQL Validation
Validate Account Balance
SELECT
    customer_id,
    account_number,
    available_balance,
    ledger_balance,
    currency,
    updated_at
FROM bank_accounts
WHERE account_number = 'ACC1001';
Validate EFT Payment
SELECT
    transaction_reference,
    sender_account,
    recipient_account,
    transaction_type,
    amount,
    fee_amount,
    transaction_status,
    created_at
FROM bank_payment_transactions
WHERE transaction_reference = 'EFT5001';
Validate Reversal Record
SELECT
    transaction_reference,
    transaction_type,
    amount,
    transaction_status,
    balance_after_transaction,
    created_at
FROM bank_transactions
WHERE transaction_reference = 'EFT9001'
ORDER BY created_at ASC;
Sample API Validation
Get Account Balance
GET /api/accounts/ACC1001/balance

Expected response:

{
  "customerId": "CUST1001",
  "accountNumber": "ACC1001",
  "availableBalance": 5445.00,
  "ledgerBalance": 5445.00,
  "currency": "ZAR",
  "status": "ACTIVE"
}
Get Payment Status
GET /api/payments/eft/EFT5001

Expected response:

{
  "transactionReference": "EFT5001",
  "paymentType": "EFT",
  "senderAccount": "ACC1001",
  "recipientAccount": "ACC2001",
  "amount": 1500.00,
  "feeAmount": 8.00,
  "status": "COMPLETED"
}
Defect Reporting Approach

Each defect in this portfolio follows a risk based structure.

Defect Section	Purpose
Defect Title	Clear summary of the issue
Severity	Business and system impact
Priority	Urgency for resolution
Environment	Build, platform and test environment
Module	Affected area
Steps to Reproduce	Clear reproduction path
Expected Result	What should happen
Actual Result	What happened
Evidence	Screenshots, SQL, API response and reconciliation tables
Business Impact	How the issue affects users or the business
Compliance Risk	How the issue affects auditability, traceability or certification
Recommendation	Suggested retest or correction focus
Example Defect Themes
Defect Theme	Example
Balance Mismatch	Customer dashboard does not match database balance
Missing Credit	Sender debited but recipient not credited
Incorrect Status	Failed payment displays as completed
Duplicate Transaction	Payment reference processed more than once
Reversal Failure	Failed payment does not restore customer funds
Paytable Mismatch	New game build differs from certified version
Jurisdiction Rule Failure	Game allows wager above market limit
Skills Demonstrated
Skill	Evidence in Portfolio
Manual Testing	Test cases, scenarios and expected results
Compliance Testing	Jurisdictional and certification style testing
Financial Validation	Balance, payout, debit, credit and fee calculations
SQL Testing	Backend transaction validation queries
API Testing	Payment and balance response validation
Reconciliation	Comparing UI, history, statement, admin, API and database records
Regression Testing	Certified build comparison and change validation
Negative Testing	Failed payments, duplicate requests and invalid wagers
Defect Reporting	Clear defects with risk and evidence
Risk Analysis	Business and compliance impact explained
Documentation	Test summaries, matrices and structured case studies
Tools and Technologies Referenced
Category	Tools and Technologies
Test Management	JIRA style defect tracking
API Testing	Postman, REST API concepts, JSON validation
Database Testing	SQL, PostgreSQL, MySQL
Automation Direction	Selenium WebDriver, Playwright, TestNG, JUnit, Maven
Documentation	Markdown, Word, Excel style test artefacts
Version Control	Git and GitHub
How To Use This Repository

This repository can be reviewed as a QA portfolio.

Recommended review order:

Step	Section
1	Read this README
2	Review iGaming case studies
3	Review Banking case studies
4	Review SQL validation examples
5	Review API testing examples
6	Review defect reports
7	Review test documentation samples
Target Roles

This portfolio supports applications for roles such as:

Role
QA Analyst
Test Analyst
Technical Test Analyst
Compliance QA Analyst
FinTech QA Analyst
Banking QA Tester
iGaming Test Analyst
Manual QA Tester
API Tester
SQL QA Tester
Automation Tester
SDET Trainee or Junior SDET
Professional Positioning

This portfolio positions me as a QA professional with experience and interest in regulated transactional systems.

My testing approach focuses on:

Focus Area	Explanation
Accuracy	Financial values must calculate correctly
Traceability	Every transaction must be traceable by reference, timestamp and status
Consistency	UI, API, database and admin records must match
Compliance Awareness	Testing must consider business, audit and regulatory risk
Evidence	Test results must be supported by screenshots, SQL results and API responses
Risk Based Thinking	High risk transaction defects must be prioritised clearly
Disclaimer

All case studies, test data, SQL queries, API examples, defects and documents in this repository are fictional and created for portfolio purposes.

No real banking system, iGaming system, customer account, employer system, client system, regulatory document or confidential data is included.

The purpose of this repository is to demonstrate transferable QA skills across regulated transaction based environments such as iGaming, Banking and FinTech.

Contact

Name: Khwezilokusa Maphalala
Location: Gauteng, South Africa
Email: khwezilokusa.maphalala@gmail.com
Portfolio Focus: Regulated QA, iGaming Testing, Banking QA, FinTech QA, Transaction Validation, SQL Validation and API Testing
