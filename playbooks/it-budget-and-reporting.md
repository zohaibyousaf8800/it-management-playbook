# IT Budget and Reporting Playbook

| | |
|---|---|
| Document owner | [IT Manager] |
| Applies to | IT operational and project spend at [Company] |
| Review cycle | Annual (budget build); monthly (reporting) |
| Related documents | [Vendor and License Management](vendor-and-license-management.md), [Monthly IT Report Template](../templates/monthly-it-report-template.md) |

## Purpose

To give [Company] a predictable IT budget that finance can plan around, and a short, honest monthly report that shows what the business got for the money: service performance, risk, and what is coming next.

## Scope

- All IT operating expenditure (subscriptions, support, connectivity, consumables) and IT project expenditure (hardware refresh, migrations, new systems).
- Staff costs are included if IT salaries sit in the IT cost centre in your organisation; the structure below works either way — mark the category clearly.

## Annual budget categories

Build the budget from the contract register and the asset lifecycle, not from last year's total. Each line states its basis (quantity x unit cost, contract value, or lifecycle plan).

| Category | Contents | Basis |
|---|---|---|
| People | IT salaries, on-call payments, training and certifications, recruitment | Headcount plan agreed with [HR/Finance] |
| Software and subscriptions | Microsoft 365 licences, security tooling, ITSM, SaaS applications | Licence position from the quarterly true-up, priced at renewal rates |
| Hardware lifecycle | End-user devices (laptops/desktops on a [4-year] cycle), servers, network refresh, peripherals | Asset register age profile — devices due for replacement this year, named |
| Infrastructure and connectivity | Internet lines, WAN/VPN, telephony, cloud consumption (Azure) | Contract values plus 12-month consumption trend for metered services |
| Support and services | Hardware support contracts, managed services, project contractors | Contract register |
| Security and compliance | Endpoint protection, backup, security assessments, cyber insurance contribution where applicable | Contract values and planned assessments |
| Projects | Planned initiatives (for example, device refresh programme, network upgrade, system migration) | One line per project with the approved business case figure |
| Contingency | Unplanned replacements and price movement | 5-10% of operating subtotal, drawn only with [IT Manager] approval |

Rules:

- Cloud consumption is budgeted from trend with a stated growth assumption, and reviewed monthly — metered spend is never "set and forget".
- Every subscription line names the contract owner and renewal date, cross-checked against the [renewal register](vendor-and-license-management.md).
- Hardware lines are driven by the asset register, so the refresh conversation is about named, ageing devices — not a lump sum.

## Budget timetable

| When | What |
|---|---|
| T-3 months before financial year | Draft built from contract register, licence true-up and asset lifecycle |
| T-2 months | Review with [Finance]: challenge quantities, licence tiers and project priorities |
| T-1 month | Final approval; projects sequenced by quarter |
| Monthly | Actuals vs budget by category, forecast to year end, variances explained |
| Mid-year | Formal reforecast: move budget between categories only with [Finance] agreement |

## Monthly IT report

Produced within the first **5 business days** of the month, using the [Monthly IT Report Template](../templates/monthly-it-report-template.md). Keep it to two pages plus data appendices. It contains:

1. **Service performance:** ticket volumes, first-response and resolution against [SLA targets](incident-management.md), P1/P2 incidents with one-line summaries.
2. **Endpoint and patch compliance:** Intune device compliance %, patch compliance by ring, devices out of compliance with owners.
3. **Security posture:** open critical/high vulnerabilities against target, Secure Score trend, any security incidents.
4. **Joiners, movers, leavers:** numbers processed, any late notifications and their impact.
5. **Licence position:** purchased vs assigned vs used for the top subscriptions by cost; licences reclaimed.
6. **Spend:** actuals vs budget by category, forecast to year end, and any variance over 5% explained in one or two sentences.
7. **Renewals and decisions due:** contracts hitting their decision date in the next 90 days, with the recommendation.
8. **Projects:** milestone status (on track / at risk / delayed) and spend against plan.
9. **Risks and asks:** anything leadership needs to decide or be aware of, stated plainly.

## Variance discipline

- Any category forecast to vary by more than 5% or by an agreed cash threshold is explained in the month it is first forecast — not when the invoice arrives.
- Underspend caused by delayed projects is reported as timing, not savings, unless the project is cancelled.

## Owner

[IT Manager] owns this playbook, the budget build and the monthly report. [Finance] owns the chart of accounts and final approval.

## KPIs and review

| KPI | Target |
|---|---|
| Monthly report issued within 5 business days | 100% |
| Year-end operating variance | Within plus or minus 5% |
| Budget lines with a stated basis (quantity, contract or lifecycle) | 100% |
| Renewals flagged at least 90 days ahead in the report | 100% |

Review this playbook annually during the budget build, and after any significant change to the organisation's structure or cost centres.
