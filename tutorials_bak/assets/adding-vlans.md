# Adding a VLAN

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Network** (`/network`). It opens on the **VLANs** tab.
2. Click **Add VLAN** (in the filters row).
3. Fill in the **Add VLAN** form:

   **VLAN Details**
   - **Sub-Organization** — required if your account has access to more than one org.
   - **VLAN ID** — required, a number from 1 to 4094.
   - **Name** — required, e.g. `Corporate`.
   - **Status** — **Active**, **Reserved**, or **Deprecated**. Defaults to Active.

   **Network**
   - **Subnet** — optional. Enter the network address one octet at a time (four boxes), then the network size after the `/`. The network size defaults to `/24`; e.g. `10.0.100.0` / `24`.
   - **Gateway** — optional. Auto-fills to the subnet's first usable address (e.g. `10.0.100.1` for `10.0.100.0/24`) as soon as you finish entering a valid subnet — edit it by hand if your router uses a different address. Once you've typed into it yourself, it stops auto-filling even if you change the subnet again.
   - **Location / Department** — optional free text, e.g. `HQ - 3rd Floor / Finance`.
   - **DHCP Server** — toggle on if this VLAN has a DHCP server. When on, a **DHCP Server IP** field appears and is required to save; it auto-fills from the subnet the same way Gateway does (most routers serve both roles), and can also be edited independently.

   **Notes**
   - **Description** — optional free text.

4. Click **Add VLAN** to save.

### Entering IP addresses quickly

Subnet, Gateway, and DHCP Server IP all use the same octet-box input: type a number and it advances to the next box automatically, and pressing `Tab` or typing `.` while a box already has a value selects that value so you can immediately overtype it instead of appending to it. You can also paste a full address (or full CIDR, for Subnet) into the first box and it'll fill in across all the boxes.

### Reusing a VLAN ID

The same VLAN ID is often reused across different sites (e.g. VLAN 10 at both HQ and a branch office) — this is allowed, whether the reuse is in the same organization or a different one. If the ID you entered is already used in this organization, its parent, or one of its sub-organizations, a heads-up banner appears above the form so you can double check it's intentional and not a typo. It's purely informational and never blocks saving.

## Finding VLANs

- Use the search bar to search by name, subnet, or location.
- Click a column header to sort; use the column visibility menu to show or hide columns (including Gateway and DHCP). The table paginates at 25 rows per page.
- Click a row to view its full details, including Gateway, DHCP Server IP, and the description.

## Editing and deleting

- To edit a VLAN, click the pencil icon on its row (or **Edit** from the view dialog) and update the same form. The submit button reads **Save Changes**.
- To delete a VLAN, click the trash icon on its row (or **Delete** from the view dialog), then confirm in the dialog that appears.

## Notes

- VLANs aren't linked to hardware items yet — the registry is standalone for now.
- No connector currently imports VLANs automatically; they're entered by hand.
- Adding a VLAN counts against your organization's pooled asset limit — see https://docs.itdirectory.app/how-to/billing.
