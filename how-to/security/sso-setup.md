# Setting up Single Sign-On (Microsoft Entra ID)

**Who can do this:** Org Admin only.

Lets your team sign in with their Microsoft accounts instead of an email/password, and lets you pre-provision a role for someone before they ever log in.

## Steps

1. In the left sidebar, click **Settings**.
2. On the horizontal tab bar, click **SSO (Entra ID)**. You'll land on `/settings/sso`, subtitled "Let your team sign in with their Microsoft accounts".
3. You'll see two page tabs: **Connection** and **User Invitations**.

### Connection tab

4. Note the **Callback URL** field at the top — it's read-only and pre-filled (`<your-app-url>/api/sso/callback`). Click the copy icon next to it and register this URL in your Azure app registration.
5. Fill in:
   - **Tenant ID (Directory ID)** — from your Azure/Entra tenant.
   - **Client ID (Application ID)** — from your Azure app registration.
   - **Client Secret** — the app registration's client secret value. Use the eye icon to show/hide what you've typed. If a secret is already saved, the field shows "•••••••••••• (saved — enter to replace)" — leave it blank to keep the existing one.
6. Once Tenant ID, Client ID, and a Client Secret are all present, the **"Enable SSO login for this organization"** checkbox becomes available. Check it to turn SSO on.
7. Click **Save Changes**. A "SSO configuration saved" toast confirms success. ("Please fill in all fields" appears if something required is missing.)

### User Invitations tab

8. Click **User Invitations**. This lets you pre-register a person's email + role so their account is created automatically the first time they sign in via Entra ID.
9. Click **Invite User**. In the **Invite SSO User** dialog:
   - **Email** — the person's email address.
   - **Role** — dropdown, limited to **Org Admin** or **Org Technician** at invite time (company-scoped roles can be assigned after their first login, from **Settings → Users**).
10. Click **Send Invitation**. The invitation now appears in the list as `email — {Role} · Invited {date}`, with a trash icon to revoke it.

## Notes

- There's no in-app password setup for SSO users — the account is created automatically on first Entra ID sign-in.
- Employee and device sync (importing people/devices from Entra/Intune) are configured separately — see https://docs.itdirectory.app/how-to/connectors/connectors.
- If SSO is disabled after being enabled, affected users fall back to needing a local password (or lose access if they never had one) — double check before disabling for an active organization.
