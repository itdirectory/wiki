# Configuring expiry reminders

**Who can do this:** Org Admin only.

Sets up a daily email digest of hardware, license, and domain items approaching expiration. This page only stores the configuration — a separate background process reads it and actually sends the emails.

## Steps

1. In the left sidebar, click **Settings**, then click the **Reminders** tab (`/settings/reminders`).
2. In **Recipient emails**, add each address that should receive the digest: type an address and press Enter (or a comma) to turn it into a tag, or paste in a whole list at once and each valid address becomes its own tag. Remove one by clicking the × on its tag, or press Backspace with the input empty to remove the last one. An invalid entry shows a brief "Not a valid email address" error instead of being added.
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
