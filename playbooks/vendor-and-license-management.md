# Vendor and License Management Playbook

| | |
|---|---|
| Document owner | [IT Manager] |
| Applies to | All IT suppliers, subscriptions and software licences at [Company] |
| Review cycle | Quarterly |
| Related documents | [IT Budget and Reporting](it-budget-and-reporting.md) |

## Purpose

To stop two common ways organisations waste money and create risk: renewals that arrive as a surprise, and licence counts that drift away from what is actually used. Every contract has an owner, every renewal has a decision date, and every licence position can be explained.

## Scope

- Software subscriptions and licences (Microsoft 365, security tooling, line-of-business SaaS).
- Support and maintenance contracts (hardware support, ISP/connectivity, managed services).
- Professional services agreements run by IT.

Procurement rules (tendering thresholds, purchase orders) are owned by [Finance]; this playbook covers the IT-side management of the relationship and the licence position.

## Contract and renewal register

Maintain one register (the ITSM tool, or a controlled spreadsheet) with, for every contract:

- Supplier, product/service, and business owner in [Company].
- Contract start and end dates, renewal type (auto-renew or fixed term), and notice period.
- Annual cost, billing cycle, and cost centre.
- Licence metric and quantity purchased (seats, cores, devices).
- Decision date: **notice period plus 30 days before expiry** — the date by which renew, renegotiate or exit must be decided.

The register is reviewed monthly. Anything reaching its decision date without an owner decision escalates to [IT Manager].

## Renewal process

1. **T-90 days (or decision date, whichever is earlier):** contract owner reviews usage and need. For licences, pull the usage data first (see true-ups below) — never renew on last year's numbers.
2. **T-60:** agree the negotiating position: required quantities, term options (monthly vs annual pricing), and alternatives. Get competing quotes where the market allows it.
3. **T-30:** decision approved by [IT Manager] and [Finance] per spending limits; purchase order raised.
4. **Expiry:** confirm renewal paperwork completed and the new term dates entered in the register before the old term lapses. A lapsed support contract on a production system is treated as a P3 incident.

Auto-renewing contracts are reviewed with the same rigour — auto-renewal is a billing convenience, not a decision.

## Licence management and true-ups

1. **Monthly:** reconcile the Microsoft 365 licence position — licences purchased vs assigned vs actually used (sign-in and usage reports). Unassigned licences and licences held by disabled/leaver accounts are returned to the pool or removed at the next billing opportunity.
2. **Quarterly:** true-up of the wider estate — compare deployed installations and SaaS user lists against purchased quantities for each product. Record the position (compliant / over-licensed / under-licensed) per product.
3. **Under-licensing** is corrected at the next purchase cycle and reported to [Finance] the quarter it is found. Never install or assign beyond purchased quantities as a "temporary" fix.
4. **Over-licensing** above 10% of a product's spend triggers a reduction plan at renewal (fewer seats, lower tier, or consolidation).
5. Harvest before you buy: no new licence purchase is approved until the pool of unassigned licences has been checked.

## Vendor review cadence

| Vendor tier | Definition | Review |
|---|---|---|
| Strategic | Business-critical or top-5 annual spend | Quarterly service review: SLA performance, incidents, roadmap, actions |
| Operational | Regular service (connectivity, support contracts) | Six-monthly review: performance against contract terms |
| Transactional | Ad-hoc purchases, low spend | Annual check: still needed, pricing still sane |

Every review is minuted with actions and owners. Repeated SLA failure (two consecutive review periods) triggers a formal improvement plan with the vendor and, where exit is realistic, a market test.

## Vendor onboarding and exit

- **Onboarding:** security review proportionate to the data the vendor will touch (for Microsoft 365-connected apps: permissions requested, data location, sub-processors, SSO/MFA support). Record the outcome; no production data before the review is signed off by [IT Manager].
- **Exit:** on termination, revoke the vendor's accounts and API access, export [Company] data in a usable format before the contract ends, and obtain written confirmation of data deletion where required.

## Owner

[IT Manager] owns this playbook and the renewal register. [Finance] owns purchase orders and payment.

## KPIs and review

| KPI | Target |
|---|---|
| Contracts with an owner and a decision date in the register | 100% |
| Renewals decided by their decision date | 100% |
| Microsoft 365 licences unassigned for over 30 days | Below 5% of total |
| Products over-licensed by more than 10% | 0 without an agreed reduction plan |
| Strategic vendor reviews held on schedule | 100% |

Review this playbook quarterly alongside the budget review.
