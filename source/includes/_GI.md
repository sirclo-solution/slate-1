# Good Issued

### HTTP Request

`POST /operation/gi`

## Request Body Parameters 

Request body must be a JSON document with the following properties

| Section | Node   | Subnode  | Description | Expected Value | Required 
| ----- | ------| ------| ------------------ | ----| --- | 
| basic details|bookingNo||Booking No (BookingNo as specified by Inbound/Outbound Booking) | Alphanumeric| Yes | 
| | timestamp |  | Format = ISO8601, in UTC (eg: 2020-05-26T10:24:46Z for May 26 at 10:24:46 AM) |  Alphanumeric| Yes|
||AWB||Airway bill no |Alphanumeric | Yes
||messageId||unique## Outbound Request Body Parameters  number to identify integration message| UUID (Universally Unique Identifier) | Yes|
| [Loop] products|productCode||Product SKU from ODOO| Alphanumeric|Yes
||quantity|value |Product Quantity from ODOO| Numeric |Yes
|||uom|Product UOM|Text |Yes


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
