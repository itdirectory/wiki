# Adding a Public IP

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Network** (`/network`), then switch to the **Public IPs** tab.
2. Click **Add Public IP** (in the filters row).
3. Fill in the **Add Public IP** form:

   **Details**
   - **Sub-Organization** — required if your account has access to more than one org.
   - **IP Address** — required. Enter it one octet at a time (four boxes); typing advances to the next box automatically, and you can paste a full address into the first box.
   - **Provider** — optional free text, e.g. `AWS`, `Cloudflare`.
   - **Status** — **Active**, **Reserved**, or **Deprecated**. Defaults to Active.

   **Notes**
   - **Description** — optional free text, e.g. what the address is used for.

4. Click **Add Public IP** to save.

### Duplicate addresses

Unlike a VLAN ID, a public IP is a real, individually-allocated resource — the same address can't be entered twice within the same organization. If you try, the form shows an error and the record isn't saved. The same address *can* be reused across two different organizations (e.g. separate sub-orgs each documenting their side of a shared address), since each org's registry is independent.

## Finding Public IPs

- Use the search bar to search by IP address, provider, or description.
- Click a column header to sort; use the column visibility menu to show or hide columns. The table paginates at 25 rows per page.
- Click a row to view its full details, including the description.

## Editing and deleting

- To edit a Public IP, click the pencil icon on its row (or **Edit** from the view dialog) and update the same form. The submit button reads **Save Changes**.
- To delete a Public IP, click the trash icon on its row (or **Delete** from the view dialog), then confirm in the dialog that appears.

## Notes

- Public IPs aren't linked to hardware or domain records yet — the registry is standalone for now.
- No connector currently imports public IPs automatically; they're entered by hand.
- Adding a Public IP counts against your organization's pooled asset limit — see https://docs.itdirectory.app/how-to/billing.
