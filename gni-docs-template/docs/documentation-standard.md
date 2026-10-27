# GNI documentation authoring standard — Draft 0.1

## Audience and distribution

- **Internal developer guide:** source-level details, entity names, workflow coupling, technical troubleshooting.
- **Customer technical guide:** supported integration points, configuration prerequisites, operational runbooks. Exclude proprietary internal implementation and secrets unless specifically licensed/approved.
- **End-user guide:** UI workflows and screenshots, written after testing and product review.

Do **not** publish the entire internal documentation tree to customers by default.

## File structure

```text
README.md
docs/
  overview.md
  architecture.md
  workflows.md
  api/
    krd2201-0-api.md
    krd2201-1-api.md
  review-findings.md
  documentation-standard.md
mkdocs.yml
```

## Package reference template

1. Name, visibility, ownership, scope and version
2. Business purpose and lifecycle
3. Public state and exported API members
4. Parameters, return contracts and exceptions
5. Dependencies and persistent side effects
6. Call sequence and examples (**only executable when verified**)
7. Known limitations / needs-review
8. Source evidence and revision history

## Evidence labels

- **Verified from supplied source:** exact code statement / call / signature.
- **Inferred from source:** interpretation requiring engineering confirmation.
- **Not yet verified:** requires runtime, missing source, business owner, or data dictionary.

## Editorial rules

- Keep procedure names and database identifiers exact.
- Prefer English explanatory prose but preserve original code names.
- Do not invent parameter meaning, return values, transaction behavior, or business rules.
- Never include credentials, production personal data, keys, or connection strings.
- Every change affecting a public API must update its Markdown reference in the same change request.
- Obtain technical reviewer and product-owner sign-off before external distribution.
