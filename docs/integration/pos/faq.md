---
sidebar_position: 11
title: FAQ
description: SQL POS frequently-asked questions
slug: /integration/pos/faq
tags: ["FAQ", "POS"]
---
## General

### Backup Error: C:\itUnicode\SQL-POS\SQL-POS-0001.fdb could not be read

- shut down IT Sync before Backup. This is because IT Sync is running behind

### Error When install SQL POS: Must specify additional Parameter

![1](../../../static/img/integration/pos/qna/installation-error.png)

**Solution:**

    - **If New Installation:**

![2](../../../static/img/integration/pos/qna/new-installation.png)

    ```
    1. Delete all the Item from `C:\itUnicode`
    2. Control Panel → Uninstall SQL-POS
    ```

- **If already have transactions:**

    ![3](../../../static/img/integration/pos/qna/new-installation1.png)

    1. Backup SQL POS first
    2. Delete all the Item from `C:\itUnicode`
    3. Control Panel → Uninstall SQL-POS

### Error Message: (Warning: Assigned Printer does not exist: Print to PDF (Mac Desktop))

    ![11](../../../static/img/integration/pos/qna/printer-not-exist.png)

Solution:

1. **Testing Database only** - Delete whole ITUnicode database
2. **Real Database** – May request backup from user upload to us to check (suspect file corrupted)

### Error Message: Failed to Set Connection

![13](../../../static/img/integration/pos/qna/failed-to-set-error.png)

**Solution:**

- Make sure SQL Account version is 759 & above

### Error Message: Failed to Set (Configure SQL POS branch)

1. Configure and make sure SQL Account able to run firebird test successfully

2. Add 3050

3. In SQL POS:

![23](../../../static/img/integration/pos/qna/set-branch-pos.png)

- Put in DNS Number
- Unticked **DisableChkPing**
- Click on "Ping" button to run a ping test, 0% lost means it is connected fine

### Error Message: File in use when design barcode report

![16](../../../static/img/integration/pos/qna/file-in-use-error.png)

- Try Exit the program and logon
- Delete this report and design again

### How to Print Receipt with Chinese word?

- Reason: Windows Non-Unicode program language is set to Chinese

Solution :

- Control Panel → Regional → Language for Non Unicode → Set to English (United States)

    ![6](../../../static/img/integration/pos/qna/print-receipt-chinese-word.png)

- Font change to Arial

1. Click on Design report

    ![7](../../../static/img/integration/pos/qna/print-receipt-chinese-word1.png)

2. Click on Modify

    ![8](../../../static/img/integration/pos/qna/print-receipt-chinese-word2.png)

3. Click on Description Text Object → Menu select Format → Font

    ![9](../../../static/img/integration/pos/qna/print-receipt-chinese-word3.png)

4. Change to Arial

    ![10](../../../static/img/integration/pos/qna/print-receipt-chinese-word4.png)

5. Save the report

### How to resolve when facing network failed error?

1. Make sure Firebird is installed
2. In SQL Account, make sure to set to **Firebird Server** if **Run this POS when call from SQLAcc** setting is ticked

### What are the side effects if you are using Offline Mode?

- You will not be able to capture live Master Transaction from SQL Account Master Data.

### Why unable to get the UTD QTY in SQL POS even though Each Bill(Real Time)?

- In Setting → SQL Account → Need to ticked Run This POS When call from SQLAcc

    ![4](../../../static/img/integration/pos/qna/unable-get-utd-qty.png)

### Why unable to find the Product Code when the Stock Item Code contains Chinese word?

- Stock Item Code supports alphanumeric characters only.
- SQL POS does not support Unicode on Stock Item Code, may key in the Chinese Word in Item Description.

### Previously using IT Uni POS, how should I integrate with SQL?

#### 1. SQL POS (v316) → FoxPro

1. In SQL Account → Click on SQL POS(to generate New POS Database)

2. In SQLPOS→ Setting → System Tab → Tools → Select UniPos Migration →

    ![5](../../../static/img/integration/pos/qna/integrate-it-uni-pos.png)

    1. Import From: `C:\user\public\itposdata` or `C:\user\public\unipos`

    2. Ticked all the Setting

    3. Click on Migrate

#### 2. SQL POS (v333) → Firebird Database

In SQL POS System → Double click SQL POS → Logon Screen → Right Click
Restore Database

### Unable to capture correct price Tag Price

Assigned price tag for item A and Item B, how come only first Item A will capture price tag
price, but second item B ref price?

Solution:

Setting → SQL Account → Ticked Unlink SQL Accounting when available

![12](../../../static/img/integration/pos/qna/printer-not-exist-solution.png)

### What is Price Set in Stock Item?

- Multiple price set in Maintain Stock Item, user allow to set multiple price with comma.

- Example :
  - Price 1 : RM 10.
  - Price 2 : RM 15.
  - Price 3 : RM 20.

    ![14](../../../static/img/integration/pos/qna/price-set.png)

- When select itemcode RED BEAN 500G, auto prompt the price for user to select

    ![15](../../../static/img/integration/pos/qna/price-set1.png)

### What to do if I want to print Barcode Label with Chinese Company Name?

- Save as JPEG, then load the picture into Foxit Design

### Why Close Counter Collect Payment Type does not match with Payment Method in Bills?

![17](../../../static/img/integration/pos/qna/payment-type-not-match.png)

- Collect Payment Summary Payment Type is group by Account Code, may verify whether the payment method is using same account code

:::info
Steps to verify which account a payment method has been posted to

- Setting → POS Screen → Payment Method → Double click on the Payment Name

:::

### Why in Setting Receipt & License Retrieve From SQL button is missing?

![18](../../../static/img/integration/pos/qna/receipt-license-retrieve-button-missing.png)

- After registered license, the button will be disabled.

### Why is printed receipt split across multiple pages?

![19](../../../static/img/integration/pos/qna/receipt-auto-cut.png)

**Solution:**

- Upgrade software to v334 and above
- After the design, the paper size on some printers changed incorrectly and needs to be tweaked again.

**Step to Tweak:**

- Navigate to Print Receipt → Follow the steps below:

![20](../../../static/img/integration/pos/qna/receipt-auto-cut-solution.png)

### When keying in Daily Cash Sales No, it prompts "The Control is Read Only"

![21](../../../static/img/integration/pos/qna/unable-key-in-daily-cash-sales.png)

**Answer:**

- The control is enforced by license, to activate, request new license key by sending the email.

### Why receipt format editor unable to show Chinese word correctly

1. Navigate to Menu Screen → Select **Print Receipt**

2. Click on **Modify**

3. Select the **Report Name** → Click on **Modify**

4. Double click on the object to show in Chinese

    ![22](../../../static/img/integration/pos/qna/unable-show-chinese-word.png)

:::caution
After Fill in \<UTF-8\> , remember to save the report.
:::

### Fail to assign Printer

![24](../../../static/img/integration/pos/qna/fail-assign-printer.png)

**Solution :**

1. Check in **Setting** → **Device** → Receipt Printer → assigned valid Receipt Printer
    **A4 Printer** Normally use EPSON LQ-310 or other laser printer → Assigned
    valid Laser Printer

2. Check Report Format and assigned to a valid printer

3. Window XP → Upgrade to Window 7 & Above

### How to disable receipt preview when done payment?

![25](../../../static/img/integration/pos/qna/disable-preview-receipt.png)

Solution:

- Navigate to SQL POS **Setting** → **Receipt & License** Tab → **No Copy of Receipt** set to **0**

### How to disable user from returning stock?

Navigate to Maintain User → Refund Item

![26](../../../static/img/integration/pos/qna/disallow-user-return-stock.png)

:::note
Set to Yes, user **allow** to return stock with input quantity - 1

Set to No, user **not allow** to have negative stock
:::

### How to un-closed counter?

➔ Close Counter → Right click un-closed counter

### Unable to Sent Email from Gmail

![27](../../../static/img/integration/pos/qna/unable-sent-email.png)

**Solution:**

1. Follow this [Google Account Security page](https://myaccount.google.com/security)

2. Click on **Less Secure App Access**

    ![28](../../../static/img/integration/pos/qna/unable-sent-email-solution.png)

3. Turn on the switch

    ![29](../../../static/img/integration/pos/qna/unable-sent-email-solution1.png)

### Post to SQL Account raise error (Failed to Post Payment of 02/6/2020 OLED IDispatch exception code 0 from : knockoff amount (0.00) must not exceed outstanding amount (321.6))

![30](../../../static/img/integration/pos/qna/fail-post-payment.png)

**Solution:**

1. Use SQL Pos v340 & Above

2. Navigate to SQL POS Setting → SQL Account → Ticked **Direct write to SQLAcc** & try to post again

## SQL POS F&B

### Error Message: Counter is closed, wait for Main Counter to open

    ![31](../../../static/img/integration/pos/qna/counter-closed.png)

- This error message indicates that when multiple POS units are linked together, the Main Counter must be opened first.
