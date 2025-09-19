---
sidebar_position: 2
title: General
description: Production Job Order
slug: /usage/production/general
tags: ["SQL Account", "Usage", "Production", "General"]
---

## Overview Workflow

Sales coordinator usually will input the Sales Order (SO) based on the customer PO received. The stock products will be updated into the system as ordered qty. If the stock is purchased from a supplier, then the purchaser has to transfer from SO to PO.

Unless the stock is manufactured, then you have to proceed to the Job Order process. How much of the materials/components required to meet the products ordered by the customer? This question was raised by the Material Planning department. Therefore, the Job Order takes place as the order to be input after the Sales Order. It will plan the materials/components required based on the qty ordered from Sales Order.

When products produce out, you have to transfer the Job Order to the Stock Assembly to commit the stock on hand.

![1](../../../static/img/getting-started/user-guide/production/jj1.png)

![2](../../../static/img/getting-started/user-guide/production/jj2.png)

## Job Order

### Introduction

Sales coordinator usually will input the Sales Order (SO) based on the customer PO received. The stock products will be updated into the system as ordered qty.


How much of the materials/components required to meet the products ordered by the customer? This question was raised by the Material Planning department. Therefore, the Job Order takes place as the order to be input after the Sales Order. It will plan the materials/components required based on the qty ordered from Sales Order. When products produce out, basically you have to transfer the Job Order to the Stock Assembly to commit the stock on hand.


IMPORTANT: It is required for the Job Order module. For more information about price, please refer to our sales personnel.

:::important

It is required the SO -> PO and Job Order module. For more information about price, please refer to our sales personal.

:::

## Sales Order

    1. Create Sales Order (SO)
        
       Go to **Sales | Sales Order**

       Create and save the customer PO into Sales Order.

       ![3](../../../static/img/getting-started/user-guide/production/jj3.png)

    2. SO Check the Available Stock Balance
       
       You can press F11 (Available Stock Balance) on the item code highlighted.

       Below is **CAR** stock available balance.

       ![4](../../../static/img/getting-started/user-guide/production/jj4.png)

       :::note
       
       **Results for CAR Item:**

       SO Qty = -100.00

       PO Qty = 0.00

       JO Qty = 0.00

       Qty (On Hand) = 0.00

       Available Qty = -100.00
       
       :::

       Below is **WHEEL** stock available balance.

       ![5](../../../static/img/getting-started/user-guide/production/jj5.png)

## Purchase Order (Transfer From So)

    1. Create New Purchase Order (PO)
       
       Go to Purchase | Purchase Order

       i.  Click on the NEW button to start with a new PO

       ii. Select the Supplier

       ![6](../../../static/img/getting-started/user-guide/production/jj6.png)

    2. PO Transfer From SO

       i.  Right click on P/Oder (Title)

       ii. Click on Transfer From Sales Order in the menu

       ![7](../../../static/img/getting-started/user-guide/production/jj7.png)

    3. Document Transfer (SO -> PO)

       i.   Pick the Item from the SO list

       ii.  Input X/F Qty to transfer over PO

       iii. Click OK to proceed

            ![8](../../../static/img/getting-started/user-guide/production/jj8.png)

       iv.  Save the PO Document

            Click on the SAVE button

            ![9](../../../static/img/getting-started/user-guide/production/jj9.png)

       v.   PO Check the Available Stock Balance
            
            You can press F11 (Available Stock Balance) on the item code highlighted.

            Below is WHEEL stock available balance

            ![10](../../../static/img/getting-started/user-guide/production/jj10.png)

    :::note

    **Results for CAR Item:**

    SO Qty = -100.00

    PO Qty = -35.00

    JO Qty = 0.00

    Qty (On Hand) = 0.00

    Available Qty = -65.00
    
    :::

## Create New Job Order

CLICK on the NEW button and SELECT the Customer

![11](../../../static/img/getting-started/user-guide/production/jj11.png)

:::info

> **Customer Info from SO**

Basically, the customer and others information copy from SO.

> **Assembly Item Info (Header & Footer)**

Assembly item transferred from SO. It will determine the BOM Components required and the assembly unit cost.

> **BOM Components Details**

Total components quantity requirement to meet the total output.

:::

## Document Transfer (SO --> JO)

1. Create New Job Order (JO)

   Go to **Production | Job Order...**

   i. Click on the NEW button to start with a new JO

   ii. Select the Customer

   ![12](../../../static/img/getting-started/user-guide/production/jj12.png)

2. JO Transfer From SO
   
   i.   Right click on Job Order (Title)

   ii.  Click on Transfer From Sales Order in the menu

   ![13](../../../static/img/getting-started/user-guide/production/jj13.png)

3. Document Transfer (SO --> JO)

   i.   Pick the Item from the SO list

   ii.  Input X/F Qty to transfer over JO

   iii. Click OK to proceed

   ![14](../../../static/img/getting-started/user-guide/production/jj14.png)

4. Show Multilevel BOM in Flat Mode

This function enables it to drill down to the flatten level of the multilevel BOM structure. For example, the CAR multilevel BOM structure.

|**Level 0** | **Level 1** | **Level 2** | **Level 3** |
|---|---|---|---|
|Car | Frame | Front Frame | Orange |
|Car | Frame | Front Frame | Screw |
|Car | Frame | Back Frame | Red Light |
|Car | Frame | Back Frame | Screw |
|Car | Wheel | Rim | 
|Car | Wheel | Tyres | 
|Car | Engine | Engine Block | Filter |
|Car | Engine | Engine Block | Screw |
|Car | Engine | Piston | Tube |
|Car | Engine | Piston | Cover |
|Car | Labour | 

Before FLAT MODE, BOM components show at **LEVEL 1**.

![15](../../../static/img/getting-started/user-guide/production/jj15.png)

Click on Show Multilevel BOM in Flat Mode button.

It will prompt the below message.
