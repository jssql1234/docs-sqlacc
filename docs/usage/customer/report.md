---
sidebar_position: 2
title: Reports
description: All kind of customer reports and it's purpose
slug: /usage/customer/report
tags: ["SQL Account", "Usage", "Customer", "Reports"]
---

## Print Customer Document Listing

The **Print Customer Document Listing** allows you to view all customer transactions, including Invoices, Payments, Credit Notes, Debit Notes, Refunds, and Contras. It is also used for batch printing or emailing documents.

1. Go to **Customer** → **Print Customer Document Listing**.

    ![printCustDocList](../../../static/img/usage/customer/report/print-cust-doc-list.png)

2. Select the **Document Type** you wish to view (e.g., Invoice, Payment).

    ![docListType](../../../static/img/usage/customer/report/doc-list-type.png)

3. Click **Apply**.

    ![docListApply](../../../static/img/usage/customer/report/doc-list-apply.png)

4. Click **Preview** to view the listing report.

    ![docListPreview](../../../static/img/usage/customer/report/doc-list-preview.png)

**Example of Customer Invoice Listing Report:**

![custInvoiceListReport](../../../static/img/usage/customer/report/cust-invoice-list-report.png)

### Print Document Style

- Check the **Print Document Style** box.

    ![tickPrintDocStyle](../../../static/img/usage/customer/report/tick-print-doc-style.png)

| Field Name | Description |
| :--- | :--- |
| **Print Document Style** | Enables bulk printing or batch emailing of the actual documents (not just the list). |
| **Include Cancelled Documents** | Includes documents marked as cancelled in the listing. |

1. Once enabled, you can select the specific **Report Format** for the documents.

    ![custInvoiceReportFormat](../../../static/img/usage/customer/report/cust-invoice-report-format.png)
    ![custInvoiceReportFormat2](../../../static/img/usage/customer/report/cust-invoice-report-format2.png)

### Group/Sort by

You can refine your report by filtering and grouping data.

- **Filters**: Filter by Customer, Agent, Area, Currency, Project, or Company Category.
    ![GrpBy-which](../../../static/img/usage/customer/report/grp-by-which.png)

- **Group/Sort By**: Choose how to organize the data (e.g., by Customer Code).
    ![grp-sortBy](../../../static/img/usage/customer/report/grp-sort-by.png)
    ![grpByCustName](../../../static/img/usage/customer/report/grp-by-cust-name.png)

- **Listing Report**: Select the desired listing format before previewing.
    ![ListingReport](../../../static/img/usage/customer/report/listing-report.png)

## Print Customer Balance Report

This report provides a summary of **outstanding balances for all customers** as of a specific date.

1. Go to **Customer** → **Print Customer Balance Report**.

    ![printCustBalanceReport](../../../static/img/usage/customer/report/print-cust-balance-report.png)

2. Select the **Date** or period for the report.

    ![datePeriod](../../../static/img/usage/customer/report/date-period.png)

3. Apply filters such as **Customer**, **Agent**, or **Area** if needed.

    ![custBalanceFilter](../../../static/img/usage/customer/report/cust-balance-filter.png)
    ![custBalanceApplyFilter](../../../static/img/usage/customer/report/cust-balance-apply-filter.png)

4. Click the **[+]** icon to expand a row and view transaction details for a specific customer.

    ![plusIconToExpand](../../../static/img/usage/customer/report/plus-icon-to-expand.png)

5. Click **Preview** to generate the report.

    ![previewCustBalance](../../../static/img/usage/customer/report/preview-cust-balance.png)

## Print Customer Due Document Listing

The **Customer Due Document Listing** is primarily used to identify overdue amounts and generate **Reminder Letters**.

1. Go to **Customer** → **Print Customer Due Document Listing**.
2. Filter by **Date** and **Document Type** (Invoice, Debit Note, etc.).
3. Select whether to show **Overdue** or **Undue** documents.
4. Click **Apply**.

    ![cust-due-doc-list-apply](../../../static/img/usage/customer/report/cust-due-doc-list-apply.png)

### Generating Reminder Letters

1. In the **Group / Sort by** section, ensure **Customer Code** is checked.
2. Click **Apply**.

    ![grp-sort-by-customer-code](../../../static/img/usage/customer/report/grp-sort-by-customer-code.png)

3. Click **Preview** and select the **Cust Overdue Letter** format.

    ![cust-overdue-letter](../../../static/img/usage/customer/report/cust-overdue-letter.png)
    ![print-overdue-letter](../../../static/img/usage/customer/report/print-overdue-letter.png)

## Customer Analysis By Document

This report provides a high-level analysis of all customer-related documents, showing totals for Invoices, Credit Notes, Payments, and more.

1. Go to **Customer** → **Print Customer Analysis By Document**.
2. Filter by **Document Date** and other optional fields.
3. Click **Apply**.

    ![cust-analysis-by-doc-apply](../../../static/img/usage/customer/report/cust-analysis-by-doc-apply.png)
