# Editing organization details

**Who can do this:** Org Admin only.

## Steps

1. In the left sidebar, click **Settings**, then click the **General** tab (`/settings/general`, subtitled "Organization details and preferences").
2. Update **Organization Name** as needed.
3. Note the **Slug** field is read-only — it's auto-generated from the organization name and can't be edited directly.
4. Click **Save Changes** (disabled until you've actually changed something). A "Settings saved" toast confirms success.

## Deleting your organization

5. Further down the same page is a **Danger Zone** section warning that deleting is permanent and includes all sub-organizations, employees, assets, users, and credentials. Click **Delete Organization** to open the confirmation dialog.
6. Unlike deleting a sub-org (see [Creating and managing sub-organizations](creating-sub-organizations.md)), there's no "move to parent" choice here — this is your root organization, so there's no parent to move anything to. The dialog always shows a full count of what will be deleted: sub-organizations, employees, hardware, software assets, users, and domains.
7. Type your organization's name exactly into the confirmation field to enable the **Delete Organization** button, then click it.
8. On success, you're signed out immediately and returned to the login page — this deletes the organization your own account belongs to.

## Notes

- Deleting your organization is irreversible and cannot be started by anyone but an Org Admin.
