# Editing organization details

**Who can do this:** Org Admin only.

## Steps

1. In the left sidebar, click **Settings**, then click **General** in the settings menu on the left (`/settings/general`, subtitled "Organization details and preferences").
2. Update **Organization Name** as needed.
3. Note the **Slug** field is read-only — it's auto-generated from the organization name and can't be edited directly.
4. Click **Save Changes** (disabled until you've actually changed something). A "Settings saved" toast confirms success.

## Company logo

5. Under **Company logo**, click **Upload logo** (or **Replace logo** if one is already set) and choose a PNG, JPEG or WebP image of up to 256 KB. It's saved right away — no need to click Save Changes — and a "Logo updated" toast confirms it. WebP images are converted to PNG.
6. To go back to no logo, click **Remove** ("Logo removed").

The logo is printed on handover forms and shown in the employee portal (see [Employee portal](../people/employee-portal.md)). Sub-organizations use this logo too. A file that's too large or not a PNG/JPEG/WebP image is rejected with "The logo must be a PNG, JPEG or WebP image of up to 256 KB."

## Deleting your organization

7. Further down the same page is a **Danger Zone** section warning that deleting is permanent and includes all sub-organizations, employees, assets, users, and credentials. Click **Delete Organization** to open the confirmation dialog.
8. Unlike deleting a sub-org (see [Creating and managing sub-organizations](creating-sub-organizations.md)), there's no "move to parent" choice here — this is your root organization, so there's no parent to move anything to. The dialog always shows a full count of what will be deleted: sub-organizations, employees, hardware items, software assets, user accounts, domains, VLANs, and public IPs.
9. Type your organization's name exactly into the confirmation field to enable the **Delete Organization** button, then click it.
10. On success, you're signed out immediately and returned to the login page — this deletes the organization your own account belongs to.

## Notes

- Deleting your organization is irreversible and cannot be started by anyone but an Org Admin.
