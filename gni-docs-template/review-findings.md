# Review findings and documentation gaps

> These are source-level observations for engineering review, **not** validated production defects. No changes to code have been made.

| ID | Finding | Source observation | Recommended check |
| --- | --- | --- | --- |
| RF-01 | Update branch appears unreachable | In both `JUSTDOIT` methods, `WHEN g_Txarg = 'I' OR g_Txarg = 'U'` precedes `WHEN g_Txarg = 'U'`. | Confirm intended update semantics and actual test coverage. |
| RF-02 | Validation path may mutate state | Detail `JUSTDOIT('VALIDATE')` calls `KRD2201_2_API.DO_NEW(NULL)`; master validation calls accounting `PA_API#.CREATE_J` under conditions. | Confirm contract for `VALIDATE` and effects on transaction rollback. |
| RF-03 | Shared public package variables | Migration and memorandum flags and identifiers are public session-level state. | Define reset/initialization strategy across APEX pooled sessions. |
| RF-04 | XIRR table cleanup | `CALCULATE_XIRR` starts with `DELETE XIRR_SCHEDULE_TMP`. | Verify GTT/session scope, commit semantics, concurrent users, and method failure behavior. |
| RF-05 | Unconditional failed validation for selected credit lines | Detail `VALIDATE_ROW` includes `PLOG.ASSERT#(1 = 2, ...)` when `KREDIT_KHAT IN ('KK','KX')`. | Confirm whether these products are intentionally blocked. |
| RF-06 | Potential uninitialized count | `l_Loan_Count` is checked with `l_Loan_Count = 0` when `lx.krd_fifd IS NULL`, before a visible assignment on that path. | Confirm expected behavior with PL/SQL NULL boolean semantics. |
| RF-07 | Broad exception swallowing | Master `DO_NEW` uses `WHEN OTHERS THEN NULL` for reference lookup; multiple other blocks also catch broadly. | Decide where diagnostics and explicit fallback are required. |
| RF-08 | Transaction ownership is undocumented | Source invokes DML, broker, accounting and loan APIs without an explicit overarching transaction contract. | Document caller COMMIT/ROLLBACK obligations and hidden commits in dependencies. |
| RF-09 | Public `GETRECORD` can return an uninitialized row | Searches package-level collection; returns declared row even when no matching `FID`. | Define not-found contract and initialization preconditions. |
| RF-10 | API and UI are coupled | `SET_MULTI_ITEM` depends on APEX page, region and session-item functions. | Document supported pages and UI states with page export evidence. |

## Missing evidence for publication

1. Package specifications and bodies for `KRD2201_1X_API`, `KRD2201_2_API`, `KRD2201_3_API`, and other external calls.
2. DDL for relevant log/business tables; indexes and FKs.
3. Page 2201 (and conditional page 3 / page 4) APEX export and screens.
4. Business-approved meaning of status, operation, credit-line and payment codes.
5. Reproducible nonproduction test scenarios, sample transactions and expected outputs.
6. Distribution classification for internal vs customer deliverables.
