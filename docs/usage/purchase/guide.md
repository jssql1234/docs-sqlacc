---
sidebar_position: 1
title: Guide
description: A guideline for Purchase Data Entry
slug: /usage/purchase/guide
tags: ["SQL Account", "Usage", "Purchase", "Guide"]
---

## Purchase Workflow

Example of the purchase process workflow aligned with the SQL Account flow:

![sales-process-workflow](../../../static/img/usage/purchase/guide/sales-process-workflow.png)

## Purchase Request

A Purchase Request is an internal document used within a company to request products or services between departments.

For example, if you need to purchase office supplies, you must submit a Purchase Request to the purchasing department.

![purchase-request](../../../static/img/usage/purchase/guide/purchase-request.png)

![purchase-request-details](../../../static/img/usage/purchase/guide/purchase-request-details.png)

1. Go to **Purchase > Purchase Request > New**.

2. Select the **Supplier Code**.

3. Insert the **Item Code** and details (e.g., **Qty**, **Unit Cost**).

4. Enter a description to explain the **Purchase Request**.

   ![purchase-request-data-entry](../../../static/img/usage/purchase/guide/purchase-request-data-entry.png)

5. Click **Save** once you are done. Below is an example of the created entry:

   ![purchase-request-example-entry](../../../static/img/usage/purchase/guide/purchase-request-example-entry.png)

## Purchase Order

A Purchase Order is a document issued by the purchasing department when placing an order with a supplier.

It contains details such as quantity and unit price for the items being purchased.

![purchase-order](../../../static/img/usage/purchase/guide/purchase-order.png)

![purchase-order-details](../../../static/img/usage/purchase/guide/purchase-order-details.png)

1. Go to **Purchase > Purchase Order > New**.

2. Select the **Supplier Code**.

3. Insert the items:

   1. Enter the **Item Code** and details (e.g., **Qty**, **Unit Cost**).

      :::info
      You can navigate the search columns using the **TAB** key on your keyboard. This applies to all dropdown tables.
      :::

   2. Click the **Show/Hide/Move Column** icon to customize your column layout.

   3. To enter a discount amount, enable the **Discount** field using the method in step 3b. You can enter multiple levels of discounts as shown in the image below.

4. Enter a description for your **Purchase Order**.

   ![purchase-order-data-entry](../../../static/img/usage/purchase/guide/purchase-order-data-entry.png)

5. Click **Save** once you are done. Below is an example of the created entry:

   ![purchase-order-example-entry](../../../static/img/usage/purchase/guide/purchase-order-example-entry.png)

### Project

There are two types of projects to note:

1. **Document Project**: To set a project for the entire document, go to the **MORE** section on the **left sidebar**.

2. **Detail Project**: To set a project for individual items, add the **Project** column using the **Field Chooser**.

   ![detail-project](../../../static/img/usage/purchase/guide/detail-project.png)

### Attachment

Use this feature to attach external PDF, Excel, Word documents, or image files.

![attachment](../../../static/img/usage/purchase/guide/attachment.png)

1. Click **Attachment** on the left sidebar.

2. Click the small black arrow next to the **Link** icon.

3. Select **Attach files to Local Drive** and choose the file from your computer.

### Note

1. Click the **Note** section on the **left sidebar**.

2. **Right-click** inside the section to open the **Rich Text Editor**.

3. Enter your notes as needed. See the example below.

4. Click the **X** button to save and exit the editor.

5. A **Save changes?** prompt will appear. Click **Yes** to save.

![note](../../../static/img/usage/purchase/guide/note.png)

### How to Preview a Report

To preview a report, click the **Preview** button and select your desired format.

![select-report](../../../static/img/usage/purchase/guide/select-report.png)

### How to Send a Report via WhatsApp

![send-report-via-whatsapp](../../../static/img/usage/purchase/guide/send-report-via-whatsapp.png)

A QR code will appear on the screen. Scan it using the **WhatsApp Web** function in your WhatsApp mobile app.

## Goods Received

A Goods Received Note (GRN) is issued after receiving a delivery as proof of receipt.

![goods-received](../../../static/img/usage/purchase/guide/goods-received.png)

![goods-received-details](../../../static/img/usage/purchase/guide/goods-received-details.png)

1. Go to **Purchase > Goods Received > New**.

2. Select the **Supplier Code**.

3. Enter the **Item Code** and details (e.g., **Qty**, **Unit Cost**).

4. Enter a description for the **Goods Received** note.

   ![goods-received-data-entry](../../../static/img/usage/purchase/guide/goods-received-data-entry.png)

5. Click **Save** once you are done. Below is an example of the created entry:

![goods-received-example-entry](../../../static/img/usage/purchase/guide/goods-received-example-entry.png)

### Transfer from PO to GRN

1. Go to **Purchase > Goods Received > New**.

2. Select the **Supplier Code**.

3. **Right-click on the G/R Note title** and select **Transfer from Purchase Order**. Select the documents you wish to transfer.

4. **Save** the Goods Received Note.

![goods-received-transfer-from-po](../../../static/img/usage/purchase/guide/goods-received-transfer-from-po.png)

### Notes - Landing Cost

:::info
This is an additional module.
:::

**Landing Cost** handles costs associated with getting goods to the warehouse that are not billed by the same supplier (e.g., freight, insurance, or handling fees). These costs are added to your stock cost. For example, if you buy a product from Supplier A but it is shipped by Transport Company B, you enter the transport charges as a landing cost to increase your product's cost.

![landing-cost-1](../../../static/img/usage/purchase/guide/landing-cost-1.png)

#### How to set up Landing Cost

Follow the steps shown in the image below:

![landing-cost-2](../../../static/img/usage/purchase/guide/landing-cost-2.png)

1. **Landing Cost 1**: Enter your landing cost in this column. (This value is for reference and may not be included in all calculations).
2. **Landing Cost 2**: If you have a different calculation than Landing Cost 1, enter the value here.
3. Click the **+** button to select the cost allocation method.

![cost-allocated-by-subtotal](../../../static/img/usage/purchase/guide/cost-allocated-by-subtotal.png)

##### Formula for Cost Allocated By Subtotal

- **Formula**: `(Item Subtotal / Document Subtotal) * Landing Cost 1`

![formula-subtotal](../../../static/img/usage/purchase/guide/formula-subtotal.png)

:::info
**Example:**

- **Formula**: `(Item Subtotal / Document Subtotal) * Landing Cost 1`
- **Item 1**: `(50.00 / 1949.00) * 200 = 5.13`
- **Item 2**: `(1899.00 / 1949.00) * 200 = 194.87`

:::

![stock-card-check-cost](../../../static/img/usage/purchase/guide/stock-card-check-cost.png)

:::info
**How to calculate Unit Cost (e.g., 5.51):**

- **Formula**: `Product Unit Cost + (Item Landing Cost 1 / Item Qty)`
- **Calculation**: `5 + (5.13 / 10) = 5.51`

:::

##### Formula for Cost Allocated By Qty

- **Formula**: `(Item Qty / Document Qty) * Landing Cost 1`

![cost-allocated-by-quantity](../../../static/img/usage/purchase/guide/cost-allocated-by-quantity.png)

![formula-quantity](../../../static/img/usage/purchase/guide/formula-quantity.png)

:::info
**Example:**

- **Item 1**: `(10 / 11) * 200 = 181.81`
- **Item 2**: `(1 / 11) * 200 = 18.18`

:::

**Stock Card Report Outcome:**

:::info

- **Item ANT**: Unit cost will be **23.18**.
  - `Unit Cost + (Landing Cost 1 / Qty) = 5 + (181.82 / 10) = 23.18`
- **Item LCLIP**: Unit cost will be **1917.18**.
  - `Unit Cost + (Landing Cost 1 / Qty) = 1899 + (18.18 / 1) = 1917.18`

:::

##### Formula for Cost Allocated By Smallest Qty

- **Formula**: `(Item Qty * Rate) / Sum(Qty * Rate) * Landing Cost 1`

![cost-allocated-by-smallest-quantity](../../../static/img/usage/purchase/guide/cost-allocated-by-smallest-quantity.png)

![formula-smallest-quantity](../../../static/img/usage/purchase/guide/formula-smallest-quantity.png)

:::info
**Example:**

- **Item 1**: `(10 * 12) / 121 * 200 = 198.35`
- **Item 2**: `(1 * 1) / 121 * 200 = 1.65`

:::

**Stock Card Report Outcome:**

:::info

- **Item 1 (ANT)**: Unit cost = `[Unit Price + (Item Landing Cost 1 / Item Qty)] / Item Rate`
  - `[30 + (198.35 / 10)] / 12 = 4.15`
- **Item 2 (LCLIP)**: Unit cost = `Unit Price + (Item Landing Cost 1 / Item Qty)`
  - `1899 + 1.65 = 1900.65`

:::

## Purchase Invoice

You can enter a Purchase Invoice after your Purchase Order has been approved and the goods have been received.

![purchase-invoice](../../../static/img/usage/purchase/guide/purchase-invoice.png)

1. Go to **Purchase > Purchase Invoice > New**.

   ![purchase-invoice-data-entry](../../../static/img/usage/purchase/guide/purchase-invoice-data-entry.png)

2. Select the **Supplier Code**.

3. Insert the items:

   1. Enter the **Item Code** and details (e.g., **Qty**, **Unit Cost**).

   :::info
   You can navigate the search columns using the **TAB** key on your keyboard. This applies to all dropdown tables.
   :::

   ![search-supplier-column](../../../static/img/usage/purchase/guide/search-supplier-column.png)

4. Enter a description for the **Purchase Invoice**.

5. Click **Save** once you are done. Below is an example of the created entry:

**Double Entry:**

| Account            | DR (RM) | CR (RM) |
|--------------------|---------|---------|
| Purchase Account   | 500.00  |         |
| Supplier Account   |         | 500.00  |

### Transfer from GRN

1. Go to **Purchase > Purchase Invoice > New**.

2. Select the **Supplier Code**.

3. **Right-click on the Purchase Invoice title** and select **Transfer from Goods Received**. Select the documents you wish to transfer.

4. **Save** the Purchase Invoice.

![purchase-invoice-transfer-from-do](../../../static/img/usage/purchase/guide/purchase-invoice-transfer-from-do.png)

## Cash Purchase

Cash Purchases are used for transactions that are paid for immediately with cash, with no outstanding balance.

![cash-purchase](../../../static/img/usage/purchase/guide/cash-purchase.png)

1. Go to **Purchase > Cash Purchase > New**.

   ![cash-purchase-data-entry](../../../static/img/usage/purchase/guide/cash-purchase-data-entry.png)

2. Select the **Supplier Code**.

3. Insert the items:

   1. Enter the **Item Code** and details (e.g., **Qty**, **Unit Cost**).

   :::info
   You can navigate the search columns using the **TAB** key on your keyboard. This applies to all dropdown tables.
   :::

   ![search-supplier-column-2](../../../static/img/usage/purchase/guide/search-supplier-column-2.png)

4. Enter a description for the **Cash Purchase**.

5. Click **Save** once you are done.

![cash-purchase-example-entry](../../../static/img/usage/purchase/guide/cash-purchase-example-entry.png)

### Transfer From

You can transfer existing Purchase Orders, Goods Received Notes, or Purchase Requests to a Cash Purchase.

**Right-click on the Cash Purchase title** to select the source document.

![cash-purchase-transfer-from](../../../static/img/usage/purchase/guide/cash-purchase-transfer-from.png)

### Payment Details

For Cash Purchases, you can select the payment method and enter the payment amount.

![cash-purchase-payment-paid-details](../../../static/img/usage/purchase/guide/cash-purchase-payment-paid-details.png)

![cash-purchase-payment-paid-payment-by](../../../static/img/usage/purchase/guide/cash-purchase-payment-paid-payment-by.png)

You can also enter the **Cheque No.** and **Bank Charges** if applicable.

Once you **Save** the Cash Purchase, the system automatically creates a Supplier Payment document.

![cash-purchase-generate-pv-number](../../../static/img/usage/purchase/guide/cash-purchase-generate-pv-number.png)

## Extra Goods Received

Extra Goods Received is typically used when invoices are issued before the goods are received.

:::note
This requires the **Invoice > DO** module.
:::

![navigate-extra-goods-received](../../../static/img/usage/purchase/guide/navigate-extra-goods-received.png)

1. Go to **Purchase > Extra Goods Received > New**.

2. Select the **Supplier Code**.

3. Enter the **Item Code** and details (e.g., **Qty**, **Unit Cost**).

4. Enter a description for the **Extra Goods Received** note.

   ![extra-goods-received-data-entry](../../../static/img/usage/purchase/guide/extra-goods-received-data-entry.png)

5. Click **Save** once you are done.

### Transfer from PI to EGR

You can transfer from an existing Purchase Invoice or Cash Purchase.

**Right-click on the Extra Goods Received title** to select the source document.

![extra-goods-received-transfer-from](../../../static/img/usage/purchase/guide/extra-goods-received-transfer-from.png)

## Purchase Debit Note

A Purchase Debit Note is used to increase an expense amount or the amount owed to a supplier.

![purchase-debit-note](../../../static/img/usage/purchase/guide/purchase-debit-note.png)

1. Go to **Purchase > Purchase Debit Note > New**.

2. Select the **Supplier Code**.

3. Enter the **Item Code** and details (e.g., **Qty**, **Unit Cost**).

4. Enter a description for the **Purchase Debit Note**.

   ![purchase-debit-note-data-entry](../../../static/img/usage/purchase/guide/purchase-debit-note-data-entry.png)

5. Click **Save** once you are done. Below is an example of the created entry:

   ![purchase-debit-note-example-entry](../../../static/img/usage/purchase/guide/purchase-debit-note-example-entry.png)

### Transfer from PI

Instead of entering a new document, you can transfer from an existing Purchase Request, Purchase Order, or Goods Received document.

**Right-click on the Purchase Debit Note title** to select the source document.

![purchase-debit-note-transfer-from](../../../static/img/usage/purchase/guide/purchase-debit-note-transfer-from.png)

## Purchase Return

A Purchase Return document is created when you return purchased goods to a supplier.

![purchase-returned](../../../static/img/usage/purchase/guide/purchase-returned.png)

1. Go to **Purchase > Purchase Return > New**.

2. Select the **Supplier Code**.

3. Enter the **Item Code** and details (e.g., **Qty**, **Unit Cost**).

4. Enter a description for the **Purchase Return**.

   ![purchase-returned-data-entry](../../../static/img/usage/purchase/guide/purchase-returned-data-entry.png)

5. Click **Save** once you are done. Below is an example of the created entry:

![purchase-returned-example-entry](../../../static/img/usage/purchase/guide/purchase-returned-example-entry.png)

### Transfer from PI to PRN

Instead of entering a new document, you can transfer from an existing Purchase Invoice or Cash Purchase document.

**Right-click on the Purchase Return title** to select the source document.

![purchase-returned-transfer-from](../../../static/img/usage/purchase/guide/purchase-returned-transfer-from.png)

## Purchase Cancelled Note

A Purchase Cancelled Note is used to remove any outstanding Purchase Orders.

![purchase-cancelled-note](../../../static/img/usage/purchase/guide/purchase-cancelled-note.png)

1. Go to **Purchase > Purchase Cancelled Note > New**.

2. Select the **Supplier Code**.

3. Enter the **Item Code** and details (e.g., **Qty**, **Unit Cost**).

### Transfer from PO to PCN

Instead of entering a new document, you can transfer from an existing Purchase Order.

**Right-click on the Purchase Cancelled Note title** to select the source document.

![purchase-cancelled-note-transfer-from](../../../static/img/usage/purchase/guide/purchase-cancelled-note-transfer-from.png)
