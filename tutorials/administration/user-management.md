# Managing users

**Who can do this:** Org Admin only.

## Getting to Users

1. In the left sidebar, click **Settings**, then click **Users** in the settings menu on the left (`/settings/users`, subtitled "Team members in your organization").
2. The table lists Name, Email, Role, Companies, Status (Active/Inactive), and Joined date. Next to each email is a badge:
   - **Local** — signs in with a password.
   - **SSO** — signs in with Microsoft only.
   - **Invited** — hasn't accepted their invitation yet.
   - **Invite expired** — the invitation link (valid 7 days) ran out before they used it.

## Inviting a user

3. Click **Invite User** (top right).
4. In the **Invite User** dialog ("We'll email them a link to set their password."), fill in:
   - **Full Name**
   - **Email**
   - **Role** — one of:
     - **Org Admin** — full access to all companies and settings.
     - **Company Admin** — full access to assigned companies only.
     - **Org Technician** — directory & employee ops across all companies, no settings.
     - **Company Technician** — directory & employee ops on assigned companies only.
   - **Company Access** — if you chose Company Admin or Company Technician and your org has sub-orgs, a checklist appears to grant access to specific sub-orgs. If you leave it empty, a warning appears: "No companies selected — user will have no data access".
5. Click **Send Invitation**. A "Invitation sent to {email}" toast confirms it, and the user appears in the list as **Invited**.
   - If the user was created but the email couldn't be sent, you'll see "{email} was added, but the invitation email couldn't be sent — use Resend invite." — resend it as below.
   - "Email already in use" means an account with that email already exists.
6. The user gets an email with a **Set your password** link, valid for 7 days. If your organization has single sign-on enabled, the email also tells them they can sign in with Microsoft instead. What they see is described in [Signing in](../getting-started/signing-in.md#accepting-an-invitation).

## Resending an invitation

7. On an **Invited** or **Invite expired** row, click the send (paper plane) icon (**Resend invitation**). A "Invitation resent to {email}" toast confirms it. The new link is valid for another 7 days.
   - If the email fails to send, the link they already have keeps working.
   - The icon only shows for active users whose invitation is still pending; once they've set a password or signed in with Microsoft, it disappears.

## Editing a user

8. Click the pencil icon on their row. The **Edit User** dialog has the same **Full Name**, **Role**, and **Company Access** fields, plus:
   - **Account Status** — Active / Inactive toggle. Inactive users cannot log in but their history is preserved.
   - **"Require password change on next login"** — checkbox, only shown for users who have a password.
9. Click **Save Changes**. A "User updated" toast confirms success.

## Removing a user

10. Click the trash icon on their row. The **Remove User** dialog asks "Permanently remove {name}? To preserve history, consider deactivating instead."
11. Click **Remove** to confirm (cannot be undone). A "User removed" toast confirms it.

## Notes

- You can't change your own role or Active/Inactive status, or remove yourself, from this page — the system blocks it. Change your own display name from **My Account** instead (see [Managing your own profile and password](../getting-started/account-profile-security.md)).
- Prefer **deactivating** (Edit → set status to Inactive) over **removing** when someone leaves but you want to keep their historical assignments intact.
- An invited user can also set their password with **Forgot password?** on the login page.
- SSO users can also be pre-provisioned via **Settings → Single sign-on → SSO User Invitations** — see [Security settings](security-settings.md).
