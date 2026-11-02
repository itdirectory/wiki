# Using the Overview page

**Who can do this:** Any signed-in user. The **Integrations** and **Plan usage** cards are shown to Org Admins only.

The Overview page (`/dashboard`) is the first page after sign-in. It summarizes your inventory, flags what's expired or about to expire, and links straight to the matching items.

## Getting around the app

- **Sidebar** (left):
  - **Inventory**: **Overview**, **Hardware**, **Software & services**, **Domains**, **Network**. Hardware, Software & services and Domains show how many items they hold.
  - **Workspace**: **Employees**, **Reports**, and **Settings** (Org Admins only).
  - At the bottom, your user menu has **My Account**, **Theme** and **Sign out**.
- **Company selector**: if your organization has sub-organizations, a selector at the top of the sidebar picks one company or **All organizations**. Every list, the Overview page and the reports follow this choice. It's remembered the next time you visit.
- **Top bar**:
  - **Search assets, people, domains…** opens quick search. You can also open it with **⌘K** (Mac) or **Ctrl K** (Windows).
  - The **bell** opens **Announcements** from the IT Directory team. A red dot means some are unread.
  - **Add asset** opens a menu: **Hardware**, **Software or service**, **Domain**, **Employee**, **VLAN**, **Public IP**. Each choice goes to that list and opens its add form.

## The page header

1. The line above the **Overview** title shows the date. With sub-organizations, it also shows which company you're viewing (or **All organizations**).
2. **Export report** downloads a CSV file (`needs-attention-<date>.csv`) listing each item that needs attention, with the columns **Item**, **Detail**, **Type**, **Assigned to**, **Status**, **Days left**:
   - **Type** is one of: Warranty, Renewal, Seats, Domain, SSL certificate.
   - **Assigned to** is the employee a device is assigned to, or the owner of a software item or domain. If nobody is set, it shows "Unassigned".
   - **Status** is "Expired", "Today", "In Nd", "N% used" (for seats) or "Error" (for a failed domain check).
   - It uses the same 30-day window as the **Expirations & issues** tiles and covers the company currently selected.

## Attention banner

If anything in **Expirations & issues** has a count, a dark banner at the top shows "**N items need your attention**". Below it is a summary such as "1 domain is failing DNS checks, 3 warranties have expired and 2 integrations have stopped syncing". Only the parts that apply are shown.

Click **Review now** to scroll down to the **Expirations & issues** panel.

## Summary cards

There are three cards: **Hardware**, **Software & services** and **Domains**. Each one shows:

- **A total**: the number of devices, a breakdown such as "3 licenses · 6 SaaS · 2 services", or the number of monitored domains. Click it, or the ↗ icon in the card's corner, to open the full list.
- **A colored bar and a legend.** Click any line in the legend to open the list showing exactly the items it counts:

| Card | Legend lines |
|---|---|
| **Hardware** | **Active**, **Storage**, **In repair**, **Retired**, **Disposed**: the hardware list filtered to that status. A status with no devices isn't listed. |
| **Software & services** | **Active** (no renewal date, or not due in the next 30 days), **Expiring soon** (due within 30 days), **Expired**: the list's **Renewal** filter set to the matching option |
| **Domains** | **Healthy** (checked, no errors, domain and certificate not expiring within 30 days), **Needs attention** (a failed check, or the domain or its certificate expires within 30 days or has already expired), **Certificates expired**: the list's **Issue** filter set to **No issues**, **Any issue** or **Certificate expired** |

Domains that haven't been checked yet appear as a grey part of the bar, but not in the legend. **Certificates expired** overlaps **Needs attention**, so it appears in the legend only and isn't drawn in the bar.

If a card has nothing yet (for example "No hardware yet"), it shows an **Add** button instead. The button opens that list's add form.

## Quick actions

The fourth card, **Quick actions**, has:

- **Add asset**: the same menu as in the top bar.
- **Import CSV**: choose **Hardware**, **Employees**, **Software & services** or **Domains** to open that list's bulk-import dialog.
- **Onboard employee**: opens the add form on the Employees page.
- **Run a report**: goes to [Reports](../reports-and-reminders/reports.md).

## Expirations & issues

This panel has eight tiles. Each tile shows a count, and clicking it opens the list filtered to exactly those items. "Expiring" means within the next **30 days**.

| Tile | Counts | Opens |
|---|---|---|
| **Warranties expired** | Hardware whose warranty has ended | Hardware, **Warranty: Expired** |
| **Warranties expiring** | Hardware warranties ending in the next 30 days | Hardware, **Warranty: Expiring (30d)** |
| **Renewals overdue** | Software & services past their renewal or expiry date | Software & services, **Renewal: Expired / overdue** |
| **Renewals due** | Software & services renewing in the next 30 days | Software & services, **Renewal: Due in 30d** |
| **Seats near limit** | Licenses and subscriptions with **80% or more** of their seats assigned | Software & services, **Seats: ≥ 80% used** |
| **Domains expiring** | Domains whose registration expires within 30 days, including already expired | Domains, **Issue: Registration expiring (30d)** |
| **Certificates expiring** | SSL certificates expiring within 30 days, including already expired | Domains, **Issue: Certificate expiring (30d)** |
| **Domain check failures** | Domains whose last DNS / RDAP / TLS check failed | Domains, **Issue: Check failed** |

A tile turns red or amber when its count is above zero. When you open a list from a tile, its search and other filters are cleared, so the list shows exactly the counted items. The filter is applied through the list's own filter dropdowns, so you can change or clear it there.

## Integrations (Org Admins only)

The **Integrations** card lists the connectors your organization has set up. **Microsoft 365 licenses** appears only after it has synced at least once or has daily sync turned on. Each row shows the connector's logo, name and status:

- **Synced** *time ago*: the last sync succeeded within the last 48 hours.
- **Stale · last sync** *time ago*: the last sync was more than 48 hours ago.
- **Never synced**
- **Sync failed**: the last sync returned an error.
- **Not enabled**

Click a row to open the list that connector fills: Cloudflare → Domains, Microsoft Entra ID → Employees, Microsoft Intune → Hardware, Microsoft 365 licenses → Software & services. Click the **↻** button to sync it now. The cards refresh afterwards, even when the sync fails. **Manage** goes to the integrations page. If no connector is set up, the card shows **Set one up**. See [Setting up connectors](../administration/connectors.md).

## Plan usage (Org Admins only)

The **Plan usage** card shows your plan (**Trial** with the days left, **Paid** or **Suspended**) and usage bars for **Assets**. If you have sub-organizations, or your plan includes them, it also shows a bar for **Sub-organizations**. A bar turns amber at 80% and red when full. Click the card to open the billing page. See [Viewing plan & billing status](../administration/billing.md).

## Notes

- Everything on the page follows the sidebar's company selector, except **Plan usage**, which always shows your whole organization because the limits are shared across all companies.
- Microsoft 365 licenses you've hidden aren't counted anywhere on this page.
- Counts reflect the moment the page loaded. Reload the page, or switch companies, to refresh them.
- The banner's "integrations have stopped syncing" part counts only enabled integrations whose last sync failed.
