---
sidebar_position: 16
id: new-acc-XLS-MDB-import
title: New Excel Import Guide
description: A quick guide on Excel Import Program for SQL Account
slug: /miscellaneous/new-acc-XLS-MDB-import
tags: ["SQL Account", "Excel", "Import"]
---

:::info[Download]
Click [here](https://download.sql.com.my/customer/Fairy/SQLAccXLSnMDBImp-setup.exe) to download the XLS n MDB import utility program.
:::

## Requirement
- Firebird Server
- SQL Accounting
- Microsoft Excel or Access

## Example Template
- Updated 16 Jun 2025
- [Example Template-SQLAcc-ImportExcel](https://docs.google.com/spreadsheets/d/1TcFVqH1VCJ5SjHAt2VCHIeTTcQVUjtIBxLaZGGM0E5k/edit#gid=1780239004)
- [Sample output](https://download.sql.com.my/customer/Fairy/Example-CSV.zip)

:::info
**Tips for Programmer to Export Transaction**
01. Use INNER JOIN SQL to join the Master & Detail table 
02. Export to Excel, txt or CSV file
:::

:::info
**Tips for Yeos Transaction Import**
User might had to adjust some data in the excel file
01. Remove the 1st row(i.e 1st row must be a title of the column)
02. PRD Qty & Gross AMT column need * -1 (only for Credit Note) or can use
    [My Excel for Credit Note/Payment is in Negative Value, can it be import?](Http://google.com)
:::

:::info
**Tips for Coca-Cola Transaction Import**
User might had to at Coca-Cola system before export 
01. Group the ARTNUM
02. Net the AMTSUBJECTTOGST & GSTAMT column
It might had rounding issue after import 
(i.e. excel not match with Tax Invoice Issue from coca-cola)
:::

:::info
**Tips for GSK Transaction Import**
01. User might had to convert the file to excel file
02. Export File by Document Type (i.e. Invoice 1 file & Credit Note 1 file)
:::

## Things to Consider
- Float, Currency & Integer type Must not had , (comma) or Currency Symbol & Default Value is 0 not empty
- No Formula in the cell
- No Merge cell is use
- No Hidden column
- Avoid use Unicode Character for Row 1 (Header)
- Date Format should be in dd/mm/yyyy (entry time in Excel as dd/mm/yyyy) - Updated 14 Nov 2013

(image)

- Below is the column type can/can't import

(image)

- Try just use Alphanumeric of the **Worksheet Name**

(image)

- Make sure the **Key of Records** is properly Sorted

(image)

- Special Character (for csv or txt output only)

| User Input            | Text Output                     |
|-----------------------|----------------------------------|
| SalesOrder            | `SalesOrder`                    |
| Sales Order 5' 12"    | `"Sales Order 5' 12""`           |
| SalesOrder6'13"       | `"SalesOrder6'13""`              |
| SalesOrder6" x 13"    | `"SalesOrder6"" x 13""`          |
| Sales Order           | `"Sales Order"`                 |
| Sales Order 5' 12     | `"Sales Order 5' 12"`            |
| Sales Order 12"       | `"Sales Order 12""`              |
| Sales;Order 12        | `"Sales;Order 12"`               |

:::info
For Easy Export you can use " for all output value
Eg "AL","161924123243970563"
:::

## Import Program
- Version (5.19.19.104) - 02 Aug 2025
- Version (4.5.4.37) - 01 Jun 2022 (UE Only) - (Deprecated)
- Evaluation Limit : 100 rows Records per file (Except Master File with not limit)
- [SQLAccXLSnMDBImp-setup.exe](https://download.sql.com.my/customer/Fairy/SQLAccXLSnMDBImp-setup.exe)
- MD5 : A03B8F018B92822D4D3CC59680D9B812

## Steps
### Master Data
Below is example for import Stock Item...

01. Click 1. Get File button
02. Select the File type (eg Microsoft Excel)
(image)

03. Select the File file wanted to import
04. Click **Open**
(image)
(image)
05. Click the combo box (Circle in Red) to select the Worksheet/Table in the file
06. Click **2. Get Data** button to load the file.
07. Drag the available column at the **SourceField** & drop to the **TargetField**.
08. For Detail Part (Circle in Green) (Eg Click on the UOM tab).
09. Click **New** button.
10. Drag the available column at the **SourceField** & drop to the **TargetField** at detail part.
11. Click **Save** after Done (only for Detail Part).
12. Click **Post To A/c** button if all done mapping.

:::info
Blue Circle - Is use to let system know Start from which row till End which row to import.
Orange Circle - The Worksheet/Table records.
:::

## Transaction Data
Below is example for import Customer Invoice...

01. Click 1. Get File button
02. Select the File type (eg Microsoft Excel)

(image)

03. Select the File file wanted to import
04. Click Open

(image)

05. Click the combo box (Icon 5) to select the Worksheet/Table in the file
06. Click 2. Get Data button to load the file.
07. Tick the Is Opening Transactions to import opening balance (Available for AR & AP Module Only).
08. Drag the available column at the SourceField & drop to the TargetField.
09. Click 3. Verify button.
10. Click 4. Post To A/c button if confirm all data is Ok.

:::info
Do you realise there is an arrow near the **Verify** button?
In the arrow there is an Option **A.Load Setting...,** this to load previously mapped fields
:::

## Transactions Data - Get File 3
- This Option only for Excel
- Only available in Version 4.6.3.19 & above

01. Click arrow at the 1. Get File button
(image)

02. Select Get File 3... & system will prompt 2 dialog like below
(image)

03. Select the Excel Header File.
(image)

04. Select the Excel Detail File.
(image)

05. Click the combo box to select the Worksheet/Table for each Header & Detail file
06. Click the combo box to select the Key Field to link both Header & Detail file
07. Click **4. Get Data** button
(image)

08. Enter the Merge File name.
09. Click Save button.

## Options
- Only available in Version 4.3.2.14 & above

### Check Duplicate Records
Menu: Tools | Check Duplicate Records...

This Function is to check the duplicate records for the selected file
01. Follow from Step 1 to 6 as above.
(image)

07. Tick the Column(s) to Group
08. Click 3. Verify... button
(image)

### Split Memo to Columns
Menu: Tools | Split Memo to Columns...

This option is to Split the memo (Data more then 1 row in the cell) into individual Columns.
01. Follow from Step 1 to 6 as above.
(image)

07. Set Number of Column(s) to split (Default is 4).
08. Select the Column to be Split
09. Click **5. Split** button.
(image)

10. Scroll to the right. Highlight in Yellow is the newly Columns Created.
11. Click 6. Export Excel(*.xls) to export out the Result.

### Split String to Columns
Menu: Tools | Split String to Columns...

This option is to Split the Long String into individual Columns (Max. 60 Character each Column).
- Only available in Version 5.10.10.42 & above
01. Follow from Step 1 to 6 as above.
(image)

07. Set Number of Column(s) to split (Default is 4).
08. Select the Column to be Split
09. Click 5. Split button.
(image)

10. Scroll to the right. Highlight in Yellow is the newly Columns Created.
11. Click 6. Export Excel(*.xls) to export out the Result.

### Convert Rows to Columns
Menu: Tools | Convert Rows to Columns...

Only available in Version 4.3.2.15 & above
01. Follow from Step 1 to 6 as above.
(image)

07. Set Number of Column(s) to split (Default is 4).
08. Select the Column to be Convert
09. Click 5. Convert button.
(image)

10. Scroll to the right. Highlight in Yellow is the newly Columns Created.
11. Click 6. Export Excel(*.xls) to export out the Result.

:::info
System will use
The 1st column in excel as a Key of Grouping.
The empty row as "Reset/End of" Record.
:::

## Auto Import
-Only available
\- in Version 4.9.6.31 & above.
\- for Registered import Database.
\- in <span style={{ color: "blue", fontWeight: "bold" }}>
  Firebird Server Setting
</span> (Standalone can't Auto Import)
- Excel Filename must be <span style={{ color: "blue", fontWeight: "bold" }}>
  BIZOBJECT.YYYYMMDDHHMMSS.xlsx
</span> eg SL_IV.20190214101508.xlsx
- Must only 1 Sheet in Excel File.
- Must <span style={{ color: "blue", fontWeight: "bold" }}>
  Manually Import for 1st time
</span> use to make sure is success mapping. - Auto Import base on last mapping import

### Import Setting
Menu: File | Auto Import Settings...
(image)

01. Select SQL Accounting DCF file
02. Select SQL Accounting Database to import & export
03. Enter the SQL Accounting User Name & Password
04. Select/Tick to Enable Download From FTP (available in Version Build 32 & above)
05. Select/Tick to Enable With Export CSV File (available in Version Build 85 & above)
06. Click Next

(image)

The following Steps if Download From FTP is Enable/Tick/Selected
07. Enter the Host/IP Address for FTP
08. Enter the FTP Port No
09. Enter the FTP User Name & Password
10. Enter the FTP Folder to download From
11. Select the Action to Do After Download
12. Click Test Connection...
13. Click Next

| Action                                                   | Description                                                                                                                |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Delete the file(s) in FTP Folder                          | Will delete the file(s) after download                                                                                      |
| Move to Archive/YYYYMMDD Folder                           | Will Auto Create YYYYMMDD & move to this folder after done download <br/> Make sure in the FTP folder had the folder Archive (eg download/Archive) |
| Leave it As It (I will self Manually Delete or Move it)    | Do nothing after Download                                                                                                   |

:::info
	The file will download to the Pending Folder which is set at the Last Steps
:::

(image)

14. Select the Biz Object Type/Document Type to Import
15. Click Next

(image)

16. Select the Pending folder where Excel files keep to import to SQL Accounting
17. Select the Done folder to move after done import the Excel file

| Field                  | Description                                                         |
|------------------------|----------------------------------------------------------------------|
| Include SubFolder File(s) | This option is for User who have More than 1 system                 |
| Export Log File           | To Auto Export out for Log file to the selected folder             |
| Last Import Date          | Last Import Date and Time. System will auto update                |
| Keep Last Log Line        | To show last how many line for Log                                 |

17. Click Next
(image)

18. Select Export folder
19. Select Last Date To
20. Click + to add
21. Enter Description, SQL Query & Export File Name
22. Click Check for Save

| Parameter         | Description                                                                                                           |
|-------------------|-----------------------------------------------------------------------------------------------------------------------|
| Last Date To      | Data End Date to Export From SQL Accounting.<br/>System will use this Date + 1<br/>Eg To Export 12 Nov 2018 just set the date as 11 Nov 2018 |
| Text Export...    | To manually export selected Record Query                                                                              |
| Description       | Description for the Query                                                                                            |
| SQL Query         | A Query to Export Data                                                                                               |
| Export File name  | A CSV file name                                                                                                      |
## Video
- [Import Excel - Stock](-)
- [Import Excel - Maintain Customer](-)
- [Import Excel - GL Account](-)
- [Import Excel - Transactions](-)

