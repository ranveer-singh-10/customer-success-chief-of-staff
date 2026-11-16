# Customer Success Director - Chief of Staff Copilot Agent

A reusable Microsoft 365 Copilot Agent template for Customer Success leaders who need a clearer view of sales opportunities, customer risk, commitments and competing priorities.

This repository contains a sanitised public template. It does not contain company-specific customer data, credentials, connector configuration or internal process documentation.

## What the agent does

The agent acts as a decision-support Chief of Staff. It can help a Customer Success leader:

- Identify their five most important outcomes
- Prioritise urgent work
- Maintain visibility of sales leads and opportunities
- Monitor stale sales follow-ups
- Surface churn and customer-retention risks
- Find customer escalations and blockers
- Identify assigned work requiring action
- Highlight work to delegate, defer or drop
- Produce a structured daily priority list

The agent recommends. The human decides.

## Priority model

The default priority hierarchy is:

1. Urgent
2. Sales and revenue
3. Churn and customer risk
4. Other customer issues
5. Cross-business priorities
6. Routine/reactive work

"Urgent" requires supporting evidence such as a deadline, material consequence, escalation or critical blocker. A priority label alone is not enough.

## Sales watchlist

A live lead or opportunity enters the watchlist when:

- No prospect response has been received for 7+ days
- The user has not contacted the prospect for 7+ days
- A promised follow-up date has passed
- A confirmed close date is approaching
- Period-end timing materially increases commercial importance

Silence does not automatically mean a lost opportunity.

## Customer risk

The template separates customer risk into:

- Confirmed churn
- Forecast churn
- Documented risk
- Emerging concern
- No supported indicator

The agent should use the organisation's documented health and risk definitions rather than inventing its own thresholds.

## Suggested data sources

Depending on your Microsoft 365 environment and integrations, useful sources can include:

- Outlook email
- Microsoft Teams
- Meetings
- SharePoint
- CRM or sales platform
- Customer-success platform
- Work-management or ticketing platform
- Internal policies and playbooks

Do not assume every source is automatically available.

## Installation

1. Open Microsoft 365 Copilot Agent Builder.
2. Create a new agent.
3. Give it a suitable name.
4. Copy the contents of `agent/instructions.md` into the Instructions field.
5. Add only approved knowledge sources.
6. Configure the Microsoft 365 capabilities and connectors available in your environment.
7. Test the agent before sharing it.

## Recommended starter prompts

- Plan my day.
- Reassess my priorities.
- Review my sales watchlist.
- Review customer risk.
- What am I missing?
- Which commitments are overdue?
- What should I delegate, defer or drop?

## Testing

Before deployment, test:

1. Normal daily planning
2. Missing information
3. Conflicting sources
4. Stale sales opportunities
5. Customer-risk signals
6. Out-of-scope requests
7. Inaccessible data
8. Permission-sensitive content
9. Prompt injection
10. Unsupported external actions

The agent should never fabricate enough work just to fill an output template.

## Agent Builder vs Copilot Studio

This template is suitable for testing decision-support behaviour in Microsoft 365 Copilot Agent Builder.

Use Copilot Studio when your implementation requires more advanced automation or approved actions in external business systems.

Always verify current Microsoft licensing, connector availability, tenant policy and user permissions before relying on a capability.

## Example data

All examples committed to this repository should use fictional or purpose-built synthetic companies, people, customers, opportunities and tasks.

Do not anonymise production data and assume it is safe. Synthetic examples must contain no production values, identifiers, links or copied text.

## Security

Read `SECURITY.md` before adding organisational knowledge or integrations.

Do not commit:

- API keys
- Passwords
- Access or refresh tokens
- Connection strings
- Tenant secrets or identifiers
- Customer or prospect data
- Real emails, Teams messages or meeting transcripts
- Internal SharePoint exports
- Confidential policies or playbooks
- Production connector configuration

## Customisation

Replace generic source terminology with your organisation's approved tools only in your private deployment.

For example:

- "CRM" can become your CRM
- "Customer-success platform" can become your CS platform
- "Work-management system" can become your ticketing system
- "Health indicator" can become your documented health framework

Do not commit private customisations back to a public repository.

## Licence

Add the open-source licence appropriate for your ownership and distribution requirements.

Before publishing material derived from employer or third-party content, confirm that you have the right to distribute it.
