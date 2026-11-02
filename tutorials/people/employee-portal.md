# Employee portal and handover forms

**Who can do this:** Turning the portal on and changing its settings: Org Admin only. Requesting signatures, recording returns and signing an employee out of the portal: any authenticated user with access to the employee's sub-organization.

The employee portal is a separate website where employees (not IT Directory users) sign in with their work email, see what's assigned to them, and sign **handover forms** for the equipment they received. Signed forms are kept with an audit record and can be viewed or downloaded as PDFs.

## Turning the portal on

1. In the left sidebar, click **Settings**, then click **Employee portal** in the settings menu on the left (under **Features**) (`/settings/portal`).
2. Set the switches:
   - **Enable the employee portal** — turns the portal on for your organization and all its sub-organizations.
   - **Ask for a signature when items are assigned** — sends updated handover forms automatically (see "Automatic requests on assignment" below). Can only be switched on while the portal is enabled.
   - **Include software & services in handover forms** — off by default: employees sign for hardware only. On: their software and service seats are listed on the form too. Can only be switched on while the portal is enabled.
3. Optionally edit **Handover declaration** — the text shown above the signature on handover forms (Markdown, up to 5,000 characters). Leave it empty to use the default, which is shown greyed out in the empty box. Changes apply to new requests only — signed forms keep the text they were signed with.
4. Click **Save Changes**. A "Settings saved" toast confirms it.

The **Portal address** box at the bottom shows the portal's URL, with a link to open it — share this address with your employees.

## Requesting a signature from one employee

1. In the left sidebar, click **Employees** (`/employees`) and click an employee to open their view pane.
2. Expand the **Handover** section (collapsed by default; its header shows the employee's handover status and, once signed, "last signed" with the date).
3. Click **Request signature**. A "Signature request emailed to <first name>" toast confirms it.
   - The form lists everything the employee currently holds — hardware only, unless **Include software & services in handover forms** is on.
   - The button is disabled when there's nothing to sign for, with a hint below it (e.g. "No hardware assigned — nothing to sign for yet").
   - Requesting a new signature replaces any earlier request that's still waiting (it shows as **Replaced**).

The section lists the employee's latest five requests and return receipts — **Handover** or **Return**, the item count (and "· automatic" for automatic requests), the date, and a status: **Waiting**, **Signed**, **Cancelled**, **Replaced** or **Returned**. Click the **⋯** menu on a row for:
- **View form** / **View signed form** / **View receipt** — opens the PDF in a preview window, with **Open in new tab** and **Download**.
- **Download form (PDF)** / **Download signed PDF** / **Download receipt (PDF)**.
- **Email again** (waiting requests only) — re-sends the email ("Reminder emailed to <first name>").
- **Cancel request** (waiting requests only) — "Request cancelled".

An unsigned form's PDF has a blank signature line, so it can also be printed and signed on paper.

**Sign out of portal** (in the same section) ends all of the employee's portal sessions ("<first name> was signed out of the portal").

## Requesting signatures from several employees

While the portal is enabled, the employees list gets a checkbox column and a **Handover** column (it can be hidden from the columns menu like any other column).

1. Tick the employees on the current page (the header checkbox selects the whole page).
2. In the bar that appears ("N selected"), click **Request signature**. Click **Clear** to deselect.
3. The toast reports the result, e.g. "5 requests sent · 2 skipped (nothing to sign)". Employees beyond the rate limit are reported as "not sent (rate limit — try again later)".

The **Handover** column shows one of:
- **Awaiting signature** — a request is waiting for the employee.
- **Not signed** — the employee has never signed a handover form.
- **Signed** — their last signed form covers everything they hold.
- **Changed since signing** — they've received items since their last signed form.

Only *added* items change the status; removing or returning items never does.

## Automatic requests on assignment

With **Ask for a signature when items are assigned** on, assigning items to an employee who **has signed a handover form before** updates their form automatically. This applies to every way items get assigned: the hardware form, hardware CSV import, assigning a software seat, and the Microsoft Intune device sync.

- If they have no waiting request, a new one is created for everything they hold and emailed to them.
- If a request is already waiting, its item list is updated in place, so the link they already have shows everything.
- The email goes out at most once every 10 minutes, so assigning several items in a row sends one email.
- An employee who has never signed gets no automatic request — the first request is always sent by hand.
- Removing or returning items never triggers anything.
- With **Include software & services in handover forms** off, assigning a software seat doesn't trigger a request.

## Receiving items back

When an employee returns equipment, record it from their view pane. The employee doesn't sign anything for a return.

1. Open the employee's view pane and expand **Handover**.
2. Click **Receive items back**. The **Receive items back** dialog lists their current hardware and software.
3. Tick the returned items (or **Select all**).
4. Click **Record return (N)**. A "Return recorded and items unassigned" toast confirms it.

The items are unassigned immediately (hardware becomes unassigned, software seats are freed), and a **Return** receipt — recorded under your name, with the date and time — is added to the employee's handover history. The receipt also appears in the employee's portal under **Your forms**.

Software seats synced from Microsoft 365 aren't listed — they follow Microsoft 365 and are unassigned there.

## What the employee sees

1. The employee receives an email with a link to the form, or opens the portal address directly.
2. They enter their **Work email** and click **Email me a sign-in code**, then type the 6-digit **Sign-in code** from the email and click **Sign in**.
   - The code expires in 10 minutes. A new one can be requested once a minute (**Send a new code**, with a countdown).
   - The email must match the employee's email in IT Directory, and their organization must have the portal enabled.
   - If the same email belongs to employees in more than one organization or sub-organization, they choose one on a **Choose an organization** page.
3. The portal has three tabs (a bottom tab bar on phones):
   - **Overview** — a greeting and, when something is waiting, **Review & sign**; an ID-badge card with their own details (name, email, job title, department, phone, start date); totals of what they have; and shortcuts, including **View my latest signed form**. Shows your company logo when one is uploaded.
   - **My items** — **Devices**, **Software & services**, and **Domains you're responsible for** (domains the employee is set as owner of, by name only — informational, never part of a handover). Each item shows a badge: **Signed for**, **Awaiting your signature** or **Not signed yet**.
   - **Forms** — **Waiting for your signature** and **Your forms** (signed forms and return receipts, each with view and download links).
4. To sign, they open a form, check the **Items** list and **Declaration**, type their **Full name**, draw their **Signature** with a finger, pen or mouse, tick the consent checkbox, and click **Sign** ("Signed — thank you!").

If items were added to the form while they had it open, signing fails with "New items were just added to this form. Please review the updated list and sign again."

Employees only see what they have. The portal never shows costs, prices, purchase dates, warranty, renewal or expiry dates, license keys, or IT's notes, and expired software isn't listed.

## What's recorded on a signed form

Each signed form keeps a frozen copy of the item list and the declaration text as they were when signed, plus:
- the drawn signature image and the typed full name
- the email address they signed in with, and how it was verified (a one-time code sent to that email)
- the date and time, IP address and browser
- a document hash (SHA-256) over the form's contents

The PDF shows the items, the declaration, the signature with name and date, and an **Electronic signature record** (signed at, signed as, verified by, method, IP address, document hash). Return receipts show **Received by** and an **Electronic receipt record** instead. Your company logo is printed at the top right — see [General settings](../administration/general-settings.md).

This is a simple electronic signature backed by that audit record; no third-party signing service is involved.

## Daily reminders for unsigned forms

Every request still waiting for a signature is emailed to the employee again about once a day, until it is signed or cancelled. This applies to manual and automatic requests alike, runs only while the portal is enabled, and is separate from the [expiry reminders](../reports-and-reminders/reminders.md) (it goes to the employee, not your reminder recipients, and needs no setup).

## Notes

- If the employee portal isn't set up on your installation, the settings page says so ("The employee portal isn't set up on this installation…") and the Handover section and list columns don't appear.
- Settings apply to the root organization and all its sub-organizations.
- Turning the portal off hides the Handover section and columns and stops sign-ins and reminders, but doesn't delete any requests or signed forms; turning it back on brings them back.
- Deleting an employee also deletes their handover requests, signed forms and return receipts. Download any PDFs you need to keep first.
- Portal sign-ins last up to 2 hours.
- Requesting signatures and re-sending emails are limited to 100 per user per hour.
