# LOAN_API — Public API Reference

This catalogue contains **88 active public declarations** (including overloads). Signatures are reproduced from the supplied specification, with line references.

> **Important:** This is not a list of internal/private routines. Some descriptions are preliminary and require developer review.

## Index

### Accounts & Balances

- [`get_loan_amount`](#get-loan-amount) — function (spec line 130)
- [`get_overdue_min_amount`](#get-overdue-min-amount) — function (spec line 136)
- [`get_gl_value`](#get-gl-value) — function (spec line 161)
- [`get_gl_acc_active_passive`](#get-gl-acc-active-passive) — function (spec line 189)
- [`get_gl_acc_from_matrix`](#get-gl-acc-from-matrix) — function (spec line 191)
- [`get_offer_id`](#get-offer-id) — function (spec line 219)
- [`get_account_feature`](#get-account-feature) — function (spec line 273)
- [`is_acc_exists`](#is-acc-exists) — function (spec line 278)
- [`is_online_offer`](#is-online-offer) — function (spec line 287)
- [`create_account`](#create-account) — procedure (spec line 304)
- [`get_new_acc`](#get-new-acc) — function (spec line 318)
- [`do_loan_status_control`](#do-loan-status-control) — procedure (spec line 338)
- [`get_acc_type_by_status`](#get-acc-type-by-status) — function (spec line 353)
- [`change_account_status`](#change-account-status) — procedure (spec line 451)

### EOD/SOD & Operations

- [`do_loan_collateral_out`](#do-loan-collateral-out) — procedure (spec line 350)
- [`do_int_calculation`](#do-int-calculation) — procedure (spec line 382)
- [`do_int_calculation_ex`](#do-int-calculation-ex) — procedure (spec line 396)
- [`do_overdue_transit_operation`](#do-overdue-transit-operation) — procedure (spec line 402)
- [`do_guarantee_out`](#do-guarantee-out) — procedure (spec line 418)
- [`do_Loan_Close_With_Collateral_Out`](#do-loan-close-with-collateral-out) — procedure (spec line 422)
- [`do_non_cash_loan_close`](#do-non-cash-loan-close) — procedure (spec line 424)
- [`stop_eod_task`](#stop-eod-task) — procedure (spec line 455)
- [`stop_loan_task`](#stop-loan-task) — procedure (spec line 457)
- [`run_loan_task`](#run-loan-task) — procedure (spec line 460)
- [`do_loan_control`](#do-loan-control) — procedure (spec line 604)
- [`do_loan_control`](#do-loan-control) — procedure (spec line 607)

### History & Changes

- [`clear_addtional_data`](#clear-addtional-data) — procedure (spec line 109)
- [`add_additional_group`](#add-additional-group) — procedure (spec line 111)
- [`end_additional_group`](#end-additional-group) — procedure (spec line 113)
- [`end_additional_main_group`](#end-additional-main-group) — procedure (spec line 114)
- [`add_additional_info`](#add-additional-info) — procedure (spec line 115)
- [`add_additional_info`](#add-additional-info) — procedure (spec line 117)
- [`add_column_update`](#add-column-update) — procedure (spec line 118)
- [`add_column_update`](#add-column-update) — procedure (spec line 122)
- [`finalize_addtional_process`](#finalize-addtional-process) — procedure (spec line 125)
- [`reverse_update`](#reverse-update) — procedure (spec line 128)
- [`table_log_operation`](#table-log-operation) — procedure (spec line 289)
- [`create_loan_history`](#create-loan-history) — procedure (spec line 343)
- [`do_delete_operation`](#do-delete-operation) — procedure (spec line 368)

### Interest & Penalties

- [`get_pen_info_for_calc`](#get-pen-info-for-calc) — procedure (spec line 71)
- [`get_interest_calc_dates`](#get-interest-calc-dates) — function (spec line 80)
- [`get_interest_calc_dates_ex`](#get-interest-calc-dates-ex) — function (spec line 85)
- [`get_interest_calc_info`](#get-interest-calc-info) — procedure (spec line 90)
- [`get_interest_calc_info_ex`](#get-interest-calc-info-ex) — procedure (spec line 101)
- [`get_pen_info_for_calc`](#get-pen-info-for-calc) — procedure (spec line 137)
- [`get_basis_year_days_cnt`](#get-basis-year-days-cnt) — function (spec line 158)
- [`loan_int_diff_operation`](#loan-int-diff-operation) — procedure (spec line 163)
- [`loan_int_diff_operation_ex`](#loan-int-diff-operation-ex) — procedure (spec line 177)
- [`Get_Delay_Int_Rate`](#get-delay-int-rate) — function (spec line 200)
- [`get_amount_for_pen_calc`](#get-amount-for-pen-calc) — function (spec line 233)
- [`do_Loan_Delay_Int_Rate_Upd`](#do-loan-delay-int-rate-upd) — procedure (spec line 448)

### Journal & Vouchers

- [`get_trn_caller_id`](#get-trn-caller-id) — function (spec line 144)
- [`get_voucher_data_from_query`](#get-voucher-data-from-query) — function (spec line 146)
- [`do_journal_entry`](#do-journal-entry) — procedure (spec line 294)
- [`create_journal_entries`](#create-journal-entries) — procedure (spec line 300)
- [`do_commission_recognition`](#do-commission-recognition) — procedure (spec line 416)
- [`do_journal_control`](#do-journal-control) — procedure (spec line 427)

### Payments & Allocation

- [`get_Pym_Startdate`](#get-pym-startdate) — function (spec line 263)
- [`recalculate_int_payment_plan`](#recalculate-int-payment-plan) — procedure (spec line 311)
- [`generate_allocated_payment_list`](#generate-allocated-payment-list) — procedure (spec line 358)
- [`add_payment_details`](#add-payment-details) — procedure (spec line 364)
- [`do_Auto_Payment`](#do-auto-payment) — procedure (spec line 370)

### Schedules & Rates

- [`get_formatted_grace_from_list`](#get-formatted-grace-from-list) — function (spec line 150)
- [`get_grace_info`](#get-grace-info) — function (spec line 153)
- [`get_commission_schedule`](#get-commission-schedule) — function (spec line 203)
- [`add_months_for_loan`](#add-months-for-loan) — function (spec line 211)
- [`get_next_Plan_Pym`](#get-next-plan-pym) — function (spec line 215)
- [`get_plan_payment_amount`](#get-plan-payment-amount) — function (spec line 223)
- [`get_Plan_Month_Count`](#get-plan-month-count) — function (spec line 239)
- [`get_plan_paid_month_count`](#get-plan-paid-month-count) — function (spec line 251)
- [`get_plan_error`](#get-plan-error) — function (spec line 255)
- [`get_Annuity_Amount`](#get-annuity-amount) — function (spec line 258)
- [`is_Payment_Date`](#is-payment-date) — function (spec line 283)
- [`do_plan_control`](#do-plan-control) — procedure (spec line 336)
- [`do_schedule_allignment`](#do-schedule-allignment) — procedure (spec line 431)
- [`do_com_schedule_allignment`](#do-com-schedule-allignment) — procedure (spec line 441)
- [`calculate_xirr`](#calculate-xirr) — function (spec line 467)
- [`get_min_flow_ratio`](#get-min-flow-ratio) — function (spec line 475)
- [`get_flow_ratio_info`](#get-flow-ratio-info) — function (spec line 499)
- [`get_stop_ratio_info`](#get-stop-ratio-info) — function (spec line 504)
- [`get_incorrect_days`](#get-incorrect-days) — function (spec line 510)
- [`get_incorrect_days_count`](#get-incorrect-days-count) — function (spec line 513)
- [`get_schedule_from_memo`](#get-schedule-from-memo) — function (spec line 515)
- [`get_standart_schedule`](#get-standart-schedule) — function (spec line 521)
- [`get_annuity_schedule`](#get-annuity-schedule) — function (spec line 542)
- [`get_created_schedule`](#get-created-schedule) — procedure (spec line 570)
- [`create_schedule`](#create-schedule) — procedure (spec line 572)

### Utilities & Configuration

- [`get_ovd_date`](#get-ovd-date) — function (spec line 229)

---

## Accounts & Balances

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 71; body declaration candidate line(s): 70, 736

**Signature**

```sql
-- *

  procedure get_pen_info_for_calc(p_date                   in date default glbl.getsysdate,
                                  p_doc_no                 in varchar2,
                                  p_acc_type               in varchar2,
                                  p_pen_calc_grace_days    in number,
                                  p_ovd_amount             out number,
                                  p_calculated_pen_day_cnt out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates` — FUNCTION

**Purpose:** Builds an interest calculation date collection based on EOD/SOD scheduling and the last calculation access date.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 80; body declaration candidate line(s): 259

**Signature**

```sql
function get_interest_calc_dates(p_last_calc_access_date in date,
                                   p_eod_sod               in varchar2,
                                   p_int_calc_at           in varchar2)
    return loan_api.g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates_ex` — FUNCTION

**Purpose:** Public function related to get interest calc dates ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 85; body declaration candidate line(s): 323

**Signature**

```sql
function get_interest_calc_dates_ex(p_date        in date,
                                      p_eod_sod     in varchar2,
                                      p_int_calc_at in varchar2)
    return g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info` — PROCEDURE

**Purpose:** Determines interest calculation day count and year-day basis from interest-calculation configuration.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 90; body declaration candidate line(s): 104

**Signature**

```sql
procedure get_interest_calc_info(p_last_calc_date       in date,
                                   p_pymt_day             in number,
                                   p_trn_date             in date,
                                   p_int_calc_type        in varchar2,
                                   p_rate_type            in varchar2,
                                   p_int_rate_periodicity in varchar2,
                                   p_calc_day_count       out number,
                                   p_year_day_count       out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info_ex` — PROCEDURE

**Purpose:** Public procedure related to get interest calc info ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 101; body declaration candidate line(s): 183

**Signature**

```sql
procedure get_interest_calc_info_ex(p_last_calc_date in date,
                                   p_pymt_day       in number,
                                   p_trn_date       in date,
                                   p_int_calc_type  in varchar2,
                                   p_calc_day_count out number,
                                   p_year_day_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `clear_addtional_data` — PROCEDURE

**Purpose:** Public procedure related to clear addtional data. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 109; body declaration candidate line(s): 378

**Signature**

```sql
procedure clear_addtional_data(p_state varchar2 default 'CLEAR');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_group` — PROCEDURE

**Purpose:** Public procedure related to add additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 111; body declaration candidate line(s): 404

**Signature**

```sql
procedure add_additional_group(p_tag_name varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_group` — PROCEDURE

**Purpose:** Public procedure related to end additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 113; body declaration candidate line(s): 410

**Signature**

```sql
procedure end_additional_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_main_group` — PROCEDURE

**Purpose:** Public procedure related to end additional main group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 114; body declaration candidate line(s): 398

**Signature**

```sql
procedure end_additional_main_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 115; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 117; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 118; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value varchar2,
                              p_new_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 122; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value date,
                              p_new_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `finalize_addtional_process` — PROCEDURE

**Purpose:** Finalizes accumulated additional information and executes mapped updates for the supplied identifiers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 125; body declaration candidate line(s): 480

**Signature**

```sql
procedure finalize_addtional_process(p_doc_no   varchar2,
                                       p_offer_id varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `reverse_update` — PROCEDURE

**Purpose:** Reads prior history additional information and attempts to restore recorded old values.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 128; body declaration candidate line(s): 591

**Signature**

```sql
procedure reverse_update(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_loan_amount` — FUNCTION

**Purpose:** Returns a loan amount using the TOTAL, DEBT, or DUE calculation mode and related account and schedule data.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 130; body declaration candidate line(s): 643

**Signature**

```sql
function get_loan_amount(p_doc_no      in varchar2,
                           p_amount_type in varchar2,
                           p_date        in date default glbl.getsysdate,
                           p_oper_type   in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_overdue_min_amount` — FUNCTION

**Purpose:** Public function related to get overdue min amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 136; body declaration candidate line(s): 719

**Signature**

```sql
function get_overdue_min_amount(p_product_code in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 137; body declaration candidate line(s): 70, 736

**Signature**

```sql
procedure get_pen_info_for_calc(p_date                in date default glbl.getsysdate,
                                  p_doc_no              in varchar2,
                                  p_pen_calc_grace_days in number,
                                  p_PEN_INT_RATIO       in number,
                                  p_ovd_amount_for_pen  out number,
                                  p_pen_calc_days_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_trn_caller_id` — FUNCTION

**Purpose:** Public function related to get trn caller id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 144; body declaration candidate line(s): 772

**Signature**

```sql
function get_trn_caller_id(p_oper_type in varchar2) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_voucher_data_from_query` — FUNCTION

**Purpose:** Executes a supplied SQL query with DBMS_SQL and maps returned column values for vouchers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 146; body declaration candidate line(s): 789

**Signature**

```sql
function get_voucher_data_from_query(p_query       in varchar2,
                                       p_result_type in varchar2)
    return g_col_value_tab_map;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_formatted_grace_from_list` — FUNCTION

**Purpose:** Public function related to get formatted grace from list. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 150; body declaration candidate line(s): 912

**Signature**

```sql
function get_formatted_grace_from_list(p_period_list in varchar2)
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_grace_info` — FUNCTION

**Purpose:** Public function related to get grace info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 153; body declaration candidate line(s): 952

**Signature**

```sql
function get_grace_info(p_Doc_No          In Varchar2,
                          p_period_end_date in date,
                          p_acc_type        In Varchar2 default 'A',
                          p_info_type       in varchar2) Return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_basis_year_days_cnt` — FUNCTION

**Purpose:** Public function related to get basis year days cnt. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 158; body declaration candidate line(s): 998

**Signature**

```sql
function get_basis_year_days_cnt(p_int_calc_type in varchar2,
                                   p_date          in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_value` — FUNCTION

**Purpose:** Public function related to get gl value. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 161; body declaration candidate line(s): 1026

**Signature**

```sql
function get_gl_value(p_parameter_name in varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 163; body declaration candidate line(s): 1043

**Signature**

```sql
procedure loan_int_diff_operation(p_trn_date        in date,
                                    p_oper_type       in varchar2,
                                    p_trn_type        in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation_ex` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 177; body declaration candidate line(s): 1197

**Signature**

```sql
procedure loan_int_diff_operation_ex(p_oper_type       in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_active_passive` — FUNCTION

**Purpose:** Public function related to get gl acc active passive. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 189; body declaration candidate line(s): 1345

**Signature**

```sql
function get_gl_acc_active_passive(p_acc_no in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_from_matrix` — FUNCTION

**Purpose:** Public function related to get gl acc from matrix. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 191; body declaration candidate line(s): 1367

**Signature**

```sql
function get_gl_acc_from_matrix(p_product_code in number default null,
                                  p_cust_type    in number default null,
                                  p_period_id    in number default null,
                                  p_currency_id  in number default null,
                                  p_base_type    in varchar2,
                                  p_loan_doc_no  in varchar2 default null,
                                  p_customer_no  in varchar2 default null,
                                  p_acc_type     in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `Get_Delay_Int_Rate` — FUNCTION

**Purpose:** Public function related to get delay int rate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 200; body declaration candidate line(s): 1602

**Signature**

```sql
-- krd_eod.Get_Delay_Int_Rate
  Function Get_Delay_Int_Rate(p_Loan_Id    In Varchar2,
                              p_Delay_Type In Varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_commission_schedule` — FUNCTION

**Purpose:** Public function related to get commission schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 203; body declaration candidate line(s): 1628

**Signature**

```sql
-- kredi_api.Get_Krd_Kom_Plan
  Function get_commission_schedule(p_begin_date    In Date,
                                   p_end_date      In Date,
                                   p_amount        In Number,
                                   p_int_calc_type in varchar2)
    Return Krd_Kom_Plan_Tt
    Pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_months_for_loan` — FUNCTION

**Purpose:** Public function related to add months for loan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 211; body declaration candidate line(s): 1744

**Signature**

```sql
function add_months_for_loan(p_date   date,
                               p_months number,
                               p_day    number default null) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_next_Plan_Pym` — FUNCTION

**Purpose:** Public function related to get next plan pym. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 215; body declaration candidate line(s): 1776

**Signature**

```sql
Function get_next_Plan_Pym(p_doc_no   In Varchar2,
                             P_date     In Date,
                             p_acc_type in varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_offer_id` — FUNCTION

**Purpose:** Public function related to get offer id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 219; body declaration candidate line(s): 1809

**Signature**

```sql
Function get_offer_id(p_branch_id In Number Default Glbl.Getsube,
                        P_date      In Date Default Glbl.Getsysdate)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_payment_amount` — FUNCTION

**Purpose:** Public function related to get plan payment amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 223; body declaration candidate line(s): 1832

**Signature**

```sql
-- krd_eod.get_Plan_Pym +
  function get_plan_payment_amount(p_doc_no   in varchar2,
                                   p_date     in date default glbl.getsysdate,
                                   p_acc_type in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_ovd_date` — FUNCTION

**Purpose:** Public function related to get ovd date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 229; body declaration candidate line(s): 2734

**Signature**

```sql
Function get_ovd_date(p_doc_no   varchar2,
                        p_acc_type varchar2,
                        p_date     date default glbl.getsysdate) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_amount_for_pen_calc` — FUNCTION

**Purpose:** Public function related to get amount for pen calc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 233; body declaration candidate line(s): 1850

**Signature**

```sql
Function get_amount_for_pen_calc(p_doc_no        In Varchar2,
                                   P_date          In Date,
                                   p_for_spec_days in varchar2 default 'N',
                                   p_int_calc_type in varchar2 default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Plan_Month_Count` — FUNCTION

**Purpose:** Public function related to get plan month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 239; body declaration candidate line(s): 1944

**Signature**

```sql
-- kredi_api.get_Plan_Month_Count +
  /*Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ')
    Return Number;*/
  Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ',
                                p_work_days     varchar2 default 'Y',
                                p_pymt_day      number default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_paid_month_count` — FUNCTION

**Purpose:** Public function related to get plan paid month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 251; body declaration candidate line(s): 1987

**Signature**

```sql
-- new
  function get_plan_paid_month_count(p_doc_no in varchar2,
                                     p_term   in number,
                                     p_date   in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_error` — FUNCTION

**Purpose:** Public function related to get plan error. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 255; body declaration candidate line(s): 2047

**Signature**

```sql
-- kredi_api.get_plan_error +
  Function get_plan_error(p_doc_no varchar2, p_date date default glbl.getsysdate) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Annuity_Amount` — FUNCTION

**Purpose:** Public function related to get annuity amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 258; body declaration candidate line(s): 2604

**Signature**

```sql
-- kredi_api.Get_Annuitet_Amount +
  Function get_Annuity_Amount(p_Doc_No      In Varchar2,
                              p_return_type In varchar2 default 'NO_ZERO')
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Pym_Startdate` — FUNCTION

**Purpose:** Public function related to get pym startdate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 263; body declaration candidate line(s): 2633

**Signature**

```sql
-- kredi_api.Get_Pym_Startdate +
  Function get_Pym_Startdate(p_Doc_No          In Varchar2,
                             p_pymt_date       In Date,
                             p_pymt_day        In Number,
                             p_pymt_period     In Number,
                             p_acc_type        In varchar2,
                             p_loan_end_Date   in date,
                             p_check_is_closed in varchar2 default 'Y')
    Return Date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_account_feature` — FUNCTION

**Purpose:** Public function related to get account feature. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 273; body declaration candidate line(s): 2799

**Signature**

```sql
function get_account_feature(p_branch_no   number,
                               p_account_no  number,
                               p_account_sub number)
    return cs_account.account_feature%type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_acc_exists` — FUNCTION

**Purpose:** Public function related to is acc exists. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 278; body declaration candidate line(s): 2818

**Signature**

```sql
function is_acc_exists(p_customer_no   number,
                         p_memorandum_id varchar2 default null,
                         p_doc_no        varchar2,
                         p_acc_type      varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_Payment_Date` — FUNCTION

**Purpose:** Public function related to is payment date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 283; body declaration candidate line(s): 2845

**Signature**

```sql
-- kredi_api.Is_Payment_Date +
  Function is_Payment_Date(p_Document_No In Varchar2, p_Date Date)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_online_offer` — FUNCTION

**Purpose:** Public function related to is online offer. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 287; body declaration candidate line(s): 2858

**Signature**

```sql
function is_online_offer(p_memorandum_id varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `table_log_operation` — PROCEDURE

**Purpose:** Public procedure related to table log operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 289; body declaration candidate line(s): 3344

**Signature**

```sql
procedure table_log_operation(p_doc_no     in varchar2,
                                p_table_name in varchar2,
                                p_tx_fid     in number,
                                p_oper_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_entry` — PROCEDURE

**Purpose:** Public procedure related to do journal entry. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 294; body declaration candidate line(s): 2876

**Signature**

```sql
Procedure do_journal_entry(p_entries_list  g_entries_list_tab,
                             p_trn_caller_id in number,
                             p_tx_fid        in out number,
                             p_trn_type      in varchar2,
                             p_is_eod        in varchar2 default 'Y');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_journal_entries` — PROCEDURE

**Purpose:** Public procedure related to create journal entries. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 300; body declaration candidate line(s): 2954

**Signature**

```sql
procedure create_journal_entries(p_oper_type in varchar2,
                                   p_tx_fid    in number,
                                   p_trn_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_account` — PROCEDURE

**Purpose:** Creates/assigns loan-related accounts based on the requested operation and returns the created account list.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 304; body declaration candidate line(s): 3129

**Signature**

```sql
procedure create_account(p_doc_no        in varchar2,
                           p_memorandum_id in varchar2 default null,
                           p_oper_type     in varchar2,
                           p_acc_type      in varchar2 default null,
                           p_tx_fid        in number,
                           p_created_acc   out g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `recalculate_int_payment_plan` — PROCEDURE

**Purpose:** Public procedure related to recalculate int payment plan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 311; body declaration candidate line(s): 3445

**Signature**

```sql
procedure recalculate_int_payment_plan(p_doc_no               in varchar2,
                                         p_acc_type             in varchar2,
                                         p_main_amount          in number,
                                         p_INT_RATIO            in number,
                                         p_int_calc_type        in varchar2,
                                         p_schedule_update_type in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_new_acc` — FUNCTION

**Purpose:** Public function related to get new acc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 318; body declaration candidate line(s): 2520

**Signature**

```sql
--kredi_api.open_new_acc +
  function get_new_acc(p_branch_no       in number,
                       p_customer_no     in number,
                       p_balance_acc     in varchar2,
                       p_detail_code     in varchar2,
                       p_ccy_id          in number,
                       p_main_acc        in number default null,
                       p_cr_int_rate     in number default null,
                       p_dr_int_rate     in number default null,
                       p_com_int_rate    in number default null,
                       p_product_code    in number default null,
                       p_period_id       in number default null,
                       p_acc_description in varchar2,
                       p_memorandum_id   in varchar2 default null,
                       p_loan_doc_no     in varchar2,
                       p_loan_acc_type   in varchar2,
                       p_tx_fid          in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_plan_control` — PROCEDURE

**Purpose:** Public procedure related to do plan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 336; body declaration candidate line(s): 3506

**Signature**

```sql
-- kredi_api.plan_control +
  procedure do_plan_control(p_document_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_status_control` — PROCEDURE

**Purpose:** Public procedure related to do loan status control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 338; body declaration candidate line(s): 3515

**Signature**

```sql
-- kredi_api.loan_status_control +
  procedure do_loan_status_control(p_branch_no   in number,
                                   p_customer_no in number,
                                   p_loan_acc    in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_loan_history` — PROCEDURE

**Purpose:** Writes a loan-operation history record for a transaction.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 343; body declaration candidate line(s): 3587

**Signature**

```sql
procedure create_loan_history(p_oper_type VARCHAR2 default null,
                                p_doc_no    VARCHAR2 default null,
                                p_trn_date  DATE default glbl.getsysdate,
                                p_tx_fid    NUMBER,
                                p_trn_type  varchar2,
                                p_add_info  add_info_tab default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_collateral_out` — PROCEDURE

**Purpose:** Public procedure related to do loan collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 350; body declaration candidate line(s): 3942

**Signature**

```sql
--krd_eod.loan_collateral_out +
  procedure do_loan_collateral_out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_acc_type_by_status` — FUNCTION

**Purpose:** Public function related to get acc type by status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 353; body declaration candidate line(s): 4211

**Signature**

```sql
function get_acc_type_by_status(p_acc_type         varchar2,
                                  p_to_loan_status   varchar2,
                                  p_from_loan_status varchar2 default 'NORM')
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `generate_allocated_payment_list` — PROCEDURE

**Purpose:** Computes a payment allocation list for a loan operation.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 358; body declaration candidate line(s): 4239

**Signature**

```sql
procedure generate_allocated_payment_list(p_doc_no                in varchar2,
                                            p_oper_type             in varchar2,
                                            p_pym_amount            in number,
                                            p_has_schedule_upd_type out varchar2,
                                            p_payment_list          out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_payment_details` — PROCEDURE

**Purpose:** Public procedure related to add payment details. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 364; body declaration candidate line(s): 4389

**Signature**

```sql
procedure add_payment_details(p_doc_no                in varchar2,
                                p_has_schedule_upd_type out varchar2,
                                p_payment_list          in out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_delete_operation` — PROCEDURE

**Purpose:** Public procedure related to do delete operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 368; body declaration candidate line(s): 4483

**Signature**

```sql
procedure do_delete_operation(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Auto_Payment` — PROCEDURE

**Purpose:** Executes automatic loan payment processing in EOD/SOD context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 370; body declaration candidate line(s): 4540

**Signature**

```sql
/** Makes automatic loan payments at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S                           
  */
  Procedure do_Auto_Payment(p_min_id     number default null,
                            p_max_id     number default null,
                            p_doc_no     in varchar2 default null,
                            p_eod_sod    in varchar2 default 'E',
                            p_test_param in number default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation` — PROCEDURE

**Purpose:** Performs batch interest calculation with optional branch range, loan document and EOD/SOD arguments.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 382; body declaration candidate line(s): 5135

**Signature**

```sql
/** Makes automatic loan int calculation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S 
      p_date - operation date                            
  */
  
  procedure do_int_calculation(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation_ex` — PROCEDURE

**Purpose:** Public procedure related to do int calculation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 396; body declaration candidate line(s): 5768

**Signature**

```sql
procedure do_int_calculation_ex(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_overdue_transit_operation` — PROCEDURE

**Purpose:** Public procedure related to do overdue transit operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 402; body declaration candidate line(s): 4832

**Signature**

```sql
/** Makes automatic loan overdue operation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_branch_id - loan branch id  
      p_customer_no - unique customer number 
      p_loan_acc - loan account sub 
      p_date - operation date                            
  */

  Procedure do_overdue_transit_operation(p_min_id number default null,
                                         p_max_id number default null,
                                         p_doc_no in varchar2 default null,
                                         p_date   in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_commission_recognition` — PROCEDURE

**Purpose:** Public procedure related to do commission recognition. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 416; body declaration candidate line(s): 6338

**Signature**

```sql
Procedure do_commission_recognition(Pdate In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_guarantee_out` — PROCEDURE

**Purpose:** Public procedure related to do guarantee out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 418; body declaration candidate line(s): 6236

**Signature**

```sql
Procedure do_guarantee_out(p_branch_id   In Number Default Null,
                             p_customer_no In Number Default Null,
                             p_loan_acc    In Number Default Null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Close_With_Collateral_Out` — PROCEDURE

**Purpose:** Public procedure related to do loan close with collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 422; body declaration candidate line(s): 6594

**Signature**

```sql
procedure do_Loan_Close_With_Collateral_Out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_non_cash_loan_close` — PROCEDURE

**Purpose:** Public procedure related to do non cash loan close. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 424; body declaration candidate line(s): 6756

**Signature**

```sql
Procedure do_non_cash_loan_close(p_doc_no in varchar2,
                                   p_Date   In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_control` — PROCEDURE

**Purpose:** Public procedure related to do journal control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 427; body declaration candidate line(s): 6861

**Signature**

```sql
-- new
  procedure do_journal_control(p_branch_id   IN Number,
                               p_customer_no IN Number,
                               p_account_sub IN Number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 431; body declaration candidate line(s): 7118

**Signature**

```sql
-- new
  /*procedure over_to_norm(p_min_id  number default null,
                              p_max_id  number default null,
                              p_doc_no  in varchar2 default null);
  */
  --kredi_api.Odeme_Plani_Duzenle
  Procedure do_schedule_allignment(p_doc_no         In Varchar2,
                                   p_payment_amount In Number,
                                   p_acc_type       In Varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_com_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do com schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 441; body declaration candidate line(s): 7190

**Signature**

```sql
-- kredi_api.Kom_Odeme_Plani_Duzenle
  Procedure do_com_schedule_allignment(p_doc_no      In Varchar2,
                                       p_option_code In Varchar2,
                                       p_amount      In Number,
                                       p_plan_type   In Varchar2,
                                       p_mig_status  In Number Default 0);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Delay_Int_Rate_Upd` — PROCEDURE

**Purpose:** Public procedure related to do loan delay int rate upd. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 448; body declaration candidate line(s): 7310

**Signature**

```sql
-- krd_eod.Loan_Delay_Int_Rate_Upd
  Procedure do_Loan_Delay_Int_Rate_Upd;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `change_account_status` — PROCEDURE

**Purpose:** Public procedure related to change account status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 451; body declaration candidate line(s): 7351

**Signature**

```sql
-- kredi_api.Kredi_Hesap_Kapat , kredi_api.Kredi_Hesap_Ac
  procedure change_account_status(p_doc_no in varchar2,
                                  p_status in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_eod_task` — PROCEDURE

**Purpose:** Public procedure related to stop eod task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 455; body declaration candidate line(s): 7389

**Signature**

```sql
procedure stop_eod_task;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_loan_task` — PROCEDURE

**Purpose:** Public procedure related to stop loan task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 457; body declaration candidate line(s): 7405

**Signature**

```sql
procedure stop_loan_task(p_task_code in varchar2 default null,
                           p_task_type in varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `run_loan_task` — PROCEDURE

**Purpose:** Runs a task identified by its task code and task type.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 460; body declaration candidate line(s): 7442

**Signature**

```sql
/** Parallel execution for loan processes
      @params
      p_task_code  - task_code in loan_tasks_list table                  
  */

  procedure run_loan_task(p_task_code in varchar2, p_task_type in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `calculate_xirr` — FUNCTION

**Purpose:** Public function related to calculate xirr. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 467; body declaration candidate line(s): 7786

**Signature**

```sql
/*procedure norm_to_over(p_min_id  number default null,
  p_max_id  number default null,
  p_doc_no  in varchar2 default null);  */

  function calculate_xirr(p_doc_no  varchar2,
                          p_type    varchar2,
                          p_calc_as varchar2 default 'XIRR') return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_min_flow_ratio` — FUNCTION

**Purpose:** Public function related to get min flow ratio. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 475; body declaration candidate line(s): 8074

**Signature**

```sql
/*  function get_mix_operation_acsess(p_fid            varchar2,
                                      p_oper_type      varchar2,
                                      p_memo_oper_type varchar2) return number;
  
    function get_mix_operation_types(p_fid            varchar2,
                                     p_memo_oper_type varchar2) return varchar2;
  
    procedure validate_mix_memorandum(p_memorandum_id varchar2,
                                      p_oper_type     varchar2,
                                      p_state         varchar2);
  
    procedure update_mix_memorandum(p_memorandum_id varchar2,
                                    p_oper_type     varchar2,
                                    p_tx_fid        number,
                                    p_state         varchar2);
  */

  function get_min_flow_ratio(
    p_doc_no     varchar2,
    p_type       varchar2,
    p_begin_date date default null,
    p_end_date   date default null
  ) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_flow_ratio_info` — FUNCTION

**Purpose:** Public function related to get flow ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 499; body declaration candidate line(s): 8115

**Signature**

```sql
FUNCTION get_flow_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N')
    RETURN LOAN_FLOW_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_stop_ratio_info` — FUNCTION

**Purpose:** Public function related to get stop ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 504; body declaration candidate line(s): 8151

**Signature**

```sql
FUNCTION get_stop_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N',
                               p_info_type varchar2 default 'INT')
    RETURN LOAN_STOP_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days` — FUNCTION

**Purpose:** Public function related to get incorrect days. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 510; body declaration candidate line(s): 8179

**Signature**

```sql
function get_incorrect_days(p_date date) return NUMBER_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days_count` — FUNCTION

**Purpose:** Public function related to get incorrect days count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 513; body declaration candidate line(s): 8218

**Signature**

```sql
function get_incorrect_days_count(p_date date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_schedule_from_memo` — FUNCTION

**Purpose:** Public function related to get schedule from memo. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 515; body declaration candidate line(s): 8225

**Signature**

```sql
function get_schedule_from_memo(p_memorandum_id varchar2,
                                  p_int_ratio     number,
                                  p_int_calc_type varchar2,
                                  p_int_amount    number) return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_standart_schedule` — FUNCTION

**Purpose:** Returns pipelined standard schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 521; body declaration candidate line(s): 8324

**Signature**

```sql
function get_standart_schedule(p_begin_date          date default glbl.getsysdate,
                                 p_main_pymt_date      date,
                                 p_int_pymt_date       date,
                                 p_pymt_day            number default null,
                                 p_end_date            date,
                                 p_offer_amount        number,
                                 p_ovd_main_amount     number default 0,
                                 p_int_calc_type       varchar2,
                                 p_main_grace_period   varchar2 default null,
                                 p_int_grace_period    varchar2 default null,
                                 p_remain_int_amount   number default 0,
                                 p_min_main_pay_amount number default null,
                                 p_calc_int_in_grace   varchar2 default 'Y',
                                 p_work_days           varchar2 default 'Y',
                                 
                                 p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                 p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_annuity_schedule` — FUNCTION

**Purpose:** Returns pipelined annuity schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 542; body declaration candidate line(s): 8697

**Signature**

```sql
function get_annuity_schedule(p_begin_date      date,
                                p_main_pymt_date  date,
                                p_int_pymt_date   date,
                                p_pymt_day        number default null,
                                p_end_date        date,
                                p_offer_amount    number,
                                p_ovd_main_amount number default 0,
                                p_int_calc_type   varchar2,
                                
                                p_main_grace_period varchar2 default null,
                                p_int_grace_period  varchar2 default null,
                                
                                p_annuity_amount     number default null,
                                p_max_annuity_amount number default null,
                                p_remain_int_amount  number default 0,
                                
                                p_work_days         varchar2 default 'Y',
                                p_own_annuity       varchar2 default 'N',
                                p_calc_int_in_grace varchar2 default 'Y',
                                p_is_mortgage       varchar2 default 'N',
                                
                                p_max_iteration number default null,
                                
                                p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_created_schedule` — PROCEDURE

**Purpose:** Public procedure related to get created schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 570; body declaration candidate line(s): 9306

**Signature**

```sql
Procedure get_created_schedule(p_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_schedule` — PROCEDURE

**Purpose:** Builds a payment schedule using the supplied dates, amounts, interest and schedule options.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 572; body declaration candidate line(s): 9392

**Signature**

```sql
-- new
  procedure create_schedule(p_schedule_no         number,
                            p_coll_name           varchar2 default null,
                            p_fk_id               number default null,
                            p_doc_no              varchar2 default 'XXX',
                            p_memorandum_id       varchar2 default null,
                            p_customer_no         number default null,
                            p_tx_fid              number default null,
                            p_begin_date          date default glbl.getsysdate,
                            p_main_pymt_date      date,
                            p_int_pymt_date       date,
                            p_pymt_day            number default null,
                            p_end_date            date,
                            p_offer_amount        number,
                            p_ovd_main_amount     number default 0,
                            p_int_ratio           number,
                            p_int_calc_type       varchar2,
                            p_annuity_amount      number default null,
                            p_max_annuity_amount  number default null,
                            p_min_main_pay_amount number default null,
                            p_remain_int_amount   number default 0,
                            p_main_grace_period   varchar2 default null,
                            p_int_grace_period    varchar2 default null,
                            p_main_pymt_period    number default 1,
                            p_int_pymt_period     number default 1,
                            p_product_code        number default null,
                            p_same_annuity        varchar2 default 'N',
                            p_calc_int_in_grace   varchar2 default 'Y',
                            p_return_type         varchar2 default 'NO_ZERO',
                            p_loan_flow_rate_tab  LOAN_FLOW_RATE_TAB default null,
                            p_loan_stop_rate_tab  LOAN_STOP_RATE_TAB default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 604; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 607; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate,
                            p_min_rowid rowid,
                            p_max_rowid rowid);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

## EOD/SOD & Operations

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 71; body declaration candidate line(s): 70, 736

**Signature**

```sql
-- *

  procedure get_pen_info_for_calc(p_date                   in date default glbl.getsysdate,
                                  p_doc_no                 in varchar2,
                                  p_acc_type               in varchar2,
                                  p_pen_calc_grace_days    in number,
                                  p_ovd_amount             out number,
                                  p_calculated_pen_day_cnt out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates` — FUNCTION

**Purpose:** Builds an interest calculation date collection based on EOD/SOD scheduling and the last calculation access date.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 80; body declaration candidate line(s): 259

**Signature**

```sql
function get_interest_calc_dates(p_last_calc_access_date in date,
                                   p_eod_sod               in varchar2,
                                   p_int_calc_at           in varchar2)
    return loan_api.g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates_ex` — FUNCTION

**Purpose:** Public function related to get interest calc dates ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 85; body declaration candidate line(s): 323

**Signature**

```sql
function get_interest_calc_dates_ex(p_date        in date,
                                      p_eod_sod     in varchar2,
                                      p_int_calc_at in varchar2)
    return g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info` — PROCEDURE

**Purpose:** Determines interest calculation day count and year-day basis from interest-calculation configuration.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 90; body declaration candidate line(s): 104

**Signature**

```sql
procedure get_interest_calc_info(p_last_calc_date       in date,
                                   p_pymt_day             in number,
                                   p_trn_date             in date,
                                   p_int_calc_type        in varchar2,
                                   p_rate_type            in varchar2,
                                   p_int_rate_periodicity in varchar2,
                                   p_calc_day_count       out number,
                                   p_year_day_count       out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info_ex` — PROCEDURE

**Purpose:** Public procedure related to get interest calc info ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 101; body declaration candidate line(s): 183

**Signature**

```sql
procedure get_interest_calc_info_ex(p_last_calc_date in date,
                                   p_pymt_day       in number,
                                   p_trn_date       in date,
                                   p_int_calc_type  in varchar2,
                                   p_calc_day_count out number,
                                   p_year_day_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `clear_addtional_data` — PROCEDURE

**Purpose:** Public procedure related to clear addtional data. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 109; body declaration candidate line(s): 378

**Signature**

```sql
procedure clear_addtional_data(p_state varchar2 default 'CLEAR');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_group` — PROCEDURE

**Purpose:** Public procedure related to add additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 111; body declaration candidate line(s): 404

**Signature**

```sql
procedure add_additional_group(p_tag_name varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_group` — PROCEDURE

**Purpose:** Public procedure related to end additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 113; body declaration candidate line(s): 410

**Signature**

```sql
procedure end_additional_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_main_group` — PROCEDURE

**Purpose:** Public procedure related to end additional main group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 114; body declaration candidate line(s): 398

**Signature**

```sql
procedure end_additional_main_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 115; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 117; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 118; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value varchar2,
                              p_new_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 122; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value date,
                              p_new_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `finalize_addtional_process` — PROCEDURE

**Purpose:** Finalizes accumulated additional information and executes mapped updates for the supplied identifiers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 125; body declaration candidate line(s): 480

**Signature**

```sql
procedure finalize_addtional_process(p_doc_no   varchar2,
                                       p_offer_id varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `reverse_update` — PROCEDURE

**Purpose:** Reads prior history additional information and attempts to restore recorded old values.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 128; body declaration candidate line(s): 591

**Signature**

```sql
procedure reverse_update(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_loan_amount` — FUNCTION

**Purpose:** Returns a loan amount using the TOTAL, DEBT, or DUE calculation mode and related account and schedule data.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 130; body declaration candidate line(s): 643

**Signature**

```sql
function get_loan_amount(p_doc_no      in varchar2,
                           p_amount_type in varchar2,
                           p_date        in date default glbl.getsysdate,
                           p_oper_type   in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_overdue_min_amount` — FUNCTION

**Purpose:** Public function related to get overdue min amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 136; body declaration candidate line(s): 719

**Signature**

```sql
function get_overdue_min_amount(p_product_code in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 137; body declaration candidate line(s): 70, 736

**Signature**

```sql
procedure get_pen_info_for_calc(p_date                in date default glbl.getsysdate,
                                  p_doc_no              in varchar2,
                                  p_pen_calc_grace_days in number,
                                  p_PEN_INT_RATIO       in number,
                                  p_ovd_amount_for_pen  out number,
                                  p_pen_calc_days_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_trn_caller_id` — FUNCTION

**Purpose:** Public function related to get trn caller id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 144; body declaration candidate line(s): 772

**Signature**

```sql
function get_trn_caller_id(p_oper_type in varchar2) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_voucher_data_from_query` — FUNCTION

**Purpose:** Executes a supplied SQL query with DBMS_SQL and maps returned column values for vouchers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 146; body declaration candidate line(s): 789

**Signature**

```sql
function get_voucher_data_from_query(p_query       in varchar2,
                                       p_result_type in varchar2)
    return g_col_value_tab_map;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_formatted_grace_from_list` — FUNCTION

**Purpose:** Public function related to get formatted grace from list. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 150; body declaration candidate line(s): 912

**Signature**

```sql
function get_formatted_grace_from_list(p_period_list in varchar2)
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_grace_info` — FUNCTION

**Purpose:** Public function related to get grace info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 153; body declaration candidate line(s): 952

**Signature**

```sql
function get_grace_info(p_Doc_No          In Varchar2,
                          p_period_end_date in date,
                          p_acc_type        In Varchar2 default 'A',
                          p_info_type       in varchar2) Return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_basis_year_days_cnt` — FUNCTION

**Purpose:** Public function related to get basis year days cnt. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 158; body declaration candidate line(s): 998

**Signature**

```sql
function get_basis_year_days_cnt(p_int_calc_type in varchar2,
                                   p_date          in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_value` — FUNCTION

**Purpose:** Public function related to get gl value. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 161; body declaration candidate line(s): 1026

**Signature**

```sql
function get_gl_value(p_parameter_name in varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 163; body declaration candidate line(s): 1043

**Signature**

```sql
procedure loan_int_diff_operation(p_trn_date        in date,
                                    p_oper_type       in varchar2,
                                    p_trn_type        in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation_ex` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 177; body declaration candidate line(s): 1197

**Signature**

```sql
procedure loan_int_diff_operation_ex(p_oper_type       in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_active_passive` — FUNCTION

**Purpose:** Public function related to get gl acc active passive. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 189; body declaration candidate line(s): 1345

**Signature**

```sql
function get_gl_acc_active_passive(p_acc_no in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_from_matrix` — FUNCTION

**Purpose:** Public function related to get gl acc from matrix. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 191; body declaration candidate line(s): 1367

**Signature**

```sql
function get_gl_acc_from_matrix(p_product_code in number default null,
                                  p_cust_type    in number default null,
                                  p_period_id    in number default null,
                                  p_currency_id  in number default null,
                                  p_base_type    in varchar2,
                                  p_loan_doc_no  in varchar2 default null,
                                  p_customer_no  in varchar2 default null,
                                  p_acc_type     in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `Get_Delay_Int_Rate` — FUNCTION

**Purpose:** Public function related to get delay int rate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 200; body declaration candidate line(s): 1602

**Signature**

```sql
-- krd_eod.Get_Delay_Int_Rate
  Function Get_Delay_Int_Rate(p_Loan_Id    In Varchar2,
                              p_Delay_Type In Varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_commission_schedule` — FUNCTION

**Purpose:** Public function related to get commission schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 203; body declaration candidate line(s): 1628

**Signature**

```sql
-- kredi_api.Get_Krd_Kom_Plan
  Function get_commission_schedule(p_begin_date    In Date,
                                   p_end_date      In Date,
                                   p_amount        In Number,
                                   p_int_calc_type in varchar2)
    Return Krd_Kom_Plan_Tt
    Pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_months_for_loan` — FUNCTION

**Purpose:** Public function related to add months for loan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 211; body declaration candidate line(s): 1744

**Signature**

```sql
function add_months_for_loan(p_date   date,
                               p_months number,
                               p_day    number default null) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_next_Plan_Pym` — FUNCTION

**Purpose:** Public function related to get next plan pym. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 215; body declaration candidate line(s): 1776

**Signature**

```sql
Function get_next_Plan_Pym(p_doc_no   In Varchar2,
                             P_date     In Date,
                             p_acc_type in varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_offer_id` — FUNCTION

**Purpose:** Public function related to get offer id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 219; body declaration candidate line(s): 1809

**Signature**

```sql
Function get_offer_id(p_branch_id In Number Default Glbl.Getsube,
                        P_date      In Date Default Glbl.Getsysdate)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_payment_amount` — FUNCTION

**Purpose:** Public function related to get plan payment amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 223; body declaration candidate line(s): 1832

**Signature**

```sql
-- krd_eod.get_Plan_Pym +
  function get_plan_payment_amount(p_doc_no   in varchar2,
                                   p_date     in date default glbl.getsysdate,
                                   p_acc_type in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_ovd_date` — FUNCTION

**Purpose:** Public function related to get ovd date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 229; body declaration candidate line(s): 2734

**Signature**

```sql
Function get_ovd_date(p_doc_no   varchar2,
                        p_acc_type varchar2,
                        p_date     date default glbl.getsysdate) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_amount_for_pen_calc` — FUNCTION

**Purpose:** Public function related to get amount for pen calc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 233; body declaration candidate line(s): 1850

**Signature**

```sql
Function get_amount_for_pen_calc(p_doc_no        In Varchar2,
                                   P_date          In Date,
                                   p_for_spec_days in varchar2 default 'N',
                                   p_int_calc_type in varchar2 default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Plan_Month_Count` — FUNCTION

**Purpose:** Public function related to get plan month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 239; body declaration candidate line(s): 1944

**Signature**

```sql
-- kredi_api.get_Plan_Month_Count +
  /*Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ')
    Return Number;*/
  Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ',
                                p_work_days     varchar2 default 'Y',
                                p_pymt_day      number default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_paid_month_count` — FUNCTION

**Purpose:** Public function related to get plan paid month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 251; body declaration candidate line(s): 1987

**Signature**

```sql
-- new
  function get_plan_paid_month_count(p_doc_no in varchar2,
                                     p_term   in number,
                                     p_date   in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_error` — FUNCTION

**Purpose:** Public function related to get plan error. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 255; body declaration candidate line(s): 2047

**Signature**

```sql
-- kredi_api.get_plan_error +
  Function get_plan_error(p_doc_no varchar2, p_date date default glbl.getsysdate) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Annuity_Amount` — FUNCTION

**Purpose:** Public function related to get annuity amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 258; body declaration candidate line(s): 2604

**Signature**

```sql
-- kredi_api.Get_Annuitet_Amount +
  Function get_Annuity_Amount(p_Doc_No      In Varchar2,
                              p_return_type In varchar2 default 'NO_ZERO')
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Pym_Startdate` — FUNCTION

**Purpose:** Public function related to get pym startdate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 263; body declaration candidate line(s): 2633

**Signature**

```sql
-- kredi_api.Get_Pym_Startdate +
  Function get_Pym_Startdate(p_Doc_No          In Varchar2,
                             p_pymt_date       In Date,
                             p_pymt_day        In Number,
                             p_pymt_period     In Number,
                             p_acc_type        In varchar2,
                             p_loan_end_Date   in date,
                             p_check_is_closed in varchar2 default 'Y')
    Return Date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_account_feature` — FUNCTION

**Purpose:** Public function related to get account feature. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 273; body declaration candidate line(s): 2799

**Signature**

```sql
function get_account_feature(p_branch_no   number,
                               p_account_no  number,
                               p_account_sub number)
    return cs_account.account_feature%type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_acc_exists` — FUNCTION

**Purpose:** Public function related to is acc exists. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 278; body declaration candidate line(s): 2818

**Signature**

```sql
function is_acc_exists(p_customer_no   number,
                         p_memorandum_id varchar2 default null,
                         p_doc_no        varchar2,
                         p_acc_type      varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_Payment_Date` — FUNCTION

**Purpose:** Public function related to is payment date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 283; body declaration candidate line(s): 2845

**Signature**

```sql
-- kredi_api.Is_Payment_Date +
  Function is_Payment_Date(p_Document_No In Varchar2, p_Date Date)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_online_offer` — FUNCTION

**Purpose:** Public function related to is online offer. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 287; body declaration candidate line(s): 2858

**Signature**

```sql
function is_online_offer(p_memorandum_id varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `table_log_operation` — PROCEDURE

**Purpose:** Public procedure related to table log operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 289; body declaration candidate line(s): 3344

**Signature**

```sql
procedure table_log_operation(p_doc_no     in varchar2,
                                p_table_name in varchar2,
                                p_tx_fid     in number,
                                p_oper_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_entry` — PROCEDURE

**Purpose:** Public procedure related to do journal entry. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 294; body declaration candidate line(s): 2876

**Signature**

```sql
Procedure do_journal_entry(p_entries_list  g_entries_list_tab,
                             p_trn_caller_id in number,
                             p_tx_fid        in out number,
                             p_trn_type      in varchar2,
                             p_is_eod        in varchar2 default 'Y');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_journal_entries` — PROCEDURE

**Purpose:** Public procedure related to create journal entries. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 300; body declaration candidate line(s): 2954

**Signature**

```sql
procedure create_journal_entries(p_oper_type in varchar2,
                                   p_tx_fid    in number,
                                   p_trn_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_account` — PROCEDURE

**Purpose:** Creates/assigns loan-related accounts based on the requested operation and returns the created account list.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 304; body declaration candidate line(s): 3129

**Signature**

```sql
procedure create_account(p_doc_no        in varchar2,
                           p_memorandum_id in varchar2 default null,
                           p_oper_type     in varchar2,
                           p_acc_type      in varchar2 default null,
                           p_tx_fid        in number,
                           p_created_acc   out g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `recalculate_int_payment_plan` — PROCEDURE

**Purpose:** Public procedure related to recalculate int payment plan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 311; body declaration candidate line(s): 3445

**Signature**

```sql
procedure recalculate_int_payment_plan(p_doc_no               in varchar2,
                                         p_acc_type             in varchar2,
                                         p_main_amount          in number,
                                         p_INT_RATIO            in number,
                                         p_int_calc_type        in varchar2,
                                         p_schedule_update_type in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_new_acc` — FUNCTION

**Purpose:** Public function related to get new acc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 318; body declaration candidate line(s): 2520

**Signature**

```sql
--kredi_api.open_new_acc +
  function get_new_acc(p_branch_no       in number,
                       p_customer_no     in number,
                       p_balance_acc     in varchar2,
                       p_detail_code     in varchar2,
                       p_ccy_id          in number,
                       p_main_acc        in number default null,
                       p_cr_int_rate     in number default null,
                       p_dr_int_rate     in number default null,
                       p_com_int_rate    in number default null,
                       p_product_code    in number default null,
                       p_period_id       in number default null,
                       p_acc_description in varchar2,
                       p_memorandum_id   in varchar2 default null,
                       p_loan_doc_no     in varchar2,
                       p_loan_acc_type   in varchar2,
                       p_tx_fid          in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_plan_control` — PROCEDURE

**Purpose:** Public procedure related to do plan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 336; body declaration candidate line(s): 3506

**Signature**

```sql
-- kredi_api.plan_control +
  procedure do_plan_control(p_document_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_status_control` — PROCEDURE

**Purpose:** Public procedure related to do loan status control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 338; body declaration candidate line(s): 3515

**Signature**

```sql
-- kredi_api.loan_status_control +
  procedure do_loan_status_control(p_branch_no   in number,
                                   p_customer_no in number,
                                   p_loan_acc    in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_loan_history` — PROCEDURE

**Purpose:** Writes a loan-operation history record for a transaction.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 343; body declaration candidate line(s): 3587

**Signature**

```sql
procedure create_loan_history(p_oper_type VARCHAR2 default null,
                                p_doc_no    VARCHAR2 default null,
                                p_trn_date  DATE default glbl.getsysdate,
                                p_tx_fid    NUMBER,
                                p_trn_type  varchar2,
                                p_add_info  add_info_tab default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_collateral_out` — PROCEDURE

**Purpose:** Public procedure related to do loan collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 350; body declaration candidate line(s): 3942

**Signature**

```sql
--krd_eod.loan_collateral_out +
  procedure do_loan_collateral_out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_acc_type_by_status` — FUNCTION

**Purpose:** Public function related to get acc type by status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 353; body declaration candidate line(s): 4211

**Signature**

```sql
function get_acc_type_by_status(p_acc_type         varchar2,
                                  p_to_loan_status   varchar2,
                                  p_from_loan_status varchar2 default 'NORM')
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `generate_allocated_payment_list` — PROCEDURE

**Purpose:** Computes a payment allocation list for a loan operation.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 358; body declaration candidate line(s): 4239

**Signature**

```sql
procedure generate_allocated_payment_list(p_doc_no                in varchar2,
                                            p_oper_type             in varchar2,
                                            p_pym_amount            in number,
                                            p_has_schedule_upd_type out varchar2,
                                            p_payment_list          out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_payment_details` — PROCEDURE

**Purpose:** Public procedure related to add payment details. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 364; body declaration candidate line(s): 4389

**Signature**

```sql
procedure add_payment_details(p_doc_no                in varchar2,
                                p_has_schedule_upd_type out varchar2,
                                p_payment_list          in out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_delete_operation` — PROCEDURE

**Purpose:** Public procedure related to do delete operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 368; body declaration candidate line(s): 4483

**Signature**

```sql
procedure do_delete_operation(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Auto_Payment` — PROCEDURE

**Purpose:** Executes automatic loan payment processing in EOD/SOD context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 370; body declaration candidate line(s): 4540

**Signature**

```sql
/** Makes automatic loan payments at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S                           
  */
  Procedure do_Auto_Payment(p_min_id     number default null,
                            p_max_id     number default null,
                            p_doc_no     in varchar2 default null,
                            p_eod_sod    in varchar2 default 'E',
                            p_test_param in number default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation` — PROCEDURE

**Purpose:** Performs batch interest calculation with optional branch range, loan document and EOD/SOD arguments.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 382; body declaration candidate line(s): 5135

**Signature**

```sql
/** Makes automatic loan int calculation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S 
      p_date - operation date                            
  */
  
  procedure do_int_calculation(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation_ex` — PROCEDURE

**Purpose:** Public procedure related to do int calculation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 396; body declaration candidate line(s): 5768

**Signature**

```sql
procedure do_int_calculation_ex(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_overdue_transit_operation` — PROCEDURE

**Purpose:** Public procedure related to do overdue transit operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 402; body declaration candidate line(s): 4832

**Signature**

```sql
/** Makes automatic loan overdue operation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_branch_id - loan branch id  
      p_customer_no - unique customer number 
      p_loan_acc - loan account sub 
      p_date - operation date                            
  */

  Procedure do_overdue_transit_operation(p_min_id number default null,
                                         p_max_id number default null,
                                         p_doc_no in varchar2 default null,
                                         p_date   in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_commission_recognition` — PROCEDURE

**Purpose:** Public procedure related to do commission recognition. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 416; body declaration candidate line(s): 6338

**Signature**

```sql
Procedure do_commission_recognition(Pdate In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_guarantee_out` — PROCEDURE

**Purpose:** Public procedure related to do guarantee out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 418; body declaration candidate line(s): 6236

**Signature**

```sql
Procedure do_guarantee_out(p_branch_id   In Number Default Null,
                             p_customer_no In Number Default Null,
                             p_loan_acc    In Number Default Null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Close_With_Collateral_Out` — PROCEDURE

**Purpose:** Public procedure related to do loan close with collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 422; body declaration candidate line(s): 6594

**Signature**

```sql
procedure do_Loan_Close_With_Collateral_Out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_non_cash_loan_close` — PROCEDURE

**Purpose:** Public procedure related to do non cash loan close. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 424; body declaration candidate line(s): 6756

**Signature**

```sql
Procedure do_non_cash_loan_close(p_doc_no in varchar2,
                                   p_Date   In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_control` — PROCEDURE

**Purpose:** Public procedure related to do journal control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 427; body declaration candidate line(s): 6861

**Signature**

```sql
-- new
  procedure do_journal_control(p_branch_id   IN Number,
                               p_customer_no IN Number,
                               p_account_sub IN Number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 431; body declaration candidate line(s): 7118

**Signature**

```sql
-- new
  /*procedure over_to_norm(p_min_id  number default null,
                              p_max_id  number default null,
                              p_doc_no  in varchar2 default null);
  */
  --kredi_api.Odeme_Plani_Duzenle
  Procedure do_schedule_allignment(p_doc_no         In Varchar2,
                                   p_payment_amount In Number,
                                   p_acc_type       In Varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_com_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do com schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 441; body declaration candidate line(s): 7190

**Signature**

```sql
-- kredi_api.Kom_Odeme_Plani_Duzenle
  Procedure do_com_schedule_allignment(p_doc_no      In Varchar2,
                                       p_option_code In Varchar2,
                                       p_amount      In Number,
                                       p_plan_type   In Varchar2,
                                       p_mig_status  In Number Default 0);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Delay_Int_Rate_Upd` — PROCEDURE

**Purpose:** Public procedure related to do loan delay int rate upd. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 448; body declaration candidate line(s): 7310

**Signature**

```sql
-- krd_eod.Loan_Delay_Int_Rate_Upd
  Procedure do_Loan_Delay_Int_Rate_Upd;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `change_account_status` — PROCEDURE

**Purpose:** Public procedure related to change account status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 451; body declaration candidate line(s): 7351

**Signature**

```sql
-- kredi_api.Kredi_Hesap_Kapat , kredi_api.Kredi_Hesap_Ac
  procedure change_account_status(p_doc_no in varchar2,
                                  p_status in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_eod_task` — PROCEDURE

**Purpose:** Public procedure related to stop eod task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 455; body declaration candidate line(s): 7389

**Signature**

```sql
procedure stop_eod_task;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_loan_task` — PROCEDURE

**Purpose:** Public procedure related to stop loan task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 457; body declaration candidate line(s): 7405

**Signature**

```sql
procedure stop_loan_task(p_task_code in varchar2 default null,
                           p_task_type in varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `run_loan_task` — PROCEDURE

**Purpose:** Runs a task identified by its task code and task type.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 460; body declaration candidate line(s): 7442

**Signature**

```sql
/** Parallel execution for loan processes
      @params
      p_task_code  - task_code in loan_tasks_list table                  
  */

  procedure run_loan_task(p_task_code in varchar2, p_task_type in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `calculate_xirr` — FUNCTION

**Purpose:** Public function related to calculate xirr. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 467; body declaration candidate line(s): 7786

**Signature**

```sql
/*procedure norm_to_over(p_min_id  number default null,
  p_max_id  number default null,
  p_doc_no  in varchar2 default null);  */

  function calculate_xirr(p_doc_no  varchar2,
                          p_type    varchar2,
                          p_calc_as varchar2 default 'XIRR') return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_min_flow_ratio` — FUNCTION

**Purpose:** Public function related to get min flow ratio. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 475; body declaration candidate line(s): 8074

**Signature**

```sql
/*  function get_mix_operation_acsess(p_fid            varchar2,
                                      p_oper_type      varchar2,
                                      p_memo_oper_type varchar2) return number;
  
    function get_mix_operation_types(p_fid            varchar2,
                                     p_memo_oper_type varchar2) return varchar2;
  
    procedure validate_mix_memorandum(p_memorandum_id varchar2,
                                      p_oper_type     varchar2,
                                      p_state         varchar2);
  
    procedure update_mix_memorandum(p_memorandum_id varchar2,
                                    p_oper_type     varchar2,
                                    p_tx_fid        number,
                                    p_state         varchar2);
  */

  function get_min_flow_ratio(
    p_doc_no     varchar2,
    p_type       varchar2,
    p_begin_date date default null,
    p_end_date   date default null
  ) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_flow_ratio_info` — FUNCTION

**Purpose:** Public function related to get flow ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 499; body declaration candidate line(s): 8115

**Signature**

```sql
FUNCTION get_flow_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N')
    RETURN LOAN_FLOW_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_stop_ratio_info` — FUNCTION

**Purpose:** Public function related to get stop ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 504; body declaration candidate line(s): 8151

**Signature**

```sql
FUNCTION get_stop_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N',
                               p_info_type varchar2 default 'INT')
    RETURN LOAN_STOP_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days` — FUNCTION

**Purpose:** Public function related to get incorrect days. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 510; body declaration candidate line(s): 8179

**Signature**

```sql
function get_incorrect_days(p_date date) return NUMBER_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days_count` — FUNCTION

**Purpose:** Public function related to get incorrect days count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 513; body declaration candidate line(s): 8218

**Signature**

```sql
function get_incorrect_days_count(p_date date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_schedule_from_memo` — FUNCTION

**Purpose:** Public function related to get schedule from memo. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 515; body declaration candidate line(s): 8225

**Signature**

```sql
function get_schedule_from_memo(p_memorandum_id varchar2,
                                  p_int_ratio     number,
                                  p_int_calc_type varchar2,
                                  p_int_amount    number) return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_standart_schedule` — FUNCTION

**Purpose:** Returns pipelined standard schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 521; body declaration candidate line(s): 8324

**Signature**

```sql
function get_standart_schedule(p_begin_date          date default glbl.getsysdate,
                                 p_main_pymt_date      date,
                                 p_int_pymt_date       date,
                                 p_pymt_day            number default null,
                                 p_end_date            date,
                                 p_offer_amount        number,
                                 p_ovd_main_amount     number default 0,
                                 p_int_calc_type       varchar2,
                                 p_main_grace_period   varchar2 default null,
                                 p_int_grace_period    varchar2 default null,
                                 p_remain_int_amount   number default 0,
                                 p_min_main_pay_amount number default null,
                                 p_calc_int_in_grace   varchar2 default 'Y',
                                 p_work_days           varchar2 default 'Y',
                                 
                                 p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                 p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_annuity_schedule` — FUNCTION

**Purpose:** Returns pipelined annuity schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 542; body declaration candidate line(s): 8697

**Signature**

```sql
function get_annuity_schedule(p_begin_date      date,
                                p_main_pymt_date  date,
                                p_int_pymt_date   date,
                                p_pymt_day        number default null,
                                p_end_date        date,
                                p_offer_amount    number,
                                p_ovd_main_amount number default 0,
                                p_int_calc_type   varchar2,
                                
                                p_main_grace_period varchar2 default null,
                                p_int_grace_period  varchar2 default null,
                                
                                p_annuity_amount     number default null,
                                p_max_annuity_amount number default null,
                                p_remain_int_amount  number default 0,
                                
                                p_work_days         varchar2 default 'Y',
                                p_own_annuity       varchar2 default 'N',
                                p_calc_int_in_grace varchar2 default 'Y',
                                p_is_mortgage       varchar2 default 'N',
                                
                                p_max_iteration number default null,
                                
                                p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_created_schedule` — PROCEDURE

**Purpose:** Public procedure related to get created schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 570; body declaration candidate line(s): 9306

**Signature**

```sql
Procedure get_created_schedule(p_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_schedule` — PROCEDURE

**Purpose:** Builds a payment schedule using the supplied dates, amounts, interest and schedule options.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 572; body declaration candidate line(s): 9392

**Signature**

```sql
-- new
  procedure create_schedule(p_schedule_no         number,
                            p_coll_name           varchar2 default null,
                            p_fk_id               number default null,
                            p_doc_no              varchar2 default 'XXX',
                            p_memorandum_id       varchar2 default null,
                            p_customer_no         number default null,
                            p_tx_fid              number default null,
                            p_begin_date          date default glbl.getsysdate,
                            p_main_pymt_date      date,
                            p_int_pymt_date       date,
                            p_pymt_day            number default null,
                            p_end_date            date,
                            p_offer_amount        number,
                            p_ovd_main_amount     number default 0,
                            p_int_ratio           number,
                            p_int_calc_type       varchar2,
                            p_annuity_amount      number default null,
                            p_max_annuity_amount  number default null,
                            p_min_main_pay_amount number default null,
                            p_remain_int_amount   number default 0,
                            p_main_grace_period   varchar2 default null,
                            p_int_grace_period    varchar2 default null,
                            p_main_pymt_period    number default 1,
                            p_int_pymt_period     number default 1,
                            p_product_code        number default null,
                            p_same_annuity        varchar2 default 'N',
                            p_calc_int_in_grace   varchar2 default 'Y',
                            p_return_type         varchar2 default 'NO_ZERO',
                            p_loan_flow_rate_tab  LOAN_FLOW_RATE_TAB default null,
                            p_loan_stop_rate_tab  LOAN_STOP_RATE_TAB default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 604; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 607; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate,
                            p_min_rowid rowid,
                            p_max_rowid rowid);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

## History & Changes

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 71; body declaration candidate line(s): 70, 736

**Signature**

```sql
-- *

  procedure get_pen_info_for_calc(p_date                   in date default glbl.getsysdate,
                                  p_doc_no                 in varchar2,
                                  p_acc_type               in varchar2,
                                  p_pen_calc_grace_days    in number,
                                  p_ovd_amount             out number,
                                  p_calculated_pen_day_cnt out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates` — FUNCTION

**Purpose:** Builds an interest calculation date collection based on EOD/SOD scheduling and the last calculation access date.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 80; body declaration candidate line(s): 259

**Signature**

```sql
function get_interest_calc_dates(p_last_calc_access_date in date,
                                   p_eod_sod               in varchar2,
                                   p_int_calc_at           in varchar2)
    return loan_api.g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates_ex` — FUNCTION

**Purpose:** Public function related to get interest calc dates ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 85; body declaration candidate line(s): 323

**Signature**

```sql
function get_interest_calc_dates_ex(p_date        in date,
                                      p_eod_sod     in varchar2,
                                      p_int_calc_at in varchar2)
    return g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info` — PROCEDURE

**Purpose:** Determines interest calculation day count and year-day basis from interest-calculation configuration.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 90; body declaration candidate line(s): 104

**Signature**

```sql
procedure get_interest_calc_info(p_last_calc_date       in date,
                                   p_pymt_day             in number,
                                   p_trn_date             in date,
                                   p_int_calc_type        in varchar2,
                                   p_rate_type            in varchar2,
                                   p_int_rate_periodicity in varchar2,
                                   p_calc_day_count       out number,
                                   p_year_day_count       out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info_ex` — PROCEDURE

**Purpose:** Public procedure related to get interest calc info ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 101; body declaration candidate line(s): 183

**Signature**

```sql
procedure get_interest_calc_info_ex(p_last_calc_date in date,
                                   p_pymt_day       in number,
                                   p_trn_date       in date,
                                   p_int_calc_type  in varchar2,
                                   p_calc_day_count out number,
                                   p_year_day_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `clear_addtional_data` — PROCEDURE

**Purpose:** Public procedure related to clear addtional data. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 109; body declaration candidate line(s): 378

**Signature**

```sql
procedure clear_addtional_data(p_state varchar2 default 'CLEAR');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_group` — PROCEDURE

**Purpose:** Public procedure related to add additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 111; body declaration candidate line(s): 404

**Signature**

```sql
procedure add_additional_group(p_tag_name varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_group` — PROCEDURE

**Purpose:** Public procedure related to end additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 113; body declaration candidate line(s): 410

**Signature**

```sql
procedure end_additional_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_main_group` — PROCEDURE

**Purpose:** Public procedure related to end additional main group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 114; body declaration candidate line(s): 398

**Signature**

```sql
procedure end_additional_main_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 115; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 117; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 118; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value varchar2,
                              p_new_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 122; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value date,
                              p_new_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `finalize_addtional_process` — PROCEDURE

**Purpose:** Finalizes accumulated additional information and executes mapped updates for the supplied identifiers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 125; body declaration candidate line(s): 480

**Signature**

```sql
procedure finalize_addtional_process(p_doc_no   varchar2,
                                       p_offer_id varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `reverse_update` — PROCEDURE

**Purpose:** Reads prior history additional information and attempts to restore recorded old values.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 128; body declaration candidate line(s): 591

**Signature**

```sql
procedure reverse_update(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_loan_amount` — FUNCTION

**Purpose:** Returns a loan amount using the TOTAL, DEBT, or DUE calculation mode and related account and schedule data.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 130; body declaration candidate line(s): 643

**Signature**

```sql
function get_loan_amount(p_doc_no      in varchar2,
                           p_amount_type in varchar2,
                           p_date        in date default glbl.getsysdate,
                           p_oper_type   in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_overdue_min_amount` — FUNCTION

**Purpose:** Public function related to get overdue min amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 136; body declaration candidate line(s): 719

**Signature**

```sql
function get_overdue_min_amount(p_product_code in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 137; body declaration candidate line(s): 70, 736

**Signature**

```sql
procedure get_pen_info_for_calc(p_date                in date default glbl.getsysdate,
                                  p_doc_no              in varchar2,
                                  p_pen_calc_grace_days in number,
                                  p_PEN_INT_RATIO       in number,
                                  p_ovd_amount_for_pen  out number,
                                  p_pen_calc_days_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_trn_caller_id` — FUNCTION

**Purpose:** Public function related to get trn caller id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 144; body declaration candidate line(s): 772

**Signature**

```sql
function get_trn_caller_id(p_oper_type in varchar2) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_voucher_data_from_query` — FUNCTION

**Purpose:** Executes a supplied SQL query with DBMS_SQL and maps returned column values for vouchers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 146; body declaration candidate line(s): 789

**Signature**

```sql
function get_voucher_data_from_query(p_query       in varchar2,
                                       p_result_type in varchar2)
    return g_col_value_tab_map;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_formatted_grace_from_list` — FUNCTION

**Purpose:** Public function related to get formatted grace from list. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 150; body declaration candidate line(s): 912

**Signature**

```sql
function get_formatted_grace_from_list(p_period_list in varchar2)
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_grace_info` — FUNCTION

**Purpose:** Public function related to get grace info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 153; body declaration candidate line(s): 952

**Signature**

```sql
function get_grace_info(p_Doc_No          In Varchar2,
                          p_period_end_date in date,
                          p_acc_type        In Varchar2 default 'A',
                          p_info_type       in varchar2) Return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_basis_year_days_cnt` — FUNCTION

**Purpose:** Public function related to get basis year days cnt. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 158; body declaration candidate line(s): 998

**Signature**

```sql
function get_basis_year_days_cnt(p_int_calc_type in varchar2,
                                   p_date          in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_value` — FUNCTION

**Purpose:** Public function related to get gl value. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 161; body declaration candidate line(s): 1026

**Signature**

```sql
function get_gl_value(p_parameter_name in varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 163; body declaration candidate line(s): 1043

**Signature**

```sql
procedure loan_int_diff_operation(p_trn_date        in date,
                                    p_oper_type       in varchar2,
                                    p_trn_type        in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation_ex` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 177; body declaration candidate line(s): 1197

**Signature**

```sql
procedure loan_int_diff_operation_ex(p_oper_type       in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_active_passive` — FUNCTION

**Purpose:** Public function related to get gl acc active passive. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 189; body declaration candidate line(s): 1345

**Signature**

```sql
function get_gl_acc_active_passive(p_acc_no in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_from_matrix` — FUNCTION

**Purpose:** Public function related to get gl acc from matrix. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 191; body declaration candidate line(s): 1367

**Signature**

```sql
function get_gl_acc_from_matrix(p_product_code in number default null,
                                  p_cust_type    in number default null,
                                  p_period_id    in number default null,
                                  p_currency_id  in number default null,
                                  p_base_type    in varchar2,
                                  p_loan_doc_no  in varchar2 default null,
                                  p_customer_no  in varchar2 default null,
                                  p_acc_type     in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `Get_Delay_Int_Rate` — FUNCTION

**Purpose:** Public function related to get delay int rate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 200; body declaration candidate line(s): 1602

**Signature**

```sql
-- krd_eod.Get_Delay_Int_Rate
  Function Get_Delay_Int_Rate(p_Loan_Id    In Varchar2,
                              p_Delay_Type In Varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_commission_schedule` — FUNCTION

**Purpose:** Public function related to get commission schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 203; body declaration candidate line(s): 1628

**Signature**

```sql
-- kredi_api.Get_Krd_Kom_Plan
  Function get_commission_schedule(p_begin_date    In Date,
                                   p_end_date      In Date,
                                   p_amount        In Number,
                                   p_int_calc_type in varchar2)
    Return Krd_Kom_Plan_Tt
    Pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_months_for_loan` — FUNCTION

**Purpose:** Public function related to add months for loan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 211; body declaration candidate line(s): 1744

**Signature**

```sql
function add_months_for_loan(p_date   date,
                               p_months number,
                               p_day    number default null) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_next_Plan_Pym` — FUNCTION

**Purpose:** Public function related to get next plan pym. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 215; body declaration candidate line(s): 1776

**Signature**

```sql
Function get_next_Plan_Pym(p_doc_no   In Varchar2,
                             P_date     In Date,
                             p_acc_type in varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_offer_id` — FUNCTION

**Purpose:** Public function related to get offer id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 219; body declaration candidate line(s): 1809

**Signature**

```sql
Function get_offer_id(p_branch_id In Number Default Glbl.Getsube,
                        P_date      In Date Default Glbl.Getsysdate)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_payment_amount` — FUNCTION

**Purpose:** Public function related to get plan payment amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 223; body declaration candidate line(s): 1832

**Signature**

```sql
-- krd_eod.get_Plan_Pym +
  function get_plan_payment_amount(p_doc_no   in varchar2,
                                   p_date     in date default glbl.getsysdate,
                                   p_acc_type in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_ovd_date` — FUNCTION

**Purpose:** Public function related to get ovd date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 229; body declaration candidate line(s): 2734

**Signature**

```sql
Function get_ovd_date(p_doc_no   varchar2,
                        p_acc_type varchar2,
                        p_date     date default glbl.getsysdate) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_amount_for_pen_calc` — FUNCTION

**Purpose:** Public function related to get amount for pen calc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 233; body declaration candidate line(s): 1850

**Signature**

```sql
Function get_amount_for_pen_calc(p_doc_no        In Varchar2,
                                   P_date          In Date,
                                   p_for_spec_days in varchar2 default 'N',
                                   p_int_calc_type in varchar2 default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Plan_Month_Count` — FUNCTION

**Purpose:** Public function related to get plan month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 239; body declaration candidate line(s): 1944

**Signature**

```sql
-- kredi_api.get_Plan_Month_Count +
  /*Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ')
    Return Number;*/
  Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ',
                                p_work_days     varchar2 default 'Y',
                                p_pymt_day      number default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_paid_month_count` — FUNCTION

**Purpose:** Public function related to get plan paid month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 251; body declaration candidate line(s): 1987

**Signature**

```sql
-- new
  function get_plan_paid_month_count(p_doc_no in varchar2,
                                     p_term   in number,
                                     p_date   in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_error` — FUNCTION

**Purpose:** Public function related to get plan error. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 255; body declaration candidate line(s): 2047

**Signature**

```sql
-- kredi_api.get_plan_error +
  Function get_plan_error(p_doc_no varchar2, p_date date default glbl.getsysdate) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Annuity_Amount` — FUNCTION

**Purpose:** Public function related to get annuity amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 258; body declaration candidate line(s): 2604

**Signature**

```sql
-- kredi_api.Get_Annuitet_Amount +
  Function get_Annuity_Amount(p_Doc_No      In Varchar2,
                              p_return_type In varchar2 default 'NO_ZERO')
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Pym_Startdate` — FUNCTION

**Purpose:** Public function related to get pym startdate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 263; body declaration candidate line(s): 2633

**Signature**

```sql
-- kredi_api.Get_Pym_Startdate +
  Function get_Pym_Startdate(p_Doc_No          In Varchar2,
                             p_pymt_date       In Date,
                             p_pymt_day        In Number,
                             p_pymt_period     In Number,
                             p_acc_type        In varchar2,
                             p_loan_end_Date   in date,
                             p_check_is_closed in varchar2 default 'Y')
    Return Date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_account_feature` — FUNCTION

**Purpose:** Public function related to get account feature. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 273; body declaration candidate line(s): 2799

**Signature**

```sql
function get_account_feature(p_branch_no   number,
                               p_account_no  number,
                               p_account_sub number)
    return cs_account.account_feature%type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_acc_exists` — FUNCTION

**Purpose:** Public function related to is acc exists. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 278; body declaration candidate line(s): 2818

**Signature**

```sql
function is_acc_exists(p_customer_no   number,
                         p_memorandum_id varchar2 default null,
                         p_doc_no        varchar2,
                         p_acc_type      varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_Payment_Date` — FUNCTION

**Purpose:** Public function related to is payment date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 283; body declaration candidate line(s): 2845

**Signature**

```sql
-- kredi_api.Is_Payment_Date +
  Function is_Payment_Date(p_Document_No In Varchar2, p_Date Date)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_online_offer` — FUNCTION

**Purpose:** Public function related to is online offer. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 287; body declaration candidate line(s): 2858

**Signature**

```sql
function is_online_offer(p_memorandum_id varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `table_log_operation` — PROCEDURE

**Purpose:** Public procedure related to table log operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 289; body declaration candidate line(s): 3344

**Signature**

```sql
procedure table_log_operation(p_doc_no     in varchar2,
                                p_table_name in varchar2,
                                p_tx_fid     in number,
                                p_oper_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_entry` — PROCEDURE

**Purpose:** Public procedure related to do journal entry. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 294; body declaration candidate line(s): 2876

**Signature**

```sql
Procedure do_journal_entry(p_entries_list  g_entries_list_tab,
                             p_trn_caller_id in number,
                             p_tx_fid        in out number,
                             p_trn_type      in varchar2,
                             p_is_eod        in varchar2 default 'Y');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_journal_entries` — PROCEDURE

**Purpose:** Public procedure related to create journal entries. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 300; body declaration candidate line(s): 2954

**Signature**

```sql
procedure create_journal_entries(p_oper_type in varchar2,
                                   p_tx_fid    in number,
                                   p_trn_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_account` — PROCEDURE

**Purpose:** Creates/assigns loan-related accounts based on the requested operation and returns the created account list.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 304; body declaration candidate line(s): 3129

**Signature**

```sql
procedure create_account(p_doc_no        in varchar2,
                           p_memorandum_id in varchar2 default null,
                           p_oper_type     in varchar2,
                           p_acc_type      in varchar2 default null,
                           p_tx_fid        in number,
                           p_created_acc   out g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `recalculate_int_payment_plan` — PROCEDURE

**Purpose:** Public procedure related to recalculate int payment plan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 311; body declaration candidate line(s): 3445

**Signature**

```sql
procedure recalculate_int_payment_plan(p_doc_no               in varchar2,
                                         p_acc_type             in varchar2,
                                         p_main_amount          in number,
                                         p_INT_RATIO            in number,
                                         p_int_calc_type        in varchar2,
                                         p_schedule_update_type in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_new_acc` — FUNCTION

**Purpose:** Public function related to get new acc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 318; body declaration candidate line(s): 2520

**Signature**

```sql
--kredi_api.open_new_acc +
  function get_new_acc(p_branch_no       in number,
                       p_customer_no     in number,
                       p_balance_acc     in varchar2,
                       p_detail_code     in varchar2,
                       p_ccy_id          in number,
                       p_main_acc        in number default null,
                       p_cr_int_rate     in number default null,
                       p_dr_int_rate     in number default null,
                       p_com_int_rate    in number default null,
                       p_product_code    in number default null,
                       p_period_id       in number default null,
                       p_acc_description in varchar2,
                       p_memorandum_id   in varchar2 default null,
                       p_loan_doc_no     in varchar2,
                       p_loan_acc_type   in varchar2,
                       p_tx_fid          in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_plan_control` — PROCEDURE

**Purpose:** Public procedure related to do plan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 336; body declaration candidate line(s): 3506

**Signature**

```sql
-- kredi_api.plan_control +
  procedure do_plan_control(p_document_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_status_control` — PROCEDURE

**Purpose:** Public procedure related to do loan status control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 338; body declaration candidate line(s): 3515

**Signature**

```sql
-- kredi_api.loan_status_control +
  procedure do_loan_status_control(p_branch_no   in number,
                                   p_customer_no in number,
                                   p_loan_acc    in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_loan_history` — PROCEDURE

**Purpose:** Writes a loan-operation history record for a transaction.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 343; body declaration candidate line(s): 3587

**Signature**

```sql
procedure create_loan_history(p_oper_type VARCHAR2 default null,
                                p_doc_no    VARCHAR2 default null,
                                p_trn_date  DATE default glbl.getsysdate,
                                p_tx_fid    NUMBER,
                                p_trn_type  varchar2,
                                p_add_info  add_info_tab default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_collateral_out` — PROCEDURE

**Purpose:** Public procedure related to do loan collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 350; body declaration candidate line(s): 3942

**Signature**

```sql
--krd_eod.loan_collateral_out +
  procedure do_loan_collateral_out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_acc_type_by_status` — FUNCTION

**Purpose:** Public function related to get acc type by status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 353; body declaration candidate line(s): 4211

**Signature**

```sql
function get_acc_type_by_status(p_acc_type         varchar2,
                                  p_to_loan_status   varchar2,
                                  p_from_loan_status varchar2 default 'NORM')
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `generate_allocated_payment_list` — PROCEDURE

**Purpose:** Computes a payment allocation list for a loan operation.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 358; body declaration candidate line(s): 4239

**Signature**

```sql
procedure generate_allocated_payment_list(p_doc_no                in varchar2,
                                            p_oper_type             in varchar2,
                                            p_pym_amount            in number,
                                            p_has_schedule_upd_type out varchar2,
                                            p_payment_list          out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_payment_details` — PROCEDURE

**Purpose:** Public procedure related to add payment details. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 364; body declaration candidate line(s): 4389

**Signature**

```sql
procedure add_payment_details(p_doc_no                in varchar2,
                                p_has_schedule_upd_type out varchar2,
                                p_payment_list          in out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_delete_operation` — PROCEDURE

**Purpose:** Public procedure related to do delete operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 368; body declaration candidate line(s): 4483

**Signature**

```sql
procedure do_delete_operation(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Auto_Payment` — PROCEDURE

**Purpose:** Executes automatic loan payment processing in EOD/SOD context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 370; body declaration candidate line(s): 4540

**Signature**

```sql
/** Makes automatic loan payments at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S                           
  */
  Procedure do_Auto_Payment(p_min_id     number default null,
                            p_max_id     number default null,
                            p_doc_no     in varchar2 default null,
                            p_eod_sod    in varchar2 default 'E',
                            p_test_param in number default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation` — PROCEDURE

**Purpose:** Performs batch interest calculation with optional branch range, loan document and EOD/SOD arguments.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 382; body declaration candidate line(s): 5135

**Signature**

```sql
/** Makes automatic loan int calculation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S 
      p_date - operation date                            
  */
  
  procedure do_int_calculation(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation_ex` — PROCEDURE

**Purpose:** Public procedure related to do int calculation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 396; body declaration candidate line(s): 5768

**Signature**

```sql
procedure do_int_calculation_ex(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_overdue_transit_operation` — PROCEDURE

**Purpose:** Public procedure related to do overdue transit operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 402; body declaration candidate line(s): 4832

**Signature**

```sql
/** Makes automatic loan overdue operation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_branch_id - loan branch id  
      p_customer_no - unique customer number 
      p_loan_acc - loan account sub 
      p_date - operation date                            
  */

  Procedure do_overdue_transit_operation(p_min_id number default null,
                                         p_max_id number default null,
                                         p_doc_no in varchar2 default null,
                                         p_date   in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_commission_recognition` — PROCEDURE

**Purpose:** Public procedure related to do commission recognition. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 416; body declaration candidate line(s): 6338

**Signature**

```sql
Procedure do_commission_recognition(Pdate In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_guarantee_out` — PROCEDURE

**Purpose:** Public procedure related to do guarantee out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 418; body declaration candidate line(s): 6236

**Signature**

```sql
Procedure do_guarantee_out(p_branch_id   In Number Default Null,
                             p_customer_no In Number Default Null,
                             p_loan_acc    In Number Default Null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Close_With_Collateral_Out` — PROCEDURE

**Purpose:** Public procedure related to do loan close with collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 422; body declaration candidate line(s): 6594

**Signature**

```sql
procedure do_Loan_Close_With_Collateral_Out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_non_cash_loan_close` — PROCEDURE

**Purpose:** Public procedure related to do non cash loan close. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 424; body declaration candidate line(s): 6756

**Signature**

```sql
Procedure do_non_cash_loan_close(p_doc_no in varchar2,
                                   p_Date   In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_control` — PROCEDURE

**Purpose:** Public procedure related to do journal control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 427; body declaration candidate line(s): 6861

**Signature**

```sql
-- new
  procedure do_journal_control(p_branch_id   IN Number,
                               p_customer_no IN Number,
                               p_account_sub IN Number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 431; body declaration candidate line(s): 7118

**Signature**

```sql
-- new
  /*procedure over_to_norm(p_min_id  number default null,
                              p_max_id  number default null,
                              p_doc_no  in varchar2 default null);
  */
  --kredi_api.Odeme_Plani_Duzenle
  Procedure do_schedule_allignment(p_doc_no         In Varchar2,
                                   p_payment_amount In Number,
                                   p_acc_type       In Varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_com_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do com schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 441; body declaration candidate line(s): 7190

**Signature**

```sql
-- kredi_api.Kom_Odeme_Plani_Duzenle
  Procedure do_com_schedule_allignment(p_doc_no      In Varchar2,
                                       p_option_code In Varchar2,
                                       p_amount      In Number,
                                       p_plan_type   In Varchar2,
                                       p_mig_status  In Number Default 0);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Delay_Int_Rate_Upd` — PROCEDURE

**Purpose:** Public procedure related to do loan delay int rate upd. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 448; body declaration candidate line(s): 7310

**Signature**

```sql
-- krd_eod.Loan_Delay_Int_Rate_Upd
  Procedure do_Loan_Delay_Int_Rate_Upd;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `change_account_status` — PROCEDURE

**Purpose:** Public procedure related to change account status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 451; body declaration candidate line(s): 7351

**Signature**

```sql
-- kredi_api.Kredi_Hesap_Kapat , kredi_api.Kredi_Hesap_Ac
  procedure change_account_status(p_doc_no in varchar2,
                                  p_status in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_eod_task` — PROCEDURE

**Purpose:** Public procedure related to stop eod task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 455; body declaration candidate line(s): 7389

**Signature**

```sql
procedure stop_eod_task;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_loan_task` — PROCEDURE

**Purpose:** Public procedure related to stop loan task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 457; body declaration candidate line(s): 7405

**Signature**

```sql
procedure stop_loan_task(p_task_code in varchar2 default null,
                           p_task_type in varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `run_loan_task` — PROCEDURE

**Purpose:** Runs a task identified by its task code and task type.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 460; body declaration candidate line(s): 7442

**Signature**

```sql
/** Parallel execution for loan processes
      @params
      p_task_code  - task_code in loan_tasks_list table                  
  */

  procedure run_loan_task(p_task_code in varchar2, p_task_type in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `calculate_xirr` — FUNCTION

**Purpose:** Public function related to calculate xirr. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 467; body declaration candidate line(s): 7786

**Signature**

```sql
/*procedure norm_to_over(p_min_id  number default null,
  p_max_id  number default null,
  p_doc_no  in varchar2 default null);  */

  function calculate_xirr(p_doc_no  varchar2,
                          p_type    varchar2,
                          p_calc_as varchar2 default 'XIRR') return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_min_flow_ratio` — FUNCTION

**Purpose:** Public function related to get min flow ratio. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 475; body declaration candidate line(s): 8074

**Signature**

```sql
/*  function get_mix_operation_acsess(p_fid            varchar2,
                                      p_oper_type      varchar2,
                                      p_memo_oper_type varchar2) return number;
  
    function get_mix_operation_types(p_fid            varchar2,
                                     p_memo_oper_type varchar2) return varchar2;
  
    procedure validate_mix_memorandum(p_memorandum_id varchar2,
                                      p_oper_type     varchar2,
                                      p_state         varchar2);
  
    procedure update_mix_memorandum(p_memorandum_id varchar2,
                                    p_oper_type     varchar2,
                                    p_tx_fid        number,
                                    p_state         varchar2);
  */

  function get_min_flow_ratio(
    p_doc_no     varchar2,
    p_type       varchar2,
    p_begin_date date default null,
    p_end_date   date default null
  ) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_flow_ratio_info` — FUNCTION

**Purpose:** Public function related to get flow ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 499; body declaration candidate line(s): 8115

**Signature**

```sql
FUNCTION get_flow_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N')
    RETURN LOAN_FLOW_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_stop_ratio_info` — FUNCTION

**Purpose:** Public function related to get stop ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 504; body declaration candidate line(s): 8151

**Signature**

```sql
FUNCTION get_stop_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N',
                               p_info_type varchar2 default 'INT')
    RETURN LOAN_STOP_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days` — FUNCTION

**Purpose:** Public function related to get incorrect days. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 510; body declaration candidate line(s): 8179

**Signature**

```sql
function get_incorrect_days(p_date date) return NUMBER_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days_count` — FUNCTION

**Purpose:** Public function related to get incorrect days count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 513; body declaration candidate line(s): 8218

**Signature**

```sql
function get_incorrect_days_count(p_date date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_schedule_from_memo` — FUNCTION

**Purpose:** Public function related to get schedule from memo. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 515; body declaration candidate line(s): 8225

**Signature**

```sql
function get_schedule_from_memo(p_memorandum_id varchar2,
                                  p_int_ratio     number,
                                  p_int_calc_type varchar2,
                                  p_int_amount    number) return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_standart_schedule` — FUNCTION

**Purpose:** Returns pipelined standard schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 521; body declaration candidate line(s): 8324

**Signature**

```sql
function get_standart_schedule(p_begin_date          date default glbl.getsysdate,
                                 p_main_pymt_date      date,
                                 p_int_pymt_date       date,
                                 p_pymt_day            number default null,
                                 p_end_date            date,
                                 p_offer_amount        number,
                                 p_ovd_main_amount     number default 0,
                                 p_int_calc_type       varchar2,
                                 p_main_grace_period   varchar2 default null,
                                 p_int_grace_period    varchar2 default null,
                                 p_remain_int_amount   number default 0,
                                 p_min_main_pay_amount number default null,
                                 p_calc_int_in_grace   varchar2 default 'Y',
                                 p_work_days           varchar2 default 'Y',
                                 
                                 p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                 p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_annuity_schedule` — FUNCTION

**Purpose:** Returns pipelined annuity schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 542; body declaration candidate line(s): 8697

**Signature**

```sql
function get_annuity_schedule(p_begin_date      date,
                                p_main_pymt_date  date,
                                p_int_pymt_date   date,
                                p_pymt_day        number default null,
                                p_end_date        date,
                                p_offer_amount    number,
                                p_ovd_main_amount number default 0,
                                p_int_calc_type   varchar2,
                                
                                p_main_grace_period varchar2 default null,
                                p_int_grace_period  varchar2 default null,
                                
                                p_annuity_amount     number default null,
                                p_max_annuity_amount number default null,
                                p_remain_int_amount  number default 0,
                                
                                p_work_days         varchar2 default 'Y',
                                p_own_annuity       varchar2 default 'N',
                                p_calc_int_in_grace varchar2 default 'Y',
                                p_is_mortgage       varchar2 default 'N',
                                
                                p_max_iteration number default null,
                                
                                p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_created_schedule` — PROCEDURE

**Purpose:** Public procedure related to get created schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 570; body declaration candidate line(s): 9306

**Signature**

```sql
Procedure get_created_schedule(p_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_schedule` — PROCEDURE

**Purpose:** Builds a payment schedule using the supplied dates, amounts, interest and schedule options.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 572; body declaration candidate line(s): 9392

**Signature**

```sql
-- new
  procedure create_schedule(p_schedule_no         number,
                            p_coll_name           varchar2 default null,
                            p_fk_id               number default null,
                            p_doc_no              varchar2 default 'XXX',
                            p_memorandum_id       varchar2 default null,
                            p_customer_no         number default null,
                            p_tx_fid              number default null,
                            p_begin_date          date default glbl.getsysdate,
                            p_main_pymt_date      date,
                            p_int_pymt_date       date,
                            p_pymt_day            number default null,
                            p_end_date            date,
                            p_offer_amount        number,
                            p_ovd_main_amount     number default 0,
                            p_int_ratio           number,
                            p_int_calc_type       varchar2,
                            p_annuity_amount      number default null,
                            p_max_annuity_amount  number default null,
                            p_min_main_pay_amount number default null,
                            p_remain_int_amount   number default 0,
                            p_main_grace_period   varchar2 default null,
                            p_int_grace_period    varchar2 default null,
                            p_main_pymt_period    number default 1,
                            p_int_pymt_period     number default 1,
                            p_product_code        number default null,
                            p_same_annuity        varchar2 default 'N',
                            p_calc_int_in_grace   varchar2 default 'Y',
                            p_return_type         varchar2 default 'NO_ZERO',
                            p_loan_flow_rate_tab  LOAN_FLOW_RATE_TAB default null,
                            p_loan_stop_rate_tab  LOAN_STOP_RATE_TAB default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 604; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 607; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate,
                            p_min_rowid rowid,
                            p_max_rowid rowid);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

## Interest & Penalties

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 71; body declaration candidate line(s): 70, 736

**Signature**

```sql
-- *

  procedure get_pen_info_for_calc(p_date                   in date default glbl.getsysdate,
                                  p_doc_no                 in varchar2,
                                  p_acc_type               in varchar2,
                                  p_pen_calc_grace_days    in number,
                                  p_ovd_amount             out number,
                                  p_calculated_pen_day_cnt out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates` — FUNCTION

**Purpose:** Builds an interest calculation date collection based on EOD/SOD scheduling and the last calculation access date.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 80; body declaration candidate line(s): 259

**Signature**

```sql
function get_interest_calc_dates(p_last_calc_access_date in date,
                                   p_eod_sod               in varchar2,
                                   p_int_calc_at           in varchar2)
    return loan_api.g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates_ex` — FUNCTION

**Purpose:** Public function related to get interest calc dates ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 85; body declaration candidate line(s): 323

**Signature**

```sql
function get_interest_calc_dates_ex(p_date        in date,
                                      p_eod_sod     in varchar2,
                                      p_int_calc_at in varchar2)
    return g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info` — PROCEDURE

**Purpose:** Determines interest calculation day count and year-day basis from interest-calculation configuration.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 90; body declaration candidate line(s): 104

**Signature**

```sql
procedure get_interest_calc_info(p_last_calc_date       in date,
                                   p_pymt_day             in number,
                                   p_trn_date             in date,
                                   p_int_calc_type        in varchar2,
                                   p_rate_type            in varchar2,
                                   p_int_rate_periodicity in varchar2,
                                   p_calc_day_count       out number,
                                   p_year_day_count       out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info_ex` — PROCEDURE

**Purpose:** Public procedure related to get interest calc info ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 101; body declaration candidate line(s): 183

**Signature**

```sql
procedure get_interest_calc_info_ex(p_last_calc_date in date,
                                   p_pymt_day       in number,
                                   p_trn_date       in date,
                                   p_int_calc_type  in varchar2,
                                   p_calc_day_count out number,
                                   p_year_day_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `clear_addtional_data` — PROCEDURE

**Purpose:** Public procedure related to clear addtional data. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 109; body declaration candidate line(s): 378

**Signature**

```sql
procedure clear_addtional_data(p_state varchar2 default 'CLEAR');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_group` — PROCEDURE

**Purpose:** Public procedure related to add additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 111; body declaration candidate line(s): 404

**Signature**

```sql
procedure add_additional_group(p_tag_name varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_group` — PROCEDURE

**Purpose:** Public procedure related to end additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 113; body declaration candidate line(s): 410

**Signature**

```sql
procedure end_additional_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_main_group` — PROCEDURE

**Purpose:** Public procedure related to end additional main group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 114; body declaration candidate line(s): 398

**Signature**

```sql
procedure end_additional_main_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 115; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 117; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 118; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value varchar2,
                              p_new_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 122; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value date,
                              p_new_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `finalize_addtional_process` — PROCEDURE

**Purpose:** Finalizes accumulated additional information and executes mapped updates for the supplied identifiers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 125; body declaration candidate line(s): 480

**Signature**

```sql
procedure finalize_addtional_process(p_doc_no   varchar2,
                                       p_offer_id varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `reverse_update` — PROCEDURE

**Purpose:** Reads prior history additional information and attempts to restore recorded old values.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 128; body declaration candidate line(s): 591

**Signature**

```sql
procedure reverse_update(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_loan_amount` — FUNCTION

**Purpose:** Returns a loan amount using the TOTAL, DEBT, or DUE calculation mode and related account and schedule data.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 130; body declaration candidate line(s): 643

**Signature**

```sql
function get_loan_amount(p_doc_no      in varchar2,
                           p_amount_type in varchar2,
                           p_date        in date default glbl.getsysdate,
                           p_oper_type   in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_overdue_min_amount` — FUNCTION

**Purpose:** Public function related to get overdue min amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 136; body declaration candidate line(s): 719

**Signature**

```sql
function get_overdue_min_amount(p_product_code in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 137; body declaration candidate line(s): 70, 736

**Signature**

```sql
procedure get_pen_info_for_calc(p_date                in date default glbl.getsysdate,
                                  p_doc_no              in varchar2,
                                  p_pen_calc_grace_days in number,
                                  p_PEN_INT_RATIO       in number,
                                  p_ovd_amount_for_pen  out number,
                                  p_pen_calc_days_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_trn_caller_id` — FUNCTION

**Purpose:** Public function related to get trn caller id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 144; body declaration candidate line(s): 772

**Signature**

```sql
function get_trn_caller_id(p_oper_type in varchar2) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_voucher_data_from_query` — FUNCTION

**Purpose:** Executes a supplied SQL query with DBMS_SQL and maps returned column values for vouchers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 146; body declaration candidate line(s): 789

**Signature**

```sql
function get_voucher_data_from_query(p_query       in varchar2,
                                       p_result_type in varchar2)
    return g_col_value_tab_map;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_formatted_grace_from_list` — FUNCTION

**Purpose:** Public function related to get formatted grace from list. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 150; body declaration candidate line(s): 912

**Signature**

```sql
function get_formatted_grace_from_list(p_period_list in varchar2)
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_grace_info` — FUNCTION

**Purpose:** Public function related to get grace info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 153; body declaration candidate line(s): 952

**Signature**

```sql
function get_grace_info(p_Doc_No          In Varchar2,
                          p_period_end_date in date,
                          p_acc_type        In Varchar2 default 'A',
                          p_info_type       in varchar2) Return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_basis_year_days_cnt` — FUNCTION

**Purpose:** Public function related to get basis year days cnt. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 158; body declaration candidate line(s): 998

**Signature**

```sql
function get_basis_year_days_cnt(p_int_calc_type in varchar2,
                                   p_date          in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_value` — FUNCTION

**Purpose:** Public function related to get gl value. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 161; body declaration candidate line(s): 1026

**Signature**

```sql
function get_gl_value(p_parameter_name in varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 163; body declaration candidate line(s): 1043

**Signature**

```sql
procedure loan_int_diff_operation(p_trn_date        in date,
                                    p_oper_type       in varchar2,
                                    p_trn_type        in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation_ex` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 177; body declaration candidate line(s): 1197

**Signature**

```sql
procedure loan_int_diff_operation_ex(p_oper_type       in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_active_passive` — FUNCTION

**Purpose:** Public function related to get gl acc active passive. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 189; body declaration candidate line(s): 1345

**Signature**

```sql
function get_gl_acc_active_passive(p_acc_no in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_from_matrix` — FUNCTION

**Purpose:** Public function related to get gl acc from matrix. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 191; body declaration candidate line(s): 1367

**Signature**

```sql
function get_gl_acc_from_matrix(p_product_code in number default null,
                                  p_cust_type    in number default null,
                                  p_period_id    in number default null,
                                  p_currency_id  in number default null,
                                  p_base_type    in varchar2,
                                  p_loan_doc_no  in varchar2 default null,
                                  p_customer_no  in varchar2 default null,
                                  p_acc_type     in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `Get_Delay_Int_Rate` — FUNCTION

**Purpose:** Public function related to get delay int rate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 200; body declaration candidate line(s): 1602

**Signature**

```sql
-- krd_eod.Get_Delay_Int_Rate
  Function Get_Delay_Int_Rate(p_Loan_Id    In Varchar2,
                              p_Delay_Type In Varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_commission_schedule` — FUNCTION

**Purpose:** Public function related to get commission schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 203; body declaration candidate line(s): 1628

**Signature**

```sql
-- kredi_api.Get_Krd_Kom_Plan
  Function get_commission_schedule(p_begin_date    In Date,
                                   p_end_date      In Date,
                                   p_amount        In Number,
                                   p_int_calc_type in varchar2)
    Return Krd_Kom_Plan_Tt
    Pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_months_for_loan` — FUNCTION

**Purpose:** Public function related to add months for loan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 211; body declaration candidate line(s): 1744

**Signature**

```sql
function add_months_for_loan(p_date   date,
                               p_months number,
                               p_day    number default null) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_next_Plan_Pym` — FUNCTION

**Purpose:** Public function related to get next plan pym. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 215; body declaration candidate line(s): 1776

**Signature**

```sql
Function get_next_Plan_Pym(p_doc_no   In Varchar2,
                             P_date     In Date,
                             p_acc_type in varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_offer_id` — FUNCTION

**Purpose:** Public function related to get offer id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 219; body declaration candidate line(s): 1809

**Signature**

```sql
Function get_offer_id(p_branch_id In Number Default Glbl.Getsube,
                        P_date      In Date Default Glbl.Getsysdate)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_payment_amount` — FUNCTION

**Purpose:** Public function related to get plan payment amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 223; body declaration candidate line(s): 1832

**Signature**

```sql
-- krd_eod.get_Plan_Pym +
  function get_plan_payment_amount(p_doc_no   in varchar2,
                                   p_date     in date default glbl.getsysdate,
                                   p_acc_type in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_ovd_date` — FUNCTION

**Purpose:** Public function related to get ovd date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 229; body declaration candidate line(s): 2734

**Signature**

```sql
Function get_ovd_date(p_doc_no   varchar2,
                        p_acc_type varchar2,
                        p_date     date default glbl.getsysdate) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_amount_for_pen_calc` — FUNCTION

**Purpose:** Public function related to get amount for pen calc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 233; body declaration candidate line(s): 1850

**Signature**

```sql
Function get_amount_for_pen_calc(p_doc_no        In Varchar2,
                                   P_date          In Date,
                                   p_for_spec_days in varchar2 default 'N',
                                   p_int_calc_type in varchar2 default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Plan_Month_Count` — FUNCTION

**Purpose:** Public function related to get plan month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 239; body declaration candidate line(s): 1944

**Signature**

```sql
-- kredi_api.get_Plan_Month_Count +
  /*Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ')
    Return Number;*/
  Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ',
                                p_work_days     varchar2 default 'Y',
                                p_pymt_day      number default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_paid_month_count` — FUNCTION

**Purpose:** Public function related to get plan paid month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 251; body declaration candidate line(s): 1987

**Signature**

```sql
-- new
  function get_plan_paid_month_count(p_doc_no in varchar2,
                                     p_term   in number,
                                     p_date   in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_error` — FUNCTION

**Purpose:** Public function related to get plan error. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 255; body declaration candidate line(s): 2047

**Signature**

```sql
-- kredi_api.get_plan_error +
  Function get_plan_error(p_doc_no varchar2, p_date date default glbl.getsysdate) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Annuity_Amount` — FUNCTION

**Purpose:** Public function related to get annuity amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 258; body declaration candidate line(s): 2604

**Signature**

```sql
-- kredi_api.Get_Annuitet_Amount +
  Function get_Annuity_Amount(p_Doc_No      In Varchar2,
                              p_return_type In varchar2 default 'NO_ZERO')
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Pym_Startdate` — FUNCTION

**Purpose:** Public function related to get pym startdate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 263; body declaration candidate line(s): 2633

**Signature**

```sql
-- kredi_api.Get_Pym_Startdate +
  Function get_Pym_Startdate(p_Doc_No          In Varchar2,
                             p_pymt_date       In Date,
                             p_pymt_day        In Number,
                             p_pymt_period     In Number,
                             p_acc_type        In varchar2,
                             p_loan_end_Date   in date,
                             p_check_is_closed in varchar2 default 'Y')
    Return Date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_account_feature` — FUNCTION

**Purpose:** Public function related to get account feature. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 273; body declaration candidate line(s): 2799

**Signature**

```sql
function get_account_feature(p_branch_no   number,
                               p_account_no  number,
                               p_account_sub number)
    return cs_account.account_feature%type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_acc_exists` — FUNCTION

**Purpose:** Public function related to is acc exists. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 278; body declaration candidate line(s): 2818

**Signature**

```sql
function is_acc_exists(p_customer_no   number,
                         p_memorandum_id varchar2 default null,
                         p_doc_no        varchar2,
                         p_acc_type      varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_Payment_Date` — FUNCTION

**Purpose:** Public function related to is payment date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 283; body declaration candidate line(s): 2845

**Signature**

```sql
-- kredi_api.Is_Payment_Date +
  Function is_Payment_Date(p_Document_No In Varchar2, p_Date Date)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_online_offer` — FUNCTION

**Purpose:** Public function related to is online offer. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 287; body declaration candidate line(s): 2858

**Signature**

```sql
function is_online_offer(p_memorandum_id varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `table_log_operation` — PROCEDURE

**Purpose:** Public procedure related to table log operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 289; body declaration candidate line(s): 3344

**Signature**

```sql
procedure table_log_operation(p_doc_no     in varchar2,
                                p_table_name in varchar2,
                                p_tx_fid     in number,
                                p_oper_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_entry` — PROCEDURE

**Purpose:** Public procedure related to do journal entry. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 294; body declaration candidate line(s): 2876

**Signature**

```sql
Procedure do_journal_entry(p_entries_list  g_entries_list_tab,
                             p_trn_caller_id in number,
                             p_tx_fid        in out number,
                             p_trn_type      in varchar2,
                             p_is_eod        in varchar2 default 'Y');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_journal_entries` — PROCEDURE

**Purpose:** Public procedure related to create journal entries. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 300; body declaration candidate line(s): 2954

**Signature**

```sql
procedure create_journal_entries(p_oper_type in varchar2,
                                   p_tx_fid    in number,
                                   p_trn_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_account` — PROCEDURE

**Purpose:** Creates/assigns loan-related accounts based on the requested operation and returns the created account list.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 304; body declaration candidate line(s): 3129

**Signature**

```sql
procedure create_account(p_doc_no        in varchar2,
                           p_memorandum_id in varchar2 default null,
                           p_oper_type     in varchar2,
                           p_acc_type      in varchar2 default null,
                           p_tx_fid        in number,
                           p_created_acc   out g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `recalculate_int_payment_plan` — PROCEDURE

**Purpose:** Public procedure related to recalculate int payment plan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 311; body declaration candidate line(s): 3445

**Signature**

```sql
procedure recalculate_int_payment_plan(p_doc_no               in varchar2,
                                         p_acc_type             in varchar2,
                                         p_main_amount          in number,
                                         p_INT_RATIO            in number,
                                         p_int_calc_type        in varchar2,
                                         p_schedule_update_type in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_new_acc` — FUNCTION

**Purpose:** Public function related to get new acc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 318; body declaration candidate line(s): 2520

**Signature**

```sql
--kredi_api.open_new_acc +
  function get_new_acc(p_branch_no       in number,
                       p_customer_no     in number,
                       p_balance_acc     in varchar2,
                       p_detail_code     in varchar2,
                       p_ccy_id          in number,
                       p_main_acc        in number default null,
                       p_cr_int_rate     in number default null,
                       p_dr_int_rate     in number default null,
                       p_com_int_rate    in number default null,
                       p_product_code    in number default null,
                       p_period_id       in number default null,
                       p_acc_description in varchar2,
                       p_memorandum_id   in varchar2 default null,
                       p_loan_doc_no     in varchar2,
                       p_loan_acc_type   in varchar2,
                       p_tx_fid          in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_plan_control` — PROCEDURE

**Purpose:** Public procedure related to do plan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 336; body declaration candidate line(s): 3506

**Signature**

```sql
-- kredi_api.plan_control +
  procedure do_plan_control(p_document_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_status_control` — PROCEDURE

**Purpose:** Public procedure related to do loan status control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 338; body declaration candidate line(s): 3515

**Signature**

```sql
-- kredi_api.loan_status_control +
  procedure do_loan_status_control(p_branch_no   in number,
                                   p_customer_no in number,
                                   p_loan_acc    in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_loan_history` — PROCEDURE

**Purpose:** Writes a loan-operation history record for a transaction.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 343; body declaration candidate line(s): 3587

**Signature**

```sql
procedure create_loan_history(p_oper_type VARCHAR2 default null,
                                p_doc_no    VARCHAR2 default null,
                                p_trn_date  DATE default glbl.getsysdate,
                                p_tx_fid    NUMBER,
                                p_trn_type  varchar2,
                                p_add_info  add_info_tab default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_collateral_out` — PROCEDURE

**Purpose:** Public procedure related to do loan collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 350; body declaration candidate line(s): 3942

**Signature**

```sql
--krd_eod.loan_collateral_out +
  procedure do_loan_collateral_out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_acc_type_by_status` — FUNCTION

**Purpose:** Public function related to get acc type by status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 353; body declaration candidate line(s): 4211

**Signature**

```sql
function get_acc_type_by_status(p_acc_type         varchar2,
                                  p_to_loan_status   varchar2,
                                  p_from_loan_status varchar2 default 'NORM')
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `generate_allocated_payment_list` — PROCEDURE

**Purpose:** Computes a payment allocation list for a loan operation.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 358; body declaration candidate line(s): 4239

**Signature**

```sql
procedure generate_allocated_payment_list(p_doc_no                in varchar2,
                                            p_oper_type             in varchar2,
                                            p_pym_amount            in number,
                                            p_has_schedule_upd_type out varchar2,
                                            p_payment_list          out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_payment_details` — PROCEDURE

**Purpose:** Public procedure related to add payment details. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 364; body declaration candidate line(s): 4389

**Signature**

```sql
procedure add_payment_details(p_doc_no                in varchar2,
                                p_has_schedule_upd_type out varchar2,
                                p_payment_list          in out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_delete_operation` — PROCEDURE

**Purpose:** Public procedure related to do delete operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 368; body declaration candidate line(s): 4483

**Signature**

```sql
procedure do_delete_operation(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Auto_Payment` — PROCEDURE

**Purpose:** Executes automatic loan payment processing in EOD/SOD context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 370; body declaration candidate line(s): 4540

**Signature**

```sql
/** Makes automatic loan payments at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S                           
  */
  Procedure do_Auto_Payment(p_min_id     number default null,
                            p_max_id     number default null,
                            p_doc_no     in varchar2 default null,
                            p_eod_sod    in varchar2 default 'E',
                            p_test_param in number default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation` — PROCEDURE

**Purpose:** Performs batch interest calculation with optional branch range, loan document and EOD/SOD arguments.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 382; body declaration candidate line(s): 5135

**Signature**

```sql
/** Makes automatic loan int calculation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S 
      p_date - operation date                            
  */
  
  procedure do_int_calculation(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation_ex` — PROCEDURE

**Purpose:** Public procedure related to do int calculation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 396; body declaration candidate line(s): 5768

**Signature**

```sql
procedure do_int_calculation_ex(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_overdue_transit_operation` — PROCEDURE

**Purpose:** Public procedure related to do overdue transit operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 402; body declaration candidate line(s): 4832

**Signature**

```sql
/** Makes automatic loan overdue operation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_branch_id - loan branch id  
      p_customer_no - unique customer number 
      p_loan_acc - loan account sub 
      p_date - operation date                            
  */

  Procedure do_overdue_transit_operation(p_min_id number default null,
                                         p_max_id number default null,
                                         p_doc_no in varchar2 default null,
                                         p_date   in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_commission_recognition` — PROCEDURE

**Purpose:** Public procedure related to do commission recognition. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 416; body declaration candidate line(s): 6338

**Signature**

```sql
Procedure do_commission_recognition(Pdate In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_guarantee_out` — PROCEDURE

**Purpose:** Public procedure related to do guarantee out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 418; body declaration candidate line(s): 6236

**Signature**

```sql
Procedure do_guarantee_out(p_branch_id   In Number Default Null,
                             p_customer_no In Number Default Null,
                             p_loan_acc    In Number Default Null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Close_With_Collateral_Out` — PROCEDURE

**Purpose:** Public procedure related to do loan close with collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 422; body declaration candidate line(s): 6594

**Signature**

```sql
procedure do_Loan_Close_With_Collateral_Out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_non_cash_loan_close` — PROCEDURE

**Purpose:** Public procedure related to do non cash loan close. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 424; body declaration candidate line(s): 6756

**Signature**

```sql
Procedure do_non_cash_loan_close(p_doc_no in varchar2,
                                   p_Date   In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_control` — PROCEDURE

**Purpose:** Public procedure related to do journal control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 427; body declaration candidate line(s): 6861

**Signature**

```sql
-- new
  procedure do_journal_control(p_branch_id   IN Number,
                               p_customer_no IN Number,
                               p_account_sub IN Number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 431; body declaration candidate line(s): 7118

**Signature**

```sql
-- new
  /*procedure over_to_norm(p_min_id  number default null,
                              p_max_id  number default null,
                              p_doc_no  in varchar2 default null);
  */
  --kredi_api.Odeme_Plani_Duzenle
  Procedure do_schedule_allignment(p_doc_no         In Varchar2,
                                   p_payment_amount In Number,
                                   p_acc_type       In Varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_com_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do com schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 441; body declaration candidate line(s): 7190

**Signature**

```sql
-- kredi_api.Kom_Odeme_Plani_Duzenle
  Procedure do_com_schedule_allignment(p_doc_no      In Varchar2,
                                       p_option_code In Varchar2,
                                       p_amount      In Number,
                                       p_plan_type   In Varchar2,
                                       p_mig_status  In Number Default 0);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Delay_Int_Rate_Upd` — PROCEDURE

**Purpose:** Public procedure related to do loan delay int rate upd. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 448; body declaration candidate line(s): 7310

**Signature**

```sql
-- krd_eod.Loan_Delay_Int_Rate_Upd
  Procedure do_Loan_Delay_Int_Rate_Upd;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `change_account_status` — PROCEDURE

**Purpose:** Public procedure related to change account status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 451; body declaration candidate line(s): 7351

**Signature**

```sql
-- kredi_api.Kredi_Hesap_Kapat , kredi_api.Kredi_Hesap_Ac
  procedure change_account_status(p_doc_no in varchar2,
                                  p_status in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_eod_task` — PROCEDURE

**Purpose:** Public procedure related to stop eod task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 455; body declaration candidate line(s): 7389

**Signature**

```sql
procedure stop_eod_task;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_loan_task` — PROCEDURE

**Purpose:** Public procedure related to stop loan task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 457; body declaration candidate line(s): 7405

**Signature**

```sql
procedure stop_loan_task(p_task_code in varchar2 default null,
                           p_task_type in varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `run_loan_task` — PROCEDURE

**Purpose:** Runs a task identified by its task code and task type.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 460; body declaration candidate line(s): 7442

**Signature**

```sql
/** Parallel execution for loan processes
      @params
      p_task_code  - task_code in loan_tasks_list table                  
  */

  procedure run_loan_task(p_task_code in varchar2, p_task_type in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `calculate_xirr` — FUNCTION

**Purpose:** Public function related to calculate xirr. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 467; body declaration candidate line(s): 7786

**Signature**

```sql
/*procedure norm_to_over(p_min_id  number default null,
  p_max_id  number default null,
  p_doc_no  in varchar2 default null);  */

  function calculate_xirr(p_doc_no  varchar2,
                          p_type    varchar2,
                          p_calc_as varchar2 default 'XIRR') return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_min_flow_ratio` — FUNCTION

**Purpose:** Public function related to get min flow ratio. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 475; body declaration candidate line(s): 8074

**Signature**

```sql
/*  function get_mix_operation_acsess(p_fid            varchar2,
                                      p_oper_type      varchar2,
                                      p_memo_oper_type varchar2) return number;
  
    function get_mix_operation_types(p_fid            varchar2,
                                     p_memo_oper_type varchar2) return varchar2;
  
    procedure validate_mix_memorandum(p_memorandum_id varchar2,
                                      p_oper_type     varchar2,
                                      p_state         varchar2);
  
    procedure update_mix_memorandum(p_memorandum_id varchar2,
                                    p_oper_type     varchar2,
                                    p_tx_fid        number,
                                    p_state         varchar2);
  */

  function get_min_flow_ratio(
    p_doc_no     varchar2,
    p_type       varchar2,
    p_begin_date date default null,
    p_end_date   date default null
  ) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_flow_ratio_info` — FUNCTION

**Purpose:** Public function related to get flow ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 499; body declaration candidate line(s): 8115

**Signature**

```sql
FUNCTION get_flow_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N')
    RETURN LOAN_FLOW_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_stop_ratio_info` — FUNCTION

**Purpose:** Public function related to get stop ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 504; body declaration candidate line(s): 8151

**Signature**

```sql
FUNCTION get_stop_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N',
                               p_info_type varchar2 default 'INT')
    RETURN LOAN_STOP_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days` — FUNCTION

**Purpose:** Public function related to get incorrect days. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 510; body declaration candidate line(s): 8179

**Signature**

```sql
function get_incorrect_days(p_date date) return NUMBER_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days_count` — FUNCTION

**Purpose:** Public function related to get incorrect days count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 513; body declaration candidate line(s): 8218

**Signature**

```sql
function get_incorrect_days_count(p_date date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_schedule_from_memo` — FUNCTION

**Purpose:** Public function related to get schedule from memo. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 515; body declaration candidate line(s): 8225

**Signature**

```sql
function get_schedule_from_memo(p_memorandum_id varchar2,
                                  p_int_ratio     number,
                                  p_int_calc_type varchar2,
                                  p_int_amount    number) return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_standart_schedule` — FUNCTION

**Purpose:** Returns pipelined standard schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 521; body declaration candidate line(s): 8324

**Signature**

```sql
function get_standart_schedule(p_begin_date          date default glbl.getsysdate,
                                 p_main_pymt_date      date,
                                 p_int_pymt_date       date,
                                 p_pymt_day            number default null,
                                 p_end_date            date,
                                 p_offer_amount        number,
                                 p_ovd_main_amount     number default 0,
                                 p_int_calc_type       varchar2,
                                 p_main_grace_period   varchar2 default null,
                                 p_int_grace_period    varchar2 default null,
                                 p_remain_int_amount   number default 0,
                                 p_min_main_pay_amount number default null,
                                 p_calc_int_in_grace   varchar2 default 'Y',
                                 p_work_days           varchar2 default 'Y',
                                 
                                 p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                 p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_annuity_schedule` — FUNCTION

**Purpose:** Returns pipelined annuity schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 542; body declaration candidate line(s): 8697

**Signature**

```sql
function get_annuity_schedule(p_begin_date      date,
                                p_main_pymt_date  date,
                                p_int_pymt_date   date,
                                p_pymt_day        number default null,
                                p_end_date        date,
                                p_offer_amount    number,
                                p_ovd_main_amount number default 0,
                                p_int_calc_type   varchar2,
                                
                                p_main_grace_period varchar2 default null,
                                p_int_grace_period  varchar2 default null,
                                
                                p_annuity_amount     number default null,
                                p_max_annuity_amount number default null,
                                p_remain_int_amount  number default 0,
                                
                                p_work_days         varchar2 default 'Y',
                                p_own_annuity       varchar2 default 'N',
                                p_calc_int_in_grace varchar2 default 'Y',
                                p_is_mortgage       varchar2 default 'N',
                                
                                p_max_iteration number default null,
                                
                                p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_created_schedule` — PROCEDURE

**Purpose:** Public procedure related to get created schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 570; body declaration candidate line(s): 9306

**Signature**

```sql
Procedure get_created_schedule(p_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_schedule` — PROCEDURE

**Purpose:** Builds a payment schedule using the supplied dates, amounts, interest and schedule options.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 572; body declaration candidate line(s): 9392

**Signature**

```sql
-- new
  procedure create_schedule(p_schedule_no         number,
                            p_coll_name           varchar2 default null,
                            p_fk_id               number default null,
                            p_doc_no              varchar2 default 'XXX',
                            p_memorandum_id       varchar2 default null,
                            p_customer_no         number default null,
                            p_tx_fid              number default null,
                            p_begin_date          date default glbl.getsysdate,
                            p_main_pymt_date      date,
                            p_int_pymt_date       date,
                            p_pymt_day            number default null,
                            p_end_date            date,
                            p_offer_amount        number,
                            p_ovd_main_amount     number default 0,
                            p_int_ratio           number,
                            p_int_calc_type       varchar2,
                            p_annuity_amount      number default null,
                            p_max_annuity_amount  number default null,
                            p_min_main_pay_amount number default null,
                            p_remain_int_amount   number default 0,
                            p_main_grace_period   varchar2 default null,
                            p_int_grace_period    varchar2 default null,
                            p_main_pymt_period    number default 1,
                            p_int_pymt_period     number default 1,
                            p_product_code        number default null,
                            p_same_annuity        varchar2 default 'N',
                            p_calc_int_in_grace   varchar2 default 'Y',
                            p_return_type         varchar2 default 'NO_ZERO',
                            p_loan_flow_rate_tab  LOAN_FLOW_RATE_TAB default null,
                            p_loan_stop_rate_tab  LOAN_STOP_RATE_TAB default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 604; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 607; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate,
                            p_min_rowid rowid,
                            p_max_rowid rowid);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

## Journal & Vouchers

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 71; body declaration candidate line(s): 70, 736

**Signature**

```sql
-- *

  procedure get_pen_info_for_calc(p_date                   in date default glbl.getsysdate,
                                  p_doc_no                 in varchar2,
                                  p_acc_type               in varchar2,
                                  p_pen_calc_grace_days    in number,
                                  p_ovd_amount             out number,
                                  p_calculated_pen_day_cnt out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates` — FUNCTION

**Purpose:** Builds an interest calculation date collection based on EOD/SOD scheduling and the last calculation access date.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 80; body declaration candidate line(s): 259

**Signature**

```sql
function get_interest_calc_dates(p_last_calc_access_date in date,
                                   p_eod_sod               in varchar2,
                                   p_int_calc_at           in varchar2)
    return loan_api.g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates_ex` — FUNCTION

**Purpose:** Public function related to get interest calc dates ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 85; body declaration candidate line(s): 323

**Signature**

```sql
function get_interest_calc_dates_ex(p_date        in date,
                                      p_eod_sod     in varchar2,
                                      p_int_calc_at in varchar2)
    return g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info` — PROCEDURE

**Purpose:** Determines interest calculation day count and year-day basis from interest-calculation configuration.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 90; body declaration candidate line(s): 104

**Signature**

```sql
procedure get_interest_calc_info(p_last_calc_date       in date,
                                   p_pymt_day             in number,
                                   p_trn_date             in date,
                                   p_int_calc_type        in varchar2,
                                   p_rate_type            in varchar2,
                                   p_int_rate_periodicity in varchar2,
                                   p_calc_day_count       out number,
                                   p_year_day_count       out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info_ex` — PROCEDURE

**Purpose:** Public procedure related to get interest calc info ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 101; body declaration candidate line(s): 183

**Signature**

```sql
procedure get_interest_calc_info_ex(p_last_calc_date in date,
                                   p_pymt_day       in number,
                                   p_trn_date       in date,
                                   p_int_calc_type  in varchar2,
                                   p_calc_day_count out number,
                                   p_year_day_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `clear_addtional_data` — PROCEDURE

**Purpose:** Public procedure related to clear addtional data. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 109; body declaration candidate line(s): 378

**Signature**

```sql
procedure clear_addtional_data(p_state varchar2 default 'CLEAR');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_group` — PROCEDURE

**Purpose:** Public procedure related to add additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 111; body declaration candidate line(s): 404

**Signature**

```sql
procedure add_additional_group(p_tag_name varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_group` — PROCEDURE

**Purpose:** Public procedure related to end additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 113; body declaration candidate line(s): 410

**Signature**

```sql
procedure end_additional_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_main_group` — PROCEDURE

**Purpose:** Public procedure related to end additional main group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 114; body declaration candidate line(s): 398

**Signature**

```sql
procedure end_additional_main_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 115; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 117; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 118; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value varchar2,
                              p_new_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 122; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value date,
                              p_new_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `finalize_addtional_process` — PROCEDURE

**Purpose:** Finalizes accumulated additional information and executes mapped updates for the supplied identifiers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 125; body declaration candidate line(s): 480

**Signature**

```sql
procedure finalize_addtional_process(p_doc_no   varchar2,
                                       p_offer_id varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `reverse_update` — PROCEDURE

**Purpose:** Reads prior history additional information and attempts to restore recorded old values.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 128; body declaration candidate line(s): 591

**Signature**

```sql
procedure reverse_update(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_loan_amount` — FUNCTION

**Purpose:** Returns a loan amount using the TOTAL, DEBT, or DUE calculation mode and related account and schedule data.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 130; body declaration candidate line(s): 643

**Signature**

```sql
function get_loan_amount(p_doc_no      in varchar2,
                           p_amount_type in varchar2,
                           p_date        in date default glbl.getsysdate,
                           p_oper_type   in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_overdue_min_amount` — FUNCTION

**Purpose:** Public function related to get overdue min amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 136; body declaration candidate line(s): 719

**Signature**

```sql
function get_overdue_min_amount(p_product_code in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 137; body declaration candidate line(s): 70, 736

**Signature**

```sql
procedure get_pen_info_for_calc(p_date                in date default glbl.getsysdate,
                                  p_doc_no              in varchar2,
                                  p_pen_calc_grace_days in number,
                                  p_PEN_INT_RATIO       in number,
                                  p_ovd_amount_for_pen  out number,
                                  p_pen_calc_days_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_trn_caller_id` — FUNCTION

**Purpose:** Public function related to get trn caller id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 144; body declaration candidate line(s): 772

**Signature**

```sql
function get_trn_caller_id(p_oper_type in varchar2) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_voucher_data_from_query` — FUNCTION

**Purpose:** Executes a supplied SQL query with DBMS_SQL and maps returned column values for vouchers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 146; body declaration candidate line(s): 789

**Signature**

```sql
function get_voucher_data_from_query(p_query       in varchar2,
                                       p_result_type in varchar2)
    return g_col_value_tab_map;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_formatted_grace_from_list` — FUNCTION

**Purpose:** Public function related to get formatted grace from list. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 150; body declaration candidate line(s): 912

**Signature**

```sql
function get_formatted_grace_from_list(p_period_list in varchar2)
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_grace_info` — FUNCTION

**Purpose:** Public function related to get grace info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 153; body declaration candidate line(s): 952

**Signature**

```sql
function get_grace_info(p_Doc_No          In Varchar2,
                          p_period_end_date in date,
                          p_acc_type        In Varchar2 default 'A',
                          p_info_type       in varchar2) Return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_basis_year_days_cnt` — FUNCTION

**Purpose:** Public function related to get basis year days cnt. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 158; body declaration candidate line(s): 998

**Signature**

```sql
function get_basis_year_days_cnt(p_int_calc_type in varchar2,
                                   p_date          in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_value` — FUNCTION

**Purpose:** Public function related to get gl value. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 161; body declaration candidate line(s): 1026

**Signature**

```sql
function get_gl_value(p_parameter_name in varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 163; body declaration candidate line(s): 1043

**Signature**

```sql
procedure loan_int_diff_operation(p_trn_date        in date,
                                    p_oper_type       in varchar2,
                                    p_trn_type        in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation_ex` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 177; body declaration candidate line(s): 1197

**Signature**

```sql
procedure loan_int_diff_operation_ex(p_oper_type       in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_active_passive` — FUNCTION

**Purpose:** Public function related to get gl acc active passive. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 189; body declaration candidate line(s): 1345

**Signature**

```sql
function get_gl_acc_active_passive(p_acc_no in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_from_matrix` — FUNCTION

**Purpose:** Public function related to get gl acc from matrix. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 191; body declaration candidate line(s): 1367

**Signature**

```sql
function get_gl_acc_from_matrix(p_product_code in number default null,
                                  p_cust_type    in number default null,
                                  p_period_id    in number default null,
                                  p_currency_id  in number default null,
                                  p_base_type    in varchar2,
                                  p_loan_doc_no  in varchar2 default null,
                                  p_customer_no  in varchar2 default null,
                                  p_acc_type     in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `Get_Delay_Int_Rate` — FUNCTION

**Purpose:** Public function related to get delay int rate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 200; body declaration candidate line(s): 1602

**Signature**

```sql
-- krd_eod.Get_Delay_Int_Rate
  Function Get_Delay_Int_Rate(p_Loan_Id    In Varchar2,
                              p_Delay_Type In Varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_commission_schedule` — FUNCTION

**Purpose:** Public function related to get commission schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 203; body declaration candidate line(s): 1628

**Signature**

```sql
-- kredi_api.Get_Krd_Kom_Plan
  Function get_commission_schedule(p_begin_date    In Date,
                                   p_end_date      In Date,
                                   p_amount        In Number,
                                   p_int_calc_type in varchar2)
    Return Krd_Kom_Plan_Tt
    Pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_months_for_loan` — FUNCTION

**Purpose:** Public function related to add months for loan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 211; body declaration candidate line(s): 1744

**Signature**

```sql
function add_months_for_loan(p_date   date,
                               p_months number,
                               p_day    number default null) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_next_Plan_Pym` — FUNCTION

**Purpose:** Public function related to get next plan pym. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 215; body declaration candidate line(s): 1776

**Signature**

```sql
Function get_next_Plan_Pym(p_doc_no   In Varchar2,
                             P_date     In Date,
                             p_acc_type in varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_offer_id` — FUNCTION

**Purpose:** Public function related to get offer id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 219; body declaration candidate line(s): 1809

**Signature**

```sql
Function get_offer_id(p_branch_id In Number Default Glbl.Getsube,
                        P_date      In Date Default Glbl.Getsysdate)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_payment_amount` — FUNCTION

**Purpose:** Public function related to get plan payment amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 223; body declaration candidate line(s): 1832

**Signature**

```sql
-- krd_eod.get_Plan_Pym +
  function get_plan_payment_amount(p_doc_no   in varchar2,
                                   p_date     in date default glbl.getsysdate,
                                   p_acc_type in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_ovd_date` — FUNCTION

**Purpose:** Public function related to get ovd date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 229; body declaration candidate line(s): 2734

**Signature**

```sql
Function get_ovd_date(p_doc_no   varchar2,
                        p_acc_type varchar2,
                        p_date     date default glbl.getsysdate) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_amount_for_pen_calc` — FUNCTION

**Purpose:** Public function related to get amount for pen calc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 233; body declaration candidate line(s): 1850

**Signature**

```sql
Function get_amount_for_pen_calc(p_doc_no        In Varchar2,
                                   P_date          In Date,
                                   p_for_spec_days in varchar2 default 'N',
                                   p_int_calc_type in varchar2 default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Plan_Month_Count` — FUNCTION

**Purpose:** Public function related to get plan month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 239; body declaration candidate line(s): 1944

**Signature**

```sql
-- kredi_api.get_Plan_Month_Count +
  /*Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ')
    Return Number;*/
  Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ',
                                p_work_days     varchar2 default 'Y',
                                p_pymt_day      number default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_paid_month_count` — FUNCTION

**Purpose:** Public function related to get plan paid month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 251; body declaration candidate line(s): 1987

**Signature**

```sql
-- new
  function get_plan_paid_month_count(p_doc_no in varchar2,
                                     p_term   in number,
                                     p_date   in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_error` — FUNCTION

**Purpose:** Public function related to get plan error. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 255; body declaration candidate line(s): 2047

**Signature**

```sql
-- kredi_api.get_plan_error +
  Function get_plan_error(p_doc_no varchar2, p_date date default glbl.getsysdate) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Annuity_Amount` — FUNCTION

**Purpose:** Public function related to get annuity amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 258; body declaration candidate line(s): 2604

**Signature**

```sql
-- kredi_api.Get_Annuitet_Amount +
  Function get_Annuity_Amount(p_Doc_No      In Varchar2,
                              p_return_type In varchar2 default 'NO_ZERO')
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Pym_Startdate` — FUNCTION

**Purpose:** Public function related to get pym startdate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 263; body declaration candidate line(s): 2633

**Signature**

```sql
-- kredi_api.Get_Pym_Startdate +
  Function get_Pym_Startdate(p_Doc_No          In Varchar2,
                             p_pymt_date       In Date,
                             p_pymt_day        In Number,
                             p_pymt_period     In Number,
                             p_acc_type        In varchar2,
                             p_loan_end_Date   in date,
                             p_check_is_closed in varchar2 default 'Y')
    Return Date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_account_feature` — FUNCTION

**Purpose:** Public function related to get account feature. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 273; body declaration candidate line(s): 2799

**Signature**

```sql
function get_account_feature(p_branch_no   number,
                               p_account_no  number,
                               p_account_sub number)
    return cs_account.account_feature%type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_acc_exists` — FUNCTION

**Purpose:** Public function related to is acc exists. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 278; body declaration candidate line(s): 2818

**Signature**

```sql
function is_acc_exists(p_customer_no   number,
                         p_memorandum_id varchar2 default null,
                         p_doc_no        varchar2,
                         p_acc_type      varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_Payment_Date` — FUNCTION

**Purpose:** Public function related to is payment date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 283; body declaration candidate line(s): 2845

**Signature**

```sql
-- kredi_api.Is_Payment_Date +
  Function is_Payment_Date(p_Document_No In Varchar2, p_Date Date)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_online_offer` — FUNCTION

**Purpose:** Public function related to is online offer. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 287; body declaration candidate line(s): 2858

**Signature**

```sql
function is_online_offer(p_memorandum_id varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `table_log_operation` — PROCEDURE

**Purpose:** Public procedure related to table log operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 289; body declaration candidate line(s): 3344

**Signature**

```sql
procedure table_log_operation(p_doc_no     in varchar2,
                                p_table_name in varchar2,
                                p_tx_fid     in number,
                                p_oper_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_entry` — PROCEDURE

**Purpose:** Public procedure related to do journal entry. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 294; body declaration candidate line(s): 2876

**Signature**

```sql
Procedure do_journal_entry(p_entries_list  g_entries_list_tab,
                             p_trn_caller_id in number,
                             p_tx_fid        in out number,
                             p_trn_type      in varchar2,
                             p_is_eod        in varchar2 default 'Y');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_journal_entries` — PROCEDURE

**Purpose:** Public procedure related to create journal entries. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 300; body declaration candidate line(s): 2954

**Signature**

```sql
procedure create_journal_entries(p_oper_type in varchar2,
                                   p_tx_fid    in number,
                                   p_trn_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_account` — PROCEDURE

**Purpose:** Creates/assigns loan-related accounts based on the requested operation and returns the created account list.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 304; body declaration candidate line(s): 3129

**Signature**

```sql
procedure create_account(p_doc_no        in varchar2,
                           p_memorandum_id in varchar2 default null,
                           p_oper_type     in varchar2,
                           p_acc_type      in varchar2 default null,
                           p_tx_fid        in number,
                           p_created_acc   out g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `recalculate_int_payment_plan` — PROCEDURE

**Purpose:** Public procedure related to recalculate int payment plan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 311; body declaration candidate line(s): 3445

**Signature**

```sql
procedure recalculate_int_payment_plan(p_doc_no               in varchar2,
                                         p_acc_type             in varchar2,
                                         p_main_amount          in number,
                                         p_INT_RATIO            in number,
                                         p_int_calc_type        in varchar2,
                                         p_schedule_update_type in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_new_acc` — FUNCTION

**Purpose:** Public function related to get new acc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 318; body declaration candidate line(s): 2520

**Signature**

```sql
--kredi_api.open_new_acc +
  function get_new_acc(p_branch_no       in number,
                       p_customer_no     in number,
                       p_balance_acc     in varchar2,
                       p_detail_code     in varchar2,
                       p_ccy_id          in number,
                       p_main_acc        in number default null,
                       p_cr_int_rate     in number default null,
                       p_dr_int_rate     in number default null,
                       p_com_int_rate    in number default null,
                       p_product_code    in number default null,
                       p_period_id       in number default null,
                       p_acc_description in varchar2,
                       p_memorandum_id   in varchar2 default null,
                       p_loan_doc_no     in varchar2,
                       p_loan_acc_type   in varchar2,
                       p_tx_fid          in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_plan_control` — PROCEDURE

**Purpose:** Public procedure related to do plan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 336; body declaration candidate line(s): 3506

**Signature**

```sql
-- kredi_api.plan_control +
  procedure do_plan_control(p_document_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_status_control` — PROCEDURE

**Purpose:** Public procedure related to do loan status control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 338; body declaration candidate line(s): 3515

**Signature**

```sql
-- kredi_api.loan_status_control +
  procedure do_loan_status_control(p_branch_no   in number,
                                   p_customer_no in number,
                                   p_loan_acc    in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_loan_history` — PROCEDURE

**Purpose:** Writes a loan-operation history record for a transaction.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 343; body declaration candidate line(s): 3587

**Signature**

```sql
procedure create_loan_history(p_oper_type VARCHAR2 default null,
                                p_doc_no    VARCHAR2 default null,
                                p_trn_date  DATE default glbl.getsysdate,
                                p_tx_fid    NUMBER,
                                p_trn_type  varchar2,
                                p_add_info  add_info_tab default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_collateral_out` — PROCEDURE

**Purpose:** Public procedure related to do loan collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 350; body declaration candidate line(s): 3942

**Signature**

```sql
--krd_eod.loan_collateral_out +
  procedure do_loan_collateral_out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_acc_type_by_status` — FUNCTION

**Purpose:** Public function related to get acc type by status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 353; body declaration candidate line(s): 4211

**Signature**

```sql
function get_acc_type_by_status(p_acc_type         varchar2,
                                  p_to_loan_status   varchar2,
                                  p_from_loan_status varchar2 default 'NORM')
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `generate_allocated_payment_list` — PROCEDURE

**Purpose:** Computes a payment allocation list for a loan operation.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 358; body declaration candidate line(s): 4239

**Signature**

```sql
procedure generate_allocated_payment_list(p_doc_no                in varchar2,
                                            p_oper_type             in varchar2,
                                            p_pym_amount            in number,
                                            p_has_schedule_upd_type out varchar2,
                                            p_payment_list          out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_payment_details` — PROCEDURE

**Purpose:** Public procedure related to add payment details. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 364; body declaration candidate line(s): 4389

**Signature**

```sql
procedure add_payment_details(p_doc_no                in varchar2,
                                p_has_schedule_upd_type out varchar2,
                                p_payment_list          in out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_delete_operation` — PROCEDURE

**Purpose:** Public procedure related to do delete operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 368; body declaration candidate line(s): 4483

**Signature**

```sql
procedure do_delete_operation(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Auto_Payment` — PROCEDURE

**Purpose:** Executes automatic loan payment processing in EOD/SOD context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 370; body declaration candidate line(s): 4540

**Signature**

```sql
/** Makes automatic loan payments at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S                           
  */
  Procedure do_Auto_Payment(p_min_id     number default null,
                            p_max_id     number default null,
                            p_doc_no     in varchar2 default null,
                            p_eod_sod    in varchar2 default 'E',
                            p_test_param in number default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation` — PROCEDURE

**Purpose:** Performs batch interest calculation with optional branch range, loan document and EOD/SOD arguments.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 382; body declaration candidate line(s): 5135

**Signature**

```sql
/** Makes automatic loan int calculation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S 
      p_date - operation date                            
  */
  
  procedure do_int_calculation(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation_ex` — PROCEDURE

**Purpose:** Public procedure related to do int calculation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 396; body declaration candidate line(s): 5768

**Signature**

```sql
procedure do_int_calculation_ex(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_overdue_transit_operation` — PROCEDURE

**Purpose:** Public procedure related to do overdue transit operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 402; body declaration candidate line(s): 4832

**Signature**

```sql
/** Makes automatic loan overdue operation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_branch_id - loan branch id  
      p_customer_no - unique customer number 
      p_loan_acc - loan account sub 
      p_date - operation date                            
  */

  Procedure do_overdue_transit_operation(p_min_id number default null,
                                         p_max_id number default null,
                                         p_doc_no in varchar2 default null,
                                         p_date   in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_commission_recognition` — PROCEDURE

**Purpose:** Public procedure related to do commission recognition. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 416; body declaration candidate line(s): 6338

**Signature**

```sql
Procedure do_commission_recognition(Pdate In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_guarantee_out` — PROCEDURE

**Purpose:** Public procedure related to do guarantee out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 418; body declaration candidate line(s): 6236

**Signature**

```sql
Procedure do_guarantee_out(p_branch_id   In Number Default Null,
                             p_customer_no In Number Default Null,
                             p_loan_acc    In Number Default Null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Close_With_Collateral_Out` — PROCEDURE

**Purpose:** Public procedure related to do loan close with collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 422; body declaration candidate line(s): 6594

**Signature**

```sql
procedure do_Loan_Close_With_Collateral_Out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_non_cash_loan_close` — PROCEDURE

**Purpose:** Public procedure related to do non cash loan close. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 424; body declaration candidate line(s): 6756

**Signature**

```sql
Procedure do_non_cash_loan_close(p_doc_no in varchar2,
                                   p_Date   In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_control` — PROCEDURE

**Purpose:** Public procedure related to do journal control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 427; body declaration candidate line(s): 6861

**Signature**

```sql
-- new
  procedure do_journal_control(p_branch_id   IN Number,
                               p_customer_no IN Number,
                               p_account_sub IN Number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 431; body declaration candidate line(s): 7118

**Signature**

```sql
-- new
  /*procedure over_to_norm(p_min_id  number default null,
                              p_max_id  number default null,
                              p_doc_no  in varchar2 default null);
  */
  --kredi_api.Odeme_Plani_Duzenle
  Procedure do_schedule_allignment(p_doc_no         In Varchar2,
                                   p_payment_amount In Number,
                                   p_acc_type       In Varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_com_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do com schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 441; body declaration candidate line(s): 7190

**Signature**

```sql
-- kredi_api.Kom_Odeme_Plani_Duzenle
  Procedure do_com_schedule_allignment(p_doc_no      In Varchar2,
                                       p_option_code In Varchar2,
                                       p_amount      In Number,
                                       p_plan_type   In Varchar2,
                                       p_mig_status  In Number Default 0);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Delay_Int_Rate_Upd` — PROCEDURE

**Purpose:** Public procedure related to do loan delay int rate upd. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 448; body declaration candidate line(s): 7310

**Signature**

```sql
-- krd_eod.Loan_Delay_Int_Rate_Upd
  Procedure do_Loan_Delay_Int_Rate_Upd;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `change_account_status` — PROCEDURE

**Purpose:** Public procedure related to change account status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 451; body declaration candidate line(s): 7351

**Signature**

```sql
-- kredi_api.Kredi_Hesap_Kapat , kredi_api.Kredi_Hesap_Ac
  procedure change_account_status(p_doc_no in varchar2,
                                  p_status in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_eod_task` — PROCEDURE

**Purpose:** Public procedure related to stop eod task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 455; body declaration candidate line(s): 7389

**Signature**

```sql
procedure stop_eod_task;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_loan_task` — PROCEDURE

**Purpose:** Public procedure related to stop loan task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 457; body declaration candidate line(s): 7405

**Signature**

```sql
procedure stop_loan_task(p_task_code in varchar2 default null,
                           p_task_type in varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `run_loan_task` — PROCEDURE

**Purpose:** Runs a task identified by its task code and task type.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 460; body declaration candidate line(s): 7442

**Signature**

```sql
/** Parallel execution for loan processes
      @params
      p_task_code  - task_code in loan_tasks_list table                  
  */

  procedure run_loan_task(p_task_code in varchar2, p_task_type in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `calculate_xirr` — FUNCTION

**Purpose:** Public function related to calculate xirr. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 467; body declaration candidate line(s): 7786

**Signature**

```sql
/*procedure norm_to_over(p_min_id  number default null,
  p_max_id  number default null,
  p_doc_no  in varchar2 default null);  */

  function calculate_xirr(p_doc_no  varchar2,
                          p_type    varchar2,
                          p_calc_as varchar2 default 'XIRR') return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_min_flow_ratio` — FUNCTION

**Purpose:** Public function related to get min flow ratio. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 475; body declaration candidate line(s): 8074

**Signature**

```sql
/*  function get_mix_operation_acsess(p_fid            varchar2,
                                      p_oper_type      varchar2,
                                      p_memo_oper_type varchar2) return number;
  
    function get_mix_operation_types(p_fid            varchar2,
                                     p_memo_oper_type varchar2) return varchar2;
  
    procedure validate_mix_memorandum(p_memorandum_id varchar2,
                                      p_oper_type     varchar2,
                                      p_state         varchar2);
  
    procedure update_mix_memorandum(p_memorandum_id varchar2,
                                    p_oper_type     varchar2,
                                    p_tx_fid        number,
                                    p_state         varchar2);
  */

  function get_min_flow_ratio(
    p_doc_no     varchar2,
    p_type       varchar2,
    p_begin_date date default null,
    p_end_date   date default null
  ) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_flow_ratio_info` — FUNCTION

**Purpose:** Public function related to get flow ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 499; body declaration candidate line(s): 8115

**Signature**

```sql
FUNCTION get_flow_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N')
    RETURN LOAN_FLOW_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_stop_ratio_info` — FUNCTION

**Purpose:** Public function related to get stop ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 504; body declaration candidate line(s): 8151

**Signature**

```sql
FUNCTION get_stop_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N',
                               p_info_type varchar2 default 'INT')
    RETURN LOAN_STOP_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days` — FUNCTION

**Purpose:** Public function related to get incorrect days. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 510; body declaration candidate line(s): 8179

**Signature**

```sql
function get_incorrect_days(p_date date) return NUMBER_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days_count` — FUNCTION

**Purpose:** Public function related to get incorrect days count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 513; body declaration candidate line(s): 8218

**Signature**

```sql
function get_incorrect_days_count(p_date date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_schedule_from_memo` — FUNCTION

**Purpose:** Public function related to get schedule from memo. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 515; body declaration candidate line(s): 8225

**Signature**

```sql
function get_schedule_from_memo(p_memorandum_id varchar2,
                                  p_int_ratio     number,
                                  p_int_calc_type varchar2,
                                  p_int_amount    number) return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_standart_schedule` — FUNCTION

**Purpose:** Returns pipelined standard schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 521; body declaration candidate line(s): 8324

**Signature**

```sql
function get_standart_schedule(p_begin_date          date default glbl.getsysdate,
                                 p_main_pymt_date      date,
                                 p_int_pymt_date       date,
                                 p_pymt_day            number default null,
                                 p_end_date            date,
                                 p_offer_amount        number,
                                 p_ovd_main_amount     number default 0,
                                 p_int_calc_type       varchar2,
                                 p_main_grace_period   varchar2 default null,
                                 p_int_grace_period    varchar2 default null,
                                 p_remain_int_amount   number default 0,
                                 p_min_main_pay_amount number default null,
                                 p_calc_int_in_grace   varchar2 default 'Y',
                                 p_work_days           varchar2 default 'Y',
                                 
                                 p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                 p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_annuity_schedule` — FUNCTION

**Purpose:** Returns pipelined annuity schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 542; body declaration candidate line(s): 8697

**Signature**

```sql
function get_annuity_schedule(p_begin_date      date,
                                p_main_pymt_date  date,
                                p_int_pymt_date   date,
                                p_pymt_day        number default null,
                                p_end_date        date,
                                p_offer_amount    number,
                                p_ovd_main_amount number default 0,
                                p_int_calc_type   varchar2,
                                
                                p_main_grace_period varchar2 default null,
                                p_int_grace_period  varchar2 default null,
                                
                                p_annuity_amount     number default null,
                                p_max_annuity_amount number default null,
                                p_remain_int_amount  number default 0,
                                
                                p_work_days         varchar2 default 'Y',
                                p_own_annuity       varchar2 default 'N',
                                p_calc_int_in_grace varchar2 default 'Y',
                                p_is_mortgage       varchar2 default 'N',
                                
                                p_max_iteration number default null,
                                
                                p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_created_schedule` — PROCEDURE

**Purpose:** Public procedure related to get created schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 570; body declaration candidate line(s): 9306

**Signature**

```sql
Procedure get_created_schedule(p_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_schedule` — PROCEDURE

**Purpose:** Builds a payment schedule using the supplied dates, amounts, interest and schedule options.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 572; body declaration candidate line(s): 9392

**Signature**

```sql
-- new
  procedure create_schedule(p_schedule_no         number,
                            p_coll_name           varchar2 default null,
                            p_fk_id               number default null,
                            p_doc_no              varchar2 default 'XXX',
                            p_memorandum_id       varchar2 default null,
                            p_customer_no         number default null,
                            p_tx_fid              number default null,
                            p_begin_date          date default glbl.getsysdate,
                            p_main_pymt_date      date,
                            p_int_pymt_date       date,
                            p_pymt_day            number default null,
                            p_end_date            date,
                            p_offer_amount        number,
                            p_ovd_main_amount     number default 0,
                            p_int_ratio           number,
                            p_int_calc_type       varchar2,
                            p_annuity_amount      number default null,
                            p_max_annuity_amount  number default null,
                            p_min_main_pay_amount number default null,
                            p_remain_int_amount   number default 0,
                            p_main_grace_period   varchar2 default null,
                            p_int_grace_period    varchar2 default null,
                            p_main_pymt_period    number default 1,
                            p_int_pymt_period     number default 1,
                            p_product_code        number default null,
                            p_same_annuity        varchar2 default 'N',
                            p_calc_int_in_grace   varchar2 default 'Y',
                            p_return_type         varchar2 default 'NO_ZERO',
                            p_loan_flow_rate_tab  LOAN_FLOW_RATE_TAB default null,
                            p_loan_stop_rate_tab  LOAN_STOP_RATE_TAB default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 604; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 607; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate,
                            p_min_rowid rowid,
                            p_max_rowid rowid);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

## Payments & Allocation

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 71; body declaration candidate line(s): 70, 736

**Signature**

```sql
-- *

  procedure get_pen_info_for_calc(p_date                   in date default glbl.getsysdate,
                                  p_doc_no                 in varchar2,
                                  p_acc_type               in varchar2,
                                  p_pen_calc_grace_days    in number,
                                  p_ovd_amount             out number,
                                  p_calculated_pen_day_cnt out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates` — FUNCTION

**Purpose:** Builds an interest calculation date collection based on EOD/SOD scheduling and the last calculation access date.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 80; body declaration candidate line(s): 259

**Signature**

```sql
function get_interest_calc_dates(p_last_calc_access_date in date,
                                   p_eod_sod               in varchar2,
                                   p_int_calc_at           in varchar2)
    return loan_api.g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates_ex` — FUNCTION

**Purpose:** Public function related to get interest calc dates ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 85; body declaration candidate line(s): 323

**Signature**

```sql
function get_interest_calc_dates_ex(p_date        in date,
                                      p_eod_sod     in varchar2,
                                      p_int_calc_at in varchar2)
    return g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info` — PROCEDURE

**Purpose:** Determines interest calculation day count and year-day basis from interest-calculation configuration.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 90; body declaration candidate line(s): 104

**Signature**

```sql
procedure get_interest_calc_info(p_last_calc_date       in date,
                                   p_pymt_day             in number,
                                   p_trn_date             in date,
                                   p_int_calc_type        in varchar2,
                                   p_rate_type            in varchar2,
                                   p_int_rate_periodicity in varchar2,
                                   p_calc_day_count       out number,
                                   p_year_day_count       out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info_ex` — PROCEDURE

**Purpose:** Public procedure related to get interest calc info ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 101; body declaration candidate line(s): 183

**Signature**

```sql
procedure get_interest_calc_info_ex(p_last_calc_date in date,
                                   p_pymt_day       in number,
                                   p_trn_date       in date,
                                   p_int_calc_type  in varchar2,
                                   p_calc_day_count out number,
                                   p_year_day_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `clear_addtional_data` — PROCEDURE

**Purpose:** Public procedure related to clear addtional data. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 109; body declaration candidate line(s): 378

**Signature**

```sql
procedure clear_addtional_data(p_state varchar2 default 'CLEAR');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_group` — PROCEDURE

**Purpose:** Public procedure related to add additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 111; body declaration candidate line(s): 404

**Signature**

```sql
procedure add_additional_group(p_tag_name varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_group` — PROCEDURE

**Purpose:** Public procedure related to end additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 113; body declaration candidate line(s): 410

**Signature**

```sql
procedure end_additional_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_main_group` — PROCEDURE

**Purpose:** Public procedure related to end additional main group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 114; body declaration candidate line(s): 398

**Signature**

```sql
procedure end_additional_main_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 115; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 117; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 118; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value varchar2,
                              p_new_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 122; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value date,
                              p_new_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `finalize_addtional_process` — PROCEDURE

**Purpose:** Finalizes accumulated additional information and executes mapped updates for the supplied identifiers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 125; body declaration candidate line(s): 480

**Signature**

```sql
procedure finalize_addtional_process(p_doc_no   varchar2,
                                       p_offer_id varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `reverse_update` — PROCEDURE

**Purpose:** Reads prior history additional information and attempts to restore recorded old values.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 128; body declaration candidate line(s): 591

**Signature**

```sql
procedure reverse_update(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_loan_amount` — FUNCTION

**Purpose:** Returns a loan amount using the TOTAL, DEBT, or DUE calculation mode and related account and schedule data.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 130; body declaration candidate line(s): 643

**Signature**

```sql
function get_loan_amount(p_doc_no      in varchar2,
                           p_amount_type in varchar2,
                           p_date        in date default glbl.getsysdate,
                           p_oper_type   in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_overdue_min_amount` — FUNCTION

**Purpose:** Public function related to get overdue min amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 136; body declaration candidate line(s): 719

**Signature**

```sql
function get_overdue_min_amount(p_product_code in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 137; body declaration candidate line(s): 70, 736

**Signature**

```sql
procedure get_pen_info_for_calc(p_date                in date default glbl.getsysdate,
                                  p_doc_no              in varchar2,
                                  p_pen_calc_grace_days in number,
                                  p_PEN_INT_RATIO       in number,
                                  p_ovd_amount_for_pen  out number,
                                  p_pen_calc_days_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_trn_caller_id` — FUNCTION

**Purpose:** Public function related to get trn caller id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 144; body declaration candidate line(s): 772

**Signature**

```sql
function get_trn_caller_id(p_oper_type in varchar2) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_voucher_data_from_query` — FUNCTION

**Purpose:** Executes a supplied SQL query with DBMS_SQL and maps returned column values for vouchers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 146; body declaration candidate line(s): 789

**Signature**

```sql
function get_voucher_data_from_query(p_query       in varchar2,
                                       p_result_type in varchar2)
    return g_col_value_tab_map;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_formatted_grace_from_list` — FUNCTION

**Purpose:** Public function related to get formatted grace from list. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 150; body declaration candidate line(s): 912

**Signature**

```sql
function get_formatted_grace_from_list(p_period_list in varchar2)
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_grace_info` — FUNCTION

**Purpose:** Public function related to get grace info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 153; body declaration candidate line(s): 952

**Signature**

```sql
function get_grace_info(p_Doc_No          In Varchar2,
                          p_period_end_date in date,
                          p_acc_type        In Varchar2 default 'A',
                          p_info_type       in varchar2) Return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_basis_year_days_cnt` — FUNCTION

**Purpose:** Public function related to get basis year days cnt. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 158; body declaration candidate line(s): 998

**Signature**

```sql
function get_basis_year_days_cnt(p_int_calc_type in varchar2,
                                   p_date          in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_value` — FUNCTION

**Purpose:** Public function related to get gl value. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 161; body declaration candidate line(s): 1026

**Signature**

```sql
function get_gl_value(p_parameter_name in varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 163; body declaration candidate line(s): 1043

**Signature**

```sql
procedure loan_int_diff_operation(p_trn_date        in date,
                                    p_oper_type       in varchar2,
                                    p_trn_type        in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation_ex` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 177; body declaration candidate line(s): 1197

**Signature**

```sql
procedure loan_int_diff_operation_ex(p_oper_type       in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_active_passive` — FUNCTION

**Purpose:** Public function related to get gl acc active passive. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 189; body declaration candidate line(s): 1345

**Signature**

```sql
function get_gl_acc_active_passive(p_acc_no in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_from_matrix` — FUNCTION

**Purpose:** Public function related to get gl acc from matrix. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 191; body declaration candidate line(s): 1367

**Signature**

```sql
function get_gl_acc_from_matrix(p_product_code in number default null,
                                  p_cust_type    in number default null,
                                  p_period_id    in number default null,
                                  p_currency_id  in number default null,
                                  p_base_type    in varchar2,
                                  p_loan_doc_no  in varchar2 default null,
                                  p_customer_no  in varchar2 default null,
                                  p_acc_type     in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `Get_Delay_Int_Rate` — FUNCTION

**Purpose:** Public function related to get delay int rate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 200; body declaration candidate line(s): 1602

**Signature**

```sql
-- krd_eod.Get_Delay_Int_Rate
  Function Get_Delay_Int_Rate(p_Loan_Id    In Varchar2,
                              p_Delay_Type In Varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_commission_schedule` — FUNCTION

**Purpose:** Public function related to get commission schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 203; body declaration candidate line(s): 1628

**Signature**

```sql
-- kredi_api.Get_Krd_Kom_Plan
  Function get_commission_schedule(p_begin_date    In Date,
                                   p_end_date      In Date,
                                   p_amount        In Number,
                                   p_int_calc_type in varchar2)
    Return Krd_Kom_Plan_Tt
    Pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_months_for_loan` — FUNCTION

**Purpose:** Public function related to add months for loan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 211; body declaration candidate line(s): 1744

**Signature**

```sql
function add_months_for_loan(p_date   date,
                               p_months number,
                               p_day    number default null) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_next_Plan_Pym` — FUNCTION

**Purpose:** Public function related to get next plan pym. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 215; body declaration candidate line(s): 1776

**Signature**

```sql
Function get_next_Plan_Pym(p_doc_no   In Varchar2,
                             P_date     In Date,
                             p_acc_type in varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_offer_id` — FUNCTION

**Purpose:** Public function related to get offer id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 219; body declaration candidate line(s): 1809

**Signature**

```sql
Function get_offer_id(p_branch_id In Number Default Glbl.Getsube,
                        P_date      In Date Default Glbl.Getsysdate)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_payment_amount` — FUNCTION

**Purpose:** Public function related to get plan payment amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 223; body declaration candidate line(s): 1832

**Signature**

```sql
-- krd_eod.get_Plan_Pym +
  function get_plan_payment_amount(p_doc_no   in varchar2,
                                   p_date     in date default glbl.getsysdate,
                                   p_acc_type in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_ovd_date` — FUNCTION

**Purpose:** Public function related to get ovd date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 229; body declaration candidate line(s): 2734

**Signature**

```sql
Function get_ovd_date(p_doc_no   varchar2,
                        p_acc_type varchar2,
                        p_date     date default glbl.getsysdate) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_amount_for_pen_calc` — FUNCTION

**Purpose:** Public function related to get amount for pen calc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 233; body declaration candidate line(s): 1850

**Signature**

```sql
Function get_amount_for_pen_calc(p_doc_no        In Varchar2,
                                   P_date          In Date,
                                   p_for_spec_days in varchar2 default 'N',
                                   p_int_calc_type in varchar2 default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Plan_Month_Count` — FUNCTION

**Purpose:** Public function related to get plan month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 239; body declaration candidate line(s): 1944

**Signature**

```sql
-- kredi_api.get_Plan_Month_Count +
  /*Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ')
    Return Number;*/
  Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ',
                                p_work_days     varchar2 default 'Y',
                                p_pymt_day      number default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_paid_month_count` — FUNCTION

**Purpose:** Public function related to get plan paid month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 251; body declaration candidate line(s): 1987

**Signature**

```sql
-- new
  function get_plan_paid_month_count(p_doc_no in varchar2,
                                     p_term   in number,
                                     p_date   in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_error` — FUNCTION

**Purpose:** Public function related to get plan error. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 255; body declaration candidate line(s): 2047

**Signature**

```sql
-- kredi_api.get_plan_error +
  Function get_plan_error(p_doc_no varchar2, p_date date default glbl.getsysdate) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Annuity_Amount` — FUNCTION

**Purpose:** Public function related to get annuity amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 258; body declaration candidate line(s): 2604

**Signature**

```sql
-- kredi_api.Get_Annuitet_Amount +
  Function get_Annuity_Amount(p_Doc_No      In Varchar2,
                              p_return_type In varchar2 default 'NO_ZERO')
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Pym_Startdate` — FUNCTION

**Purpose:** Public function related to get pym startdate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 263; body declaration candidate line(s): 2633

**Signature**

```sql
-- kredi_api.Get_Pym_Startdate +
  Function get_Pym_Startdate(p_Doc_No          In Varchar2,
                             p_pymt_date       In Date,
                             p_pymt_day        In Number,
                             p_pymt_period     In Number,
                             p_acc_type        In varchar2,
                             p_loan_end_Date   in date,
                             p_check_is_closed in varchar2 default 'Y')
    Return Date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_account_feature` — FUNCTION

**Purpose:** Public function related to get account feature. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 273; body declaration candidate line(s): 2799

**Signature**

```sql
function get_account_feature(p_branch_no   number,
                               p_account_no  number,
                               p_account_sub number)
    return cs_account.account_feature%type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_acc_exists` — FUNCTION

**Purpose:** Public function related to is acc exists. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 278; body declaration candidate line(s): 2818

**Signature**

```sql
function is_acc_exists(p_customer_no   number,
                         p_memorandum_id varchar2 default null,
                         p_doc_no        varchar2,
                         p_acc_type      varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_Payment_Date` — FUNCTION

**Purpose:** Public function related to is payment date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 283; body declaration candidate line(s): 2845

**Signature**

```sql
-- kredi_api.Is_Payment_Date +
  Function is_Payment_Date(p_Document_No In Varchar2, p_Date Date)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_online_offer` — FUNCTION

**Purpose:** Public function related to is online offer. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 287; body declaration candidate line(s): 2858

**Signature**

```sql
function is_online_offer(p_memorandum_id varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `table_log_operation` — PROCEDURE

**Purpose:** Public procedure related to table log operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 289; body declaration candidate line(s): 3344

**Signature**

```sql
procedure table_log_operation(p_doc_no     in varchar2,
                                p_table_name in varchar2,
                                p_tx_fid     in number,
                                p_oper_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_entry` — PROCEDURE

**Purpose:** Public procedure related to do journal entry. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 294; body declaration candidate line(s): 2876

**Signature**

```sql
Procedure do_journal_entry(p_entries_list  g_entries_list_tab,
                             p_trn_caller_id in number,
                             p_tx_fid        in out number,
                             p_trn_type      in varchar2,
                             p_is_eod        in varchar2 default 'Y');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_journal_entries` — PROCEDURE

**Purpose:** Public procedure related to create journal entries. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 300; body declaration candidate line(s): 2954

**Signature**

```sql
procedure create_journal_entries(p_oper_type in varchar2,
                                   p_tx_fid    in number,
                                   p_trn_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_account` — PROCEDURE

**Purpose:** Creates/assigns loan-related accounts based on the requested operation and returns the created account list.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 304; body declaration candidate line(s): 3129

**Signature**

```sql
procedure create_account(p_doc_no        in varchar2,
                           p_memorandum_id in varchar2 default null,
                           p_oper_type     in varchar2,
                           p_acc_type      in varchar2 default null,
                           p_tx_fid        in number,
                           p_created_acc   out g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `recalculate_int_payment_plan` — PROCEDURE

**Purpose:** Public procedure related to recalculate int payment plan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 311; body declaration candidate line(s): 3445

**Signature**

```sql
procedure recalculate_int_payment_plan(p_doc_no               in varchar2,
                                         p_acc_type             in varchar2,
                                         p_main_amount          in number,
                                         p_INT_RATIO            in number,
                                         p_int_calc_type        in varchar2,
                                         p_schedule_update_type in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_new_acc` — FUNCTION

**Purpose:** Public function related to get new acc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 318; body declaration candidate line(s): 2520

**Signature**

```sql
--kredi_api.open_new_acc +
  function get_new_acc(p_branch_no       in number,
                       p_customer_no     in number,
                       p_balance_acc     in varchar2,
                       p_detail_code     in varchar2,
                       p_ccy_id          in number,
                       p_main_acc        in number default null,
                       p_cr_int_rate     in number default null,
                       p_dr_int_rate     in number default null,
                       p_com_int_rate    in number default null,
                       p_product_code    in number default null,
                       p_period_id       in number default null,
                       p_acc_description in varchar2,
                       p_memorandum_id   in varchar2 default null,
                       p_loan_doc_no     in varchar2,
                       p_loan_acc_type   in varchar2,
                       p_tx_fid          in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_plan_control` — PROCEDURE

**Purpose:** Public procedure related to do plan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 336; body declaration candidate line(s): 3506

**Signature**

```sql
-- kredi_api.plan_control +
  procedure do_plan_control(p_document_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_status_control` — PROCEDURE

**Purpose:** Public procedure related to do loan status control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 338; body declaration candidate line(s): 3515

**Signature**

```sql
-- kredi_api.loan_status_control +
  procedure do_loan_status_control(p_branch_no   in number,
                                   p_customer_no in number,
                                   p_loan_acc    in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_loan_history` — PROCEDURE

**Purpose:** Writes a loan-operation history record for a transaction.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 343; body declaration candidate line(s): 3587

**Signature**

```sql
procedure create_loan_history(p_oper_type VARCHAR2 default null,
                                p_doc_no    VARCHAR2 default null,
                                p_trn_date  DATE default glbl.getsysdate,
                                p_tx_fid    NUMBER,
                                p_trn_type  varchar2,
                                p_add_info  add_info_tab default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_collateral_out` — PROCEDURE

**Purpose:** Public procedure related to do loan collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 350; body declaration candidate line(s): 3942

**Signature**

```sql
--krd_eod.loan_collateral_out +
  procedure do_loan_collateral_out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_acc_type_by_status` — FUNCTION

**Purpose:** Public function related to get acc type by status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 353; body declaration candidate line(s): 4211

**Signature**

```sql
function get_acc_type_by_status(p_acc_type         varchar2,
                                  p_to_loan_status   varchar2,
                                  p_from_loan_status varchar2 default 'NORM')
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `generate_allocated_payment_list` — PROCEDURE

**Purpose:** Computes a payment allocation list for a loan operation.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 358; body declaration candidate line(s): 4239

**Signature**

```sql
procedure generate_allocated_payment_list(p_doc_no                in varchar2,
                                            p_oper_type             in varchar2,
                                            p_pym_amount            in number,
                                            p_has_schedule_upd_type out varchar2,
                                            p_payment_list          out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_payment_details` — PROCEDURE

**Purpose:** Public procedure related to add payment details. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 364; body declaration candidate line(s): 4389

**Signature**

```sql
procedure add_payment_details(p_doc_no                in varchar2,
                                p_has_schedule_upd_type out varchar2,
                                p_payment_list          in out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_delete_operation` — PROCEDURE

**Purpose:** Public procedure related to do delete operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 368; body declaration candidate line(s): 4483

**Signature**

```sql
procedure do_delete_operation(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Auto_Payment` — PROCEDURE

**Purpose:** Executes automatic loan payment processing in EOD/SOD context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 370; body declaration candidate line(s): 4540

**Signature**

```sql
/** Makes automatic loan payments at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S                           
  */
  Procedure do_Auto_Payment(p_min_id     number default null,
                            p_max_id     number default null,
                            p_doc_no     in varchar2 default null,
                            p_eod_sod    in varchar2 default 'E',
                            p_test_param in number default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation` — PROCEDURE

**Purpose:** Performs batch interest calculation with optional branch range, loan document and EOD/SOD arguments.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 382; body declaration candidate line(s): 5135

**Signature**

```sql
/** Makes automatic loan int calculation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S 
      p_date - operation date                            
  */
  
  procedure do_int_calculation(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation_ex` — PROCEDURE

**Purpose:** Public procedure related to do int calculation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 396; body declaration candidate line(s): 5768

**Signature**

```sql
procedure do_int_calculation_ex(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_overdue_transit_operation` — PROCEDURE

**Purpose:** Public procedure related to do overdue transit operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 402; body declaration candidate line(s): 4832

**Signature**

```sql
/** Makes automatic loan overdue operation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_branch_id - loan branch id  
      p_customer_no - unique customer number 
      p_loan_acc - loan account sub 
      p_date - operation date                            
  */

  Procedure do_overdue_transit_operation(p_min_id number default null,
                                         p_max_id number default null,
                                         p_doc_no in varchar2 default null,
                                         p_date   in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_commission_recognition` — PROCEDURE

**Purpose:** Public procedure related to do commission recognition. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 416; body declaration candidate line(s): 6338

**Signature**

```sql
Procedure do_commission_recognition(Pdate In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_guarantee_out` — PROCEDURE

**Purpose:** Public procedure related to do guarantee out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 418; body declaration candidate line(s): 6236

**Signature**

```sql
Procedure do_guarantee_out(p_branch_id   In Number Default Null,
                             p_customer_no In Number Default Null,
                             p_loan_acc    In Number Default Null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Close_With_Collateral_Out` — PROCEDURE

**Purpose:** Public procedure related to do loan close with collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 422; body declaration candidate line(s): 6594

**Signature**

```sql
procedure do_Loan_Close_With_Collateral_Out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_non_cash_loan_close` — PROCEDURE

**Purpose:** Public procedure related to do non cash loan close. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 424; body declaration candidate line(s): 6756

**Signature**

```sql
Procedure do_non_cash_loan_close(p_doc_no in varchar2,
                                   p_Date   In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_control` — PROCEDURE

**Purpose:** Public procedure related to do journal control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 427; body declaration candidate line(s): 6861

**Signature**

```sql
-- new
  procedure do_journal_control(p_branch_id   IN Number,
                               p_customer_no IN Number,
                               p_account_sub IN Number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 431; body declaration candidate line(s): 7118

**Signature**

```sql
-- new
  /*procedure over_to_norm(p_min_id  number default null,
                              p_max_id  number default null,
                              p_doc_no  in varchar2 default null);
  */
  --kredi_api.Odeme_Plani_Duzenle
  Procedure do_schedule_allignment(p_doc_no         In Varchar2,
                                   p_payment_amount In Number,
                                   p_acc_type       In Varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_com_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do com schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 441; body declaration candidate line(s): 7190

**Signature**

```sql
-- kredi_api.Kom_Odeme_Plani_Duzenle
  Procedure do_com_schedule_allignment(p_doc_no      In Varchar2,
                                       p_option_code In Varchar2,
                                       p_amount      In Number,
                                       p_plan_type   In Varchar2,
                                       p_mig_status  In Number Default 0);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Delay_Int_Rate_Upd` — PROCEDURE

**Purpose:** Public procedure related to do loan delay int rate upd. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 448; body declaration candidate line(s): 7310

**Signature**

```sql
-- krd_eod.Loan_Delay_Int_Rate_Upd
  Procedure do_Loan_Delay_Int_Rate_Upd;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `change_account_status` — PROCEDURE

**Purpose:** Public procedure related to change account status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 451; body declaration candidate line(s): 7351

**Signature**

```sql
-- kredi_api.Kredi_Hesap_Kapat , kredi_api.Kredi_Hesap_Ac
  procedure change_account_status(p_doc_no in varchar2,
                                  p_status in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_eod_task` — PROCEDURE

**Purpose:** Public procedure related to stop eod task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 455; body declaration candidate line(s): 7389

**Signature**

```sql
procedure stop_eod_task;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_loan_task` — PROCEDURE

**Purpose:** Public procedure related to stop loan task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 457; body declaration candidate line(s): 7405

**Signature**

```sql
procedure stop_loan_task(p_task_code in varchar2 default null,
                           p_task_type in varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `run_loan_task` — PROCEDURE

**Purpose:** Runs a task identified by its task code and task type.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 460; body declaration candidate line(s): 7442

**Signature**

```sql
/** Parallel execution for loan processes
      @params
      p_task_code  - task_code in loan_tasks_list table                  
  */

  procedure run_loan_task(p_task_code in varchar2, p_task_type in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `calculate_xirr` — FUNCTION

**Purpose:** Public function related to calculate xirr. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 467; body declaration candidate line(s): 7786

**Signature**

```sql
/*procedure norm_to_over(p_min_id  number default null,
  p_max_id  number default null,
  p_doc_no  in varchar2 default null);  */

  function calculate_xirr(p_doc_no  varchar2,
                          p_type    varchar2,
                          p_calc_as varchar2 default 'XIRR') return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_min_flow_ratio` — FUNCTION

**Purpose:** Public function related to get min flow ratio. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 475; body declaration candidate line(s): 8074

**Signature**

```sql
/*  function get_mix_operation_acsess(p_fid            varchar2,
                                      p_oper_type      varchar2,
                                      p_memo_oper_type varchar2) return number;
  
    function get_mix_operation_types(p_fid            varchar2,
                                     p_memo_oper_type varchar2) return varchar2;
  
    procedure validate_mix_memorandum(p_memorandum_id varchar2,
                                      p_oper_type     varchar2,
                                      p_state         varchar2);
  
    procedure update_mix_memorandum(p_memorandum_id varchar2,
                                    p_oper_type     varchar2,
                                    p_tx_fid        number,
                                    p_state         varchar2);
  */

  function get_min_flow_ratio(
    p_doc_no     varchar2,
    p_type       varchar2,
    p_begin_date date default null,
    p_end_date   date default null
  ) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_flow_ratio_info` — FUNCTION

**Purpose:** Public function related to get flow ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 499; body declaration candidate line(s): 8115

**Signature**

```sql
FUNCTION get_flow_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N')
    RETURN LOAN_FLOW_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_stop_ratio_info` — FUNCTION

**Purpose:** Public function related to get stop ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 504; body declaration candidate line(s): 8151

**Signature**

```sql
FUNCTION get_stop_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N',
                               p_info_type varchar2 default 'INT')
    RETURN LOAN_STOP_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days` — FUNCTION

**Purpose:** Public function related to get incorrect days. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 510; body declaration candidate line(s): 8179

**Signature**

```sql
function get_incorrect_days(p_date date) return NUMBER_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days_count` — FUNCTION

**Purpose:** Public function related to get incorrect days count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 513; body declaration candidate line(s): 8218

**Signature**

```sql
function get_incorrect_days_count(p_date date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_schedule_from_memo` — FUNCTION

**Purpose:** Public function related to get schedule from memo. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 515; body declaration candidate line(s): 8225

**Signature**

```sql
function get_schedule_from_memo(p_memorandum_id varchar2,
                                  p_int_ratio     number,
                                  p_int_calc_type varchar2,
                                  p_int_amount    number) return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_standart_schedule` — FUNCTION

**Purpose:** Returns pipelined standard schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 521; body declaration candidate line(s): 8324

**Signature**

```sql
function get_standart_schedule(p_begin_date          date default glbl.getsysdate,
                                 p_main_pymt_date      date,
                                 p_int_pymt_date       date,
                                 p_pymt_day            number default null,
                                 p_end_date            date,
                                 p_offer_amount        number,
                                 p_ovd_main_amount     number default 0,
                                 p_int_calc_type       varchar2,
                                 p_main_grace_period   varchar2 default null,
                                 p_int_grace_period    varchar2 default null,
                                 p_remain_int_amount   number default 0,
                                 p_min_main_pay_amount number default null,
                                 p_calc_int_in_grace   varchar2 default 'Y',
                                 p_work_days           varchar2 default 'Y',
                                 
                                 p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                 p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_annuity_schedule` — FUNCTION

**Purpose:** Returns pipelined annuity schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 542; body declaration candidate line(s): 8697

**Signature**

```sql
function get_annuity_schedule(p_begin_date      date,
                                p_main_pymt_date  date,
                                p_int_pymt_date   date,
                                p_pymt_day        number default null,
                                p_end_date        date,
                                p_offer_amount    number,
                                p_ovd_main_amount number default 0,
                                p_int_calc_type   varchar2,
                                
                                p_main_grace_period varchar2 default null,
                                p_int_grace_period  varchar2 default null,
                                
                                p_annuity_amount     number default null,
                                p_max_annuity_amount number default null,
                                p_remain_int_amount  number default 0,
                                
                                p_work_days         varchar2 default 'Y',
                                p_own_annuity       varchar2 default 'N',
                                p_calc_int_in_grace varchar2 default 'Y',
                                p_is_mortgage       varchar2 default 'N',
                                
                                p_max_iteration number default null,
                                
                                p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_created_schedule` — PROCEDURE

**Purpose:** Public procedure related to get created schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 570; body declaration candidate line(s): 9306

**Signature**

```sql
Procedure get_created_schedule(p_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_schedule` — PROCEDURE

**Purpose:** Builds a payment schedule using the supplied dates, amounts, interest and schedule options.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 572; body declaration candidate line(s): 9392

**Signature**

```sql
-- new
  procedure create_schedule(p_schedule_no         number,
                            p_coll_name           varchar2 default null,
                            p_fk_id               number default null,
                            p_doc_no              varchar2 default 'XXX',
                            p_memorandum_id       varchar2 default null,
                            p_customer_no         number default null,
                            p_tx_fid              number default null,
                            p_begin_date          date default glbl.getsysdate,
                            p_main_pymt_date      date,
                            p_int_pymt_date       date,
                            p_pymt_day            number default null,
                            p_end_date            date,
                            p_offer_amount        number,
                            p_ovd_main_amount     number default 0,
                            p_int_ratio           number,
                            p_int_calc_type       varchar2,
                            p_annuity_amount      number default null,
                            p_max_annuity_amount  number default null,
                            p_min_main_pay_amount number default null,
                            p_remain_int_amount   number default 0,
                            p_main_grace_period   varchar2 default null,
                            p_int_grace_period    varchar2 default null,
                            p_main_pymt_period    number default 1,
                            p_int_pymt_period     number default 1,
                            p_product_code        number default null,
                            p_same_annuity        varchar2 default 'N',
                            p_calc_int_in_grace   varchar2 default 'Y',
                            p_return_type         varchar2 default 'NO_ZERO',
                            p_loan_flow_rate_tab  LOAN_FLOW_RATE_TAB default null,
                            p_loan_stop_rate_tab  LOAN_STOP_RATE_TAB default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 604; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 607; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate,
                            p_min_rowid rowid,
                            p_max_rowid rowid);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

## Schedules & Rates

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 71; body declaration candidate line(s): 70, 736

**Signature**

```sql
-- *

  procedure get_pen_info_for_calc(p_date                   in date default glbl.getsysdate,
                                  p_doc_no                 in varchar2,
                                  p_acc_type               in varchar2,
                                  p_pen_calc_grace_days    in number,
                                  p_ovd_amount             out number,
                                  p_calculated_pen_day_cnt out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates` — FUNCTION

**Purpose:** Builds an interest calculation date collection based on EOD/SOD scheduling and the last calculation access date.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 80; body declaration candidate line(s): 259

**Signature**

```sql
function get_interest_calc_dates(p_last_calc_access_date in date,
                                   p_eod_sod               in varchar2,
                                   p_int_calc_at           in varchar2)
    return loan_api.g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates_ex` — FUNCTION

**Purpose:** Public function related to get interest calc dates ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 85; body declaration candidate line(s): 323

**Signature**

```sql
function get_interest_calc_dates_ex(p_date        in date,
                                      p_eod_sod     in varchar2,
                                      p_int_calc_at in varchar2)
    return g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info` — PROCEDURE

**Purpose:** Determines interest calculation day count and year-day basis from interest-calculation configuration.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 90; body declaration candidate line(s): 104

**Signature**

```sql
procedure get_interest_calc_info(p_last_calc_date       in date,
                                   p_pymt_day             in number,
                                   p_trn_date             in date,
                                   p_int_calc_type        in varchar2,
                                   p_rate_type            in varchar2,
                                   p_int_rate_periodicity in varchar2,
                                   p_calc_day_count       out number,
                                   p_year_day_count       out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info_ex` — PROCEDURE

**Purpose:** Public procedure related to get interest calc info ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 101; body declaration candidate line(s): 183

**Signature**

```sql
procedure get_interest_calc_info_ex(p_last_calc_date in date,
                                   p_pymt_day       in number,
                                   p_trn_date       in date,
                                   p_int_calc_type  in varchar2,
                                   p_calc_day_count out number,
                                   p_year_day_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `clear_addtional_data` — PROCEDURE

**Purpose:** Public procedure related to clear addtional data. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 109; body declaration candidate line(s): 378

**Signature**

```sql
procedure clear_addtional_data(p_state varchar2 default 'CLEAR');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_group` — PROCEDURE

**Purpose:** Public procedure related to add additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 111; body declaration candidate line(s): 404

**Signature**

```sql
procedure add_additional_group(p_tag_name varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_group` — PROCEDURE

**Purpose:** Public procedure related to end additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 113; body declaration candidate line(s): 410

**Signature**

```sql
procedure end_additional_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_main_group` — PROCEDURE

**Purpose:** Public procedure related to end additional main group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 114; body declaration candidate line(s): 398

**Signature**

```sql
procedure end_additional_main_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 115; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 117; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 118; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value varchar2,
                              p_new_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 122; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value date,
                              p_new_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `finalize_addtional_process` — PROCEDURE

**Purpose:** Finalizes accumulated additional information and executes mapped updates for the supplied identifiers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 125; body declaration candidate line(s): 480

**Signature**

```sql
procedure finalize_addtional_process(p_doc_no   varchar2,
                                       p_offer_id varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `reverse_update` — PROCEDURE

**Purpose:** Reads prior history additional information and attempts to restore recorded old values.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 128; body declaration candidate line(s): 591

**Signature**

```sql
procedure reverse_update(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_loan_amount` — FUNCTION

**Purpose:** Returns a loan amount using the TOTAL, DEBT, or DUE calculation mode and related account and schedule data.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 130; body declaration candidate line(s): 643

**Signature**

```sql
function get_loan_amount(p_doc_no      in varchar2,
                           p_amount_type in varchar2,
                           p_date        in date default glbl.getsysdate,
                           p_oper_type   in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_overdue_min_amount` — FUNCTION

**Purpose:** Public function related to get overdue min amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 136; body declaration candidate line(s): 719

**Signature**

```sql
function get_overdue_min_amount(p_product_code in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 137; body declaration candidate line(s): 70, 736

**Signature**

```sql
procedure get_pen_info_for_calc(p_date                in date default glbl.getsysdate,
                                  p_doc_no              in varchar2,
                                  p_pen_calc_grace_days in number,
                                  p_PEN_INT_RATIO       in number,
                                  p_ovd_amount_for_pen  out number,
                                  p_pen_calc_days_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_trn_caller_id` — FUNCTION

**Purpose:** Public function related to get trn caller id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 144; body declaration candidate line(s): 772

**Signature**

```sql
function get_trn_caller_id(p_oper_type in varchar2) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_voucher_data_from_query` — FUNCTION

**Purpose:** Executes a supplied SQL query with DBMS_SQL and maps returned column values for vouchers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 146; body declaration candidate line(s): 789

**Signature**

```sql
function get_voucher_data_from_query(p_query       in varchar2,
                                       p_result_type in varchar2)
    return g_col_value_tab_map;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_formatted_grace_from_list` — FUNCTION

**Purpose:** Public function related to get formatted grace from list. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 150; body declaration candidate line(s): 912

**Signature**

```sql
function get_formatted_grace_from_list(p_period_list in varchar2)
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_grace_info` — FUNCTION

**Purpose:** Public function related to get grace info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 153; body declaration candidate line(s): 952

**Signature**

```sql
function get_grace_info(p_Doc_No          In Varchar2,
                          p_period_end_date in date,
                          p_acc_type        In Varchar2 default 'A',
                          p_info_type       in varchar2) Return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_basis_year_days_cnt` — FUNCTION

**Purpose:** Public function related to get basis year days cnt. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 158; body declaration candidate line(s): 998

**Signature**

```sql
function get_basis_year_days_cnt(p_int_calc_type in varchar2,
                                   p_date          in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_value` — FUNCTION

**Purpose:** Public function related to get gl value. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 161; body declaration candidate line(s): 1026

**Signature**

```sql
function get_gl_value(p_parameter_name in varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 163; body declaration candidate line(s): 1043

**Signature**

```sql
procedure loan_int_diff_operation(p_trn_date        in date,
                                    p_oper_type       in varchar2,
                                    p_trn_type        in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation_ex` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 177; body declaration candidate line(s): 1197

**Signature**

```sql
procedure loan_int_diff_operation_ex(p_oper_type       in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_active_passive` — FUNCTION

**Purpose:** Public function related to get gl acc active passive. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 189; body declaration candidate line(s): 1345

**Signature**

```sql
function get_gl_acc_active_passive(p_acc_no in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_from_matrix` — FUNCTION

**Purpose:** Public function related to get gl acc from matrix. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 191; body declaration candidate line(s): 1367

**Signature**

```sql
function get_gl_acc_from_matrix(p_product_code in number default null,
                                  p_cust_type    in number default null,
                                  p_period_id    in number default null,
                                  p_currency_id  in number default null,
                                  p_base_type    in varchar2,
                                  p_loan_doc_no  in varchar2 default null,
                                  p_customer_no  in varchar2 default null,
                                  p_acc_type     in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `Get_Delay_Int_Rate` — FUNCTION

**Purpose:** Public function related to get delay int rate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 200; body declaration candidate line(s): 1602

**Signature**

```sql
-- krd_eod.Get_Delay_Int_Rate
  Function Get_Delay_Int_Rate(p_Loan_Id    In Varchar2,
                              p_Delay_Type In Varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_commission_schedule` — FUNCTION

**Purpose:** Public function related to get commission schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 203; body declaration candidate line(s): 1628

**Signature**

```sql
-- kredi_api.Get_Krd_Kom_Plan
  Function get_commission_schedule(p_begin_date    In Date,
                                   p_end_date      In Date,
                                   p_amount        In Number,
                                   p_int_calc_type in varchar2)
    Return Krd_Kom_Plan_Tt
    Pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_months_for_loan` — FUNCTION

**Purpose:** Public function related to add months for loan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 211; body declaration candidate line(s): 1744

**Signature**

```sql
function add_months_for_loan(p_date   date,
                               p_months number,
                               p_day    number default null) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_next_Plan_Pym` — FUNCTION

**Purpose:** Public function related to get next plan pym. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 215; body declaration candidate line(s): 1776

**Signature**

```sql
Function get_next_Plan_Pym(p_doc_no   In Varchar2,
                             P_date     In Date,
                             p_acc_type in varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_offer_id` — FUNCTION

**Purpose:** Public function related to get offer id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 219; body declaration candidate line(s): 1809

**Signature**

```sql
Function get_offer_id(p_branch_id In Number Default Glbl.Getsube,
                        P_date      In Date Default Glbl.Getsysdate)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_payment_amount` — FUNCTION

**Purpose:** Public function related to get plan payment amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 223; body declaration candidate line(s): 1832

**Signature**

```sql
-- krd_eod.get_Plan_Pym +
  function get_plan_payment_amount(p_doc_no   in varchar2,
                                   p_date     in date default glbl.getsysdate,
                                   p_acc_type in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_ovd_date` — FUNCTION

**Purpose:** Public function related to get ovd date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 229; body declaration candidate line(s): 2734

**Signature**

```sql
Function get_ovd_date(p_doc_no   varchar2,
                        p_acc_type varchar2,
                        p_date     date default glbl.getsysdate) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_amount_for_pen_calc` — FUNCTION

**Purpose:** Public function related to get amount for pen calc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 233; body declaration candidate line(s): 1850

**Signature**

```sql
Function get_amount_for_pen_calc(p_doc_no        In Varchar2,
                                   P_date          In Date,
                                   p_for_spec_days in varchar2 default 'N',
                                   p_int_calc_type in varchar2 default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Plan_Month_Count` — FUNCTION

**Purpose:** Public function related to get plan month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 239; body declaration candidate line(s): 1944

**Signature**

```sql
-- kredi_api.get_Plan_Month_Count +
  /*Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ')
    Return Number;*/
  Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ',
                                p_work_days     varchar2 default 'Y',
                                p_pymt_day      number default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_paid_month_count` — FUNCTION

**Purpose:** Public function related to get plan paid month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 251; body declaration candidate line(s): 1987

**Signature**

```sql
-- new
  function get_plan_paid_month_count(p_doc_no in varchar2,
                                     p_term   in number,
                                     p_date   in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_error` — FUNCTION

**Purpose:** Public function related to get plan error. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 255; body declaration candidate line(s): 2047

**Signature**

```sql
-- kredi_api.get_plan_error +
  Function get_plan_error(p_doc_no varchar2, p_date date default glbl.getsysdate) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Annuity_Amount` — FUNCTION

**Purpose:** Public function related to get annuity amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 258; body declaration candidate line(s): 2604

**Signature**

```sql
-- kredi_api.Get_Annuitet_Amount +
  Function get_Annuity_Amount(p_Doc_No      In Varchar2,
                              p_return_type In varchar2 default 'NO_ZERO')
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Pym_Startdate` — FUNCTION

**Purpose:** Public function related to get pym startdate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 263; body declaration candidate line(s): 2633

**Signature**

```sql
-- kredi_api.Get_Pym_Startdate +
  Function get_Pym_Startdate(p_Doc_No          In Varchar2,
                             p_pymt_date       In Date,
                             p_pymt_day        In Number,
                             p_pymt_period     In Number,
                             p_acc_type        In varchar2,
                             p_loan_end_Date   in date,
                             p_check_is_closed in varchar2 default 'Y')
    Return Date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_account_feature` — FUNCTION

**Purpose:** Public function related to get account feature. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 273; body declaration candidate line(s): 2799

**Signature**

```sql
function get_account_feature(p_branch_no   number,
                               p_account_no  number,
                               p_account_sub number)
    return cs_account.account_feature%type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_acc_exists` — FUNCTION

**Purpose:** Public function related to is acc exists. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 278; body declaration candidate line(s): 2818

**Signature**

```sql
function is_acc_exists(p_customer_no   number,
                         p_memorandum_id varchar2 default null,
                         p_doc_no        varchar2,
                         p_acc_type      varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_Payment_Date` — FUNCTION

**Purpose:** Public function related to is payment date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 283; body declaration candidate line(s): 2845

**Signature**

```sql
-- kredi_api.Is_Payment_Date +
  Function is_Payment_Date(p_Document_No In Varchar2, p_Date Date)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_online_offer` — FUNCTION

**Purpose:** Public function related to is online offer. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 287; body declaration candidate line(s): 2858

**Signature**

```sql
function is_online_offer(p_memorandum_id varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `table_log_operation` — PROCEDURE

**Purpose:** Public procedure related to table log operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 289; body declaration candidate line(s): 3344

**Signature**

```sql
procedure table_log_operation(p_doc_no     in varchar2,
                                p_table_name in varchar2,
                                p_tx_fid     in number,
                                p_oper_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_entry` — PROCEDURE

**Purpose:** Public procedure related to do journal entry. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 294; body declaration candidate line(s): 2876

**Signature**

```sql
Procedure do_journal_entry(p_entries_list  g_entries_list_tab,
                             p_trn_caller_id in number,
                             p_tx_fid        in out number,
                             p_trn_type      in varchar2,
                             p_is_eod        in varchar2 default 'Y');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_journal_entries` — PROCEDURE

**Purpose:** Public procedure related to create journal entries. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 300; body declaration candidate line(s): 2954

**Signature**

```sql
procedure create_journal_entries(p_oper_type in varchar2,
                                   p_tx_fid    in number,
                                   p_trn_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_account` — PROCEDURE

**Purpose:** Creates/assigns loan-related accounts based on the requested operation and returns the created account list.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 304; body declaration candidate line(s): 3129

**Signature**

```sql
procedure create_account(p_doc_no        in varchar2,
                           p_memorandum_id in varchar2 default null,
                           p_oper_type     in varchar2,
                           p_acc_type      in varchar2 default null,
                           p_tx_fid        in number,
                           p_created_acc   out g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `recalculate_int_payment_plan` — PROCEDURE

**Purpose:** Public procedure related to recalculate int payment plan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 311; body declaration candidate line(s): 3445

**Signature**

```sql
procedure recalculate_int_payment_plan(p_doc_no               in varchar2,
                                         p_acc_type             in varchar2,
                                         p_main_amount          in number,
                                         p_INT_RATIO            in number,
                                         p_int_calc_type        in varchar2,
                                         p_schedule_update_type in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_new_acc` — FUNCTION

**Purpose:** Public function related to get new acc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 318; body declaration candidate line(s): 2520

**Signature**

```sql
--kredi_api.open_new_acc +
  function get_new_acc(p_branch_no       in number,
                       p_customer_no     in number,
                       p_balance_acc     in varchar2,
                       p_detail_code     in varchar2,
                       p_ccy_id          in number,
                       p_main_acc        in number default null,
                       p_cr_int_rate     in number default null,
                       p_dr_int_rate     in number default null,
                       p_com_int_rate    in number default null,
                       p_product_code    in number default null,
                       p_period_id       in number default null,
                       p_acc_description in varchar2,
                       p_memorandum_id   in varchar2 default null,
                       p_loan_doc_no     in varchar2,
                       p_loan_acc_type   in varchar2,
                       p_tx_fid          in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_plan_control` — PROCEDURE

**Purpose:** Public procedure related to do plan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 336; body declaration candidate line(s): 3506

**Signature**

```sql
-- kredi_api.plan_control +
  procedure do_plan_control(p_document_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_status_control` — PROCEDURE

**Purpose:** Public procedure related to do loan status control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 338; body declaration candidate line(s): 3515

**Signature**

```sql
-- kredi_api.loan_status_control +
  procedure do_loan_status_control(p_branch_no   in number,
                                   p_customer_no in number,
                                   p_loan_acc    in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_loan_history` — PROCEDURE

**Purpose:** Writes a loan-operation history record for a transaction.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 343; body declaration candidate line(s): 3587

**Signature**

```sql
procedure create_loan_history(p_oper_type VARCHAR2 default null,
                                p_doc_no    VARCHAR2 default null,
                                p_trn_date  DATE default glbl.getsysdate,
                                p_tx_fid    NUMBER,
                                p_trn_type  varchar2,
                                p_add_info  add_info_tab default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_collateral_out` — PROCEDURE

**Purpose:** Public procedure related to do loan collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 350; body declaration candidate line(s): 3942

**Signature**

```sql
--krd_eod.loan_collateral_out +
  procedure do_loan_collateral_out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_acc_type_by_status` — FUNCTION

**Purpose:** Public function related to get acc type by status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 353; body declaration candidate line(s): 4211

**Signature**

```sql
function get_acc_type_by_status(p_acc_type         varchar2,
                                  p_to_loan_status   varchar2,
                                  p_from_loan_status varchar2 default 'NORM')
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `generate_allocated_payment_list` — PROCEDURE

**Purpose:** Computes a payment allocation list for a loan operation.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 358; body declaration candidate line(s): 4239

**Signature**

```sql
procedure generate_allocated_payment_list(p_doc_no                in varchar2,
                                            p_oper_type             in varchar2,
                                            p_pym_amount            in number,
                                            p_has_schedule_upd_type out varchar2,
                                            p_payment_list          out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_payment_details` — PROCEDURE

**Purpose:** Public procedure related to add payment details. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 364; body declaration candidate line(s): 4389

**Signature**

```sql
procedure add_payment_details(p_doc_no                in varchar2,
                                p_has_schedule_upd_type out varchar2,
                                p_payment_list          in out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_delete_operation` — PROCEDURE

**Purpose:** Public procedure related to do delete operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 368; body declaration candidate line(s): 4483

**Signature**

```sql
procedure do_delete_operation(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Auto_Payment` — PROCEDURE

**Purpose:** Executes automatic loan payment processing in EOD/SOD context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 370; body declaration candidate line(s): 4540

**Signature**

```sql
/** Makes automatic loan payments at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S                           
  */
  Procedure do_Auto_Payment(p_min_id     number default null,
                            p_max_id     number default null,
                            p_doc_no     in varchar2 default null,
                            p_eod_sod    in varchar2 default 'E',
                            p_test_param in number default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation` — PROCEDURE

**Purpose:** Performs batch interest calculation with optional branch range, loan document and EOD/SOD arguments.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 382; body declaration candidate line(s): 5135

**Signature**

```sql
/** Makes automatic loan int calculation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S 
      p_date - operation date                            
  */
  
  procedure do_int_calculation(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation_ex` — PROCEDURE

**Purpose:** Public procedure related to do int calculation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 396; body declaration candidate line(s): 5768

**Signature**

```sql
procedure do_int_calculation_ex(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_overdue_transit_operation` — PROCEDURE

**Purpose:** Public procedure related to do overdue transit operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 402; body declaration candidate line(s): 4832

**Signature**

```sql
/** Makes automatic loan overdue operation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_branch_id - loan branch id  
      p_customer_no - unique customer number 
      p_loan_acc - loan account sub 
      p_date - operation date                            
  */

  Procedure do_overdue_transit_operation(p_min_id number default null,
                                         p_max_id number default null,
                                         p_doc_no in varchar2 default null,
                                         p_date   in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_commission_recognition` — PROCEDURE

**Purpose:** Public procedure related to do commission recognition. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 416; body declaration candidate line(s): 6338

**Signature**

```sql
Procedure do_commission_recognition(Pdate In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_guarantee_out` — PROCEDURE

**Purpose:** Public procedure related to do guarantee out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 418; body declaration candidate line(s): 6236

**Signature**

```sql
Procedure do_guarantee_out(p_branch_id   In Number Default Null,
                             p_customer_no In Number Default Null,
                             p_loan_acc    In Number Default Null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Close_With_Collateral_Out` — PROCEDURE

**Purpose:** Public procedure related to do loan close with collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 422; body declaration candidate line(s): 6594

**Signature**

```sql
procedure do_Loan_Close_With_Collateral_Out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_non_cash_loan_close` — PROCEDURE

**Purpose:** Public procedure related to do non cash loan close. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 424; body declaration candidate line(s): 6756

**Signature**

```sql
Procedure do_non_cash_loan_close(p_doc_no in varchar2,
                                   p_Date   In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_control` — PROCEDURE

**Purpose:** Public procedure related to do journal control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 427; body declaration candidate line(s): 6861

**Signature**

```sql
-- new
  procedure do_journal_control(p_branch_id   IN Number,
                               p_customer_no IN Number,
                               p_account_sub IN Number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 431; body declaration candidate line(s): 7118

**Signature**

```sql
-- new
  /*procedure over_to_norm(p_min_id  number default null,
                              p_max_id  number default null,
                              p_doc_no  in varchar2 default null);
  */
  --kredi_api.Odeme_Plani_Duzenle
  Procedure do_schedule_allignment(p_doc_no         In Varchar2,
                                   p_payment_amount In Number,
                                   p_acc_type       In Varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_com_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do com schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 441; body declaration candidate line(s): 7190

**Signature**

```sql
-- kredi_api.Kom_Odeme_Plani_Duzenle
  Procedure do_com_schedule_allignment(p_doc_no      In Varchar2,
                                       p_option_code In Varchar2,
                                       p_amount      In Number,
                                       p_plan_type   In Varchar2,
                                       p_mig_status  In Number Default 0);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Delay_Int_Rate_Upd` — PROCEDURE

**Purpose:** Public procedure related to do loan delay int rate upd. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 448; body declaration candidate line(s): 7310

**Signature**

```sql
-- krd_eod.Loan_Delay_Int_Rate_Upd
  Procedure do_Loan_Delay_Int_Rate_Upd;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `change_account_status` — PROCEDURE

**Purpose:** Public procedure related to change account status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 451; body declaration candidate line(s): 7351

**Signature**

```sql
-- kredi_api.Kredi_Hesap_Kapat , kredi_api.Kredi_Hesap_Ac
  procedure change_account_status(p_doc_no in varchar2,
                                  p_status in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_eod_task` — PROCEDURE

**Purpose:** Public procedure related to stop eod task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 455; body declaration candidate line(s): 7389

**Signature**

```sql
procedure stop_eod_task;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_loan_task` — PROCEDURE

**Purpose:** Public procedure related to stop loan task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 457; body declaration candidate line(s): 7405

**Signature**

```sql
procedure stop_loan_task(p_task_code in varchar2 default null,
                           p_task_type in varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `run_loan_task` — PROCEDURE

**Purpose:** Runs a task identified by its task code and task type.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 460; body declaration candidate line(s): 7442

**Signature**

```sql
/** Parallel execution for loan processes
      @params
      p_task_code  - task_code in loan_tasks_list table                  
  */

  procedure run_loan_task(p_task_code in varchar2, p_task_type in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `calculate_xirr` — FUNCTION

**Purpose:** Public function related to calculate xirr. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 467; body declaration candidate line(s): 7786

**Signature**

```sql
/*procedure norm_to_over(p_min_id  number default null,
  p_max_id  number default null,
  p_doc_no  in varchar2 default null);  */

  function calculate_xirr(p_doc_no  varchar2,
                          p_type    varchar2,
                          p_calc_as varchar2 default 'XIRR') return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_min_flow_ratio` — FUNCTION

**Purpose:** Public function related to get min flow ratio. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 475; body declaration candidate line(s): 8074

**Signature**

```sql
/*  function get_mix_operation_acsess(p_fid            varchar2,
                                      p_oper_type      varchar2,
                                      p_memo_oper_type varchar2) return number;
  
    function get_mix_operation_types(p_fid            varchar2,
                                     p_memo_oper_type varchar2) return varchar2;
  
    procedure validate_mix_memorandum(p_memorandum_id varchar2,
                                      p_oper_type     varchar2,
                                      p_state         varchar2);
  
    procedure update_mix_memorandum(p_memorandum_id varchar2,
                                    p_oper_type     varchar2,
                                    p_tx_fid        number,
                                    p_state         varchar2);
  */

  function get_min_flow_ratio(
    p_doc_no     varchar2,
    p_type       varchar2,
    p_begin_date date default null,
    p_end_date   date default null
  ) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_flow_ratio_info` — FUNCTION

**Purpose:** Public function related to get flow ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 499; body declaration candidate line(s): 8115

**Signature**

```sql
FUNCTION get_flow_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N')
    RETURN LOAN_FLOW_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_stop_ratio_info` — FUNCTION

**Purpose:** Public function related to get stop ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 504; body declaration candidate line(s): 8151

**Signature**

```sql
FUNCTION get_stop_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N',
                               p_info_type varchar2 default 'INT')
    RETURN LOAN_STOP_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days` — FUNCTION

**Purpose:** Public function related to get incorrect days. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 510; body declaration candidate line(s): 8179

**Signature**

```sql
function get_incorrect_days(p_date date) return NUMBER_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days_count` — FUNCTION

**Purpose:** Public function related to get incorrect days count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 513; body declaration candidate line(s): 8218

**Signature**

```sql
function get_incorrect_days_count(p_date date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_schedule_from_memo` — FUNCTION

**Purpose:** Public function related to get schedule from memo. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 515; body declaration candidate line(s): 8225

**Signature**

```sql
function get_schedule_from_memo(p_memorandum_id varchar2,
                                  p_int_ratio     number,
                                  p_int_calc_type varchar2,
                                  p_int_amount    number) return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_standart_schedule` — FUNCTION

**Purpose:** Returns pipelined standard schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 521; body declaration candidate line(s): 8324

**Signature**

```sql
function get_standart_schedule(p_begin_date          date default glbl.getsysdate,
                                 p_main_pymt_date      date,
                                 p_int_pymt_date       date,
                                 p_pymt_day            number default null,
                                 p_end_date            date,
                                 p_offer_amount        number,
                                 p_ovd_main_amount     number default 0,
                                 p_int_calc_type       varchar2,
                                 p_main_grace_period   varchar2 default null,
                                 p_int_grace_period    varchar2 default null,
                                 p_remain_int_amount   number default 0,
                                 p_min_main_pay_amount number default null,
                                 p_calc_int_in_grace   varchar2 default 'Y',
                                 p_work_days           varchar2 default 'Y',
                                 
                                 p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                 p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_annuity_schedule` — FUNCTION

**Purpose:** Returns pipelined annuity schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 542; body declaration candidate line(s): 8697

**Signature**

```sql
function get_annuity_schedule(p_begin_date      date,
                                p_main_pymt_date  date,
                                p_int_pymt_date   date,
                                p_pymt_day        number default null,
                                p_end_date        date,
                                p_offer_amount    number,
                                p_ovd_main_amount number default 0,
                                p_int_calc_type   varchar2,
                                
                                p_main_grace_period varchar2 default null,
                                p_int_grace_period  varchar2 default null,
                                
                                p_annuity_amount     number default null,
                                p_max_annuity_amount number default null,
                                p_remain_int_amount  number default 0,
                                
                                p_work_days         varchar2 default 'Y',
                                p_own_annuity       varchar2 default 'N',
                                p_calc_int_in_grace varchar2 default 'Y',
                                p_is_mortgage       varchar2 default 'N',
                                
                                p_max_iteration number default null,
                                
                                p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_created_schedule` — PROCEDURE

**Purpose:** Public procedure related to get created schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 570; body declaration candidate line(s): 9306

**Signature**

```sql
Procedure get_created_schedule(p_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_schedule` — PROCEDURE

**Purpose:** Builds a payment schedule using the supplied dates, amounts, interest and schedule options.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 572; body declaration candidate line(s): 9392

**Signature**

```sql
-- new
  procedure create_schedule(p_schedule_no         number,
                            p_coll_name           varchar2 default null,
                            p_fk_id               number default null,
                            p_doc_no              varchar2 default 'XXX',
                            p_memorandum_id       varchar2 default null,
                            p_customer_no         number default null,
                            p_tx_fid              number default null,
                            p_begin_date          date default glbl.getsysdate,
                            p_main_pymt_date      date,
                            p_int_pymt_date       date,
                            p_pymt_day            number default null,
                            p_end_date            date,
                            p_offer_amount        number,
                            p_ovd_main_amount     number default 0,
                            p_int_ratio           number,
                            p_int_calc_type       varchar2,
                            p_annuity_amount      number default null,
                            p_max_annuity_amount  number default null,
                            p_min_main_pay_amount number default null,
                            p_remain_int_amount   number default 0,
                            p_main_grace_period   varchar2 default null,
                            p_int_grace_period    varchar2 default null,
                            p_main_pymt_period    number default 1,
                            p_int_pymt_period     number default 1,
                            p_product_code        number default null,
                            p_same_annuity        varchar2 default 'N',
                            p_calc_int_in_grace   varchar2 default 'Y',
                            p_return_type         varchar2 default 'NO_ZERO',
                            p_loan_flow_rate_tab  LOAN_FLOW_RATE_TAB default null,
                            p_loan_stop_rate_tab  LOAN_STOP_RATE_TAB default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 604; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 607; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate,
                            p_min_rowid rowid,
                            p_max_rowid rowid);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

## Utilities & Configuration

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 71; body declaration candidate line(s): 70, 736

**Signature**

```sql
-- *

  procedure get_pen_info_for_calc(p_date                   in date default glbl.getsysdate,
                                  p_doc_no                 in varchar2,
                                  p_acc_type               in varchar2,
                                  p_pen_calc_grace_days    in number,
                                  p_ovd_amount             out number,
                                  p_calculated_pen_day_cnt out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates` — FUNCTION

**Purpose:** Builds an interest calculation date collection based on EOD/SOD scheduling and the last calculation access date.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 80; body declaration candidate line(s): 259

**Signature**

```sql
function get_interest_calc_dates(p_last_calc_access_date in date,
                                   p_eod_sod               in varchar2,
                                   p_int_calc_at           in varchar2)
    return loan_api.g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_dates_ex` — FUNCTION

**Purpose:** Public function related to get interest calc dates ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 85; body declaration candidate line(s): 323

**Signature**

```sql
function get_interest_calc_dates_ex(p_date        in date,
                                      p_eod_sod     in varchar2,
                                      p_int_calc_at in varchar2)
    return g_date_tab_type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info` — PROCEDURE

**Purpose:** Determines interest calculation day count and year-day basis from interest-calculation configuration.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 90; body declaration candidate line(s): 104

**Signature**

```sql
procedure get_interest_calc_info(p_last_calc_date       in date,
                                   p_pymt_day             in number,
                                   p_trn_date             in date,
                                   p_int_calc_type        in varchar2,
                                   p_rate_type            in varchar2,
                                   p_int_rate_periodicity in varchar2,
                                   p_calc_day_count       out number,
                                   p_year_day_count       out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_interest_calc_info_ex` — PROCEDURE

**Purpose:** Public procedure related to get interest calc info ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 101; body declaration candidate line(s): 183

**Signature**

```sql
procedure get_interest_calc_info_ex(p_last_calc_date in date,
                                   p_pymt_day       in number,
                                   p_trn_date       in date,
                                   p_int_calc_type  in varchar2,
                                   p_calc_day_count out number,
                                   p_year_day_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `clear_addtional_data` — PROCEDURE

**Purpose:** Public procedure related to clear addtional data. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 109; body declaration candidate line(s): 378

**Signature**

```sql
procedure clear_addtional_data(p_state varchar2 default 'CLEAR');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_group` — PROCEDURE

**Purpose:** Public procedure related to add additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 111; body declaration candidate line(s): 404

**Signature**

```sql
procedure add_additional_group(p_tag_name varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_group` — PROCEDURE

**Purpose:** Public procedure related to end additional group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 113; body declaration candidate line(s): 410

**Signature**

```sql
procedure end_additional_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `end_additional_main_group` — PROCEDURE

**Purpose:** Public procedure related to end additional main group. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 114; body declaration candidate line(s): 398

**Signature**

```sql
procedure end_additional_main_group;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 115; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_additional_info` — PROCEDURE

**Purpose:** Public procedure related to add additional info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 117; body declaration candidate line(s): 416, 428

**Signature**

```sql
procedure add_additional_info(p_tag_name varchar2, p_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 118; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value varchar2,
                              p_new_value varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_column_update` — PROCEDURE

**Purpose:** Adds a mapped column-level update to the pending change-history context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 122; body declaration candidate line(s): 434, 471

**Signature**

```sql
procedure add_column_update(p_tag_name  varchar2,
                              p_old_value date,
                              p_new_value date);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `finalize_addtional_process` — PROCEDURE

**Purpose:** Finalizes accumulated additional information and executes mapped updates for the supplied identifiers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 125; body declaration candidate line(s): 480

**Signature**

```sql
procedure finalize_addtional_process(p_doc_no   varchar2,
                                       p_offer_id varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `reverse_update` — PROCEDURE

**Purpose:** Reads prior history additional information and attempts to restore recorded old values.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 128; body declaration candidate line(s): 591

**Signature**

```sql
procedure reverse_update(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_loan_amount` — FUNCTION

**Purpose:** Returns a loan amount using the TOTAL, DEBT, or DUE calculation mode and related account and schedule data.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 130; body declaration candidate line(s): 643

**Signature**

```sql
function get_loan_amount(p_doc_no      in varchar2,
                           p_amount_type in varchar2,
                           p_date        in date default glbl.getsysdate,
                           p_oper_type   in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_overdue_min_amount` — FUNCTION

**Purpose:** Public function related to get overdue min amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 136; body declaration candidate line(s): 719

**Signature**

```sql
function get_overdue_min_amount(p_product_code in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_pen_info_for_calc` — PROCEDURE

**Purpose:** Reads overdue amounts and penalty calculation day count from the payment plan; overloaded variants differ in inputs.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 137; body declaration candidate line(s): 70, 736

**Signature**

```sql
procedure get_pen_info_for_calc(p_date                in date default glbl.getsysdate,
                                  p_doc_no              in varchar2,
                                  p_pen_calc_grace_days in number,
                                  p_PEN_INT_RATIO       in number,
                                  p_ovd_amount_for_pen  out number,
                                  p_pen_calc_days_count out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_trn_caller_id` — FUNCTION

**Purpose:** Public function related to get trn caller id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 144; body declaration candidate line(s): 772

**Signature**

```sql
function get_trn_caller_id(p_oper_type in varchar2) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_voucher_data_from_query` — FUNCTION

**Purpose:** Executes a supplied SQL query with DBMS_SQL and maps returned column values for vouchers.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 146; body declaration candidate line(s): 789

**Signature**

```sql
function get_voucher_data_from_query(p_query       in varchar2,
                                       p_result_type in varchar2)
    return g_col_value_tab_map;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_formatted_grace_from_list` — FUNCTION

**Purpose:** Public function related to get formatted grace from list. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 150; body declaration candidate line(s): 912

**Signature**

```sql
function get_formatted_grace_from_list(p_period_list in varchar2)
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_grace_info` — FUNCTION

**Purpose:** Public function related to get grace info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 153; body declaration candidate line(s): 952

**Signature**

```sql
function get_grace_info(p_Doc_No          In Varchar2,
                          p_period_end_date in date,
                          p_acc_type        In Varchar2 default 'A',
                          p_info_type       in varchar2) Return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_basis_year_days_cnt` — FUNCTION

**Purpose:** Public function related to get basis year days cnt. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 158; body declaration candidate line(s): 998

**Signature**

```sql
function get_basis_year_days_cnt(p_int_calc_type in varchar2,
                                   p_date          in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_value` — FUNCTION

**Purpose:** Public function related to get gl value. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 161; body declaration candidate line(s): 1026

**Signature**

```sql
function get_gl_value(p_parameter_name in varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 163; body declaration candidate line(s): 1043

**Signature**

```sql
procedure loan_int_diff_operation(p_trn_date        in date,
                                    p_oper_type       in varchar2,
                                    p_trn_type        in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `loan_int_diff_operation_ex` — PROCEDURE

**Purpose:** Public procedure related to loan int diff operation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 177; body declaration candidate line(s): 1197

**Signature**

```sql
procedure loan_int_diff_operation_ex(p_oper_type       in varchar2,
                                    p_doc_no          in varchar2,
                                    p_acc_type        in varchar2,
                                    p_source_acc_type in varchar2,
                                    p_tx_fid          number,
                                    p_original_amount in number,
                                    p_eod_sod         in varchar2,
                                    p_payment_date    in date,
                                    p_plan_int_amount in number,
                                    p_int_amount      in number,
                                    p_calc_amount     out number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_active_passive` — FUNCTION

**Purpose:** Public function related to get gl acc active passive. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 189; body declaration candidate line(s): 1345

**Signature**

```sql
function get_gl_acc_active_passive(p_acc_no in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_gl_acc_from_matrix` — FUNCTION

**Purpose:** Public function related to get gl acc from matrix. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 191; body declaration candidate line(s): 1367

**Signature**

```sql
function get_gl_acc_from_matrix(p_product_code in number default null,
                                  p_cust_type    in number default null,
                                  p_period_id    in number default null,
                                  p_currency_id  in number default null,
                                  p_base_type    in varchar2,
                                  p_loan_doc_no  in varchar2 default null,
                                  p_customer_no  in varchar2 default null,
                                  p_acc_type     in varchar2) return varchar2 result_cache;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `Get_Delay_Int_Rate` — FUNCTION

**Purpose:** Public function related to get delay int rate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 200; body declaration candidate line(s): 1602

**Signature**

```sql
-- krd_eod.Get_Delay_Int_Rate
  Function Get_Delay_Int_Rate(p_Loan_Id    In Varchar2,
                              p_Delay_Type In Varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_commission_schedule` — FUNCTION

**Purpose:** Public function related to get commission schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 203; body declaration candidate line(s): 1628

**Signature**

```sql
-- kredi_api.Get_Krd_Kom_Plan
  Function get_commission_schedule(p_begin_date    In Date,
                                   p_end_date      In Date,
                                   p_amount        In Number,
                                   p_int_calc_type in varchar2)
    Return Krd_Kom_Plan_Tt
    Pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_months_for_loan` — FUNCTION

**Purpose:** Public function related to add months for loan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 211; body declaration candidate line(s): 1744

**Signature**

```sql
function add_months_for_loan(p_date   date,
                               p_months number,
                               p_day    number default null) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_next_Plan_Pym` — FUNCTION

**Purpose:** Public function related to get next plan pym. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 215; body declaration candidate line(s): 1776

**Signature**

```sql
Function get_next_Plan_Pym(p_doc_no   In Varchar2,
                             P_date     In Date,
                             p_acc_type in varchar2) Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_offer_id` — FUNCTION

**Purpose:** Public function related to get offer id. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 219; body declaration candidate line(s): 1809

**Signature**

```sql
Function get_offer_id(p_branch_id In Number Default Glbl.Getsube,
                        P_date      In Date Default Glbl.Getsysdate)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_payment_amount` — FUNCTION

**Purpose:** Public function related to get plan payment amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 223; body declaration candidate line(s): 1832

**Signature**

```sql
-- krd_eod.get_Plan_Pym +
  function get_plan_payment_amount(p_doc_no   in varchar2,
                                   p_date     in date default glbl.getsysdate,
                                   p_acc_type in varchar2 default null)
    return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_ovd_date` — FUNCTION

**Purpose:** Public function related to get ovd date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 229; body declaration candidate line(s): 2734

**Signature**

```sql
Function get_ovd_date(p_doc_no   varchar2,
                        p_acc_type varchar2,
                        p_date     date default glbl.getsysdate) return date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_amount_for_pen_calc` — FUNCTION

**Purpose:** Public function related to get amount for pen calc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 233; body declaration candidate line(s): 1850

**Signature**

```sql
Function get_amount_for_pen_calc(p_doc_no        In Varchar2,
                                   P_date          In Date,
                                   p_for_spec_days in varchar2 default 'N',
                                   p_int_calc_type in varchar2 default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Plan_Month_Count` — FUNCTION

**Purpose:** Public function related to get plan month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 239; body declaration candidate line(s): 1944

**Signature**

```sql
-- kredi_api.get_Plan_Month_Count +
  /*Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ')
    Return Number;*/
  Function get_Plan_Month_Count(p_Start_Date    In Date,
                                p_End_Date      In Date,
                                p_int_calc_type varchar2 default '30/360 AZ',
                                p_work_days     varchar2 default 'Y',
                                p_pymt_day      number default null)
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_paid_month_count` — FUNCTION

**Purpose:** Public function related to get plan paid month count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 251; body declaration candidate line(s): 1987

**Signature**

```sql
-- new
  function get_plan_paid_month_count(p_doc_no in varchar2,
                                     p_term   in number,
                                     p_date   in date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_plan_error` — FUNCTION

**Purpose:** Public function related to get plan error. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 255; body declaration candidate line(s): 2047

**Signature**

```sql
-- kredi_api.get_plan_error +
  Function get_plan_error(p_doc_no varchar2, p_date date default glbl.getsysdate) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Annuity_Amount` — FUNCTION

**Purpose:** Public function related to get annuity amount. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 258; body declaration candidate line(s): 2604

**Signature**

```sql
-- kredi_api.Get_Annuitet_Amount +
  Function get_Annuity_Amount(p_Doc_No      In Varchar2,
                              p_return_type In varchar2 default 'NO_ZERO')
    Return Number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_Pym_Startdate` — FUNCTION

**Purpose:** Public function related to get pym startdate. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 263; body declaration candidate line(s): 2633

**Signature**

```sql
-- kredi_api.Get_Pym_Startdate +
  Function get_Pym_Startdate(p_Doc_No          In Varchar2,
                             p_pymt_date       In Date,
                             p_pymt_day        In Number,
                             p_pymt_period     In Number,
                             p_acc_type        In varchar2,
                             p_loan_end_Date   in date,
                             p_check_is_closed in varchar2 default 'Y')
    Return Date;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_account_feature` — FUNCTION

**Purpose:** Public function related to get account feature. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 273; body declaration candidate line(s): 2799

**Signature**

```sql
function get_account_feature(p_branch_no   number,
                               p_account_no  number,
                               p_account_sub number)
    return cs_account.account_feature%type;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_acc_exists` — FUNCTION

**Purpose:** Public function related to is acc exists. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 278; body declaration candidate line(s): 2818

**Signature**

```sql
function is_acc_exists(p_customer_no   number,
                         p_memorandum_id varchar2 default null,
                         p_doc_no        varchar2,
                         p_acc_type      varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_Payment_Date` — FUNCTION

**Purpose:** Public function related to is payment date. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 283; body declaration candidate line(s): 2845

**Signature**

```sql
-- kredi_api.Is_Payment_Date +
  Function is_Payment_Date(p_Document_No In Varchar2, p_Date Date)
    Return Varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `is_online_offer` — FUNCTION

**Purpose:** Public function related to is online offer. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 287; body declaration candidate line(s): 2858

**Signature**

```sql
function is_online_offer(p_memorandum_id varchar2) return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `table_log_operation` — PROCEDURE

**Purpose:** Public procedure related to table log operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 289; body declaration candidate line(s): 3344

**Signature**

```sql
procedure table_log_operation(p_doc_no     in varchar2,
                                p_table_name in varchar2,
                                p_tx_fid     in number,
                                p_oper_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_entry` — PROCEDURE

**Purpose:** Public procedure related to do journal entry. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 294; body declaration candidate line(s): 2876

**Signature**

```sql
Procedure do_journal_entry(p_entries_list  g_entries_list_tab,
                             p_trn_caller_id in number,
                             p_tx_fid        in out number,
                             p_trn_type      in varchar2,
                             p_is_eod        in varchar2 default 'Y');
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_journal_entries` — PROCEDURE

**Purpose:** Public procedure related to create journal entries. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 300; body declaration candidate line(s): 2954

**Signature**

```sql
procedure create_journal_entries(p_oper_type in varchar2,
                                   p_tx_fid    in number,
                                   p_trn_type  in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_account` — PROCEDURE

**Purpose:** Creates/assigns loan-related accounts based on the requested operation and returns the created account list.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 304; body declaration candidate line(s): 3129

**Signature**

```sql
procedure create_account(p_doc_no        in varchar2,
                           p_memorandum_id in varchar2 default null,
                           p_oper_type     in varchar2,
                           p_acc_type      in varchar2 default null,
                           p_tx_fid        in number,
                           p_created_acc   out g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `recalculate_int_payment_plan` — PROCEDURE

**Purpose:** Public procedure related to recalculate int payment plan. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 311; body declaration candidate line(s): 3445

**Signature**

```sql
procedure recalculate_int_payment_plan(p_doc_no               in varchar2,
                                         p_acc_type             in varchar2,
                                         p_main_amount          in number,
                                         p_INT_RATIO            in number,
                                         p_int_calc_type        in varchar2,
                                         p_schedule_update_type in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_new_acc` — FUNCTION

**Purpose:** Public function related to get new acc. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 318; body declaration candidate line(s): 2520

**Signature**

```sql
--kredi_api.open_new_acc +
  function get_new_acc(p_branch_no       in number,
                       p_customer_no     in number,
                       p_balance_acc     in varchar2,
                       p_detail_code     in varchar2,
                       p_ccy_id          in number,
                       p_main_acc        in number default null,
                       p_cr_int_rate     in number default null,
                       p_dr_int_rate     in number default null,
                       p_com_int_rate    in number default null,
                       p_product_code    in number default null,
                       p_period_id       in number default null,
                       p_acc_description in varchar2,
                       p_memorandum_id   in varchar2 default null,
                       p_loan_doc_no     in varchar2,
                       p_loan_acc_type   in varchar2,
                       p_tx_fid          in number) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_plan_control` — PROCEDURE

**Purpose:** Public procedure related to do plan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 336; body declaration candidate line(s): 3506

**Signature**

```sql
-- kredi_api.plan_control +
  procedure do_plan_control(p_document_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_status_control` — PROCEDURE

**Purpose:** Public procedure related to do loan status control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 338; body declaration candidate line(s): 3515

**Signature**

```sql
-- kredi_api.loan_status_control +
  procedure do_loan_status_control(p_branch_no   in number,
                                   p_customer_no in number,
                                   p_loan_acc    in number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_loan_history` — PROCEDURE

**Purpose:** Writes a loan-operation history record for a transaction.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 343; body declaration candidate line(s): 3587

**Signature**

```sql
procedure create_loan_history(p_oper_type VARCHAR2 default null,
                                p_doc_no    VARCHAR2 default null,
                                p_trn_date  DATE default glbl.getsysdate,
                                p_tx_fid    NUMBER,
                                p_trn_type  varchar2,
                                p_add_info  add_info_tab default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_collateral_out` — PROCEDURE

**Purpose:** Public procedure related to do loan collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 350; body declaration candidate line(s): 3942

**Signature**

```sql
--krd_eod.loan_collateral_out +
  procedure do_loan_collateral_out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_acc_type_by_status` — FUNCTION

**Purpose:** Public function related to get acc type by status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 353; body declaration candidate line(s): 4211

**Signature**

```sql
function get_acc_type_by_status(p_acc_type         varchar2,
                                  p_to_loan_status   varchar2,
                                  p_from_loan_status varchar2 default 'NORM')
    return varchar2;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `generate_allocated_payment_list` — PROCEDURE

**Purpose:** Computes a payment allocation list for a loan operation.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 358; body declaration candidate line(s): 4239

**Signature**

```sql
procedure generate_allocated_payment_list(p_doc_no                in varchar2,
                                            p_oper_type             in varchar2,
                                            p_pym_amount            in number,
                                            p_has_schedule_upd_type out varchar2,
                                            p_payment_list          out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `add_payment_details` — PROCEDURE

**Purpose:** Public procedure related to add payment details. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 364; body declaration candidate line(s): 4389

**Signature**

```sql
procedure add_payment_details(p_doc_no                in varchar2,
                                p_has_schedule_upd_type out varchar2,
                                p_payment_list          in out loan_api.g_loan_accounts_tab);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_delete_operation` — PROCEDURE

**Purpose:** Public procedure related to do delete operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 368; body declaration candidate line(s): 4483

**Signature**

```sql
procedure do_delete_operation(p_tx_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Auto_Payment` — PROCEDURE

**Purpose:** Executes automatic loan payment processing in EOD/SOD context.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 370; body declaration candidate line(s): 4540

**Signature**

```sql
/** Makes automatic loan payments at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S                           
  */
  Procedure do_Auto_Payment(p_min_id     number default null,
                            p_max_id     number default null,
                            p_doc_no     in varchar2 default null,
                            p_eod_sod    in varchar2 default 'E',
                            p_test_param in number default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation` — PROCEDURE

**Purpose:** Performs batch interest calculation with optional branch range, loan document and EOD/SOD arguments.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 382; body declaration candidate line(s): 5135

**Signature**

```sql
/** Makes automatic loan int calculation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_doc_no - unique loan document number
      p_eod_sod  - operation type, may be E or S 
      p_date - operation date                            
  */
  
  procedure do_int_calculation(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_int_calculation_ex` — PROCEDURE

**Purpose:** Public procedure related to do int calculation ex. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 396; body declaration candidate line(s): 5768

**Signature**

```sql
procedure do_int_calculation_ex(p_min_id  number default 0,
                               p_max_id  number default 999999999,
                               p_doc_no  in varchar2 default null,
                               p_eod_sod in varchar2 default 'E',
                               p_date    in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_overdue_transit_operation` — PROCEDURE

**Purpose:** Public procedure related to do overdue transit operation. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 402; body declaration candidate line(s): 4832

**Signature**

```sql
/** Makes automatic loan overdue operation at the EOD & SOD 
      @params
      p_min_id, p_max_id - for parallel execute 
      p_branch_id - loan branch id  
      p_customer_no - unique customer number 
      p_loan_acc - loan account sub 
      p_date - operation date                            
  */

  Procedure do_overdue_transit_operation(p_min_id number default null,
                                         p_max_id number default null,
                                         p_doc_no in varchar2 default null,
                                         p_date   in date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_commission_recognition` — PROCEDURE

**Purpose:** Public procedure related to do commission recognition. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 416; body declaration candidate line(s): 6338

**Signature**

```sql
Procedure do_commission_recognition(Pdate In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_guarantee_out` — PROCEDURE

**Purpose:** Public procedure related to do guarantee out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 418; body declaration candidate line(s): 6236

**Signature**

```sql
Procedure do_guarantee_out(p_branch_id   In Number Default Null,
                             p_customer_no In Number Default Null,
                             p_loan_acc    In Number Default Null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Close_With_Collateral_Out` — PROCEDURE

**Purpose:** Public procedure related to do loan close with collateral out. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 422; body declaration candidate line(s): 6594

**Signature**

```sql
procedure do_Loan_Close_With_Collateral_Out(p_doc_no in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_non_cash_loan_close` — PROCEDURE

**Purpose:** Public procedure related to do non cash loan close. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 424; body declaration candidate line(s): 6756

**Signature**

```sql
Procedure do_non_cash_loan_close(p_doc_no in varchar2,
                                   p_Date   In Date Default Glbl.Getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_journal_control` — PROCEDURE

**Purpose:** Public procedure related to do journal control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 427; body declaration candidate line(s): 6861

**Signature**

```sql
-- new
  procedure do_journal_control(p_branch_id   IN Number,
                               p_customer_no IN Number,
                               p_account_sub IN Number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 431; body declaration candidate line(s): 7118

**Signature**

```sql
-- new
  /*procedure over_to_norm(p_min_id  number default null,
                              p_max_id  number default null,
                              p_doc_no  in varchar2 default null);
  */
  --kredi_api.Odeme_Plani_Duzenle
  Procedure do_schedule_allignment(p_doc_no         In Varchar2,
                                   p_payment_amount In Number,
                                   p_acc_type       In Varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_com_schedule_allignment` — PROCEDURE

**Purpose:** Public procedure related to do com schedule allignment. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 441; body declaration candidate line(s): 7190

**Signature**

```sql
-- kredi_api.Kom_Odeme_Plani_Duzenle
  Procedure do_com_schedule_allignment(p_doc_no      In Varchar2,
                                       p_option_code In Varchar2,
                                       p_amount      In Number,
                                       p_plan_type   In Varchar2,
                                       p_mig_status  In Number Default 0);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_Loan_Delay_Int_Rate_Upd` — PROCEDURE

**Purpose:** Public procedure related to do loan delay int rate upd. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 448; body declaration candidate line(s): 7310

**Signature**

```sql
-- krd_eod.Loan_Delay_Int_Rate_Upd
  Procedure do_Loan_Delay_Int_Rate_Upd;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `change_account_status` — PROCEDURE

**Purpose:** Public procedure related to change account status. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 451; body declaration candidate line(s): 7351

**Signature**

```sql
-- kredi_api.Kredi_Hesap_Kapat , kredi_api.Kredi_Hesap_Ac
  procedure change_account_status(p_doc_no in varchar2,
                                  p_status in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_eod_task` — PROCEDURE

**Purpose:** Public procedure related to stop eod task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 455; body declaration candidate line(s): 7389

**Signature**

```sql
procedure stop_eod_task;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `stop_loan_task` — PROCEDURE

**Purpose:** Public procedure related to stop loan task. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 457; body declaration candidate line(s): 7405

**Signature**

```sql
procedure stop_loan_task(p_task_code in varchar2 default null,
                           p_task_type in varchar2 default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `run_loan_task` — PROCEDURE

**Purpose:** Runs a task identified by its task code and task type.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 460; body declaration candidate line(s): 7442

**Signature**

```sql
/** Parallel execution for loan processes
      @params
      p_task_code  - task_code in loan_tasks_list table                  
  */

  procedure run_loan_task(p_task_code in varchar2, p_task_type in varchar2);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `calculate_xirr` — FUNCTION

**Purpose:** Public function related to calculate xirr. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 467; body declaration candidate line(s): 7786

**Signature**

```sql
/*procedure norm_to_over(p_min_id  number default null,
  p_max_id  number default null,
  p_doc_no  in varchar2 default null);  */

  function calculate_xirr(p_doc_no  varchar2,
                          p_type    varchar2,
                          p_calc_as varchar2 default 'XIRR') return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_min_flow_ratio` — FUNCTION

**Purpose:** Public function related to get min flow ratio. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 475; body declaration candidate line(s): 8074

**Signature**

```sql
/*  function get_mix_operation_acsess(p_fid            varchar2,
                                      p_oper_type      varchar2,
                                      p_memo_oper_type varchar2) return number;
  
    function get_mix_operation_types(p_fid            varchar2,
                                     p_memo_oper_type varchar2) return varchar2;
  
    procedure validate_mix_memorandum(p_memorandum_id varchar2,
                                      p_oper_type     varchar2,
                                      p_state         varchar2);
  
    procedure update_mix_memorandum(p_memorandum_id varchar2,
                                    p_oper_type     varchar2,
                                    p_tx_fid        number,
                                    p_state         varchar2);
  */

  function get_min_flow_ratio(
    p_doc_no     varchar2,
    p_type       varchar2,
    p_begin_date date default null,
    p_end_date   date default null
  ) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_flow_ratio_info` — FUNCTION

**Purpose:** Public function related to get flow ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 499; body declaration candidate line(s): 8115

**Signature**

```sql
FUNCTION get_flow_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N')
    RETURN LOAN_FLOW_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_stop_ratio_info` — FUNCTION

**Purpose:** Public function related to get stop ratio info. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 504; body declaration candidate line(s): 8151

**Signature**

```sql
FUNCTION get_stop_ratio_info(p_doc_no    VARCHAR2,
                               p_date      DATE DEFAULT glbl.getsysdate,
                               p_full_info varchar2 default 'N',
                               p_info_type varchar2 default 'INT')
    RETURN LOAN_STOP_RATE_TAB;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days` — FUNCTION

**Purpose:** Public function related to get incorrect days. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 510; body declaration candidate line(s): 8179

**Signature**

```sql
function get_incorrect_days(p_date date) return NUMBER_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_incorrect_days_count` — FUNCTION

**Purpose:** Public function related to get incorrect days count. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 513; body declaration candidate line(s): 8218

**Signature**

```sql
function get_incorrect_days_count(p_date date) return number;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_schedule_from_memo` — FUNCTION

**Purpose:** Public function related to get schedule from memo. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 515; body declaration candidate line(s): 8225

**Signature**

```sql
function get_schedule_from_memo(p_memorandum_id varchar2,
                                  p_int_ratio     number,
                                  p_int_calc_type varchar2,
                                  p_int_amount    number) return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_standart_schedule` — FUNCTION

**Purpose:** Returns pipelined standard schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 521; body declaration candidate line(s): 8324

**Signature**

```sql
function get_standart_schedule(p_begin_date          date default glbl.getsysdate,
                                 p_main_pymt_date      date,
                                 p_int_pymt_date       date,
                                 p_pymt_day            number default null,
                                 p_end_date            date,
                                 p_offer_amount        number,
                                 p_ovd_main_amount     number default 0,
                                 p_int_calc_type       varchar2,
                                 p_main_grace_period   varchar2 default null,
                                 p_int_grace_period    varchar2 default null,
                                 p_remain_int_amount   number default 0,
                                 p_min_main_pay_amount number default null,
                                 p_calc_int_in_grace   varchar2 default 'Y',
                                 p_work_days           varchar2 default 'Y',
                                 
                                 p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                 p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_annuity_schedule` — FUNCTION

**Purpose:** Returns pipelined annuity schedule rows.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 542; body declaration candidate line(s): 8697

**Signature**

```sql
function get_annuity_schedule(p_begin_date      date,
                                p_main_pymt_date  date,
                                p_int_pymt_date   date,
                                p_pymt_day        number default null,
                                p_end_date        date,
                                p_offer_amount    number,
                                p_ovd_main_amount number default 0,
                                p_int_calc_type   varchar2,
                                
                                p_main_grace_period varchar2 default null,
                                p_int_grace_period  varchar2 default null,
                                
                                p_annuity_amount     number default null,
                                p_max_annuity_amount number default null,
                                p_remain_int_amount  number default 0,
                                
                                p_work_days         varchar2 default 'Y',
                                p_own_annuity       varchar2 default 'N',
                                p_calc_int_in_grace varchar2 default 'Y',
                                p_is_mortgage       varchar2 default 'N',
                                
                                p_max_iteration number default null,
                                
                                p_loan_flow_rate_tab LOAN_FLOW_RATE_TAB default null,
                                p_loan_stop_rate_tab LOAN_STOP_RATE_TAB default null)
    return SCHEDULE_TT
    pipelined;
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `get_created_schedule` — PROCEDURE

**Purpose:** Public procedure related to get created schedule. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 570; body declaration candidate line(s): 9306

**Signature**

```sql
Procedure get_created_schedule(p_fid number);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `create_schedule` — PROCEDURE

**Purpose:** Builds a payment schedule using the supplied dates, amounts, interest and schedule options.

**Description confidence:** Body-reviewed summary.

**Source:** specification line 572; body declaration candidate line(s): 9392

**Signature**

```sql
-- new
  procedure create_schedule(p_schedule_no         number,
                            p_coll_name           varchar2 default null,
                            p_fk_id               number default null,
                            p_doc_no              varchar2 default 'XXX',
                            p_memorandum_id       varchar2 default null,
                            p_customer_no         number default null,
                            p_tx_fid              number default null,
                            p_begin_date          date default glbl.getsysdate,
                            p_main_pymt_date      date,
                            p_int_pymt_date       date,
                            p_pymt_day            number default null,
                            p_end_date            date,
                            p_offer_amount        number,
                            p_ovd_main_amount     number default 0,
                            p_int_ratio           number,
                            p_int_calc_type       varchar2,
                            p_annuity_amount      number default null,
                            p_max_annuity_amount  number default null,
                            p_min_main_pay_amount number default null,
                            p_remain_int_amount   number default 0,
                            p_main_grace_period   varchar2 default null,
                            p_int_grace_period    varchar2 default null,
                            p_main_pymt_period    number default 1,
                            p_int_pymt_period     number default 1,
                            p_product_code        number default null,
                            p_same_annuity        varchar2 default 'N',
                            p_calc_int_in_grace   varchar2 default 'Y',
                            p_return_type         varchar2 default 'NO_ZERO',
                            p_loan_flow_rate_tab  LOAN_FLOW_RATE_TAB default null,
                            p_loan_stop_rate_tab  LOAN_STOP_RATE_TAB default null);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 604; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---

### `do_loan_control` — PROCEDURE

**Purpose:** Public procedure related to do loan control. Verify precise behavior against implementation before external publication.

**Description confidence:** Name-based description — review required.

**Source:** specification line 607; body declaration candidate line(s): 9907, 9929

**Signature**

```sql
procedure do_loan_control(p_oper_type varchar2 default null,
                            p_date      date default glbl.getsysdate,
                            p_min_rowid rowid,
                            p_max_rowid rowid);
```

**Inputs / outputs:** See the exact signature above. Validation, accepted enum values, transactional side effects and exceptions require implementation review unless covered in the workflow or review notes.

---
