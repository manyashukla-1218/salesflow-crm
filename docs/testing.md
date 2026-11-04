# Testing

The following checks were performed manually in the Salesforce Playground.

| Test | Action | Expected result | Status |
|---|---|---|---|
| Company validation | Create or save a Sales Lead with Company blank | Salesforce blocks the save and displays a validation error | Passed |
| Priority Flow | Update a lead so Lead Status becomes Qualified | Priority Lead is automatically checked | Passed |
| Report | Run Sales Lead Overview | Lead records are grouped by Lead Status | Verified |
| Dashboard | Open SalesFlow CRM Dashboard | Donut chart and lead-details table are displayed | Verified |

## Notes

- These are manual configuration checks, not Apex unit tests.
- Do not describe the project as having automated Apex test coverage; Apex classes and tests have not yet been added.
- Use fictional sample records in screenshots. Hide or blur personal contact details before making the repository public.
