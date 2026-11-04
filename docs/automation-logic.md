# Automation Logic

## Record-triggered Flow

**Flow label:** `Mark Qualified Lead as Priority`

### Configuration

- Object: Sales Lead
- Trigger: A record is updated
- Entry condition: Lead Status equals `Qualified`
- When to run: Only when a record is updated to meet the condition requirements
- Optimization: Fast Field Updates
- Update: Set `Priority Lead` to `True` on the record that triggered the Flow

### Expected behavior

When a Sales Lead is updated and its status changes to `Qualified`, Salesforce automatically checks the Priority Lead checkbox.

### Verification

The behavior was manually tested by updating a lead's status to `Qualified` and confirming that Priority Lead became checked on the record.

## Validation rule

**Name:** `Company_Required`

**Formula:**

```text
ISBLANK(Company__c)
```

This rule blocks saving a Sales Lead when Company is blank. A manual save attempt with Company empty produced the expected Salesforce validation error.
