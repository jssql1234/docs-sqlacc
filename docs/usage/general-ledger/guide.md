---
sidebar_position: 1
title: Guide
description: General Ledger Info
slug: /usage/general-ledger/guide
tags: ["SQL Account", "Usage"]
---

## Maintain Account

1. Creating a New Account
    1. Go to **GL** → **Maintain Account** → Select a category (e.g., Fixed Assets) → **New**.
    2. Enter the **GL Code** and **Description** (alphanumeric characters are supported).
    3. Select the **Special Account Type** if applicable (e.g., if the account is an Accumulated Depreciation Account for Fixed Assets).
    4. Click **OK**. Your new account is now created.

    ![1](../../../static/img/usage/general-ledger/guide/chart-step1-1.png)

    ![2](../../../static/img/usage/general-ledger/guide/chart-step1-2.png)

2. Creating a Sub-Account
    1. Select the parent account (e.g., Cash at Bank).
    2. Follow the same steps as [creating a new account](#maintain-account).

    ![3](../../../static/img/usage/general-ledger/guide/chart-step2-1.png)

You can create unlimited levels of sub-accounts. Simply select any account and add a sub-account or sub-sub-account to it.

## Cash Book Entry

:::info

Watch the tutorial video here: [YouTube](https://www.youtube.com/watch?v=rh0L-Kol1ts&feature=youtu.be)

:::

Cash Book Entry is typically used for non-customer/supplier payments or receipts, such as payments for salaries, utilities, etc.

1. Go to **GL** → **Cash Book Entry** → **New** (choose between **Payment Voucher** or **Official Receipt**).

    ![4](../../../static/img/usage/general-ledger/guide/cb-entry-step1.png)

2. **Enter Payable Name** → Select **GL Code** → **Tax** → **Amount**.

    ![5](../../../static/img/usage/general-ledger/guide/cb-entry-step2.png)

## Journal Entry

:::info

Watch the tutorial video here: [YouTube](https://www.youtube.com/watch?v=WHzNMsCmFHg&feature=youtu.be)

:::

1. Go to **GL** → **Journal Entry**.
2. Enter your double-entry transactions.
3. Click **Save**. (The system will block the entry if the Debit and Credit amounts do not tally.)

    ![6](../../../static/img/usage/general-ledger/guide/jr-entry.png)

## Foreign Bank Adjustment

- Revalue foreign bank balances at the end of each month.
- Automatically calculate and post double-entry transactions for unrealized FOREX gains or losses.

Refer to this ledger example:

![7](../../../static/img/usage/general-ledger/guide/f-bank-adj.png)

In this scenario, the Local Balance is RM 57,350. You wish to revalue it using a monthly exchange rate of 4.50000 to adjust the local balance to RM 56,250.

### Foreign Bank Adjustment Entry

1. Click **New**.
2. Enter the date (e.g., the end of the month).
3. Click the **Bank Revalue** button.

    ![8](../../../static/img/usage/general-ledger/guide/f-bank-adj-entry-step3.png)

4. Select the foreign bank. The system will retrieve the bank balance from the ledger as of the selected date.
5. Enter the **Revalue currency rate** (e.g., 4.5000). The system will automatically calculate the unrealized FOREX gain/loss.

    ![9](../../../static/img/usage/general-ledger/guide/f-bank-adj-entry-step5.png)

6. Click **OK** to proceed.
7. Click **Save**.

    ![10](../../../static/img/usage/general-ledger/guide/f-bank-adj-entry-step7.png)

## Maintain Opening Balance

1. Go to **GL** → **Maintain Opening Balance**.
2. Highlight the account for which you wish to enter an opening balance and click **Edit**.
3. Enter the amount in **Local DR** or **Local CR**, then click **Save**.
4. Ensure that the total **DR** and **CR** figures tally.

    ![11](../../../static/img/usage/general-ledger/guide/o-balance.png)

## Bank Reconciliation

1. Go to **GL** → **Bank Reconciliation** → **New**.
2. Right-click to view **Opening Bank Reconciliation**.
3. Set the **Date** (must be before the System Conversion Date).

    ![12](../../../static/img/usage/general-ledger/guide/bank-recon.png)

## Maintain Stock Value

1. Go to **GL** → **Maintain Stock Value** → **Edit**.
2. Set the **Year**.
3. Enter the **Opening Balance**.

    ![13](../../../static/img/usage/general-ledger/guide/stock-value-step3-1.png)
    ![14](../../../static/img/usage/general-ledger/guide/stock-value-step3-2.png)

## Maintain Budget

1. Click **Edit**.
2. Enter the budget values for each month.
3. Once finished, click **Save**.

    ![15](../../../static/img/usage/general-ledger/guide/maintain-budget.png)
