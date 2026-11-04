---
sidebar_position: 8
title: Payments
description: Guide to Payments
slug: /integration/xstore/payments
tags: ["e-Commerce", "X-Store", "Payments"]
---

The **Manage Payments** page allows you to view and manage all payment details. The number below the table shows the **total number** of transactions or orders in the data table based on the view options.

![payment-overview](../../../static/img/xstore/payments/payment-overview.png)

## Data Table Features

![payment-details](../../../static/img/xstore/payments/payment-details.png)

| Column                                                                   | Description                                                                     |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| **Transaction Date** (Payment view) / **Order ID** (Order view)          | The grouping field - by transaction date or order ID                            |
| **Description**                                                          | Details of each transaction line item                                           |
| **Currency**                                                             | The currency used (e.g., MYR)                                                   |
| **Amount**                                                               | Amount of each individual transaction line item                                 |
| **Total**                                                                | Combined total amount of all transaction line items within the grouped row      |

## Export CSV Features

Users can export monthly transaction data in CSV format.

1. Click the **Export CSV** button

    ![export-button](../../../static/img/xstore/payments/export-button.png)

2. In the export dialog:

    - Select a specific store from the dropdown, or leave the default selection as All Stores to export transactions from all stores.

    - Select the desired month and year from the available options.

    - Click **Export CSV** button to start the export.

    ![export-dialog](../../../static/img/xstore/payments/export-dialog.png)

3. A ZIP file will be downloaded containing separate daily CSV files for each day within the selected month.

## General Features

![payment-actions](../../../static/img/xstore/payments/payment-actions.png)

| Actions                     | Description                                                                                                                                                                                                                             |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sync Payment**            | Click the **Sync Payment** button at the top-left corner beside the title "Payment Management" to synchronize payment data from your e-commerce platform                                                                                   |
| **Refresh Payment**         | Click the **Refresh Payment** button to refresh payment data                                                                                                                                                                            |
| **Customize Table Columns** | Click the **column icon** on the left side (beside the Start Date field) to show or hide specific columns and customize which information is displayed                                                                                  |
| **Advanced Filter**         | Click the filter options to narrow down payment data by grouping, store, or date range. See [Advanced Filter Options](#advanced-filter-options) below.                                                                                  |
| **Search by Order ID**      | Enter an **Order ID** in the search field to filter and display matching orders                                                                                                                                                         |
| **Expand All**              | Click **Expand All** in the top-right to expand all transaction rows and reveal detailed breakdowns                                                                                                                                     |

### Advanced Filter Options

![payment-filter](../../../static/img/xstore/payments/payment-filter.png)

| Filter              | Description                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Group by Payment**| Displays transactions grouped by transaction date                                                                                   |
| **Group by Order**  | Displays individual orders grouped by Platform Order ID                                                                             |
| **Store Name**      | Click the **All Stores** dropdown to choose a specific store, or leave as default to show all stores                                |
| **Payment Date**    | Select a **Start Date** and **End Date** (up to today) of transaction date to filter transactions within a date range               |
