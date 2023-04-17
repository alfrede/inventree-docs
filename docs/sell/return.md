---
title: Return Order
---

## Return Orders

Return Orders allow stock items (which have been sold or allocted to a customer) to be to be returned into stock, typically for the purpose of repair or refund.

!!! tip "An Order By Any Other Name"
    A Return Order may also be known as an [RMA](https://en.wikipedia.org/wiki/Return_merchandise_authorization) 

### Enable Return Order Functionality

By default, Return Order functionality is not enabled - it must be enabled by a *staff* user from the settings page:

{% with id="enable-return-order", url="sell/return_order_enable.png", description="Enable Return Orders" %}
{% include "img.html" %}
{% endwith %}

Once this setting is enabled, you can access the "Return Orders" page from the main navigation bar:

{% with id="return-order-navbar", url="sell/return_order_navbar.png", description="Access Return Orders" %}
{% include "img.html" %}
{% endwith %}

### Return Order Permissions

[Permissions](../settings/permissions.md) for Return Orders are managed via the `return_order` permission group. Users are assigned appropriate permissions based on the groups they are part of.

### View Return Orders

A list of Return Orders is displayed on the *Return Order* index page:

{% with id="return-order-index", url="sell/return_order_index.png", description="Return Order Index" %}
{% include "img.html" %}
{% endwith %}

Various filters are available to configure which orders are displayed, and how they are arranged.

### Return Order Status Codes

Each Return Order has a specific status code, as follows:

| Status | Description |
| --- | --- |
| Pending | The return order has been created, but not sent to the customer |
| In Progress | The return order has been issued to the customer |
| Complete | The return order was marked as complete, and is now closed |
| Cancelled | The return order was cancelled, and is now closed |

## Create a Return Order

From the Return Order index, click on <span class='badge inventree add'><span class='fas fa-plus-circle'></span> New Return Order</span> which opens the "Create Return Order" form.

A Return Order is linked to a specific customer, which can be selected from the list of existing customers

!!! warning "Customers Only"
	Only companies with the "Customer" attribute enabled will be shown and can be selected

{% with id="return-order-create", url="sell/return_order_create.png", description="Return Order Create" %}
{% include "img.html" %}
{% endwith %}

Fill in the rest of the form with the return order information, and then click on <span class='badge inventree confirm'>Submit</span> to create the order.

### Return Order Reference

Each Return Order is uniquely identified by its *Reference* field. Read more about [reference fields](../settings/reference.md).

### Responsible Owner

The order can be assigned to a responsible *owner*, which is either a user or group. 

## Return Order Detail

Indvidual Return Orders can be viewed via the Return Order detail page:

{% with id="return-order-detail", url="sell/return_order_detail.png", description="Return Order Detail" %}
{% include "img.html" %}
{% endwith %}

Here the details of the return order are available, and specific actions can be performed:

### Edit Return Order

The Return Order can be edit by selecting the <span class='fas fa-edit'></span> icon under the <span class='fas fa-tools'></span> actions menu.

### Line Items

Return Order line items can be added while the [status](#return-order-status-codes) of the order is *In Progress*. Any stock item which is currently sold or assigned to the particular customer can be selected for return.

!!! info "Serialized Stock Only"
    Only stock items which are serialized can be selected for return from the customer

### Extra Line Items

While [line items](#line-items) must reference a particular stock item, extra line items are available for any other itemized information that needs to be conveyed with the order.

## Return Order Reports

Custom [reports](../report/return_order.md) can be generated against each Return Order.