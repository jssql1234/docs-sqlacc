---
sidebar_position: 1
title: Order
description: Guide to managing orders in XStore
slug: /integration/xstore/orders
tags: ["e-Commerce", "X-Store", "Orders"]
---

## Overview

The **Order** module allows you to view, process, and manage orders from all your connected e-commerce platforms (Lazada, Shopee, TikTok, etc.) in one centralized location.

![order-management-page](../../../../static/img/xstore/orders/order-page.png)

To access this page, navigate to **Orders** in the sidebar menu.

The Order Management interface is organized into tabs representing each stage of the order lifecycle. You can:

- Filter orders by date range
- Search by Order ID or Store Name
- Perform bulk actions (packing, shipping, printing)
- Track order status across all platforms

## Order Statuses

![order-status-tabs](../../../../static/img/xstore/orders/order-statuses.png)

Orders are categorized into the following status tabs:

| Status         | Description                                                   |
| -------------- | ------------------------------------------------------------- |
| **Unpaid**     | Orders placed but not yet paid by the customer                |
| **New Order**  | Paid orders ready to be processed                             |
| **To Process** | Packed orders waiting to be shipped                           |
| **To Ship**    | Orders ready for courier handover                             |
| **Shipped**    | Orders currently in transit                                   |
| **Delivered**  | Orders successfully delivered to the customer                 |
| **Completed**  | Orders finalized and closed                                   |
| **To Cancel**  | Buyer-initiated cancellation requests pending seller approval |
| **To Return**  | Buyer-initiated return requests pending seller approval       |
| **Others**     | Orders with special or exceptional statuses                   |

## Order Processing Workflow

The order processing flow moves through several stages. Different actions are available at each stage.

### Step 1: Pack New Orders

![pack-orders](../../../../static/img/xstore/orders/pack-order.png)

1. Select orders by clicking the checkbox next to each order
2. Click the **Pack** button
3. Packed orders will move to the **To Process** tab

### Step 2: Process Orders for Shipping

![to-process-tab](../../../../static/img/xstore/orders/to-process.png)

1. Select orders by clicking the checkbox next to each order
2. Click the **To Ship** button
3. Orders will move to the **To Ship** tab
4. (Optional) Use **Stock Pick** feature to verify order items before shipping
5. (Optional) Click the **Scan** icon to use the **Scan To Ship** feature for faster processing

#### Print Picking Document

![picking-list-options](../../../../static/img/xstore/orders/pickinglist-doc.png)

1. Click the **Print Picking List** button to generate the following:
   - **Picking List Summary:** A consolidated list of all order items for batch picking
   - **Picking List:** Individual picking lists generated per order, including barcodes 
2. The printed picking list can be used together with the **Scan To Ship** feature to speed up order fulfillment

### Step 3: Stock Pick (Optional)

Use **Stock Pick** to optionally verify order items before processing orders for shipping.

![to-process-tab-stock-pick](../../../../static/img/xstore/orders/to-process-tab-stock-pick.png)

1. Click the **Stock Pick** icon

![stock-pick-empty](../../../../static/img/xstore/orders/stock-pick-empty.png)

1. Click on the screen and scan the Order ID
2. **Alternative:** Type the Order ID manually and press Enter

![stock-pick-order](../../../../static/img/xstore/orders/stock-pick-order.png)

![stock-pick-verification](../../../../static/img/xstore/orders/stock-pick-verification.png)

1. Click on the screen and scan the barcode
2. **Alternative:** Type the barcode number manually and press Enter
3. **Alternative:** Type the quantity in the **Scanned Qty** field

If the scanned quantity does not match the target quantity (status showing **Incomplete** or **Overscan**), but you have manually confirmed the order is correct:

1. Click the **Complete Verification** button to mark the order as verified
2. The verified order will appear in the verified order list as shown below

   ![stock-pick-verified-orders-list](../../../../static/img/xstore/orders/stock-pick-verified-orders-list.png)

3. Click **Proceed to Next Order** to continue; the order remains in the list until you proceed

If the scanned items fully match, a success popup will appear and the verified order list will update automatically:

![stock-pick-sucessful-verification-popup](../../../../static/img/xstore/orders/stock-pick-sucessful-verification-popup.png)

1. Click **Proceed to Next Order** on the popup to reset and continue with the next order
2. **Alternative:** Click **Review Current Order** to stay on the current order

![stock-pick-to-ship-selection](../../../../static/img/xstore/orders/stock-pick-to-ship-selection.png)
To move verified orders to **To Ship**:

1. Select orders by clicking the checkbox next to each order
2. Click the **To Ship** button

![stock-pick-to-ship-result](../../../../static/img/xstore/orders/stock-pick-to-ship-result.png)

### Step 4: Scan To Ship (Optional)

![scan-to-ship-interface](../../../../static/img/xstore/orders/scan-to-ship-empty.png)

1. Click on the screen and scan the barcode from the picking list
2. **Alternative:** Type the barcode number manually and press Enter

![scanned-orders](../../../../static/img/xstore/orders/scan-to-ship.png)

| Action                     | Description                            |
| -------------------------- | -------------------------------------- |
| **Print AWB**              | Print Air Waybills for selected orders |
| **Print Courier Manifest** | Generate a manifest for courier pickup |

### Step 5: To Ship

![to-ship-tab](../../../../static/img/xstore/orders/to-ship.png)

| Action                     | Description                            |
| -------------------------- | -------------------------------------- |
| **Print AWB**              | Print Air Waybills for selected orders |
| **Print Courier Manifest** | Generate a manifest for courier pickup |

### Step 6: Self Deliver

![self-deliver-tab](../../../../static/img/xstore/orders/self-deliver.png)

| Action                     | Description                            |
| -------------------------- | -------------------------------------- |
| **Mark as Delivered**      | Mark the order as delivered            |

## General Features

![order-filter](../../../../static/img/xstore/orders/order-filter.png)

| Feature                         | Description                                                                                             |
|---------------------------------|---------------------------------------------------------------------------------------------------------|
| **Search**                      | Find orders by **Order ID**, **Store Name**, **Package ID** or **Tracking Number** using the search bar |
| **Column Visibility**           | Click the leftmost button to show/hide specific table columns                                           |
| **Filter by Platform**          | Displays orders based on platform filtered                                                              |
| **Filter by Platform Status**   | Displays orders based on platform status filtered                                                       |
| **Filter by Shipment Provider** | Displays orders based on shipment provider filtered                                                     |
| **Date Range**                  | Filter orders by created or updated date using the date picker                                          |
