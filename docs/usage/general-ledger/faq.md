---
sidebar_position: 3
title: FAQ
description: General Ledger FAQ Info
slug: /usage/general-ledger/faq
tags: ["SQL Account", "Usage", "FAQ"]
---

## Trial Balance Issues

### Trial Balance Does Not Balance in YTD (Year To Date)

**Issue:**

The Year To Date (YTD) Debit and Credit totals do not balance in the Trial Balance because the Retained Earnings account is missing.

![1](../../../static/img/usage/general-ledger/faq/tb-not-balance-iss.png)

**Solution:**

1. Go to **GL** → **Maintain Account...**
2. Restore the **Retained Earnings** account by dragging and dropping it into the **Retained Earnings** group (original).

    ![2](../../../static/img/usage/general-ledger/faq/tb-not-balance-sol.png)

3. Re-apply the Trial Balance.
4. Once the Retained Earnings account is restored, the YTD Debit and Credit totals should balance.

### Trial Balance is Not Balanced

If your Trial Balance does not balance, perform the following checks:

#### 1. Ensure Retained Earnings has a valid Account Code

Go to **GL** → **Maintain Account**.

![66](../../../static/img/usage/general-ledger/faq/trial-balance-not-tally/1.png)

:::note
If the Retained Earnings group is empty, create an account under **Reserve**, then drag it into the **Retained Earnings** group.
:::

#### 2. Ensure the Opening Balance is Balanced

1. Go to **GL** → **Maintain Opening Balance**.
2. Uncheck **Project** at the top left.
3. Ensure that **Local DR** and **Local CR** totals are balanced.

   ![67](../../../static/img/usage/general-ledger/faq/trial-balance-not-tally/2.png)

#### 3. Identify Imbalances in Current Transactions

:::tip
If the steps above are correct, the imbalance is likely caused by a current transaction.
:::

1. Go to **GL** → **Print Journal of Transaction Listing**.
2. Select the date period that is not balanced.
3. Click **Preview**.
4. Select the report named: **GL Journal-of-Transaction-Imbalance-Document**.
5. This report will list the specific documents causing the imbalance.
6. You may need to upload a backup file to support for further investigation.

## Bank and Currency Management

### Setting a Foreign Bank Account to USD

**Issue:**

I cannot enter foreign bank transactions in USD.

![3](../../../static/img/usage/general-ledger/faq/fb-usd-iss.png)

**Solution:**

Ensure you have the following add-on modules:

- **Multi-Currency**: Allows adding multiple currency codes (e.g., USD, SGD).
- **Advance Currency**: Allows bank accounts to use foreign currencies.

1. Go to **Tools** → **Maintain Payment Method...**
2. Edit the **Foreign Bank Account**.
3. Change the currency to **USD**.

    ![4](../../../static/img/usage/general-ledger/faq/fb-usd-sol1.png)

4. The foreign bank account will now be valued in USD. See the example below in Supplier Payment.

![5](../../../static/img/usage/general-ledger/faq/fb-usd-sol2.png)

### Foreign Bank Adjustment

1. Go to **GL** → **Foreign Bank Adjustment** → **New** → Click **Bank Revalue**.

    ![39](../../../static/img/usage/general-ledger/faq/foreign-bank-adjustment/1.png)

2. In the Revalue window, select the **Bank Account Code** and **Date**.

    ![40](../../../static/img/usage/general-ledger/faq/foreign-bank-adjustment/2.png)

3. The USD balance and local amount will be displayed based on the ledger report.

    ![41](../../../static/img/usage/general-ledger/faq/foreign-bank-adjustment/3.png)

4. Enter the **Revalue to currency rate**. The system will automatically recalculate:
   - **New local balance amount**
   - **Gain/Loss Amount**

    ![42](../../../static/img/usage/general-ledger/faq/foreign-bank-adjustment/4.png)

5. Click **OK**.

    ![43](../../../static/img/usage/general-ledger/faq/foreign-bank-adjustment/5.png)

6. The system will automatically post the double entries.

    ![44](../../../static/img/usage/general-ledger/faq/foreign-bank-adjustment/6.png)

7. Click **Save**.
8. Verify the adjustment in the ledger report.

## Fixed Assets and Depreciation

### Recording Accumulated Depreciation for Fixed Assets

1. Go to **GL** → **Journal Entry** → **New**.
2. Enter the double entry for recording accumulated depreciation.

   :::info
   **Example:** Recording motor vehicle depreciation for the year 2015:
   - **Debit:** Depreciation Expenses (RM 1,000)
   - **Credit:** Accumulated Depreciation of Motor Vehicle (RM 1,000)
   :::

3. Click **Save**.

   ![6](../../../static/img/usage/general-ledger/faq/dep-fixed-asset-step1.png)

### Copying Depreciation for Subsequent Years

1. Go to **GL** → **Journal Entry** and open the depreciation entry from the previous year (e.g., 2015).
2. Right-click on an empty space and select **Copy Journal Entry**.

   ![7](../../../static/img/usage/general-ledger/faq/dep-fixed-asset-step2.png)

3. Click **New**.
4. Right-click on an empty space and select **Paste Journal Entry**.

   ![8](../../../static/img/usage/general-ledger/faq/dep-fixed-asset-step3.png)

5. Update the date, description, and amount as needed.

   ![9](../../../static/img/usage/general-ledger/faq/dep-fixed-asset-step4.png)

6. Click **Save**.

## Stock Value Management

### Auto Maintain Stock Value with Project Setup

:::caution
Requires SQL Account version 839 or above.
:::

#### Step 1: Enable Auto Post GL Stock Value

1. Go to **Tools** → **Options**.

    ![10](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/1.png)

2. Select **Miscellaneous**.
3. Check **Auto Post GL Stock Value**.

    ![11](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/2.png)

#### Step 2: Map Balance Sheet Stock Account

1. Go to **Stock** → **Maintain Stock Group**.

    ![12](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/3.png)

2. Click **Edit**.
3. Select the **Account Code** for Stock Value Posting.
4. Click **Save**.

    ![13](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/4.png)

    :::note
    Ensure all Stock Groups are mapped to a **Balance Sheet Account Code**.
    :::

    ![14](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/5.png)

#### Step 3: Map Project Code in Maintain Location

1. Go to **Stock** → **Maintain Location**.

    ![15](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/6.png)

2. Click **Edit**.
3. Assign a stock project to each location.
4. Click **Save**.

    ![16](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/7.png)

    :::info
    Ensure all locations are mapped to a **Project Code**.
    :::

    ![17](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/8.png)

    :::note
    You may skip this step if you only use one project.
    :::

#### Step 4: Maintain Stock Month End

This step shows the total stock value for the default project and specific projects (e.g., P1).

:::info **Example A: Default Project**
Project Code: ----
Closing Stock: 308,534.22
:::

![18](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/9.png)

:::info **Example B: Project P1**
Project Code: P1
Closing Stock: 3,560.00
:::

![19](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/10.png)

#### Step 5: Automatic Stock Value Updates in Financial Reports

:::note
When you apply a **Profit & Loss Statement, Balance Sheet, or Trial Balance**, the system automatically retrieves the stock value from the **Stock Month End Balance** and updates the closing stock value in **Maintain Stock Value**.
:::

1. Example of a Balance Sheet Statement showing the **Closing Stock Value**.

    ![20](../../../static/img/usage/general-ledger/faq/auto-post-gl-stock-value/11.png)

:::info
If the date falls outside the **Maintain Acceptable Trans Date** range, the system will not retrieve the stock value or perform the update.
:::

### Auto Post Stock Month End Value Setup

:::warning
Requires SQL Account version 748 or above.
:::

This feature automatically posts the stock value from the Month End value to the GL Maintain Stock Value.

#### Step 1: Configure Stock Groups

Go to **Stock** → **Maintain Stock Group**.

![21](../../../static/img/usage/general-ledger/faq/auto-post-stock-month-end-value/1.png)

#### Step 2: Generate Stock Month End Balance Report

Go to **Stock** → **Print Stock Month End Balance Report**.

![22](../../../static/img/usage/general-ledger/faq/auto-post-stock-month-end-value/2.png)

:::info
You must fill in the **Balance Sheet Account** in the Stock Group to update the GL Stock Value.
:::

#### Step 3: Verify in Maintain Stock Value

Go to **GL** → **Maintain Stock Value**.

![23](../../../static/img/usage/general-ledger/faq/auto-post-stock-month-end-value/3.png)

## Bank Reconciliation

### Auto Bank Reconciliation Example

#### Step 1: Create a New Bank Reconciliation

1. Go to **GL** → **Bank Reconciliation** → **New**.
2. Select the **Bank Statement Date**.
3. Select the **Account**.
4. Check **Show Current Recon Transactions**.
5. Click **Apply**.

   ![24](../../../static/img/usage/general-ledger/faq/auto-recon/1.png)

6. Click **Load Statement**.

   ![25](../../../static/img/usage/general-ledger/faq/auto-recon/2.png)

7. Select your **Bank Statement (PDF / CSV)**.

   ![26](../../../static/img/usage/general-ledger/faq/auto-recon/3.png)

8. The system will detect your bank name and prompt a confirmation message. Click **Yes** if it is correct.

   ![28](../../../static/img/usage/general-ledger/faq/auto-recon/5.png)

9. Once the statement is loaded, the bank closing amount will be automatically filled.

   ![29](../../../static/img/usage/general-ledger/faq/auto-recon/6.png)

   :::info
   **Matching Criteria:**
   1. Cheque number + Amount
   2. Description + Amount
   :::

10. The system will automatically match transactions with the bank statement and check them (highlighted in yellow).

    Transactions that cannot be auto-matched will remain unchecked (indicated by the red box).

   ![30](../../../static/img/usage/general-ledger/faq/auto-recon/7.png)

#### Step 2: Manually Match Unmatched Transactions

1. Select an unmatched transaction.
2. At the bottom, search for **SAME DR/CR AMOUNT**. You will see one or more **Match** buttons if matching amounts are found.

   ![31](../../../static/img/usage/general-ledger/faq/auto-recon/8.png)

3. Click **Match** when you identify the correct bank transaction (e.g., Salary for Ali).

   ![32](../../../static/img/usage/general-ledger/faq/auto-recon/9.png)

   The system will then check the transaction and display the date and bank description in the **Bank Statement (Match)** column.

### Manual Bank Reconciliation Example

:::note
For Opening Bank Reconciliation, please refer to this [Guide](../../usage/general-ledger/guide.md#bank-reconciliation).
:::

Bank reconciliation ensures that the company's records (check register, **General Ledger**, **Balance Sheet**, etc.) match the bank's records.

#### Reconciling Bank Transactions

1. Go to **GL** → **Bank Reconciliation**.

   ![33](../../../static/img/usage/general-ledger/faq/bank-recon/1.png)

   ![34](../../../static/img/usage/general-ledger/faq/bank-recon/2.png)

2. Select the **Bank Statement Date**.
3. Select the **Bank Account** (e.g., Hong Leong Bank).
4. Set the **Display Period** (typically, the 'From' date is left blank, and the 'To' date matches the Bank Statement Date).
5. Check the following options:
   - **Show Unticked Transaction**
   - **Show Current Recon Transaction**
   - **Merge Bank Charges**
6. Click **Apply**.
7. Check the transactions that match your bank statement and click **Save**.

   ![35](../../../static/img/usage/general-ledger/faq/bank-recon/3.png)

   ![36](../../../static/img/usage/general-ledger/faq/bank-recon/4.png)

#### Printing the Bank Reconciliation Report

After completing the reconciliation, you can save and preview the report.

![37](../../../static/img/usage/general-ledger/faq/bank-recon/5.png)

:::tip
Press **F6** to preview the report.
:::

## Financial Analysis and Reporting

### How to Calculate P&L Percentages

![38](../../../static/img/usage/general-ledger/faq/cal-p&l-percent/1.png)

:::note
**Formula:** (Account Amount / Total Sales) * 100
:::

#### Examples

- **Sales % (A):** (184,119.49 / 296,502.11) * 100 = **62.1%**
- **Purchase % (C):** (7,406.8 / 296,502.11) * 100 = **2.5%**
- **Gross Profit % (D):** (281,662.21 / 296,502.11) * 100 = **95.0%**
- **Expenses % (E):** (10,000 / 296,502.11) * 100 = **3.4%**
- **Net Profit % (F):** (271,805.66 / 296,502.11) * 100 = **91.7%**

:::info
Percentages are rounded to one decimal point.
:::

### P&L Statement for More Than 12 Months

1. Go to **GL** → **Print Profit & Loss Statement**.

    ![49](../../../static/img/usage/general-ledger/faq/p&l-more-than-12/1.png)

2. Right-click the **SQL Icon** and select **800 x 600** to resize the screen.

    ![50](../../../static/img/usage/general-ledger/faq/p&l-more-than-12/2.png)

3. Drag the report name **This Year - 2 Column** to your desktop.

    ![51](../../../static/img/usage/general-ledger/faq/p&l-more-than-12/3.png)

4. Drag the report from your desktop back into the SQL Account window.

    ![52](../../../static/img/usage/general-ledger/faq/p&l-more-than-12/4.png)

5. Click **OK** when prompted.

    ![53](../../../static/img/usage/general-ledger/faq/p&l-more-than-12/5.png)

6. Double-click the report name **This Year - 2 Column** (displayed in blue).

    ![54](../../../static/img/usage/general-ledger/faq/p&l-more-than-12/6.png)

   1. Enter a new report name.
   2. Change the period class to **Fixed Date**.
   3. Set **Param 1** (Date From) and **Param 2** (Date To).
   4. Click **OK**.

   ![55](../../../static/img/usage/general-ledger/faq/p&l-more-than-12/7.png)

:::info
Apply the report as usual; the results will be based on the parameters set. You can repeat these steps for the **Balance Sheet Statement**.
:::

### P&L Statement with Appropriation Account

1. Go to **GL** → **Maintain Account**.

    ![56](../../../static/img/usage/general-ledger/faq/p&l-statement-appropriation-acc/1.png)

    1. Select the **Appropriation Account**.
    2. Click **New**.

        ![57](../../../static/img/usage/general-ledger/faq/p&l-statement-appropriation-acc/2.png)

    3. Enter the **GL Code** and **Description**, then click **OK**.

2. Go to **GL** → **Journal Entry** → **New**.

    ![58](../../../static/img/usage/general-ledger/faq/p&l-statement-appropriation-acc/3.png)

    **Example:** Debit Dividend (2,000), Credit Bank (2,000).

3. Go to **GL** → **Print P&L Statement**.
   1. Select the **Date**.
   2. Select the report format: **This Year – 2 Column**.
   3. Click **Apply**.

       ![59](../../../static/img/usage/general-ledger/faq/p&l-statement-appropriation-acc/4.png)

   4. Click **Preview**.

       ![60](../../../static/img/usage/general-ledger/faq/p&l-statement-appropriation-acc/5.png)

       ![61](../../../static/img/usage/general-ledger/faq/p&l-statement-appropriation-acc/6.png)

## Troubleshooting and Other FAQs

### General Ledger Report Ref1 (DocNo) Appears as `<<New>>`

If `Ref1(DocNo)` appears as `<<New>>` in the General Ledger Report, follow these steps to fix it:

![62](../../../static/img/usage/general-ledger/faq/solution-gl-report-ref1-as-new/1.png)

1. Identify the document source and date (e.g., 31/03/2015).

    ![63](../../../static/img/usage/general-ledger/faq/solution-gl-report-ref1-as-new/2.png)

2. Go to **Journal Entry** and locate the entries for that date.

    ![64](../../../static/img/usage/general-ledger/faq/solution-gl-report-ref1-as-new/3.png)

3. Click **Edit** and then **Save** for all entries on that date.
4. Re-apply the ledger report to verify the fix.

    ![65](../../../static/img/usage/general-ledger/faq/solution-gl-report-ref1-as-new/4.png)

### Budget Management

#### Budget Setting

1. Go to **GL** → **Maintain Budget**.

    ![45](../../../static/img/usage/general-ledger/faq/maintain-budget/1.png)

2. Select the **Year**.
3. Choose a **Project Code** or select 'Non Project'.
4. Click **Edit**.
5. Enter monthly budget amounts; quarterly, half-yearly, and yearly totals will update automatically.
6. Enter budgets by account code.
7. Click **Save**.

    ![46](../../../static/img/usage/general-ledger/faq/maintain-budget/2.png)

#### Profit & Loss Statement with Budget

You can compare actuals against monthly or yearly budgets using various report formats:

- This Month vs. Monthly Budget
- This Year vs. Yearly Budget
- This Year vs. Last Year Budget

    ![47](../../../static/img/usage/general-ledger/faq/maintain-budget/3.png)

#### Balance Sheet Statement with Budget

Similar to the P&L, the Balance Sheet supports budget comparisons:

- This Month vs. Monthly Budget
- This Year vs. Yearly Budget

    ![48](../../../static/img/usage/general-ledger/faq/maintain-budget/4.png)

### Withholding Tax

#### Setup Withholding Tax Account

Go to **GL** → **Maintain Account**. Create a **Withholding Tax Payable** account under **Current Liabilities**.

| GL Account | Description | Remark |
| :--- | :--- | :--- |
| 460-XXX | Withholding Tax Payable | Under Current Liabilities |

#### Maintain Withholding Tax Codes

Go to **Tools** → **Maintain Withholding Tax**.

1. Click **New**.
2. Enter the following details:
   - **Code:** e.g., WTH-TAX15
   - **Description:** e.g., Withholding Tax 15%
   - **Tax Rate:** 15%
   - **Tax Account (DR):** Leave blank to follow document accounts.
   - **Tax Account (CR):** Select the **Withholding Tax Payable** account.

    ![68](../../../static/img/usage/general-ledger/faq/witholding-tax/1.png)

3. Click **Save**.

#### Withholding Tax Purchase Entry

Available in **Purchase Invoice**, **Cash Purchase**, **Purchase Debit Note**, and **Purchase Returned**.

1. In the document entry, insert the following columns:
   - WH Local Tax Amt
   - WH Tax
   - WH Tax Rate

    ![69](../../../static/img/usage/general-ledger/faq/witholding-tax/2.png)

2. Select the **WH Tax** code.

    ![70](../../../static/img/usage/general-ledger/faq/witholding-tax/3.png)

3. The system will automatically post the double entry. Press **Ctrl + O** to verify.

    | GL Description | Local DR | Local CR |
    | :--- | :--- | :--- |
    | Expenses Account | XXX | |
    | Withholding Tax Payable | | XXX |

    ![71](../../../static/img/usage/general-ledger/faq/witholding-tax/4.png)

:::note
The withholding tax amount is not added to the purchase invoice total.
:::

#### Payment of Withholding Tax

1. Go to **GL** → **Cash Book Entry**.
2. Create a **New PV**.
3. Enter the Payee and select the bank account.
4. In the detail grid, select the **Withholding Tax Payable** account.
5. Enter the amount and click **Save**.

    ![72](../../../static/img/usage/general-ledger/faq/witholding-tax/5.png)

6. Check the ledger report for the outstanding balance of **Withholding Tax Payable**.
