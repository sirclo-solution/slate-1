# Good Issued

### HTTP Request

`POST /klog/v1/operation/gi`

### Request Body Parameters

Request body must be a JSON document with the following properties

| Section | Node   | Subnode  | Description | Map to Odoo | Expected Value | Required | 
| ----- | ------| ------| ---------------------------------| ------------------ | ----| --- | 
| basic details|bookingNo||Booking No (BookingNo as specified by Inbound/Outbound Booking) |*sale_id.partner_id.name + sale_id.client_order_ref*, **Suggested pattern:** *{partner_name}-{client_order_ref}* (Masing2 bagian hanya mengandung karakter alfanumerik (alfabet atau angka) tanpa karakter lainnya.)|Alphanumeric| Yes | 
| | timestamp |  | Format = ISO8601, in UTC (eg: 2020-05-26T10:24:46Z for May 26 at 10:24:46 AM) | x_module_status_updated_timestamp ( Not Exist )| Alphanumeric| Yes|
||AWB||Airway bill no |AWB Number |Alphanumeric | Yes
||messageId||unique number to identify integration message| Generate UUID (Universally Unique Indentifier) |UUID (Universally Unique Identifier) | Yes|
||action||Action for API call , Add, Edit||Add | Yes
| [Loop] products|productCode||Product Code from ODOO|stock_move.product_id.barcode| Alphanumeric|Yes
||quantity|value |Product Quantity from ODOO|Product Qty|Numeric |Yes
|||uom|Product UOM|Order UOM|Text |Yes


> Request body example:

```json
{
  "basicDetails": {
    "bookingNo": "20200811_081455_budi",
    "timestamp": "2020-11-19T04:44:53.002Z",
    "awb": "AWBTEST",
    "messageId": "32a9de58-c62a-4b20-8b3a-ac5c007f9448"
  },
  "products": [
    {
      "productCode": "ENESS0318-8992772265041",
      "quantity": {
        "value": 10,
        "uom": "Pcs"
      }
    }
  ]
}
```

### Responses 

|Code| Description 
|----|---------------------
| 200| Request acknowledged 


> The above request returns JSON structured like this:

```json
{"200" : "Request acknowledged"}
```
