---
sidebar_position: 8
id: first-year-acc-more-than-12
title: Set First Year Account more than 12 Months
description: This guideline is to guide how to setting if your first year account is more than 12 month , below example given is first year account in 18 months. 
slug: /first-year-acc-more-than-12
tags: ["SQL Account", "Tools", "12 months","Account", "First Year"]
---

# Setting for First Year Account more than 12 Months

:::info
This guideline is to guide how to setting if your first year account is more than 12 month , below example given is first year account in 18 months. 
:::

First financial period will in 18 month which is from 1st July 2014 to 31st December 2015.

:::caution
You are advise to set your financial start period and system conversion date as below. 
:::

1) Go Tools > Option > General Ledger > setting your financial start period and system conversion date as 1/1/2014, so in the following year, you do not need to run year end to set again your financial start period & System conversion date.

![1](/img/tools/first-year-acc-more-than-12/1.png)

2) You can follow below step to setting your profit & loss statement print in 18 months which is from 1st July 2014 to 31st December 2015.
![2](/img/tools/first-year-acc-more-than-12/2.png)


2A i & 2A ii. right click as pointed , select 640 x 480 to smaller your SQL Screen <br />
2B i & 2B ii. highlight report name “this year-2column” click and drag it to desktop 
![3](/img/tools/first-year-acc-more-than-12/3.png)


2C. From desktop click the report “This Year-2Column” drag it back to SQL report section.<br />
2D. Click ok
![4](/img/tools/first-year-acc-more-than-12/4.png)

3A. Double click on the new report name “ This year 2 column” in blue color . <br />
3B. Change Period Class to Fixed Date
- Param 1 = Date from eg 1/7/2014
- Param 2 = Date to eg 31/12/2015

3C. You can insert a report name for you easy to differentiate . 