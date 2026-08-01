# Adding a domain

**Who can do this:** Any authenticated user with access to the target sub-organization.

## Steps

1. In the left sidebar, click **Domains** (`/domains`).
2. Click **Add Domain** (top right, next to **Import**).
3. Fill in the **Add Domain** form:

   **Domain Details**
   - **Sub-Organization** — required if your account has access to more than one org.
   - **Domain** — required, e.g. `example.com`, `sub.example.com`, or a wildcard like `*.example.com`.

   **Notes**
   - **Notes** — optional free text.

4. Click **Add Domain** to save. WHOIS/DNS/SSL details are populated automatically shortly after (by a background process), not entered by hand.

## Finding domains

- Use the search bar ("Search by name, registrar…"). The table paginates at 25 rows per page.
- To edit a domain, open its row and update the same form — note that changing the domain name itself triggers a fresh WHOIS/DNS/SSL check. The submit button reads **Save Changes**.

## Notes

- Domains can also be imported automatically from Cloudflare — see https://docs.itdirectory.app/how-to/connectors/connectors.
- Adding a domain counts against your organization's pooled asset limit — see https://docs.itdirectory.app/how-to/settings/billing.
