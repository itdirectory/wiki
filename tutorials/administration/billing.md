# Viewing plan & billing status

**Who can do this:** Org Admin only.

This page is read-only — there's no self-serve way to change your plan in-app.

## Steps

1. In the left sidebar, click **Settings**, then click **Billing** in the settings menu on the left (`/settings/billing`, subtitled "Plan, trial, and capacity").
2. Check the status badge at the top: **Trial** or **Paid**.
3. If you're on a trial, a box shows "Trial ends on {date}".
4. Review the two usage bars:
   - **Assets** — used vs. limit, pooled across your organization and all its sub-orgs. Hardware, employees, software & services, domains, VLANs and public IPs all count; hidden Microsoft 365 licenses don't (see [Adding a software license, SaaS subscription, or service](../inventory/adding-software-services.md)).
   - **Sub-Organizations** — used vs. limit.
   Both bars turn amber at 80% of the limit and red at 100%.
5. To upgrade or increase a limit, click **Contact us to upgrade** — this opens an email to sales with a pre-filled subject.

## Notes

- If you hit your asset or sub-org limit, creation actions elsewhere in the app (adding hardware, employees, software, domains, VLANs or public IPs, or creating a sub-org) fail with "You've reached your asset limit — contact us to upgrade." (or the sub-organization equivalent) until you upgrade.
- When a trial ends without upgrading, or access is paused by the vendor, every user in your organization (and its sub-orgs) is sent to **Your trial has ended** after signing in, with **Contact us to upgrade** and **Sign out** — nothing else in the app is reachable. Your data is kept; access returns once the plan is changed.
- Plan changes, entitlements, and trial extensions are handled outside the app by the vendor — there is no self-checkout flow.
