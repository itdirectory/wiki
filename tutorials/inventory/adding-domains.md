# Adding a domain

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Domains** (`/domains`).
2. Click **Add Domain** (top right, next to **Import**). The **Add domain** form opens in a pane on the right.
   - Shortcut from any page: click **Add asset** in the top bar and choose **Domain**.
3. Fill in the form:

   **Domain details**
   - **Sub-Organization** — required; shown only if your account has access to more than one org.
   - **Domain** — required, e.g. `example.com`, `sub.example.com`, or a wildcard like `*.example.com`.
   - **Owner** — optional, the employee responsible for this domain. Searchable employee picker ("Search employees…"); the owner must belong to the domain's sub-organization.

   **Notes**
   - Optional free text.

4. Click **Add Domain** to save (the **Cancel** and **Add Domain** buttons stay pinned at the bottom of the pane). A "Domain added" message confirms it. WHOIS/DNS/SSL details are populated automatically shortly after (by a background process), not entered by hand.

## Viewing and editing domains

- Click a row to open the domain's details in the right-hand pane: status badges, **Owner**, **Last Checked**, notes, and the **WHOIS**, **DNS** and **SSL / TLS** results. Click outside it, press `Esc` or click **×** to close it.
- Click **Refresh Now** in the details pane to ask for a fresh check ("Refresh requested").
- Click **Edit** to switch the pane to the **Edit domain** form. Changing the domain name itself triggers a fresh WHOIS/DNS/SSL check. **Save Changes** saves and returns you to the updated details; **Cancel** returns to the details without saving.
- You can also click the pencil icon on a row to edit directly, or the trash icon (or **Delete** in the details pane) to delete, then confirm in the **Delete Domain** dialog.
- An add or edit form doesn't close when you click outside it — use **Cancel**, **×** or `Esc`.
- To jump straight to a domain from anywhere, use the search box in the top bar (or press ⌘K / Ctrl K) and pick it — its details pane opens.

## Finding and filtering domains

- Use the search bar ("Search by name, registrar…").
- Narrow the list with the filter dropdowns next to the search bar. Each one starts with **All**, and filters can be combined:
  - **Issue** — **Any issue**, **Registration expiring (30d)**, **Certificate expiring (30d)**, **Certificate expired**, **Check failed**, or **No issues**.
  - **Registrar**, **SSL issuer** — pick from the values found on your domains.
  - **Owner** — **Has owner** or **No owner**.
- While any filter is set, click **Clear filters** to reset them all.
- The list has an **Owner** column; click a column header to sort (including by owner), and use the column visibility menu to show or hide columns.
- The table paginates at 25 rows per page.

## Notes

- The owner must be in the domain's own sub-organization. If you move a domain to another sub-organization in the edit form, also pick an owner from that sub-organization; otherwise saving fails with "Employee not found".
- An employee's details pane lists the domains they own under **Owned Domains** — see [Adding an employee](../people/adding-employees.md).
- When the list is completely empty (no search or filters), it shows an **Add Domain** button. Org admins also see **Set up Cloudflare sync**, which leads to Settings → Integrations; other users see a hint to ask their org admin.
- Domains can also be imported automatically from Cloudflare — see [Setting up connectors](../administration/connectors.md). Domains imported this way show a **Cloudflare** badge.
- You can also bulk-import domains via the **Import** button next to Add Domain. Columns: **Domain** (required), **Owner** (the owner's employee email) and **Notes**. It accepts CSV files only (Excel files aren't supported), up to 5MB and 20,000 rows.
- Adding a domain counts against your organization's pooled asset limit — see [Viewing plan & billing status](../administration/billing.md).
