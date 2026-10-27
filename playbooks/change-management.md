# Change Management Playbook

| | |
|---|---|
| Document owner | [IT Manager] |
| Applies to | All production IT systems and services at [Company] |
| Review cycle | Quarterly |
| Related documents | [Change Request Template](../templates/change-request-template.md), [Incident Management](incident-management.md) |

## Purpose

To make changes to production systems in a controlled way: planned, risk-assessed, approved at the right level, communicated to the people affected, and reversible if something goes wrong. Most serious incidents in a small IT operation are caused by changes, not by random failures — this process exists to keep it that way.

## Scope

- In scope: infrastructure, network, Microsoft 365 tenant settings, Intune policies, security configuration, line-of-business applications, and vendor-delivered changes to those systems.
- Out of scope: standard, pre-approved changes (see below) and pure content edits (for example, updating a SharePoint page).

## Change types

| Type | Description | Approval | Lead time |
|---|---|---|---|
| **Standard** | Pre-approved, low-risk, repeatable work done from an agreed procedure | Pre-approved by [IT Manager]; logged after completion | None — do and log |
| **Normal — minor** | Low risk, limited scope, single system, easy rollback | [IT Manager] | 3 business days |
| **Normal — major** | Higher risk, cross-system, affects many users, or hard to reverse | CAB | 10 business days |
| **Emergency** | Required to resolve or prevent a P1/P2 incident | [IT Manager] or deputy, verbally first, paperwork within 1 business day | None — expedited |

Examples of standard changes: password policy-compliant resets of service accounts, adding a user to an approved application group, routine certificate renewals done from the runbook, Intune app deployments already tested in the pilot ring.

## CAB (Change Advisory Board)

- **Membership:** [IT Manager] (chair), service desk lead, infrastructure engineer, and a business representative from the most affected department. Finance/HR system owners join when their systems are on the agenda.
- **Cadence:** weekly, 30 minutes. Major changes are not approved outside the meeting except by the emergency path.
- **Inputs:** change requests submitted on the [Change Request Template](../templates/change-request-template.md) by the lead-time deadline.
- **Outputs:** approve, approve with conditions, defer for more information, or reject — recorded on the change record with reasons.

## Approval flow

1. **Raise.** Requester completes the change request: what, why, risk, impact, test evidence, implementation plan, rollback plan, proposed window.
2. **Assess.** [IT Manager] classifies the change (standard / minor / major / emergency) and checks the assessment is honest — especially affected users and rollback.
3. **Approve.** Per the table above. Approver must not be the implementer for major changes.
4. **Schedule.** Agree a window that minimises business impact. Default maintenance window: [e.g. Tuesday 18:00-20:00]. No major changes during business-critical periods defined by [Company] (for example, month-end close, enrolment or sales peaks).
5. **Communicate.** Notify affected users and the service desk before the window: what is changing, when, expected impact, and what to do if something looks wrong afterwards.
6. **Implement.** Follow the documented plan step by step. Record actual start/end times and any deviation in the change record. If a step fails, stop and invoke the rollback plan rather than improvising.
7. **Verify.** Run the post-change checks in the plan (service health, logon test, key user confirmation). Only then mark the change successful.
8. **Close and review.** Close the change with outcome (successful / successful with issues / rolled back / failed). Major and failed changes are reviewed at the next CAB.

## Rollback planning

Every normal change must have a written rollback plan before approval. A rollback plan states:

- The trigger points for abandoning the change (failed check, time limit, user impact).
- The exact steps to return to the previous state, and who performs them.
- How long rollback takes — implementation must not start unless implementation **plus** rollback fits inside the window.
- What data, if any, cannot be recovered by rollback, and how that risk is mitigated (backups, exports, snapshots taken before starting).

"Reinstall from scratch" is not a rollback plan.

## Rules that are not negotiable

- No unlogged changes to production. If it is not in the ITSM tool, it did not get approved.
- No self-approval of major changes.
- Backups or snapshots verified before any change to data or identity systems.
- Failed changes raise an incident and are linked to it; the pair is reviewed together.

## Owner

[IT Manager] owns this playbook and chairs the CAB.

## KPIs and review

| KPI | Target |
|---|---|
| Changes with a documented rollback plan | 100% of normal changes |
| Change success rate (no incident, no rollback) | 95% or higher |
| Emergency changes as a share of all changes | Below 10% (a rising trend means planning is failing) |
| Changes causing a P1/P2 incident | 0 |
| Unlogged changes discovered | 0 |

Review monthly at CAB using the change log; review this playbook quarterly.
