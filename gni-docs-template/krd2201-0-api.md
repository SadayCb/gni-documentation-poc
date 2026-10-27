# API reference — `KRD2201_0_API`

**Source:** supplied package specification and body. **Visibility:** all procedures/functions below occur in the package specification and therefore are publicly callable to authorized database consumers. Calls may require application transaction context.

## Package state
`g_Musteri_No`, `g_Teklif_Id`, `g_Islem`, `g_Mig` (default `0`), `g_no_matrix` (default `0`), `g_oapi_txfid`, `G_FILL_DATA_FROM_MEMORANDUM` (default `'Y'`). These are public package variables, so their session-level lifecycle deserves review.

## Public members

| Member | Signature / result | Observed purpose |
| --- | --- | --- |
| `JUSTDOIT` | `(p_Tx_Fid NUMBER, p_Request VARCHAR2 DEFAULT 'ALL')` | Main orchestration for init, validation, master insert/delete, detail orchestration, accounting, history, documents, and end state. |
| `STARTTX` | `(p_Tx_Fid NUMBER)` | Calls `TRN_BROKER.REGISTER` for `SSV_KRD2201_0_LOG`. |
| `SET_PROCESS_PARAMETER` | `(p_Prin_Id NUMBER)` | Sets workflow parameters `LIMIT`, `KRD_GM_LIMIT`, `KRD_SB_LIMIT`; uses branch/product and user-limit queries. |
| `SET_MULTI_ITEM` | `(p_Item_Name VARCHAR2, p_Item_Value VARCHAR2)` | Handles APEX field change callbacks and dynamic UI updates; code is page/region dependent. |
| `GET_OCEAN_PRODUCT` | `(Pproduct NUMBER) RETURN VARCHAR2` | Checks `SP_URUN_PR.EXTERNAL_PRODUCT_ID`; returns `'E'` if a matching external ID exists, otherwise `'H'`. |
| `CALCULATE_XIRR` | `(p_doc_no VARCHAR2, p_type VARCHAR2, p_calc_as VARCHAR2 DEFAULT 'XIRR', p_offer_amnt NUMBER, p_int_rate NUMBER, p_plan_begin DATE) RETURN NUMBER` | Builds scheduled cash flows and performs iterative XIRR/IRR rate search. |

## `JUSTDOIT`

**Inputs:** `p_Tx_Fid` links the execution to staged rows and `TRN_BROKER`; `p_Request='VALIDATE'` triggers a separate branch, while default `'ALL'` proceeds through the main processing path.

**Side effects:** inserts into `KRD_TEKLIF`, invokes subordinate package processing, may call accounting interfaces and loan-history creation, prints documents and sets broker transaction state. Never present it as a read-only method.

**Important:** both `I` and `U` are handled by the first `CASE WHEN` branch; the later `U` branch is unreachable in this implementation. See [Review findings](../review-findings.md).

## `CALCULATE_XIRR`

For `p_type='APP2201'`, uses provided offer amount, initial rate, start date, and `APEX_KRD2201_4_COLL_V` schedule rows; for `p_type='SCHEDULE'`, loads offer/schedule from persisted tables including `LOAN_PAYMENT_PLAN`. Calculation uses actual day differences / 365 for `XIRR`, and row sequence for `IRR`. Returns a `NUMBER` rate (implementation uses percentage-based arithmetic).

**Caution:** the method deletes rows from `XIRR_SCHEDULE_TMP` and repopulates them; confirm its table type and session isolation. No guarantee of convergence, bounds checking, or transaction-safe read-only behavior can be made from this source.

## `SET_MULTI_ITEM`

Uses APEX runtime functions (`V`, `V$`, `S#`, `SR#`, and `GLBL_LOV`) and branches on page/region/item identifiers. It is an application callback, not an isolated pure API. APEX metadata and UI screenshots are needed for a complete field-by-field guide.

## Supporting private routines
`INIT`, `GETRECORD`, `VALIDATE_ROW`, `VALIDATE_ALL`, `DO_NEW`, `DO_AMMEND`, `DO_ERASE`, `AFTER_TX`, `BOOK_NEW`, `BOOK_ERASE`, `ENDPROCESS`, and `DOCUMENT` appear in the body only and should not be presented as public entry points.
