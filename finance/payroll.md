# Payroll

This document describes how payroll is executed at Elm Lake Cranberry.

## Payroll Provider

**OnPay** is the payroll provider for ELC.

OnPay is responsible for:

- Calculating gross and net pay
- Withholding federal, state, and local taxes
- Processing direct deposits
- Filing payroll tax returns (941, state unemployment, etc.)
- Generating W-2s and other tax documents
- Maintaining employment records and pay history

## Payroll Cadence

Payroll is processed on a **biweekly** schedule. Employees are paid every other week via direct deposit.

Key dates in each pay cycle:

- **Timecard deadline**: Timecards must be submitted before payroll processing begins
- **Payroll processing**: Payroll is reviewed and approved before the scheduled pay date
- **Pay date**: Funds are deposited to employee accounts on the scheduled pay day

Exact dates vary by pay period. The payroll administrator maintains the payroll calendar.

## Roles and Responsibilities

| Role | Responsibilities |
|------|------------------|
| Payroll Administrator | Enter time data, review payroll preview, submit payroll for processing |
| Owner/Manager | Approve payroll before submission, review payroll reports |
| Employees | Submit timecards, verify pay stubs, update personal information |

## System Connections

### OnPay to Banking

OnPay initiates payroll funding from the designated bank account. The bank account must have sufficient funds before payroll processes. OnPay handles the ACH transfers to employee accounts.

### OnPay to QuickBooks Online

Payroll transactions sync automatically from OnPay to QBO. This includes:

- Gross wages by employee or department
- Employer payroll taxes
- Payroll liabilities (taxes withheld, benefits deductions)

No manual journal entries are required for routine payroll. The sync creates the appropriate entries in QBO.

## Payroll Workflow

1. Employees submit timecards by the deadline
2. Payroll administrator enters or imports time data into OnPay
3. Payroll administrator reviews the payroll preview for accuracy
4. Manager approves the payroll
5. Payroll administrator submits payroll for processing
6. OnPay withdraws funds from the bank account
7. OnPay deposits pay to employee accounts on pay day
8. Payroll transactions sync to QBO

## Off-Cycle Payroll

Occasional off-cycle payrolls may be needed for:

- Corrections to previous pay periods
- Final paychecks for departing employees
- Bonuses or other one-time payments

Off-cycle payrolls follow the same approval process but are processed outside the regular schedule.

## Records and Compliance

OnPay maintains payroll records required for compliance, including:

- Pay stubs and earnings history
- Tax filings and payment records
- W-2s and other year-end documents

Employees can access their own records through the OnPay self-service portal.

## Security and Access

- Only authorized personnel have administrative access to OnPay
- Employee self-service access is limited to their own records
- No payroll credentials or employee PII are stored in this repository

## AI Boundaries

AI systems do not interact with payroll systems. Payroll processing, employee record changes, and tax filings are handled exclusively by authorized personnel through OnPay.

AI may assist with:

- Reviewing payroll reports for anomalies
- Analyzing labor cost trends from exported data

AI does not:

- Access OnPay directly
- Process or approve payroll
- Modify employee records
