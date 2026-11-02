# Adding a Public IP

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Network** (`/network`), then switch to the **Public IPs** tab.
2. Click **Add Public IP** (at the end of the search row). The **Add public IP** form opens in a pane on the right.
   - Shortcut from any page: click **Add asset** in the top bar and choose **Public IP**.
3. Fill in the form:

   **Details**
   - **Sub-Organization** — required; shown only if your account has access to more than one org.
   - **IP Address** — required. Enter it one octet at a time (four boxes); after three digits, or when you type `.`, it moves to the next box automatically, and you can paste a full address into any box.
   - **Provider** — optional free text, e.g. `AWS`, `Cloudflare`.
   - **Status** — **Active**, **Reserved**, or **Deprecated**. Defaults to Active.

   **Notes**
   - **Description** — optional free text, e.g. what the address is used for.

4. Click **Add Public IP** to save (the **Cancel** and **Add Public IP** buttons stay pinned at the bottom of the pane). A "Public IP added" message confirms it.

### Duplicate addresses

Unlike a VLAN ID, a public IP is a real, individually-allocated resource — the same address can't be entered twice within the same organization. If you try, you'll see "This IP address is already registered in this organization." and the record isn't saved (the form stays open so you can correct it). The same address *can* be reused across two different organizations (e.g. separate sub-orgs each documenting their side of a shared address), since each org's registry is independent.

## Finding Public IPs

- Use the search bar ("Search by IP, provider…") — it also matches the description.
- Click a column header to sort; use the column visibility menu to show or hide columns. The table paginates at 25 rows per page.
- Click a row to open its details in the right-hand pane, including the description. Click outside it, press `Esc` or click **×** to close it.
- To jump straight to a public IP from anywhere, use the search box in the top bar (or press ⌘K / Ctrl K) and pick it — its details pane opens.

## Editing and deleting

- To edit a Public IP, click the pencil icon on its row, or **Edit** in the details pane, and update the same form. **Save Changes** saves; if you started from the details pane, you return to the updated details, and **Cancel** returns to them without saving.
- An add or edit form doesn't close when you click outside it — use **Cancel**, **×** or `Esc`.
- To delete a Public IP, click the trash icon on its row (or **Delete** in the details pane), then confirm in the **Delete Public IP** dialog.

## Notes

- When the list is completely empty (no search), it shows an **Add Public IP** button.
- Public IPs aren't linked to hardware or domain records yet — the registry is standalone for now.
- No connector currently imports public IPs automatically; they're entered by hand.
- Adding a Public IP counts against your organization's pooled asset limit — see [Viewing plan & billing status](../administration/billing.md).
