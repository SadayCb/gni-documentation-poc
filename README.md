# GNI Loan API — Technical Documentation

> **Status:** Draft / Proof of Concept · **Audience:** Internal developers and integration teams · **Language:** English

`LOAN_API` is a shared Oracle PL/SQL package for core loan processes. Unlike an APEX page-specific package, it exposes operations used across multiple workflows.

## Start here

| Document | Purpose |
|---|---|
| [Overview](docs/overview.md) | Scope, architecture and functional domains |
| [Getting started](docs/guides/getting-started.md) | Guided onboarding path |
| [Public API catalogue](docs/api/loan-api.md) | All active public procedures/functions with signatures |
| [Workflows](docs/workflows.md) | Cross-cutting process diagrams |
| [Dependencies](docs/reference/dependencies.md) | Major tables and integration packages |
| [Review & security](docs/reference/review-findings.md) | Source-based issues and gaps to validate |

## Documentation principles

- Package **specification** is the source of truth for callable signatures.
- Package **body** supports behavioral interpretation and dependency mapping.
- Unconfirmed behavior is marked **Review required**, not invented.
- Public/customer-facing documentation must be reviewed and sanitized before release.

## Scope

This proof of concept intentionally excludes the earlier Page 2201 documentation and covers only `LOAN_API`.
