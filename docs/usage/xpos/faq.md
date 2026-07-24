---
sidebar_position: 3
title: FAQ
description: Frequently asked questions in X-Pos System
slug: /usage/xpos/faq
tags: ["SQL Account", "Usage", "X-Pos", "FAQ"]
---

## Terminal Setup

### Why is my terminal not available for synchronization?

The terminal must be saved and marked as **Active** before online synchronization is available.

1. Go to **POS** > **Maintain POS Terminal...**.
2. Open the terminal.
3. Confirm that **Active** is selected.
4. Save the terminal, then click **Sync Terminal** again.

Also confirm that the terminal has a valid **Location** and **Settings** profile. See [Maintain POS Terminal](./guide.md#maintain-pos-terminal) for the complete setup procedure.

### Why can't I bind an API user to a terminal?

Use **Bind API User** only after the terminal has been saved. The system creates or reuses a dedicated API user using the terminal code, for example `COUNTER01_API`.

Check the following if binding fails:

- The application API host is configured.
- Your user account has permission to maintain system users.
- The terminal code is valid and unique.
- The system `ADMIN` account is not selected as the terminal API user.

### Why are the wrong items or prices shown on the terminal?

Check the terminal's assigned **Location** and **Settings** profile. Then save any changes and run **Sync Terminal** again.

The settings profile controls default price tags and item mappings. The location controls the stock or outlet data supplied to the terminal.

## Payment Methods and POS Settings 

### Why does a payment post to the wrong account?

Review the payment method's **GL Code**. POS payments are posted to the SQL Account payment method or GL account selected in this field. 

### How do I require a reference number for card or e-wallet payments?

Open the payment method and select **Must Fill Ref. No**. The cashier must then enter a reference number before completing payment.

### Why can't a cashier use split payment?

In **Maintain POS Settings**, select **Accept Multiple Payment** in the **Payment** section. Save the settings profile and synchronize the terminal.

### Why is an unknown scanned item ignored?

Check the **Item Not Exist** setting in the assigned POS settings profile. To post the item as a custom item, select the option that uses the **Default Custom Item Code**, and ensure that code has been configured.

## Metadata Export and Synchronization

### Why can't I start a metadata export?

Export is unavailable while the terminal is in insert or edit mode. Save or cancel the changes first, then retry. The terminal must also be active.

### What is the difference between Sync and Download?

| Action | Use |
| --- | --- |
| **Sync** | Creates the metadata package and uploads it directly to the POS metadata service. |
| **Download** | Creates a ZIP package that you can transfer to the terminal manually. |

### What should I do when a PIN is displayed after synchronization?

Record the PIN immediately and use it when pairing or setting up the terminal. The PIN is also copied to the clipboard by the application.

:::warning
The PIN cannot be retrieved again. If it is lost, revoke the current terminal binding and synchronize again to create a new PIN.
:::

### Why is a terminal missing from the multi-terminal export list?

Only terminals that already have a UUID binding appear in the multi-terminal export list. Synchronize the terminal once individually first, then reopen **Export Data**.

### Why does metadata synchronization fail with a token or upload error?

Confirm that the API and POS metadata service configuration is correct and that the workstation has internet connectivity. Then retry the synchronization. 

### When should I use Unbind?

Use **Unbind** only when the terminal must be connected as a new device. It clears the terminal UUID binding and removes its related local temporary export folder.

Do not use **Unbind** for a normal metadata refresh. For routine updates, use **Sync** instead.

## Printing and Counter Closing

### Why is no receipt printed after a sale?

Check the following in the terminal's POS settings profile:

- **Auto Print Receipt** is selected.
- A compatible receipt printer is configured and available.
- The terminal has been synchronized after changing the settings.

### Why is the receipt paper not cut automatically?

Select **Cut Receipt Paper** in the POS settings profile, then test the printer. Paper cutting depends on whether the receipt printer supports the cut-paper command.

### Why can't a user close the counter?

If **Close Counter with Password** is enabled in the POS settings profile, the user must enter the required password to close the counter. Confirm the outlet's counter-close access procedure and password before retrying.
