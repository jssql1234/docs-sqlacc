---
sidebar_position: 9
title: Settings
description: Guide to Settings
slug: /integration/xstore/settings
tags: ["e-Commerce", "X-Store", "Settings"]
---

The Settings module consists of these main sections to help you manage your organization:

- **Company** - Manage your organization's profile and configuration
- **Users** - Control team member access and invitations
- **Permissions** - Define roles and access control
- **Post Orders** - Post invoices for the orders to SQL Account
- **Customize Template** - Customize Picking List Template

## Company

:::info
Check out our [Setup Guide](../xstore/setup#step-1-create-company) for detailed instructions on creating your company profile.
:::

View and update your company information, including business details and API configurations.

![company-overview](../../../static/img/xstore/settings/company-overview.png)

### Company Profile

Your company profile displays:

- Company ID
- Company name
- Logo
- Registration number
- Email address
- Phone number

![company-profile](../../../static/img/xstore/settings/company-profile.png)

#### Update Company Logo

Click on your current logo to upload a new one.

![company-logo](../../../static/img/xstore/settings/company-logo.png)

#### SQL Account Integration

:::info
For more details on SQL Account configuration, see our [Setup Guide](../xstore/setup#step-3-configure-company-settings).
:::

You may add your SQL Account configuration here:

1. System Conversion Date
2. SQL Account Access Key and Secret Key

You can click **Test Connection** to verify the connection with the SQL Account API service. A green dot indicates a successful connection, and clicking it will display the SQL Account API version. A red dot indicates a connection error, and clicking it will display the error message.

![company-keys](../../../static/img/xstore/settings/company-keys.png)

#### Company Setting

Enable specific company features such as enabling **Auto Synchronize Quantity to Platform** and update your desired default **Post Order Option** whether to *Manual Post* or *Post All*.

![company-sync](../../../static/img/xstore/settings/company-sync.png)

### Editing Company Details

**To update your company information:**

1. Click the **Update Company Details** button

   ![company-update-details-button](../../../static/img/xstore/settings/company-update.png)

2. Modify any of the following fields:

   - Company name
   - Registration number
   - Email address
   - Phone number

3. Click **Save** to apply changes

![company-form](../../../static/img/xstore/settings/company-form.png)

:::warning Validation Required
You must provide a valid email address and phone number. Invalid entries will trigger a warning message.
:::

![company-validate](../../../static/img/xstore/settings/company-validate.png)

#### Canceling Changes

If you click **Cancel** after making edits, you'll see a confirmation dialog. Click **Continue** to discard your changes.

![company-cancel](../../../static/img/xstore/settings/company-cancel.png)

## Users

Manage your team members, including viewing, editing, inviting, and removing users.

![user-management-overview](../../../static/img/xstore/settings/user-management-overview.png)

### Active Users Table

The users table displays all team members with their name, ID (with copy function), email, phone number, assigned role, status, and actions. Use the search bar to filter users by name, ID, email, or phone number. Your account always appears in the first row.

![user-management-table](../../../static/img/xstore/settings/user-management-table.png)

| Column         | Description                 |
| -------------- | --------------------------- |
| User Name & ID | Full name with copyable ID  |
| Email          | Contact email address       |
| Phone Number   | Contact phone number        |
| Role           | User role in company        |
| Status         | User status in company      |
| Actions        | Edit and Remove user        |

### Editing User Details

You can modify a user's role and status directly in the table.

1. Click the **Edit** icon in the user's row
2. Update the desired fields.
3. Click the **Save** button.

![user-management-update](../../../static/img/xstore/settings/user-management-update.png)

### Removing Users

1. Click the **Delete** icon in the user's row
2. Type `delete user` in the confirmation dialog
3. Click **Continue** to remove the user

![user-management-remove-user](../../../static/img/xstore/settings/user-management-remove-user.png)

### Inviting New Users

#### Step 1: Enter User Details

1. Click the **Invite Users** button
2. In the dialog, enter either:
   - Email address (press Enter after each email)
   - User ID
3. Click **Batch Invite** to add users to the invitation list

:::info Finding User ID
User IDs appear in the users table. Ask the person you want to invite to copy their ID and send it to you.
:::

![user-invitation-input](../../../static/img/xstore/settings/user-invitation-input.png)

#### Step 2: Assign Roles and Send

1. Select a role from the **Role** dropdown for each user
2. Click **Send Invitation** to send all invitations
3. Use **Clear All** to remove all pending invitations from the list

![user-invitation-send](../../../static/img/xstore/settings/user-invitation-send.png)

#### Step 3: Review Invitation Status

After sending, you'll see a status summary showing:

| Status     | Meaning                         |
| ---------- | ------------------------------- |
| ✅ Success | Invitation sent successfully    |
| ℹ️ Exist   | User already joined the company |
| ❌ Failed  | Invitation could not be sent    |

![user-invitation-status](../../../static/img/xstore/settings/user-invitation-status.png)

### Managing Pending Invitations

Click **Pending Invitations** to switch to the pending list view.

- Shows invitations not yet accepted
- Includes a **Revoke** button for each invitation
- Invitations expire after 24 hours
- Expired invitations must be resent

![user-invitation-pending-list](../../../static/img/xstore/settings/user-invitation-pending-list.png)

### Accepting Invitations

Recipients receive an email with an invitation link.

:::tip Invitation with User ID
Users invited by User ID join the company immediately without needing to accept an invitation.
:::

![user-invitation-email](../../../static/img/xstore/settings/user-invitation-email.png)

#### Option 1: Sign in with Passkey

Log in using a Passkey and redirect to the Company List page.

:::info Prerequisite
You must register a user account with a passkey before using this method to accept the invitation.
:::

![user-invitation-accept-passkey](../../../static/img/xstore/settings/user-invitation-accept-passkey.png)

#### Option 2: Sign up with Email

Register a new account, log in automatically, and redirect to the Company List page.

![user-invitation-accept-email](../../../static/img/xstore/settings/user-invitation-accept-email.png)

## Permissions

:::info
Currently, adding, editing, and deleting roles are not available.
:::

Define and manage roles with specific permissions to control what users can do in the system.

The roles table displays:

- Role name
- Last updated date
- Updated by (user name)
- Action buttons (Edit, Delete)

![permissions-overview](../../../static/img/xstore/settings/permissions-overview.png)

### Editing Roles

1. Click the **Edit** icon in the role's row
2. Update the role name or adjust permissions
3. Click **Update Role**
4. Confirm your changes by clicking **Continue**

![permissions-role-edit](../../../static/img/xstore/settings/permissions-role-edit.png)

### Deleting Roles

1. Click the **Delete** icon
2. Confirm the deletion in the dialog

:::warning Deletion Requirements
Roles can only be deleted if they're not assigned to any users. If the role is in use, you'll see a warning message.
:::

![permissions-role-delete](../../../static/img/xstore/settings/permissions-role-delete.png)

### Creating New Roles

1. Click **Create Role** at the top right of the table

   ![permissions-role-create-button](../../../static/img/xstore/settings/permissions-role-create-button.png)

2. In the dialog:
   - Enter a role name
   - Select the permissions to assign
3. Click **Create Role**
4. Confirm by clicking **Continue**

![permissions-role-create-dialog](../../../static/img/xstore/settings/permissions-role-create-dialog.png)

## Post Order

View orders in the Shipped, Delivered, or Completed state and post their invoices to SQL Account. This section has two tabs:

1. **Unposted Tab**: Orders that haven't been posted yet, or orders that were updated after their last posting date (i.e., the order's updated date is later than its posted date).
2. **Posted Tab**: Orders that have already been posted and have no changes since.

![post-overview](../../../static/img/xstore/settings/post-overview.png)

You can change the View Options to see more order details, or use the filter options to narrow down which orders are displayed. By default, orders are filtered to those created within the last 30 days. You can include older orders by adjusting the filter options.

![post-view](../../../static/img/xstore/settings/post-view.png)

### Posting

1. Select the orders you want to post, then click **Post Selected**. To select every order that matches your current filters, click **Select all filtered items**.

   ![post-selection](../../../static/img/xstore/settings/post-selection.png)

2. To post all filtered orders in the **Unposted Tab** at once, click the dropdown next to **Post Selected** and choose **Post All**. You can also set your preferred posting option in advance under [Company Setting](#company-setting).

   ![post-all](../../../static/img/xstore/settings/post-all.png)

3. Clicking **Post Selected** opens a confirmation dialog. Check **Include Cancelled Orders** if you want cancelled orders posted along with the rest, then click **Continue** to proceed. Click **Cancel** to back out without posting.

   ![post-confirmation](../../../static/img/xstore/settings/post-confirmation.png)

4. A progress card shows the status of the posting process. If **Include Cancelled Orders** isn't selected, cancelled orders are shown as skipped. Orders still waiting to be processed are shown as queued.

   ![post-progress](../../../static/img/xstore/settings/post-progress.png)

5. Once posting completes, successfully posted orders move to the **Posted Tab** and their *Posted Date* is updated. Orders that fail to post stay in the current tab, with the failure reason shown in the **Post Status** column.

   ![post-success](../../../static/img/xstore/settings/post-success.png)

6. If an order fails to post with the reason *"Shop SKU not mapped to SQL Account stock item"*, open the order's details page to map the SKU accordingly.

   ![post-map](../../../static/img/xstore/settings/post-map.png)

### Failed Posting

1. Click **View Failed Results** to see orders that failed to post in the previous post process, along with their failure reasons.
2. Filter orders by failure reason.
3. Select the relevant orders individually, or use **Select all filtered items** to select every order with a matching failure reason.
4. Repost selected orders.

This is useful once you've resolved the underlying cause of a failure and want to retry posting those orders.

![post-failed](../../../static/img/xstore/settings/post-failed.png)

## Customize Template

Personalize the appearance and layout of **Picking List** according to requirements. Users can preview the template while making changes and adjust various template settings before saving it.

1. Click **Settings > Customize Template** in the sidebar

   ![customize-sidebar](../../../static/img/xstore/settings/customize-sidebar.png)

2. Users can customize the template and click **Apply** to preview how the Picking List will look with their selected settings. Once satisfied with the changes, click **Save** to save the customized template settings.

   ![customize-btn](../../../static/img/xstore/settings/customize-btn.png)

3. A success message will be displayed after the customized template settings are saved successfully.

   ![customize-success](../../../static/img/xstore/settings/customize-success.png)

4. Certain essential information is required and cannot be hidden.

   ![customize-required](../../../static/img/xstore/settings/customize-required.png)