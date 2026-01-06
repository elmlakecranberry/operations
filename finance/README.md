# Financial Execution

This folder documents how financial operations are executed at Elm Lake Cranberry. It covers the tools, workflows, and roles involved in day-to-day financial activity.

## Governance

Financial authority, approval thresholds, and decision rights are defined in **elc-management**, not here. This folder documents implementation only. If there is a conflict between this documentation and management policy, management governs.

## Systems Overview

Financial execution at ELC relies on the following systems:

| System | Purpose |
|--------|---------|
| QuickBooks Online (QBO) | Accounting system of record |
| OnPay | Payroll processing and tax filings |
| Commercial bank accounts | Cash management and payments |
| CPA firm | Tax preparation and accounting oversight |

QBO serves as the central hub. Other systems either feed data into QBO or pull reports from it.

## What This Folder Contains

- [Payroll](payroll.md) — How payroll is processed and funded
- [Banking](banking.md) — Bank account structure and payment flows
- [AP/AR](ap-ar.md) — Accounts payable and receivable processes
- [Tax Coordination](tax-coordination.md) — Working with the CPA firm
- [System Connections](system-connections.md) — How financial systems integrate

## What This Folder Does NOT Contain

- Budgets or financial targets
- Spending policies or approval authority
- Strategic financial decisions
- Account numbers, credentials, or sensitive data

Those belong to management or are stored securely outside this repository.

## Roles

The following roles interact with financial systems:

| Role | Responsibilities |
|------|------------------|
| Owner/Manager | Approves transactions, reviews reports, makes financial decisions |
| Bookkeeper | Day-to-day transaction entry, reconciliation, report generation |
| Payroll Administrator | Processes payroll, manages employee records in OnPay |
| CPA (external) | Year-end review, tax preparation, accounting guidance |

Most employees do not need direct access to financial systems. Requests for financial information should go through the bookkeeper or manager.

## AI Boundaries

AI systems may assist with:

- Reviewing transactions for anomalies
- Analyzing financial data and reports
- Drafting reports or summaries for human review

AI systems do not:

- Execute payments or transfers
- Access banking systems directly
- Process payroll
- Prepare or file taxes
- Make financial decisions

All financial execution is human-initiated and human-approved.
