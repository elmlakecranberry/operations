# System Connections

This document describes how financial systems at Elm Lake Cranberry connect to each other and how data flows between them.

## QuickBooks Online as the Hub

QuickBooks Online (QBO) serves as the central accounting system. Other financial systems either feed data into QBO or are reconciled against it.

```
                    ┌─────────────────┐
                    │   CPA Firm      │
                    │  (Reviews QBO)  │
                    └────────┬────────┘
                             │
                             ▼
┌─────────────┐       ┌─────────────┐       ┌─────────────┐
│   OnPay     │──────▶│     QBO     │◀──────│   Banks     │
│  (Payroll)  │       │   (Hub)     │       │  (Feeds)    │
└─────────────┘       └─────────────┘       └─────────────┘
      │                                            │
      │                                            │
      ▼                                            ▼
┌─────────────┐                            ┌─────────────┐
│  Payroll    │                            │  Operating  │
│  Bank Acct  │                            │  Bank Acct  │
└─────────────┘                            └─────────────┘
```

## Data Flows

### OnPay to QuickBooks Online

**Direction**: OnPay → QBO (automatic sync)

**What syncs**:
- Payroll expense entries (wages, salaries)
- Employer payroll tax expenses
- Payroll liabilities (taxes withheld, deductions)

**Frequency**: After each payroll run

**How it works**: OnPay has a direct integration with QBO. After payroll is processed, journal entries are automatically created in QBO. No manual entry is required for routine payroll.

**Human review**: Bookkeeper verifies payroll entries appear correctly in QBO after each payroll.

### Banks to QuickBooks Online

**Direction**: Banks → QBO (bank feeds)

**What syncs**:
- Cleared transactions (deposits, withdrawals, transfers)
- Transaction details (date, amount, payee/description)

**Frequency**: Daily (automatic refresh)

**How it works**: Bank feeds connect directly to bank accounts and import cleared transactions into QBO. Transactions appear in a queue for matching or categorization.

**Human review**: Bookkeeper reviews imported transactions, matches them to recorded entries, and categorizes unmatched items. This is part of regular reconciliation.

### OnPay to Banks

**Direction**: OnPay → Bank (payment execution)

**What happens**:
- OnPay initiates ACH withdrawal from designated bank account
- OnPay initiates ACH deposits to employee accounts

**Frequency**: Each payroll run

**How it works**: OnPay is authorized to debit the payroll funding account. The bank must have sufficient funds before payroll processes. OnPay handles the ACH network transactions.

**Human review**: Payroll administrator confirms payroll funding amount before submission. Bank transactions appear in QBO via bank feeds.

### CPA Access to QuickBooks Online

**Direction**: QBO → CPA (read access and adjustments)

**What the CPA accesses**:
- Financial reports
- Transaction detail
- Account balances

**What the CPA may do**:
- Review transactions and balances
- Post adjusting journal entries
- Generate reports for tax preparation

**Frequency**: Periodic (year-end, quarterly reviews, as needed)

**How it works**: CPA has an Accountant user role in QBO, which provides access without administrative privileges. CPA logs in directly to review and adjust.

**Human review**: Management reviews and approves adjusting entries proposed by the CPA.

## Integration Points Summary

| Source System | Destination | Data Type | Method | Frequency |
|---------------|-------------|-----------|--------|-----------|
| OnPay | QBO | Payroll entries | Automatic sync | Per payroll |
| OnPay | Bank | Payroll funding | ACH debit | Per payroll |
| OnPay | Employee banks | Pay deposits | ACH credit | Per payroll |
| Bank | QBO | Transactions | Bank feeds | Daily |
| QBO | CPA | Reports/data | Direct access | As needed |

## What Does NOT Auto-Post

The following require manual entry or explicit approval:

- Vendor bills (entered manually from invoices)
- Customer invoices (created manually in QBO)
- Non-payroll journal entries
- Adjusting entries
- Transfers between accounts (initiated manually)

No system auto-posts transactions to QBO without human initiation, except for:
- Bank feed imports (which require human matching/approval)
- Payroll sync from OnPay (which requires prior payroll approval)

## Error Handling

When sync issues occur:

| Issue | Resolution |
|-------|------------|
| Bank feed disconnection | Bookkeeper reconnects feed; may require re-authentication |
| OnPay sync failure | Check OnPay-QBO connection; contact OnPay support if needed |
| Duplicate transactions | Bookkeeper identifies and deletes duplicates in QBO |
| Missing transactions | Bookkeeper manually enters or investigates source |

Sync errors are typically visible in QBO or OnPay dashboards. Regular reconciliation catches discrepancies.

## Security Principles

- Each system connection uses its own authentication
- No credentials are shared between systems
- Access to each system is limited to authorized personnel
- This repository does not store credentials, tokens, or connection details

## AI Boundaries

AI systems do not have direct access to any of these systems or their integrations.

AI may assist with:

- Analyzing exported transaction data
- Identifying patterns or anomalies in financial reports
- Documenting system relationships (like this document)

AI does not:

- Access QBO, OnPay, or banking systems
- Initiate or approve data syncs
- Modify integration settings
- Execute any financial transactions
