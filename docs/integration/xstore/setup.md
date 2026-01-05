---
sidebar_position: 113
title: Setup
description: A guide to set up SQL X-Store App
slug: /integration/xstore/setup
tags: ["e-Commerce", "X-Store", "Setup"]
---

<div align="justify"> This guide walks you through the complete setup of the **SQL X-Store** App — from creating a company to syncing data from **E-commerce platforms** and **SQL Account**.</div>

## Step 1: Create Company

1. Click **Create Company** in Company List page

    ![1](../../../static/img/xstore/setup/create-company.png)

2. Enter the **Company Name**, **Email**, and **Phone Number**

3. Click **Create Company**

    ![2](../../../static/img/xstore/setup/input-company-info.png)

4. Select the newly created company

    ![3](../../../static/img/xstore/setup/select-company.png)

5. The system will navigate to the **Company Profile** page

    ![4](../../../static/img/xstore/setup/company-profile.png)

## Step 2: Link Store

<div align="justify"> Connect E-commerce stores to sync **store**, **product**, **order**, and **payment** data.</div>

1. Click **Stores** in the sidebar

    ![5](../../../static/img/xstore/setup/store-sidebar.png)

2. Click **Link Store**

    ![6](../../../static/img/xstore/setup/link-store.png)

> 📌 For detailed instructions on linking store, navigate to **Integration > XStore > [Stores](./stores.md)**

### Auto-Sync Behavior

- After linking, the system **automatically syncs the past 3 days** of product, order, and payment data.
- Sync actions are locked for **10 minutes** to prevent overload.
- After 10 minutes, manual sync becomes available.

## Step 3: Configure Company Settings

1. Click **Settings > Company** from the sidebar

    ![7](../../../static/img/xstore/setup/company-sidebar.png)

2. Click **Edit**

    ![8](../../../static/img/xstore/setup/add-key.png)

3. Copy the **Access Key** and **Secret Key** from SQL Account and fill in both fields to enable SQL sync

4. Click **Save**

    ![9](../../../static/img/xstore/setup/input-key.png)

## Step 4: Code Mapping

<div align="justify">Sync **Stock**, **Customer**, **Location**, and **Payment** codes from SQL Account to map codes such as **Location**, **Project**, **Voucher**, **Discount**, **Shipping**, **Transaction**, **Payment**, and **Customer** codes for invoice posting to SQL Account.</div>

1. Click **Stores** in the sidebar

    ![10](../../../static/img/xstore/setup/store-sidebar.png)

2. Click the **Config** (⚙️) icon of any store

    ![11](../../../static/img/xstore/setup/store-config.png)

3. A dialog will open:

    1. Select the **code type** from the dropdown

    2. Click **Map Codes**

        ![12](../../../static/img/xstore/setup/map-codes.png)

4. A success message will appear once mapping is completed

    ![13](../../../static/img/xstore/setup/map-success.png)

## Step 5: Sync Stock Items from SQL Account

Sync stock items from SQL Account for **product mapping** and **quantity control**.

1. Click **Inventory > Stocks** in the sidebar

    ![14](../../../static/img/xstore/setup/stock-sidebar.png)

2. Click **Sync Stock**

    ![15](../../../static/img/xstore/setup/sync-stock.png)

3. Choose sync method:

    1. **Sync All**, or

    2. Tick checkboxes and click **Sync Selected**

        ![16](../../../static/img/xstore/setup/select-stockSync.png)

4. Synced stock items will appear in the Data Table

    ![17](../../../static/img/xstore/setup/stock-items.png)

## Manual Sync

If platform data failed to sync during store linking, you can sync manually

### Sync Product Data

1. Click **Inventory > Products** in the sidebar

    ![18](../../../static/img/xstore/setup/product-sidebar.png)

2. Click (**⟲**) icon

    ![19](../../../static/img/xstore/setup/sync-product.png)

3. A dialog will open:

    1. Tick checkboxes to select stores

    2. Click **Sync Selected**

        ![20](../../../static/img/xstore/setup/select-productSync.png)

### Sync Order Data

1. Click **Orders** in the sidebar

    ![21](../../../static/img/xstore/setup/order-sidebar.png)

2. Click (**⟲**) icon

    ![22](../../../static/img/xstore/setup/sync-order.png)

3. A dialog will open:

    1. Sync with **Date Filter**

        1. Select date range using the **Date Picker**

            ![23](../../../static/img/xstore/setup/select-syncDate.png)

        2. Tick checkboxes to select stores

        3. Click **Sync Selected**

        4. To change the selected date, click **Change**

            ![24](../../../static/img/xstore/setup/change-syncDate.png)

    2. Sync without **Date Filter** (will only sync past 3 days data)

        1. Tick checkboxes to select stores

        2. Click **Sync Selected**

            ![25](../../../static/img/xstore/setup/select-orderSync.png)

### Sync Payment Data

1. Click **Payments** in the sidebar

    ![26](../../../static/img/xstore/setup/payment-sidebar.png)

2. Click (**⟲**) icon

    ![27](../../../static/img/xstore/setup/sync-payment.png)

3. A dialog will open:

    1. Sync with **Date Filter**

        1. Select date range using the **Date Picker**

            ![28](../../../static/img/xstore/setup/select-paymentSyncDate.png)

        2. Tick checkboxes to select stores

        3. Click **Sync Selected**

        4. To change the selected date, click **Change**

            ![29](../../../static/img/xstore/setup/change-syncDate.png)

    2. Sync without **Date Filter** (will only sync past 3 days data)

        1. Tick checkboxes to select stores

        2. Click **Sync Selected**

            ![30](../../../static/img/xstore/setup/select-orderSync.png)
