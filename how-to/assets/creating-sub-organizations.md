# Creating and managing sub-organizations

**Who can do this:** Org Admin only.

Sub-organizations represent departments, teams, or client companies within your organization. Company-scoped users (Company Admin / Company Technician) only see the sub-orgs they're explicitly granted access to.

## Steps

1. In the left sidebar, click **Settings**, then click the **Sub-Organizations** tab (`/settings/sub-organizations`, subtitled "Departments or teams within your organization").
2. Click **Add Sub-Org** (top right). If you have no sub-orgs yet, you can also click the **Create one** button in the empty state.
3. In the **Create Sub-Organization** dialog, enter a **Name** (e.g. "Engineering") — this is the only field.
4. Click **Create**. The new sub-org is created as a child of the organization you're currently viewing (there's no separate parent picker — it's always the org you're currently in).

## Renaming a sub-org

5. In the sub-org table, click the pencil icon on the row you want to rename.
6. In the **Rename Sub-Organization** dialog, update **Name** and click **Save**.

## Deleting a sub-org

7. Click the trash icon on the row you want to delete.
8. The **Delete "{name}"** dialog warns "This action cannot be undone." If the sub-org has any assets, it shows a summary box with counts of employees, hardware, software assets, users, and domains it contains; if it has none, it just says "This organization has no assets."
9. If it has assets, choose what happens to them:
   - **Move to parent organization (recommended)** — reassigns everything to the root org.
   - **Permanently delete everything** — deletes hardware, software assets, employees, and users tied to this sub-org, irreversibly.
10. Type the sub-org's name exactly into the confirmation field to enable the **Delete Organization** button — the field's border turns green once it matches, or red with a "Name doesn't match" note if it doesn't — then click it. A confirmation toast reflects which mode you chose (assets moved to the parent, or permanently deleted).

## Notes

- The sub-org table shows Name, Employees, Hardware, Licenses, and Users counts per row.
- Every root organization has a pooled asset/sub-org limit tied to its billing plan. If you're at your sub-org limit, creating a new one fails with "You've reached your sub-organization limit — contact us to upgrade" — see https://docs.itdirectory.app/how-to/billing.
- To grant a Company Admin/Technician access to specific sub-orgs, do that from **Settings → Users** — see https://docs.itdirectory.app/how-to/user-management.
