# Data Model

## Custom object: Sales Lead

The project uses a custom Salesforce object named **Sales Lead**. Its API name is expected to be `Sales_Lead__c`; confirm the exact API name in Object Manager before using it in metadata or code.

| Field | Type | Purpose |
|---|---|---|
| Sales Lead Name | Record Name (Text) | Identifies the lead record |
| Company | Text | Company associated with the lead |
| Email | Email | Lead email address |
| Phone | Phone | Lead contact number |
| Lead Status | Picklist | Tracks the lead stage |
| Lead Source | Picklist | Records how the lead was acquired |
| Follow-up Date | Date | Stores the planned follow-up date |
| Priority Lead | Checkbox | Indicates whether the lead is priority |

### Picklist values

**Lead Status**
- New
- Contacted
- Qualified
- Converted
- Rejected

**Lead Source**
- Website
- Referral
- LinkedIn
- Advertisement

### Data-quality rule

The `Company_Required` validation rule checks `ISBLANK(Company__c)` and prevents a record from being saved when Company is blank.
