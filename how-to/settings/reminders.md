# Configuring expiry reminders

**Who can do this:** Org Admin only.

Sets up a daily email digest of hardware, license, and domain items approaching expiration. This page only stores the configuration — a separate background process reads it and actually sends the emails.

## Steps

1. In the left sidebar, click **Settings**, then click the **Reminders** tab (`/settings/reminders`).
2. In **Recipient emails**, enter a comma-separated list of addresses that should receive the digest (e.g. `it-team@company.com, ops@company.com`).
3. For each of the four categories, toggle it on/off and set how many days before the due date it should start alerting:
   - **Hardware warranty expiry**
   - **Software license / SaaS renewal**
   - **Domain expiry**
   - **SSL certificate expiry**
   Each defaults to 30 days before due, adjustable from 1–365.
4. That's it — there's no Save button. Changes autosave about a second after you stop typing/toggling; watch the bottom-right indicator cycle through "Saving…" → "Saved" (or "Failed to save" if something goes wrong).

## Notes

- The **"Last sent"** / **"Last send failed"** line reflects the background worker's most recent run, not anything triggered from this page.
- This page is configuration only — it doesn't preview or send a test email.
