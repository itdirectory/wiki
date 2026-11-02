# Running and sharing reports

**Who can do this:** Any signed-in user. Reports only include the organizations you have access to — Company Admins and Company Technicians see only the companies they've been granted.

Reports turn your inventory into spend, utilization and lifecycle summaries you can export to CSV, email or print.

## Opening a report

1. In the left sidebar, under **Workspace**, click **Reports** (`/reports`). You can also use **Run a report** on the [Overview page](../getting-started/overview-dashboard.md).
2. Reports are listed in three groups — **Financial**, **Assets** and **People**. Click one to open it (`/reports/<report>`).
3. The report page shows a header (the report title, a short description, "Generated *date* at *time*", and — with sub-organizations — which company it covers), any options for that report, a row of summary figures, charts, and one or more tables.
4. To cover a single company, pick it in the sidebar's company selector. With **All organizations** selected, the report covers every company you can access.

## The six reports

### Software spend (Financial)
What you spend on software each year, and with whom. Only software and services with a cost entered are included.
- **Summary:** **Annual run-rate**, **Monthly run-rate**, **One-time licenses** (not part of the run-rate), **Paid products**, **Vendors**.
- **Charts:** **Annual cost by vendor**, **Annual cost by kind**.
- **Tables:** **By vendor** (Products, Annual cost, One-time) and **By product** (Product, Vendor, Kind, Billing, Cost per cycle, Annual cost, Renews, Owner).
- No options.

### Renewal forecast (Financial)
What renews soon, and how much each renewal will cost. A renewal's amount is one billing cycle's cost.
- **Option:** **Window** — **Next 30 days**, **Next 90 days** (default), **Next 180 days** or **Next 12 months**.
- **Summary:** **Renewals in window**, **Amount due**, **Due in 30 days**, **Overdue**, **Overdue amount**.
- **Chart:** **Amount due by week** (30-day window) or **Amount due by month** (longer windows), with overdue items in their own bar.
- **Table:** **Renewals** — Renews, Status ("Overdue Nd", "Today", "In Nd"), Product, Vendor, Kind, Amount, Owner. Overdue items come first, then by renewal date. Items already past their date are always included as overdue, whatever the window.

### License utilization & waste (Financial)
Where you're paying for seats nobody uses. Only software with a seat count is included.
- **Summary:** **Seat utilization** (% of seats in use), **Unused seats**, **Recoverable per year** (unused seats × annual cost per seat), **Over-allocated products**.
- **Charts:** **Seats by product** (assigned / unused / over-allocated), **Recoverable per year**.
- **Table:** **Seats by product** (most unused seats first) — Product, Vendor, Kind, Seats, Assigned, Unused, Utilization, Cost / seat / yr, Recoverable / yr, Flags. Flags include "Over-allocated by N", "No seats assigned", "No owner" and "One-time license".
- No options.

### Hardware lifecycle & refresh (Assets)
Which devices to replace or redeploy, and what replacing them will cost. Retired and disposed devices are left out.
- **Option:** **Refresh after** — **3 years**, **4 years** (default) or **5 years**.
- **Summary:** **Devices in service**, **Average age**, **Due for refresh** (older than the chosen age), **Out of warranty, in use** (active devices whose warranty has ended), **Idle devices** (unassigned devices that are active or in storage), **Est. replacement cost** (the original purchase price of devices due for refresh).
- **Charts:** **Fleet age** (devices by years since purchase: < 1 yr … 5+ yrs, Unknown), **Refresh due by type**.
- **Tables:** **Fleet by type** (Type, Devices, Avg age (yrs), Due for refresh, Out of warranty) and **Devices to act on** (Device, Type, Age (yrs), Purchased, Warranty, Status, Assigned to, Purchase price, Why).
- Age is counted from the purchase date. A device with no purchase date has an unknown age and is never flagged as due for refresh.

### Department cost (People)
What IT costs per department and per head.
- **Summary:** **Departments**, **Headcount**, **Software cost / yr** (allocated by seat), **Software cost / head / yr**.
- **Charts:** **Software cost by department**, **Headcount by department**.
- **Table:** **By department** — Department, Headcount, Devices, Device value, Software seats, Software / yr, Software / head / yr. Employees without a department are grouped under "No department".
- No options.

### Employee asset statement (People)
Everything one employee holds — for example before onboarding or offboarding.
- **Options:** pick the employee in **Choose an employee…** (the report stays empty until you do), and **Include prices** (on by default) — turn it off to leave out purchase prices and software costs, e.g. for a copy you send to the employee.
- **Summary:** **Employee** (with job title and department), **Devices**, **Software seats**, and — when prices are included — **Device value** and **Software cost / yr**.
- **Tables:** **Devices** (Device, Type, Status, Asset tag, Serial, Purchase price) and **Software** (Product, Vendor, Kind, Assigned, Cost / yr).
- This report has no charts.

## Reading the numbers

- **Currencies are never converted.** Each item keeps the currency it was entered in; money figures and totals show one line per currency (e.g. "$12,000" and "€3,400"). Money charts show one currency at a time — when several are present, switch with the currency buttons (**USD**, **EUR**, **ILS**) at the chart's top-right.
- **Annual cost:** monthly billing × 12, quarterly × 4, annual × 1. A license with no billing cycle is a one-time purchase and is left out of yearly figures; a SaaS subscription or service with no billing cycle is treated as billed once a year.
- **Cost per seat:** annual cost ÷ total seats (or ÷ the number of people assigned when no seat count is set). Recoverable spend and department/employee software costs are allocated this way.
- **Sorting:** click any column header to sort by it; click again to reverse, and a third time to return to the original order.
- Tables with more than one row get a **Total** row.
- Reports show the current state only — there's no history of past assignments.
- Microsoft 365 licenses you've hidden are left out of every report.

## Exporting, emailing and printing

The buttons at the top-right of a report:

- **Export CSV** — downloads the report's tables with the options you've chosen. A report with several tables puts them one after another in the same file, each under its title. Each money column is split into one column per currency (e.g. "Annual cost (USD)", "Annual cost (EUR)"). Charts and summary figures aren't included.
- **Email** — opens the **Email "*report title*"** dialog. The report is attached as a CSV.
  1. **Recipient** is pre-filled with your own address — or, for the **Employee asset statement**, with that employee's email.
  2. Change the address if needed and click **Send** (or press Enter). A "Report sent to …" message confirms it.
- **Print** — opens your browser's print dialog. The sidebar, top bar, buttons and options are left out of the printout.

### Who can receive a report

A recipient must be one of:
- your own sign-in email address;
- an address on the same email domain as your sign-in address;
- a user or employee in an organization the report covers;
- an address an Org Admin has approved under **Settings → Report recipients** — see [Security settings](../administration/security-settings.md).

Any other address is refused with "This address isn't allowed. Recipients must share your login's email domain, be an org member, or be approved under Settings → Security."

## Notes

- You can email up to **20 reports per hour**. Past that, sending fails with "Too many requests" until the hour is up.
- The **Employee asset statement** email greets the employee by first name and leaves out the link to IT Directory (employees don't have an account). Turn off **Include prices** first if they shouldn't see costs.
- Every report email is logged (who sent it, to whom, which report). There's no screen to view this log in the app yet.
- If a report fails to load, the page shows "This report couldn't be generated."
