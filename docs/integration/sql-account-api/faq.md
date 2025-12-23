---
sidebar_position: 99
id: sql-account-api-faq
title: FAQ
description: Frequently Asked Questions (FAQ) in SQL Accounting API
slug: /sql-account-api/faq
tags: ["SQL Account", "SQL Account API"]
---

## Error: Record has been changed by another user

When attempting to update (PUT) a data entry such as a sales invoice, this error might trigger. This indicates current update is invalid with an older update count. To fix this, _increment_ the `updatecount` field by 1 after fetching the data from sqlacc.

For example, the original `updatecount` field is 2, and incrementing it to 3 and send for update:

```json
"updatecount": 3,
   "sdsdocdetail": [
      {
         "dtlkey": 99,
         ...
      }
   ]
```

## How to update a Data Entry?

To update a data entry such as a sales invoice, use a payload identical to the creation payload except for the `dtlkey`. In the `sdsdocdetail` payload section, insert the document `dtlkey` retrieved from SQL Account API.

For insert operations, omit the field or set it to -1.

:::warning
If provided dtlkey is invalid, system will treat is as Insert New Record
:::

### Update

```json
"sdsdocdetail": [
      {
         "dtlkey": 99,
         "seq": 1,
         "itemcode": "ISCT",
         "description": "Industrial Style Round Coffee Table - Edited",
      },
]
```

### Insert

```json
{
   "seq": 2,
   "itemcode": "MISC",
   "description": "MISC - New Insert",
},
{
   "dtlkey": -1,
   "seq": 3,
   "itemcode": "RM-04",
   "description": "Arm Rest - New Insert",
}
```

## What is the max limit for GET request?

A maximum of **50 records per request** limit applied for every GET endpoints.

## What are the filters available for GET requests?

In general, there are 3 common filters available:

| **Example GET Method**                             | **Description**                                                                                                                                      |
| -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| `/purchaseinvoice/?docno=PI-00001`                 | Return list (master data only). Can filter by all master table fields.                                                                               |
| `/purchaseinvoice/*?docno=PI-00001&code=400-A0001` | Return single record (master + detail data). Can filter by indexed table fields. Field available: `code`, `docdate`, `docno`, `postdate`, `eiv_utc`. |
| `/purchaseinvoice/{dockey}`                        | Return single record (master + detail data), by path parameter `dockey` only.                                                                        |
