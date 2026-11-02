# Configuring expiry reminders

**Who can do this:** Org Admin only.

Sets up a daily email digest of hardware warranties, software renewals, domain expirations and SSL certificate expirations that are coming up. This page only stores the configuration — a separate background process reads it and sends the emails.

## Steps

1. In the left sidebar, click **Settings**, then click **Reminders** in the settings menu on the left (under **Features**) (`/settings/reminders`).
2. In **Recipient emails**, add each address that should receive the digest: type an address and press Enter (or a comma) to turn it into a tag, or paste in a whole list at once and each valid address becomes its own tag. Remove one by clicking the × on its tag, or press Backspace with the input empty to remove the last one. An invalid entry shows a brief "Not a valid email address" error instead of being added.
3. For each of the four categories, turn on its **Enabled** switch and set **Days before due** — how many days before the due date the first reminder goes out:
   - **Hardware warranty expiry**
   - **Software license / SaaS renewal**
   - **Domain expiry**
   - **SSL certificate expiry**
   Each category is off until you enable it, and defaults to 30 days before due, adjustable from 1–365.
4. That's it — there's no Save button. Changes autosave about a second after you stop typing/toggling; watch the bottom-right indicator cycle through "Saving…" → "Saved" (or "Failed to save" if something goes wrong).

## When reminders are sent

Each item is reminded about at up to four points, each at most once:
- the configured number of days before it's due
- 7 days before (only when the configured number is more than 7)
- 1 day before
- 1 day after it's due

The emails go out once a day, at a send hour set by your installation (06:00 UTC by default). All recipients get one digest per day listing every item that reached one of these points; if nothing did, no email is sent. An item that reaches several points at once (for example, one added two days before it expires) appears once, and the earlier points aren't sent later. If you change an item's due date, its reminders follow the new date.

## What's included

- Items in your organization **and its sub-organizations**. Items from a sub-organization show which company they belong to.
- Items due within the configured number of days, plus items that expired up to 7 days ago — so enabling a category doesn't email you about everything that expired months ago.
- **Software license / SaaS renewal** covers licenses, SaaS and services (their renewal or expiry date).
- Each item in the email links to it in IT Directory.

## Notes

- The **"Last sent"** / **"Last send failed"** box reflects the background process's most recent run, not anything triggered from this page. "Last sent" only changes when an email actually went out.
- If sending fails, the same items are retried later; they aren't marked as reminded.
- Hidden Microsoft 365 licenses are never included (see [Adding software & services](../inventory/adding-software-services.md)).
- Nothing is sent while there are no recipients, or while your organization's trial has ended or the account is suspended.
- Reminders for unsigned handover forms are separate: they go to the employee, not to these recipients, and need no setup here — see [Employee portal and handover forms](../people/employee-portal.md).
- This page is configuration only — it doesn't preview or send a test email.
