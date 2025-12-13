# Payroll & HR: OnPay

OnPay is the payroll and HR system for Elm Lake Cranberry.

## What OnPay Is Authoritative For

OnPay is the source of truth for:

- **Payroll processing** – Pay calculations, deductions, direct deposits
- **Employment records** – Hire dates, job titles, pay rates, employment status
- **Tax withholdings** – Federal, state, and local tax records
- **Pay history** – Past pay stubs, earnings records
- **Tax documents** – W-2s, 1099s, and other tax forms
- **Benefits enrollment** – Health insurance, retirement contributions (if applicable)

If you need to know what someone was paid, when they started, or their current employment status, OnPay is where you look.

## What OnPay Is NOT Authoritative For

OnPay does not define:

- **Compensation policies** – Pay structures and raise guidelines are management decisions
- **Performance management** – Reviews, evaluations, and development plans
- **Hiring and termination decisions** – Those are management authority
- **Personnel policies** – Time off policies, conduct expectations, etc.
- **Org structure or reporting lines** – Authority and roles are defined in management

OnPay executes payroll. Management makes personnel decisions.

## Who Uses OnPay

| Role | Access Level | Typical Tasks |
|------|--------------|---------------|
| Payroll administrator | Full access | Run payroll, manage employee records |
| Owner/Manager | Admin access | Review payroll, approve changes |
| Employees | Self-service | View pay stubs, update personal info, access tax documents |

## Operational Cadence

- **Pay frequency**: [Biweekly / Weekly / As configured]
- **Timecard deadline**: Timecards must be submitted by [day/time] before pay day
- **Payroll processing**: Payroll is processed [X days] before pay day
- **Direct deposit timing**: Funds are deposited on pay day morning

## Common Tasks

### For Employees

- View current and past pay stubs
- Update direct deposit information
- Update address or contact information
- Download W-2s and tax documents

### For Administrators

- Add new employees
- Process regular payroll
- Handle payroll corrections
- Run payroll reports
- Process year-end tax filings

## Integration with Other Systems

- **QuickBooks Online**: Payroll transactions sync automatically to the general ledger
- Payroll expense entries appear in QuickBooks without manual entry

## Getting Help

- **System issues**: Contact OnPay support
- **Process questions**: Contact the payroll administrator
- **Policy questions**: Refer to the management repo or ask a manager
- **Personal payroll questions**: Employees should contact the payroll administrator
