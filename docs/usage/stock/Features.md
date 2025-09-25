---
sidebar_position: 1
title: Features
description: Stock Features
slug: /usage/stock/Features
tags: ["SQL Account", "Usage", "Inventory", "Stock"]
---

## Maintain Stock Group

1. **Stock** > **Maintain Stock Group**.

2. It commonly use to categorize the stock based on the following points into considerations.
    - Brandings, eg. Apple, Sony, Samsung, LG, etc;
    - Different costing method;
    - Product types, eg. raw materials, trading products, manufactured products;
    - To report different sales/purchase account in Profit & Loss Statement.

![229](../../../static/img/getting-started/user-guide/jt1.png)

3. Maintain Stock Group form as shown the screenshot below.

![230](../../../static/img/getting-started/user-guide/jt2.png)

<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation &amp; Properties</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Code</strong></td>
      <td>
        • Input the new Stock Group code <br />
        • Field type: Alphanumerical <br />
        • Length: 20
      </td>
    </tr>
    <tr>
      <td><strong>Description</strong></td>
      <td>
        • Input the Stock Group description <br />
        • Field type: Alphanumerical <br />
        • Length: 200
      </td>
    </tr>
    <tr>
      <td><strong>Costing Method</strong></td>
      <td>
        • Select an appropriate Costing Method for stock valuation <br />
        • Options: FIFO, Weighted Average, Fixed Costing
      </td>
    </tr>
    <tr>
      <td><strong>Sales Code</strong></td>
      <td>• Select a GL Account for Sales</td>
    </tr>
    <tr>
      <td><strong>Cash Sales Code</strong></td>
      <td>• Select a GL Account for Cash Sales</td>
    </tr>
    <tr>
      <td><strong>S.Return Code</strong></td>
      <td>• Select a GL Account for Sales Returns Inward</td>
    </tr>
    <tr>
      <td><strong>Purchase Code</strong></td>
      <td>• Select a GL Account for Purchase</td>
    </tr>
    <tr>
      <td><strong>Cash Purchase Code</strong></td>
      <td>• Select a GL Account for Cash Purchase</td>
    </tr>
    <tr>
      <td><strong>P.Return Code</strong></td>
      <td>• Select a GL Account for Purchase Returns Outward</td>
    </tr>
  </tbody>
</table>


## Maintain Stock Item

1. **Stock** > **Maintain Stock Item**.

2. To setup the stock item list.

![231](../../../static/img/getting-started/user-guide/jt3.png)

### 1.Main Header
1. Maintain Stock Item entry form as shown the screenshot below.

![232](../../../static/img/getting-started/user-guide/jt4.png)

<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation &amp; Properties</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Code</strong></td>
      <td>
        • Input the new Stock Code <br />
        • Field type: Alphanumerical <br />
        • Length: 30
      </td>
    </tr>
    <tr>
      <td><strong>Description</strong></td>
      <td>
        • Input the Stock Description (This usually will appear in most of the documents print-out, eg. invoice, purchase order, etc...) <br />
        • Field type: Alphanumerical <br />
        • Length: 200
      </td>
    </tr>
    <tr>
      <td><strong>2nd Description</strong></td>
      <td>
        • Input the 2nd Description, eg. size, alternative product name <br />
        • Field type: Alphanumerical <br />
        • Length: 200
      </td>
    </tr>
    <tr>
      <td><strong>Serial No.</strong></td>
      <td>
        • Tick to enable serial control items (Requires Serial Number module) <br />
        • Field type: Checkbox
      </td>
    </tr>
    <tr>
      <td><strong>Stock Control</strong></td>
      <td>
        • Tick to enable stock control. System will check availability so stock balance is not below zero or re-order level <br />
        • Field type: Checkbox
      </td>
    </tr>
    <tr>
      <td><strong>Active</strong></td>
      <td>
        • Tick for the stock in use <br />
        • Untick for discontinued stock <br />
        • Field type: Checkbox
      </td>
    </tr>
    <tr>
      <td><strong>Item Group</strong></td>
      <td>• Select an appropriate Stock Group</td>
    </tr>
    <tr>
      <td><strong>Base UOM</strong></td>
      <td>• Enter a base UOM for stock valuation, eg. UNIT</td>
    </tr>
    <tr>
      <td><strong>Ref. Cost</strong></td>
      <td>• Enter a standard cost</td>
    </tr>
    <tr>
      <td><strong>Ref. Price</strong></td>
      <td>• Enter a standard selling price</td>
    </tr>
    <tr>
      <td><strong>Shelf</strong></td>
      <td>• Enter a shelf/rank no., eg. A-01, A-02, A-03 in location A</td>
    </tr>
    <tr>
      <td><strong>Reorder Level</strong></td>
      <td>
        • Enter a stock reorder level to alert new order <br />
        • Refer to menu: Stock \ Print Stock Reorder Advice...
      </td>
    </tr>
    <tr>
      <td><strong>Reorder Qty</strong></td>
      <td>• Enter a reorder qty (MOQ)</td>
    </tr>
    <tr>
      <td><strong>Lead Time</strong></td>
      <td>• Enter a lead time to receive the goods</td>
    </tr>
    <tr>
      <td><strong>Output Tax</strong></td>
      <td>• Enter a default Output Tax</td>
    </tr>
    <tr>
      <td><strong>Input Tax</strong></td>
      <td>• Enter a default Input Tax</td>
    </tr>
    <tr>
      <td><strong>Remark 1</strong></td>
      <td>• Free field to enter extra info</td>
    </tr>
    <tr>
      <td><strong>Remark 2</strong></td>
      <td>• Free field to enter extra info</td>
    </tr>
    <tr>
      <td><strong>Barcode</strong></td>
      <td>• Enter a barcode (represents base UOM)</td>
    </tr>
    <tr>
      <td><strong>Tariff</strong></td>
      <td>
        • Assign a tariff code <br />
        • Lookup from Maintain Tax <br />
        • Related Topic: Maintain_Customer#Tax , Maintain_Supplier#Tax
      </td>
    </tr>
    <tr>
      <td><strong>Bal Qty</strong></td>
      <td>• Display the latest qty balance</td>
    </tr>
  </tbody>
</table>

### 2. UOM
1. Allow to set multiple UOM, eg. 1 carton = 12 units.
2. Beside that, you can set the default UOM for Sales, Purchase and Stock entry form.
3. See the screenshot below.

![233](../../../static/img/getting-started/user-guide/jt5.png)

### 3. Cust.Price
1. Allow to set **multiple pricing/contract price** for customer.
2. You can use **price tag** to tag the price for a customer.
3. It is required **multiple pricing** module.
4. See the screenshot below.

![234](../../../static/img/getting-started/user-guide/jt6.png)

### 4. Supp.Price
1. Allow to set **multiple pricing/contract** price for supplier.
2. You can use **price tag** to tag the price for a supplier.
3. It is required **multiple pricing** module.
4. See the screenshot below.

![235](../../../static/img/getting-started/user-guide/jt7.png)

- Related Topic : [How is the Price Tag work?](https://sites.google.com/site/sqlestream/sql-financial-accounting/7-system-setting/7-20-how-is-the-price-tag-work)

### 5. BOM
1. Allow to setup **recipes/ingredients** for a manufactured product.
2. It is required **Bill of Materials** module.
3. See the screenshot below.

![236](../../../static/img/getting-started/user-guide/8jt.png)

### 6. More Desc.
1. Enter the product details or specifications.
2. See the screenshot below.

![237](../../../static/img/getting-started/user-guide/9jt.png)

> **Tips:**  
> Example view from Sales Tax Invoice:

![238](../../../static/img/getting-started/user-guide/10jt.png)

### 7. Opn Bal.
1. To enter the Opening Stock qty and value balances.

![239](../../../static/img/getting-started/user-guide/11jt.png)

### 8. Category
1. To set the multiple stock category for reporting purpose, eg. country origins, brands, etc.
2. See the screenshot below.

![240](../../../static/img/getting-started/user-guide/12jt.png)

### 9. Alternative
1. Enable to identify the alternative items to replace.

![241](../../../static/img/getting-started/user-guide/13jt.png)

### 10. Cust. Item
1. To enter the **customer item code** and **description**.
2. Purpose is to search or print the customer item code and description in tax invoice instead of using the original item description.

![242](../../../static/img/getting-started/user-guide/14jt.png)


### 11. Supp. Item
1. To enter the **supplier item code** and **description**.
2. Purpose is to search or print the supplier item code and description in purchase invoice instead of using the original item description.

![243](../../../static/img/getting-started/user-guide/15jt.png)


### 12. Barcode
1. To enter the barcode for different UOM.
2. See the screenshot below.

![244](../../../static/img/getting-started/user-guide/16jt.png)


### 13. Note
1. Others stock information.

<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation &amp; Properties</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Item Creation Date</b></td>
      <td>
        <ul>
          <li>Item created date.</li>
          <li>Field type: Date</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Item Matrix</b></td>
      <td>
        <ul>
          <li>Required Stock Matrix module.</li>
          <li>Field type: Lookup</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Min Qty</b></td>
      <td>
        <ul>
          <li>Enter the minimum qty.</li>
          <li>Field type: Float</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Max Qty</b></td>
      <td>
        <ul>
          <li>Enter the maximum qty.</li>
          <li>Field type: Float</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Picture</b></td>
      <td>
        <ul>
          <li>Load a product picture.</li>
          <li>Recommended picture size (jpg or jpeg) less than 16kb.</li>
          <li>Field type: Picture</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Note</b></td>
      <td>
        <ul>
          <li>Enter the product additional information for internal view.</li>
          <li>Field type: Rich Text</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>


2. See the screenshot below.

![245](../../../static/img/getting-started/user-guide/17jt.png)

> **Note:**  
> Do not load the picture size more than 16kb. This is to avoid the database size growth bigger.

## Maintain Stock Category

1. It can be use as to extend to categorize the stock besides the stock group.
2. It allows to set multiple stock category for an stock item code.
3. Commonly use for:-
    1. Brandings, eg. Apple, Sony, Samsung, LG, etc;
    2. Country origins;
    3. Product types, eg. raw materials, trading products, manufactured products;
4. **Stock** > **Maintain Stock Category.**

![246](../../../static/img/getting-started/user-guide/18jt.png)

5. Maintain Stock Category form as shown the screenshot below.

![247](../../../static/img/getting-started/user-guide/19jt.png)

<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation &amp; Properties</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Code</b></td>
      <td>
        <ul>
          <li>Input the new <b>Stock Category</b> code.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 15</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Description</b></td>
      <td>
        <ul>
          <li>Input the <b>Stock Category</b> description.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 200</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Maintain Stock Category Template
1. It is a pre-defined the conditions for Stock Category use in reports.
2. It allows to set the conditions in **AND** or **OR** for stock category.
3. **Stock** > **Maintain Stock Category Template.**

![248](../../../static/img/getting-started/user-guide/20jt.png)

4. Maintain Stock Category Template form as shown the screenshot below.

![249](../../../static/img/getting-started/user-guide/21jt.png)

<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation &amp; Properties</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Code</b></td>
      <td>
        <ul>
          <li>Input the new Stock Category code.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 15</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Description</b></td>
      <td>
        <ul>
          <li>Input the Stock Category description.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 200</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Template</b></td>
      <td>
        <ul>
          <li>To set the pre-defined conditions for stock category.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### How To Set The Template
- Use **OR** condition
1. At the new **Maintain Category View**, click the + sign.
2. Drag the **stock category** selected over into the blank line.

 ![250](../../../static/img/getting-started/user-guide/22jt.png)

3. You will see the stock category added in the template list as per the screenshot below.'

 ![251](../../../static/img/getting-started/user-guide/23jt.png)

- Use **AND** condition
1. At the new **Maintain Category View**, click the **+** sign.
2. Select multiple stock category (**Hold CTRL** + click on **stock category**).
3. Drag the **stock category** selected over into the **blank** line.

  ![252](../../../static/img/getting-started/user-guide/24jt.png)

4. You will see the stock category added in the template list as per the screenshot below.

  ![253](../../../static/img/getting-started/user-guide/25jt.png)

  ![255](../../../static/img/getting-started/user-guide/26jt.png)

## Maintain Item Template
1. It is usually use for a set or package items.  
2. It can be create a template consists of the item selected and use in Sales/Purchase/Stock documents.  
3. **Stock** > **Maintain Item Template**.

![256](../../../static/img/getting-started/user-guide/27jt.png)  

4. Maintain Item Template form as shown the screenshot below.  

![257](../../../static/img/getting-started/user-guide/28jt.png)


<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation &amp; Properties</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Code</b></td>
      <td>
        <ul>
          <li>Input the new Item Template code.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 20</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Description</b></td>
      <td>
        <ul>
          <li>Input the Item Template description.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 200</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Description 2</b></td>
      <td>
        <ul>
          <li>Input the Item Template description 2.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 200</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Reference Price</b></td>
      <td>
        <ul>
          <li>Input the Reference Selling Price.</li>
          <li>Field type: Float</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Item Template</b></td>
      <td>
        <ul>
          <li>Insert the items details.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Matrix</b></td>
      <td>
        <ul>
          <li>To load the Matrix profile.</li>
          <li>It requires Stock Matrix module.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

###  How to Use The Template
  1. For example at the Sales Invoice, click on Item Template (Left Side Bar).
  2. Double click on the Item Template. See the screenshot below.  

  ![258](../../../static/img/getting-started/user-guide/29jt.png)

  3. List of items updated into the Sales Invoice detail. See the screenshot below.

  ![259](../../../static/img/getting-started/user-guide/30jt.png)


## Maintain Item Matrix Profile
1. It commonly use to organize the coding requirement to generate the item code. Very frequent use in the following industries:
2. **Stock** > **Maintain Stock Item Matrix Profile**.

![260](../../../static/img/getting-started/user-guide/31jt.png)

3. Example of the stock item matrix settings to generate the T-Shirt code with different sizes and colors.
4. See the requirement setting as shown in the screenshot below.

![261](../../../static/img/getting-started/user-guide/32jt.png)

5. Matrix setting:-

<table class="table-small">
  <thead>
    <tr>
      <th>Matrix</th>
      <th>Setting</th>
      <th>Length</th>
      <th>Code</th>
      <th>Note</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Prefix</b></td>
      <td>1 - 5</td>
      <td>5</td>
      <td></td>
      <td>To enter a prefix when generating the item code.</td>
    </tr>
    <tr>
      <td><b>Dimension 1 (Row)</b></td>
      <td>7 - 10</td>
      <td>4</td>
      <td>
        <ul>
          <li>BLUE</li>
          <li>YELL</li>
          <li>BLCK</li>
          <li>WHIT</li>
          <li>RED_</li>
        </ul>
      </td>
      <td>Preset code list.</td>
    </tr>
    <tr>
      <td><b>Dimension 2 (Column)</b></td>
      <td>12 - 13</td>
      <td>1</td>
      <td>
        <ul>
          <li>_S</li>
          <li>_M</li>
          <li>_L</li>
          <li>XL</li>
        </ul>
      </td>
      <td>Preset code list.</td>
    </tr>
    <tr>
      <td><b>Separator</b></td>
      <td>-</td>
      <td>1</td>
      <td></td>
      <td>A separator between the prefix, dimension row, and column.</td>
    </tr>
  </tbody>
</table>

> **Note:**  
> Code length must follow as set in Matrix Settings constantly, especially the Dimension 1 (Row) and 2 (Column).

### How Does It Works
  #### Generate Matrix Item Code
  1. Go to Maintain Stock Item.
  2. Right click the area below the **Detail** button.
  3. Click on **Generate Item Code**. See the screenshot below.

![262](../../../static/img/getting-started/user-guide/33jt.png)

  4. Select the **Matrix Profile**,eg. **SHIRT**.
  5. Enter a **Prefix**,eg. **CROC**.
  6. Select an **Item Group**,eg. **T-Shirt**.
  7. Press **Ok** to start generate.

![263](../../../static/img/getting-started/user-guide/34jt.png)

  8. List of CROC item code created in Maintain Stock Item.

![264](../../../static/img/getting-started/user-guide/35jt.png)

 #### Generate Invoice Using Matrix
 1. At Sales Invoice, select one of the prefix item code, eg. **CROC**.

![265](../../../static/img/getting-started/user-guide/36jt.png)

2. Click on **Matrix** tab. You can start enter the quantity in the dimension row and column.

![266](../../../static/img/getting-started/user-guide/37jt.png)

3. Click back to Invoice tab. Item code will be inserted automatically.

![267](../../../static/img/getting-started/user-guide/38jt.png)

## Maintain Location 

1. It is use for warehouse, inter-branch transfer, consignment, van-sales, etc.
2. It is require **Multiple Location (Warehouse)** module.
3. **Stock** > **Maintain Location**.

![268](../../../static/img/getting-started/user-guide/39jt.png)

4. Maintain Location form as shown the screenshot below.

![269](../../../static/img/getting-started/user-guide/40jt.png)

<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation &amp; Properties</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Code</b></td>
      <td>
        <ul>
          <li>Input the new Location code.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 20</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Description</b></td>
      <td>
        <ul>
          <li>Input the Location description.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 200</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Description 2</b></td>
      <td>
        <ul>
          <li>Input the Location description 2.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 200</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Address Line 1</b></td>
      <td>
        <ul>
          <li>Input the Location Address Line 1.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 60</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Address Line 2</b></td>
      <td>
        <ul>
          <li>Input the Location Address Line 2.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 60</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Address Line 3</b></td>
      <td>
        <ul>
          <li>Input the Location Address Line 3.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 60</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Address Line 4</b></td>
      <td>
        <ul>
          <li>Input the Location Address Line 4.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 60</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Attention</b></td>
      <td>
        <ul>
          <li>Input the contact person name.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 70</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Phone 1</b></td>
      <td>
        <ul>
          <li>Input the Phone 1.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 30</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Phone 2</b></td>
      <td>
        <ul>
          <li>Input the Phone 2.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 30</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Fax 1</b></td>
      <td>
        <ul>
          <li>Input the Fax 1.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 30</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Fax 2</b></td>
      <td>
        <ul>
          <li>Input the Fax 2.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 30</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Email</b></td>
      <td>
        <ul>
          <li>Input the Email.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 200</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>ISACTIVE</b></td>
      <td>
        <ul>
          <li>To make the location Active or Inactive.</li>
          <li>Field type: Checkbox</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Note</b></td>
      <td>
        <ul>
          <li>Input the Additional Note to describe the location.</li>
          <li>Field type: Rich Text</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Attachments</b></td>
      <td>
        <ul>
          <li>To insert attachment files, such as Excel, PDF, pictures...</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Maintain Batch 
1. **Batch number** is very useful and widely explore for alternative usage. Commonly usage are:
    - Trace the goods purchased from the suppliers;
    - Trace the returns goods come from which production batch;
    - Differentiate costing of the products;
2. **Stock** > **Maintain Batch**.


![270](../../../static/img/getting-started/user-guide/41jt.png)

3. Fill-in the batch details. See the screenshot below.

![271](../../../static/img/getting-started/user-guide/42jt.png)

<table class="table-small">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Explanation &amp; Properties</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Code</b></td>
      <td>
        <ul>
          <li>Input the new <b>Batch</b> code.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 30</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Description</b></td>
      <td>
        <ul>
          <li>Input the <b>Batch</b> description.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 160</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Expiry Date</b></td>
      <td>
        <ul>
          <li>Set an <b>Expiry Date</b>.</li>
          <li>Field type: Date</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Manufacturing Date</b></td>
      <td>
        <ul>
          <li>Set a <b>Manufacturing Date</b>.</li>
          <li>Field type: Date</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Remark 1</b></td>
      <td>
        <ul>
          <li>Free field.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 200</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>Remark 2</b></td>
      <td>
        <ul>
          <li>Free field.</li>
          <li>Field type: Alphanumerical</li>
          <li>Length: 200</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><b>ISACTIVE</b></td>
      <td>
        <ul>
          <li>To make the batch <b>Active</b> or<b> Inactive</b>.</li>
          <li>Field type: Checkbox</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

4. You can choose to lock the stock item to the batch number. Purpose is to avoid other user assign wrong batch number to an item code.

![272](../../../static/img/getting-started/user-guide/43jt.png)

### Copy & Paste Function
#### Append Batch Existing Number
1. Click on **More** (arrow key down).
2. **Copy Stock Batch**.

![273](../../../static/img/getting-started/user-guide/44jt.png)

3. Click on **New**.
4. Click on **More** (arrow key down).
5. **Paste Stock Batch**.

![274](../../../static/img/getting-started/user-guide/45jt.png)

6. **Batch code** copied and will paste into new batch code as well.
7. Append the batch code and save it.

![275](../../../static/img/getting-started/user-guide/46jt.png)

#### New Batch Number
1. Click on **More** (arrow key down).
2. **Copy Stock Batch**.

![276](../../../static/img/getting-started/user-guide/47jt.png)

3. Click on **New**.
4. Click on **More** (arrow key down).
5. **Paste Stock Batch**.

![277](../../../static/img/getting-started/user-guide/48jt.png)

6. **Batch code** copied and will paste into new batch code as well.
7. Remove the batch number.
8. Click on Save. System will assign a new batch number automatically.

![278](../../../static/img/getting-started/user-guide/49jt.png)

