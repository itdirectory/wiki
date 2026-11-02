# Release Notes

## 1.8.0

November 2, 2026

### What's New

#### Microsoft 365 licenses, synced automatically
- Connect Microsoft 365 under Settings → Integrations to bring in every license your company subscribes to, with no manual entry.
- Each license shows how many seats you've bought and which employees hold one, matched to your employees automatically.
- Turn on daily sync to keep seat counts and holders up to date as people join, leave or change licenses.
- If you have sub-organizations, each one sees only the seats held by its own employees, and the totals still add up to what you've purchased.
- Synced licenses are marked with a Microsoft 365 badge. Their seats and names follow Microsoft 365, but you can still add your own cost, renewal date, owner and notes.
- Disconnect at any time to turn synced licenses back into regular items you can edit freely, keeping their current seat holders.

#### Hide synced licenses you don't need to track
- Hide a synced license, such as a free plan, from its row or from its details panel.
- Hidden licenses drop out of your software list, counts, the Overview page, search, reports and reminders, and they don't count toward your plan's item limit.
- Employees who hold a hidden license still see it in their own items, and it still appears on their page, marked "Hidden".
- Use "show hidden licenses" under the software list to see them again and unhide any of them.

#### Invite new users by email
- Adding a user under Settings → Users now sends them an invitation email, so you no longer choose and share a temporary password.
- They open the link and set their own password. If your company uses Microsoft sign-in, they can sign in with Microsoft instead.
- The users list shows who is still invited and whose invitation has expired.
- Resend an invitation with one click if it got lost or expired.

#### A more clickable Overview page
- Click the totals on the Hardware, Software & services and Domains cards to open the full list.
- Click any line under a card, such as "In repair", "Expiring soon" or "Needs attention", to open the list showing exactly those items.
- Click an integration in the Integrations card to open the list it keeps up to date.

#### New list filters
- Software & services: a new Renewal option shows items that aren't due in the next 30 days.
- Domains: new Issue options show domains with any issue, with an expired certificate, or with no issues.

#### License keys are optional
- You can now add a license without entering its key.

### Bug Fixes

#### Finding employees when assigning items
- In organizations with many employees, some people didn't appear while typing in the employee picker. Search now finds every employee.
- Items assigned to one of those employees now show their name instead of an empty field.

#### No more bouncing between pages after sign-in
- A newly added user who had to both confirm their email and change their password could get stuck going back and forth between the two pages. They're now taken through one step at a time.

#### Stronger account security
- Changing or resetting your password now signs you out everywhere, including on other devices.
- Password reset and email confirmation links are removed from the address bar as soon as the page opens, so they don't stay in your browser history.
- If an invitation email fails to resend, the link the person already has keeps working.
- Repeated password reset requests for the same email address are now limited, to prevent inbox flooding.

---

## 1.7.0

October 31, 2026

### What's New

#### Employee portal and digital handover forms
- Employees can now sign in to their own portal with their work email, using a one-time code sent to their inbox. No password needed.
- In the portal, employees see the devices (and, optionally, software) assigned to them, plus any domains they're responsible for.
- You can ask an employee to sign a handover form for the items they've received. They review the list and sign it by drawing their signature, right from their phone or computer.
- Signed forms become PDFs you can preview or download at any time, with a full record of who signed, when, and from where.
- When you assign new items to an employee who has signed before, a new signature request can be sent automatically.
- Employees get a daily reminder for any forms they haven't signed yet.
- When items come back, record the return from the employee's page and they are unassigned right away.
- The employees list shows each person's handover status, and you can request signatures from several employees at once.
- Turn the portal on, choose whether it covers software too, and edit the declaration text under Settings → Employee portal.

#### Your company logo
- Upload your company logo under Settings → General.
- It appears on handover forms and in the employee portal.

#### A redesigned Overview page
- A banner at the top tells you at a glance how many items need attention and why.
- Summary cards show your hardware, software and domains by status, each with a link to the full list.
- A new "Expirations & issues" panel shows expired or expiring warranties, overdue or upcoming renewals, software close to its seat limit, and domain and certificate problems. Click any of them to jump straight to exactly those items.
- Quick actions let you add an item, import a spreadsheet, onboard an employee or run a report in one click.
- See the sync status of your integrations, and your plan usage, without leaving the page.
- Export the full list of items that need attention as a spreadsheet.

#### New, richer reports
- Six new reports: software spend, upcoming renewals and their cost, license usage, hardware lifecycle, cost per department, and a statement of everything assigned to a single employee.
- Each report has its own page with a summary, charts and sortable tables.
- Adjust reports with simple options, such as the renewal window or how old a device must be before it's due for replacement.
- Export any report as a spreadsheet, email it, or print it.

#### Filters on every list
- Hardware, Software & services, Domains and Employees now have filter dropdowns next to the search box, such as status, warranty, vendor, brand, renewal, department or owner.
- Combine as many filters as you like, and clear them all with one click.

#### Item details open in a side panel
- Viewing, adding or editing an item now opens in a panel on the right, so the list stays in view behind it.
- Forms are organized into clear sections, and the Save and Cancel buttons always stay visible.
- Forms you're filling in won't close if you click outside them by accident.

#### Prices in your currency
- Hardware purchase prices and software costs can now be entered in US dollars, euros or Israeli shekels, item by item.
- Reports show totals per currency.

#### Domain owners
- Assign a responsible employee to each domain.
- See and filter by owner in the domains list, and import owners from a spreadsheet.
- An employee's page lists the domains they own.

#### Email sign-in codes for extra security
- Signing in with a password now takes a second step: a 6-digit code sent to your email.
- Tick "Trust this browser" to skip the code on that device for 30 days. Changing your password signs out every trusted browser.
- Signing in with Microsoft single sign-on works as before.

#### A fresh look for navigation
- A new top bar with quick search, announcements, and an "Add asset" menu that's available from any page.
- The sidebar is now grouped into Inventory and Workspace and shows how many items each section holds.
- Your selected company is remembered between visits.
- Settings are organized into clear groups: Organization, Access and Features.

#### A simpler integrations page
- All integrations appear in a single gallery, each showing whether it's connected, when it last synced, and whether the last sync failed.
- Run a sync right from the gallery or from the Overview page.

#### Smarter expiry reminders
- Reminders now follow up as the date gets closer (a week before and a day before) and once more the day after something expires.
- Reminders cover items across all of your sub-companies.

### Bug Fixes

#### More reliable subdomain discovery
- Fixed an issue where subdomains of your domains could stop being discovered. Discovery now also uses more than one source, so it keeps working if one is unavailable.

#### Links to a specific item always open it
- Picking a result from search, or following a link from the Overview, now opens the right item even if you're already on that list page.

---

## 1.6.0

August 27, 2026

### What's New

#### A new Network section — VLANs and Public IPs
- A new Network item in the sidebar, with two tabs: **VLANs** — a registry of your network VLANs (ID, name, subnet, gateway, DHCP server, physical location, and status) — and **Public IPs** — a registry of your allocated public IP addresses (address, provider, description, and status).
- Adding a VLAN's subnet auto-fills sensible defaults for its Gateway and DHCP Server IP, which you can still edit by hand.

#### Dark mode
- The app now supports a dark theme. Switch between Light, Dark, or System from the user menu in the sidebar — your choice is remembered on your device.

### Bug Fixes

#### Items stay where you put them
- Fixed a bug in certain multi-company setups where a newly added item could be saved to a company your account doesn't have visibility into, making it seem to disappear right after you created it.

#### Better screen reader support
- Icon-only buttons across the app — like edit, delete, and copy — now have proper labels, so screen readers can correctly announce what each one does.

---

## 1.5.0

August 18, 2026

### What's New

#### Simpler, safer report recipient management
- Admins can now approve extra email addresses allowed to receive emailed reports, right from Settings → Security.
- Anyone on your own team, or a colleague at the same company, can already receive reports with no extra setup — the new approval list is only needed for outside parties, like an auditor or partner.

#### Security settings, all in one place
- Single sign-on setup, user invitations, and report recipient approvals now live together on one Security settings page, organized into simple tabs.
- The old sign-on settings page automatically redirects here, so any saved links still work.

#### Easier multi-email entry
- Adding several email addresses — for report recipients or reminder notifications — now uses a simple tag-style input: type an address and press enter, paste in a whole list at once, or remove one with a click.

#### Extra confirmation before deleting an organization
- Deleting a sub-organization, or your account's own organization, now asks you to type its name to confirm — an extra safeguard against accidentally deleting the wrong one.

### Bug Fixes

#### Assignments now stay with the right company
- Moving a hardware item or a license/subscription to a different company no longer leaves it assigned to an employee (or seat holder) from its old company.
- Bulk-importing hardware or software now correctly skips an "assigned to" match if that person belongs to a different company, instead of assigning it incorrectly.

#### More reliable connector syncs
- Syncing devices, employees, or domains from a connected service now keeps going even if a few individual items fail, and clearly reports how many succeeded, failed, or were skipped.
- Device and employee syncs no longer leave an assignment pointing at the wrong company when their group mappings disagree.

#### Cleaner emailed reports
- Fixed an issue where certain characters in report details could occasionally break the formatting of an emailed report.

### Heads Up

#### Bulk import now accepts CSV files only
- Uploading a spreadsheet for bulk import now supports CSV files only — Excel (.xlsx/.xls) files are no longer accepted. Export your spreadsheet to CSV before importing.
- Import files are also now limited to 5MB and 20,000 rows to keep large imports reliable.

#### A few actions are now rate-limited
- To protect against abuse, actions like signing in, signing up, searching, and sending reports are now limited to a reasonable number of attempts per hour. If you hit the limit, just wait a bit before trying again.

---

## 1.4.0

August 1, 2026

### What's New

#### Bulk import from a spreadsheet
- Add multiple hardware items, employees, software & services, or domains at once by uploading a spreadsheet, instead of entering them one at a time.
- The import guides you through matching your file's columns to the right fields.
- See a preview of your data before anything is saved, and get a report of exactly which rows were added and which need a fix.
- A downloadable template with example data and guidance on accepted values makes it quick to get started.

#### Sort and customize your lists
- Sort any item list by clicking a column heading.
- Choose which columns are shown using the new "Columns" button next to each list.
- Your column choices are remembered the next time you visit.

### Bug Fixes

#### Cursor and toolbar polish
- Buttons and links throughout the app now consistently show a pointer cursor on hover.
- A few toolbar controls were resized so they line up properly with nearby search and filter fields.

---

## 1.3.0

July 29, 2026

### What's New

- A new notification banner keeps you and your team in the loop about upcoming maintenance, downtime, or new features. Messages are color-coded by urgency and can include bold text and clickable links. Each person can dismiss a message on their own — once you've seen it, it won't keep showing up for you, but teammates who haven't seen it yet still will.
- Redesigned the forms for adding and editing hardware, software & services, domains, and employees: fields are now grouped into clear, labeled sections, and the Save/Cancel buttons stay visible at the bottom of the window so you don't have to scroll to find them.
- Clearer labeling in the organization switcher ("All Organizations" instead of "All Sub-Organizations").
- The signup page now links to our Terms of Use and Privacy Policy.
