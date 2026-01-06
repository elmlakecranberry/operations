# Banking

This document describes the banking structure and payment flows at Elm Lake Cranberry.

## Account Structure

ELC maintains commercial bank accounts for different operational purposes. Typical account types include:

| Account Type | Purpose |
|--------------|---------|
| Operating Account | Primary account for revenue deposits and expense payments |
| Payroll Account | Dedicated account for payroll funding (if separate) |
| Savings/Reserve | Funds held for taxes, capital, or contingencies |

The specific account structure may vary based on business needs. Management determines which accounts are maintained and how funds are allocated between them.

## Bank Connections

### Banking to QuickBooks Online

Bank transactions are imported into QBO through bank feeds. This allows:

- Automatic import of cleared transactions
- Matching imported transactions to recorded entries
- Bank reconciliation against QBO records

Bank feeds require initial setup and periodic reauthorization. The bookkeeper manages bank feed connections.

### Banking to OnPay

OnPay connects to the designated bank account to:

- Withdraw funds for payroll processing
- Initiate ACH deposits to employee accounts

The bank account used for payroll must be configured in OnPay and must have sufficient funds before each payroll run.

### Banking to AP/AR

- **Accounts Payable**: Payments to vendors are made via check, ACH, or wire from the operating account
- **Accounts Receivable**: Customer payments are deposited to the operating account

## Payment Methods

| Method | Typical Use |
|--------|-------------|
| ACH Transfer | Payroll, recurring vendor payments |
| Check | Vendor payments, one-time payments |
| Wire Transfer | Large or time-sensitive payments |
| Credit Card | Smaller purchases, supplies (if applicable) |

Payment method selection depends on vendor requirements, amount, and urgency.

## Approval Authority

Payment approvals are governed by management policy. General guidelines:

| Payment Type | Approval Required |
|--------------|-------------------|
| Routine operating expenses | Per established approval thresholds |
| Large or unusual payments | Manager or owner approval |
| Payroll | Payroll administrator processes; manager approves |
| New vendor setup | Verification required before first payment |

Specific approval thresholds and signing authority are defined in management documentation, not here.

## Reconciliation

Bank accounts are reconciled regularly to ensure:

- All transactions are recorded in QBO
- No unauthorized transactions have occurred
- Cash balances are accurate

The bookkeeper performs reconciliation. Discrepancies are investigated and resolved promptly.

## Security

Banking access is restricted to authorized personnel only.

**This repository does not store:**

- Account numbers
- Routing numbers
- Online banking credentials
- Security questions or PINs
- Authorized signer information

Banking credentials and sensitive account details are maintained securely outside this repository.

## Fraud Prevention

Standard fraud prevention practices include:

- Positive pay or similar check verification services (if available)
- Dual approval for large transactions
- Regular review of account activity
- Prompt investigation of unusual transactions

Suspected fraud is reported to management and the bank immediately.

## AI Boundaries

AI systems do not have access to banking systems or credentials.

AI may assist with:

- Reviewing bank statements or transaction exports for anomalies
- Analyzing cash flow patterns from exported data

AI does not:

- Access online banking
- Initiate or approve payments
- View account numbers or credentials
