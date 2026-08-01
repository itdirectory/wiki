# Setting up connectors (Cloudflare, Microsoft Intune, Microsoft Entra ID)

**Who can do this:** Org Admin only.

Connectors automatically import data from outside services — Cloudflare domains, Intune-managed devices, or Entra ID employees — instead of adding those items by hand.

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
10. Click **Sync Now** to import immediately, or **Save** to just store the config. **Uninstall** (red, bottom left) removes the saved token entirely.

## Microsoft Intune (import devices as hardware)

11. Click **Install**/**Configure** on the Microsoft Intune card.
12. This connector reuses your organization's Entra ID credentials — if you haven't configured those yet, you'll see a prompt to go to **Settings → SSO — Entra ID** first (see https://docs.itdirectory.app/how-to/security/sso-setup). Come back here afterward.
13. Once configured, the dialog shows a notice that this requires the `DeviceManagementManagedDevices.Read.All` application permission with admin consent in Azure.
14. Turn on **"Auto-sync daily"** if desired (saves immediately).
15. If you have sub-organizations, use the **Per-Company Device Group Routing** box to map an Entra security group name to a specific sub-org — devices in that group are routed there ahead of the device's enrolled-user company.
16. Click **Sync Now**. A summary shows "{added} added, {updated} updated, {skipped} skipped".

## Microsoft Entra ID (import employees)

17. Click **Install**/**Configure** on the Microsoft Entra ID card. Same reuse-SSO-credentials behavior as Intune above.
18. Optionally set a **Group (optional)** name to limit the sync to one security group — leave blank to sync all tenant users.
19. Turn on **"Auto-sync daily"** if desired.
20. If you have sub-organizations, use the **Per-Company Group Routing** box the same way as devices — users in a mapped group go to that sub-org, everyone else goes to the root org.
21. Note the required permissions notice (`User.Read.All`, plus `Group.Read.All`/`GroupMember.Read.All` once any group name is set).
22. Click **Sync Now**. A summary shows "{added} added, {updated} updated, {skipped} skipped" plus a per-company breakdown.

## Notes

- Employees and devices sync independently even though they share one Entra ID connection — you can enable one without the other.
- None of these connectors run continuously — "Auto-sync daily" is handled by a separate background worker that runs once a day; "Sync Now" runs one sync immediately.
