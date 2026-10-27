# GNI Credit Registration — Page 2201

> **Documentation PoC · Version 0.1 · Language: English · Status: Draft / Technical review required**

## Purpose
This repository demonstrates the proposed documentation standard for GNI's Oracle APEX / PL/SQL-based credit-registration functionality associated with page **2201**.

The pilot covers two supplied package specifications and implementations:

- [`KRD2201_0_API`](docs/api/krd2201-0-api.md) — master credit-offer processing, workflow control, and related operations.
- [`KRD2201_1_API`](docs/api/krd2201-1-api.md) — credit-offer detail processing, validations, account creation, and cleanup.

## Start here

| Reader | Recommended path |
| --- | --- |
| New developer | [Module overview](docs/overview.md) → [Execution flow](docs/workflows.md) → [API reference](docs/api/krd2201-0-api.md) |
| Implementation / support team | [Architecture](docs/architecture.md) → [Review findings](docs/review-findings.md) |
| Technical lead | [Documentation conventions](docs/documentation-standard.md) → [Review findings](docs/review-findings.md) |

## Scope and evidence
Based only on the provided `KRD2201_0_API` and `KRD2201_1_API` specifications and bodies. Definitions of `KRD2201_1X_API`, `KRD2201_2_API`, `KRD2201_3_API`, `LOAN_API`, `TRN_BROKER`, APEX page metadata, database DDL, and deployed configuration were **not** supplied. Behavior attributed to these dependencies must be independently verified.

The documentation describes observed source behavior, **not** a production certification, security assessment, or complete user manual. Identifiers used below are technical identifiers, not customer-facing product terminology.

## Review gates
- [ ] Confirm business terminology with product owner
- [ ] Validate cross-package behavior against missing package bodies
- [ ] Confirm transaction ownership and privileges
- [ ] Review potential defects listed in [Review findings](docs/review-findings.md)
- [ ] Approve a customer-safe release (exclude internal SQL, account details, sensitive configuration)
