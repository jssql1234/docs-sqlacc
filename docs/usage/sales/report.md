---
sidebar_position: 2
title: Reports
description: Sales Report guideline
slug: /usage/sales/report
tags: ["SQL Account", "Sales", "Sales Report"]
---

## Print Sales Document Listing

1. Go to **Sales** → **Print Sales Document Listing**. Filter the document type you need, such as **Sales Quotation**, **Sales Order**, **Delivery Order**, or **Invoice Listing**.

2. Filter by **Date**. If left unchecked, all periods will be displayed.

3. Filter by **Area** or other criteria (optional).

4. Use the **Group/Sort By** feature to group results and provide summaries for different categories.

5. Click **Apply** to generate the listing. If you change any settings in steps 3 or 4, click **Apply** again to refresh the results.

   ![sales-document-listing](../../../static/img/usage/sales/report/sales-document-listing.png)

### Export Report to Excel

1. **Right-click** on any column header (title bar).

2. Select **Grid Export** → **Export to Excel**.

   ![export-report-into-excel](../../../static/img/usage/sales/report/export-report-into-excel.png)

### Batch Printing Invoices

To print an entire month's invoices in batch (page-by-page format):

1. Go to **Sales** → **Print Sales Document Listing**.

2. Check the **Print Document Style** option.

:::info
Watch the tutorial video here: [Sales Invoicing Batch Print Invoices](https://www.youtube.com/watch?v=MbNMVn0mBiw&feature=youtu.be)
:::

![batch-printing-invoices](../../../static/img/usage/sales/report/batch-printing-invoices.png)

## Print Outstanding Sales Document Listing

This report helps you track transferred documents, such as identifying outstanding items or seeing which Invoice a Delivery Order (DO) was transferred to.

1. Go to **Sales** → **Print Outstanding Sales Document Listing**.

2. Filter the information as needed and click **Apply**.

3. **Criteria Options:**

   - **Print Outstanding Item**: To check items that have not yet been transferred.
   - **Print Fulfilled Item**: To check documents that have been fully transferred and identify the target documents.
   - **Include cancelled documents**: Check this to include cancelled documents in the report.
   - **Outstanding SO & PO**: To check the number of outstanding items from both Sales Orders and Purchase Orders.
   - **Transfer Doc Date Follow Filtered Date**: Check this if you want the transfer document date to align with the filtered date range.

4. Click **Apply**.

   ![outstanding-sales-doc-listing](../../../static/img/usage/sales/report/outstanding-sales-doc-listing.png)

5. To see where a document has been transferred, **Preview** the report.

   ![outstanding-sales-doc-listing-preview](../../../static/img/usage/sales/report/outstanding-sales-doc-listing-preview.png)
