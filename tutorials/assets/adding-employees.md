# Adding an employee

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Employees** (`/employees`).
2. Click **Add Employee** (top right, next to **Import**).
3. Fill in the **Add Employee** form, organized into sections:

   **Basic Info**
   - **Sub-Organization** — required if your account has access to more than one org.
   - **Full Name** — required.
   - **Email** — required.

   **Work Details**
   - **Job Title**, **Department** — optional.

   **Contact & Start Date**
   - **Phone**, **Start Date** — optional.

   **Notes**
   - **Notes** — optional free text.

4. Click **Add Employee** to save.

## Finding employees and assigning items

- Use the search bar ("Search by name, email, department…") to filter the list. The table paginates at 25 rows per page.
- Click an employee's row to open their detail view. From there you can assign existing hardware or software to them directly (separate "Search hardware…" / "Search software…" boxes) — this is different from the Add Employee form, which only creates the employee record.
- To edit an employee, open their row and update the same form — the submit button reads **Save Changes**.

## Notes

- Adding an employee counts against your organization's pooled asset limit — see https://docs.itdirectory.app/tutorials/billing.
- Employees can also be bulk-imported via the **Import** button, or synced automatically from Microsoft Entra ID — see https://docs.itdirectory.app/tutorials/connectors. Bulk import accepts CSV files only (Excel files aren't supported), up to 5MB and 20,000 rows.
