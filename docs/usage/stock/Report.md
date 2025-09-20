---
sidebar_position: 3
title: Stock Report
description: Stock Report
slug: /usage/stock/Stock Report
tags: ["SQL Account", "Usage", "Inventory", "Stock","Report"]
---

## Print Stock Document Listing
- Print Stock Document Listing can be used for you to see all the stock adjustment documents that you have issued.
- You can see Stock Received Listing, Stock Issue Listing, Stock Transfer Listing, Stock Adjustment Listing.

### 1.How to Print Stock Document Listing
1. **Stock** > **Print Stock Document Listing**

![297](../../../static/img/getting-started/user-guide/68jt.png)

2. Select which Document listing you want to see. Follow the image

![298](../../../static/img/getting-started/user-guide/69jt.png)

3. Press Apply Button

![299](../../../static/img/getting-started/user-guide/70jt.png)

4. Click Preveiw & Listing Report
5. Example of stock document listing report

![300](../../../static/img/getting-started/user-guide/71jt.png)

### 2.Print Document Style
1. Tick relevant check boxes

![301](../../../static/img/getting-started/user-guide/72jt.png)

<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Print Document Style</b></td>
      <td>
        <ul>
          <li>Tick this checkbox to print out bulk report or send batch email</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Include Cancelled Documents</b></td>
      <td>
        <ul>
          <li>Tick this checkbox to include cancelled documents in the listing</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

2. If you Tick Print Document Style , you will see that you will able able to choose purchase document report format.

![302](../../../static/img/getting-started/user-guide/73jt.png)

### 3. Group/Sort By
1. You can filter your documents based on Project, location and Company Category

![303](../../../static/img/getting-started/user-guide/74jt.png)

2. You can use the Group by/Sort by table to choose how you want to group your report listing

![304](../../../static/img/getting-started/user-guide/75jt.png)

3. Here is an example of the report

![305](../../../static/img/getting-started/user-guide/76jt.png)

## Print Stock Reorder Advice
- Print Stock Reorder Advice can be used for you to check which items have quantities below the set reorder level (set in maintain stock item)

### 1. How to Print Stock Reorder Advice
1. **Stock** > **Print Stock Reorder Advice**

![306](../../../static/img/getting-started/user-guide/77jt.png)

![307](../../../static/img/getting-started/user-guide/78jt.png)

![308](../../../static/img/getting-started/user-guide/79jt.png)

2. Press Apply Button
3. Click Preveiw & Listing Report
4. Example of stock reorder report

![309](../../../static/img/getting-started/user-guide/80jt.png)

### 2. Setting
1. Select what quantities you wish to compare against

![310](../../../static/img/getting-started/user-guide/81jt.png)

<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>On Hand Qty</b></td>
      <td>Stock balance quantity</td>
    </tr>
    <tr>
      <td><b>On Hand + PO Qty &amp; On Hand + SO Qty</b></td>
      <td>Stock balance quantity plus Purchase Order Quantity or Sales Order Quantity</td>
    </tr>
    <tr>
      <td><b>On Hand + PO Qty - SO Qty</b></td>
      <td>Stock balance quantity plus Purchase Order Quantity minus Sales Order Quantity</td>
    </tr>
    <tr>
      <td><b>On Hand + PO Qty (+/-) JO Qty</b></td>
      <td>Stock balance quantity plus Purchase Order Quantity plus Job Order Quantity</td>
    </tr>
    <tr>
      <td><b>On Hand - SO Qty (+/-) JO Qty</b></td>
      <td>Stock balance quantity minus Sales Order Quantity plus Job Order Quantity</td>
    </tr>
    <tr>
      <td><b>On Hand + PO Qty - SO Qty (+/-) JO Qty</b></td>
      <td>Stock balance quantity plus Purchase Order Quantity minus Sales Order Quantity minus Job Order Quantity</td>
    </tr>
  </tbody>
</table>

2. After that, select the type of comparison. Will the balance quantities be compared to the Max Value, Min Value or the Reorder level . All set in Maintain Stock Item .

### 3. Group/Sort By
1. You can filter your documents based on Item, Batch and Company Category

![311](../../../static/img/getting-started/user-guide/82jt.png)

2. You can use the Group by/Sort by table to choose how you want to group your report listing

![312](../../../static/img/getting-started/user-guide/83jt.png)

## Print Stock Physical Worksheet
1. Click on **Stock**

2. Choose **Print Stock Physical Worksheet**

3. **Filter** by date, stock group or others **information** that you want to do for the stock take, please **make sure that you choose the correct location and batch if you have these two modules**.

   ![70](../../../static/img/getting-started/user-guide/69.png)

4. lick on Preview & choose your report format.

   ![71](../../../static/img/getting-started/user-guide/70.png)

5. **Print out the “Stock Take Sheet”** for stock keeper.

   The stock keeper should manually **fill in the actual quantity into the “physical qty” column**.

   ![72](../../../static/img/getting-started/user-guide/71.png)

6. After complete updating the stock take report by your stock-keeper, do your stock adjustment in system from **Stock** > **Stock Adjustment** > **and drag out Book Qty and Physical Qty**.

   ![73](../../../static/img/getting-started/user-guide/72.png)

   ![74](../../../static/img/getting-started/user-guide/73.png)

7. Click on the first item in **Stock Physical Worksheet**, press on **Ctrl + A** on the keyboard to select all items.

   **Then Drag & Drop into Stock Adjustment**.

   ![75](../../../static/img/getting-started/user-guide/74.png)

8. Based on the stock keeper’s Stock Take Report, **fill in the actual physical quantity** in your warehouse into the Stock Adjustment **Physical Qty column**, the system will calculate the variance based on the Book Qty and apply a correction to the Qty column.

   :::note

   **Book Qty** = Quantity that is recorded in system.

   **Physical Qty** = Actual Quantity at your warehouse.

   **Qty** = Variance between Physical and Book Quantity, system will auto-adjust then update accordingly. (Physical Qty – Book Qty)

   :::

## Print Stock Card & Print Stock Card Qty
- Print Card can be used to see your stock movement and stock cost during a certain period of time.
- You can see your stock movement based on location and batch.

### 1. How to Print Stock Card
1. **Stock** > **Print Stock Document Listing**

![313](../../../static/img/getting-started/user-guide/84jt.png)

![314](../../../static/img/getting-started/user-guide/85jt.png)

2. Press Apply Button
3. Click Preview & Listing Report
4. Example of stock card report

![315](../../../static/img/getting-started/user-guide/86jt.png)

### 2. How to Print Stock Card Qty
- Same as Print Stock Card the different is this report is just shown Qty

## Print Stock Month End Balance
- Print Stock Month End Balance can be used to see your month end stock quantity and total cost .
### 1. How to Print Stock Month End Balance
1. **Stock** > **Print Stock Month End Balance**

![316](../../../static/img/getting-started/user-guide/87jt.png)

2. Set the date and press the Apply button.

![317](../../../static/img/getting-started/user-guide/88jt.png)

3. You can set your filters, you can filter yout stock month end by location, and stock group and item

![318](../../../static/img/getting-started/user-guide/89jt.png)

4. Press Preview button
5. Click Preview& Listing Report
6. Example of stock month end report

![319](../../../static/img/getting-started/user-guide/90jt.png)

## Print Stock Aging
- Print Stock Aging is used to see how many quantities of a certain stock that you have on hand and how much quantity of that stock is sold

![320](../../../static/img/getting-started/user-guide/91jt.png)

### 1. How to Print Stock Aging
1. **Stock** > **Print Stock Aging**
2. Set your filter option and group by options

![321](../../../static/img/getting-started/user-guide/92jt.png)

![322](../../../static/img/getting-started/user-guide/93jt.png)

3. Tick Qty and/or Cost if you want to see the aging for both or either

![323](../../../static/img/getting-started/user-guide/94jt.png)

4. set stock aging type

![324](../../../static/img/getting-started/user-guide/95jt.png)

5. Months = aging calculated by every 1 months
6. Months + 5 Years = aging calculated for every month and also above 5 years
7. 3 motnhs = aging calculated every 3 months
8. Press Apply Button
9. Click Preview

![325](../../../static/img/getting-started/user-guide/96jt.png)

## Print Stock Analysis By Document
- Print Stock Analysis By Document can be used to see your stock movement quantity for each document type like Invoice, Cash sales, purchase invoice etc.
### 1. How to Print Stock Analysis By Document
1. **Stock** > **Print Stock Analysis By Document**

![326](../../../static/img/getting-started/user-guide/97jt.png)

![327](../../../static/img/getting-started/user-guide/98jt.png)

2. Press Apply Button
3. Click Preview
4. Example of stock analysis by document report

![328](../../../static/img/getting-started/user-guide/99jt.png)


## Print Stock Batch Expiry
- Print Stock Batch Expiry to see all the items in your batches along with their manufacturing dates and expiry dates.
### 1. How to Print Stock Batch Expiry
1. **Stock** > **Print Stock Batch Expiry**

![329](../../../static/img/getting-started/user-guide/100jt.png)

2. Press Apply Button

![330](../../../static/img/getting-started/user-guide/101jt.png)

3. Click Preview
4. Example of stock batch expiry report

![331](../../../static/img/getting-started/user-guide/102jt.png)

### 2. How to Assign Batch to Your Stock Item
- For example, After you have created your batch codes and assigned the items at "Maintain Batch" go to Sales Invoice. Select the stock item and slect the batch

![332](../../../static/img/getting-started/user-guide/103jt.png)

![333](../../../static/img/getting-started/user-guide/104jt.png)


## Print Stock Serial Number Conflict
- Print Stock Serial Number Conflict to see
- SN item issue out with SN without receiving SN
- Duplicate SN received at same location and batch

![334](../../../static/img/getting-started/user-guide/105jt.png)

### 1. How to Print Stock Serial Number Conflict
1. **Stock** > **Print Stock Serial Number Conflict**

![335](../../../static/img/getting-started/user-guide/106jt.png)

2. Press Apply Button

![336](../../../static/img/getting-started/user-guide/107jt.png)

3. Click Preview
4. Example of stock batch expiry report

![337](../../../static/img/getting-started/user-guide/108jt.png)

### 2. How to Assign Serial to Your Stock Item
1. First go to Maintain Stock Item an tick the serial number check box

![338](../../../static/img/getting-started/user-guide/109jt.png)

2. At your purchases, assign Serial number to your stock item, you can key it in, import it in from a text file, or automatically generate it .

![339](../../../static/img/getting-started/user-guide/110jt.png)

### 3. How to Automatically Generate Serial Number for Your Stock Item
1. Click the generator button, set your number format, and press OK.

![340](../../../static/img/getting-started/user-guide/111jt.png)

### 4. How to Import Serial Number for Text File for Your Stock Item
1. Click the import button, select your text file, and press OK.

![341](../../../static/img/getting-started/user-guide/112jt.png)

2. Your serial number has been successfully imported

![342](../../../static/img/getting-started/user-guide/113jt.png)

## Print Stock Serial Number Outstanding
- Print Stock Serial Number Outstanding to see if you did not assign any serial number to you purchase stock items.
- Example of missing out a serial number can be seen in this purchase invoice.

![343](../../../static/img/getting-started/user-guide/114jt.png)

### 1. How to Print Stock Serial Number Outstanding
1. **Stock** > **Print Stock Serial Number Outstanding**

![344](../../../static/img/getting-started/user-guide/115jt.png)

2. Press Apply Button

![345](../../../static/img/getting-started/user-guide/116jt.png)

3. Click Preview

![346](../../../static/img/getting-started/user-guide/117jt.png)