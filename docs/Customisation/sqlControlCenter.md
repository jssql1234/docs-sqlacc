---
title: SQL Control Center
description: Customisations in SQL Control Center
slug: /Customisation/sqlControlCenter
tags: ["SQL Account"]
---

## Shipping/Forwarding

This Customisation is the simple calculation for the Shipping/Forwarding company.

[Sample Database](https://download.sql.com.my/customer/Fairy/ACC%20BK-%5bShipping%5d.zip)

[Video](https://www.youtube.com/watch?v=LPoz1h3hyvQ)

### History New/Updates/Changes

14 May 2025

* Use Maintain Currency for Currency Symbol & Currency Rate for detail UDF
05 Feb 2016

* Fixed TaxInvoice-Fowarding2 batch print Tax summary mixing together
* Fixed Quotation & Debit Note OnBeforeSave Script Seq not correct.
04 Jan 2016

* Fixed TaxInvoice-Fowarding2 Title missing Tax word

07 Dec 2015

Fixed 0Sales Local - Invoice Listing - Level 1 Ent column some shown empty when 0.
02 Nov 2015

* Fix Seq Error
* Fix TaxInvoice-Fowarding2 format show A instead Tax Rate

20 Oct 2015

* Fix Transfer Document TaxAmt calculate incorrectly if using UDF_ExRate \<> 1
* Fix Partial Transfer Qty TaxAmt calculate incorrectly

19 Oct 2015

* Fix upgrade to Version 721 error.
* Fix Transfer Document TaxAmt calculate incorrectly

14 Oct 2015

* Fix 0Sales Local - Invoice Listing - Level 1 margin not correct
* Convert DocRef3 to UDF_EntCost for 0Sales Local - Invoice Listing - Level 1 Ent column

### Settings

#### Maintain User

*Menu: Tools | Maintain User...*

Untick the Access Right for Prompt Replace Unit Price Dialog under the Group : Sales

### Steps

#### Invoice

*Menu: Sales | Invoice...*

[ch366](../../static/img/getting-started/user-guide/ch366.jpg)

1. Select Customer Code
2. Select Item Code
3. Enter the Cost incurred for the selected item code (for the Profit & Loss By Document report)
4. Enter Qty
5. Enter UnitPrice
6. Enter Exchange Rate (if have)
7. Click More tab to enter extra/others Information

[ch367](../../static/img/getting-started/user-guide/ch367.jpg)

#### Profit & Loss By Document

*Menu: Sales | Print Sales Document Listing...*

[ch368](../../static/img/getting-started/user-guide/ch368.jpg)

1. Select Invoice Listing & Range Date
2. Tick Group by Customer Code
3. Click Apply
4. Press F6 to preview
5. Select report name 0Sales Local - Invoice Listing - Level 1
6. Click Ok button


## Bonus Point System 

This Customisation is to calculate/maintain the Point/Bonus

- Pros
    * Able to set Claim Rate (i.e. 1 Point = How many RM eg 1 Point = RM0.01 so enter as 0.01)
    * Able to set Point Rate by item code (i.e. RM1 = How many point eg RM1 = 1 so enter as 1)
    * Point Rate can be calculate by Amount and/or Qty
    * Able to Claim like Voucher as Discount
    * Able to Claim Item
    * Claim Point Rate can be change runtime

- Cons
    * Unable to handle the cancel & Delete Invoice - Manually deduct the point using Update Button on Extra DO
    * If the customer no transaction within the month it unable to Generate Statement
    *  No Auto Deduct Expiry Point - manually deduct the point using Update Button on Extra DO
    * Able to handle 2 decimal Point only
    * Batch Insert no checking (i.e. User may over deduct the point)
    * User had to manually Adjust for Opening after the Year End Purging had done.

[Sample Database](https://www.sql.com.my/document/ACC%20BK-%5BBonusVoucherPoint%5D.zip)

### History New/Updates/Changes

25 Dec 2015

* Enable Support GST Version
* Add UnClaim Voucher Listing report
* Add Bonus-Sales Invoice 7 (GST 2) report
* Fix Bonus Statement show $ symbol
* Remove auto 5 cents rounding script

### Modules Required

* DIY Field
* DIY Script
* Invoice ----> DO
* Multiple Document Number Set

### Settings

#### Maintain User

*Menu: Tools | Maintain User...*

Untick the Access Right for Prompt Replace Unit Price Dialog under the Group : Sales

#### Maintain Item

*Menu: Stock | Maintain Stock Item...*

[ch369](../../static/img/getting-started/user-guide/ch369.jpg)

1. Item Code to be create - Voucher => For Claim use (eg 1 point = RM 0.01)

[ch370](../../static/img/getting-started/user-guide/ch370.jpg)

2. For each item code enter the Voucher Rate (eg 0.5 point = RM 1)

#### Sales Invoice

*Menu: Sales | Invoice...*

    This applicable also at Sales Debit Note, Sales Cash Sales & Sales Credit Note

| **UDF Field**      | **Description**                                                                 |
|---------------------|---------------------------------------------------------------------------------|
| **UDF_VoucherNo**  | Enter the Voucher Number (Extra DO DocNo). Amount will be based on the Extra DO DocAmt. Not applicable for Sales Credit Note. |
| **UDF_VoucherRate**| From maintain item. User can still adjust the rate if needed.                    |
| **UDF_UseQty**     | **Tick** → `UDF_Voucher = UDF_VoucherRate * Qty`. **UnTick** → `UDF_Voucher = UDF_VoucherRate * Amount`. |
| **UDF_Voucher**    | `Total current item point`.                                                      |

#### Extra Delivery Order

*Menu: Sales | Extra Delivery Order...*

    This is the center or Ledger for all Point IN & OUT.

[ch371](../../static/img/getting-started/user-guide/ch371.jpg)

| **Field**       | **Description**                                                                 |
|------------------|---------------------------------------------------------------------------------|
| **DocNo**       | `CRP-XXXXX` → Claim/Deduct Transactions Point. `VOC-XXXXX` → In/Add Transactions Point. |
| **DocNoEx**     | Source document number from which this document is generated.                    |
| **DocRef1**     | Indicates which `VOC-XXXXX` is used for Claim/Deduct Point.                      |
| **DocAmt**      | Total point for each transaction.                                                |
| **UDF_CRPoint** | **Tick** → Claim/Deduct Transactions Point. **UnTick** → In/Add Transactions Point. |

### Steps

#### Sales Invoice

Below is example in Sales Invoice with Voucher Claim
*Menu: Sales | Invoice...*

[ch372](../../static/img/getting-started/user-guide/ch372.jpg)

1. Enter all Information (eg Company Code, Date, ItemCode, etc) as norm for Normal Sales (i.e. Add Point).
2. Select itemcode Voucher.
3. Enter the Voucher Number.
4. Save.

:::success If no Voucher is use (i.e. Just deduct/redeem either fully/partly by Point)
* Just enter the UDF_VoucherRate as - (Negative Value) after enter the Negative UnitPrice
:::

#### Extra Delivery Order

*Menu: Sales | Extra Delivery Order...*

In here user can do adjustment for the point for each Customer.
1. Click Update Button

[ch372](../../static/img/getting-started/user-guide/ch372.jpg)

2. Untick this if you wanted to Add the point
3. Enter the Point to Add/Reduce.
4. Click Post Button

#### Extra Delivery Order Listing
*Menu: Sales | Print Sales Document Listing...*

    Here is for user to print the Bonus Statement or UnClaim Voucher Listing report

[ch373](../../static/img/getting-started/user-guide/ch373.jpg)

1. Select Extra Delivery Order Listing & Range Date
2. Tick Customer Code
3. Click Apply button
4. Press F6 to preview
5. Select report name Bonus Statement or UnClaim Voucher Listing
6. Click Ok button

## Branch Control 

Branch Control Setting is done to prevent branch user from selecting Customer, Project, Stock Item or Location info that is not relevant to them.

### Restricted for

* Branch user only allows to select their own customer
* Preset default Agent, Project, Item Code, Location code for each branch user
*  Reports only shows transactions issued by the branch user
* Filter reports only using information assigned to the branch user
* Generate accurate P&L, Stock Balance Report for branches

### Modules Required

* DIY Field
* DIY Script

## Branch Control Module **Features**

### Project & Location

- Authorising each branch users to have the accessibility to their respective branch, SQL will automatically assign transactions created by the user to a specific branch to prevent human mistakes. Account entries, stock warehouse will automatically be posted to the appropriate branch.

[ch374](../../static/img/getting-started/user-guide/ch374.png)

### Customer List

- The user can only select/access the customer information for the own branch and is not permitted to post transactions for any other branch. You can avoid information being shared to other branches at data entry staff’s level.

[ch375](../../static/img/getting-started/user-guide/ch375.png)

### Agent / Area List

- Automatically set the default agent/area code based on user login to ease the user's instead of requiring manual selection.

[ch376](../../static/img/getting-started/user-guide/ch376.png)

### Stock Item List

- The user only able to select the list of item code belong to their branch.

[ch377](../../static/img/getting-started/user-guide/ch377.png)

### Payment Method

- Restrict payment methods for each branch to prevent human error and posting to unnecessary accounts.

[ch378](../../static/img/getting-started/user-guide/ch378.png)

### Reporting

- Stay on top of your financial and operational transactions across all your branches with SQL. You can monitor all transactions happening in each branch. with this information, you can identify which branch is the most profitable and which branch that needs to monitor closely.

[ch379](../../static/img/getting-started/user-guide/ch379.png)

### Profit & Loss Project

- By consolidating headquarter accounts with branch accounts, SQL allows for the viewing of consolidated balance sheets, profit and loss accounts by authorised users to evaluate the company’s overall performance. Bosses are able to drill down to the transactions of each branch individually.

[ch380](../../static/img/getting-started/user-guide/ch380.png)

## One Time Setting

*Menu: Tools | Maintain User...*

[ch381](../../static/img/getting-started/user-guide/ch381.jpg)

Here are the guidelines to set **Branch Control Setting**
1. **MUST** Logon as **ADMIN** account
2. Choose for the sub account, e.g. Yuki agent account
3. Go to **Access Right for Branch Control** tab
4. Choose the **Branch Control Settings** tab you need

### Sales

1. Tick Lock Customer
2. If want filter customers by :

| **Filter By**       | **Number** |
|----------------------|------------|
| Area                | 1          |
| Agent               | 2          |
| Company Category    | 3          |

The setting can only function within the range of **1 to 3**.

3. Enter the Area code for Area in Allowable List, you are allow to enter more than 1 area codes.
4. If want search customer by

| **Search By**     | **Number** |
|-------------------|------------|
| Code              | 1          |
| Company Name      | 2          |
| Company Name 2    | 3          |
| Currency Code     | 4          |

The setting can only function within the range of **1 to 4**.

:::note E.g.
Tick the **Lock Customer** Option and filtered customer list by area, enter as 1 in Filter Customers by. Enter Area code such as KL, JB, and SG in the allowable list column. User prefer to search for Customer Code, enter as 1 if would like to search Customer Column.
:::

[ch382](../../static/img/getting-started/user-guide/ch382.jpg)

### Purchase

1. Tick Lock Supplier
2. If want filter suppliers by

| **Filter By**        | **Number** |
|-----------------------|------------|
| Area                  | 1          |
| Agent                 | 2          |
| Company Category      | 3          |

The setting can only function within the range of **1 to 3**.

3. Enter the Agent code for Agent in **Allowable List**, you are allow to enter more than 1 agent codes.
4. If want search supplier by :

| **Search By**     | **Number** |
|-------------------|------------|
| Code              | 1          |
| Company Name      | 2          |
| Company Name 2    | 3          |
| Currency Code     | 4          |

The setting can only function within the range of **1 to 4**.

:::note E.g.
Tick the Lock Supplier option and filter supplier list by agent, enter as 2 in Filter Suppliers by. Enter Agent code, such as YUKI, in the allowable list column, and user prefer to search for supplier code, enter as 1 in Search Supplier Column.
:::

[ch383](../../static/img/getting-started/user-guide/ch383.jpg)

### Item Code

1. Tick Lock Item Code
2. If want filter stock item by

| **Filter By**  | **Number** |
|----------------|------------|
| Stock Group    | 1          |
| Category       | 2          |
| Item Code      | 3          |

The setting can only function within the range of **1 to 3**.

3. Enter the item code for Item Code in **Allowable Item Code**, you are allow to enter more than 1 item codes.
4. If want search item code by

| **Search By**   | **Number** |
|-----------------|------------|
| Item Code       | 1          |
| Description     | 2          |
| Description 2   | 3          |

The setting can only function within the range of **1 to 3**.

:::note E.g. 
Tick the Lock Item Code option and filter by item code. Enter item codes, such as BOM-02/Red, ER/Lamp, and ISCT, in the column, and search for item descriptions by item code.
:::

[ch384](../../static/img/getting-started/user-guide/ch384.jpg)

### General Setting

1. Tick Lock Project if you need to lock the project code
2. Tick if want search by Project Code, unticked will search by Project Description.
3. Enter the code for Project Code in Allowable ... columns, you are allow to enter more than 1 codes for Project Code
4. Repeat Step 1 to Step 3 for the remaining settings.

:::note E.g. 
Tick the Lock Project option. Tick IsSearchProjectCode to allow searching by project code, and enter project codes, such as P1 and P2, in the column for search.
:::

[ch385](../../static/img/getting-started/user-guide/ch385.jpg)