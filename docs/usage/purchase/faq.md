---
sidebar_position: 3
title: FAQ
description: FAQ
slug: /usage/purchase/faq
tags: ["SQL Account", "Usage", "Purchase", "FAQ"]
---

## 1. Why are the Unit Price and Subtotal missing in the Goods Received Note/Invoice even after granting "Show Cost" rights?

**Issue:**

1. User Access Control has been granted for **Show Cost in Purchase Goods Received**.
2. However, the Purchase Goods Received Note still does not display the **Unit Price**, **Tax Amount**, or **Subtotal**.

![missing-column](../../../static/img/usage/purchase/faq/missing-column.png)

**Solution:**

1. Hover your mouse over any column header in the detail grid.

    ![right-click-detail-grid-columns](../../../static/img/usage/purchase/faq/right-click-detail-grid-columns.png)

2. **Right-click > Grid Layout > Load Layout**.

    ![grid-load-layout](../../../static/img/usage/purchase/faq/grid-load-layout.png)

3. In the **Load Grid Layout** window, click **Reset Layout**.

    ![reset-layout](../../../static/img/usage/purchase/faq/reset-layout.png)

4. The detail grid layout will be reset to reflect the user's current access rights.

    ![default-layout](../../../static/img/usage/purchase/faq/default-layout.png)
