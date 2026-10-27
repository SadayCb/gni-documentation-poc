# API reference — `KRD2201_1_API`

**Source:** supplied package specification and body.

## Public package state
`g_Fkid`, `g_Sened`, `g_Memorandum`, `g_Txfid`, `g_Sube`, `g_loan_type`, `g_Is_online_offer`. These values are shared across related package calls; exact session/reset semantics need testing.

## Public members

| Member | Signature / result | Observed purpose |
| --- | --- | --- |
| `GETRECORD` | `(Pfid NUMBER) RETURN SSV_KRD2201_1_LOG%ROWTYPE` | Searches the already-loaded in-memory detail collection by `FID`; no database lookup is performed in this function. |
| `JUSTDOIT` | `(p_Tx_Fid NUMBER, p_Request VARCHAR2 DEFAULT 'ALL')` | Detail-side validation, account operations, master/detail inserts or deletion, and downstream calls. |
| `STARTTX` | `(p_Tx_Fid NUMBER)` | Registers `SSV_KRD2201_1_LOG` with transaction broker. |
| `SET_PROCESS_PARAMETER` | `(p_Prin_Id NUMBER)` | Sets the workflow `LIMIT` parameter to `-1`. |
| `SET_MULTI_ITEM` | `(p_Item_Name VARCHAR2, p_Item_Value VARCHAR2)` | Populates and updates APEX form items, including memorandum-derived values, under conditional UI states. |

## Major detail operations (private implementation)

### `VALIDATE_ROW`

Reads schedule and supplementary log rows and checks payment start date, contract date, credit line type, duplicate memorandum/contract, term, and approved amount. Errors are raised via `PLOG.ASSERT#`, `RAISE_APPLICATION_ERROR`, and localized `GNI_MESSAGE` lookup.

### `DO_NEW`

Observed sequence: load detail/context; update `LM_FLOW`; insert `KRD_TEKLIF_DETAY`; update memorandum status; optionally adjust main-limit information for a particular operation type; insert `KRD_TESIS`; invoke `LOAN_API.CREATE_ACCOUNT`; locate a `CS_ACCOUNT` payment account and update `KRD_TESIS` with payment details.

### `DO_ERASE`

Looks up `KRD_TESIS` and `KRD_TEKLIF_DETAY`; may change/close loan/payment account status; deletes associated credit records including payment plans, collateral association, credit detail and selected auxiliary data; updates `LM_FLOW` status. This is a destructive operation; order/constraints and downstream effects must be tested.

### `OPEN_CARI_ACC`

Called before `VALIDATE_ALL` for normal processing. May select or create an account depending on payment setup; full behavior depends on other packages and runtime session data. **Needs review** before documenting customer-facing account semantics.

## Usage considerations
- Public `GETRECORD` depends on prior initialization of the package-level collection.
- `JUSTDOIT(..., 'VALIDATE')` invokes `KRD2201_2_API.DO_NEW(NULL)`, making validation potentially state-changing.
- This package alone does not specify the behavior of subordinate `KRD2201_2_API` / `KRD2201_3_API` routines.
