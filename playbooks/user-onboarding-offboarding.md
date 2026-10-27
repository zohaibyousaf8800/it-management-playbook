# User Onboarding and Offboarding Playbook

| | |
|---|---|
| Document owner | [IT Manager] |
| Applies to | All joiners, movers and leavers at [Company] |
| Review cycle | Quarterly |
| Related documents | [Asset Sign-off Form](../templates/asset-signoff-form.md), [New Starter IT Checklist](../templates/new-starter-it-checklist.csv) |

## Purpose

To make sure every new starter has working accounts, a compliant device and the right access on day one — and that every leaver's access is removed completely, on time, with company data handled according to policy.

## Scope

- Permanent staff, contractors and interns.
- Microsoft 365 accounts, Intune-managed devices, and business applications administered by IT.
- Physical access (building passes, keys) is owned by [Facilities/HR]; IT coordinates dates with them but does not issue passes.

## Onboarding steps

Target: request received at least **5 working days** before the start date. Late requests are handled best-effort and flagged to the hiring manager.

1. **Trigger.** HR raises a new-starter request containing: full name, job title, department, manager, start date, work location, and required applications.
2. **Create the Microsoft 365 account.**
   - Create the user in Microsoft 365 (or sync from on-premises AD where hybrid identity is in use).
   - Apply the standard naming convention and set department, title, manager and location attributes — these drive dynamic group membership and reporting.
   - Assign licences according to the role profile (for example, Microsoft 365 Business Premium for standard users). Record assignments for the monthly licence review.
3. **Access provisioning.**
   - Add the user to the department and application security groups defined in the access matrix. Never grant access by copying another user's permissions without manager approval.
   - Shared mailbox and distribution group membership confirmed with the line manager.
4. **Device preparation and Intune enrolment.**
   - Allocate a device from stock, record it in the asset register, and complete an [Asset Sign-off Form](../templates/asset-signoff-form.md) at handover.
   - Enrol the device in Intune (Windows Autopilot where available, otherwise manual enrolment) and confirm the device reports as **compliant**: encryption on, OS in support, endpoint protection active.
   - Apply the standard configuration profile set: Wi-Fi/VPN, email, OneDrive Known Folder Move, and printer mapping.
5. **MFA and sign-in security.**
   - Register the user for multi-factor authentication (Microsoft Authenticator preferred) during the first sign-in session — do not leave a grace period unmonitored.
   - Confirm the account is covered by the organisation's Conditional Access policies.
6. **Day-one support.**
   - IT contact attends (in person or by call) for the first sign-in, password set and MFA registration.
   - Issue the IT welcome note: how to raise a ticket, support hours, and security basics (phishing reporting, password rules).
7. **Confirm completion.** Close the request only when: account active, licence assigned, device compliant in Intune, MFA registered, and sign-off form filed.

## Movers (role changes)

1. Manager raises a change-of-role request listing new department, title and required access.
2. Remove groups and application access belonging to the old role **before** adding new access.
3. Update directory attributes so dynamic groups, licences and reports stay accurate.
4. Confirm with the manager that the resulting access matches the new role.

## Offboarding steps

Target: access disabled at the agreed date and time confirmed by HR — for involuntary leavers, immediately on HR instruction.

1. **Trigger.** HR raises a leaver request with last working day and any legal-hold or data-retention instructions.
2. **Disable access.**
   - Block sign-in and revoke refresh tokens in Microsoft 365 (Entra ID).
   - Reset the password and remove the account from all security and distribution groups.
   - Remove MFA methods and disable the account; do not delete it yet (see step 4).
3. **Data handling.**
   - Convert the mailbox to a shared mailbox and grant the manager (or a named delegate) access for the retention period defined in policy (default 30 days), unless a legal hold applies.
   - Transfer OneDrive content ownership to the manager; record what was transferred and when.
   - Export or archive data only where HR or Legal have requested it in writing.
4. **Licence and account lifecycle.**
   - Reclaim the Microsoft 365 licence on the disable date and return it to the pool.
   - Keep the disabled account for the retention period (default 90 days), then delete it and note the deletion date in the leaver record.
5. **Devices and assets.**
   - Recover all devices and accessories; check them against the asset register and the leaver's sign-off forms.
   - Wipe recovered devices via Intune before reissue or disposal.
6. **Access review confirmation.** Add the leaver to the next access review list so a second person confirms no residual access (VPN, SaaS admin roles, shared accounts).

## Access reviews

- **Monthly:** review privileged accounts (Global Administrator and other admin roles) — confirm each is still required.
- **Quarterly:** department managers re-certify their team's application access using the access matrix; IT removes anything not re-certified within 10 working days.

## Owner

[IT Manager] owns this playbook. The service desk performs provisioning steps; HR owns the accuracy and timing of joiner/leaver notifications.

## KPIs and review

| KPI | Target |
|---|---|
| Starters fully provisioned by day one | 98% or higher |
| Leaver accounts disabled at agreed time | 100% |
| Devices compliant in Intune at handover | 100% |
| Orphaned accounts found in quarterly review | 0 |

Review this playbook quarterly alongside the access-review results. Record exceptions (for example, late HR notifications) and agree corrective actions with HR.
