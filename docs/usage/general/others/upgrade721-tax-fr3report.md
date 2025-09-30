---
sidebar_position: 4
title: Upgrade to 721 TaxRate Show A - Fast Report
description: A guide about Upgrade to 721 TaxRate Show A - Fast Report
slug: /usage/general/others/upgrade721-tax-fr3report
tags: ["SQL Account", "Others", "Upgrade", "Report"]
---

## Introduction

This happen if you had write script to get the **TaxRate** from Maintain Tax in the report.

This due to changing SQLAccounting Coding Structure to cater future Changes in Tax Rate.

## Problem

You will get below error when you preview the report.

![1](../../../../static/img/others/yc6-upgrade.jpg)

## Solution

1. Click **Code** Tab
2. Scroll down & look for **procedure SetUp;**
3. Replace this script with below script

![2](../../../../static/img/others/yc7-upgrade.jpg)

```pascal
SQL := 'SELECT Dockey, Tax, TaxRate, Sum(CAST(LocalTaxAmt AS REAL)) LocalTaxAmt, Sum(CAST(LocalAmount AS REAL)) LocalAmount '+
       'FROM Document_Detail ' +
       'WHERE Tax <> '''' ' +
       'GROUP BY Dockey, Tax, TaxRate';
AddDataSet('GSTAmt', ['Tax', 'TaxRate', 'LocalTaxAmt', 'LocalAmount'])
```

4. Click on **Subreport1** tab

![3](../../../../static/img/others/yc8-upgrade.jpg)

5. Double Click the Tax Rate memo
6. Replace this script with below script

![4](../../../../static/img/others/yc9-upgrade.jpg)

```pascal
[IIF(Trim(<GSTAmt."TaxRate">)='',<GSTAmt."Tax">,<GSTAmt."Tax"> +' @ ' + <GSTAmt."TaxRate">)]
```

7. Click **OK** button
8. **Save** the report