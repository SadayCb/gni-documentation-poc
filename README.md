# GNI Software — LOAN_API Documentation

> **Document status:** Draft — Proof of Concept. This document describes a shared PL/SQL package, not an individual Oracle APEX screen.

## Documentation Overview

| Section | Item | Details / Reference |
|:--|:--|:--|
| **General** | Document Name | **LOAN_API — Technical & Functional Documentation** |
| | Package Name | `GAIA.LOAN_API` |
| | Created Date | 27 October 2026 |
| | Created By | GNI Software — Development Team |
| | Document Version | 1.0 — Draft |
| | Documentation Status | Under Technical & Business Review |
| | Technology | Oracle PL/SQL · Oracle Database |
| **Introduction** | Purpose of the Document | [Purpose & Overview](docs/overview.md) — Package objectives, responsibilities and scope. |
| | Scope of the Document | Public interfaces and verified implementation behavior. [Getting Started](docs/guides/getting-started.md) |
| | System Architecture | [Architecture](docs/architecture.md) — Components, dependencies and execution flow. |
| **API Specifications** | Procedures & Functions | [Complete API Reference](docs/api/loan-api.md) — Public procedures, functions and overloads. |
| | Business Workflows | [Business Workflows](docs/workflows.md) — Loan operations, schedules, payments and EOD/SOD processes. |
| | Technical Dependencies | [Dependencies](docs/reference/dependencies.md) — Related packages, procedures and functions. |
| **Data Model** | Tables & Views | [Data Model](docs/data-model.md) — Related database objects and data operations. |
| | Data Relationships | [Data Model & Relationships](docs/data-model.md) — Read/write interactions and dependencies. |
| **Error Handling** | Errors & Exceptions | [Error Handling Reference](docs/error-handling.md) — Application errors, validation rules and exception handling. |
| | Review Findings | [Technical Review Findings](docs/reference/review-findings.md) — Potential issues and unverified behavior. |

## Documentation Navigation

- [Introduction and Functional Overview](docs/overview.md)
- [Developer Onboarding](docs/guides/getting-started.md)
- [Public API Reference](docs/api/loan-api.md)
- [Operational Workflows](docs/workflows.md)
- [Data Model](docs/data-model.md)
- [Error Handling](docs/error-handling.md)
- [Dependencies](docs/reference/dependencies.md)
- [Review Findings](docs/reference/review-findings.md)

## Source and Review Policy

The PL/SQL package **specification** defines the exposed signatures. The package **body** is used to explain selected behavior and identify dependencies. Unverified business semantics are explicitly marked for review. Do not publish internal implementation details to customers without technical and security approval.
