# Adding a VLAN

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Network** (`/network`). It opens on the **VLANs** tab.
2. Click **Add VLAN** (at the end of the search row). The **Add VLAN** form opens in a pane on the right.
   - Shortcut from any page: click **Add asset** in the top bar and choose **VLAN**.
3. Fill in the form:

   **VLAN details**
   - **Sub-Organization** — required; shown only if your account has access to more than one org.
   - **VLAN ID** — required, a number from 1 to 4094.
   - **Name** — required, e.g. `Corporate`.
   - **Status** — **Active**, **Reserved**, or **Deprecated**. Defaults to Active.

   **Network**
   - **Subnet** — optional. Enter the network address one octet at a time (four boxes), then the CIDR prefix after the `/`. The prefix defaults to `/24`; e.g. `10.0.100.0` / `24`.
   - **Gateway** — optional. Auto-fills to the subnet's first usable address (e.g. `10.0.100.1` for `10.0.100.0/24`) as soon as you finish entering a valid subnet — edit it by hand if your router uses a different address. Once you've typed into it yourself, it stops auto-filling even if you change the subnet again.
   - **Location / Department** — optional free text, e.g. `HQ - 3rd Floor / Finance`.
   - **DHCP Server** — switch on if this VLAN has a DHCP server. When on, an address field for the DHCP server appears below the switch and is required to save; it auto-fills from the subnet the same way Gateway does (most routers serve both roles), and can also be edited independently.

   **Notes**
   - **Description** — optional free text.

4. Click **Add VLAN** to save (the **Cancel** and **Add VLAN** buttons stay pinned at the bottom of the pane). A "VLAN added" message confirms it.

### Entering IP addresses quickly

Subnet, Gateway, and the DHCP server address all use the same octet-box input: after three digits, or when you type `.`, it moves to the next box automatically, and moving into a box selects its value so you can immediately overtype it. You can also paste a full address (or full CIDR, for Subnet) into any box and it fills in across all the boxes.

### Reusing a VLAN ID

The same VLAN ID is often reused across different sites (e.g. VLAN 10 at both HQ and a branch office) — this is allowed, whether the reuse is in the same organization or a different one. If the ID you entered is already used in this organization, its parent, or one of its sub-organizations, a heads-up banner appears just above the **Cancel** / **Add VLAN** buttons so you can double check it's intentional and not a typo. It's purely informational and never blocks saving.

## Finding VLANs

- Use the search bar ("Search by name, subnet, location…").
- Click a column header to sort; use the column visibility menu to show or hide columns (including Gateway and DHCP). The table paginates at 25 rows per page.
- Click a row to open its details in the right-hand pane, including Gateway, DHCP Server, and the description. Click outside it, press `Esc` or click **×** to close it.
- To jump straight to a VLAN from anywhere, use the search box in the top bar (or press ⌘K / Ctrl K) and pick it — its details pane opens.

## Editing and deleting

- To edit a VLAN, click the pencil icon on its row, or **Edit** in the details pane, and update the same form. **Save Changes** saves; if you started from the details pane, you return to the updated details, and **Cancel** returns to them without saving.
- An add or edit form doesn't close when you click outside it — use **Cancel**, **×** or `Esc`.
- To delete a VLAN, click the trash icon on its row (or **Delete** in the details pane), then confirm in the **Delete VLAN** dialog.

## Notes

- When the list is completely empty (no search), it shows an **Add VLAN** button.
- VLANs aren't linked to hardware items yet — the registry is standalone for now.
- No connector currently imports VLANs automatically; they're entered by hand.
- Adding a VLAN counts against your organization's pooled asset limit — see [Viewing plan & billing status](../administration/billing.md).
