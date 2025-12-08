---
sidebar_position: 2
title: Order Detail
description: Guide to managing order details and actions in XStore
slug: /integration/xstore/order-details
tags: ["SQL Account", "Integration", "e-Commerce", "XStore", "Order Detail"]
---

The **Order Detail** module allows you to view individual order information and perform actions such as cancellations, returns, and refunds.

To access this page, click the **document icon** on any order row.

---

## Overview

The Order Details interface allows you to:

- View order information
- Perform order actions (cancel, return, refund)
- Map order items to stock items

![Order Detail Overview](../../../../static/img/xstore/order-details/order-detail-overview.png)

> **Quick Feature:** Use the mapping button to quickly link order items to your stock items directly from this page.

---

## Platform-Specific Guides

Each e-commerce platform has unique order detail layouts and available actions. Select your platform below:

- [Lazada](#lazada)
- [Shopee](#shopee)
- [TikTok](#tiktok)

---

## Lazada

### Order Detail Page

![Lazada Order Detail](../../../../static/img/xstore/order-details/lazada/order-detail.png)

The order information section displays:

| Section              | Details                                     |
| -------------------- | ------------------------------------------- |
| **Order Details**    | Order ID, Shop ID, Payment Method           |
| **Payment Details**  | Currency, Payment Time                      |
| **Shipment Details** | Provider type, Shipping type, address, etc. |
| **Voucher Details**  | Applied discounts and promotions on an item |

Order items are grouped by package and tracking ID.

![Lazada Cancelled Order Item](../../../../static/img/xstore/order-details/lazada/cancelled-order-item.png)

> **Note:** Cancelled items display a red badge indicating the cancellation reason.

### Return Order Info

![Lazada Return Order Info](../../../../static/img/xstore/order-details/lazada/return-order-info.png)

### Cancel Order Info

![Lazada Cancel Order Info](../../../../static/img/xstore/order-details/lazada/cancel-order-info.png)

---

### Repack Order

![Lazada Repack Order](../../../../static/img/xstore/order-details/lazada/repack-order.png)

**Available for:** Orders in the **To Process** tab

Use the Repack action to repack specific items in the order after cancellation of specific items.

---

### Cancel Order (Seller-Initiated)

![Lazada Cancel Order Button](../../../../static/img/xstore/order-details/lazada/seller-cancel-order.png)

**Available for:** Orders in **New Order**, **To Process**, or **To Ship** tabs

**Steps to cancel:**

1. Click the **Cancel Order** button
2. Select the cancellation reason
3. Choose the items to cancel
4. Submit the cancellation request

![Lazada Cancel Order Form](../../../../static/img/xstore/order-details/lazada/seller-cancel-order-form.png)

![Lazada Cancel Order Warning](../../../../static/img/xstore/order-details/lazada/seller-cancel-order-form-warning.png)

> **Warning:** Hover over the warning icon to see Lazada's cancellation policies and potential consequences on this order.

---

### Return Order (Buyer-Initiated)

![Lazada Return Order](../../../../static/img/xstore/order-details/lazada/buyer-return-order.png)

When a buyer initiates a return, the order moves to the **To Return** tab for seller approval.

**Return Processing Options:**

| Option                | Description                                |
| --------------------- | ------------------------------------------ |
| **Refund Only**       | Issue refund without requiring item return |
| **Return and Refund** | Refund after receiving returned item       |
| **Reject Refund**     | Decline the refund request with evidence   |

**1. Refund Only**

During **"Request Initiate"** status, process the refund directly to the buyer.

**2. Return and Refund**

![Lazada Confirm Return Receipt](../../../../static/img/xstore/order-details/lazada/buyer-return-order-confirm-return-receipt.png)

During **"Buyer Return Item"** status:

1. Wait for the item to be returned
2. Click **Confirm Return Receipt** when received
3. Process the refund

![Lazada Process Refund](../../../../static/img/xstore/order-details/lazada/buyer-return-order-process-refund.png)

**3. Reject Refund**

![Lazada Reject Refund](../../../../static/img/xstore/order-details/lazada/buyer-return-order-reject.png)

To reject a refund request:

1. Provide a rejection reason
2. Upload supporting evidence
3. Submit for platform review

**4. Refund Pending**

![Lazada Refund Pending](../../../../static/img/xstore/order-details/lazada/buyer-return-order-refund-pending.png)

After processing, the status changes to **Refund Pending** while Lazada processes and reviews the refund.

---

## Shopee

### Order Detail Page

![Shopee Order Detail](../../../../static/img/xstore/order-details/shopee/order-detail.png)

The order information section displays:

| Section              | Details                                   |
| -------------------- | ----------------------------------------- |
| **Buyer Details**    | Customer username, user ID and address    |
| **Payment Details**  | Payment method, Currency and Payment time |
| **Shipment Details** | Carrier information                       |
| **Extra Details**    | Additional order notes and info           |

### Return Order Info

![Shopee Return Order Info](../../../../static/img/xstore/order-details/shopee/return-order-info.png)

---

### Cancel Order (Seller-Initiated)

![Shopee Cancel Order Button](../../../../static/img/xstore/order-details/shopee/seller-cancel-order.png)

**Available for:** Orders in the **New Order** and **To Process** tabs

![Shopee Cancel Order Form](../../../../static/img/xstore/order-details/shopee/seller-cancel-order-form.png)

**Out of Stock Cancellation:**

![Shopee Cancel Order Out of Stock](../../../../static/img/xstore/order-details/shopee/seller-cancel-order-outofstock.png)

When selecting "Out of Stock" as the reason:

1. Select the out-of-stock items
2. Submit the cancellation

> **Note:** Cancelling with "Out of Stock" may reset the item quantity to 0 on the platform.

---

### Cancel Order (Buyer-Initiated)

![Shopee Cancel Order Button](../../../../static/img/xstore/order-details/shopee/buyer-cancel-order.png)

Sellers can accept or reject the buyer's cancellation request.

---

### Return Order (Buyer-Initiated)

**1. Refund Only**

![Shopee Refund Only](../../../../static/img/xstore/order-details/shopee/buyer-refund-only.png)

When a buyer requests **Refund Only**, review the request and choose to approve or reject.

**2. Return and Refund (Buyer's Offer)**

![Shopee Return Refund Action](../../../../static/img/xstore/order-details/shopee/buyer-return-refund-action.png)

When the latest offer is from the buyer, you can:

| Action           | Description                       |
| ---------------- | --------------------------------- |
| **Create Offer** | Counter with a new offer amount   |
| **Accept Offer** | Accept the buyer's proposed terms |
| **Dispute**      | Escalate to Shopee for resolution |

**3. Return and Refund (Seller's Offer)**

![Shopee Return Refund Order](../../../../static/img/xstore/order-details/shopee/buyer-return-refund.png)

When you've made an offer and are awaiting buyer response, you can still modify your offer.

**Create Offer Form:**

![Shopee Create Offer Form](../../../../static/img/xstore/order-details/shopee/buyer-return-refund-create-offer.png)

**Dispute Form:**

![Shopee Dispute Form](../../../../static/img/xstore/order-details/shopee/buyer-return-refund-dispute.png)

---

## TikTok

### Order Detail Page

![TikTok Order Detail](../../../../static/img/xstore/order-details/tiktok/order-detail.png)

### Cancel Order Info

![TikTok Cancel Order Info](../../../../static/img/xstore/order-details/tiktok/cancel-order-info.png)

### Return Order Info

![TikTok Return Order Info](../../../../static/img/xstore/order-details/tiktok/return-order-info.png)

---

### Cancel Order (Seller-Initiated)

![TikTok Cancel Order Button](../../../../static/img/xstore/order-details/tiktok/seller-cancel-order.png)

**Available for:** Orders in the **New Order** and **To Process** tabs

![TikTok Cancel Order Form](../../../../static/img/xstore/order-details/tiktok/seller-cancel-order-form.png)

Select a cancellation reason and submit to cancel the order.

---

### Cancel Order (Buyer-Initiated)

![TikTok Buyer Cancel Request](../../../../static/img/xstore/order-details/tiktok/buyer-cancel-order.png)

When a buyer requests cancellation, choose your response:

**Approve Cancellation:**

![TikTok Approve Cancellation](../../../../static/img/xstore/order-details/tiktok/buyer-cancel-order-approve.png)

**Reject Cancellation:**

![TikTok Reject Cancellation](../../../../static/img/xstore/order-details/tiktok/buyer-cancel-order-reject.png)

---

### Return Order (Buyer-Initiated)

![TikTok Return Request](../../../../static/img/xstore/order-details/tiktok/buyer-return-order.png)

When a buyer initiates a return, review the request and respond:

**Approve Return:**

![TikTok Approve Return](../../../../static/img/xstore/order-details/tiktok/buyer-return-order-approve.png)

**Reject Return:**

![TikTok Reject Return](../../../../static/img/xstore/order-details/tiktok/buyer-return-order-reject.png)

---

## Related

- [Order Management](./orders) – Managing orders across all platforms
