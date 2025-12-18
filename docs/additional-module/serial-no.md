---
title: Serial No Module
description: A guide about serial no module for SQL Account
slug: /additional-module/serial-no
tags: ["SQL Account", "Additional Module"]
---

## Instruction

1. Navigate **Stock** > **Maintain Stock Item** > **Edit**, checked **Serial No.** > **Save**.

   ![1](../../static/img/additional-module/serial-no/1.png)

2. Next, go to **Purchase** > **Goods Received Note** > **New**.

   :::info

   There are **3 methods** to apply serial no:

   :::

   ### Method 1: Manually Enter

   1. Click on the **Qty** column.

   2. Click on "▼" symbol.

   3. Click on "+" (Green Icon).

   4. Input manually at the empty box.

   ![2](../../static/img/additional-module/serial-no/2.png)

   ### Method 2: Import from Notepad / Word

   1. Prepare the **serial no** you wish to import in a notepad, save it.

      ![3](../../static/img/additional-module/serial-no/3.png)

   2. Click **Import**.

      ![4](../../static/img/additional-module/serial-no/4.png)

   3. Select the notepad file you had just created.

      ![5](../../static/img/additional-module/serial-no/5.png)

   4. When completed, a dialog with status "_Done_" will pop, click Ok and you will be all set.

      ![6](../../static/img/additional-module/serial-no/6.png)

   ### Method 3: Generator

   1. Click on **Generator**.

      ![7](../../static/img/additional-module/serial-no/7.png)

      ![8](../../static/img/additional-module/serial-no/8.png)

      | Field      | Description                       |
      | ---------- | --------------------------------- |
      | Format     | Serial No Format                  |
      | Start From | The number you wish to start from |
      | Count      | How many units to generate        |

   2. Sample output.

      ![9](../../static/img/additional-module/serial-no/9.png)

3. In **Delivery Order**

   1. Go to **Sales** > **Delivery Order**, and click _Add_

      ![10](../../static/img/additional-module/serial-no/10.png)

      In this form, you can find a "**+**" (Green Icon), it's functionality is similar to [Method 1](#method-1-manually-enter).

      For "**Import**", it's functionality is similar to [Method 2](#method-2-import-from-notepad--word).

   2. Select and tick the serial no, press Ok.

      ![11](../../static/img/additional-module/serial-no/11.png)

   :::info[Note]
   Stock Adjustment does not support serial no; consider using Stock Received and Stock Issue as alternatives.
   :::

### Serial No Report

| Report                      | Functionality                                                                                                                                                 | Way to Access                     |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| Stock Physical Worksheet    | Show all serial no that have not been issued                                                                                                                  | Print Stock Physical Worksheet    |
| Stock Serial No Conflict    | - Check serial no which have been issued but no receiving information<br /> - Check duplicate serial no received at the same location/batch for the same item | Print Stock Serial No Conflict    |
| Stock Outstanding Serial No | For documents that are issued or received but do not have a serial no                                                                                         | Print Stock Outstanding Serial No |
| Serial No Inquiry           | Check serial no movement                                                                                                                                      | Inquiry > Serial No Inquiry       |

### Access Right for Serial No

Group Stock

1. Always match Qty with Serial No.

   - Enable this right to enforce that the **serial no** matches the **qty**.
   - For example, 2 qty = 2 serial no.
   - When this right is enabled, _Print Outstanding Serial Numbers_ will yield no result.

2. Allow Non-Existent Serial No.

   - Enable this right to allow **non-existent serial no** for issued serial no.
   - When this right is enabled, _Print Stock Serial No Conflict_ will yield no result.
