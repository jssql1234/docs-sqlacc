---
sidebar_position: 1
title: General
description: Purchase Data Entry here
slug: /usage/purchase/general
tags: ["SQL Account", "Usage", "Purchase", "General"]
---

## Purchase Request

Purchase Request is an internal document used within a company between departments to request for purchase or a product

For example, you want to purchase more office supplies. You have to submit a purchase request to the purchasing department.

![1](../../../static/img/getting-started/user-guide/purchase/jj1.png)

![2](../../../static/img/getting-started/user-guide/purchase/jj2.png)

### Data Entry

**1. Purchase | Purchase Request | New**

**2. Select Supplier Code**

**3. Insert Item Code and details** (e.g. Qty, Unit Cost)

**4. Write a description to explain your purchase request**

![3](../../../static/img/getting-started/user-guide/purchase/jj3.png)

**5. Click the Save button once you are done. Below is the example of the entry created.**

![4](../../../static/img/getting-started/user-guide/purchase/jj4.png)

## Purchase Order

Purchase Order is a document that is issued by the purchasing department when placing an order with their supplier.

A purchase order document contains the details (quantity, unit price) of the items that want to be purchased.

![10](../../../static/img/getting-started/user-guide/purchase/jj10.png)

![11](../../../static/img/getting-started/user-guide/purchase/jj11.png)

### Data Entry

1. **Purchase | Purchase Order | New**

2. **Select Supplier Code**

3. **Insert Item**

   3a. **Insert Item Code and details** (e.g. Qty, Unit Cost)

      :::note

      You can navigate the search column by using the “TAB” button on your keyboard. It will apply to all drop down tables.

      :::

   3b. **Click on the show/hide/move column icon to customize your column layout**.

   3c. If you want to key in for a discount amount, you may tick the discount field by following step 3b and update the discount field. You can key in multiple levels of discount as shown by the picture attached.

4. **Write a description to explain your purchase order**

![12](../../../static/img/getting-started/user-guide/purchase/jj12.png)

5. **Click the Save button once you are done. Below is the example of the entry created:**

![13](../../../static/img/getting-started/user-guide/purchase/jj13.png)

### More : Project

There are 2 types of project you need to be take note:

1.Document Project

2.Detail Project

For **document project**, you need to point to **MORE** section **(on the left side bar)**.

For **detail project**, you have to insert the **project** column out from Field Chooser.

![14](../../../static/img/getting-started/user-guide/purchase/jj14.png)

### Attachment

You can use this feature to attach external PDF, excel, word documents and image files.

![15](../../../static/img/getting-started/user-guide/purchase/jj15.png)

1. Go to the left of the screen and click "Attachment"

2. Click the small black arrow at the link icon

3. Select ‘Attach files to Local Drive’, and choose the file from your computer that you want to attach

### Note

1. Click on the Note section (on the LEFT side bar).

2. RIGHT click it, you will see the Rich Text Editor pop-up.

3. You can start key-in the note. See the example screenshot below.

4. Click on the X button to save and exit the Rich Text Editor.

5. You will get prompted the ‘Save changes?’ message. Click YES to save it.

![16](../../../static/img/getting-started/user-guide/purchase/jj16.png)

### How to preview report

To preview the report, you may click on the preview button and select the format you wish to print.

![17](../../../static/img/getting-started/user-guide/purchase/jj17.png)

### How to send report via Whatsapp

![18](../../../static/img/getting-started/user-guide/purchase/jj18.png)

A QR code will appear on the screen. Scan the QR code with your Whatsapp's Whatsapp Web function.

## Goods Receive

Goods Received is a document that is issued after receiving the delivery as proof of the order receipt.

![19](../../../static/img/getting-started/user-guide/purchase/jj19.png)

![20](../../../static/img/getting-started/user-guide/purchase/jj20.png)

### Data Entry

1. **Purchase | Goods Receive | New**

2. **Select Supplier Code**

3. **Insert Item Code and details (e.g. Qty, Unit Cost)**

4. **Write a description to explain your goods receive**

![21](../../../static/img/getting-started/user-guide/purchase/jj21.png)

5. **Click the Save button once you are done. Below is the example of the entry created:**

![22](../../../static/img/getting-started/user-guide/purchase/jj22.png)

### Transfer From PO

1. **Purchase | Goods Receive | New**

2. **Select Supplier Code**

3. **Right Click on G/R Note title**, select **Transfer from Purchase Order**, tick the document that you wish to transfer

4. **Save** the Goods Received Note

![23](../../../static/img/getting-started/user-guide/purchase/jj23.png)

### Notes - Landing Cost

Landing Cost is to handle the cost to the warehouse that is not billed by the same supplier. In other words, it is an additional cost to increase your stock cost. This cost is depending on the company whether they want to add in or not. For Instant, I buy the product from Supplier A, but ship by Transport company B, this transport charges you may enter at landing cost to increase your product cost.

![24](../../../static/img/getting-started/user-guide/purchase/jj24.png)

How to set Landing Cost?

Follow the below image:

![25](../../../static/img/getting-started/user-guide/purchase/jj25.png)

1. **Landing Cost 1** = Key your Landing Cost to this column.(This cost will not take into the account.)
2. **Landing Cost 2** = If you have a different calculation than Landing Cost 1, you may enter your value to this column.
3. Click on + Button to select the cost allocated.

![26](../../../static/img/getting-started/user-guide/purchase/jj26.png)

**Formula for Cost Allocated By SubTotal**

- Formula : Item Subtotal / Document Subtotal * Landing Cost1

![27](../../../static/img/getting-started/user-guide/purchase/jj27.png)

:::note

   Item 1 = A/B * C

   Landing Cost1 (D) = 50.00 / 1949.00 * 200 = 5.13

   Item 2

   Landing Cost (D) = 1899.00 / 1949.00 * 200 = 194.87

:::

![28](../../../static/img/getting-started/user-guide/purchase/jj28.png)

:::note

   How to get unit cost = 5.51?

   Formula : Product Unit Cost + Item Landing Cost1 / Item Qty

   Formula : 5 + (5.13 / 10) = 5.51

:::

**Formula for Cost Allocated By Qty**

- Formula : Item Qty / Document Qty * Landing Cost1

![29](../../../static/img/getting-started/user-guide/purchase/jj29.png)

![30](../../../static/img/getting-started/user-guide/purchase/jj30.png)

:::note

   Item 1 : 10 / 11 * 200 = 181.81

   Item 2 : 1 / 11 * 200 = 18.18

:::

**Stock Card Report Outcome:**

:::note

   *Item ANT : unit cost will be 23.18, how to get 23.18 ?
   
   Unit Cost + (Landing Cost1 / Qty) = 5 + (181.82 / 10) = 23.18

   *Item LCLIP : Unit Cost will be 1917.18

   Unit Cost + (Landing Cost1 / Qty) = 1899 + (18.18 / 1) = 1917.18

:::

**Formula for Cost Allocated By Smallest Qty**

- Formula : Item Qty * Rate/ Sum(Qty * Rate) * Landing Cost1

![31](../../../static/img/getting-started/user-guide/purchase/jj31.png)

![32](../../../static/img/getting-started/user-guide/purchase/jj32.png)

:::note

   Item 1 : 10 * 12 = 120 / 121 = 198.35

   Item 2 : 1 * 1 = 1 / 121 = 1.65

:::

**Stock Card Report Outcome**

:::note

   Item 1 : Unit cost for ANT = [Unit Price + (Item Landing Cost1 / Item Qty)] / ItemRate = [30 + (198.35 / 10)] / 12 = 4.15

   Item 2 : Unit cost for LCLIP = [Unit Price + (Item Landing Cost1 / Item Qty)] / ItemRate = 1899 + 1.65 = 1900.65

:::

That seed will grow to be a peach tree. You may wish for an apple or an orange, but you will get a peach.

## Purchase Invoice

You can key in the purchase invoice after your purchase order has been approved and after you have received your goods.

![38](../../../static/img/getting-started/user-guide/purchase/jj38.png)

### Data Entry

1. **Purchase | Purchase Invoice | New**

![39](../../../static/img/getting-started/user-guide/purchase/jj39.png)

2. **Select Supplier Code**

3. **Insert Item**

   3a. **Insert Item Code and details** (e.g. Qty, Unit Cost)

   :::note

      You can navigate the search column by using the "TAB" button on your keyboard. It will apply to all drop down tables.

   :::

   ![40](../../../static/img/getting-started/user-guide/purchase/jj40.png)

4. **Write a description to explain your purchase invoice**

5. **Click the Save button once you are done.  Below is the example of the entry created:**

**Double Entry will be:-**

| Account            | DR (RM) | CR (RM) |
|--------------------|---------|---------|
| Purchase Account   | 500.00  |         |
| Supplier Account   |         | 500.00  |

### Transfer From DO

1. **Purchase | Purchase Invoice | New**

## Cash Purchase



## Extra Goods Receive



## Purchase Debit Note



## Purchase Returned



## Purchase Cancelled Note


