---
sidebar_position: 2
title: Order Detail
description: Guide to managing order details and actions in XStore
slug: /integration/xstore/order-details
tags: ["e-Commerce", "X-Store", "Order Detail"]
---

## Overview

**Order Detail** allows you to view individual order information and perform actions such as cancellations, returns, and refunds. To access this page, click the **Document** icon on any order row.

![order-detail-enter](../../../../static/img/xstore/order-details/order-detail-enter.png)

![order-detail-overview](../../../../static/img/xstore/order-details/order-detail-overview.png)

The Order Details interface allows you to:

- View order information
- Perform order actions (cancel, return, refund)
- Map order items to stock items

:::info
**Quick Feature:** Use the mapping button to quickly link order items to your stock items directly from this page.
:::

## Lazada

### Order Detail Page

![lazada-order-detail](../../../../static/img/xstore/order-details/lazada/order-detail.png)

| Section           | Description                                                        |
| ----------------- | ------------------------------------------------------------------ |
| **Order Items**   | Products in the order, including their status and shipping details |
| **Order Details** | Buyer, payment, shipping, and billing information                  |
| **Summary**       | Order charges, discounts, and totals                               |

#### Return Order Info

![lazada-return-order-info](../../../../static/img/xstore/order-details/lazada/return-order-info.png)

#### Cancel Order Info

![lazada-cancel-order-info](../../../../static/img/xstore/order-details/lazada/cancel-order-info.png)

### Repack Order

:::info
Available for orders in the **To Process** tab
:::

![lazada-repack-order](../../../../static/img/xstore/order-details/lazada/repack-order.png)

Use the **Repack** action to repack specific items in the order after cancellation of specific items.

### Cancel Order (Seller-Initiated)

:::info
Available for orders in the **New Order**, **To Process**, and **To Ship** tabs
:::

![lazada-cancel-order-button](../../../../static/img/xstore/order-details/lazada/seller-cancel-order.png)

1. Click the **Cancel Order** button at the top right corner

2. Select the cancellation reason and choose the items to cancel

    ![lazada-cancel-order-form](../../../../static/img/xstore/order-details/lazada/seller-cancel-order-form.png)

3. Submit the cancellation request

:::warning
Hover over the warning icon to see Lazada's cancellation policies and potential consequences on this order.

![lazada-cancel-order-warning](../../../../static/img/xstore/order-details/lazada/seller-cancel-order-form-warning.png)
:::

### Return Order (Buyer-Initiated)

:::info
When a buyer initiates a return, the order moves to the **To Return** tab for seller approval.

Return and Refund process may **vary based on the reason** selected by buyers.
:::

![lazada-return-order](../../../../static/img/xstore/order-details/lazada/buyer-return-order.png)

#### 1. Refund Only

During **"Request Initiate"** status, process the refund directly to the buyer.

#### 2. Return and Refund

![lazada-confirm-return-receipt](../../../../static/img/xstore/order-details/lazada/buyer-return-order-confirm-return-receipt.png)

During **"Buyer Return Item"** status:
  1. Wait for the item to be returned
  2. Click **Confirm Return Receipt** when received
  3. Refresh or resync the order to go to the next step
  4. Process or Reject the refund request
    
    ![lazada-process-refund](../../../../static/img/xstore/order-details/lazada/buyer-return-order-process-refund.png)

#### 3. Reject Refund

![lazada-reject-refund](../../../../static/img/xstore/order-details/lazada/buyer-return-order-reject.png)

To reject a refund request:
  1. Provide a reason for rejection
  2. Upload supporting evidence
  3. Submit for platform review

#### 4. Refund Pending

![lazada-refund-pending](../../../../static/img/xstore/order-details/lazada/buyer-return-order-refund-pending.png)

After processing, the status changes to **Refund Pending** while Lazada processes and reviews the refund.

## Shopee

### Order Detail Page

![shopee-order-detail](../../../../static/img/xstore/order-details/shopee/order-detail.png)

| Section            | Details                                                                                   |
| -------------------| ------------------------------------------------------------------------------------------|
| **Order Items**    | The item details in the order, including the status and shipping details                  |
| **Order Details**  | The other information of the order, including buyer details. payment details, and etc.    |
| **Summary**        | The summary payment information                                                           |

#### Return Order Info

![shopee-return-order-info](../../../../static/img/xstore/order-details/shopee/return-order-info.png)

#### Cancel Order Info

![shopee-cancel-order-info](../../../../static/img/xstore/order-details/shopee/cancel-order-info.png)

### Cancel Order (Seller-Initiated)

:::info
Available for orders in the **New Order** and **To Process** tabs
:::

![shopee-cancel-order-button](../../../../static/img/xstore/order-details/shopee/seller-cancel-order.png)

1. Click the **Cancel Order** button at the top right corner

2. Select the cancellation reason

  ![shopee-cancel-order-form](../../../../static/img/xstore/order-details/shopee/seller-cancel-order-form.png)

3. For **Out of Stock** cancellation, select the out-of-stock items

  ![shopee-cancel-order-out-of-stock](../../../../static/img/xstore/order-details/shopee/seller-cancel-order-outofstock.png)

4. Submit the cancellation request

:::warning
Cancelling with "Out of Stock" may reset the item quantity to 0 on the platform
:::

### Cancel Order (Buyer-Initiated)

![shopee-cancel-order-button](../../../../static/img/xstore/order-details/shopee/buyer-cancel-order.png)

Sellers can accept or reject the buyer's cancellation request.

### Return Order (Buyer-Initiated)

#### 1. Refund Only

![shopee-refund-only](../../../../static/img/xstore/order-details/shopee/buyer-refund-only.png)

When a buyer requests **Refund Only**, review the request and confirm refund.

#### 2. Return and Refund (Buyer's Offer)

![shopee-return-refund-action](../../../../static/img/xstore/order-details/shopee/buyer-return-refund.png)

When the latest offer is from the buyer, you can:

  | Action           | Description                       |
  | ---------------- | --------------------------------- |
  | **Create Offer** | Counter with a new offer amount   |
  | **Accept Offer** | Accept the buyer's proposed terms |
  | **Dispute**      | Escalate to Shopee for resolution |

#### 3. Return and Refund (Seller's Offer)

![shopee-return-refund-order](../../../../static/img/xstore/order-details/shopee/seller-return-refund.png)

When you've made an offer and are awaiting buyer response, you can still modify your offer.

#### Create Offer Form:

![shopee-create-offer-form](../../../../static/img/xstore/order-details/shopee/buyer-return-refund-create-offer.png)

#### Dispute Form:

![shopee-dispute-form](../../../../static/img/xstore/order-details/shopee/buyer-return-refund-dispute.png)

## TikTok

### Order Detail Page

![tiktok-order-detail](../../../../static/img/xstore/order-details/tiktok/order-detail.png)

| Section            | Details                                                                                   |
| -------------------| ------------------------------------------------------------------------------------------|
| **Order Items**    | The item details in the order, including the status and shipping details                  |
| **Order Details**  | Other order information, including buyer details, payment details, etc.    |
| **Summary**        | The summary payment information                                                           |

#### Cancel Order Info

![tiktok-cancel-order-info](../../../../static/img/xstore/order-details/tiktok/cancel-order-info.png)

#### Return Order Info

![tiktok-return-order-info](../../../../static/img/xstore/order-details/tiktok/return-order-info.png)

### Cancel Order (Seller-Initiated)

![tiktok-cancel-order-button](../../../../static/img/xstore/order-details/tiktok/seller-cancel-order.png)

1. In the upper-right corner, click the **More** icon and select **Cancel Order**

2. Select a cancellation reason. The estimated refund amount appears under **Refund allocation**

    ![tiktok-cancel-order-form](../../../../static/img/xstore/order-details/tiktok/seller-cancel-order-form.png)

3. Click **Continue** to submit the cancellation request

### Cancel Order (Buyer-Initiated)

![tiktok-buyer-cancel-request](../../../../static/img/xstore/order-details/tiktok/buyer-cancel-order.png)

When a buyer requests cancellation, choose your response:
1. **Approve Cancellation:**

    ![tiktok-approve-cancellation](../../../../static/img/xstore/order-details/tiktok/buyer-cancel-order-approve.png)

2. **Reject Cancellation:**

    ![tiktok-reject-cancellation](../../../../static/img/xstore/order-details/tiktok/buyer-cancel-order-reject.png)

### Refund Order (Seller-Initiated)

![tiktok-refund-order-button](../../../../static/img/xstore/order-details/tiktok/seller-refund-order.png)

1. In the upper-right corner, click the **More** icon and select **Refund Only**

2. Select the items to refund and choose a refund reason

3. Review the estimated amount under **Refund allocation**. To specify a different amount, enter it in **Refund owed**

    ![tiktok-refund-order-form](../../../../static/img/xstore/order-details/tiktok/seller-refund-order-form.png)

4. Click **Create Refund** to submit the refund request

### Return Refund Order (Buyer-Initiated)

![tiktok-return-or-refund-request](../../../../static/img/xstore/order-details/tiktok/buyer-return-order.png)

The buttons will be shown according to the **Return Type** and **Return Status**
1. **Reject Return or Refund:**

    ![tiktok-reject-return-or-refund](../../../../static/img/xstore/order-details/tiktok/buyer-return-order-reject.png)

2. **Approve Return:**

    ![tiktok-approve-return](../../../../static/img/xstore/order-details/tiktok/buyer-return-order-approve-return.png)

## Shopify

### Order Detail Page

![shopify-order-detail](../../../../static/img/xstore/order-details/shopify/order-detail.png)

| Section            | Details                                                                                   |
| -------------------| ------------------------------------------------------------------------------------------|
| **Order Items**    | The item details in the order, including the status and shipping details                  |
| **Order Details**  | Other order information, including payment details, shipping details, etc. |
| **Summary**        | The summary payment information                                                           |

### Mark Order as Paid 

:::info
Available for **Unpaid** orders
:::

![mark-as-paid](../../../../static/img/xstore/order-details/shopify/mark-as-paid.png)

1. In the upper-right corner, click the **More** icon and select **Mark as Paid**

2. Confirm your selection and request will be submitted

### Fulfill Order

You can fulfill Shopify orders from the [**Orders page**](./orders.md#step-2-to-process--to-shipself-deliver) or from the order details. Use the order details when you need to add carrier and tracking information.

![shopify-fulfill-order](../../../../static/img/xstore/order-details/shopify/fulfill-order.png)

1. Under **Shipping Details**, click the **More** icon and select **Fulfill Order**

2. Enter the **Shipping Carrier**, **Tracking Number**, and **Tracking URL**

3. To add tracking information for another shipment, click **Add another tracking number**

    ![shopify-fulfill-order-form](../../../../static/img/xstore/order-details/shopify/fulfill-order-form.png)

4. Choose whether to send a notification to the customer

5. Click **Fulfill Order** to submit the request

After the order is fulfilled, you can change its carrier or tracking information. Under **Shipping Details**, click the **More** icon and select **Update Tracking**.

![shopify-update-tracking](../../../../static/img/xstore/order-details/shopify/update-tracking.png)

### Cancel Order (Seller-Initiated)

:::info
Available for **Non Fulfilled** orders
:::

![shopify-cancel-order](../../../../static/img/xstore/order-details/shopify/seller-cancel-order.png)

1. In the upper-right corner, click the **More** icon and select **Cancel Order**

2. Under **Refund Payments**, select how to issue the refund

3. Select a **Cancellation Reason**

4. Optional: Enter additional information in **Staff Note**

5. Select **Restock items** to add the cancelled items back to your inventory

6. Choose whether to notify the customer by email

    ![shopify-cancel-order-form](../../../../static/img/xstore/order-details/shopify/seller-cancel-order-form.png)

7. Click **Cancel Order** to submit the request

### Return Refund Order (Seller-Initiated)

#### Create Return

:::info
Available for **Fulfilled** orders
:::

![shopify-create-return](../../../../static/img/xstore/order-details/shopify/seller-create-return.png)

1. In the upper-right corner, click the **More** icon and select **Create Return**

2. Select the items and quantities to return, then choose a return reason

3. If applicable, enter the **Return shipping fee** and **Restocking fee**

4. Review the **Expected refund** under **Summary**

    ![shopify-create-return-form](../../../../static/img/xstore/order-details/shopify/seller-create-return-form.png)

5. Click **Create Return** to submit the request

#### Process Return

![shopify-process-return](../../../../static/img/xstore/order-details/shopify/seller-process-return.png)

1. On the **Return Order** card, click the **More** icon and select **Process Return**

2. Select the items and quantities to process

3. To add returned items back to your inventory, select **Restock at** and choose a location

4. If applicable, enter the **Shipping refund** and update the amount under **Refund methods**

    ![shopify-process-return-form](../../../../static/img/xstore/order-details/shopify/seller-process-return-form.png)

5. Choose whether to notify the customer by email

6. Review the refund details, then click **Process Return**

To close the return without processing it, select **Close Return** from the **More** menu on the **Return Order** card.

### Return Refund Order (Buyer-Initiated)

A buyer's return or refund request appears on the **Return Order** card. Open the **More** menu and choose one of the following actions:

![shopify-return-request](../../../../static/img/xstore/order-details/shopify/buyer-request-return-refund.png)

#### Accept and Refund

1. Select **Accept & refund** from the **More** menu

2. Review the returned items and the amount under **Refund summary**

3. Choose whether to notify the customer by email, then click **Accept & refund**

    ![shopify-accept-return](../../../../static/img/xstore/order-details/shopify/buyer-accept-return.png)

#### Decline Return

1. Select **Decline return** from the **More** menu

2. Select a **Decline Reason** and, optionally, enter a note for the customer

3. Click **Confirm** to decline the request

    ![shopify-reject-return](../../../../static/img/xstore/order-details/shopify/buyer-reject-return.png)

:::info
The refund amount for a buyer-initiated request cannot be adjusted manually.
:::

## WooCommerce

### Order Detail Page

![woo-order-detail](../../../../static/img/xstore/order-details/woocommerce/order-detail.png)

| Section            | Details                                                                                   |
| -------------------| ------------------------------------------------------------------------------------------|
| **Order Items**    | The item details in the order, including the status and shipping details                  |
| **Order Details**  | Other order information, including payment details, shipping details, etc. |
| **Summary**        | The summary payment information                                                           |

### Order Notes

![woo-order-note](../../../../static/img/xstore/order-details/woocommerce/order-notes.png)

Use **Order Notes** to add an internal note or send a note to the customer:

1. Enter the note in **Add Note**

2. To make the note visible to the customer, select **Note to Customer**. Leave it cleared to save a private note

3. Click **Add Note**

### Cancel Order (Seller-Initiated)

:::info
Available for **Pending**, **On Hold** and **Processing** orders
:::

![woo-order-action](../../../../static/img/xstore/order-details/woocommerce/order-actions.png)

1. In the upper-right corner, click the **More** icon and select **Cancel Order**

2. Click **Continue** to confirm the cancellation

    ![woo-seller-cancel-order](../../../../static/img/xstore/order-details/woocommerce/seller-cancel-order.png)

### Process Refund (Seller-Initiated)
![woo-order-action](../../../../static/img/xstore/order-details/woocommerce/order-actions.png)

1. In the upper-right corner, click the **More** icon and select **Process Refund**

2. Enter the refund amount in **Offer Amount**, up to the displayed maximum payable amount

3. Optional: Enter a reason and specify the quantity of each item to restock

4. If applicable, select **API Refund**

    ![woo-seller-create-refund](../../../../static/img/xstore/order-details/woocommerce/seller-create-refund.png)

5. Click **Continue** to create the refund
