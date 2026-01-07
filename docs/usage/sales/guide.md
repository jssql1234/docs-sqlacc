---
sidebar_position: 1
title: Guide
description: Sales work flow
slug: /usage/sales/guide
tags: ["Sales Management", "Order Processing", "Transactions"]
---

## Sales Workflow

Example of the sales process workflow aligned with the SQL Account flow:

![sales-work-flow](../../../static/img/usage/sales/guide/sales-work-flow.png)

## Sales Quotation

:::info
Watch the tutorial video here: [Sales Quotation](https://www.youtube.com/watch?v=2hKhtpaQfP4)
:::

1. Go to **Sales** → **Quotation** → **New**.

2. Select the **Customer Code**.

3. Insert the requested items and estimate profit & loss using the **Profit Estimator**.

   ![profit-estimator](../../../static/img/usage/sales/guide/profit-estimator.png)

4. Once all details are entered correctly, **Save** the Sales Quotation.

5. **Preview** the report to **print** or **export** it to PDF, Email, RTF (Microsoft Word), Excel, or other formats.

   ![preview-export](../../../static/img/usage/sales/guide/preview-export.png)

### Project

There are two types of projects to note:

1. **Document Project**: To set a project for the entire document, go to the **MORE** section on the **left sidebar**.

2. **Detail Project**: To set a project for individual items, **add the project column using the Field Chooser**.

   ![quotation-project](../../../static/img/usage/sales/guide/quotation-project.png)

### Attachment

Use this feature to attach external PDF, Excel, Word documents, or image files.

1. Click **Attachment** on the left sidebar.

2. Click the **Add** (first) icon.

3. Select the file from your computer to attach.

   ![quotation-attachment](../../../static/img/usage/sales/guide/quotation-attachment.png)

### Note

1. Click the **Note** section on the **left sidebar**.

2. **Right-click** inside the section to open the Rich Text Editor.

3. Enter your notes as needed. See the example below.

4. Click the **X** button (top-right corner) to exit the editor.

5. A **Save changes?** prompt will appear. Click **Yes** to save.

   ![quotation-note](../../../static/img/usage/sales/guide/quotation-note.png)

## Sales Order

:::info
Watch the tutorial video here: [Sales Invoicing Sales Order](https://www.youtube.com/watch?v=klEAjmFT0og&feature=youtu.be)
:::

1. Go to **Sales** → **Sales Order** → **New**.

2. Select the **Customer Code**.

3. **Right-click on the Sales Order title** and select **Transfer from Quotation**. You can transfer the entire quotation or only specific items (requires the **Partial Delivery Module**).

   ![document-transfer](../../../static/img/usage/sales/guide/document-transfer.png)

4. **Save** the Sales Order.

   :::note
   To view outstanding sales orders, go to **Sales** → **Print Outstanding Sales Document Listing** and select **Sales Order**. This applies to other sales documents as well.
   :::

## Delivery Order

1. Go to **Sales** → **Delivery Order** → **New**.

2. Select the **Customer Code**.

3. **Right-click on the D/Order title** and select **Transfer from Sales Order**.

4. **Save** the Delivery Order.

   :::note
   Saving the Delivery Order will automatically deduct the stock.
   :::

## Invoice

### Create New Invoice

:::info
Watch the tutorial video here: [Sales Invoicing Sales Invoice](https://www.youtube.com/watch?v=hQ6bX5pOKRQ&feature=youtu.be)
:::

1. Go to **Sales** → **Invoice** → **New**.

2. Select the **Customer Code**.

3. **Right-click on the Invoice title** and select **Transfer from Delivery Order**.

4. **Save** the Invoice.

### Show Double Entry

:::info
Watch the tutorial video here: [Ctrl + O](https://www.youtube.com/watch?v=FAKSzjEezjo&t=9s)
:::

**There are two methods to view the double entry for a transaction:**

1. After saving the invoice, press **Ctrl + O** on your keyboard to display the double entry result.

   ![show-double-entry-1](../../../static/img/usage/sales/guide/show-double-entry-1.png)

2. After saving the invoice, **right-click on the Invoice title** and select **Show Double Entry**.

   ![show-double-entry-2](../../../static/img/usage/sales/guide/show-double-entry-2.png)

## Cash Sales

1. Go to **Sales** → **Cash Sales** → **New**.

2. Select the **Customer Code**.

3. Insert the items and **Save** the Cash Sales.

4. Upon saving, a **Payment/Change** dialog box will appear.

   ![cash-sales-1](../../../static/img/usage/sales/guide/cash-sales-1.png)

   ![payment-received](../../../static/img/usage/sales/guide/payment-received.png)

## Credit Note

:::info
Watch the tutorial video here: [Sales Invoicing Sales Credit Note](https://www.youtube.com/watch?v=2LrsegwiWJM&feature=youtu.be)
:::

1. Go to **Sales** → **Credit Note** → **New**.

2. Select the **Customer Code**.

3. **Right-click on the Credit Note title** and select **Transfer from Sales Invoice/Cash Sales**. Enter the returned quantity in the **X/F** column.

4. **Save** the Credit Note.

   ![sales-credit-note](../../../static/img/usage/sales/guide/sales-credit-note.png)

## Sales Cancelled Note

The Sales Cancelled Note is used to cancel outstanding Sales Orders.

1. Go to **Sales** → **Sales Cancelled Note** → **New**.

2. **Right-click on the Cancelled Note title** and select **Transfer from Sales Order**. (Note: Items in a Sales Cancelled Note can only be added by transferring from a Sales Order).

   ![sales-cancelled-note-1](../../../static/img/usage/sales/guide/sales-cancelled-note-1.png)

3. You can choose to transfer the Sales Order either in full or partially.

   ![sales-cancelled-note-2](../../../static/img/usage/sales/guide/sales-cancelled-note-2.png)

4. **Save** the Cancelled Note.
