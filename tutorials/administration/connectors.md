# Setting up connectors (Cloudflare, Microsoft Entra ID, Microsoft Intune, Microsoft 365 licenses)

**Who can do this:** Org Admin only.

Connectors automatically import data from outside services — Cloudflare domains, Entra ID employees, Intune-managed devices, or Microsoft 365 licenses — instead of adding those items by hand.

## Getting to the Integrations gallery

1. In the left sidebar, click **Settings**, then **Integrations** under **Features** in the settings menu (`/settings/connectors`, subtitled "Bring assets in automatically from the services you already use").
2. You'll see one card per connector. Each card shows the logo and name, a link to where its records land (→ Domains / Employees / Hardware / Software & services), a short description, and a status line: **Not connected**, **Not enabled**, **Never synced**, **Sync failed**, **Stale · last sync {x}** (no sync for more than 2 days) or **Synced {x}**, plus "· Auto-sync daily" when that's on.
3. A connector that isn't set up has a **Connect** button. One that is set up has **Configure** and a ↻ button (**Sync now**) that syncs it right away; the status line updates when it finishes, even if the sync failed.

## Cloudflare (import domains)

1. Click **Connect**/**Configure** on the Cloudflare card.
2. In Cloudflare, go to **My Profile → API Tokens** and create a token with **Zone:Read** and **DNS:Read** permissions (DNS:Read is needed to discover subdomains).
3. Paste the token into the **API token** field in the **Connection** section (eye icon to show/hide). Once saved, the field shows "(saved — enter to replace)"; type a new token only to replace it.
4. In the **Sync** section, turn on **Enable this connector** (available once a token is entered).
5. Optionally turn on **Auto-sync daily** so new zones import once a day (available once the connector is enabled).
6. Click **Save** ("Cloudflare configuration saved"). These settings only take effect when you click Save.
7. With a saved token and the connector enabled, a **Sync now** button appears in the **Sync** section. Click it to import right away. The result shows "{added} added, {updated} updated, {skipped} skipped", plus how many zone errors or DNS issues occurred, if any (e.g. the token is missing DNS:Read). The toast also mentions how many subdomains were discovered. New domains stop being added once your organization reaches its plan's item limit (counted as skipped, not a separate error) — see [Viewing plan & billing status](billing.md).
8. **Uninstall** (bottom left) removes the saved token entirely.

## Microsoft Entra ID (import employees)

1. Click **Connect**/**Configure** on the Microsoft Entra ID card.
2. This connector reuses your organization's Entra ID credentials. If you haven't configured those yet, you'll see "Connect Microsoft Entra ID first" and a **Set up single sign-on** button that takes you to **Settings → Single sign-on** (see [Security settings](security-settings.md)). Come back here afterward.
3. In the **Source** section, optionally enter a **Group (optional)** name to limit the sync to one security group, and click **Save** next to it. Leave it empty to sync every user in the tenant.
4. If you have sub-organizations, use the **Company routing** section to map an Entra group name to each sub-org (click **Save** on its row). Users in a company's group go to that company; everyone else goes to the root organization.
5. In the **Sync** section, turn on **Auto-sync daily** if desired (saves immediately).
6. Check the permissions note at the bottom of the **Sync** section: `User.Read.All` always; `Group.Read.All` and `GroupMember.Read.All` as well, once you've set a sync group or any company routing.
7. Click **Sync now**. The result shows "{added} added, {updated} updated, {skipped} skipped", plus an error count if any users failed to sync, and a per-company breakdown below it. A company whose mapped group couldn't be found in Entra shows "group not found" instead of counts — that's different from the **Group (optional)** name not being found at all, which stops the whole sync with "Group not found. Check the group name in SSO settings." New employees stop being added once your organization reaches its plan's item limit (counted as skipped, not a separate error).

## Microsoft Intune (import devices as hardware)

1. Click **Connect**/**Configure** on the Microsoft Intune card. It uses the same Entra ID credentials — if they aren't configured yet, you'll see the same **Set up single sign-on** button.
2. If you have sub-organizations, use the **Company routing** section to map an Entra group name to each sub-org. Devices in a company's group go to that company, ahead of the enrolled user's company; others follow their assigned employee, or go to the root organization.
3. In the **Sync** section, turn on **Auto-sync daily** if desired (saves immediately).
4. The permissions note lists `DeviceManagementManagedDevices.Read.All` (application permission, with admin consent in Azure).
5. Click **Sync now**. The result shows "{added} added, {updated} updated, {skipped} skipped", plus an error count if any devices failed to sync. New devices stop being added once your organization reaches its plan's item limit (counted as skipped, not a separate error).

## Microsoft 365 licenses (import licenses and seat holders)

1. Click **Connect**/**Configure** on the **Microsoft 365 licenses** card. It uses the same Entra ID credentials — if they aren't configured yet, you'll see the same **Set up single sign-on** button.
2. In Azure, grant the app registration the `Organization.Read.All` and `User.Read.All` application permissions, with admin consent (listed in the dialog's permissions note).
3. Run the Microsoft Entra ID employee sync first (above), so license holders can be matched to employees.
4. There's no separate enable switch — the connector is ready once Entra ID is set up. Optionally turn on **Auto-sync daily** to refresh licenses and seat assignments once a day (saves immediately).
5. Click **Sync now**. The result reads "Sync complete — {n} license(s), {x} seat(s) assigned, {y} removed", plus "{z} user(s) not matched to an employee" when some holders couldn't be matched. The dialog then shows "Last synced {date}".
6. Open **Software & services** to see the imported licenses — each is a SaaS item with a **Microsoft 365** badge. See [Microsoft 365 licenses](../inventory/adding-software-services.md#microsoft-365-licenses) for what you can and can't edit, and how to hide licenses you don't need.

**What the sync does**

- Each Microsoft 365 subscription becomes a SaaS item (vendor Microsoft) with a readable name. Each user's assigned licenses become seats for the matching employee — matched by their Entra ID first (employees imported by the Entra ID sync), then by email. Users with no matching employee are counted but not assigned a seat.
- Seats follow Azure exactly: assignments added or removed in Azure are added or removed here on the next sync, and the assigned count is always the real number.
- Your own cost, billing, dates, owner and notes are never overwritten.
- With sub-organizations, each sub-org gets its own copy of a license holding only its own employees' seats; the root organization's copy holds the remaining purchased units. Total seats across all copies add up to what you've purchased.
- A subscription that disappears from Microsoft 365 is unlinked: its synced seats are dropped and it becomes a regular, editable item.
- New license items stop being added once your organization reaches its plan's item limit (counted as skipped). Hidden licenses don't count toward the limit.

**Disconnecting**

- After the first sync, a **Disconnect** section appears. Click **Disconnect & unlock records**, then **Disconnect** to confirm ("Unlock all synced licenses?"). Syncing stops, and imported licenses and their seats stay, becoming editable like any other item. The toast reads "Disconnected — {n} license record(s) are now editable".

## Notes

- Employees, devices and licenses sync independently even though they share one Entra ID connection — you can turn auto-sync on for one without the others.
- Connectors don't run continuously — "Auto-sync daily" is handled by a background worker that syncs each connector about once a day; **Sync now** runs one sync immediately.
- You can also run a sync from the Integrations card on the Overview page — see [Overview dashboard](../getting-started/overview-dashboard.md).
- If a sync is interrupted by a slow or unresponsive connection to the outside service, it times out rather than hanging — run **Sync now** again.
- If a Microsoft sync fails for missing permissions, the error names the permission to grant in Azure (e.g. "Missing Organization.Read.All and User.Read.All permission. Grant admin consent in Azure Portal.").
