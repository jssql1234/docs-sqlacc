---
title: Membership
sidebar_position: 5
description: A guide to setup membership for SQL POS System
slug: /integration/pos/memebrship
tags: ["SQL Account", "POS"]
---

## Setting

1. Go to setting > system > enable member module

    ![1](../../../static/img/integration/pos/membership/membership-setting.png)

2. Go to SQL Account, need set the posting type by each bill, or each bill (real time)

    - the pos cash sales need posted into SQL Account only the point will be captured

    ![2](../../../static/img/integration/pos/membership/membership-setting1.png)

3. In setting > others, you can setup the membership detail

    ![3](../../../static/img/integration/pos/membership/membership-setting2.png)

4. In setting \> pos screen \> pos title command, add \<check voucher\> \& \<member history\>

    ![4](../../../static/img/integration/pos/membership/membership-setting3.png)

    ![5](../../../static/img/integration/pos/membership/membership-setting4.png)

## Transactions

### Select members during issue bill

![6](../../../static/img/integration/pos/membership/select-members.png)

1. When payment, point entitled for this bill will show at bottom, if you want to redeem voucher / point, then can also click on the voucher button

    ![7](../../../static/img/integration/pos/membership/select-members1.png)

2. Click on deduct point, system will show you balance point, and how much value can redeem, insert your desired redeem value, and confirm voucher.

    ![8](../../../static/img/integration/pos/membership/select-members2.png)

3. Once confirmed, you can see the subtotal RM 50 – voucher RM 35 = Total Amount to pay is RM 15

    ![9](../../../static/img/integration/pos/membership/select-members3.png)

### Add new member

1. Click on the member icon at bottom > Add

    ![10](../../../static/img/integration/pos/membership/add-members.png)

    ![11](../../../static/img/integration/pos/membership/add-members1.png)

2. Insert the name, click on member, to add to phone number, IC No, etc, then click on Add /OK

    ![12](../../../static/img/integration/pos/membership/add-members2.png)

### Search member by phone number or IC No

1. The first search column can search any column you saw on screen like company, code, phone 1, attention, mobile.

2. The 2nd scan, can search by IC Number

    :::note
    if you ic number just now create member time with -, then you need search with -, xxxxxx-xx-xxxx
    :::

    ![13](../../../static/img/integration/pos/membership/search-members.png)

### Check member history

1. After selected the customer > click on member history on top icon

    ![14](../../../static/img/integration/pos/membership/check-member-history.png)

2. All point gained / redeemed will be display, you can preview / print

    ![15](../../../static/img/integration/pos/membership/check-member-history1.png)

### Set birthday discount

1. Go to setting > others, set the birthday discount (on birthday actual date) , or birthday month discount, then set the % of discount entitled.

    ![16](../../../static/img/integration/pos/membership/set-birthday-discount.png)

2. Example today is ALI Bday, when Ali purchase thing from you, during payment, system will auto prompt its Ali birthday, and a 20% discount will be entitled

    ![17](../../../static/img/integration/pos/membership/set-birthday-discount1.png)

## Voucher

### Generate voucher for member?

1. Go to stock item, click on more > generate voucher > new

    ![18](../../../static/img/integration/pos/membership/generate-voucher.png)

    ![19](../../../static/img/integration/pos/membership/generate-voucher1.png)

    :::tip Example
    This example will show generate voucher by redeem point, example this customer available point
    balance is 52,510, if you generate voucher amount is RM 10, system will auto calculate able to
    generate 5 x RM 10 voucher, if you generate RM 20 voucher, system will auto calculate able to
    generate 2 x RM 20 voucher based on the available point balance. In this example, I generate RM 10
    voucher, system auto generated 5 x RM 10 vouchers, you can click on the print icon on right panel,
    to print the voucher.
    :::

    ![20](../../../static/img/integration/pos/membership/generate-voucher2.png)

    So next time when this customer come purchase, during payment, if they provide you the voucher, you can scan / key in the voucher code

2. Click on **voucher** , during payment

    ![21](../../../static/img/integration/pos/membership/generate-voucher3.png)

3. Scan the voucher code / manual search the voucher number, example customer given 3 vouchers, scan / search all the vouchers, click confirm voucher

    ![22](../../../static/img/integration/pos/membership/generate-voucher4.png)

    So the bill RM 99 – Voucher RM 30 = customer to pay is RM 69.

    ![23](../../../static/img/integration/pos/membership/generate-voucher5.png)

### Generate Free Voucher?

1. Go to stock item, click on more > generate voucher > new

2. Example your company given Free voucher for any event, then you can set generate for certain member or all member, then set the voucher amount, the expiry date, and number of vouchers.

    ![24](../../../static/img/integration/pos/membership/generate-free-voucher.png)

### Access right to generate voucher

1. Click on user list > edit the user > others > generate free voucher, generate point voucher

    ![25](../../../static/img/integration/pos/membership/access-right-generate-voucher.png)

    ![26](../../../static/img/integration/pos/membership/access-right-generate-voucher1.png)

### Set default all members / selected member has a percentage discount on bill?

1. In SQL Account, go to stock > maintain stock price tag > create the price tag

    ![27](../../../static/img/integration/pos/membership/set-member-discount.png)

2. In SQL POS, stock item > more > price tag, to set the discount rate > NEW

    ![28](../../../static/img/integration/pos/membership/set-member-discount1.png)

3. Set the discount period, and the discount rate > save

    ![29](../../../static/img/integration/pos/membership/set-member-discount2.png)

### Assign member with price tag?

1. In SQL POS, during create new member, you can add tag the customer below which group.

    ![30](../../../static/img/integration/pos/membership/assign-member-price-tag.png)

2. Choose this member below to which group

    ![31](../../../static/img/integration/pos/membership/assign-member-price-tag1.png)

3. When issue bill, once u selected the member, the discount will inserted automatically.

    ![32](../../../static/img/integration/pos/membership/assign-member-price-tag2.png)
