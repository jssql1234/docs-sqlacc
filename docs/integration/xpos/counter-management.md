---
sidebar_position: 4
title: Counter Management
description: A guide on counter management in X-Pos Terminal
slug: /integration/xpos/terminal/counter-management
tags: ["SQL Account", "Integration", "X-Pos", "Counter Management"]
---

The **Counter Managament** module allows you to view counter summaries, handle cash flows, close counters, and preview or print closed counter reports

## General Features

### Filter Counter by Date

1. Use the **calendar** on the left panel to navigate between months using the **◀** and **▶** arrows
2. Select a **date** to show counters opened on that day

    ![filter-counter-date](../../../static/img/integration/xpos/counter-management/filter-counter-date.png)

3. Select a counter in the list to view its full **Counter Details** on the right panel

    ![counter-management-1](../../../static/img/integration/xpos/counter-management/counter-management-1.png)
    ![counter-management-2](../../../static/img/integration/xpos/counter-management/counter-management-2.png)
    ![counter-management-3](../../../static/img/integration/xpos/counter-management/counter-management-3.png)

    | Section | Information available |
    | --- | --- |
    | **Counter Information** | Terminal ID, opening time, close time, counter report ID, opened by, closed by, and note |
    | **Sales Summary** | Payment method, amount (RM), and transaction count |
    | **Payment Summary** | Payment method, actual amount (RM), expected amount (RM), and difference (actual − expected) |
    | **Deduction Summary** | Deduction type (return, bill discount, item discount, tax amount) and amount (RM) |
    | **Cash Summary** | Actual cash, cash sales, opening cash, cash in, cash out, total expected cash, and total variance |
    | **Cash Flow Summary** | Time, user, amount (RM), and reason for each cash in/out transaction |
    | **Hold Bill Summary** | ID, time, user, amount (RM), and remark for each held bill |
    | **Void Bill Summary** | ID, time, user, amount (RM), and remark for each voided bill |

### Print Batch Reports

1. Click **Print Batch Reports**

    ![print-batch-report](../../../static/img/integration/xpos/counter-management/print-batch-report.png)

2. Select a **Report Type**:

    | Report Type | Description |
    | ----------- | ------------ |
    | **By Summary** | Consolidates all counters within the date range into a single combined report |
    | **By Counter** | Generates an individual close counter report for each counter within the date range, viewable one by one |

3. Select the **Start Date** and **End Date**
4. Select a **Template** (e.g., ` POS_CLOSECOUNTER_BYDATE `)
5. (Optional) Check **Send Report to Email** to email the reports. This requires an email to be configured first
6. A **preview** of the report is shown on the right

    - For **By Summary**, the preview shows the combined totals across all counters in the range

        ![print-batch-report-by-summary](../../../static/img/integration/xpos/counter-management/print-batch-report-by-summary.png)

    - For **By Counter**, the preview shows each counter's report individually. Use **Previous** and **Next** to navigate between counters, indicated by the page counter (e.g., **1 of 2**)

        ![print-batch-report-by-counter](../../../static/img/integration/xpos/counter-management/print-batch-report-by-counter.png)

7. Click **Print** to generate the report(s), or **Cancel** to discard the selection

### Cash Management

1. Click **Cash Management**

    ![cash-management](../../../static/img/integration/xpos/counter-management/cash-management.png)

2. Select **Cash In** or **Cash Out** using the toggle at the top of the form
3. Enter the **Amount**
4. (Optional) Enter the **Reason**
5. (Optional) Check **Open Cash Drawer** to trigger the physical cash drawer to open
6. (Optional) Check **Print Cash In / Out Receipt** and select a template (e.g., ` POS_CASHINOUT `)
7. Click **Save** to confirm the transaction, or **Cancel** to discard it

    ![cash-in-out](../../../static/img/integration/xpos/counter-management/cash-in-out.png)

8. Once saved, a **success** message is displayed:

    ![cash-in-out-status](../../../static/img/integration/xpos/counter-management/cash-in-out-status.png)

### Close Counter

1. Click **Close Counter**

    ![close-counter](../../../static/img/integration/xpos/counter-management/close-counter.png)

2. Count the amounts received and adjust the **Actual (RM)** amount for each payment method
3. (Optional) Check **Send Report to Email** to email the report. This requires an email to be configured first
4. (Optional) Check **Print Closing Summary Report** and select a template (e.g., ` POS_CLOSECOUNTER_BYID `)
5. Click **Proceed Close Counter** to close the counter, or **Cancel** to discard it

    ![close-counter-summary](../../../static/img/integration/xpos/counter-management/close-counter-summary.png)

6. Once closed, a **Counter Closed** confirmation is shown with the **Counter ID**, **Date**, **Time**, and **Operator**
7. (Optional) Check **Auto Post to SQL Account** post the closed counter to SQL Acc automatically
8. Click **OK** to complete, or **Undo** within the countdown to reopen the counter

    ![close-counter-detail](../../../static/img/integration/xpos/counter-management/close-counter-detail.png)

### Print Close Counter Report

1. Click **Print** icon

    ![print-counter-report](../../../static/img/integration/xpos/counter-management/print-counter-report.png)

2. Select a **Template** (e.g., ` POS_CLOSECOUNTER_BYID `)
3. (Optional) Check **Send Report to Email** to email the report. This requires an email to be configured first
4. Click **Print** to generate the report, or **Cancel** to discard the selection

    ![print-counter-report-summary](../../../static/img/integration/xpos/counter-management/print-counter-report-summary.png)

### PopUp Menu

1. Click **⋯ (three dots)** icon

    ![three-dot](../../../static/img/integration/xpos/counter-management/three-dot.png)

2. Select one of the following actions:

    ![popup-menu](../../../static/img/integration/xpos/counter-management/popup-menu.png)

    | Action | Description |
    | --- | --- |
    | **Undo Closed Counter** | Reopens a closed counter within the **configured timeout window**. It is unavailable after the counter has been **posted to SQL Account** |
    | **View Transaction** | Opens the **Transaction** page and displays the transactions in the selected counter |

### Edit Payment Summary Actual Amount

1. Click **Edit** icon

    ![payment-summary](../../../static/img/integration/xpos/counter-management/payment-summary.png)

2. Adjust the **Actual (RM)** amount for the relevant payment method.
3. Click **Save** to update the actual amounts or **Cancel** to discard the changes.

    ![edit-payment-summary](../../../static/img/integration/xpos/counter-management/edit-payment-summary.png)
