---
sidebar_position: 2
title: FR3 FAQ
description: How to do custom reports
slug: /usage/Tools New/Fast Report/FR3 FAQ
tags: ["SQL Account", "Usage", "Tools"]
---

## Frequently Ask Question (FAQ)

### 1. Unit price is 0, display as FOC

In Memo, enter following syntax :

```pascal
[FormatFloat(',0.00;-,0.00;FOC ',<Document_Detail."UnitPrice">)]
```

![45](../../../../static/img/report/fastReport-basicGuide/45.png)

### 2. Document Currency Description change Cents to Sens

Syntax:

```pascal
[Document_Currency."Description"] : [StringReplace(CurrencyToLangWord(<Main."DocAmt">,<Profile."CurrencyLang">), 'CENTS', 'SENS', TRUE)]
```

![46](../../../../static/img/report/fastReport-basicGuide/46.png)

### 3. More Description convert RichTextToPlainText

Syntax :

```pascal
[RichTextToPlaintext(<Document_Detail."Description3">)]
```

![47](../../../../static/img/report/fastReport-basicGuide/47.png)

![48](../../../../static/img/report/fastReport-basicGuide/48.png)

### 4. How to change report paper size?

File -> Page Setting ->

![49](../../../../static/img/report/fastReport-basicGuide/49.png)

### 5. if Qty > 10, text color in red and in bold?

1. Double Click on Memo

2. Click on **Highlight Tab**

3. Click on **Add Button**

4. Expression value > 10

   ![50](../../../../static/img/report/fastReport-basicGuide/50.png)

5. Click on Font

   Can set for Font Type, Font Style, Size, Color or Effects

   ![51](../../../../static/img/report/fastReport-basicGuide/51.png)

6. Press **OK**

7. Right Click on Memo, **Ticked Allow Expression**

**Result** :

![52](../../../../static/img/report/fastReport-basicGuide/52.png)

### 6. Why in Report I have placed at the position I want, but when preview it will show at bottom?

Right click on Memo, **unticked Shift** and **Unticked Shift when Overlapped**

### 7. Export to PDF Logo is blur

![53](../../../../static/img/report/fastReport-basicGuide/53.png)

### 8. How to capture remark1 as url path?

In Memo properties :

Hyperlink Expression added in the Data Field Name

![54](../../../../static/img/report/fastReport-basicGuide/54.png)

Result :

![55](../../../../static/img/report/fastReport-basicGuide/55.png)

### 9. Payslip to show AL or MC Only

1. Click on **SubReport3**

2. Right click on **Leave MasterData Band**
   ![56](../../../../static/img/report/fastReport-basicGuide/56.png)

3. Click on Filter button

4. Enter the expression :

     ```pascal
     (<Leave."LeaveType"> ='AL') OR (<Leave."LeaveType"> ='MC')
     ```

5. Press OK

6. Press OK

   ![57](../../../../static/img/report/fastReport-basicGuide/57.png)

### 10. How to get Net Unit Price

 1. Click on **Memo Text**

 2. Place on **Document Detail Band**

 3. Drag data field from right to left box :

     ```pascal
     [<Document_Detail."Amount"> / <Document_Detail."Qty">]
     ```

 4. Press OK

 5. Adjust the position

 6. Preview and see the result

   ![58](../../../../static/img/report/fastReport-basicGuide/58.png)

### 11. UOM = UNIT, Qty display without Decimal Point, else with 2 Decimal Point

 1. Click On Memo Text

 2. Copy the below syntax and Paste into Memo:

     ```pascal
     [IIF(<Document_Detail."UOM"> = 'UNIT'>,
     FormatFloat('#,0;-#,0 ', <Document_Detail."Qty">) ,
     FormatFloat('#,0.00;-#,0.00 ', <Document_Detail."Qty">))]
     ```

    ![59](../../../../static/img/report/fastReport-basicGuide/59.png)

 3. Press **OK**

 4. Result After Preview :

    ![60](../../../../static/img/report/fastReport-basicGuide/60.png)

### 12. How to Get Supplier Bank in Payment Voucher?

 1. Click on Memo ![A](../../../../static/img/report/fastReport-basicGuide/A.png)

 2. Paste this syntax inside Memo

     ```pascal
     [<GetbankName(pl_SUPPLIERBANKACC."Bank">)]
     ```

    ![61](../../../../static/img/report/fastReport-basicGuide/61.png)

### 13. How to change the Amount in Word to First Character to Upper Case only?

Can use function NameCase

![62](../../../../static/img/report/fastReport-basicGuide/62.png)

Before :

![63](../../../../static/img/report/fastReport-basicGuide/63.png)

After :

![64](../../../../static/img/report/fastReport-basicGuide/64.png)