# Goods Received Note

### HTTP Request

`POST /klog/v1/operation/grn`

### Bookings - Request Body Parameters

| Section | Node   | Subnode  | Description | Map to Odoo | Expected Value | Required | 
| ----- | ------| ------| ---------------------------------| ------------------ | ----| --- | 
| basic details| bookingNo || BookingNo (BookingNo as specified by Inbound/Outbound Booking)|Booking No |Alphanumeric| Yes | 
| | Timestamp |  | Format = ISO8601, in UTC (eg: 2020-05-26T10:24:46Z for May 26 at 10:24:46 AM) | GRN datetime| Alphanumeric| Yes|
||messageId||unique number to identify integration message| Generate UUID (Universally Unique Indentifier) |UUID (Universally Unique Identifier) | Yes|
| | action | | Action for API call , Add, Edit | fixed | Add | Yes
| [Loop] products|productCode| |Product Code from ODOO (Group by Product code, Sum(Qty),UOM, Status,DamageReasoncode)|Product Code|Alphanumeric|Yes
||quantity|values|Product Quantity from ODOO| Product Quantity | Numeric | Yes
|||uom|Product UOM|Product booking UOM|Text | Yes
||status||Product Status|Product Status|Normal/Damage|
||reason ||Damage Reason code|Product Damage Reason Code|


> Request body example:

```json
{
  "basicDetails": {
    "bookingNo": "20200811_081455_budi",
    "timestamp": "2020-11-18T09:44:53.136Z",
    "messageId": "62h9af40-c52a-4b20-7b3a-ac5c007f9668"
  },
  "products": [
    {
      "productCode": "ENESS0318-8992772265041",
      "quantity": {
        "value": 10,
        "uom": "Pcs"
      },
      "status": "Normal",
      "reason": "Pcs"
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
