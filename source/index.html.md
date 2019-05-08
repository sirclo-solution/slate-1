--- 
title: Order 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

**Welcome To SIRCLO API Documentation**
You can used this API to connect your backend system to Sirclo system. 

**Version:** 1.0 

# Authentication 

Authentication & Authorization is handled by Oauth from Sirclo account module.

<aside class="notice">
All request to fulfillment control are authenticated and authorized using a mechanism discussed in <code>Authentication</code> Section.
</aside>

# Order API 
## Get All Orders


**Description:** Get All Orders 

### HTTP Request 
`***GET*** /order` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "orders": [
        {
            "id": 111,
            "created_at": "2018-11-07T03:46:16.457936Z",
            "updated_at": "2018-11-07T03:46:16.457938Z",
            "order_number": "",
            "order_date": "2018-11-07T03:40:57Z",
            "customer_code": "",
            "remote_order_id": "1362230256",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "181362230256",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "",
            "delivery_name": "Danny",
            "delivery_street_address": "Jl Biak no 19C\r\nsebelah Bank Permata",
            "delivery_street_address_2": "",
            "delivery_suburb": "Gambir",
            "delivery_city": "Jakarta Pusat",
            "delivery_region": "DKI Jakarta",
            "delivery_post_code": "10150",
            "delivery_country": "Indonesia",
            "delivery_method": "JNE REG",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "pending",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 45000,
            "discount_total": 0,
            "subtotal": 2500,
            "total": 47500,
            "order_status": "",
            "remarks": "",
            "marketplace_code": "bklp",
            "phone_number": "087867255331",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "0001-01-01T00:00:00Z",
            "accepted_at": "0001-01-01T00:00:00Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        },
        {
            "id": 5,
            "created_at": "2018-11-06T10:00:10.569693Z",
            "updated_at": "2018-11-07T21:00:10.873379Z",
            "order_number": "",
            "order_date": "2018-11-05T08:29:23Z",
            "customer_code": "",
            "remote_order_id": "214",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "201800242",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "bank-transfer",
            "delivery_name": "Danny ",
            "delivery_street_address": "Melati 6 no 38 Kapuk Cengkareng ",
            "delivery_street_address_2": "",
            "delivery_suburb": "",
            "delivery_city": "Kota Jakarta Barat - Cengkareng",
            "delivery_region": "DKI Jakarta",
            "delivery_post_code": "11720",
            "delivery_country": "Indonesia",
            "delivery_method": "JNE REG",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "Shipped",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 9000,
            "discount_total": 0,
            "subtotal": 450000,
            "total": 459000,
            "order_status": "packed",
            "remarks": "zxcv",
            "marketplace_code": "srcl",
            "phone_number": "087867255331",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "2018-11-05T08:29:23Z",
            "accepted_at": "2018-11-06T10:00:10.569613Z",
            "packed_at": "2018-11-06T10:00:10.569613Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        }
    ]
}
```

## Get Order

**Summary:** GetOrder

**Description:** Get single order 

### HTTP Request 
`***GET*** /order/{orderID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| orderID | path | Specific order id to get information from | Yes | integer |

**Responses**

> The above command returns JSON structured like this:

```json
    {
    "order": {
        "id": 5,
        "created_at": "2018-11-06T10:00:10.569693Z",
        "updated_at": "2018-11-09T02:00:09.206881Z",
        "order_number": "",
        "order_date": "2018-11-05T08:29:23Z",
        "customer_code": "",
        "remote_order_id": "214",
        "currency_code": "IDR",
        "exchange_rate": 1,
        "customer_reference": "201800242",
        "quote_expiry_date": "0001-01-01T00:00:00Z",
        "required_date": "0001-01-01T00:00:00Z",
        "warehouse_code": "",
        "payment_method": "bank-transfer",
        "delivery_name": "Danny ",
        "delivery_street_address": "Melati 6 no 38 Kapuk Cengkareng ",
        "delivery_street_address_2": "",
        "delivery_suburb": "",
        "delivery_city": "Kota Jakarta Barat - Cengkareng",
        "delivery_region": "DKI Jakarta",
        "delivery_post_code": "11720",
        "delivery_country": "Indonesia",
        "delivery_method": "JNE REG",
        "delivery_number": "",
        "delivery_method_code": "",
        "delivery_enterprise_code": "",
        "delivery_enterprise_name": "",
        "buyer_delivery_number": "",
        "remote_order_status": "Shipped",
        "discount": 0,
        "tax_code": "PPN",
        "tax_rate": 0.1,
        "tax_total": 0,
        "shipping_total": 9000,
        "discount_total": 0,
        "subtotal": 450000,
        "total": 459000,
        "order_status": "packed",
        "remarks": "zxcv",
        "marketplace_code": "srcl",
        "phone_number": "087867255331",
        "airwaybill_number": "",
        "shipment_reference": "",
        "shipment_extras": "",
        "processed_at": "2018-11-05T08:29:23Z",
        "accepted_at": "2018-11-06T10:00:10.569613Z",
        "packed_at": "2018-11-06T10:00:10.569613Z",
        "cancelled_at": "0001-01-01T00:00:00Z",
        "shipment_tracked_at": "0001-01-01T00:00:00Z",
        "edited_at": "0001-01-01T00:00:00Z",
        "exported_at": "0001-01-01T00:00:00Z",
        "printed_at": "0001-01-01T00:00:00Z",
        "accepted_by": 0,
        "packed_by": 0,
        "cancelled_by": 0,
        "printed_by": 0,
        "line_items": [
            {
                "id": 5,
                "created_at": "2018-11-06T10:00:10.865249Z",
                "updated_at": "2018-11-09T02:00:09.209977Z",
                "line_number": 1,
                "remote_order_item_id": "91",
                "product_code": "DR0001",
                "product_description": "Sophie Dress",
                "order_quantity": 1,
                "unit_price": 409090.90909090906,
                "raw_price": 450000,
                "discount_rate": 0,
                "discount_amount": 0,
                "line_discount": 0,
                "line_tax": 40909.09090909091,
                "shipping_amount": 9000,
                "line_total": 450000,
                "line_comments": "",
                "line_item_status": "",
                "description": "",
                "is_user_entry": false,
                "source": "srcl"
            }
        ],
        "store_id": 4,
        "store_name": "",
        "comment": "",
        "price_adjustment": 0,
        "edit_reason": "",
        "cancel_reason": ""
    }
}
```

## Get Order Count 

**Summary:** OrderCount

**Description:** 

### HTTP Request 
`***GET*** /order/count` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |

**Responses**

> The above command returns JSON structured like this:

```json
{"order_count":{"pending":66,"accepted":32,"packed":7,"cancelled":0,"completed":0}} 
```

## Get Pending Orders

**Summary:** GetPendingOrders

**Description:** 

### HTTP Request 
`***GET*** /order/pending` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| last_id | query | Specific Last id to get information from | No | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "orders": [
        {
            "id": 48,
            "created_at": "2018-11-06T10:00:15.292263Z",
            "updated_at": "2018-11-07T21:00:11.678398Z",
            "order_number": "",
            "order_date": "2018-11-01T04:50:13Z",
            "customer_code": "",
            "remote_order_id": "122",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "201800060;Pending;Rp 658",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "",
            "delivery_name": "",
            "delivery_street_address": "",
            "delivery_street_address_2": "",
            "delivery_suburb": "",
            "delivery_city": "",
            "delivery_region": "",
            "delivery_post_code": "",
            "delivery_country": "",
            "delivery_method": "",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "Processing",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 0,
            "discount_total": 0,
            "subtotal": 0,
            "total": 0,
            "order_status": "pending",
            "remarks": "",
            "marketplace_code": "srcl",
            "phone_number": "",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "2018-11-01T04:50:13Z",
            "accepted_at": "0001-01-01T00:00:00Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        },
        {
            "id": 33,
            "created_at": "2018-11-06T10:00:13.580142Z",
            "updated_at": "2018-11-07T21:00:11.345521Z",
            "order_number": "",
            "order_date": "2018-11-01T04:50:13Z",
            "customer_code": "",
            "remote_order_id": "137",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "201800050;Pending;Rp 1",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "",
            "delivery_name": "",
            "delivery_street_address": "",
            "delivery_street_address_2": "",
            "delivery_suburb": "",
            "delivery_city": "",
            "delivery_region": "",
            "delivery_post_code": "",
            "delivery_country": "",
            "delivery_method": "",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "Processing",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 0,
            "discount_total": 0,
            "subtotal": 0,
            "total": 0,
            "order_status": "pending",
            "remarks": "",
            "marketplace_code": "srcl",
            "phone_number": "",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "2018-11-01T04:50:13Z",
            "accepted_at": "0001-01-01T00:00:00Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        },
    ]
}
```
## Post Accepted Orders

**Summary:** PostAcceptedOrders

**Description:** 

### HTTP Request 
`***POST*** /order/{orderID}/accepted` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| orderID | path| Order ID which selected to accept | Yes | integer |
| params | body | Accept params with order number | Yes | integer |

> Body Parameters 

```json
{
    "order_number":""
}
```

**Responses**

> The above command returns JSON structured like this:

```json
{
    "Message":"200 OK"
}
```

## Get Accepted Orders

**Summary:** GetAcceptedOrders

**Description:** 

### HTTP Request 
`***GET*** /order/accepted` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| last_id | query | Specific Last id to get information from | No | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "orders": [
        {
            "id": 28,
            "created_at": "2018-11-06T10:00:13.282615Z",
            "updated_at": "2018-11-08T08:00:09.168292Z",
            "order_number": "",
            "order_date": "2018-11-01T04:27:52Z",
            "customer_code": "",
            "remote_order_id": "142",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "201800148",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "bank-transfer",
            "delivery_name": "Danny ",
            "delivery_street_address": "Melati 6 no 38 Kapuk Cengkareng ",
            "delivery_street_address_2": "",
            "delivery_suburb": "",
            "delivery_city": "Kota Jakarta Barat - Cengkareng",
            "delivery_region": "DKI Jakarta",
            "delivery_post_code": "11720",
            "delivery_country": "Indonesia",
            "delivery_method": "JNE REG",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "Processing",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 27000,
            "discount_total": 0,
            "subtotal": 525000,
            "total": 552000,
            "order_status": "accepted",
            "remarks": "",
            "marketplace_code": "srcl",
            "phone_number": "087867255331",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "2018-11-01T04:27:52Z",
            "accepted_at": "2018-11-06T10:00:13.28256Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        },
        {
            "id": 96,
            "created_at": "2018-11-06T10:00:30.084335Z",
            "updated_at": "2018-11-08T08:00:10.54573Z",
            "order_number": "",
            "order_date": "2018-11-01T04:27:52Z",
            "customer_code": "",
            "remote_order_id": "74",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "201800048",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "bank-transfer",
            "delivery_name": "Danny ",
            "delivery_street_address": "Melati 6 no 38 Kapuk Cengkareng ",
            "delivery_street_address_2": "",
            "delivery_suburb": "",
            "delivery_city": "Kota Jakarta Barat - Cengkareng",
            "delivery_region": "DKI Jakarta",
            "delivery_post_code": "11720",
            "delivery_country": "Indonesia",
            "delivery_method": "JNE REG",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "Processing",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 27000,
            "discount_total": 0,
            "subtotal": 0,
            "total": 27000,
            "order_status": "accepted",
            "remarks": "",
            "marketplace_code": "srcl",
            "phone_number": "087867255331",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "2018-11-01T04:27:52Z",
            "accepted_at": "2018-11-06T10:00:30.084259Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        }
    ]
}
```

## Post Packed Orders

**Summary:** PostPackedOrders

**Description:** 

### HTTP Request 
`***POST*** /order/{orderID}/pack` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| orderID | path| Order ID which selected to accept | Yes | integer |
| params | body | packed params with airwaybill number | Yes | integer |

> Body Parameters 

```json
{
    "airwaybill_number":""
}
```

**Responses**

> The above command returns JSON structured like this:

```json
{
    "Message":"200 OK"
}
```

## Get Packed Order

**Summary:** GetPackedOrders

**Description:** 

### HTTP Request 
`***GET*** /order/packed` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| last_id | query | Specific Last id to get information from | No | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "orders": [
        {
            "id": 5,
            "created_at": "2018-11-06T10:00:10.569693Z",
            "updated_at": "2018-11-08T08:00:08.831873Z",
            "order_number": "",
            "order_date": "2018-11-05T08:29:23Z",
            "customer_code": "",
            "remote_order_id": "214",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "201800242",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "bank-transfer",
            "delivery_name": "Danny ",
            "delivery_street_address": "Melati 6 no 38 Kapuk Cengkareng ",
            "delivery_street_address_2": "",
            "delivery_suburb": "",
            "delivery_city": "Kota Jakarta Barat - Cengkareng",
            "delivery_region": "DKI Jakarta",
            "delivery_post_code": "11720",
            "delivery_country": "Indonesia",
            "delivery_method": "JNE REG",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "Shipped",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 9000,
            "discount_total": 0,
            "subtotal": 450000,
            "total": 459000,
            "order_status": "packed",
            "remarks": "zxcv",
            "marketplace_code": "srcl",
            "phone_number": "087867255331",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "2018-11-05T08:29:23Z",
            "accepted_at": "2018-11-06T10:00:10.569613Z",
            "packed_at": "2018-11-06T10:00:10.569613Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        },
        {
            "id": 6,
            "created_at": "2018-11-06T10:00:11.126521Z",
            "updated_at": "2018-11-08T08:00:08.851102Z",
            "order_number": "",
            "order_date": "2018-11-02T02:29:42Z",
            "customer_code": "",
            "remote_order_id": "213",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "201800241",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "bank-transfer",
            "delivery_name": "Danny ",
            "delivery_street_address": "Melati 6 no 38 Kapuk Cengkareng ",
            "delivery_street_address_2": "",
            "delivery_suburb": "",
            "delivery_city": "Kota Jakarta Barat - Cengkareng",
            "delivery_region": "DKI Jakarta",
            "delivery_post_code": "11720",
            "delivery_country": "Indonesia",
            "delivery_method": "JNE REG",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "Shipped",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 27000,
            "discount_total": 0,
            "subtotal": 489000,
            "total": 516000,
            "order_status": "packed",
            "remarks": "coba pake message",
            "marketplace_code": "srcl",
            "phone_number": "087867255331",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "2018-11-02T02:29:42Z",
            "accepted_at": "2018-11-06T10:00:11.126466Z",
            "packed_at": "2018-11-06T10:00:11.126466Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        }
    ]
}
```

## Get Finished Orders

**Summary:** GetFinishedOrders

**Description:** 

### HTTP Request 
`***GET*** /order/finished` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| last_id | query | Specific Last id to get information from | No | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "orders": [
        {
            "id": 70,
            "created_at": "2018-11-06T10:00:27.245501Z",
            "updated_at": "2018-11-08T08:00:10.140689Z",
            "order_number": "",
            "order_date": "2018-11-01T04:50:13Z",
            "customer_code": "",
            "remote_order_id": "100",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "201800072;Pending;Rp 3",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "",
            "delivery_name": "",
            "delivery_street_address": "",
            "delivery_street_address_2": "",
            "delivery_suburb": "",
            "delivery_city": "",
            "delivery_region": "",
            "delivery_post_code": "",
            "delivery_country": "",
            "delivery_method": "",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "Cancelled",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 0,
            "discount_total": 0,
            "subtotal": 0,
            "total": 0,
            "order_status": "cancelled",
            "remarks": "",
            "marketplace_code": "srcl",
            "phone_number": "",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "2018-11-01T04:50:13Z",
            "accepted_at": "0001-01-01T00:00:00Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "2018-11-06T10:00:27.245404Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        },
        {
            "id": 112,
            "created_at": "2018-11-07T03:46:16.505716Z",
            "updated_at": "2018-11-07T04:00:12.619461Z",
            "order_number": "",
            "order_date": "2018-10-29T10:23:43Z",
            "customer_code": "",
            "remote_order_id": "1313507118",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "181313507118",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "",
            "delivery_name": "Danny",
            "delivery_street_address": "Jl Biak no 19C\r\nsebelah Bank Permata",
            "delivery_street_address_2": "",
            "delivery_suburb": "Gambir",
            "delivery_city": "Jakarta Pusat",
            "delivery_region": "DKI Jakarta",
            "delivery_post_code": "10150",
            "delivery_country": "Indonesia",
            "delivery_method": "J&T REG",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "expired",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 10000,
            "discount_total": 0,
            "subtotal": 7700,
            "total": 17700,
            "order_status": "cancelled",
            "remarks": "",
            "marketplace_code": "bklp",
            "phone_number": "087867255331",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "0001-01-01T00:00:00Z",
            "accepted_at": "0001-01-01T00:00:00Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "2018-11-07T03:46:16.505639Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        }
    ]
}
```

## Get Unresolved Orders

**Summary:** GetUnresolvedOrders

**Description:** 

### HTTP Request 
`***GET*** /order/unresolved` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| last_id | query | Specific Last id to get information from | No | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "orders": [
        {
            "id": 111,
            "created_at": "2018-11-07T03:46:16.457936Z",
            "updated_at": "2018-11-07T03:46:16.457938Z",
            "order_number": "",
            "order_date": "2018-11-07T03:40:57Z",
            "customer_code": "",
            "remote_order_id": "1362230256",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "181362230256",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "",
            "delivery_name": "Danny",
            "delivery_street_address": "Jl Biak no 19C\r\nsebelah Bank Permata",
            "delivery_street_address_2": "",
            "delivery_suburb": "Gambir",
            "delivery_city": "Jakarta Pusat",
            "delivery_region": "DKI Jakarta",
            "delivery_post_code": "10150",
            "delivery_country": "Indonesia",
            "delivery_method": "JNE REG",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "pending",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 45000,
            "discount_total": 0,
            "subtotal": 2500,
            "total": 47500,
            "order_status": "",
            "remarks": "",
            "marketplace_code": "bklp",
            "phone_number": "087867255331",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "0001-01-01T00:00:00Z",
            "accepted_at": "0001-01-01T00:00:00Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        }
    ]
}
```

## Search Orders

**Summary:** SearchOrders

**Description:** 

### HTTP Request 
`***GET*** /order/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| last_id | query | Specific Last id to get information from | No | integer |
| q | query |  | Yes | string |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "orders": [
        {
            "id": 111,
            "created_at": "2018-11-07T03:46:16.457936Z",
            "updated_at": "2018-11-07T03:46:16.457938Z",
            "order_number": "",
            "order_date": "2018-11-07T03:40:57Z",
            "customer_code": "",
            "remote_order_id": "1362230256",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "181362230256",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "",
            "delivery_name": "Danny",
            "delivery_street_address": "Jl Biak no 19C\r\nsebelah Bank Permata",
            "delivery_street_address_2": "",
            "delivery_suburb": "Gambir",
            "delivery_city": "Jakarta Pusat",
            "delivery_region": "DKI Jakarta",
            "delivery_post_code": "10150",
            "delivery_country": "Indonesia",
            "delivery_method": "JNE REG",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "pending",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 45000,
            "discount_total": 0,
            "subtotal": 2500,
            "total": 47500,
            "order_status": "",
            "remarks": "",
            "marketplace_code": "bklp",
            "phone_number": "087867255331",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "0001-01-01T00:00:00Z",
            "accepted_at": "0001-01-01T00:00:00Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        },
        {
            "id": 59,
            "created_at": "2018-11-06T10:00:26.69154Z",
            "updated_at": "2018-11-09T08:53:09.3207Z",
            "order_number": "",
            "order_date": "2018-11-01T04:50:13Z",
            "customer_code": "",
            "remote_order_id": "111",
            "currency_code": "IDR",
            "exchange_rate": 1,
            "customer_reference": "201800066;Pending;Rp 459",
            "quote_expiry_date": "0001-01-01T00:00:00Z",
            "required_date": "0001-01-01T00:00:00Z",
            "warehouse_code": "",
            "payment_method": "",
            "delivery_name": "",
            "delivery_street_address": "",
            "delivery_street_address_2": "",
            "delivery_suburb": "",
            "delivery_city": "",
            "delivery_region": "",
            "delivery_post_code": "",
            "delivery_country": "",
            "delivery_method": "",
            "delivery_number": "",
            "delivery_method_code": "",
            "delivery_enterprise_code": "",
            "delivery_enterprise_name": "",
            "buyer_delivery_number": "",
            "remote_order_status": "Processing",
            "discount": 0,
            "tax_code": "PPN",
            "tax_rate": 0.1,
            "tax_total": 0,
            "shipping_total": 0,
            "discount_total": 0,
            "subtotal": 0,
            "total": 0,
            "order_status": "pending",
            "remarks": "",
            "marketplace_code": "srcl",
            "phone_number": "",
            "airwaybill_number": "",
            "shipment_reference": "",
            "shipment_extras": "",
            "processed_at": "2018-11-01T04:50:13Z",
            "accepted_at": "0001-01-01T00:00:00Z",
            "packed_at": "0001-01-01T00:00:00Z",
            "cancelled_at": "0001-01-01T00:00:00Z",
            "shipment_tracked_at": "0001-01-01T00:00:00Z",
            "edited_at": "0001-01-01T00:00:00Z",
            "exported_at": "0001-01-01T00:00:00Z",
            "printed_at": "0001-01-01T00:00:00Z",
            "accepted_by": 0,
            "packed_by": 0,
            "cancelled_by": 0,
            "printed_by": 0,
            "line_items": null,
            "store_id": 4,
            "store_name": "",
            "comment": "",
            "price_adjustment": 0,
            "edit_reason": "",
            "cancel_reason": ""
        }
    ]
}
```

## Get Order History 

**Summary:** GetOrderHistory

**Description:** 

### HTTP Request 
`***GET*** /order/{orderID}/history ` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| orderID | path | Specific Order id to get information from | Yes | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "history": [
        {
            "timestamp": "2018-11-09T03:53:16.486142Z",
            "activity_id": "46d2f968-50a4-4974-be7b-2de3459fbd96",
            "action": "import_orders_cron",
            "actor": "system",
            "diff": {
                "OrderDate.loc.name": {
                    "old": "GMT",
                    "new": "Local"
                },
                "OrderDate.loc.zone[0].name": {
                    "old": "GMT",
                    "new": "UTC"
                }
            }
        },
        {
            "timestamp": "2018-11-09T02:00:09.212839Z",
            "activity_id": "5c922118-a204-458b-aecd-7d28a4d31b8c",
            "action": "import_orders_cron",
            "actor": "system",
            "diff": {
                "OrderDate.loc.name": {
                    "old": "GMT",
                    "new": "Local"
                },
                "OrderDate.loc.zone[0].name": {
                    "old": "GMT",
                    "new": "UTC"
                }
            }
        },
        {
            "timestamp": "2018-11-09T02:00:08.129067Z",
            "activity_id": "5c922118-a204-458b-aecd-7d28a4d31b8c",
            "action": "import_orders_cron",
            "actor": "system",
            "diff": {
                "OrderDate.loc.name": {
                    "old": "GMT",
                    "new": "Local"
                },
                "OrderDate.loc.zone[0].name": {
                    "old": "GMT",
                    "new": "UTC"
                }
            }
        }
    ]
}
```

## Get Paged Fetch Order Log

**Summary:** Get Paged Fetch Order Log

### HTTP Request 
`***GET*** /order/fetchorderlog/page/{pageNo}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| perpage | query | Is 10 search result per page | Yes | integer |
| pageNo | path | The Number of the specific page | Yes | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "fetchorderlog": [
        {
            "created_at": "2019-01-16T09:53:46.726555Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        },
        {
            "created_at": "2019-01-16T09:53:46.70026Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        },
        {
            "created_at": "2019-01-16T09:53:46.665463Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        },
        {
            "created_at": "2019-01-16T09:53:46.614791Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        },
        {
            "created_at": "2019-01-16T09:53:46.577527Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        },
        {
            "created_at": "2019-01-16T09:53:46.54533Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        },
        {
            "created_at": "2019-01-16T09:53:46.519414Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        },
        {
            "created_at": "2019-01-16T09:53:46.494376Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        },
        {
            "created_at": "2019-01-16T09:53:46.46311Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        },
        {
            "created_at": "2019-01-16T09:53:46.438451Z",
            "marketplace": "Blibli",
            "api_response": "{\"requestId\":\"\",\"headers\":null,\"errorMessage\":\"Invalid signature\",\"errorCode\":\"401\",\"success\":false,\"value\":null}",
            "store_name": "Angga",
            "activity_id": "77457d67-ed8a-4f8c-a1eb-a48943258fff"
        }
    ],
    "total_count": 40447
}
```

## Get Paged AWB Update LOg

**Summary:** Get Paged Awb Update Log

### HTTP Request 
`***GET*** /order/awbupdatelog/page/{pageNo}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| perpage | query | Is 10 search result per page | Yes | integer |
| pageNo | path | The Number of the specific page | Yes | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "awbupdatelog": [],
    "total_count": 0
}
```

## Get Paged Stock Update Log 

**Summary:** Get Paged Stock Update Log

### HTTP Request 
`***GET*** /order/stockupdatelog/page/{pageNo}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| perpage | query | Is 10 search result per page | Yes | integer |
| pageNo | path | The Number of the specific page | Yes | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "stockupdatelog": [
        {
            "sku": "BZIC113",
            "created_at": "2019-01-16T08:04:40.54828Z",
            "marketplace": "Blibli",
            "api_response": "{\n \"requestId\": \"59c70507-8f6e-4a7c-b364-026c030695bb\",\n \"errorMessage\": \"\",\n \"errorCode\": \"\",\n \"success\": true\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        },
        {
            "sku": "SKU-CD7C02C2E32C353B697F3AADF2259ADD",
            "created_at": "2019-01-16T08:04:39.594803Z",
            "marketplace": "Lazada",
            "api_response": "{\n \"type\": \"ISP\",\n \"code\": \"501\",\n \"detail\": [\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA12VAR1\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"72172422\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"A08940006535\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testfree003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom0001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun002\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA24VAR2\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"11433364\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"10080107\"\n  }\n ]\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        },
        {
            "sku": "10080107",
            "created_at": "2019-01-16T08:04:39.594798Z",
            "marketplace": "Lazada",
            "api_response": "{\n \"type\": \"ISP\",\n \"code\": \"501\",\n \"detail\": [\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA12VAR1\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"72172422\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"A08940006535\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testfree003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom0001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun002\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA24VAR2\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"11433364\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"10080107\"\n  }\n ]\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        },
        {
            "sku": "NK33103G",
            "created_at": "2019-01-16T08:04:39.594793Z",
            "marketplace": "Lazada",
            "api_response": "{\n \"type\": \"ISP\",\n \"code\": \"501\",\n \"detail\": [\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA12VAR1\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"72172422\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"A08940006535\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testfree003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom0001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun002\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA24VAR2\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"11433364\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"10080107\"\n  }\n ]\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        },
        {
            "sku": "testbun003",
            "created_at": "2019-01-16T08:04:39.594787Z",
            "marketplace": "Lazada",
            "api_response": "{\n \"type\": \"ISP\",\n \"code\": \"501\",\n \"detail\": [\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA12VAR1\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"72172422\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"A08940006535\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testfree003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom0001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun002\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA24VAR2\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"11433364\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"10080107\"\n  }\n ]\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        },
        {
            "sku": "11433364",
            "created_at": "2019-01-16T08:04:39.594782Z",
            "marketplace": "Lazada",
            "api_response": "{\n \"type\": \"ISP\",\n \"code\": \"501\",\n \"detail\": [\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA12VAR1\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"72172422\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"A08940006535\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testfree003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom0001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun002\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA24VAR2\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"11433364\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"10080107\"\n  }\n ]\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        },
        {
            "sku": "ZPRDLAZADA24VAR2",
            "created_at": "2019-01-16T08:04:39.594776Z",
            "marketplace": "Lazada",
            "api_response": "{\n \"type\": \"ISP\",\n \"code\": \"501\",\n \"detail\": [\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA12VAR1\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"72172422\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"A08940006535\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testfree003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom0001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun002\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA24VAR2\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"11433364\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"10080107\"\n  }\n ]\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        },
        {
            "sku": "testbun002",
            "created_at": "2019-01-16T08:04:39.59477Z",
            "marketplace": "Lazada",
            "api_response": "{\n \"type\": \"ISP\",\n \"code\": \"501\",\n \"detail\": [\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA12VAR1\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"72172422\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"A08940006535\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testfree003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom0001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun002\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA24VAR2\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"11433364\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"10080107\"\n  }\n ]\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        },
        {
            "sku": "testcom001",
            "created_at": "2019-01-16T08:04:39.594765Z",
            "marketplace": "Lazada",
            "api_response": "{\n \"type\": \"ISP\",\n \"code\": \"501\",\n \"detail\": [\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA12VAR1\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"72172422\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"A08940006535\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testfree003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom0001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun002\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA24VAR2\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"11433364\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"10080107\"\n  }\n ]\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        },
        {
            "sku": "testcom0001",
            "created_at": "2019-01-16T08:04:39.594759Z",
            "marketplace": "Lazada",
            "api_response": "{\n \"type\": \"ISP\",\n \"code\": \"501\",\n \"detail\": [\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA12VAR1\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"72172422\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"A08940006535\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testfree003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom0001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testcom001\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun002\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"ZPRDLAZADA24VAR2\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"11433364\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"testbun003\"\n  },\n  {\n   \"message\": \"SELLER_SKU_NOT_FOUND\",\n   \"seller_sku\": \"10080107\"\n  }\n ]\n}",
            "store_name": "Angga",
            "activity_id": "d0bc10e6-277a-40ca-bd5e-857875764e99"
        }
    ],
    "total_count": 9102
}
```

## Get Paged Accept Sales Order Log

**Summary:** Get Paged Accept Sales Order Log

### HTTP Request 
`***GET*** /order/acceptorderlog/page/{pageNo}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Authorization | header | Access token to access this API | Yes | string |
| perpage | query | Is 10 search result per page | Yes | integer |
| pageNo | path | The Number of the specific page | Yes | integer |

**Responses**

> The above command returns JSON structured like this:

```json
{
    "acceptorderlog": [
        {
            "customer_reference": "201900003",
            "created_at": "2019-01-10T06:07:23.255596Z",
            "marketplace": "SIRCLO",
            "api_response": "<!DOCTYPE html>\n<html style=\"height:100%;margin:0;padding:0;\">\n\t<head>\n\t\t<title>Under Maintenance</title>\n\t</head>\n\n\t<body style=\"height:100%;margin:0;padding:0;\">\n\t\t<img src=\"https://files.sirclocdn.xyz/sirclo/files/under_maintenance.png\" alt=\"Under Maintenance\" style=\"display:block;margin:0 auto;max-width:100%;max-height:100%;padding:0;\" />\n\t</body>\n</html>\n",
            "store_name": "Angga",
            "activity_id": "dbf551e8-99a0-43bc-b96d-efaaac432364"
        }
    ],
    "total_count": 1
}
```

#Logistix API 

## Create AWB
**Summary: Create Airwaybill Logistix**

### HTTP Request 
`***POST*** /createAWB` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| api_key| header | This api key provide by us | Yes | string |
| request_tag | header | Unique identifier for log purposes | Yes | string |
| body Parameters| body | No Description| Yes |  |

> Body Parameters

```json
{
    "user_id":"2",
    "order_id":"2",
    "sender_name":"warehouse",
    "sender_address":"Taman Tekno BSD Blok D2, Setu, South Tangerang City, Banten",
    "sender_location_code":"ID-BT0411",
    "sender_post_code":"15314",
    "receiver_name":"GOP 6",
    "receiver_phone":"0821177066",
    "receiver_address":"My Republic Plaza (GOP6), level 3, Wing A, Zone 1-2, Jl.BSD Green Office Park, Sampora, Cisauk, Tangerang - Banten",
    "receiver_location_code":"ID-BT0403",
    "receiver_post_code":"15345",
    "package_weight":"1",
    "package_width":"20",
    "package_height":"30",
    "package_lenght":"20",
    "description":"b3d76245-5b8e-4748-a286-9b900940ff6b"
}
```

**Responses**

> The above command returns JSON structured like this:

```json
{
    "awb_number":"PH089AD97",
    "courier_code": "JN01",
    "estimated_cost":"19.000"
}
```

## Get Location

**Summary: Get Province and SUbdistrict**

### HTTP Request 
`***GET*** /location/srcl`


**Responses**

> The above command returns JSON structured like this:

```json
{
    "locations": [
        {
            "location_code": "ID",
            "provider_data": "INDONESIA",
            "provinces": [
                {
                    "location_code": "ID-AC",
                    "provider_data": "NANGGROE ACEH DARUSSALAM (NAD)",
                    "cities": [
                        {
                            "location_code": "ID-AC01",
                            "provider_data": "ACEH BARAT",
                            "districts": [
                                {
                                    "location_code": "ID-AC0101",
                                    "provider_data": "ACEH BARAT-ARONGAN LAMBALEK"
                                },
                                {
                                    "location_code": "ID-AC0102",
                                    "provider_data": "ACEH BARAT-BUBON"
                                },
                                {
                                    "location_code": "ID-AC0103",
                                    "provider_data": "ACEH BARAT-JOHAN PAHLAWAN"
                                },
                                {
                                    "location_code": "ID-AC0104",
                                    "provider_data": "ACEH BARAT-KAWAY XVI"
                                },
                                {
                                    "location_code": "ID-AC0105",
                                    "provider_data": "ACEH BARAT-MEUREUBO"
                                },
                                {
                                    "location_code": "ID-AC0106",
                                    "provider_data": "ACEH BARAT-PANTE CEUREUMEN (PANTAI CEUREMEN)"
                                },
                                {
                                    "location_code": "ID-AC0107",
                                    "provider_data": "ACEH BARAT-PANTON REU"
                                },
                                {
                                    "location_code": "ID-AC0108",
                                    "provider_data": "ACEH BARAT-SAMATIGA"
                                },
                                {
                                    "location_code": "ID-AC0109",
                                    "provider_data": "ACEH BARAT-SUNGAI MAS"
                                },
                                {
                                    "location_code": "ID-AC010A",
                                    "provider_data": "ACEH BARAT-WOYLA"
                                },
                                {
                                    "location_code": "ID-AC010B",
                                    "provider_data": "ACEH BARAT-WOYLA BARAT"
                                },
                                {
                                    "location_code": "ID-AC010C",
                                    "provider_data": "ACEH BARAT-WOYLA TIMUR"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC02",
                            "provider_data": "ACEH BARAT DAYA",
                            "districts": [
                                {
                                    "location_code": "ID-AC0201",
                                    "provider_data": "ACEH BARAT DAYA-BABAH ROT"
                                },
                                {
                                    "location_code": "ID-AC0202",
                                    "provider_data": "ACEH BARAT DAYA-BLANG PIDIE"
                                },
                                {
                                    "location_code": "ID-AC0203",
                                    "provider_data": "ACEH BARAT DAYA-JEUMPA"
                                },
                                {
                                    "location_code": "ID-AC0204",
                                    "provider_data": "ACEH BARAT DAYA-KUALA BATEE"
                                },
                                {
                                    "location_code": "ID-AC0205",
                                    "provider_data": "ACEH BARAT DAYA-LEMBAH SABIL"
                                },
                                {
                                    "location_code": "ID-AC0206",
                                    "provider_data": "ACEH BARAT DAYA-MANGGENG"
                                },
                                {
                                    "location_code": "ID-AC0207",
                                    "provider_data": "ACEH BARAT DAYA-SETIA"
                                },
                                {
                                    "location_code": "ID-AC0208",
                                    "provider_data": "ACEH BARAT DAYA-SUSOH"
                                },
                                {
                                    "location_code": "ID-AC0209",
                                    "provider_data": "ACEH BARAT DAYA-TANGAN-TANGAN"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC03",
                            "provider_data": "ACEH BESAR",
                            "districts": [
                                {
                                    "location_code": "ID-AC0301",
                                    "provider_data": "ACEH BESAR-BAITUSSALAM"
                                },
                                {
                                    "location_code": "ID-AC0302",
                                    "provider_data": "ACEH BESAR-BLANK BINTANG"
                                },
                                {
                                    "location_code": "ID-AC0303",
                                    "provider_data": "ACEH BESAR-DARUL IMARAH"
                                },
                                {
                                    "location_code": "ID-AC0304",
                                    "provider_data": "ACEH BESAR-DARUL KAMAL"
                                },
                                {
                                    "location_code": "ID-AC0305",
                                    "provider_data": "ACEH BESAR-DARUSSALAM"
                                },
                                {
                                    "location_code": "ID-AC0306",
                                    "provider_data": "ACEH BESAR-INDRAPURI"
                                },
                                {
                                    "location_code": "ID-AC0307",
                                    "provider_data": "ACEH BESAR-INGIN JAYA"
                                },
                                {
                                    "location_code": "ID-AC0308",
                                    "provider_data": "ACEH BESAR-KOTA COT GLIE (KUTA COT GLIE)"
                                },
                                {
                                    "location_code": "ID-AC0309",
                                    "provider_data": "ACEH BESAR-KOTA JANTHO"
                                },
                                {
                                    "location_code": "ID-AC030A",
                                    "provider_data": "ACEH BESAR-KOTA MALAKA (KUTA MALAKA)"
                                },
                                {
                                    "location_code": "ID-AC030B",
                                    "provider_data": "ACEH BESAR-KRUENG BARONA JAYA"
                                },
                                {
                                    "location_code": "ID-AC030C",
                                    "provider_data": "ACEH BESAR-KUTA BARO"
                                },
                                {
                                    "location_code": "ID-AC030D",
                                    "provider_data": "ACEH BESAR-LEMBAH SEULAWAH"
                                },
                                {
                                    "location_code": "ID-AC030E",
                                    "provider_data": "ACEH BESAR-LEUPUNG"
                                },
                                {
                                    "location_code": "ID-AC030F",
                                    "provider_data": "ACEH BESAR-LHOKNGA (LHO’’NGA)"
                                },
                                {
                                    "location_code": "ID-AC0310",
                                    "provider_data": "ACEH BESAR-LHOONG"
                                },
                                {
                                    "location_code": "ID-AC0311",
                                    "provider_data": "ACEH BESAR-MANTASIEK (MONTASIK)"
                                },
                                {
                                    "location_code": "ID-AC0312",
                                    "provider_data": "ACEH BESAR-MESJID RAYA"
                                },
                                {
                                    "location_code": "ID-AC0313",
                                    "provider_data": "ACEH BESAR-PEUKAN BADA"
                                },
                                {
                                    "location_code": "ID-AC0314",
                                    "provider_data": "ACEH BESAR-PULO ACEH"
                                },
                                {
                                    "location_code": "ID-AC0315",
                                    "provider_data": "ACEH BESAR-SEULIMEUM"
                                },
                                {
                                    "location_code": "ID-AC0316",
                                    "provider_data": "ACEH BESAR-SIMPANG TIGA"
                                },
                                {
                                    "location_code": "ID-AC0317",
                                    "provider_data": "ACEH BESAR-SUKA MAKMUR"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC04",
                            "provider_data": "ACEH JAYA",
                            "districts": [
                                {
                                    "location_code": "ID-AC0401",
                                    "provider_data": "ACEH JAYA-DARUL HIKMAH"
                                },
                                {
                                    "location_code": "ID-AC0402",
                                    "provider_data": "ACEH JAYA-INDRA JAYA"
                                },
                                {
                                    "location_code": "ID-AC0403",
                                    "provider_data": "ACEH JAYA-JAYA"
                                },
                                {
                                    "location_code": "ID-AC0404",
                                    "provider_data": "ACEH JAYA-KEUDE PANGA"
                                },
                                {
                                    "location_code": "ID-AC0405",
                                    "provider_data": "ACEH JAYA-KRUENG SABEE"
                                },
                                {
                                    "location_code": "ID-AC0406",
                                    "provider_data": "ACEH JAYA-PASIE RAYA"
                                },
                                {
                                    "location_code": "ID-AC0407",
                                    "provider_data": "ACEH JAYA-SAMPOINIET"
                                },
                                {
                                    "location_code": "ID-AC0408",
                                    "provider_data": "ACEH JAYA-SETIA BAKTI"
                                },
                                {
                                    "location_code": "ID-AC0409",
                                    "provider_data": "ACEH JAYA-TEUNOM"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC05",
                            "provider_data": "ACEH SELATAN",
                            "districts": [
                                {
                                    "location_code": "ID-AC0501",
                                    "provider_data": "ACEH SELATAN-BAKONGAN"
                                },
                                {
                                    "location_code": "ID-AC0502",
                                    "provider_data": "ACEH SELATAN-BAKONGAN TIMUR"
                                },
                                {
                                    "location_code": "ID-AC0503",
                                    "provider_data": "ACEH SELATAN-KLUET SELATAN"
                                },
                                {
                                    "location_code": "ID-AC0504",
                                    "provider_data": "ACEH SELATAN-KLUET TENGAH"
                                },
                                {
                                    "location_code": "ID-AC0505",
                                    "provider_data": "ACEH SELATAN-KLUET TIMUR"
                                },
                                {
                                    "location_code": "ID-AC0506",
                                    "provider_data": "ACEH SELATAN-KLUET UTARA"
                                },
                                {
                                    "location_code": "ID-AC0507",
                                    "provider_data": "ACEH SELATAN-KOTA BAHAGIA"
                                },
                                {
                                    "location_code": "ID-AC0508",
                                    "provider_data": "ACEH SELATAN-LABUHAN HAJI"
                                },
                                {
                                    "location_code": "ID-AC0509",
                                    "provider_data": "ACEH SELATAN-LABUHAN HAJI BARAT"
                                },
                                {
                                    "location_code": "ID-AC050A",
                                    "provider_data": "ACEH SELATAN-LABUHAN HAJI TIMUR"
                                },
                                {
                                    "location_code": "ID-AC050B",
                                    "provider_data": "ACEH SELATAN-MEUKEK"
                                },
                                {
                                    "location_code": "ID-AC050C",
                                    "provider_data": "ACEH SELATAN-PASIE RAJA"
                                },
                                {
                                    "location_code": "ID-AC050D",
                                    "provider_data": "ACEH SELATAN-SAMA DUA"
                                },
                                {
                                    "location_code": "ID-AC050E",
                                    "provider_data": "ACEH SELATAN-SAWANG"
                                },
                                {
                                    "location_code": "ID-AC050F",
                                    "provider_data": "ACEH SELATAN-TAPAK TUAN"
                                },
                                {
                                    "location_code": "ID-AC0510",
                                    "provider_data": "ACEH SELATAN-TRUMON"
                                },
                                {
                                    "location_code": "ID-AC0511",
                                    "provider_data": "ACEH SELATAN-TRUMON TENGAH"
                                },
                                {
                                    "location_code": "ID-AC0512",
                                    "provider_data": "ACEH SELATAN-TRUMON TIMUR"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC06",
                            "provider_data": "ACEH SINGKIL",
                            "districts": [
                                {
                                    "location_code": "ID-AC0601",
                                    "provider_data": "ACEH SINGKIL-DANAU PARIS"
                                },
                                {
                                    "location_code": "ID-AC0602",
                                    "provider_data": "ACEH SINGKIL-GUNUNG MERIAH (MARIAH)"
                                },
                                {
                                    "location_code": "ID-AC0603",
                                    "provider_data": "ACEH SINGKIL-KOTA BAHARU"
                                },
                                {
                                    "location_code": "ID-AC0604",
                                    "provider_data": "ACEH SINGKIL-KUALA BARU"
                                },
                                {
                                    "location_code": "ID-AC0605",
                                    "provider_data": "ACEH SINGKIL-PULAU BANYAK"
                                },
                                {
                                    "location_code": "ID-AC0606",
                                    "provider_data": "ACEH SINGKIL-PULAU BANYAK BARAT"
                                },
                                {
                                    "location_code": "ID-AC0607",
                                    "provider_data": "ACEH SINGKIL-SIMPANG KANAN"
                                },
                                {
                                    "location_code": "ID-AC0608",
                                    "provider_data": "ACEH SINGKIL-SINGKIL"
                                },
                                {
                                    "location_code": "ID-AC0609",
                                    "provider_data": "ACEH SINGKIL-SINGKIL UTARA"
                                },
                                {
                                    "location_code": "ID-AC060A",
                                    "provider_data": "ACEH SINGKIL-SINGKOHOR"
                                },
                                {
                                    "location_code": "ID-AC060B",
                                    "provider_data": "ACEH SINGKIL-SURO MAKMUR"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC07",
                            "provider_data": "ACEH TAMIANG",
                            "districts": [
                                {
                                    "location_code": "ID-AC0701",
                                    "provider_data": "ACEH TAMIANG-BANDA MULIA"
                                },
                                {
                                    "location_code": "ID-AC0702",
                                    "provider_data": "ACEH TAMIANG-BANDAR PUSAKA"
                                },
                                {
                                    "location_code": "ID-AC0703",
                                    "provider_data": "ACEH TAMIANG-BENDAHARA"
                                },
                                {
                                    "location_code": "ID-AC0704",
                                    "provider_data": "ACEH TAMIANG-KARANG BARU"
                                },
                                {
                                    "location_code": "ID-AC0705",
                                    "provider_data": "ACEH TAMIANG-KEJURUAN MUDA"
                                },
                                {
                                    "location_code": "ID-AC0706",
                                    "provider_data": "ACEH TAMIANG-KOTA KUALA SIMPANG"
                                },
                                {
                                    "location_code": "ID-AC0707",
                                    "provider_data": "ACEH TAMIANG-MANYAK PAYED"
                                },
                                {
                                    "location_code": "ID-AC0708",
                                    "provider_data": "ACEH TAMIANG-RANTAU"
                                },
                                {
                                    "location_code": "ID-AC0709",
                                    "provider_data": "ACEH TAMIANG-SEKERAK"
                                },
                                {
                                    "location_code": "ID-AC070A",
                                    "provider_data": "ACEH TAMIANG-SERUWAY"
                                },
                                {
                                    "location_code": "ID-AC070B",
                                    "provider_data": "ACEH TAMIANG-TAMIANG HULU"
                                },
                                {
                                    "location_code": "ID-AC070C",
                                    "provider_data": "ACEH TAMIANG-TENGGULUN"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC08",
                            "provider_data": "ACEH TENGAH",
                            "districts": [
                                {
                                    "location_code": "ID-AC0801",
                                    "provider_data": "ACEH TENGAH-ATU LINTANG"
                                },
                                {
                                    "location_code": "ID-AC0802",
                                    "provider_data": "ACEH TENGAH-BEBESEN"
                                },
                                {
                                    "location_code": "ID-AC0803",
                                    "provider_data": "ACEH TENGAH-BIES"
                                },
                                {
                                    "location_code": "ID-AC0804",
                                    "provider_data": "ACEH TENGAH-BINTANG"
                                },
                                {
                                    "location_code": "ID-AC0805",
                                    "provider_data": "ACEH TENGAH-CELALA"
                                },
                                {
                                    "location_code": "ID-AC0806",
                                    "provider_data": "ACEH TENGAH-JAGONG JEGET"
                                },
                                {
                                    "location_code": "ID-AC0807",
                                    "provider_data": "ACEH TENGAH-KEBAYAKAN"
                                },
                                {
                                    "location_code": "ID-AC0808",
                                    "provider_data": "ACEH TENGAH-KETOL"
                                },
                                {
                                    "location_code": "ID-AC0809",
                                    "provider_data": "ACEH TENGAH-KUTE PANANG"
                                },
                                {
                                    "location_code": "ID-AC080A",
                                    "provider_data": "ACEH TENGAH-LINGE"
                                },
                                {
                                    "location_code": "ID-AC080B",
                                    "provider_data": "ACEH TENGAH-LUT TAWAR"
                                },
                                {
                                    "location_code": "ID-AC080C",
                                    "provider_data": "ACEH TENGAH-PEGASING"
                                },
                                {
                                    "location_code": "ID-AC080D",
                                    "provider_data": "ACEH TENGAH-RUSIP ANTARA"
                                },
                                {
                                    "location_code": "ID-AC080E",
                                    "provider_data": "ACEH TENGAH-SILIH NARA"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC09",
                            "provider_data": "ACEH TENGGARA",
                            "districts": [
                                {
                                    "location_code": "ID-AC0901",
                                    "provider_data": "ACEH TENGGARA-BABUL MAKMUR"
                                },
                                {
                                    "location_code": "ID-AC0902",
                                    "provider_data": "ACEH TENGGARA-BABUL RAHMAH"
                                },
                                {
                                    "location_code": "ID-AC0903",
                                    "provider_data": "ACEH TENGGARA-BABUSSALAM"
                                },
                                {
                                    "location_code": "ID-AC0904",
                                    "provider_data": "ACEH TENGGARA-BADAR"
                                },
                                {
                                    "location_code": "ID-AC0905",
                                    "provider_data": "ACEH TENGGARA-BAMBEL"
                                },
                                {
                                    "location_code": "ID-AC0906",
                                    "provider_data": "ACEH TENGGARA-BUKIT TUSAM"
                                },
                                {
                                    "location_code": "ID-AC0907",
                                    "provider_data": "ACEH TENGGARA-DARUL HASANAH"
                                },
                                {
                                    "location_code": "ID-AC0908",
                                    "provider_data": "ACEH TENGGARA-DELENG POKHISEN"
                                },
                                {
                                    "location_code": "ID-AC0909",
                                    "provider_data": "ACEH TENGGARA-KETAMBE"
                                },
                                {
                                    "location_code": "ID-AC090A",
                                    "provider_data": "ACEH TENGGARA-LAWE ALAS"
                                },
                                {
                                    "location_code": "ID-AC090B",
                                    "provider_data": "ACEH TENGGARA-LAWE BULAN"
                                },
                                {
                                    "location_code": "ID-AC090C",
                                    "provider_data": "ACEH TENGGARA-LAWE SIGALA-GALA"
                                },
                                {
                                    "location_code": "ID-AC090D",
                                    "provider_data": "ACEH TENGGARA-LAWE SUMUR"
                                },
                                {
                                    "location_code": "ID-AC090E",
                                    "provider_data": "ACEH TENGGARA-LEUSER"
                                },
                                {
                                    "location_code": "ID-AC090F",
                                    "provider_data": "ACEH TENGGARA-SEMADAM"
                                },
                                {
                                    "location_code": "ID-AC0910",
                                    "provider_data": "ACEH TENGGARA-TANAH ALAS"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC0A",
                            "provider_data": "ACEH TIMUR",
                            "districts": [
                                {
                                    "location_code": "ID-AC0A01",
                                    "provider_data": "ACEH TIMUR-BANDA ALAM"
                                },
                                {
                                    "location_code": "ID-AC0A02",
                                    "provider_data": "ACEH TIMUR-BIREM BAYEUN"
                                },
                                {
                                    "location_code": "ID-AC0A03",
                                    "provider_data": "ACEH TIMUR-DARUL AMAN"
                                },
                                {
                                    "location_code": "ID-AC0A04",
                                    "provider_data": "ACEH TIMUR-DARUL FALAH"
                                },
                                {
                                    "location_code": "ID-AC0A05",
                                    "provider_data": "ACEH TIMUR-DARUL IKSAN (IHSAN)"
                                },
                                {
                                    "location_code": "ID-AC0A06",
                                    "provider_data": "ACEH TIMUR-IDI RAYEUK"
                                },
                                {
                                    "location_code": "ID-AC0A07",
                                    "provider_data": "ACEH TIMUR-IDI TIMUR"
                                },
                                {
                                    "location_code": "ID-AC0A08",
                                    "provider_data": "ACEH TIMUR-IDI TUNONG"
                                },
                                {
                                    "location_code": "ID-AC0A09",
                                    "provider_data": "ACEH TIMUR-INDRA MAKMUR"
                                },
                                {
                                    "location_code": "ID-AC0A0A",
                                    "provider_data": "ACEH TIMUR-JULOK"
                                },
                                {
                                    "location_code": "ID-AC0A0B",
                                    "provider_data": "ACEH TIMUR-MADAT"
                                },
                                {
                                    "location_code": "ID-AC0A0C",
                                    "provider_data": "ACEH TIMUR-NURUSSALAM"
                                },
                                {
                                    "location_code": "ID-AC0A0D",
                                    "provider_data": "ACEH TIMUR-PANTE BIDARI (BEUDARI)"
                                },
                                {
                                    "location_code": "ID-AC0A0E",
                                    "provider_data": "ACEH TIMUR-PEUDAWA"
                                },
                                {
                                    "location_code": "ID-AC0A0F",
                                    "provider_data": "ACEH TIMUR-PEUNARON"
                                },
                                {
                                    "location_code": "ID-AC0A10",
                                    "provider_data": "ACEH TIMUR-PEUREULAK"
                                },
                                {
                                    "location_code": "ID-AC0A11",
                                    "provider_data": "ACEH TIMUR-PEUREULAK BARAT"
                                },
                                {
                                    "location_code": "ID-AC0A12",
                                    "provider_data": "ACEH TIMUR-PEUREULAK TIMUR"
                                },
                                {
                                    "location_code": "ID-AC0A13",
                                    "provider_data": "ACEH TIMUR-RANTAU SELAMAT"
                                },
                                {
                                    "location_code": "ID-AC0A14",
                                    "provider_data": "ACEH TIMUR-RANTO PEUREULAK"
                                },
                                {
                                    "location_code": "ID-AC0A15",
                                    "provider_data": "ACEH TIMUR-SERBA JADI"
                                },
                                {
                                    "location_code": "ID-AC0A16",
                                    "provider_data": "ACEH TIMUR-SIMPANG JERNIH"
                                },
                                {
                                    "location_code": "ID-AC0A17",
                                    "provider_data": "ACEH TIMUR-SIMPANG ULIM"
                                },
                                {
                                    "location_code": "ID-AC0A18",
                                    "provider_data": "ACEH TIMUR-SUNGAI RAYA"
                                }
                            ]
                        },
                        {
                            "location_code": "ID-AC0B",
                            "provider_data": "ACEH UTARA",
                            "districts": [
                                {
                                    "location_code": "ID-AC0B01",
                                    "provider_data": "ACEH UTARA-BAKTIYA"
                                },
                                {
                                    "location_code": "ID-AC0B02",
                                    "provider_data": "ACEH UTARA-BAKTIYA BARAT"
                                },
                                {
                                    "location_code": "ID-AC0B03",
                                    "provider_data": "ACEH UTARA-BANDA BARO"
                                },
                                {
                                    "location_code": "ID-AC0B04",
                                    "provider_data": "ACEH UTARA-COT GIREK"
                                },
                                {
                                    "location_code": "ID-AC0B05",
                                    "provider_data": "ACEH UTARA-DEWANTARA"
                                },
                                {
                                    "location_code": "ID-AC0B06",
                                    "provider_data": "ACEH UTARA-GEUREDONG PASE"
                                },
                                {
                                    "location_code": "ID-AC0B07",
                                    "provider_data": "ACEH UTARA-KUTA MAKMUR"
                                },
                                {
                                    "location_code": "ID-AC0B08",
                                    "provider_data": "ACEH UTARA-LANGKAHAN"
                                },
                                {
                                    "location_code": "ID-AC0B09",
                                    "provider_data": "ACEH UTARA-LAPANG"
                                },
                                {
                                    "location_code": "ID-AC0B0A",
                                    "provider_data": "ACEH UTARA-LHOKSUKON"
                                },
                                {
                                    "location_code": "ID-AC0B0B",
                                    "provider_data": "ACEH UTARA-MATANGKULI"
                                },
                                {
                                    "location_code": "ID-AC0B0C",
                                    "provider_data": "ACEH UTARA-MEURAH MULIA"
                                },
                                {
                                    "location_code": "ID-AC0B0D",
                                    "provider_data": "ACEH UTARA-MUARA BATU"
                                },
                                {
                                    "location_code": "ID-AC0B0E",
                                    "provider_data": "ACEH UTARA-NIBONG"
                                },
                                {
                                    "location_code": "ID-AC0B0F",
                                    "provider_data": "ACEH UTARA-NISAM"
                                },
                                {
                                    "location_code": "ID-AC0B10",
                                    "provider_data": "ACEH UTARA-NISAM ANTARA"
                                },
                                {
                                    "location_code": "ID-AC0B11",
                                    "provider_data": "ACEH UTARA-PAYA BAKONG"
                                },
                                {
                                    "location_code": "ID-AC0B12",
                                    "provider_data": "ACEH UTARA-PIRAK TIMUR"
                                },
                                {
                                    "location_code": "ID-AC0B13",
                                    "provider_data": "ACEH UTARA-SAMUDERA"
                                },
                                {
                                    "location_code": "ID-AC0B14",
                                    "provider_data": "ACEH UTARA-SAWANG"
                                },
                                {
                                    "location_code": "ID-AC0B15",
                                    "provider_data": "ACEH UTARA-SEUNUDDON (SEUNUDON)"
                                },
                                {
                                    "location_code": "ID-AC0B16",
                                    "provider_data": "ACEH UTARA-SIMPANG KRAMAT (KERAMAT)"
                                },
                                {
                                    "location_code": "ID-AC0B17",
                                    "provider_data": "ACEH UTARA-SYAMTALIRA ARON"
                                },
                                {
                                    "location_code": "ID-AC0B18",
                                    "provider_data": "ACEH UTARA-SYAMTALIRA BAYU"
                                },
                                {
                                    "location_code": "ID-AC0B19",
                                    "provider_data": "ACEH UTARA-TANAH JAMBO AYE"
                                },
                                {
                                    "location_code": "ID-AC0B1A",
                                    "provider_data": "ACEH UTARA-TANAH LUAS"
                                },
                                {
                                    "location_code": "ID-AC0B1B",
                                    "provider_data": "ACEH UTARA-TANAH PASIR"
                                }
                            ]
                        },
```

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
