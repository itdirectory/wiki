# Adding a software license, SaaS subscription, or service

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Software & services** (`/software-assets`).
2. Click **Add Asset** (top right, next to **Import**). You can also use **Add asset → Software or service** in the top bar from any page. The form opens in a pane on the right, titled **Add software or service**.
3. At the top of the form, pick the type by clicking a tile:
   - **License** — keyed software (e.g. JetBrains, Windows).
   - **SaaS** — a subscription with seats (e.g. Slack, ChatGPT).
   - **Service** — a membership or recurring service with no seats (e.g. Apple Developer).

   If you opened the form from the Licenses, SaaS or Services tab, that type is preselected.
4. Fill in the form, organized into sections:

   **Basic info**
   - **Sub-Organization** — required, shown only if your account has access to more than one org.
   - **Name** — required.

   **Vendor & ownership**
   - **Vendor** — optional.
   - **Owner** (responsible person) — optional, searchable employee picker. This is who's *managerially responsible*, not necessarily a seat holder.

   **License details** (only for License)
   - **License Key** — optional. When editing, leave it blank to keep the current key.
   - **License Type** — optional: Perpetual, Subscription, Per Seat, Volume.
   - **Version** — optional.

   **Subscription details** (only for SaaS)
   - **Plan / Tier**, **Website URL**, **Billing Cycle** (Monthly / Quarterly / Annual) — all optional.

   *(Service has no extra section.)*

   **Billing & dates**
   - **Total Seats** — optional, not shown for Service.
   - **Cost** — labeled **Cost per Cycle** for SaaS. Pick the currency next to the amount: **ILS (₪)**, **USD ($)** (default) or **EUR (€)**.
   - **Purchase Date** — optional.
   - **Expiry Date** (License) / **Renewal Date** (SaaS and Service) — optional.

   **Notes**
   - Optional free text.

5. Click **Add Asset** to save (you'll see "Asset added"). The **Add Asset** / **Cancel** buttons stay pinned at the bottom of the pane while you scroll.

## Viewing and editing

- Click a row to open its details in the right-hand pane. A details pane closes on a click outside it, the ×, or Esc; an add/edit form closes only with **Cancel**, the ×, or Esc, so a stray click doesn't lose what you typed.
- From the details pane, click **Edit** (or the pencil icon on the row). The pane switches to **Edit License** / **Edit SaaS** / **Edit Service**; click **Save Changes**. Saving or cancelling an edit started from the details pane returns you to the details.
- **Delete** is in the details pane footer and as a trash icon on the row. It asks for confirmation; seat assignments are removed too.
- License keys are masked in the list and details; click the eye icon to reveal one, then the copy icon to copy it.

## Assigning seats

1. Licenses and SaaS items support **seat assignments** — which employees hold a seat. Service items don't.
2. Click the people icon (**Manage seats**) on the row. The dialog **{name} — Seat Assignments** shows "{x} of {y} seats used" and the current holders.
3. Search for an employee ("Search employees to assign…") and click **Assign**. Click × next to a holder to remove their seat.
4. When every seat is taken you'll see "No seats remaining — remove an existing assignment first."

## Finding software & services

- Use the kind tabs (**All** / **Licenses** / **SaaS** / **Services**) and the search bar ("Search by name, vendor, plan…"). The table paginates at 25 rows per page.
- Filter dropdowns next to the search bar can be combined:
  - **Renewal** — **Expired / overdue**, **Due in 30d**, or **Not due in 30d**.
  - **Seats** — **≥ 80% used**.
  - **Vendor** — any vendor in your list.
  - **License type** — shown on the All and Licenses tabs only.
  - **Billing** — billing cycle, shown on the All and SaaS tabs only.
  - **Owner** — **Has owner** / **No owner**.
- Click **Clear filters** to reset them. Switching tabs drops a License type or Billing filter the new tab doesn't show.

## Microsoft 365 licenses

If your organization uses the **Microsoft 365 licenses** integration (see [Setting up connectors](../administration/connectors.md)), each subscribed license appears here as a SaaS item with a **Microsoft 365** badge.

- **Managed in Azure:** the type, name, vendor, total seats, sub-organization and seat holders follow Microsoft 365 and can't be changed here. The edit form says "Synced from Microsoft 365 — name, vendor, seats and company are managed in Azure. Cost, billing, dates, owner and notes are yours to edit."
- **Yours to edit:** cost and currency, billing details, purchase and renewal dates, owner and notes.
- **Seats:** the people icon reads **View seats** and the list is read-only: "Assignments are synced from Microsoft 365 — assign or remove this license in Azure, and it updates here on the next sync."
- **No delete:** synced licenses have no Delete action. To make them regular, editable items, use **Disconnect & unlock records** on the connector.
- **Allocation:** the details pane shows a **Microsoft 365 allocation** box with **Purchased**, **Assigned** and **Available** for the whole tenant, the license status and SKU, any units in grace period / suspended / locked out, and how many holders weren't matched to an employee.

## Hiding a synced license

Use this for free or irrelevant Microsoft 365 licenses you don't want to track. Only synced licenses can be hidden — a manually added item can simply be deleted.

1. Click the eye-off icon (**Hide**) on the row, or **Hide** in the details pane footer. You'll see "{name} hidden".
2. Hidden licenses disappear from the list. When any exist, a link under the table reads "{n} hidden license(s) — show"; click it to include them (marked **Hidden**), and "— hide" to leave them out again.
3. To bring one back, show hidden licenses and click **Unhide** on its row or in its details pane ("{name} is visible again").

## Notes

- Hidden licenses are left out of sidebar and Overview counts, search, reports, reminders, list filters and your plan's item limit. They keep syncing. An employee who holds one still sees it in the employee portal, and it still appears on their employee page, marked **Hidden**.
- You can bulk-import software & services via the **Import** button next to Add Asset. It accepts CSV files only (Excel files aren't supported), up to 5MB and 20,000 rows.
- Adding a software item counts against your organization's pooled asset limit — see [Viewing plan & billing status](../administration/billing.md).
