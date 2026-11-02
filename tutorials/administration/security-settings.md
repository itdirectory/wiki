# Security settings: single sign-on, invitations & report recipients

**Who can do this:** Org Admin only.

Configures single sign-on with Microsoft Entra ID, pre-provisions SSO users, and approves external email addresses allowed to receive emailed reports.

## Getting there

The settings live on two pages in the **Access** group of the settings menu on the left:

- **Single sign-on** (`/settings/sso`): the Entra ID connection, with **User Invitations** below it.
- **Report recipients** (`/settings/report-recipients`).

1. In the left sidebar, click **Settings**, then click **Single sign-on** in the settings menu.
   - If you have an old bookmark to `/settings/security`, it will automatically redirect here.

## Entra ID connection

2. A status pill next to the "Connection" heading shows **Connected** (green) or **Not configured** (gray).
3. Note the **Callback URL** field at the top — it's read-only and pre-filled (`<your-app-url>/api/sso/callback`). Click the copy icon next to it and register this URL in your Azure app registration.
4. Fill in:
   - **Tenant ID (Directory ID)** — from your Azure/Entra tenant.
   - **Client ID (Application ID)** — from your Azure app registration.
   - **Client Secret** — the app registration's client secret value. Use the eye icon to show/hide what you've typed. If a secret is already saved, the field shows "•••••••••••• (saved — enter to replace)" — leave it blank to keep the existing one; typing anything replaces it once you save.
5. Once Tenant ID, Client ID, and a Client Secret (new or already-saved) are all present, the **"Enable SSO login for this organization"** checkbox becomes available. Check it to turn SSO on.
6. Click **Save Changes**. A "SSO configuration saved" toast confirms success. ("Please fill in all fields" appears if something required is missing; "Failed to save" appears on a server error.)
7. A note at the bottom of this section reminds you: "Employee and device sync are managed in Settings → Integrations" (linked) — see [Setting up connectors](connectors.md).

## User Invitations

8. Scroll down to **SSO User Invitations**, below the connection settings. This lets you pre-register a person's email + role so their account is created automatically the first time they sign in via Entra ID.
9. Click **Invite User**. In the **Invite SSO User** dialog ("The user will be provisioned when they first sign in via Entra ID."):
    - **Email** — the person's email address.
    - **Role** — dropdown, limited to **Org Admin** or **Org Technician** at invite time. A helper note explains company-scoped roles can be assigned after their first login, from **Settings → Users**.
10. Click **Send Invitation**. On success you'll see an "Invitation created" toast, and the invite appears in the list as `email` / `{Role} · Invited {date}` with a trash icon to revoke it.

## Report recipients

11. Click **Report recipients** in the settings menu (`/settings/report-recipients`). This is where you approve additional, *outside* email addresses (a different domain than your own — e.g. an external IT provider or auditor) to receive reports emailed from the Reports page.
12. Note the description on this page: anyone on your own email domain, or anyone who's already a user/employee in your org, can already receive reports with no setup here — this list is only needed for outside parties.
13. Under **Allowed external recipients**, add addresses one at a time (type an address and press Enter, or paste in a whole list) and remove one by clicking its ×.
14. Click **Save Changes**. A "Settings saved" toast confirms success ("Failed to save changes" on error).

## Notes

- There's no in-app password setup for SSO users — the account is created automatically on first Entra ID sign-in.
- Employee and device sync (importing people/devices from Entra/Intune) are configured separately — see [Setting up connectors](connectors.md).
- If SSO is disabled after being enabled, affected users fall back to needing a local password (or lose access if they never had one) — double check before disabling for an active organization.
- Report recipients approved here apply to every report sent from your organization, regardless of which admin sends it.
