# Adding a software license, SaaS subscription, or service

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Software & Services** (`/software-assets`).
2. Click **Add Asset** (top right, next to **Import**). The dialog is titled **Add Software / Service**.
3. Fill in the form, organized into sections:

   **Basic Info**
   - **Sub-Organization** — required if your account has access to more than one org.
   - **Type** — required, one of:
     - **License** — a keyed software license (e.g. JetBrains, Windows).
     - **SaaS** — a keyless subscription with seats (e.g. Slack, ChatGPT).
     - **Service** — a membership, domain, or other recurring service with no seats (e.g. Apple Developer).
   - **Name** — required.

   **Vendor & Ownership**
   - **Vendor** — optional.
   - **Owner (responsible person)** — optional, searchable employee picker. This is who's *managerially responsible*, not necessarily a seat holder.

   **License Details** (only shown if Type = License)
   - **License Key** — required when creating a new License asset (leave blank when editing to keep the current key).
   - **License Type** — optional: Perpetual, Subscription, Per Seat, Volume.
   - **Version** — optional.

   **Subscription Details** (only shown if Type = SaaS)
   - **Plan / Tier**, **Website URL**, **Billing Cycle** (Monthly / Quarterly / Annual) — all optional.

   *(Type = Service has no extra section here.)*

   **Billing & Dates**
   - **Total Seats** — optional, hidden entirely for Service.
   - **Cost ($)** — labeled "Cost per Cycle ($)" for SaaS.
   - **Purchase Date** — optional.
   - **Expiry Date** — labeled "Renewal Date" for SaaS/Service, "Expiry Date" for License.

   **Notes**
   - **Notes** — optional free text.

4. Click **Add Asset** to save. (If you left License Key blank while creating a License, you'll see an inline "License key is required" error.)

## Assigning seats

- Licenses and SaaS assets support **seat assignments** — which employees hold a seat. This is managed from the asset's row/detail view (seat manager dialog), not from the Add form. Service assets don't support seats.

## Finding software & services

- Use the kind tabs (All / Licenses / SaaS / Services) and the search bar ("Search by name, vendor, plan…"). The table paginates at 25 rows per page.
- To edit an existing asset, open its row and update the same form — the submit button reads **Save Changes**.

## Notes

- You can also bulk-import software & services via the **Import** button next to Add Asset. It accepts CSV files only (Excel files aren't supported), up to 5MB and 20,000 rows.
- Adding a software asset counts against your organization's pooled asset limit — see https://docs.itdirectory.app/tutorials/billing.
