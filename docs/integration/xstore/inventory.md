---
sidebar_position: 108
title: Inventory
description: A guide on inventory
slug: /integration/xstore/inventory
tags: ["SQL Account", "Integration", "e-Commerce", "XStore", "Inventory"]
---

## Products Page

### Map Products

1. Go to **Inventory > Products**

   ![1](../../../static/img/xstore/inventory/product-overview.png)

2. Click the **Map Product Button** to open the **Map Product Dialog**

   ![2](../../../static/img/xstore/inventory/map-product.png)

   ![3](../../../static/img/xstore/inventory/map-dialog-overview.png)

   :::info
   Use the **Filter Button** to narrow your **Platform Products View**, or use the **Search Bar** to find specific ecommerce products and stock items.
   :::

3. Select ecommerce products synced from various platforms and map them to stock items synced from SQL Account

   ![4](../../../static/img/xstore/inventory/mapping-product-1.png)

   ![5](../../../static/img/xstore/inventory/mapping-product-2.png)

   :::info
   **Ecommerce Products** are mapped to **Stock Item UOM**.
   :::

4. To unmap products, select them and click **Unmap**

   ![6](../../../static/img/xstore/inventory/unmap-product-1.png)

   ![7](../../../static/img/xstore/inventory/unmap-product-2.png)

## Stocks Page

### Map Products to Specific Stock Items

1. Go to **Inventory > Stocks**

   ![8](../../../static/img/xstore/inventory/stock-overview.png)

2. Click the icon to view stock details

   ![9](../../../static/img/xstore/inventory/view-stock-detail.png)

   :::info
   - **Map Product** can be performed here as well
   - **Location Description** and **Code** are fetched from SQL Account
   :::

3. Click the **+** icon to open the **Map Product Dialog**

   ![10](../../../static/img/xstore/inventory/stock-detail.png)

4. Select the **Platform Product** and click **Map Product** to map it directly to this **Stock Item UOM**

   ![11](../../../static/img/xstore/inventory/map-selective-uom.png)

   :::info
   Ensure your store is mapped to the correct stock item location, or mapped items won't appear.
   :::

### Update Quantity

1. Click the **+/-** icon to update the ecommerce platform product quantity

   ![12](../../../static/img/xstore/inventory/update-quantity.png)

   :::info
   The ecommerce platform quantity is based on the current quantity of stock items in the location mapped to your store.
   :::
