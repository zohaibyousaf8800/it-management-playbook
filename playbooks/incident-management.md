# Incident Management Playbook

| | |
|---|---|
| Document owner | [IT Manager] |
| Applies to | All IT services operated or supported by [Company] IT |
| Review cycle | Quarterly, and after every P1 incident |
| Related documents | [Incident Report Template](../templates/incident-report-template.md), [SLA Targets](../templates/sla-targets.csv) |

## Purpose

To restore normal service as quickly as possible when something breaks, with clear priorities, honest communication, and a record that lets the organisation learn from each significant incident.

## Scope

- Incidents: unplanned interruptions or degradations of IT service (outages, failures, security events handled jointly with the security process).
- Service requests (standard, pre-approved work such as password resets or software installs) are handled by the service desk process, not this playbook — although both are logged in the same ITSM tool.

## Priority matrix

Priority is set from **impact** (how much of the business is affected) and **urgency** (how time-critical the work is).

| Priority | Definition | Examples | Response target | Resolution target |
|---|---|---|---|---|
| **P1 — Critical** | Business-critical service down, or a whole site/department unable to work | Microsoft 365 tenant-wide outage, core network down, ransomware suspected | 15 minutes | 4 hours |
| **P2 — High** | A key service degraded, or a team/department significantly affected | Email delays for one site, VPN failures for remote staff, line-of-business app errors for a team | 30 minutes | 8 business hours |
| **P3 — Medium** | Single user or small group affected; a workaround exists | One user's laptop fault with a loan device available, printer failure with an alternative device | 4 business hours | 3 business days |
| **P4 — Low** | Minor issue or cosmetic problem; no work blocked | Monitor flicker, non-urgent software fault, peripheral replacement | 1 business day | 5 business days |

Targets are also published in machine-readable form in [sla-targets.csv](../templates/sla-targets.csv). Clocks run on business hours except P1, which runs around the clock.

## Process steps

1. **Log.** Every incident is logged in the ITSM tool with reporter, service, impact, urgency, and time detected. No ticket, no work — verbal reports are logged by the person who receives them.
2. **Triage and assign.** The service desk validates priority against the matrix and assigns an owner. The person who owns the ticket owns the communication.
3. **Respond.** Acknowledge to the reporter within the response target. For P1/P2, post an initial status to the agreed comms channel (for example, the company-wide Teams channel) within 30 minutes.
4. **Diagnose and fix.** Work the problem; record actions and findings in the ticket as you go, not at the end. Apply fixes under [Change Management](change-management.md) rules — emergency changes follow the expedited path there.
5. **Communicate.** P1: updates at least hourly. P2: updates at least every 4 business hours. P3/P4: update on status change and at resolution.
6. **Resolve and confirm.** Confirm with the reporter that service is restored before closing. Record root cause (or "unknown — monitoring"), resolution, and total elapsed time.
7. **Close.** Categorise accurately (hardware, software, network, security, user request). Wrong categories destroy the reporting this process depends on.

## Escalation path

| Level | Who | When |
|---|---|---|
| 1st line | Service desk | First response, known fixes, triage |
| 2nd line | Infrastructure / systems engineers | Not resolvable at 1st line within 30 minutes (P1/P2) |
| 3rd line | Vendor support or specialist partner | Product defect suspected, or 2nd line exhausted |
| Management | [IT Manager], then [Head of Operations / CTO] | P1 immediately; any incident forecast to breach its resolution target |

Escalation is about getting the right help faster, not about blame. Escalate early.

## Major incidents (P1)

1. [IT Manager] (or deputy) acts as incident lead: coordinates the fix, owns communications, keeps the timeline.
2. Open a dedicated incident channel; log key events and decisions with timestamps.
3. Notify leadership within 30 minutes with: what is affected, business impact, what is being done, next update time.
4. Stand down formally when service is restored; announce it on the same channel used for updates.

## Post-incident review (PIR)

Held within **5 business days** of every P1, and of any P2 that breached its target or recurred. Use the [Incident Report Template](../templates/incident-report-template.md).

The PIR covers: timeline, root cause, detection and response quality, what went well, what did not, and agreed actions with owners and dates. PIRs are blameless — they examine systems and processes, not individuals. Actions are tracked in the ITSM tool until closed and reviewed monthly by [IT Manager].

## Owner

[IT Manager] owns this playbook and the SLA reporting. The service desk lead owns day-to-day triage quality.

## KPIs and review

| KPI | Target |
|---|---|
| First response within target (all priorities) | 95% or higher |
| Resolution within target | 90% or higher |
| P1 incidents with PIR completed in 5 business days | 100% |
| Repeat incidents (same root cause within 90 days) | Decreasing quarter on quarter |
| Tickets logged with correct category | 95% or higher |

Review monthly in the IT operations report; review this playbook quarterly and after every P1.
