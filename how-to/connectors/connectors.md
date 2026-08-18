# Setting up connectors (Cloudflare, Microsoft Entra ID, Microsoft Intune)

**Who can do this:** Org Admin only.

Connectors automatically import data from outside services — Cloudflare domains, Entra ID employees, or Intune-managed devices — instead of adding those items by hand.

## Getting to the Connectors gallery

1. In the left sidebar, click **Settings**, then click the **Connectors** tab (`/settings/connectors`, subtitled "Connect your organization to various services").
2. You'll see two tabs: **Installed** (default) and **Available**.
3. On the **Available** tab, each connector card shows its name, description, and a button — **Install** (not yet set up) or **Configure** (already set up).
4. On the **Installed** tab, each row shows "Last synced {x} ago" (or "Never synced"), an **Enabled**/**Disabled** badge, a **Sync Now** button, and **Configure**.

## Cloudflare (import domains)

5. Click **Install**/**Configure** on the Cloudflare card.
6. In Cloudflare, go to **My Profile → API Tokens** and create a token with **Zone:Read** and **DNS:Read** permissions (DNS:Read is needed to discover subdomains).
7. Paste the token into the **API Token** field (eye icon to show/hide).
8. Check **"Enable this connector"**.
9. Optionally turn on **"Auto-sync daily"** so zones import automatically once a day.
10. Click **Sync Now** to import immediately, or **Save** to just store the config. The result shows "{added} added, {updated} updated, {skipped} skipped" — if any zones failed to sync or their DNS records weren't accessible (e.g. the token is missing DNS:Read), it also notes how many zone errors or DNS issues occurred. New domains stop being added once your organization reaches its plan's item limit (counted as skipped, not a separate error) — see [Viewing plan & billing status](billing.md). **Uninstall** (red, bottom left) removes the saved token entirely.

## Microsoft Entra ID (import employees)

11. Click **Install**/**Configure** on the Microsoft Entra ID card.
12. This connector reuses your organization's Entra ID credentials — if you haven't configured those yet, you'll see a prompt to go to **Settings → Security → Entra ID** first (see [Security settings](security-settings.md)). Come back here afterward.
13. Optionally set a **Group (optional)** name to limit the sync to one security group — leave blank to sync all tenant users.
14. Turn on **"Auto-sync daily"** if desired (saves immediately).
15. If you have sub-organizations, use the **Per-Company Group Routing** box to map an Entra security group name to a specific sub-org — users in a mapped group go to that sub-org, everyone else goes to the root org.
16. Note the required permissions notice: `User.Read.All` always; `Group.Read.All` and `GroupMember.Read.All` as well, once you've set a sync group name or any per-company group mapping.
17. Click **Sync Now**. A total summary shows "{added} added, {updated} updated, {skipped} skipped", plus an error count if any users failed to sync, and a per-company breakdown below it. A company whose mapped group couldn't be found on Entra shows "group not found" instead of counts for that row — that's different from the group name in the field above not being found at all, which stops the whole sync and shows an error. New employees stop being added once your organization reaches its plan's item limit (counted as skipped, not a separate error).

## Microsoft Intune (import devices as hardware)

18. Click **Install**/**Configure** on the Microsoft Intune card. Same reuse-Entra-ID-credentials behavior as above — if not configured yet, you'll see the same prompt pointing to **Settings → Security → Entra ID**.
19. Once configured, the dialog shows a notice that this requires the `DeviceManagementManagedDevices.Read.All` application permission with admin consent in Azure.
20. Turn on **"Auto-sync daily"** if desired (saves immediately).
21. If you have sub-organizations, use the **Per-Company Device Group Routing** box to map an Entra security group name to a specific sub-org — devices in that group are routed there ahead of the device's enrolled-user company.
22. Click **Sync Now**. The result shows "{added} added, {updated} updated, {skipped} skipped", plus an error count if any devices failed to sync. New devices stop being added once your organization reaches its plan's item limit (counted as skipped, not a separate error).

## Notes

- Employees and devices sync independently even though they share one Entra ID connection — you can enable one without the other.
- None of these connectors run continuously — "Auto-sync daily" is handled by a separate background worker that runs once a day; "Sync Now" runs one sync immediately.
- If a sync is interrupted by a slow or unresponsive connection to the outside service, it will time out and stop rather than hang indefinitely — re-run **Sync Now** to try again.
