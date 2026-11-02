# Signing in

**Who can do this:** Any user, any role.

## Signing in with a password

1. Go to the login page (`/login`). Enter your **Email** and click **Continue**.
   - If your account signs in with Microsoft (single sign-on), you're sent straight to Microsoft's sign-in page instead — there's no password step. See "Signing in with Microsoft" below.
2. Enter your **Password** and click **Sign in**. (Click **Change** next to your email to go back and use a different one.)
   - A wrong password shows "Invalid email or password". After too many attempts you'll see "Too many sign-in attempts. Please try again later."
3. Unless your organization has sign-in codes turned off, a 6-digit code is now emailed to you. The page shows "We emailed a 6-digit code to {your email}. It expires in 10 minutes."
4. Type the code into **Sign-in code**. It's submitted automatically once all six digits are in (or click **Verify**).
5. Optional: tick **Trust this browser for 30 days** before entering the code to skip the code step on this browser for the next 30 days.

### If the code doesn't arrive or doesn't work

- **Resend code** appears after a 60-second countdown ("New code in {N}s"). Clicking it shows "A new code is on its way." Only the most recent code works.
- A wrong code shows "That code isn't right. Check the latest email and try again."
- After 5 wrong guesses the code stops working: you'll see "Too many wrong codes. Sign in again to get a new code." and are returned to the start.
- If the email can't be sent: "We couldn't email your sign-in code. Please try again shortly."
- **Use a different account** returns you to the email step.

## Signing in with Microsoft

If your organization has single sign-on set up (see [Security settings](../administration/security-settings.md)) and your account is a Microsoft-only account, or you were pre-invited as an SSO user, entering your email on the login page takes you to Microsoft. After signing in there you're brought back and signed in ("Signing you in…"). There's no emailed sign-in code for Microsoft sign-ins.

## Forgot your password

1. On the password step, click **Forgot password?** (`/forgot-password`).
2. Enter your **Email** and click **Send reset link**.
3. The page shows "If an account exists for that email, we've sent a password reset link. It expires in 1 hour." (It says this whether or not the account exists.)
4. Open the link in the email. On **Set new password**, fill in **New password** and **Confirm new password** and click **Set new password**.
5. On "Password updated. Redirecting you to sign in…", sign in with the new password.

## Accepting an invitation

When an Org Admin adds you (see [Managing users](../administration/user-management.md)), you get an email "You've been invited to {organization} on IT Directory".

1. Click **Set your password** in the email. The link is valid for 7 days.
2. On **Set your password** ("Choose a password to finish setting up your account"), fill in **New password** and **Confirm new password**, then click **Set password**.
3. On "Password set. Redirecting you to sign in…", sign in with your email and new password.
   - If your organization uses Microsoft sign-in, the email says you can "sign in with Microsoft" instead — just enter your email on the login page.

If the link has expired, ask your admin to resend the invitation, or use **Forgot password?** on the login page.

## Verifying your email

If your email address isn't verified yet, every page sends you to **Verify your email** (`/verify-pending`) — "We sent a verification link to {your email}. Check your inbox and click the link to continue."

- Click the link in the email (valid for 24 hours). You'll see "Your email address has been verified." and then sign in again.
- **Resend verification email** sends a new link (then shows "Resend in {N}s" for a short wait).
- **Sign out** if you're signed in to the wrong account.

Entering an emailed sign-in code, or setting your password from an invitation or reset link, also verifies your email.

## Notes

- Passwords must be at least 8 characters and include an uppercase letter, a lowercase letter, a number and a symbol.
- Sign-in codes are on by default for every organization. Only IT Directory can turn them off; you can see whether they apply to you under **My Account → Security** (see [Managing your own profile and password](account-profile-security.md)).
- Password sessions end after a period of inactivity (8 hours by default) — staying active keeps you signed in. Microsoft sign-in sessions last 1 hour, after which you sign in with Microsoft again.
- Changing or resetting your password signs you out everywhere, on every device, and every browser you chose to trust will ask for a code again.
- An admin may require you to set a new password; you'll then be taken to **My Account → Security** before you can continue.
- If your organization's trial has ended or access is paused, you'll see **Your trial has ended** after signing in — see [Viewing plan & billing status](../administration/billing.md).
