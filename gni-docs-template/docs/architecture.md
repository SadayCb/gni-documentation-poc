# Architecture and dependencies

## High-level component map

```mermaid
flowchart TD
    A[Oracle APEX Page 2201 / UI callbacks] --> M[KRD2201_0_API]
    A --> D[KRD2201_1_API]
    M --> T[TRN_BROKER]
    D --> T
    M --> DL[KRD2201_1_API and KRD2201_1X_API]
    D --> OTHER[KRD2201_2_API and KRD2201_3_API]
    D --> LOAN[LOAN_API]
    M --> ACC[PA_API# / MM_ACCOUNTING#]
    M --> MASTER[(KRD_TEKLIF)]
    D --> DETAIL[(KRD_TEKLIF_DETAY / KRD_TESIS)]
    M --> LOG0[(SSV_KRD2201_0_LOG)]
    D --> LOG1[(SSV_KRD2201_1_LOG)]
```

**Diagram note:** Connections are observed code references, not a complete deployed component diagram.

## Important database objects observed

| Object | Observed role |
| --- | --- |
| `SSV_KRD2201_0_LOG` | Master-side staged transaction records |
| `SSV_KRD2201_1_LOG`, `SS_KRD2201_1_LOG` | Detail-side staged transaction records / lookup |
| `SS_KRD2201_1X_LOG`, `SS_KRD2201_3_LOG` | Supplementary memorandum, contract and schedule information |
| `KRD_TEKLIF` | Master offer record created by `KRD2201_0_API.DO_NEW` |
| `KRD_TEKLIF_DETAY` | Loan/offer detail record inserted by `KRD2201_1_API.DO_NEW` |
| `KRD_TESIS` | Loan-related record inserted/removed during detail handling |
| `LM_FLOW` | Upstream memorandum status and reference updates |
| `GL_JOURNAL_LINES` | Checks for accounting journal statuses |
| `CS_ACCOUNT` | Payment account lookup |
| `XIRR_SCHEDULE_TMP` | Temporary calculation input for XIRR / IRR algorithm; storage isolation is unverified |

## Known integration calls
`TRN_BROKER.REGISTER`, `TRN_BROKER.SETTXSTEP`, `TRN_BROKER.SETTXSTATE`, `TRN_BROKER.WF_SET_PARAMETER`, `LOAN_API.CREATE_ACCOUNT`, `LOAN_API.CREATE_LOAN_HISTORY`, `LOAN_API.CHANGE_ACCOUNT_STATUS`, `MM_ACCOUNTING#.POST_JOURNAL`, `PA_API#.CREATE_J`, `GLBL_REPORT.PRINT_FORM_DOCUMENTS`.

Only caller-side behavior is documented; the called package contracts were not supplied.
