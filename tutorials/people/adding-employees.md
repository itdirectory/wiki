# Adding an employee

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Employees** (`/employees`).
2. Click **Add Employee** (top right, next to **Import**). The **Add employee** form opens in a pane on the right.
   - Shortcut from any page: click **Add asset** in the top bar and choose **Employee**.
3. Fill in the form, organized into sections:

   **Basic info**
   - **Sub-Organization** — required; shown only if your account has access to more than one org.
   - **Full Name** — required.
   - **Email** — required.

   **Work details**
   - **Job Title**, **Department** — optional.

   **Contact & start date**
   - **Phone**, **Start Date** — optional.

   **Notes**
   - Optional free text.

4. Click **Add Employee** to save (the **Cancel** and **Add Employee** buttons stay pinned at the bottom of the pane). An "Employee added" message confirms it.

## Viewing an employee and assigning items

Click an employee's row to open their details in the right-hand pane. Besides their contact details, it shows:

- **Assigned Hardware** — their devices. Pick a device in the "Search hardware…" box and click **Assign** to assign it; click the **×** on a device to unassign it.
- **Software & Services** — their seats. Pick an item in the "Search software…" box and click **Assign**; click the **×** on a seat to remove it. Seats synced from Microsoft 365 carry a Microsoft 365 badge and can't be removed here, and a license your team has hidden is marked **Hidden**.
- **Owned Domains** — domains this employee is the owner of (shown only if there are any). Click one to open it. Ownership is set on the domain — see [Adding a domain](../inventory/adding-domains.md).
- **Handover** — the employee portal's handover forms for this person (request a signature, receive items back, view or download signed PDFs). See [Employee portal](employee-portal.md).

At the bottom of the pane:

- **Send By Email to** *first name* — emails the employee a PDF listing the items assigned to them.
- **Delete** — removes the employee after you confirm in the **Remove Employee** dialog. Their hardware is unlinked and their software seats are released.
- **Edit** — switches the pane to the **Edit employee** form. **Save Changes** saves and returns you to the updated details; **Cancel** returns to the details without saving.

You can also edit or delete directly from a row with the pencil and trash icons. An add or edit form doesn't close when you click outside it — use **Cancel**, **×** or `Esc`. A details pane closes on an outside click too.

To jump straight to an employee from anywhere, use the search box in the top bar (or press ⌘K / Ctrl K) and pick them — their details pane opens.

## Finding employees

- Use the search bar ("Search by name, email, department…").
- Narrow the list with the filter dropdowns next to the search bar. Each one starts with **All**, and filters can be combined:
  - **Department** — pick from the departments already used.
  - **Hardware** — **Has hardware** or **No hardware**.
  - **Software** — **Has seats** or **No seats**.
- While any filter is set, click **Clear filters** to reset them all.
- Click a column header to sort; use the column visibility menu to show or hide columns.
- The table paginates at 25 rows per page.

## Notes

- When the employee portal is turned on, the list also shows a **Handover** column with each person's handover status, and a checkbox on each row. Select employees and click **Request signature** to ask them all to sign at once. See [Employee portal](employee-portal.md).
- The **Software** count in the list leaves out Microsoft 365 licenses your team has hidden; the employee's details pane still shows them.
- When the list is completely empty (no search or filters), it shows an **Add Employee** button. Org admins also see **Set up Microsoft Entra ID sync**, which leads to Settings → Integrations; other users see a hint to ask their org admin.
- Employees synced from Microsoft Entra ID show an **Azure** badge.
- Adding an employee counts against your organization's pooled asset limit — see [Viewing plan & billing status](../administration/billing.md).
- Employees can also be bulk-imported via the **Import** button, or synced automatically from Microsoft Entra ID — see [Setting up connectors](../administration/connectors.md). Bulk import accepts CSV files only (Excel files aren't supported), up to 5MB and 20,000 rows.
