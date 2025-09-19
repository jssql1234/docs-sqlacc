---
sidebar_position: 2
title: Report Builder FAQ
description: How to do custom reports
slug: /usage/Tools New/RTM/ReportBuilderFAQ
tags: ["SQL Account", "Usage", "Tools"]
---

## How to rename the component I use?

![ch101](../../../../static/img/getting-started/user-guide/ch101.jpg)

1. Click Icon here (eg DBText)
2. Click on the place to be print/shown
3. At the Properties for XXXXXX, look for Identity | UserName & change the Name you like (Only Alphanumeric & no spacing)

## Why when Export to PDF format the Company Logo look "ugly"?

![ch102](../../../../static/img/getting-started/user-guide/ch102.jpg)

1. In the report designer set the setting
- ImageCompressionLevel to 1
- Untick ScaleImages
2. At the Company Logo Right Click
- Tick DirectDraw
- Untick Stretch
3. Resize your Jpeg Logo to smaller dimension
4. Resize the Company Logo (Report Builder component) to the same dimension of your Jpeg Logo

## Why when Export to PDF format the the file size so large?

![ch103](../../../../static/img/getting-started/user-guide/ch103.jpg)

1. In the report designer set the setting look for PDFSettings
- CompressionLevel to clMax
2. In the report designer set the setting look for PDFSettings | EmbedFontOptions
- efUseSubset to True (checked)

**Special DisplayFormat**

## 1. How if data is PI-12345 but I wanted to be printed as 12345?

### Just Enter as Follow code:-

<details>
    <summary>Code</summary>

Procedure DBTxtDocNoOnGetText(var Text: String);

begin

  Delete(Text, 1, 3);

  Text := Text;

end;

</details>

##  2. How if data is PI-12345 but I wanted to be printed as PI12345?

### Just Enter as Follow code:-

<details>
    <summary>Code</summary>

Procedure DBTxtDocNoOnGetText(var Text: String);

begin

  Delete(Text, 3, 1);

  Text := Text;

end;

</details>

## 3. How if data is 17-08-2005 but I wanted to be printed as 17 hb?

### Just Enter as Follow code in the DisplayFormat:-

**dd 'hb'**

## 4. How if data is 1234-001 but I wanted to be printed as 1234 & the value is not fixed (i.e may 12345-001, 1234-001)?

### Just Enter as Follow code:-

<details>
    <summary>Code</summary>

Procedure DBTxtDocNoOnGetText(var Text: String);

begin

  Text := SubStrOfDelimitedStr(Text, 0, 1, '-');

end;

</details>

## 5. How if data is 1234-001 but I wanted to be printed as 001 & the value is not fixed (i.e may 12345-001, 1234-32)?

### Just Enter as Follow code:-

<details>
    <summary>Code</summary>

Procedure DBTxtDocNoOnGetText(var Text: String);

begin

  Text := SubStrOfDelimitedStr(Text, 1, 1, '-');

end;

</details>

## 6. How to reverse this #,0.00;-#,0.00 to this -#,0.00;#,0.00?

### Just Enter as Follow code:-

<details>
    <summary>Code</summary>

procedure DetailBeforePrint;

var d, s : string;

begin

  s := Option.GetFieldValue('AccountingValueDisplayFormat');

  d := ValueOfSemiColonStr(s, 1)+';'+ ValueOfSemiColonStr(s, 0);  

  DBTxtC4.DisplayFormat := d;

end;

</details>

## 7. How to set 0 when empty?

### Below is Example :

<details>
    <summary>Code</summary>

procedure DBTxtTaxOnGetText(var Text:String);

begin

  if Trim(plSQL_1.GetFieldValue('TaxAmt')) = '' then

    Text := '0.00' ;

end;

</details>

## 8. How to Combine Currency Symbol with DocAmt or DBCalc.Value using TppVariable?

<details>
    <summary>Code</summary>

procedure VarSumDROnCalc(var Value : Variant);

var V : string;

begin

  V := FormatFloat(Option.GetFieldValue('AccountingValueDisplayFormat'), DBCalcSCR.Value);

  Value := Option.GetFieldValue('LocalCurrencySymbol') + ' ' + V;

end;

</details>

## How to Set Current Date Time plus/minus N?

<details>
  <summary>Code</summary>

procedure Variable1OnCalc(var Value : Variant);

var lDT : Variant;

begin

  //Example deduct 1.5 hrs

  lDT := CurrentDateTime-0.0625; //(1.5/24)

  Value := FormatDateTime('dd/MM/yyyy hh:mm AM/PM', lDT); 

end;

</details>

## How to Maintain the QR Code Size with large Data?

:::note
It might unable to scan if size too small & data too large
:::

![ch104](../../../../static/img/getting-started/user-guide/ch104.jpg)

## How to Add QR Code for E-Invoicing?

:::note
Only Available in Version 852 & above
:::

![ch105](../../../../static/img/getting-started/user-guide/ch105.jpg)

* The measurement is in Inch
* This guide design for is for Laser Printer only
* For Dot Matrix Printer make sure set to 1 for Height & Width

## How to Add FromDocNo and FromDocDate Variable in Report Design ?

1. Go in Report Design | Click on ![1](../../../../static/img/report/add-fromDocNo-fromDocDate/1.png) then place at the grid – refer below Pic

   ![2](../../../../static/img/report/add-fromDocNo-fromDocDate/2.png)

   1. Right Click on Variable2 | Select Calculation |

      ![3](../../../../static/img/report/add-fromDocNo-fromDocDate/3.png)

      After Done press OK

2. If the date is not appearing in report preview

   ![4](../../../../static/img/report/add-fromDocNo-fromDocDate/4.png)

   1. Click on **Calc Tab**

   2. **Menu bar** | click **View** | Select **Events**

   3. Look for ***Variable***

   4. Click on **OnPrint**

   5. Click on **Document_Detail**

   6. Click on **FromDocNo**

   7. Drag from **FromDocNo** to the query box.

## How to Create SUM Variable for TAX Column ?

![1](../../../../static/img/report/crtSUMforTaxCol/1.png)

1. Click on the variable icon

2. Click on where you want to create a new variable, right click on the variable created > go calculations , Insert the query in the next section accordingly

3. Click on the variable created, and make sure choose it to `DOUBLE`.

**Query:**

1. **Formula for Sub Total**

    ```pascal
    Variable1.DisplayFormat := Option.GetFieldValue('AccountingValueDisplayFormat');

    Value := GetAggregateValue(agSUM, Document_Detail, 'DocKey', 'Amount');
    ```

2. **Formula for Total Exclude GST (RM)**

    ```pascal
    Variable2.DisplayFormat := Option.GetFieldValue('AccountingValueDisplayFormat');

    Value := GetAggregateValue(agSUM, Document_Detail, 'DocKey', 'LocalAmount');
    ```

3. **Formula for Total of Tax Amt (RM)**

    ```pascal
    Variable5.DisplayFormat := Option.GetFieldValue('AccountingValueDisplayFormat');

    Value := GetAggregateValue(agSUM, Document_Detail, 'DocKey', 'LocalTaxAmt');
    ```

4. **Formula for Total Include GST (RM)**

    ```pascal
    Variable6.DisplayFormat := Option.GetFieldValue('AccountingValueDisplayFormat');

    Value := GetAggregateValue(agSUM, Document_Detail, 'DocKey', 'LocalAmountWithTax');
    ```

## How to Disable Query for Deleted Field ?

1. If you had deleted any field in report designer with Query, then u will get the below message, click **OK**

   ![1](../../../../static/img/report/disbQryinRpt/1.png)

2. Click on the blue colour report name to enter in report designer page

   ![2](../../../../static/img/report/disbQryinRpt/2.png)

3. Click on the field, the field name will be shown at the left bottom of the application as shown below. If you had deleted the field, refer to step 4.

   ![3](../../../../static/img/report/disbQryinRpt/3.png)

4. Click on **CALC**, go View > Modules

   ![4](../../../../static/img/report/disbQryinRpt/4.png)

5. Follow the steps below:

   1. Click on **Event Handlers**

   2. Go to **procedure DetailBeforePrint**

   3. An error will be shown at the bottom, double click on it, and the system will redirect to the row with the error

   ![5](../../../../static/img/report/disbQryinRpt/5.png)

6. Enter '//' as in the image below :

   ![6](../../../../static/img/report/disbQryinRpt/6.png)

7. Right click and compile , make sure no error > save > close the preview screen and try preview again.

:::info[Note]
You can also refer to the guidance video at [HERE](https://www.sql.com.my/) regarding the above issue.
:::

## Display Exemption Number & Expiry Date in Invoice Template

### Part A : Custom | Maintain Customer

![1](../../../../static/img/report/displayExmpNoExpDateInv/1.png)

### Part B : Report Format add customer exemption Number

1. Go to Sales | Sales Invoice | Select any of your invoice | Preview | choose your invoice format template | click on the bottom blue color report name to go into report designer page

   ![2](../../../../static/img/report/displayExmpNoExpDateInv/2.png)

2. Insert **Exemption Number** label

   1. click on the A label icon
   2. click on the area that you want to locate the field
   3. rename the label

   ![3](../../../../static/img/report/displayExmpNoExpDateInv/3.png)

3. Insert **Tax Exemption Number** DBText

   1. click on the DBText field
   2. click on the are that you want to located the field
   3. select Document Company & TaxExemptNo

   ![4](../../../../static/img/report/displayExmpNoExpDateInv/4.png)

4. Insert **Expiry Date** label

   1. click on the A label icon
   2. click on the area that you want to locate the field
   3. rename the label

   ![5](../../../../static/img/report/displayExmpNoExpDateInv/5.png)

5. Insert **Tax Expiry Date** DBText

   1. click on the DBText field
   2. click on the are that you want to located the field
   3. select Document Company & TaxExpDate

   ![6](../../../../static/img/report/displayExmpNoExpDateInv/6.png)

### Part C: Save as a new report name & preview the new format

1. Once you complete, go file | save as | enter a new report name | Save

   ![7](../../../../static/img/report/displayExmpNoExpDateInv/7.png)

2. Preview your new report

   ![8](../../../../static/img/report/displayExmpNoExpDateInv/8.png)

3. The exemption number & expiry date added

   ![9](../../../../static/img/report/displayExmpNoExpDateInv/9.png)

## How to Drag XML Report into SQL ?

:::info[note]
If this XML Report is Customer Aging, go Customer Aging to drag the XML Report

If this XML report is Supplier Aging Report, go to Supplier Aging to drag the XML Report
:::

1. Open the XML Report & also Customer Aging, drag the XML Report into the Report Name field

   ![1](../../../../static/img/report/dragXMLRpt/1.png)

2. Double Click on the new report template in blue color.

   ![2](../../../../static/img/report/dragXMLRpt/2.png)

3. Click on the arrow down key to choose the right template

   - Eg : If the report Name is Cust-Local-**L0**-06 Month

      - L0 = no special grouping, the template you have to choose eg Cust 06 Month Aging
      - L1 = Grouping by 1 level, the template you have to choose eg Cust 06 Month Aging – Level 1
      - L2 =Grouping by 2 level, the template you have to choose eg Cust 06 Month Aging – Level 2

   - Eg : If the report Name is Cust-Local-L0-**06** Month

     - 04 = 04 Month
     - 06 = 06 Month
     - 12 = 12 Month

## How to Fix Report Tax Rate show A instead of 6% ?

![1](../../../../static/img/report/fastReport-taxShwA/1.png)

1. Preview the Report format, Click on blue color link and enter into Report Design.

   ![2](../../../../static/img/report/fastReport-taxShwA/2.png)

2. Check GST Summary using which Pipeline | This Report using plSQL_7.

   ![3](../../../../static/img/report/fastReport-taxShwA/3.png)

3. Click on Calc Tab.

   ![4](../../../../static/img/report/fastReport-taxShwA/4.png)

4. Click on Menu View | Select Module

   ![5](../../../../static/img/report/fastReport-taxShwA/5.png)

5. Click on Events | Click on Main:plSQL_0 | Look for SQL_7(Refer Step 2 to see which pipeline) | Insert TaxRate

   ![6](../../../../static/img/report/fastReport-taxShwA/6.png)

   Query:

    ```sql
    SQL_7 := 'SELECT DocKey, Tax, TaxRate, Sum(LocalAmount) LocalAmount, Sum(Qty) Qty, Sum(LocalTaxAmt) localTaxAmt, Description '+
        'FROM Document_Detail ' +
        'Where Tax &lt;> ''''' +
        'GROUP BY Dockey, Tax, TaxRate';
   ```

6. Click on Event Handler | Select Procedure ReportBeforePrint | Look for Pipeline SQL_7 | Insert TaxRate

    ![7](../../../../static/img/report/fastReport-taxShwA/7.png)

    Query:

    ```pascal
    LocalSQL_SELECT(plSQL_7, SQL_7, 'Dockey;Tax;TaxRate');
    ```

7. Click on SubReport1:plSQL_7 Tab

    ![8](../../../../static/img/report/fastReport-taxShwA/8.png)

8. Click on VarTax | Right Click | Select Calculation

   ![9](../../../../static/img/report/fastReport-taxShwA/9.png)

9. Amend the Query | Press OK

   - Before Amend:

        ![10](../../../../static/img/report/fastReport-taxShwA/10.png)

   - After Amend:

        ![11](../../../../static/img/report/fastReport-taxShwA/11.png)

   Query:

    ```pascal
    Value := plsql_7.getfieldvalue('Tax') + ' @ ' + plsql_7.getfieldvalue('TaxRate');
    ```

10. File | Save

    ![12](../../../../static/img/report/fastReport-taxShwA/12.png)

11. Close the report builder

12. Preview again the same report format.

    ![13](../../../../static/img/report/fastReport-taxShwA/13.png)

## How to Make Official Receipt Format Set Knock Off Grid to Show Full Width ?

1. Go to **subreport1 : Document_KnockOff**

    ![1](../../../../static/img/report/ORSetKnockOffGridToShwFullWidth/1.png)

2. Go to **Report**, click on **Title**

    ![2](../../../../static/img/report/ORSetKnockOffGridToShwFullWidth/2.png)

3. Move all field in Column Header to **Title**

    ![3](../../../../static/img/report/ORSetKnockOffGridToShwFullWidth/3.png)

4. Go to **File** > **Page Setup...**

    ![4](../../../../static/img/report/ORSetKnockOffGridToShwFullWidth/4.png)

5. Go to **Layout**, change the **column** to ***1***

    ![5](../../../../static/img/report/ORSetKnockOffGridToShwFullWidth/5.png)

6. Now, it expands to full page, you can adjust all your column as your wish.

    ![6](../../../../static/img/report/ORSetKnockOffGridToShwFullWidth/6.png)

7. Once you done adjust, go file > save as, key a new report name.

8. Close the preview, and preview your new report name.

## How to do Rounding of Figure in Report ?

**Sample Invoice with Rounding RM0.02 :**

![1](../../../../static/img/report/roundingRpt/1.png)

1. Using Tax Invoice format 06-Tax-Invoice
   ![2](../../../../static/img/report/roundingRpt/2.png)

   :::info[note]
   Click on blue color link - **06-Tax-Invoice**
   :::

2. Click on **Calc** Tab

   ![3](../../../../static/img/report/roundingRpt/3.png)

3. Right Click select **Module**

   ![4](../../../../static/img/report/roundingRpt/4.png)

4. Click on **Declarations**

   ![5](../../../../static/img/report/roundingRpt/5.png)

5. Declare **SQL_Rounding** under **Variable**

   ![6](../../../../static/img/report/roundingRpt/6.png)

6. Click on Events | On Create | Procedure GlobalOnCreate insert syntax as below :

    ```pascal
    SQL_Rounding := 'SELECT DocKey, Sum(Amount) Amount, Description '+
    'FROM Document_Detail ' +
    'WHERE ItemCode=''RTN5Cents'' '+
    'GROUP BY DocKey';
    ```

    **Refer Picture below :**

   ![7](../../../../static/img/report/roundingRpt/7.png)

    :::info[Optional]
    Add additional syntax in plSQL_4 – Refer below, only if Total Amount beforeGST you want to exclude rounding amount.

   ![8](../../../../static/img/report/roundingRpt/8.png)

    ```pascal
    SQL_4 := 'SELECT DocKey, Sum(Amount) Amount, Description '+
    'FROM Document_Detail ' +
    'WHERE ItemCode <> ''DISC'' '+
    'or Itemcode is null ' +
    'and ItemCode <> ''RTN5Cents'' ' +
    'GROUP BY DocKey';
    ```

   :::

7. Click on Event Handlers | Click on procedure Report BeforePrint, insert syntax as below :

    ```pascal
    LocalSQL_SELECT(plSQL_Rounding, SQL_Rounding, 'DocKey');
    SetDataPipelineFieldLink(Main, plSQL_Rounding, 'DocKey', 'DocKey');
    ```

   ![9](../../../../static/img/report/roundingRpt/9.png)

8. File | Save | Exit from report design and go in to Report Design again.

9. Insert DBText | and place at the place you want.

   ![10](../../../../static/img/report/roundingRpt/10.png)

   1. Click on DBText

   2. Place at the Group Footer area

   3. Select plSQL_Rounding

   4. Manually type in Amount

   Here is the output :

   ![11](../../../../static/img/report/roundingRpt/11.png)

   After adjust the position :

   ![12](../../../../static/img/report/roundingRpt/12.png)

    **Item Detail hide Item Code RTN5Cents to be appearing, refer step as below :**

10. Click on Document_Detail Tab as below | Click on Calc | Event Handlers | Procedure RdiscOnPrint

    ![13](../../../../static/img/report/roundingRpt/13.png)

    - Syntax:

        ```pascal
        RDisc.Visible := (Document_Detail.getfieldvalue('Itemcode') <> 'DISC')
        and (Document_Detail.getfieldvalue('Itemcode') <> 'RTN5Cents');
        ```

    - Output :

        ![14](../../../../static/img/report/roundingRpt/14.png)

        **How to do if the report never create the region before?**

11. Right click tick all the Toolbars

    ![15](../../../../static/img/report/roundingRpt/15.png)

12. Click on Region component

    ![16](../../../../static/img/report/roundingRpt/16.png)

13. Place at the design grid | Click at the region | Select no Fill

    ![17](../../../../static/img/report/roundingRpt/17.png)

14. Select No Line

    ![18](../../../../static/img/report/roundingRpt/18.png)

15. Place all the DBtext/DBRichText inside the Region.

    ![19](../../../../static/img/report/roundingRpt/19.png)

16. Click on Region to check the object name :

    ![20](../../../../static/img/report/roundingRpt/20.png)

17. Click on Calc tab | Right Click select Events

    ![21](../../../../static/img/report/roundingRpt/21.png)

18. Look for RDisc | Select OnOnPrint | Place the syntax inside bottom box

    ![22](../../../../static/img/report/roundingRpt/22.png)

    Syntax :

    ```pascal
    RDisc.Visible := (Document_Detail.getfieldvalue('Itemcode') <> 'DISC')
    and (Document_Detail.getfieldvalue('Itemcode') <> 'RTN5Cents');
    ```

    :::info[note]
    **RDisc** is your object name, if you object name is **Region1**, then have to change as below :

    ```pascal
    Region1.Visible := (Document_Detail.getfieldvalue('Itemcode') <> 'DISC')
    and (Document_Detail.getfieldvalue('Itemcode') <> 'RTN5Cents');
    ```

    :::

## How to Update GST from 6% to 0% (show zero instead of blank) ?

SQL Account system build in report format will automatic detect your Tax Rate based on your invoice issued.

- if invoice issued on May it will show GST @ 6%, while invoice issued on June will display GST @ 0%.
- D/O issued on May, transferred to Invoice and invoice date is in June, then system will automatic detect it and set the GST rate correctly.
- However, if your format is customized previously, you can refer this guideline on how to change the script from GST @ 6% to GST 0% .

1. Click on your report name to enter into report designer page.

   ![1](../../../../static/img/report/RTM-6to0/1.png)

2. Follow the steps below:

   1. Go to **Calc**, click on **View** > select **Module**

      ![2](../../../../static/img/report/RTM-6to0/2.png)

   2. Go **Event Handlers**

   3. Go **Procedure lbTaxAmtOnGetText(var Text:String);**

   4. Replace to this script:

    ```pascal
    var s : string;
    begin
        if (plSQL_0.GetFieldValue('TaxDate') < '01 Jun >2018') or
            VarToCurr(plSQL_1.GetFieldValue('TaxAmt')) <> 0) then

            s := 'GST Amt @ 6% ' else
            s := 'GST Amt @ 0% ';
        if plSQL_2.GetFieldValue('Code') &lt;> '----' >then
            Text := s + '(RM) :' else
            Text := s + ':';
    end;
    ```

   ![3](../../../../static/img/report/RTM-6to0/3.png)

To Display Tax as 0.00 Instead of Blank:

   1. Click on your report name to enter into report designer page.

      ![4](../../../../static/img/report/RTM-6to0/4.png)

   2. Go to **Calc**, click on **View** and select **Events**

      ![5](../../../../static/img/report/RTM-6to0/5.png)

   3. Find **DBTxtTax**and select **OnGetText**, then paste the script as below:

       ```pascal
       begin
           if Trim(plSQL_1.GetFieldValue('TaxAmt')) = '' then
               Text := '0.00' ;
       end;
       ```

      ![6](../../../../static/img/report/RTM-6to0/6.png)

   Once you completed, save the report and exit, then you may preview again your format outcome.