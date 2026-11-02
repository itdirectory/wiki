# Adding a hardware item

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Hardware** (`/hardware`).
2. Click **Add Hardware** (top right, next to **Import**). The **Add hardware** form opens in a pane on the right.
   - Shortcut from any page: click **Add asset** in the top bar and choose **Hardware**.
3. Fill in the form, organized into sections:

   **Basic info**
   - **Sub-Organization** — required; shown only if your account has access to more than one org.
   - **Name** — required (e.g. "MacBook Pro 14").
   - **Type** — required: Laptop, Desktop, Server, Monitor, Phone, Tablet, Networking, Peripheral, or Other. Defaults to Laptop.
   - **Status** — defaults to Active (Active / In Storage / In Repair / Retired / Disposed).

   **Device details**
   - **Brand**, **Model**, **Serial Number**, **Asset Tag** — all optional.

   **Ownership & purchase**
   - **Assigned To** — optional, searchable employee picker (shows "No employees yet — add employees first" if your org has none — see [Adding an employee](../people/adding-employees.md)).
   - **Vendor / Supplier** — optional.
   - **Purchase Price** — optional amount, with a currency picker next to it: **ILS (₪)**, **USD ($)** or **EUR (€)**. Defaults to USD; each item keeps its own currency.
   - **Purchase Date**, **Warranty Expiry** — optional.

   **Notes**
   - Optional free text.

4. Click **Add Hardware** to save (the **Cancel** and **Add Hardware** buttons stay pinned at the bottom of the pane). A "Hardware added" message confirms it.

## Viewing and editing hardware

- Click a row to open the item's details in the right-hand pane. Click outside it, press `Esc` or click **×** to close it.
- From the details pane, click **Edit** to switch the pane to the **Edit hardware** form. **Save Changes** saves and returns you to the updated details; **Cancel** returns to the details without saving.
- You can also click the pencil icon on a row to edit directly, or the trash icon (or **Delete** in the details pane) to delete, then confirm in the **Delete Hardware** dialog.
- An add or edit form doesn't close when you click outside it, so you won't lose what you've typed by accident — use **Cancel**, **×** or `Esc`.
- To jump straight to an item from anywhere, use the search box in the top bar (or press ⌘K / Ctrl K) and pick the item — its details pane opens.

## Finding and filtering hardware

- Use the type tabs below the page header (All / Laptop / Desktop / …) to filter by device type.
- Use the search bar ("Search by name, serial, tag…") to search.
- Narrow the list further with the filter dropdowns next to the search bar. Each one starts with **All**, and filters can be combined:
  - **Status** — Active / In Storage / In Repair / Retired / Disposed.
  - **Warranty** — **Expired** or **Expiring (30d)**.
  - **Assigned** — **Assigned** or **Unassigned**.
  - **Brand**, **Vendor** — pick from the values already used in your hardware.
- While any filter is set, click **Clear filters** to reset them all.
- Click a column header to sort; use the column visibility menu to show or hide columns.
- The table paginates at 25 rows per page; use the pagination bar at the bottom.

## Notes

- When the list is completely empty (no search or filters), it shows an **Add Hardware** button. Org admins also see **Set up Microsoft Intune sync**, which leads to Settings → Integrations; other users see a hint to ask their org admin. See [Setting up connectors](../administration/connectors.md).
- Devices synced from Microsoft Intune show an **Azure** badge.
- If your organization uses the employee portal with automatic signature requests, assigning a device to an employee who has signed a handover before can send them a new signature request — see [Employee portal](../people/employee-portal.md).
- You can also bulk-import hardware via the **Import** button next to Add Hardware. It accepts CSV files only (Excel files aren't supported), up to 5MB and 20,000 rows.
- Adding hardware counts against your organization's pooled asset limit — see [Viewing plan & billing status](../administration/billing.md).
