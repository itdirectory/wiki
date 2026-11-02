# Managing your own profile and password

**Who can do this:** Any authenticated user, any role.

## Profile

1. In the left sidebar, click your name/avatar, or navigate to **Settings → Account** (`/settings/account`) — this "My Account" section is separate from the admin Settings pages and isn't restricted to Org Admins.
2. On the **Profile** tab:
   - Update **Display Name**.
   - **Email** is read-only, shown with a **Verified** or **Unverified** badge. If unverified, click **"Resend verification email"** below it.
   - **Role** is read-only (only an Org Admin can change your role, from **Settings → Users**).
3. Click **Save Profile**.

## Security (changing your password)

4. Click the **Security** tab (`/settings/account/security`).
5. If your account is SSO-only, you'll see an "SSO Account" notice instead of a password form — password changes for SSO accounts are handled by your identity provider; contact your admin to change your sign-in method.
6. If your account has a local password, fill in:
   - **Current Password**
   - **New Password**
   - **Confirm New Password**
7. Click **Change Password** (or **Set New Password**, if you were forced here after an admin required a password reset). On success you'll be signed out automatically and need to log in again with the new password.

## Notes

- If an admin required you to change your password, you'll land on this page automatically with a banner explaining why, and the button will read "Set New Password" instead of "Change Password".
