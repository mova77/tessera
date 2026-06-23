# Security Policy

This project is an OIDC / OAuth 2.0 authorization server. Because it issues and
validates security tokens and isolates tenant data, we take security reports
seriously and ask that you disclose them responsibly.

## Reporting a vulnerability

**Please do not open a public issue for a security vulnerability.**

Report it privately through GitHub's **[Report a vulnerability](../../security/advisories/new)**
feature (Security ▸ Advisories ▸ *Report a vulnerability*). This opens a private
advisory visible only to the maintainers.

When reporting, please include:

- a description of the issue and its security impact,
- the affected component / endpoint / version (commit SHA),
- reproduction steps or a proof of concept, and
- any suggested remediation.

We aim to acknowledge a report within **5 business days** and to provide an
initial assessment within **10 business days**. We will coordinate a fix and a
disclosure timeline with you, and credit you in the advisory unless you prefer
to remain anonymous.

## Scope

Security-relevant areas include, but are not limited to:

- token issuance and validation (authorization codes, access/ID tokens, refresh tokens),
- PKCE, redirect-URI handling, and other authorization-endpoint protections,
- signing-key generation, storage, and rotation,
- multi-tenant isolation (row-level security, request-scoped tenant context),
- the tamper-evident audit log, and
- authentication/authorization of administrative surfaces.

Reports that require a misconfigured deployment (for example, exposing the
service directly to untrusted clients without the documented authenticating
gateway in front of it) will be assessed on a case-by-case basis.

## Supported versions

This is pre-1.0, actively developed software. Security fixes are applied to the
`main` branch. Until a formal release line exists, please report issues against
the latest `main`.

## Handling

- We use GitHub private security advisories for coordinated disclosure.
- Dependency vulnerabilities are tracked via Dependabot; pull requests run
  dependency review and CodeQL analysis before merge.
