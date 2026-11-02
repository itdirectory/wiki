# Managing your own profile and password

**Who can do this:** Any authenticated user, any role.

## Profile

1. At the bottom of the left sidebar, click your name, then **My Account** (`/settings/account`) — this section is separate from the admin Settings pages and isn't restricted to Org Admins.
2. On the **Profile** tab:
   - Update **Display Name**.
   - **Email** is read-only, shown with a **Verified** or **Unverified** badge. If unverified, click **Resend verification email** below it.
   - **Role** is read-only (only an Org Admin can change your role, from **Settings → Users**).
3. Click **Save Profile**. A "Profile updated" toast confirms success.

## Security (sign-in codes and password)

4. Click the **Security** tab (`/settings/account/security`).
5. If your account is SSO-only, you'll see an **SSO Account** notice instead: "Password management is handled by your SSO provider. Contact your administrator to change your sign-in method."
6. If your organization uses email sign-in codes, a read-only **Sign-in codes** note explains that a one-time code is emailed after your password, that trusted browsers skip it for 30 days, and that changing your password signs them all out. You can't turn this off yourself — see [Signing in](signing-in.md).
7. To change your password, fill in:
   - **Current Password**
   - **New Password** (8+ characters, with an uppercase letter, a lowercase letter, a number and a symbol)
   - **Confirm New Password**
8. Click **Change Password** (or **Set New Password**, if you were sent here because an admin requires a new password). On success you'll see "Password changed — please sign in again" and are taken to the login page.

## Notes

- Changing your password signs you out everywhere — on every device — and every browser you chose to trust will ask for a sign-in code again.
- If an admin required you to change your password, you'll land on this page automatically with the banner "Your administrator requires you to set a new password before continuing.", and the button reads **Set New Password**.
- Forgot your current password? Sign out and use **Forgot password?** on the login page — see [Signing in](signing-in.md#forgot-your-password).
