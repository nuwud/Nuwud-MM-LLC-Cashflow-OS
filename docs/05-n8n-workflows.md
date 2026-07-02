# n8n Workflow Specs

n8n should support the money loop. It should not create a spam machine or a content treadmill.

## Core rule

Human review stays in the loop for outbound messages and affiliate content.

## Workflow 1: Daily Cashflow Command Brief

### Purpose

Give Patrick a daily view of money moves before builder work begins.

### Inputs

- Notion pipeline database
- unpaid invoices / manual input until accounting is connected
- calendar if available
- GitHub issues from this repo

### Output

Daily message to Slack, email, or Notion:

- payments expected
- invoices to send/follow up
- A-priority prospects with next actions
- blocked work waiting on money/materials
- 3 recommended sales actions
- 1 content/affiliate opportunity if relevant

### Safety

Do not invent invoices or payment facts. Mark unknowns as unknown.

## Workflow 2: Warm Follow-Up Queue

### Purpose

Prevent warm relationships from going stale.

### Trigger

Daily at start of workday.

### Logic

Find prospects where:

- Status is Replied, Discovery, Audit Offered, Invoice Sent, or Nurture
- Next Action Date is today or overdue
- Status is not Won/Lost

### Output

Draft follow-up messages for human review.

### Human action

Patrick approves, edits, or rejects.

## Workflow 3: X / LinkedIn Authority Sprinkler

### Purpose

Publish small, consistent posts that point to Nuwud's revenue systems positioning and occasionally include aligned affiliate/tool recommendations.

### Content buckets

1. Revenue leaks
2. Founder systems architecture
3. Shopify / ecommerce conversion
4. AI-native agency operations
5. Automation examples
6. Client lessons / anonymized case notes
7. Tool-stack recommendations with disclosure

### Cadence

Start conservative:

- 1 LinkedIn post per day max
- 1 to 3 X posts per day max
- 1 affiliate/tool post per week until trust and rhythm are established

### Output format

Each generated post must include:

- platform
- hook
- post body
- CTA
- related offer
- affiliate disclosure needed? yes/no
- approval status

### Safety

- No auto-posting affiliate links without human approval.
- No fake results.
- No client details without permission.
- No platform rule dodging.
- No mass unsolicited DMs.

## Workflow 4: Affiliate Resource Inserter

### Purpose

Identify where an affiliate recommendation naturally belongs in content or audit outputs.

### Inputs

- affiliate program seed list
- content ideas
- audit findings
- client platform/pain

### Matching logic

Examples:

- WordPress performance pain -> Kinsta resource
- marketing automation / CRM pain -> ActiveCampaign or HubSpot resource
- SEO / AI search visibility pain -> Semrush resource
- workflow automation content -> n8n resource
- Shopify build / commerce architecture -> Shopify partner ecosystem or app/tool resources

### Output

A recommendation card:

```text
Tool:
Reason:
Best-fit audience:
Commission type:
Disclosure required:
Suggested CTA:
Risk / caveat:
```

## Workflow 5: Prospect-to-Content Flywheel

### Purpose

Turn real sales observations into authority content.

### Trigger

When a prospect is researched or an audit is delivered.

### Output

- 3 anonymized post ideas
- 1 offer CTA
- 1 possible affiliate/resource mention
- 1 reusable checklist or framework idea

## Workflow 6: Invoice / Payment Gate Reminder

### Purpose

Protect Patrick from doing unpaid deep work.

### Logic

If a prospect or client status indicates requested diagnostic/development work but payment status is unpaid, generate a reminder:

> Work is blocked until invoice/deposit is handled.

### Output

- internal warning
- suggested client message
- next action date

## Recommended first n8n build order

1. Daily Cashflow Command Brief
2. Warm Follow-Up Queue
3. Invoice / Payment Gate Reminder
4. X / LinkedIn Authority Sprinkler
5. Affiliate Resource Inserter
6. Prospect-to-Content Flywheel
