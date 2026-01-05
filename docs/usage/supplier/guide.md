---
sidebar_position: 1
title: Guide
description: Basic Supplier Setup
slug: /usage/supplier/guide
tags: ["SQL Account", "Usage", "Supplier"]
---

## Maintain Supplier

Maintain supplier profile data such as addresses, phone numbers, fax, email, contact persons, credit limits, credit
terms, etc. In other words, this is your supplier contact list.

![des-maintain-supplier-1](../../../static/img/usage/supplier/guide/maintain-supplier-1.jpg)

### New Supplier

To create a new supplier, click the **New** button. See the screenshot below.

![des-maintain-supplier-new-supplier-1](../../../static/img/usage/supplier/guide/maintain-supplier-new-supplier-1.jpg)

You will get a blank form to be filled in with the supplier data.

![des-maintain-supplier-new-supplier-2](../../../static/img/usage/supplier/guide/maintain-supplier-new-supplier-2.jpg)

You can start entering data into the following fields:

| **Field Name**                | **Field Type**                                                         | **Length** | **Explanation**                                                                                               |
| ----------------------------- | ---------------------------------------------------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------- |
| Company                       | Alphanumerical                                                         | 100        | Input the supplier billing company name.                                                                      |
| Control A/c                   | Lookup from Maintain Accounts (Special Type: Supplier Control Account) | 10         | Select an appropriate Supplier Control Account to be posted to GL when supplier documents are created.        |
| Description 2 (under Company) | Alphanumerical                                                         | 100        | An optional field where you can enter Chinese translated name, former company name, company register no, etc. |
| Code                          | Alphanumerical                                                         | 10         | Automatically or manually generate the Supplier Code.                                                         |
| Cust Category                 | Lookup from Maintain Company Category                                  | 15         | Categorize your supplier for reporting purposes.                                                              |

#### General

![des-maintain-supplier-general-1](../../../static/img/usage/supplier/guide/maintain-supplier-general-1.jpg)

| **Field Name**    | **Field Type**                       | **Length**     | **Explanation**                                                                                                |
| ----------------- | ------------------------------------ | -------------- | -------------------------------------------------------------------------------------------------------------- |
| Branch Name       | Alphanumerical                       | 100            | You can maintain multiple sets of addresses by using different Branch Names.<br />Default Branch Name: BILLING |
| Address (4 lines) | Alphanumerical                       | 40 (each line) | Enter the company addresses.                                                                                   |
| Attention         | Alphanumerical                       | 70             | Enter the contact person's name.                                                                               |
| Phone 1 & 2       | Alphanumerical                       | 30             | Enter the telephone number.                                                                                    |
| Fax 1 & 2         | Alphanumerical                       | 30             | Enter the fax number.                                                                                          |
| Email             | Alphanumerical                       | 60             | Enter the email address.                                                                                       |
| Area              | Lookup from Maintain Area            | 10             | Select a default Area.                                                                                         |
| Agent             | Lookup from Maintain Agent           | 10             | Select a default Agent.                                                                                        |
| Currency          | Lookup from Maintain Currency        | 6              | Select a default Currency.                                                                                     |
| Credit Terms      | Lookup from Maintain Terms           | 10             | Select a default Terms.                                                                                        |
| Credit Limit      | Numeric                              | —              | Set the credit limit.                                                                                          |
| Statement         | Option                               | —              | Select a default statement type, e.g., Open Item or Brought Forward. <br />Default: Open Item                  |
| Aging On          | Option                               | —              | Select a default Aging type, e.g., Invoice Date or Due Date. Default: Invoice Date                             |
| Price Tag         | Lookup from Maintain Stock Price Tag | 10             | Set the price tag for the items.                                                                               |

#### Note

![des-maintain-supplier-note-1](../../../static/img/usage/supplier/guide/maintain-supplier-note-1.jpg)

| **Field Name**    | **Field Type** | **Length** | **Explanation**                                                                              |
| ----------------- | -------------- | ---------- | -------------------------------------------------------------------------------------------- |
| Account Open Date | Date           | —          | Creation date.                                                                               |
| Remark            | Alphanumerical | 80         | This remark will show in Inquiry → Account Inquiry.                                          |
| Biz Nature        | Alphanumerical | 100        | Enter the supplier's business nature. For example, Chemical Manufacturing, Car Service, etc. |
| Note              | Alphanumerical | Rich Text  | Record the supplier knowledge base. You can use the "Date Stamp".                            |
| Status            | Option         | —          | See **Status Options** table below.                                                          |

| **Status** | **Explanation**                                                                                   |
| ---------- | ------------------------------------------------------------------------------------------------- |
| Active     | Allows the creation of official documents and selection to print Supplier Statement.              |
| Inactive   | Does not allow the creation of official documents, and cannot select to print Supplier Statement. |
| Suspend    | Does not allow the creation of official documents, but can select to print Supplier Statement.    |
| Prospect   | Allows the creation of official documents and selection to print Supplier Statement.              |
| Pending    | Allows the creation of official documents and selection to print Supplier Statement.              |

#### Tax

![des-maintain-supplier-tax-1](../../../static/img/usage/supplier/guide/maintain-supplier-tax-1.jpg)

| **Field Name** | **Explanation & Properties**                                  |
| -------------- | ------------------------------------------------------------- |
| Default Tax    | Select a default tax code based on supplier.                  |
| Tax Area       | Not applicable to Malaysia/Singapore.                         |
| Exemption No   | • Input the Tax Exemption number applicable to your supplier. |
|                | • Field type: Alphanumerical.                                 |
|                | • Length: 50                                                  |
| Expiry Date    | Set an expiry date.                                           |
|                | • This will be tax exempted before the expiry date.           |
|                | • Field type: Date.                                           |

**Tariff Code Setting**
This setting set the supplier who has supply the taxable goods under the Sales Tax (Person Exempted from Payment of Tax) Order 2018.

| **Field Name** | **Explanation & Properties**                                                                                               |
| -------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Tariff         | • Add tariff code of taxable goods to be sold in exemption.                                                                |
|                | • Lookup: [Maintain Tariff](../../usage/tools/guide#maintain-tariff)                                                       |
|                | • Related Topic: [Maintain Stock Item → Main Header](../../usage/stock/guide#maintain-stock-item)                    |
| Tax            | • Select an appropriate tax code that falls under the Person Exempted in **Schedule C ONLY** (must be declared in SST-02). |
|                | • Schedule C tax code: PEC1, PEC2, PEC3, PEC4, PEC5                                                                        |
|                | • Lookup: [Maintain Tax](../../usage/gst/gst-maintain-tax.md)                                                         |

#### Bank Account

![des-maintain-supplier-bank-account-1](../../../static/img/usage/supplier/guide/maintain-supplier-bank-account-1.jpg)

| **Field Name** | **Explanation & Properties**         |
| -------------- | ------------------------------------ |
| Bank           | Select the correct bank.             |
| Account No     | Enter the supplier's account number. |
| Account Name   | Enter the name.                      |
| ID Type        | Select the desired ID type.          |
| ID             | Enter the ID.                        |
| Active         | • Check this box if active.          |
|                | • Uncheck this box if inactive.      |

### Edit Supplier

To edit a supplier, click the EDIT button. See the screenshot below.

![des-maintain-supplier-edit-supplier-1](../../../static/img/usage/supplier/guide/maintain-supplier-edit-supplier-1.jpg)

:::note

1. Users can edit supplier data depending on the access rights granted.
2. All edits are audited and logged by the system.

:::

### Save Supplier

You must save the supplier data before it can be used. See the screenshot below.

![des-maintain-supplier-save-supplier-1](../../../static/img/usage/supplier/guide/maintain-supplier-save-supplier-1.jpg)

### Delete Supplier

You can delete unwanted supplier data. See the screenshot below.

![des-maintain-supplier-delete-supplier-1](../../../static/img/usage/supplier/guide/maintain-supplier-delete-supplier-1.jpg)

:::note

1. Users can delete supplier data depending on the access rights granted.

:::

### Supplier Code Format

The supplier code can be automatically generated or manually overwritten. See the screenshot below.

![des-maintain-supplier-supplier-code-format-1](../../../static/img/usage/supplier/guide/maintain-supplier-supplier-code-format-1.jpg)

:::note Important

1. Every supplier code is unique.
2. If a duplicate code is detected during saving, a warning message will be displayed.

:::

You can set the supplier code format via Tools | Options...(Supplier). See the screenshot below.

![des-maintain-supplier-supplier-code-format-2](../../../static/img/usage/supplier/guide/maintain-supplier-supplier-code-format-2.jpg)

Explanation of the Supplier Code Format:

![des-maintain-supplier-supplier-code-format-3](../../../static/img/usage/supplier/guide/maintain-supplier-supplier-code-format-3.jpg)

For example,

| **Company Name** | **Customer Control Acc** | **Format**    | **Result**     |
| ---------------- | ------------------------ | ------------- | -------------- |
| ABCD SDN BHD     | 401-000                  | %.1s-%.1s%.1d | 4-A-1          |
| ABCD SDN BHD     | 401-000                  | %.2s-%.2s%.2d | 40-AB-01       |
| ABCD SDN BHD     | 401-000                  | %.3s-%.3s%.3d | 401-ABC-001    |
| ABCD SDN BHD     | 401-000                  | %.4s-%.4s%.4d | 401--ABCD-0001 |

## Supplier Invoice (SI)

- General invoices received from suppliers, such as for services, insurance, stationery, or any non-stock control billing.
- Additionally, you can check invoice statuses, including outstanding balances and payment history.

![des-supplier-invoice-1](../../../static/img/usage/supplier/guide/supplier-invoice-1.jpg)

### Basic Entry (SI)

1. Click the **New** button.
2. See the New Supplier Invoice entry form screenshot below.

    ![des-supplier-invoice-entry-1](../../../static/img/usage/supplier/guide/supplier-invoice-entry-1.jpg)

3. Select the Supplier Code. You can directly enter and search by either the supplier code or name.
4. Enter the Purchase Account and the amount to be debited.
5. Below is an example of the entry created:

    ![des-supplier-invoice-entry-2](../../../static/img/usage/supplier/guide/supplier-invoice-entry-2.jpg)

    | Account                  | DR (RM) | CR (RM) |
    | ------------------------ | ------- | ------- |
    | Stationery               | 500.00  |         |
    | Supplier Control Account |         | 500.00  |

### Project (SI)

- There are two types of projects to note:
    1. Document Project
    2. Detail Project
- For document projects, go to the More section on the left sidebar.
- For detail projects, add the project column using the Field Chooser.

![des-supplier-invoice-project-1](../../../static/img/usage/supplier/guide/supplier-invoice-project-1.jpg)

| **Label** | **Types**        | **Explanation**                                                    |
| --------- | ---------------- | ------------------------------------------------------------------ |
| A         | Document Project | It represents the project for a document to be credited.           |
| B         | Detail Project   | It represents the project for individual GL Account to be debited. |

### Attachment (SI)

- Attaching supporting documents to an invoice is very useful.
- This allows you to easily retrieve and refer to the attached files in the future.

![des-supplier-invoice-attachment-1](../../../static/img/usage/supplier/guide/supplier-invoice-attachment-1.jpg)

1. Go to the attachment section.
2. Click the (+) button to insert the file path.
3. See the sample screenshot below.

![des-supplier-invoice-attachment-2](../../../static/img/usage/supplier/guide/supplier-invoice-attachment-2.jpg)

### Note (SI)

1. Click the Note section on the left sidebar.
2. Right-click to open the Rich Text Editor.
3. You can start entering the note. See the example screenshot below.
4. Click the **X** button to save and exit the Rich Text Editor.

    ![des-supplier-invoice-note-1](../../../static/img/usage/supplier/guide/supplier-invoice-note-1.jpg)

5. A "Save changes?" prompt will appear. Click **Yes** to save it.

    ![des-supplier-invoice-note-2](../../../static/img/usage/supplier/guide/supplier-invoice-note-2.jpg)

### Invoice description (SI)

1. This shows the document description in the Supplier Statement, e.g., Purchase-Stationery April 2015.

    ![des-supplier-invoice-invoice-description-1](../../../static/img/usage/supplier/guide/supplier-invoice-invoice-description-1.jpg)

2. Sample of supplier statement screenshot below.

    ![des-supplier-invoice-invoice-description-2](../../../static/img/usage/supplier/guide/supplier-invoice-invoice-description-2.jpg)

## Supplier Payment (SP)

- Record payment amounts to suppliers.
- Offset payments against outstanding supplier invoices.

![des-supplier-payment-1](../../../static/img/usage/supplier/guide/supplier-payment-1.jpg)

### Basic Entry (SP)

1. Click the New button.
2. See the New Supplier Payment entry form screenshot below.

    ![des-supplier-payment-entry-1](../../../static/img/usage/supplier/guide/supplier-payment-entry-1.jpg)

3. Select the Supplier Code. Directly enter and search by either the supplier code or name.
4. Select the Payment Method (bank or cash account) in Payment By.
5. Enter the Paid Amount (following the bank account currency).
6. Below is an example of the entry created:

    ![des-supplier-payment-entry-2](../../../static/img/usage/supplier/guide/supplier-payment-entry-2.jpg)

    **Double Entry will be:-**

    | **Account**          | **DR (RM)** | **CR (RM)** |
    | -------------------- | ----------- | ----------- |
    | Supplier Control Acc | 2,500.00    |             |
    | Bank Account         |             | 2,500.00    |

7. Enter bank charges if applicable.

    ![des-supplier-payment-entry-3](../../../static/img/usage/supplier/guide/supplier-payment-entry-3.jpg)

8. The following double entry will be automatically posted:

    | **Account**  | **DR (RM)** | **CR (RM)** |
    | ------------ | ----------- | ----------- |
    | Bank Charges | 2.00        |             |
    | Bank Account |             | 2.00        |

9. Enter the cheque number, cash, or TT into the Cheque No. field.

    ![des-supplier-payment-entry-4](../../../static/img/usage/supplier/guide/supplier-payment-entry-4.jpg)

### Knock-Off (SP)

Purpose of knocking off invoices:

1. To display outstanding invoices in the Supplier Aging Report.
2. To indicate which invoices the payment offsets in the Supplier Statement.
3. To remove or recover GST Bad Debt Relief for items outstanding for more than six months.

#### Partial Knock-Off (SP)

1. Enter the knock-off amount in the Pay column (it will be automatically checked).
2. The Unapplied Amount will be reduced by the entered knock-off amount.

    ![des-supplier-payment-partial-knockoff-1](../../../static/img/usage/supplier/guide/supplier-payment-partial-knockoff-1.jpg)

#### Document Knock-Off (SP)

1. Check the boxes for the outstanding documents.
2. The Unapplied Amount will be reduced by the total of the selected documents.

    ![des-supplier-payment-document-knockoff-1](../../../static/img/usage/supplier/guide/supplier-payment-document-knockoff-1.jpg)

#### Random Knock-Off (SP)

1. Clicking the Pay column will automatically select the outstanding documents.
2. The Unapplied Amount will be reduced based on the outstanding balance.

    ![des-supplier-payment-random-knockoff-1](../../../static/img/usage/supplier/guide/supplier-payment-random-knockoff-1.jpg)

:::note
The unapplied amount represents the supplier payment that has not yet been allocated or knocked off against outstanding invoices or debit notes.
:::

### Attachment (SP)

- Attaching supporting documents is very useful.
- This allows you to easily retrieve and refer to the attached files in the future.

![des-supplier-payment-attachment-1](../../../static/img/usage/supplier/guide/supplier-payment-attachment-1.jpg)

1. Go to the attachment section.
2. Click the (+) button to insert the file path.
3. See the sample screenshot below.

    ![des-supplier-payment-attachment-2](../../../static/img/usage/supplier/guide/supplier-payment-attachment-2.jpg)

### Note (SP)

1. Click the Note section on the left sidebar.
2. Right-click to open the Rich Text Editor.

    ![des-supplier-payment-note-1](../../../static/img/usage/supplier/guide/supplier-payment-note-1.jpg)

3. You can start entering the note. See the example screenshot below.
4. Click the X button to save and exit the Rich Text Editor.

    ![des-supplier-payment-note-2](../../../static/img/usage/supplier/guide/supplier-payment-note-2.jpg)

5. A "Save changes?" prompt will appear. Click YES to save it.

    ![des-supplier-payment-note-3](../../../static/img/usage/supplier/guide/supplier-payment-note-3.jpg)

### Description (SP)

This shows the supplier payment description in the Supplier Statement, e.g., Payment For Jan & Feb 2016.

![des-supplier-payment-description-1](../../../static/img/usage/supplier/guide/supplier-payment-description-1.jpg)

Sample of Supplier statement screenshot below.

![des-supplier-payment-description-2](../../../static/img/usage/supplier/guide/supplier-payment-description-2.jpg)

## Supplier Debit Note (SDN)

- General debit notes received from suppliers, such as adjustments for undercharged stationery, services, insurance, or any non-stock control billing.
- Additionally, you can check the status of debit notes, including outstanding balances and payment history.

![des-supplier-debit-note-1](../../../static/img/usage/supplier/guide/supplier-debit-note-1.jpg)

### Basic Entry (SDN)

1. Click the New button.
2. See the New Supplier Debit Note entry form screenshot below.

    ![des-supplier-debit-note-entry-1](../../../static/img/usage/supplier/guide/supplier-debit-note-entry-1.jpg)

3. Select the Supplier Code. You can directly enter and search by either the supplier code or name.
4. Enter the Purchase Account and the amount to be debited.
5. Below is an example of the entry created:

    ![des-supplier-debit-note-entry-2](../../../static/img/usage/supplier/guide/supplier-debit-note-entry-2.jpg)

    **Double Entry will be:-**

    | **Account**              | **DR (RM)** | **CR (RM)** |
    | ------------------------ | ----------- | ----------- |
    | Stationery               | 500.00      |             |
    | Supplier Control Account |             | 500.00      |

### Project (SDN)

- There are two types of projects to note:
    1. Document Project
    2. Detail Project
- For document projects, go to the More section on the left sidebar.
- For detail projects, add the project column using the Field Chooser.

![des-supplier-debit-note-project-1](../../../static/img/usage/supplier/guide/supplier-debit-note-project-1.jpg)

| **Label** | **Types**        | **Explanation**                                                    |
| --------- | ---------------- | ------------------------------------------------------------------ |
| A         | Document Project | It represents the project for a document to be credited.           |
| B         | Detail Project   | It represents the project for individual GL Account to be debited. |

### Attachment (SDN)

- Attaching supporting documents to a debit note is very useful.
- This allows you to easily retrieve and refer to the attached files in the future.

![des-supplier-debit-note-attachment-1](../../../static/img/usage/supplier/guide/supplier-debit-note-attachment-1.jpg)

1. Go to the attachment section.
2. Click the **(+)** button to insert the file path.
3. See the sample screenshot below.

    ![des-supplier-debit-note-attachment-2](../../../static/img/usage/supplier/guide/supplier-debit-note-attachment-2.jpg)

### Note (SDN)

1. Click the Note section on the left sidebar.
2. Right-click to open the Rich Text Editor.
3. You can start entering the note. See the example screenshot below.
4. Click the **X** button to save and exit the Rich Text Editor.

    ![des-supplier-debit-note-note-1](../../../static/img/usage/supplier/guide/supplier-debit-note-note-1.jpg)

5. A "Save changes?" prompt will appear. Click Yes to save it.

    ![des-supplier-debit-note-note-2](../../../static/img/usage/supplier/guide/supplier-debit-note-note-2.jpg)

### D/N Description (SDN)

1. This shows the document description in the Supplier Statement, e.g., Undercharged-Stationery April 2015.

    ![des-supplier-debit-note-dn-description-1](../../../static/img/usage/supplier/guide/supplier-debit-note-dn-description-1.jpg)

2. Sample of supplier statement screenshot below.

    ![des-supplier-debit-note-dn-description-2](../../../static/img/usage/supplier/guide/supplier-debit-note-dn-description-2.jpg)

## Supplier Credit Note (SCN)

- Credit notes are used to reduce and offset outstanding invoices or debit notes.
- For credit notes created in the Purchase module, you must offset them against outstanding invoices or debit notes here.
- You can check for any unapplied amounts on a credit note. An unapplied amount means the credit note must be matched with an invoice or debit note to be knocked off.

![des-supplier-credit-note-1](../../../static/img/usage/supplier/guide/supplier-credit-note-1.jpg)

### Basic Entry (SCN)

1. Click the New button.
2. See the New Supplier Credit Note entry form screenshot below.

    ![des-supplier-credit-note-entry-1](../../../static/img/usage/supplier/guide/supplier-credit-note-entry-1.jpg)

3. Select the Supplier Code. You can directly enter and search by either the supplier code or name.
4. Enter the Purchase Account and the amount to be credited.
5. Below is an example of the entry created:

    ![des-supplier-credit-note-entry-2](../../../static/img/usage/supplier/guide/supplier-credit-note-entry-2.jpg)

    **Double Entry will be:-**

    | **Account**          | **DR (RM)** | **CR (RM)** |
    | -------------------- | ----------- | ----------- |
    | Supplier Control Acc | 500.00      |             |
    | Purchase Returns     |             | 500.00      |

### Unapplied Amount (SCN)

- The unapplied amount represents the credit note amount that has not been allocated or knocked off against outstanding invoices or debit notes.
- It will remain in the Supplier Aging Report as a negative amount (-).

![des-supplier-credit-note-unapplied-amount-1](../../../static/img/usage/supplier/guide/supplier-credit-note-unapplied-amount-1.jpg)

### Knock-Off Outstanding (SCN)

- To knock off an outstanding invoice or debit note, check the box next to the Pay column.
- You can directly enter the payment amount in the Pay column.

![des-supplier-credit-note-knockoff-outstanding-1](../../../static/img/usage/supplier/guide/supplier-credit-note-knockoff-outstanding-1.jpg)

### Project (SCN)

- There are two types of projects to note:
    1. Document Project
    2. Detail Project
- For document projects, go to the More section on the left sidebar.
- For detail projects, add the project column using the Field Chooser.

![des-supplier-credit-note-project-1](../../../static/img/usage/supplier/guide/supplier-credit-note-project-1.jpg)

| **Label** | **Types**        | **Explanation**                                                     |
| --------- | ---------------- | ------------------------------------------------------------------- |
| A         | Document Project | It represents the project for a document to be debited.             |
| B         | Detail Project   | It represents the project for individual GL Account to be credited. |

### Attachment (SCN)

- Attaching supporting documents to a credit note is very useful.
- This allows you to easily retrieve and refer to the attached files in the future.

![des-supplier-credit-note-attachment-1](../../../static/img/usage/supplier/guide/supplier-credit-note-attachment-1.jpg)

1. Go to the attachment section.
2. Click the (+) button to insert the file path.
3. See the sample screenshot below.

    ![des-supplier-credit-note-attachment-2](../../../static/img/usage/supplier/guide/supplier-credit-note-attachment-2.jpg)

### Note (SCN)

1. Click the Note section on the left sidebar.
2. Right-click to open the Rich Text Editor.
3. You can start entering the note. See the example screenshot below.
4. Click the **X** button to save and exit the Rich Text Editor.

    ![des-supplier-credit-note-note-1](../../../static/img/usage/supplier/guide/supplier-credit-note-note-1.jpg)

5. A "Save changes?" prompt will appear. Click **Yes** to save it.

    ![des-supplier-credit-note-note-2](../../../static/img/usage/supplier/guide/supplier-credit-note-note-2.jpg)

### C/N Description (SCN)

1. This shows the document description in the Supplier Statement, e.g., Overcharged-Stationery April 2015.

    ![des-supplier-credit-note-cn-description-1](../../../static/img/usage/supplier/guide/supplier-credit-note-cn-description-1.jpg)

2. Sample of supplier statement screenshot below.

    ![des-supplier-credit-note-cn-description-2](../../../static/img/usage/supplier/guide/supplier-credit-note-cn-description-2.jpg)

### Foreign Exchange Currency Gain/Loss (SCN)

- Differences in foreign currency exchange rates will automatically post FOREX Gain/Loss entries to the General Ledger.
- The posting date can be adjusted to reflect the FOREX Gain/Loss for a specific month.

![des-supplier-credit-note-gainloss-1](../../../static/img/usage/supplier/guide/supplier-credit-note-gainloss-1.jpg)

## Supplier Refund (SR)

- Receive a refund for an overpayment made to a supplier.
- Offset against the unapplied amounts of Supplier Payments and Credit Notes.

![des-supplier-refund-1](../../../static/img/usage/supplier/guide/supplier-refund-1.jpg)

### Basic Entry (SR)

1. Click the New button.
2. See the New Supplier Refund entry form screenshot below.

    ![des-supplier-refund-entry-1](../../../static/img/usage/supplier/guide/supplier-refund-entry-1.jpg)

3. Select the Supplier Code. Directly enter and search by either the supplier code or name.
4. Select the Payment Method (bank or cash account) in Received In.
5. Enter the Refund Amount (following the bank account currency).
6. Below is an example of the entry created:

    ![des-supplier-refund-entry-2](../../../static/img/usage/supplier/guide/supplier-refund-entry-2.jpg)

    **Double Entry will be:-**

    | **Account**          | **DR (RM)** | **CR (RM)** |
    | -------------------- | ----------- | ----------- |
    | Bank Acc             | 3,590.00    |             |
    | Supplier Control Acc |             | 3,590.00    |

7. Enter bank charges if applicable.

    ![des-supplier-refund-entry-3](../../../static/img/usage/supplier/guide/supplier-refund-entry-3.jpg)

8. For example, if bank charges are RM2.00, the double entry posting will be:

    | **Account**  | **DR (RM)** | **CR (RM)** |
    | ------------ | ----------- | ----------- |
    | Bank Charges | 2.00        |             |
    | Bank Account |             | 2.00        |

9. Enter the cheque number, cash, or TT into the Cheque No. field.

    ![des-supplier-refund-entry-4](../../../static/img/usage/supplier/guide/supplier-refund-entry-4.jpg)

### Knock-off (SR)

Purpose of knocking off invoices:

1. To display outstanding invoices in the Supplier Aging Report.
2. To indicate which invoices the payment offsets in the Supplier Statement.

#### Partial Knock-Off (SR)

1. Enter the knock-off amount in the Pay column (it will be automatically checked).
2. The Unapplied Amount will be reduced by the entered knock-off amount.

    ![des-supplier-refund-partial-knockoff-1](../../../static/img/usage/supplier/guide/supplier-refund-partial-knockoff-1.jpg)

#### Document Knock-Off (SR)

1. Check the boxes for the outstanding documents.
2. The Unapplied Amount will be reduced by the total of the selected documents.

    ![des-supplier-refund-document-knockoff-1](../../../static/img/usage/supplier/guide/supplier-refund-document-knockoff-1.jpg)

#### Random Knock-Off (SR)

1. Clicking the Pay column will automatically select the outstanding documents.
2. The Unapplied Amount will be reduced based on the outstanding balance.

    ![des-supplier-refund-random-knockoff-1](../../../static/img/usage/supplier/guide/supplier-refund-random-knockoff-1.jpg)

    :::note
    The Refund Unapplied amount shows the supplier refund that has not been allocated or knocked off against any unapplied amounts in supplier payments or credit notes.
    :::

### Attachment (SR)

- Attaching supporting documents is very useful.
- This allows you to easily retrieve and refer to the attached files in the future.

![des-supplier-refund-attachment-1](../../../static/img/usage/supplier/guide/supplier-refund-attachment-1.jpg)

1. Go to the attachment section.
2. Click the (+) button to insert the file path.
3. See the sample screenshot below.

    ![des-supplier-refund-attachment-2](../../../static/img/usage/supplier/guide/supplier-refund-attachment-2.jpg)

### Note (SR)

1. Click the Note section on the left sidebar.
2. Right-click to open the Rich Text Editor.

    ![des-supplier-refund-note-1](../../../static/img/usage/supplier/guide/supplier-refund-note-1.jpg)

3. You can start entering the note. See the example screenshot below.
4. Click the **X** button to save and exit the Rich Text Editor.

    ![des-supplier-refund-note-2](../../../static/img/usage/supplier/guide/supplier-refund-note-2.jpg)

5. A "Save changes?" prompt will appear. Click YES to save it.

    ![des-supplier-refund-note-3](../../../static/img/usage/supplier/guide/supplier-refund-note-3.jpg)

### Description (SR)

This shows the supplier refund description in the Supplier Statement, e.g., Refund For SC-00002 & PV-00004.

![des-supplier-refund-description-1](../../../static/img/usage/supplier/guide/supplier-refund-description-1.jpg)

Sample of supplier statement screenshot below.

![des-supplier-refund-description-2](../../../static/img/usage/supplier/guide/supplier-refund-description-2.jpg)

## Supplier Contra (SC)

- Settle outstanding balances between supplier and customer accounts without monetary transactions.
- This process uses an intermediate account known as a Contra Account, which must have a zero balance.

![des-supplier-contra-1](../../../static/img/usage/supplier/guide/supplier-contra-1.jpg)

### Basic Entry (SC)

Assuming you have created a [Customer Contra](../../usage/customer/guide#customer-contra), the same contra number will appear in the Supplier Contra.

1. Highlight the Contra No to edit. Click the Edit button.
2. See the Supplier Contra entry from screenshot below.

    ![des-supplier-contra-entry-1](../../../static/img/usage/supplier/guide/supplier-contra-entry-1.jpg)

3. Select the Supplier Code. Directly enter and search by either the supplier code or name.
4. Enter the Contra Amount (following the supplier currency).
5. Below is an example of the entry created:

    ![des-supplier-contra-entry-2](../../../static/img/usage/supplier/guide/supplier-contra-entry-2.jpg)

    **Double Entry will be:-**

    | **Account**          | **DR (RM)** | **CR (RM)** |
    | -------------------- | ----------- | ----------- |
    | Supplier Control Acc | 1,500.00    |             |
    | Contra Acc           |             | 1,500.00    |

:::note TIPS

Ensure the contra account is set up correctly. [Contra Account](../../usage/tools/guide#options)

:::

### Knock-off (SC)

Purpose of knocking off invoices:

1. To display outstanding invoices in the Supplier Aging Report.
2. To indicate the contra knock-off the invoices in Supplier Statement.

#### Partial Knock-Off (SC)

1. Enter the knock-off amount in the Pay column (it will be automatically checked).
2. The Unapplied Amount will be reduced by the entered knock-off amount.

    ![des-supplier-contra-partial-knockoff-1](../../../static/img/usage/supplier/guide/supplier-contra-partial-knockoff-1.jpg)

#### Document Knock-Off (SC)

1. Check the boxes for the outstanding documents.
2. The Unapplied Amount will be reduced by the total of the selected documents.

    ![des-supplier-contra-document-knockoff-1](../../../static/img/usage/supplier/guide/supplier-contra-document-knockoff-1.jpg)

#### Random Knock-Off (SC)

1. Clicking the Pay column will automatically select the outstanding documents.
2. The Unapplied Amount will be reduced according to the outstanding balance.

    ![des-supplier-contra-random-knockoff-1](../../../static/img/usage/supplier/guide/supplier-contra-random-knockoff-1.jpg)

    :::note

    The refund unapplied amount shows the supplier contra amount that has not been allocated or knocked off against any outstanding supplier invoices or debit notes.

    :::

### Attachment (SC)

- Attaching supporting documents is very useful.
- This allows you to easily retrieve and refer to the attached files in the future.

![des-supplier-contra-attachment-1](../../../static/img/usage/supplier/guide/supplier-contra-attachment-1.jpg)

1. Go to the attachment section.
2. Click the (+) button to insert the file path.
3. See the sample screenshot below.

    ![des-supplier-contra-attachment-2](../../../static/img/usage/supplier/guide/supplier-contra-attachment-2.jpg)

### Note (SC)

1. Click the Note section on the left sidebar.
2. Right-click to open the Rich Text Editor.

    ![des-supplier-contra-note-1](../../../static/img/usage/supplier/guide/supplier-contra-note-1.jpg)

3. You can start entering the note. See the example screenshot below.
4. Click the **X** button to save and exit the Rich Text Editor.

    ![des-supplier-contra-note-2](../../../static/img/usage/supplier/guide/supplier-contra-note-2.jpg)

5. A "Save changes?" prompt will appear. Click **Yes** to save it.

    ![des-supplier-contra-note-3](../../../static/img/usage/supplier/guide/supplier-contra-note-3.jpg)

### Description (SC)

This shows the supplier contra description in the Supplier Statement, e.g., Contra IV-00005.

![des-supplier-contra-description-1](../../../static/img/usage/supplier/guide/supplier-contra-description-1.jpg)

Sample of supplier statement screenshot below.

![des-supplier-contra-description-2](../../../static/img/usage/supplier/guide/supplier-contra-description-2.jpg)

### GL Ledger - Contra Account

1. Select the date range.
2. Select the account code, e.g., 450-000 CONTRA ACCOUNT.
3. Check the box for General Ledger.
4. Click the Apply button.
5. An example of the Contra Account ledger is shown below.

    ![des-supplier-contra-contra-account-1](../../../static/img/usage/supplier/guide/supplier-contra-contra-account-1.jpg)

## InterBank GIRO Module

To use the **Interbank GIRO** feature, you must have the **Interbank GIRO** module enabled in SQL Account.

![des-interbank-giro-requirement](../../../static/img/usage/supplier/guide/interbank-giro-requirement.png)

### Bank File Format

The following list shows the currently supported bank file formats.

![des-giro-bank-file-format](../../../static/img/usage/supplier/guide/giro-bank-file-format.png)

### Payment Method

1. Click the **Bank Info** button.

    ![des-giro-payment-method-1](../../../static/img/usage/supplier/guide/giro-payment-method-1.png)

2. Choose a **bank**.

    ![des-giro-payment-method-2](../../../static/img/usage/supplier/guide/giro-payment-method-2.png)

3. Click the **OK** button.

    ![des-giro-payment-method-3](../../../static/img/usage/supplier/guide/giro-payment-method-3.png)

4. The selected bank may have **more than one file format**; please ensure you have selected the **correct file format**.

    ![des-giro-payment-method-4](../../../static/img/usage/supplier/guide/giro-payment-method-4.png)

5. Enter the **bank information**, click **OK**, and then click **Save**.

    ![des-giro-payment-method-5](../../../static/img/usage/supplier/guide/giro-payment-method-5.png)

### Supplier Bank Account

1. Add a **bank account**, then click **Save**.

    ![des-giro-supplier-bank-account-1](../../../static/img/usage/supplier/guide/giro-supplier-bank-account-1.png)

### Supplier Payment Method

1. Select **Supplier Bank** from the drop-down list.

    ![des-giro-supplier-payment-method-1](../../../static/img/usage/supplier/guide/giro-supplier-payment-method-1.png)

2. Choose the **payment method** that contains **bank information**, then click **Save**.

    ![giro-supplier-payment-method-2](../../../static/img/usage/supplier/guide/giro-supplier-payment-method-2.png)

### Print Supplier Document (Interbank GIRO) Listing

1. Click the **GIRO** button.

    ![des-giro-print-supplier-document-listing-1](../../../static/img/usage/supplier/guide/giro-print-supplier-document-listing-1.png)

2. Enter additional information, then click the **Save** button.

    ![des-giro-print-supplier-document-listing-2](../../../static/img/usage/supplier/guide/giro-print-supplier-document-listing-2.png)

3. You can now upload the bank instruction file to the bank host.

### Excel Format

By default, the system saves Excel files in XLSX format. However, some banks (**Alliance Bank, Public Bank, RHB**) require the XLS format. To use this, you must have **Microsoft Excel 2007** or a later version installed on your machine.

Then, **open** the Excel file and **save it in XLS** format.
