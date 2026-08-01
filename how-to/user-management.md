# Managing users

**Who can do this:** Org Admin only.

## Getting to Users

1. In the left sidebar, click **Settings**, then click the **Users** tab (`/settings/users`, subtitled "Team members in your organization").
2. The table lists Name, Email (with a **Local** or **SSO** badge), Role, Companies, Status (Active/Inactive), and Joined date.

## Adding a user

3. Click **Add User** (top right).
4. In the **Add User** dialog, fill in:
   - **Full Name**
   - **Email**
   - **Temporary Password** (8+ chars, upper/lowercase, number & symbol) — the user should change this after their first login.
   - **Role** — one of:
     - **Org Admin** — full access to all companies and settings.
     - **Company Admin** — full access to assigned companies only.
     - **Org Technician** — directory & employee ops across all companies, no settings.
     - **Company Technician** — directory & employee ops on assigned companies only.
   - **Company Access** — if you chose Company Admin or Company Technician and your org has sub-orgs, a checklist appears to grant access to specific sub-orgs. If you leave it empty, a warning appears: "No companies selected — user will have no data access."
5. Click **Create User**.

## Editing a user

6. Click the pencil icon on their row. The **Edit User** dialog has the same **Full Name**, **Role**, and **Company Access** fields, plus:
   - **Account Status** — Active / Inactive toggle. Setting a user to Inactive blocks their login but preserves their history.
   - **"Require password change on next login"** — checkbox, only shown for local (non-SSO) accounts.
7. Click **Save Changes**.

## Removing a user

8. Click the trash icon on their row. The **Remove User** dialog warns this is a permanent removal, and suggests deactivating instead if you want to preserve history.
9. Click **Remove** to confirm (destructive, cannot be undone).

## Notes

- You cannot change your own role or Active/Inactive status through this page — the system blocks it even if you try.
- Prefer **deactivating** (Edit → set status to Inactive) over **removing** when someone leaves but you want to keep their historical assignments intact.
- SSO users can also be pre-provisioned via **Settings → SSO — Entra ID → User Invitations** — see https://docs.itdirectory.app/how-to/sso-setup.
