---
sidebar_position: 2
title: Reports
description: Stock Report
slug: /usage/stock/report
tags: ["SQL Account", "Usage", "Inventory", "Stock", "Report"]
---

## Print Stock Document Listing

- The **Print Stock Document Listing** report allows you to view all issued stock adjustment documents.
- This includes Stock Received, Stock Issue, Stock Transfer, and Stock Adjustment listings.

### How to Print Stock Document Listing

1. **Stock** > **Print Stock Document Listing**.

    ![print-stock-document-listing](../../../static/img/usage/stock/stock-report/print-stock-document-listing.png)

2. Select the Document Listing you want to view. Follow the image below.

    ![print-stock-document-listing1](../../../static/img/usage/stock/stock-report/print-stock-document-listing1.png)

3. Click the **Apply** button.

    ![print-stock-document-listing2](../../../static/img/usage/stock/stock-report/print-stock-document-listing2.png)

4. Click **Preview** and select the listing report.
5. Example of a stock document listing report:

    ![print-stock-document-listing3](../../../static/img/usage/stock/stock-report/print-stock-document-listing3.png)

### Print Document Style

1. Tick the relevant checkboxes.

    ![print-stock-document-listing4](../../../static/img/usage/stock/stock-report/print-stock-document-listing4.png)

    | **Field Name**                  | **Explanation**                                                   |
    | ------------------------------- | ----------------------------------------------------------------- |
    | **Print Document Style**        | Tick this checkbox to print a bulk report or send batch emails.   |
    | **Include Cancelled Documents** | Tick this checkbox to include cancelled documents in the listing. |

2. If you tick **Print Document Style**, you will be able to choose a document report format.

    ![print-stock-document-listing5](../../../static/img/usage/stock/stock-report/print-stock-document-listing5.png)

If you want further grouping & sorting, use **Group/Sort By**:

1. You can filter documents by **Project**, **Location**, and **Company Category**.

    ![print-stock-document-listing6](../../../static/img/usage/stock/stock-report/print-stock-document-listing6.png)

2. You can use the **Group by/Sort by** table to choose how you want to group your report listing.

    ![print-stock-document-listing7](../../../static/img/usage/stock/stock-report/print-stock-document-listing7.png)

3. Here is an example of the report:

    ![print-stock-document-listing8](../../../static/img/usage/stock/stock-report/print-stock-document-listing8.png)

## Print Stock Reorder Advice

- The **Print Stock Reorder Advice** report identifies items with quantities below the reorder level set in **Maintain Stock Item**.

### How to Print Stock Reorder Advice

1. **Stock** > **Print Stock Reorder Advice**.

    ![print-stock-reorder-advice](../../../static/img/usage/stock/stock-report/print-stock-reorder-advice.png)

    ![print-stock-reorder-advice1](../../../static/img/usage/stock/stock-report/print-stock-reorder-advice1.png)

    ![print-stock-reorder-advice2](../../../static/img/usage/stock/stock-report/print-stock-reorder-advice2.png)

2. Click the **Apply** button.

3. Click **Preview** and select the listing report.
4. Example of a stock reorder report:

    ![print-stock-reorder-advice3](../../../static/img/usage/stock/stock-report/print-stock-reorder-advice3.png)

### Setting

1. Select the quantity criteria for comparison.

    ![print-stock-reorder-advice4](../../../static/img/usage/stock/stock-report/print-stock-reorder-advice4.png)

    | **Field Name**                             | **Explanation**                                                                                 |
    | ------------------------------------------ | ----------------------------------------------------------------------------------------------- |
    | **On Hand Qty**                            | Current stock balance.                                                                          |
    | **On Hand + PO Qty & SO Qty**              | Stock balance plus Purchase Order Quantity or Sales Order Quantity.                             |
    | **On Hand + PO Qty - SO Qty**              | Stock balance plus Purchase Order Quantity minus Sales Order Quantity.                          |
    | **On Hand + PO Qty (+/-) JO Qty**          | Stock balance plus Purchase Order Quantity plus Job Order Quantity.                             |
    | **On Hand - SO Qty (+/-) JO Qty**          | Stock balance minus Sales Order Quantity plus Job Order Quantity.                               |
    | **On Hand + PO Qty - SO Qty (+/-) JO Qty** | Stock balance plus Purchase Order Quantity minus Sales Order Quantity minus Job Order Quantity. |

2. Select the comparison type. The balance quantities will be compared against the **Max Value**, **Min Value**, or **Reorder Level** defined in **Maintain Stock Item**.

If you want further grouping & sorting, use **Group/Sort By**:

1. You can filter documents by **Item**, **Batch**, and **Company Category**.

    ![print-stock-reorder-advice5](../../../static/img/usage/stock/stock-report/print-stock-reorder-advice5.png)

2. You can use the **Group by/Sort by** table to choose how you want to group your report listing.

    ![print-stock-reorder-advice6](../../../static/img/usage/stock/stock-report/print-stock-reorder-advice6.png)

## Print Stock Physical Worksheet

1. Go to **Stock**.

2. Select **Print Stock Physical Worksheet**.

3. Filter by date, stock group, or other criteria. Ensure you select the correct **Location** and **Batch** if these modules are enabled.

    ![70](../../../static/img/usage/stock/stock-report/stock-physical-worksheet.png)

4. Click **Preview** and choose your report format.

    ![71](../../../static/img/usage/stock/stock-report/stock-physical-worksheet1.png)

5. Print the **Stock Take Sheet** for the storekeeper.

    The storekeeper should manually record the actual quantity in the **Physical Qty** column.

    ![72](../../../static/img/usage/stock/stock-report/stock-physical-worksheet2.png)

6. Once the stock take is complete, perform the stock adjustment in the system. Go to **Stock** > **Stock Adjustment**. Drag out the **Book Qty** and **Physical Qty** columns if they are not visible.

    ![73](../../../static/img/usage/stock/stock-report/stock-physical-worksheet3.png)

    ![74](../../../static/img/usage/stock/stock-report/stock-physical-worksheet4.png)

7. Click on the first item in the **Stock Physical Worksheet**, press **Ctrl + A** on the keyboard to select all items.

    **Then Drag & Drop into Stock Adjustment**.

    ![75](../../../static/img/usage/stock/stock-report/stock-physical-worksheet5.png)

8. Based on the **Stock Take Sheet**, enter the actual physical quantity in the **Physical Qty** column of the Stock Adjustment. The system will calculate the variance against the **Book Qty** and automatically adjust the **Qty** column.

    :::info

    **Book Qty** = The quantity recorded in the system.

    **Physical Qty** = Actual Quantity at your warehouse.

    **Qty** = The variance between Physical and Book Quantity. The system will automatically adjust and update accordingly. (Physical Qty – Book Qty)

    :::

## Print Stock Card & Print Stock Card Qty

- The **Print Stock Card** report shows stock movement and costing over a specific period.
- You can view stock movement by **Location** and **Batch**.

### How to Print Stock Card

1. **Stock** > **Print Stock Document Listing**.

    ![print-stock-card](../../../static/img/usage/stock/stock-report/print-stock-card.png)

    ![print-stock-card1](../../../static/img/usage/stock/stock-report/print-stock-card1.png)

2. Click the **Apply** button.
3. Click **Preview** and select the listing report.
4. Example of a stock card report:

![print-stock-card2](../../../static/img/usage/stock/stock-report/print-stock-card2.png)

### How to Print Stock Card Qty

- Similar to the Stock Card, but this report displays only quantities.

## Print Stock Month End Balance

- The **Print Stock Month End Balance** report shows the month-end stock quantity and total cost.

### How to Print Stock Month End Balance

1. **Stock** > **Print Stock Month End Balance**.

    ![print-stock-month-end-balance](../../../static/img/usage/stock/stock-report/print-stock-month-end-balance.png)

2. Set the date and click the **Apply** button.

    ![print-stock-month-end-balance1](../../../static/img/usage/stock/stock-report/print-stock-month-end-balance1.png)

3. You can filter by **Location**, **Stock Group**, and **Item**.

    ![print-stock-month-end-balance2](../../../static/img/usage/stock/stock-report/print-stock-month-end-balance2.png)

4. Click the **Preview** button.
5. Click **Preview** and select the listing report.
6. Example of a stock month-end report:

    ![print-stock-month-end-balance3](../../../static/img/usage/stock/stock-report/print-stock-month-end-balance3.png)

## Print Stock Aging

- The **Print Stock Aging** report displays the quantity of stock on hand and its aging status.

    ![print-stock-aging](../../../static/img/usage/stock/stock-report/print-stock-aging.png)

### How to Print Stock Aging

1. **Stock** > **Print Stock Aging**.
2. Set your filter options and group by options.

    ![print-stock-aging1](../../../static/img/usage/stock/stock-report/print-stock-aging1.png)

    ![print-stock-aging2](../../../static/img/usage/stock/stock-report/print-stock-aging2.png)

3. Tick **Qty** and/or **Cost** to view the aging based on quantity, cost, or both.

    ![print-stock-aging3](../../../static/img/usage/stock/stock-report/print-stock-aging3.png)

4. Set the stock aging type.

    ![print-stock-aging4](../../../static/img/usage/stock/stock-report/print-stock-aging4.png)

5. **Months**: Aging calculated in 1-month intervals.
6. **Months + 5 Years**: Aging calculated monthly, including items older than 5 years.
7. **3 Months**: Aging calculated in 3-month intervals.
8. Click the **Apply** button.
9. Click **Preview**.

    ![print-stock-aging5](../../../static/img/usage/stock/stock-report/print-stock-aging5.png)

## Print Stock Analysis By Document

- The **Print Stock Analysis By Document** report shows stock movement quantities for each document type (e.g., Invoice, Cash Sales, Purchase Invoice).

### How to Print Stock Analysis By Document

1. **Stock** > **Print Stock Analysis By Document**.

    ![print-stock-analysis-by-document](../../../static/img/usage/stock/stock-report/print-stock-analysis-by-document.png)

    ![print-stock-analysis-by-document1](../../../static/img/usage/stock/stock-report/print-stock-analysis-by-document1.png)

2. Click the **Apply** button.
3. Click **Preview**.
4. Example of a stock analysis by document report:

    ![print-stock-analysis-by-document2](../../../static/img/usage/stock/stock-report/print-stock-analysis-by-document2.png)

## Print Stock Batch Expiry

- The **Print Stock Batch Expiry** report lists all batch items along with their manufacturing and expiry dates.

### How to Print Stock Batch Expiry

1. **Stock** > **Print Stock Batch Expiry**.

    ![print-stock-batch-expiry](../../../static/img/usage/stock/stock-report/print-stock-batch-expiry.png)

2. Click the **Apply** button.

    ![print-stock-batch-expiry1](../../../static/img/usage/stock/stock-report/print-stock-batch-expiry1.png)

3. Click **Preview**.
4. Example of a stock batch expiry report:

    ![print-stock-batch-expiry2](../../../static/img/usage/stock/stock-report/print-stock-batch-expiry2.png)

### How to Assign a Batch to a Stock Item

- For example, after creating batch codes and assigning items in **Maintain Batch**, go to **Sales Invoice**. Select the stock item and then select the batch.

    ![print-stock-batch-expiry3](../../../static/img/usage/stock/stock-report/print-stock-batch-expiry3.png)

    ![print-stock-batch-expiry4](../../../static/img/usage/stock/stock-report/print-stock-batch-expiry4.png)

## Print Stock Serial Number Conflict

- The **Print Stock Serial Number Conflict** report is used to view:

  - Serial Number (SN) items issued without being received.
  - Duplicate SNs received at the same location and batch.

    ![print-stock-serial-number-conflict](../../../static/img/usage/stock/stock-report/print-stock-serial-number-conflict.png)

### How to Print Stock Serial Number Conflict

1. **Stock** > **Print Stock Serial Number Conflict**.

    ![print-stock-serial-number-conflict1](../../../static/img/usage/stock/stock-report/print-stock-serial-number-conflict1.png)

2. Click the **Apply** button.

    ![print-stock-serial-number-conflict2](../../../static/img/usage/stock/stock-report/print-stock-serial-number-conflict2.png)

3. Click **Preview**.
4. Example of a stock serial number conflict report:

    ![print-stock-serial-number-conflict3](../../../static/img/usage/stock/stock-report/print-stock-serial-number-conflict3.png)

### How to Assign a Serial Number to a Stock Item

1. First, go to **Maintain Stock Item** and tick the **Serial No.** checkbox.

    ![print-stock-serial-number-conflict4](../../../static/img/usage/stock/stock-report/print-stock-serial-number-conflict4.png)

2. In purchase documents, assign a Serial Number to the stock item. You can enter it manually, import it from a text file, or generate it automatically.

![print-stock-serial-number-conflict5](../../../static/img/usage/stock/stock-report/print-stock-serial-number-conflict5.png)

### How to Automatically Generate Serial Numbers

1. Click the **Generator** button, set the number format, and click **OK**.

![print-stock-serial-number-conflict6](../../../static/img/usage/stock/stock-report/print-stock-serial-number-conflict6.png)

### How to Import Serial Numbers from a Text File

1. Click the **Import** button, select the text file, and click **OK**.

    ![print-stock-serial-number-conflict7](../../../static/img/usage/stock/stock-report/print-stock-serial-number-conflict7.png)

2. The serial numbers will be successfully imported.

    ![print-stock-serial-number-conflict8](../../../static/img/usage/stock/stock-report/print-stock-serial-number-conflict8.png)

## Print Stock Serial Number Outstanding

- The **Print Stock Serial Number Outstanding** report checks for purchased stock items that have not been assigned a serial number.
- An example of a missing serial number is shown in the purchase invoice below.

    ![print-stock-serial-number-outstanding](../../../static/img/usage/stock/stock-report/print-stock-serial-number-outstanding.png)

### How to Print Stock Serial Number Outstanding

1. **Stock** > **Print Stock Serial Number Outstanding**.

    ![print-stock-serial-number-outstanding1](../../../static/img/usage/stock/stock-report/print-stock-serial-number-outstanding1.png)

2. Click the **Apply** button.

    ![print-stock-serial-number-outstanding2](../../../static/img/usage/stock/stock-report/print-stock-serial-number-outstanding2.png)

3. Click **Preview**.

    ![print-stock-serial-number-outstanding3](../../../static/img/usage/stock/stock-report/print-stock-serial-number-outstanding3.png)
