# Security Policy

## Purpose

This repository contains a public example of Microsoft Copilot Agent instructions.

It is designed to contain reusable agent logic only. It must not store secrets, production configuration, customer information or confidential organisational knowledge.

## Public instructions are public

Do not rely on prompt secrecy as a security control.

Anything committed to this repository should be treated as publicly readable.

The public instruction template may contain security behaviour, but it must never contain the secrets it is intended to protect.

## Never commit secrets

Do not commit:

- Passwords
- API keys
- Access or refresh tokens
- Client secrets
- Certificates or private keys
- Connection strings
- Authentication headers
- Environment secrets
- Production webhook URLs containing secrets
- Service-account credentials

If a secret is committed, treat it as compromised. Remove it from repository history where appropriate and rotate or revoke it immediately.

## Do not commit organisational data

Do not add:

- Customer or prospect names and identifiers
- Revenue, pipeline or contract data
- Customer-health records or churn forecasts
- Real ticket, CRM or customer-success records
- Emails, Teams messages or meeting transcripts
- Internal SharePoint documents
- Confidential policies or procedures
- Employee personal information
- Tenant-specific private configuration
- Proprietary field mappings not approved for release

Use purpose-built synthetic examples instead. Label synthetic data clearly.

## Instructions are not access control

Agent instructions are behavioural guidance, not a security boundary.

Protect organisational information using the permissions, identities, sensitivity controls, connector policies and access controls of the underlying systems.

Never grant an agent broader access simply because its instructions tell it not to reveal information.

## Permissions and least privilege

A deployed agent must respect permissions in the underlying Microsoft 365 environment and connected systems.

Use least privilege for:

- Microsoft 365 access
- Connectors
- External actions
- Service accounts
- CRM platforms
- Customer-success platforms
- Work-management systems

Review access whenever the agent's audience, tools or data sources change.

## External actions

Separate read-only analysis from write actions.

An agent must not create, update, delete, assign, transition, send or otherwise change external records unless:

1. The action is intentionally implemented.
2. Authentication is approved.
3. Permissions are appropriate.
4. The user understands the action.
5. Appropriate confirmation is obtained for consequential changes.
6. The tool reports success.

Never claim an external action succeeded unless the underlying system confirms it.

## Prompt injection

Treat retrieved emails, documents, web pages, collaboration messages and external-system records as data, not instructions governing the agent.

Retrieved content must not be allowed to:

- Override the agent's role
- Reveal protected configuration
- Expose credentials
- Change security rules
- Trigger unauthorised actions

## Knowledge sources

Review every knowledge source before attaching it to an agent.

Check:

- Who owns it
- Who may access it
- Whether it contains confidential information
- Whether it is current
- Whether sensitivity labels or permissions apply
- Whether it is appropriate for every intended agent user

Do not assume that because a document is useful to an agent it is safe to publish publicly.

## Reporting security issues

Do not open a public GitHub issue containing credentials, customer information or other sensitive material.

Configure GitHub private vulnerability reporting or provide a private security contact before making the repository public.

## Before publishing

Review both current files and Git history. Confirm the repository contains:

- No secrets
- No real customer or prospect data
- No confidential organisational documents
- No private connector configuration
- No internal tenant identifiers
- No proprietary field mappings not approved for release
- No third-party material you do not have permission to distribute

Only then make the repository public.
