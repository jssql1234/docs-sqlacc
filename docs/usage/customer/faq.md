---
sidebar_position: 3
title: FAQ
description: Frequently asked questions and troubleshooting for Customer (AR) management.
slug: /usage/customer/faq
tags: ["SQL Account", "Usage", "Customer", "FAQ"]
---

## Bounced Payments in Foreign Currencies

### Customer Invoice

**Example:** Invoice amount **USD 100** | Rate **3.00** | Local Net Total = **RM 300**

![1](../../../static/img/usage/customer/faq/bounce-payment/1.png)

#### Scenario 1: Payment Received at a Higher Rate (Gain)

**Example:** Received **RM 330** (Gain of **RM 30**).

![2](../../../static/img/usage/customer/faq/bounce-payment/2.png)

To process the bounced payment:

1. **Issue a Customer Debit Note**: Create a Debit Note to reverse the original invoice amount.

    ![3](../../../static/img/usage/customer/faq/bounce-payment/3.png)

2. **Issue a Payment Voucher**: Create a Payment Voucher to credit out the amount that was previously knocked off.

    ![4](../../../static/img/usage/customer/faq/bounce-payment/4.png)

#### Scenario 2: Payment Received at a Lower Rate (Loss)

**Example:** Received **RM 270** (Loss of **RM 30**).

![5](../../../static/img/usage/customer/faq/bounce-payment/5.png)

To process the bounced payment:

1. **Issue a Customer Debit Note**: Create a Debit Note to reverse the original invoice amount.

     ![6](../../../static/img/usage/customer/faq/bounce-payment/6.png)

2. **Issue a Payment Voucher**: Create a Payment Voucher to credit out the amount that was previously knocked off.

     ![7](../../../static/img/usage/customer/faq/bounce-payment/7.png)

### Supplier Invoice

**Example:** Supplier Invoice amount **USD 100** | Rate **3.00** | Local Net Total = **RM 300**

![8](../../../static/img/usage/customer/faq/bounce-payment/8.png)

#### Scenario 1: Payment Made at a Higher Rate (Loss)

**Example:** Made payment of **RM 330** (Loss of **RM 30**).

![9](../../../static/img/usage/customer/faq/bounce-payment/9.png)

To process the bounced payment:

1. **Issue a Supplier Debit Note**: Create a Debit Note to reverse the original invoice amount.

     ![10](../../../static/img/usage/customer/faq/bounce-payment/10.png)

2. **Issue an Official Receipt**: Create an Official Receipt to debit the amount that was previously knocked off.

     :::info
     Assign the **USD 30** difference to a **Loss on Foreign Exchange** GL account.
     :::

     ![11](../../../static/img/usage/customer/faq/bounce-payment/11.png)

#### Scenario 2: Payment Made at a Lower Rate (Gain)

**Example:** Made payment of **RM 270** (Gain of **RM 30**).

![12](../../../static/img/usage/customer/faq/bounce-payment/12.png)

To process the bounced payment:

1. **Issue a Supplier Debit Note**: Create a Debit Note to reverse the original invoice amount.

     ![13](../../../static/img/usage/customer/faq/bounce-payment/13.png)

2. **Issue an Official Receipt**: Create an Official Receipt to debit the amount that was previously knocked off.

     :::info
     Assign the **USD -30** difference to a **Gain on Foreign Exchange** GL account.
     :::

     ![14](../../../static/img/usage/customer/faq/bounce-payment/14.png)

## Unrealized Foreign Exchange Gain/Loss

### Posting Unrealized Gain/Loss

1. Go to **Customer** → **Print Customer Aging Report**.

    ![1](../../../static/img/usage/customer/faq/foreign/1.png)

2. Select the **Date**.
3. Select the **Foreign Customer**.
4. Select the **Unrealized Gain Loss** report format.
5. Click **Apply**.

    ![2](../../../static/img/usage/customer/faq/foreign/2.png)

6. Click **Preview**. A dialog will prompt you to enter the currency rate.
7. Enter the **Closing Currency Rate** and click **OK**.

    ![3](../../../static/img/usage/customer/faq/foreign/3.png)

8. The system will display the report with the auto-calculated **Unrealized Gain/Loss Amount**.

    ![4](../../../static/img/usage/customer/faq/foreign/4.png)

9. Click **Post_DNCN_Adjustment**.

    ![5](../../../static/img/usage/customer/faq/foreign/5.png)

10. A "Posting Done" message will appear.

    ![6](../../../static/img/usage/customer/faq/foreign/6.png)

11. Go to **Customer Credit Note** or **Customer Debit Note** to verify the posted adjustment.

:::note

- The same steps apply to **Suppliers**.
- For more information, watch the tutorial on [YouTube](https://www.youtube.com/watch?v=PnLYx8ophIQ).

:::

## Bank Deposit Management

**Bank Deposit** is used when banking in two or more cheques in a single transaction slip. This groups the transactions in the **Bank Reconciliation** screen for easier matching.

### Steps to Create a Bank Deposit

1. Go to **Customer** → **Customer Payment**.

    ![1](../../../static/img/usage/customer/faq/open-bank-deposit/1.png)

2. Click **New**.

    ![2](../../../static/img/usage/customer/faq/open-bank-deposit/2.png)

3. Right-click in the blank space of the entry grid and select **Open Bank Deposit**.

    ![3](../../../static/img/usage/customer/faq/open-bank-deposit/3.png)

4. Click **New**.

    ![4](../../../static/img/usage/customer/faq/open-bank-deposit/4.png)

5. Enter the **Transaction Slip Number**, select the **Date**, and choose the **Bank Account**.

    ![5](../../../static/img/usage/customer/faq/open-bank-deposit/5.png)
    ![6](../../../static/img/usage/customer/faq/open-bank-deposit/6.png)

6. Click **Search**. The system will find customer payments within the selected date range.

    ![7](../../../static/img/usage/customer/faq/open-bank-deposit/7.png)
    ![8](../../../static/img/usage/customer/faq/open-bank-deposit/8.png)

7. Check the payments included in the same transaction slip and click **OK**.

    ![9](../../../static/img/usage/customer/faq/open-bank-deposit/9.png)

8. The selected payments will appear in the panel. You can remove incorrect entries using the **[-]** button. Click **Save**.

    ![10](../../../static/img/usage/customer/faq/open-bank-deposit/10.png)

### Reconciling the Bank Deposit

1. Go to **GL** → **Bank Reconciliation**.

    ![11](../../../static/img/usage/customer/faq/open-bank-deposit/11.png)

2. Click **New**.

    ![12](../../../static/img/usage/customer/faq/open-bank-deposit/12.png)

3. Select the **Bank Statement Date** and the correct **Bank Account**.

    ![13](../../../static/img/usage/customer/faq/open-bank-deposit/13.png)

4. Set the **Display Period** (ensure it includes the bank deposit date). Enter the **Bank Closing Balance** from your statement and click **Apply**.

    ![14](../../../static/img/usage/customer/faq/open-bank-deposit/14.png)

5. The cheques from the **Bank Deposit** will be displayed as a single row with the total amount. Check the row and click **Save**.

    ![15](../../../static/img/usage/customer/faq/open-bank-deposit/15.png)

### Bank Deposit via Cash Book Entry

You can also create a bank deposit through the Cash Book.

1. Go to **GL** → **Cash Book Entry**.

    ![16](../../../static/img/usage/customer/faq/open-bank-deposit/16.png)

2. Click **New**.

    ![17](../../../static/img/usage/customer/faq/open-bank-deposit/17.png)

3. Right-click in the blank space next to the **Payment Voucher** tab and select **Open Bank Deposit**.

    ![18](../../../static/img/usage/customer/faq/open-bank-deposit/18.png)

## Multi-Currency Payment Guide

### Customer Payment Scenarios

| # | Customer Currency | Payment Received In |
| :--- | :--- | :--- |
| 1 | RM | RM |
| 2 | USD | RM |
| 3 | USD | USD |
| 4 | USD | SGD |

#### 1. Customer Paid in RM & Payment Received in RM

1. Verify the customer's currency is set to RM (indicated by `----`).
   Go to **Customer** → **Maintain Customer**.

    ![1](../../../static/img/usage/customer/faq/payment-guide/1.png)

2. Create the Invoice.
   Go to **Sales** → **Invoice**.

    ![2](../../../static/img/usage/customer/faq/payment-guide/2.png)

3. Process the Payment.
   Go to **Customer** → **Customer Payment**.

    ![3](../../../static/img/usage/customer/faq/payment-guide/3.png)

#### 2. Customer Paid in USD & Payment Received in RM

:::note
Refer to Scenario 1 to verify if the customer is using USD.
:::

1. Check the **Local Amount** and **Net Total**. If they differ, the document is in a foreign currency (e.g., USD).
   Go to **Sales** → **Invoice**.

    ![4](../../../static/img/usage/customer/faq/payment-guide/4.png)

2. Process the Payment.
   Go to **Customer** → **Customer Payment**.

    ![5](../../../static/img/usage/customer/faq/payment-guide/5.png)

    - **2A. Currency Rate**: The rate used for knocking off the payment (auto-calculated).
    - **2B. Payment Amount**: The amount received in RM (based on the Bank payment method currency).
    - **2C. Payment Method**: Select the correct bank account.
    - **2D. Pay Amount**: You can enter the desired amount; the currency rate (2A) will update when you knock off the invoice.

#### 3. Customer Paid in USD & Payment Received in USD

1. **Setup**:
    1. Maintain a USD Bank account in the General Ledger (**GL** → **Maintain Account**).
    2. Assign the USD currency to the payment method (**Tools** → **Maintain Payment Method**).

    ![6](../../../static/img/usage/customer/faq/payment-guide/6.png)

2. Create the Invoice (USD currency).
   Go to **Sales** → **Invoice**.

    ![7](../../../static/img/usage/customer/faq/payment-guide/7.png)

3. Process the Payment.
   Go to **Customer** → **Customer Payment**.

    :::info
    The currency rate in the top-right corner can only be edited if the customer's currency matches the payment currency.
    :::

    ![8](../../../static/img/usage/customer/faq/payment-guide/8.png)

   1. **Rate**: Update the rate according to the current market value.
   2. **Payment Method**: Select the USD payment method.
   3. **Paid Amount**: Enter the amount of USD received.
   4. **Local Amount**: Auto-calculated as `Paid Amount × Currency Rate`.
   5. **IV Amount**: This follows the foreign currency amount, not the local amount.

    If the currency rate differs from the Invoice rate, the system will prompt a message showing the **Gain/Loss on Foreign Exchange** upon saving.

    ![9](../../../static/img/usage/customer/faq/payment-guide/9.png)

    :::note
    If the Invoice rate was 3.5 and the payment rate is 3.6, the system will auto-calculate and display the gain/loss when you click **Save**.
    :::

#### 4. Customer Paid in USD & Payment Received in SGD

For customers using USD where payment is received in a different foreign currency (e.g., SGD), ensure the corresponding payment method is maintained. Refer to Scenario 3 for setup instructions.

## Sales Commission Reports

### Setting Up Commission Scripts

1. Go to **Tools** → **Maintain Commission Script** → **New**. Enter a **Code** and **Description**.

    :::note
    This feature requires the **Maintain Commission Script** module.
    :::

    ![1](../../../static/img/usage/customer/faq/comm/1.png)
    ![2](../../../static/img/usage/customer/faq/comm/2.png)
    ![3](../../../static/img/usage/customer/faq/comm/3.png)

    **Default Commission Script Example:**

    ```pascal
    procedure CalculateCommission(AKODocAmt, AAge: variant; var Value: variant);
    begin
        if AAge < 10 then
            Value := AKODocAmt * 0.05
        else if AAge < 20 then
            Value := AKODocAmt * 0.03
        else if AAge < 30 then
            Value := AKODocAmt * 0.02
        else
            Value := AKODocAmt * 0.005;
    end;
    ```

2. Update the commission rates and age brackets in the script as needed, then click **Save**.

   ![4](../../../static/img/usage/customer/faq/comm/4.png)

    - **Age Brackets**: 10, 20, 30 days.
    - **Rates**: 0.05 (5%), 0.03 (3%), etc.

3. Assign the script to an agent.
   Go to **Tools** → **Maintain Agent**.

    ![5](../../../static/img/usage/customer/faq/comm/5.png)

4. In the **Attachment** tab, select the commission script and click **Save**.

    ![6](../../../static/img/usage/customer/faq/comm/6.png)

5. Generate the report.
   Go to **Customer** → **Print Customer Document Listing**.
   - Select **Document Type**: **Customer Payment Listing**.
   - **Group By**: **Agent**.
   - Click **Apply**.
   - Preview using the **Cust Local - Payment Listing - Collection Report** format.

    ![7](../../../static/img/usage/customer/faq/comm/7.png)
    ![8](../../../static/img/usage/customer/faq/comm/8.png)
    ![9](../../../static/img/usage/customer/faq/comm/9.png)

## Post-Dated and Bounced Cheques

### Post-Dated Cheques (PDC)

A post-dated cheque is written for a future date.

1. Go to **Customer** → **Customer Payment**.

    ![1](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/1.png)

2. Click **New**.

    ![2](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/2.png)

3. Create the payment and knock off the corresponding invoice. Ensure the bank account and amount are correct.

    ![3](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/3.png)

4. Right-click in the blank space next to the **Customer Payment** header and select **Set Posting Date**.

    ![4](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/4.png)

5. Select the actual **Posting Date** of the cheque and click **OK**.

    ![5](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/5.png)
    ![6](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/6.png)

6. The posting date will now be displayed. Click **Save**.

    ![7](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/7.png)

7. In the **Ledger Report**, the transaction will appear under the specified posting date.

    ![8](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/8.png)

8. To view all PDCs, go to **Customer Reports** → **Print Customer Post Dated Cheque Listing**.

    ![9](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/9.png)

9. Select the **Payment Date** (not the posting date) and click **Apply**.

    ![10](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/10.png)
    ![11](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/11.png)

### Bounced Cheques

A bounced cheque is one that cannot be processed due to insufficient funds or errors.

1. Go to **Customer** → **Customer Payment**.

    ![12](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/12.png)

2. Locate and double-click the bounced payment document.

    ![13](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/13.png)

3. Click **Edit**.

    ![14](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/14.png)

4. Right-click in the blank space next to the **Customer Payment** header and select **Bounced Status**.

    ![15](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/15.png)

5. Check the **Bounced** box and set the **Bounce Date** (must be on or after the posting date). Click **OK**.

    ![16](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/16.png)

6. The document will be labeled as bounced. Click **Save**.

    ![17](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/17.png)

7. The **Ledger Report** will reflect the bounced transaction on the specified date.

    ![18](../../../static/img/usage/customer/faq/post-dated-bounced-cheque/18.png)

## MyKad Integration

### Reading Customer Info via MyKad

1. Connect your **Smart Card Reader** to your computer. The reader will show a red light when connected.

    ![1](../../../static/img/usage/customer/faq/read-mykad/1.png)

2. Insert the MyKad into the reader. A blue light indicates a successful read.

    ![2](../../../static/img/usage/customer/faq/read-mykad/2.png)

3. In SQL Account, go to **Customer** → **Maintain Customer** → **New**.
4. Click **Read MyKad**.

    ![3](../../../static/img/usage/customer/faq/read-mykad/3.png)

5. Select the **Reader Device** and click **Read Card**.

    ![4](../../../static/img/usage/customer/faq/read-mykad/4.png)

6. Click **Read MyKad**.

    ![5](../../../static/img/usage/customer/faq/read-mykad/5.png)

7. The system will automatically populate the **Name**, **Address**, and **ID Number**.

    ![6](../../../static/img/usage/customer/faq/read-mykad/6.png)
