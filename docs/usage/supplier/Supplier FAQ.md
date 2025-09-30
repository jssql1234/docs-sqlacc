---
sidebar_position: 3
title: Supplier FAQ
description: Supplier Frequently Asked Questions
slug: /usage/supplier/Supplier FAQ
tags: ["SQL Account", "Supplier", "FAQ"]
---

## JOMPAY - How to add the Ref 2 (optional) in the bank payment file format?

**Issue:**

How to capture the JomPay Ref 2 (bill no) in the bank payment file format?

![Supplier_FAQ_1](../../../static/img/getting-started/user-guide/LimYuHangSupplierFAQ1.jpg)

**Solution:**

1. Go to **Tools | DIY | SQL Control Center**...
2. Add the JomPAY Ref2 field under **Supplier | Supplier Payment | Payment Fields**.

| Field Name  | Data Type | Size |
|-------------|-----------|------|
| JomPAY_Ref2 | String    | 30   |

![Supplier_FAQ_2](../../../static/img/getting-started/user-guide/LimYuHangSupplierFAQ2.jpg)

3. Create **Quick Form** and add the UDF_JomPay_Ref2.

![Supplier_FAQ_3](../../../static/img/getting-started/user-guide/LimYuHangSupplierFAQ3.jpg)

4. At **Supplier Payment**, key-in the bill no into UDF_JomPAY_Ref2 under JOMPAY tab.

![Supplier_FAQ_4](../../../static/img/getting-started/user-guide/LimYuHangSupplierFAQ4.jpg)

5. JomPAY Ref 2 will be captured in the bank JomPAY payment format.

![Supplier_FAQ_5](../../../static/img/getting-started/user-guide/LimYuHangSupplierFAQ5.jpg)

:::note NOTE:
The above solution is using SQL Account version 784 and above. Modules required:
1. Interbank GIRO
2. DIY field (or Professional Set).
:::