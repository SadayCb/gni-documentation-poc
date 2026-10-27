# Module overview

## What this module does
Page **2201** is a credit-registration / credit-offer processing workflow implemented through Oracle APEX UI callbacks and transaction-backed PL/SQL packages. The supplied code reads `SSV_KRD2201_*_LOG` entries by transaction ID, validates selected offer details, creates or removes credit-related records, coordinates other detail packages, and updates workflow state.

## Principal concepts

- **Transaction ID (`p_Tx_Fid`)**: common identifier linking log records, broker workflow, and downstream operations.
- **Offer (`Teklif_Id`)**: identifier of the master credit proposal.
- **Loan document (`Sened_No`)**: used by detail entities, account creation, payment information, and history logging.
- **Memorandum (`Memorandum_Id`)**: links offer registration to upstream approval/scoring data.
- **Transaction argument (`g_Txarg`)**: code branches on `I`, `U`, and `D`; the precise externally documented meanings must be confirmed, although the implementation treats `D` as deletion and the first two as creation-like processing.

## Main responsibilities

| Package | Evidence-based responsibility |
| --- | --- |
| `KRD2201_0_API` | Registers master transaction log, reads master records, sets workflow limits, writes `KRD_TEKLIF`, coordinates detail packages, optionally creates/posts accounting entries, prints documents, closes/deletes transaction state, calculates XIRR/IRR. |
| `KRD2201_1_API` | Reads detail transaction log, validates contract/schedule/memorandum constraints, writes `KRD_TEKLIF_DETAY` and `KRD_TESIS`, invokes `LOAN_API.CREATE_ACCOUNT`, handles payment-account association and deletion, populates APEX fields from memorandum data. |

## Not in this pilot
UI screenshots, roles/permissions matrix, full data dictionary, deployment runbook, functional acceptance scenarios, and customer operating instructions require additional sources.
